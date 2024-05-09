#aws #saa #services 

### 什麼是 EC2
虛擬伺服器 EC2 ，
需要伺服器來執行服務時，可節省內部部署的高成本高時間。

### AWS 負責
1. 建置資料中心
2. 保護資料中心
3. 購買伺服器
4. 安裝伺服器

### EC2 特色
1. 只需要購買EC2，隨時可以停止，按實際用量付費
2. AWS 透過 hypervison負責虛擬機之間分享基礎實體資源，共用機主設施 多租用戶
3. EC2 提供 windows 及 linux，也可以選擇內部商務應用程式、web應用程式、資料庫、第三方軟體
4. EC2 也可以選擇大小，更大的cpu記憶體 垂直擴展

### EC2 類型
每個ec2執行個體類型都分組在不同執行個體系列中
- 一般用途
	- 平衡的資源
	- 多樣化的平衡負載
	- web
- 運算最佳化
	- 運算密集的任務
	- 遊戲伺服器
	- 高效能運算HPC
	- 科學建模
- 記憶體最佳化
- 加速運算
	- 浮點運算
	- 圖形
- 儲存最佳化
	- 分散式檔案系統
	- 資料倉儲應用程式
	- 高頻率線上交易處理 ([[OLTP]]) 系統
	- 高[[IOPS]]系統


### EC2 計費
- 隨需 > 適合新手入門或臨時需要，不可中斷，無需預付或最低合約。不適合持續一年以上的工作負載。
- saving plans > 承諾==一或三年==的每小時支出承諾，與預留執行體類似，不用事先指定類型和大小
- 預留執行體 > 適合穩定或可預測使用量，需指定類型和大小、作業系統、租用或專用
- spot執行個體 > 通知後兩分鐘會回收、容許中斷，不影響業務營運的服務
- 專用主機 > 最貴，完全專屬於客戶的執行個體的實體伺服器

### Amazon EC2 Auto Scaling

根據變化自動增減執行個體，維持更高可用性
- 動態調整
- 預測性調整

可以設定執行個體數量==最小容量==，也可以設定==所需容量==，

>  如果沒有設定所需數量，則所需數量預設為最小數量。

也可以設定==最大容量==


### Elastic Load Balancing

是一種區域結構，不是在個別EC2上執行，可在多個執行個體之間自動分配流量，可將前後端請求解偶，後端產生新的實例時只需通知ELB即可，不需通知每一個前端服務。


### Message and Queue

應用程式之間直接彼此通訊，稱==緊湊耦合==，當有單一元件故障時將影響整個系統。
兩個 AWS 服務：
-  [[Amazon SQS]]
- [[Amazon SNS]]

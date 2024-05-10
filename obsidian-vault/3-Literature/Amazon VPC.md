#aws #services #saa 

## Amazon VPC
全名 **Amazon Virtual Private Cloud**，
提供一個建立虛擬私有網路的服務，在雲端創建一個隔離網路環境。

1. 網路隔離：建立虛擬私有網路，可以在其中定義子網路、路由表、網路訪問控制清單等。
2. 自定義 IP 地址範圍：自行定義 IP 地址範圍，確保AWS中的資源能與內部網路連接。
3. 連接到企業數據中心：通過 VPN 或 [[AWS Direct Connect]]，將AWS虛擬網路與企業數據中心連接，實現混合雲。
4. 安全性控制：支援使用安全組和網路訪問控制清單 (Network Access Control Lists, NACLs) 等機制來實現對資源的訪問控制和網路流量過濾，從而提高資源的安全性。

需要將資源放進不同的子網路中，子網路是 VPC 中的 IP 網址區塊。

若要允許公有網路流量進出 VPC ，則必須將網路閘道(IGW)連接到VPC
![[Pasted image 20240510015506.png]]

若僅允許私有網路流量進出 VPC ，則必須將VPN
連接到VPC。
![[Pasted image 20240510015630.png]]

也可以透過[[AWS Direct Connect]] 專用通道連接到 VPC
![[Pasted image 20240510015649.png]]


網際網路閘道是 VPC 和網際網路之間的連結。沒有網際網路閘道，任何人都無法存取 VPC 內的資源。



Virtual Private Gateway
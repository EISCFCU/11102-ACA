# 建立VPC

# 實施步驟

# 實施架構

# 步驟1：建立VPC


1.搜尋VPC

2.點選[VPC]

3.點選[Your VPCs]

4.點選[Create VPC]

5.Name tag: Lab VPC

IPv4 CIDR block: 10.0.0.0/16

6.點選[Create VPC]

7.點選[Tags]

8.點選[Actions]->[Edit DNS hostnames]

9. 點選[enable]

10. 點選[Save changes]


# 步驟2：建立子網
# 建立公有子網
1.點選[Subnets]

2.點選[Create subnet]

3.VPC ID: Lab VPC

Subnet name: Public Subnet

Availability Zone: Select the first Availability Zone in the list (do not keep the No Preference default)

IPv4 CIDR block: 10.0.0.0/24

4.點選[Create subnet]

5.點選[Public Subnet]

6.點選[Actions]->[Edit subnet settings]

7.點選[Enable auto-assign public IPv4 address]

8.點選[Save]

# 建立私有子網
9.點選[Create subnet]

10.VPC ID: Lab VPC

Subnet name: Private Subnet

Availability Zone: Select the first Availability Zone in the list (do not keep the No Preference default)

IPv4 CIDR block: 10.0.2.0/23

11.點選[Create subnet]


# 步驟3：建立internet gateway


1.點選[Internet Gateways]

2.點選[Create internet gateway]

3.Name tag: Lab IGW

4.點選[Create internet gateway]

5.點選[Actions]->[Attach to VPC]

6.點選[Lab VPC]

7.點選[Attach internet gateway]


# 步驟4：配置路由


1.

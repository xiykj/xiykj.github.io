- 查询cpu序列号：
```P4
wmic cpu get processorid
```
<br/>

- 查询主板序列号：
```P4
wmic baseboard get serialnumber
```
<br/>

- 查询bios序列号：
```P4
wmic bios get serialnumber
```
<br/>

- 查询网卡MAC地址（两条命令都可）：
```P4
wmic nicconfig get macaddress
```
```P4
getmac
```
<br/>


- 查询硬盘序列号：
```P4
wmic diskdrive get serialnumber
```
<br/>

- 查询内存主板数量（两条命令都可）
```P4
wmic memorychip list brief  
```
```P4
wmic MEMPHYSICAL list brief
```
<br/>

- 查询bios版本信息（两条命令都可）
```P4
wmic bios list brief
```
```P4
wmic bios list full
```
<br/>

- 查询最大支持内存容量
```P4
wmic memphysical get maxcapacity
```
<br/>

- 查询cpu信息：
```P4
wmic cpu list full
```
```P4
wmic cpu list brief
```
 
# 数据说明

格式：文件名+作用
### IP对分协议流量统计.csv
- 表头 source_ip,destination_ip,protocol,uplink_length,downlink_length,sum_length
- 解释：源数据以src_ip, des_ip, protocol为主码， groupby之后将相应的上下行流量相加

### IP流量统计
- 表头： ip,uplink_length,downlink_length,sum_length
- 解释：主码是ip (不分协议), tcpflow的真实流量是指：发送流量为： up_as_src+down_as_des, 接收流量    为:down_as_src+up_as_des

### 初赛复赛IP流量对比
- 表头：,ip,s_up_length,s_down_length,s_sum_length,f_down_length,f_up_length,f_sum_length
- 解释：s代表复赛， f代表初赛， 通过初赛和复赛两个数据集的IP流量统计表外连接得到， 如果在初赛或者复赛中没出现这个ip， 那么相应的列就为0

### 上行流量变大
- 表头：,ip,s_up_length,f_up_length,up_increment
- 没有包含极端ip:10.49.81.18 , 但是其上行流量也增加得很多

### 下行流量变大
- 表头：,ip,s_down_length,f_down_length,down_increment
- 没有包含极端ip: 10.21.12.148, 但是其下行流量也增加得很多

### 总流量变大
- 表头：,ip,s_sum_length,f_sum_length,sum_increment
- 没有包含 10.21.12.148 和 10.49.81.18 两个IP



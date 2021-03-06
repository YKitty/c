# IP地址的三类私有地址

------

对于IP地址来说有着三种私有地址。

三种私有地址如下：

``` c++
10.0.0.0 - 10.255.255.255
172.16.0.0 - 172.16.255.255
192.168.0.0 - 192.168.255.255 
```

**那么这三种私有地址有着怎样的区别呢？**

这三类私有地址不同之处仅仅在于就是他们所属**级别不同**。

对于**10开头：是A类地址。子网掩码：255.0.0.0**

对于**172.16开头：来说是B类地址。子网掩码：255.255.0.0**

对于**192.168开头：来说是C类地址。子网掩码：255.255.255.0**

**对于私有地址的理解**

私有地址只能在局域网进行使用，不能放到公网中进行通信，如果要访问公网中的某一个网址，那么就啊哟进行NAT转化，将私有地址一级一级的转化到公网的地址。

对于每一个类的私有地址，最后都会转化为相对应的同一类的公网IP地址。

举例：私有IP地址是：10.114.104.176。转化到可以访问外网的时候，一定是10开头的公网地址





对于学校来说，一般申请的都是A类地址。因为这个A类地址是一个公网地址，对于这个A类地址就构成了一个局域网。然后再这个局域网中可以采用子网掩码的方式对于这个局域网中的地址进行划分。

所以就会出现这样的情况。

比如从学校申请了一个IP地址之后，这个IP地址是A类地址的私有地址，但是子网掩码却不是A类地址的子网掩码反而是B类或者C类地址的子网掩码。

这就是因为学校对于这个局域网内的地址采用了子网划分的方法，对于子网进行了划分。
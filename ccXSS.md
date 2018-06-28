#### There is a storage type XSS in the site setting up the phone bar

Powered by Shiyan 

##### version:

CMS MaeloStore V.1.5.0

##### Download link:

https://github.com/maelosoki/MaeloStore

##### Vulnerability analysis：

The website does not filter the parameters of the search bar, resulting in the existence of XSS vulnerability. 

##### Steps To Reproduce: 

1、Login the backstage: 

http://127.0.0.1/MaeloStore/admin/

2、[Sidebar]  Pengaturan --> [Sidebar]   Website ，click Website

![](https://github.com/lzlzh2016/MaeloStore/blob/master/11.png)

3、We continue to come [Column]Telephone，Set content field to the following payload ，And choose to save。

```
<img src=x onerror=alert(/shiyan/)>
```

![](https://github.com/lzlzh2016/MaeloStore/blob/master/22.png)

4、When we return to the home page, we trigger a vulnerability

![](https://github.com/lzlzh2016/MaeloStore/blob/master/33.png)

Note: the vulnerability will be exploited by malicious users. 




























































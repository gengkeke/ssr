登录成功后，依次运行以下三条命令：

```shell
wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh

chmod +x shadowsocks-all.sh

# redhat 9 ->看这里  https://docs.fedoraproject.org/en-US/epel/

# subscription-manager repos --enable codeready-builder-for-rhel-9-$(arch)-rpms
# dnf install https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm

./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log



```

接下来会有几个参数需要选择，依次为：

1.提示选择哪个版本安装，我们输入2后按回车，即选择SSR安装。

![image](https://github.com/gengkeke/ssr/blob/master/ssr/images/1.jpg)

2.然后会提示设置SSR密码，输入自定义密码后按回车，建议不要使用默认密码。

![image](https://github.com/gengkeke/ssr/blob/master/ssr/images/2.jpg)

3.接下来选择SSR要使用的服务器端口，随便输入一个，也可以默认回车。

![image](https://github.com/gengkeke/ssr/blob/master/ssr/images/3.jpg)

4.然后选择加密方式，如果选择chacha20的话，就输入对应序号12，按回车继续。

![image](https://github.com/gengkeke/ssr/blob/master/ssr/images/4.jpg)

5.接下来选择协议，建议选择自auth_aes128_md5开始以下的几种，输入对应序号按回车。

![image](https://github.com/gengkeke/ssr/blob/master/ssr/images/5.jpg)

6.然后选择混淆方式，如下图所示，选择好后按回车。                        

![image](https://github.com/gengkeke/ssr/blob/master/ssr/images/6.jpg)

7.以上参数选择完成后，按任意键开始安装。                              

![image](https://github.com/gengkeke/ssr/blob/master/ssr/images/7.jpg)

8.安装完成后，会有如下图安装成功的提示，记住刚才设置的各项参数，在客户端连接时需要用到。

![image](https://github.com/gengkeke/ssr/blob/master/ssr/images/8.jpg)

9.经过以上几个简单的参数选择后，SSR服务器端已经自动安装成功了。保险起见，输入reboot重启VPS服务器，SSR会自动随系统重启。 

![image](https://github.com/gengkeke/ssr/blob/master/ssr/images/9.jpg)

修改端口

```shell

vi /etc/shadowsocks-r/config.json

/etc/init.d/shadowsocks-r restart

```





















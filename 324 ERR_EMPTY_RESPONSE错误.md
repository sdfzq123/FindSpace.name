#Pre
从18号开始，我博客在更新文章或者发布文章的时候，就出现这个错误，一旦出现，之前保存的就都丢了，非常苦逼。
#深入了解问题
chrome提示的是这样的
![][1]

firefox提示是这样的：
![][2]

F12之后查看network(这图是找的，现在我发布的时候直接提示第一张图，抓不到了)
![][3]
地址栏里`chrome://net-internals`来查找event，是这样的错误
![][4]
搜索之后明白原因是请求没有成功发出去，并搜索到了以下的解决方案：
#方案
##1 切换浏览器
好多人的情况是因为chrome adblock的问题。
##2 停用sitemap插件
很多人是因为sitemap插件，可是我用sitemap插件好久了，应该不会突然出现问题。停用了，不管用。
##3 停用所有插件尝试
我全部停用，仍旧出现错误。如果你的生效了，可以一个一个重新启用来检查是哪个的问题。
##4 路由器问题
切换另一个路由器，不行。
##5 DNS问题
取消自动获取，设置成114.114.114.114或者8.8.8.8，不行。
##6 清空浏览器缓存
##7 回退到问题发生前的备份
我甚至直接删掉所有文件，安装原生的wordpress尝试了，不行。
##8 联系客服
我提交了两次工单，第一次他们检查说没有问题，第二次我要求技术人员人站对待这个问题，技术人员回复说，检查过了各种信息，没有问题，我可以提出转移服务器的要求，然后我就回复了，要求转移服务器，第二天早上一上班他们就转了，给西部数据的客服态度赞一个。尽管转了之后仍不行。。
##9 qq远程小伙伴，用他们的浏览器登录
发现可以，，远程了几个，发现都可以，开始考虑是不是我网络的问题，但是不知道为什么登录另外一个wordpress空间就可以。在群里问小伙伴，小伙伴提议用vpn操作，我试了下，竟然没有问题了。。。就是速度有点慢
#PS
问题原因应该是学校的渣网，尽管以前好好的。
我还会继续查找问题源头。。



[1]: http://faq.myhostadmin.net/Customercenter/UploadImages/question/1503/octt41m82v5s2j8.png "Chrome出错提示"
[2]: http://www.findspace.name/wp-content/uploads/2015/06/firefox.png "firefox提示"
[3]: http://segmentfault.com/img/bVbXY5/view "f12"
[4]: http://www.findspace.name/wp-content/uploads/2015/06/chrome2.png "chrome://net-internals"
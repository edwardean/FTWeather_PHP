大标题
==================================
	大标题一般显示工程名，类似html的\<h1\><br />
	你只要在标题下面跟上====即可


中标题
-----------------------------------
	中标题一般显示重点项，类似html的\<h2\><br />
	你只要在标题下面输入------即可

### 小标题
	小标题类似html的\<h3\><br />
	小标题的格式如下 ### 小标题<br />
	注意#和标题字符中间要有空格

### 注意!!!下面所有语法的提示我都先用小标题提醒了!!!

###	多行文本框
	这是一个有多行的文本框
	你可以写入代码等，每行文字只要输入两个Tab再输入文字即可
	这里你可以输入一段代码

###	比如我们可以在多行文本框里输入一段代码，来一个OC版本的HelloWorld :]
		#import <Foundation/Foundation.h>

		int main(int argc, const char * argv[])
		{
		    NSLog(@"Hello, World!");        
		    return 0;
		}
###	链接
1.[点击这里你可以链接到google](http://google.com.sg)<br />

###	只是显示图片
![github](http://github.com/unicorn.png "github")

###	想点击某个图片进入一个网页，比如我想点击github的icorn然后再进入github.com
[![image]](https://github.com/)
[image]:https://github.com/github.png "github"

###	文字被一些字符包围
> 文字呗一些字符包围
>
> 只要在文字前面加上>空格即可
>
> 如果你要换行的话，新起一行，输入>空格即可，后面不接文字
> 但> 只能放在行首才有效

### 文字被一些字符包围，多重包围
> 文字被一些字符包围开始
>
> > 只要在文字前面加上>空格即可
>
> > > 如果你要换行的话，新起一行，输入>空格即可，后面不接文字
>
> > > > 但> 只能放在行首才有效

### 特殊字符处理
有一些字符如<,#等，只要在特殊字符前面加上转义字符\即可 <br />
你想换行的话其实可以直接用html标签\<br /
>
# Professional iOS Network Programming
## Chapter 2: Service Architecture

The example code from Chapter 2 of my book, [Professional iOS Network Programming](http://www.wiley.com/WileyCDA/WileyTitle/productCd-1118362403,descCd-description.html "Professional iOS Network Programming: Connecting the Enterprise to the iPhone and iPad").  Further discussion is also available on the [Wiley P2P forum](http://p2p.wrox.com/book-professional-ios-network-programming-connecting-enterprise-iphone-ipad-708/).

* Facade PHP is a web service that serves stock ticker and weather data to clients.  Each endpoint is built with two completely independent data sources that are converted to a common output format.  Thus, the backend system can be completely replaced and the service output will remain unchanged.  Each endpoint also has a second version that adds and changes the type of some fields, demonstrating how multiple app versions can be deployed after service enhancements are made.

* Facade Tester is a corresponding iOS app that consumes a service locator to discover the proper Facade PHP endpoints to use and then displays API results in a table view.  A segmented control allows the app to change which service version it consumes.

Once the PHP services are running, be sure to update the service locator URL in `FTAppDelegate loadServiceLocator`.
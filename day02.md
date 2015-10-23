----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 
## Day2 
> ![](https://img.shields.io/badge/AndroidEveryday-Day2-green.svg?style=flat)   
> ***Time : October 23th,2015*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[FlowingDrawer](https://github.com/mxn21/FlowingDrawer) --- (From [mxn21](https://github.com/mxn21)) : 
swipe right to display drawer with flowing effects[贝塞尔曲线弹性抽屉菜单]._

    ![](https://github.com/mxn21/FlowingDrawer/raw/master/screen.gif)

- _[SlidingCard](https://github.com/mxn21/SlidingCard) --- (From [mxn21](https://github.com/mxn21)) : 
Sliding cards with pretty gallery effects [手指滑动图片效果]._

    ![](https://github.com/mxn21/SlidingCard/raw/master/screen.gif)

- _[Android-ScalableVideoView](https://github.com/yqritc/Android-ScalableVideoView) --- (From [yqritc](https://github.com/yqritc)) : 
Android Texture VideoView having a variety of scale types like the scale types of ImageView. [像Imageview一样展示视频动画,extends TextureView]._

    ![](https://github.com/yqritc/Android-ScalableVideoView/raw/master/sample/sample.gif)

- _[RecyclerView-FlexibleDivider](https://github.com/yqritc/RecyclerView-FlexibleDivider) --- (From [yqritc](https://github.com/yqritc)) : 
Android library providing simple way to control divider items of RecyclerView. [给RecyclerView添加分格线]._

    ![](https://github.com/yqritc/RecyclerView-FlexibleDivider/raw/master/sample/sample2.gif)

- _[RecyclerView-MultipleViewTypesAdapter](https://github.com/yqritc/RecyclerView-MultipleViewTypesAdapter) --- (From [yqritc](https://github.com/yqritc)) : 
RecyclerView adapter classes for managing multiple view types. [RecyclerView多类型布局]._

    ![](https://github.com/yqritc/RecyclerView-MultipleViewTypesAdapter/raw/master/sample/sample.gif)

- _[debugoverlay](https://github.com/sockeqwe/debugoverlay) --- (From [sockeqwe](https://github.com/sockeqwe/)) : 
A tiny window overlay to log app internal on top of your android app. [做一个透明层让log显示在上面]._

    ![](https://camo.githubusercontent.com/c87939a0a73e3fd7305a2d3dca6cc596d2c97b15/687474703a2f2f68616e6e6573646f72666d616e6e2e636f6d2f696d616765732f64656275676f7665726c61792e706e67)

2.Logic：

- _[android-asyncservice](https://github.com/JoanZapata/android-asyncservice) --- (From [JoanZapata](https://github.com/JoanZapata) & Tag  is [AsyncTask](https://github.com/JoanZapata/android-asyncservice)) : 
AsyncService uses annotations to shorten the code needed to start asynchronous long running tasks and return result. [使用注解@AsyncService & @OnMessage来完成异步请求]._

	![](https://raw.githubusercontent.com/JoanZapata/android-asyncservice/master/logo.png)


		@AsyncService
		public class DemoService {
	
			public User getUser(String name) {
				// Runs asynchronously.
				return …;
			}
	
		}
		... then use it.
		… {
			service.getUser("joan");
		}
	
		@OnMessage void onUser(User e) {
			// Runs on UI thread.
		}

3.Architecture:

- _[mosby](https://github.com/sockeqwe/mosby) --- (From [sockeqwe](https://github.com/sockeqwe)) : 
A Model-View-Presenter library for modern Android apps. [一个Android的MVP架构]._

	![](http://i.imgur.com/xzn9gKd.png)

	(more information want to know please see today's Article)



#### article ####

- _[Model-View-Presenter](http://hannesdorfmann.com/mosby/mvp/) --- (From Author  [sockeqwe](https://github.com/sockeqwe) blog [http://hannesdorfmann.com](http://hannesdorfmann.com)) --- [Source in [Github](https://github.com/sockeqwe/mosby)]_ 

	The name of this library, Mosby, has been chosen in honor of Ted Mosby, the architect of the famous tv series How I Met Your Mother. The aim of this library is to help you build modern android apps with a clean Model-View-Presenter architecture. Furthermore, Mosby helps you to handle screen orientation changes by introducing ViewState and retaining Presenters. [Translation：MVP框架 – Ted Mosby的软件架构]. 
 
	Chinese Translation Address : [Thanks To android-tech-frontier](http://www.devtf.cn/?p=551)
	
	![](http://i.imgur.com/Zg8e2Wq.png)![](http://i.imgur.com/P2ZgWY4.png)

	![](http://i.imgur.com/2m5zDIH.png)

	This page describes the principle of Model-View-Presenter (MVP) and how to use Mosby to create MVP based applications.

	- _The [model](http://hannesdorfmann.com/mosby/mvp/) is the data that will be displayed in the view (user interface)._
	- _The [view](http://hannesdorfmann.com/mosby/mvp/) is an interface that displays data (the model) and routes user commands (events) to the Presenter to act upon that data. The view usually has a reference to its Presenter._
	- _The [Presenter](http://hannesdorfmann.com/mosby/mvp/) is the “middle-man” (played by the controller in MVC) and has references to both, view and model. Please note that the word “Model” is misleading. It should rather be business logic that retrieves or manipulates a Model. For instance: If you have a database storing User in a database table and your View wants to display a list of users, then the Presenter would have a reference to your database business logic (like a DAO) from where the Presenter will query a list of Users._

#### website	

- _[http://stackoverflow.com](http://stackoverflow.com/) --- (Build By [Jeff Atwood & Joel Spolsky ,2008](https://github.com/daimajia)) :Stack Overflow is a question and answer site for professional and enthusiast programmers. [程序猿BUG的维基百科Wiki]._

	![](http://i.imgur.com/2vFzulA.jpg)


	![](https://img.shields.io/badge/The%20Day2-End%20!-ED1C24.svg?style=flat)



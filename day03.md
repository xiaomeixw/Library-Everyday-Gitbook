----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 

## Day3
> ![](https://img.shields.io/badge/AndroidEveryday-Day3-green.svg?style=flat)   
> ***Time : October 24th,2015*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[TextSurface](https://github.com/elevenetc/TextSurface) --- (From [elevenetc](https://github.com/elevenetc)) : 
A little animation framework which could help you to show message in a nice looking way. [让TextView动画飞起来]._

    ![](https://github.com/elevenetc/TextSurface/raw/master/docs/demo.gif)

- _[DraggableView](https://github.com/elevenetc/DraggableView) --- (From [elevenetc](https://github.com/elevenetc)) : 
Draggable views with rotation and skew/scale effects. [带动画效果拖拽View条目]._

    ![](https://github.com/elevenetc/DraggableView/raw/master/docs/skewview.gif)

- _[BadgeView](https://github.com/elevenetc/BadgeView) --- (From [elevenetc](https://github.com/elevenetc)) : 
Badge view with animated effect which shows a bitmap or a text. [带动画效果的在徽章中显示图片或者文字]._

    ![](https://github.com/elevenetc/BadgeView/raw/master/docs/badgeview-spongebob.gif)

- _[BGABadgeView-Android](https://github.com/bingoogolapple/BGABadgeView-Android) --- (From [bingoogolapple](https://github.com/bingoogolapple)) : 
Android badge view copy from the china "twitter" : sina weibo. [模仿新浪微博的Android徽章控件]._

    ![](https://camo.githubusercontent.com/520ae13b5197a4d1fa94642794eeb6d427bce1c3/687474703a2f2f37786b39646a2e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f62616467652f73637265656e73686f74732f62616467652e676966)

- _[android-viewbadger](https://github.com/jgilfelt/android-viewbadger) --- (From [jgilfelt](https://github.com/jgilfelt)) : 
A simple way to "badge" any given Android view at runtime without having to cater for it in layout. [徽章View]._

    ![](https://camo.githubusercontent.com/a705a3e88c75ae2394943bd7c56f725697616ea8/687474703a2f2f7777772e6a65666667696c66656c742e636f6d2f766965776261646765722f76622d31612e706e67)

- _[BadgeView](https://github.com/elevenetc/BadgeView) --- (From [stefanjauker](https://github.com/stefanjauker/BadgeView)) : 
An extended TextView that mimics the iOS Springboard 'badges'. It can be overlaid on any other item. [徽章View]._

	![](http://i.imgur.com/ayCgRjB.png)


2.Logic：

- _[AsyncManager](https://github.com/boxme/AsyncManager) --- (From [boxme](https://github.com/boxme) & Tag  is [AsyncTask](https://github.com/boxme/AsyncManager)) : 
Android Multithreading Library For Easy Asynchronous Management. [后台异步线程]._


	![](http://i.imgur.com/0tubENV.png)

		// A BackgroundTask object will be returned from this method. Reference it if require.
		AsyncManager.runBackgroundTask(new TaskRunnable<Params, Result, Void>() {
		    @Override
		    public Result doLongOperation(Params params) throws InterruptedException {
		        // checkForThreadInterruption();
		        // Your long operation
		        return result;
		    }
		
		    // Override this callback if you need to handle the result on the UI thread
		    @Override
		    public void callback(Result result) {
		        // Handle the result from doLongOperation()
		    }
		}.setParams(params));	

3.Architecture:

- _[MvpCleanArchitecture](https://github.com/glomadrian/MvpCleanArchitecture) --- (From [glomadrian](https://github.com/glomadrian)) : 
A sample project using Clean architecture and MVP in Android. [探索MVP架构]._

	![](https://github.com/glomadrian/MvpCleanArchitecture/raw/master/img/screenshot_1.png)


- _[androidmvp](https://github.com/antoniolg/androidmvp) --- (From [antoniolg](https://github.com/antoniolg)) : 
MVP Android Example used to explain how to use this pattern in our Android apps. [MVP架构的一个Simple范例]._

	![](http://i.imgur.com/DsX7bsb.png)

- _[UpcomingMoviesMVP](https://github.com/jlmd/UpcomingMoviesMVP) --- (From [jlmd](https://github.com/jlmd)) : 
Sample project of MVP and Material Design using as repository a list of upcoming movies. [MVP架构 & Material Design的一个电影Simple范例]._

	![](https://github.com/jlmd/UpcomingMoviesMVP/raw/master/art/screenshot1.png)

- _![](http://i.imgur.com/TRBV7jp.jpg) [FastAndroid](https://github.com/huntermr/FastAndroid) --- (From [huntermr](https://github.com/huntermr)) : 
A Rapid development framework With MVP & some famous libraries . [融入了MVP模式,集成了多个开源项目后,进行整合形成的Android快速开发框架]._

	![](http://i.imgur.com/Z2wSnv2.png)

#### article ####

- _[cA small leak will sink a great ship](https://corner.squareup.com/2015/08/a-small-leak.html) --- (From Author  [Piwai](https://github.com/pyricau) blog [http://www.piwai.info/](http://www.piwai.info/)) --- [No Source]_ 

	This post started as an internal email thread when I was building LeakCanary. I found a strange memory leak and started digging in order to figure out what was happening.
	TL;DR: Prior to Android Lollipop, alert dialogs may cause memory leaks in your Android apps. [Translation：Square工程师 : 一个内存泄漏引发的悲惨结果]. 
 
	Chinese Translation Address : [Thanks To android-tech-frontier](http://www.devtf.cn/?p=1065)

	![](http://i.imgur.com/AHA60WS.png)![](http://i.imgur.com/WpHtwuM.png)

	A super cool man in Android , This is his resume website : [http://www.piwai.info/cv.html#/welcome](http://www.piwai.info/cv.html#/welcome)


#### website 	

- _[https://medium.com/android-news](https://medium.com/android-news) --- (Build By [Evan Williams,2012](https://en.wikipedia.org/wiki/Medium_(publishing_platform))) : Medium is a blog-publishing platform.The platform has evolved into a hybrid of non-professional contributions and professional, paid contributions. [基于主题的协作型媒体Blog文章消费写作平台]._

	![](http://i.imgur.com/wbgsH2m.jpg)

	![](https://img.shields.io/badge/The%20Day3-End%20!-ED1C24.svg?style=flat)












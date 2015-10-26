List of Android  Libraries I browsed EveryDay.
==================
![Project status](https://img.shields.io/badge/project-maintained-brightgreen.svg?style=flat) [![API](https://img.shields.io/badge/API-8%2B-green.svg?style=flat)](https://developer.android.com/about/versions/android-2.2.html) [![library](https://img.shields.io/badge/awesome-library-ff69b4.svg?style=flat)](https://github.com/stars/xiaomeixw) [![android](https://img.shields.io/badge/For-Android-blue.svg?style=flat-square)](https://www.android.com/)

![](http://i.imgur.com/g4x1ThH.png)

About android library I will Keep update everyday.The Image is upload to github's servers or markdown's servers not qiniu so If your are an Android developer from China，It is well known that The image loading will be very slow ,no hurry please just waiting.

## Other lists
- _Looking for  Read the gitbook online? Check out_ [https://xiaomeixw.gitbooks.io](https://xiaomeixw.gitbooks.io/library-everyday/content/).
- _Looking for Give a suggest or Recommend library? Check out_ jpxw007@gmail.com.
- _Looking for The Clean Architecture? Check out_ [xiaomeixw/The-Clean-Architecture-Gitbook](https://github.com/xiaomeixw/The-Clean-Architecture-Gitbook).
- _Looking for My Blog? Check out_ [http://www.sabria.me](http://www.sabria.me/).
- _Looking for More  libraries? Check out_ [my github's stars](https://github.com/stars/xiaomeixw)

## Tips
Contains the following content：

- _library_
- _article/blog_
- _website_
- _tools_
- _apps_
- _news_


## Maintainers
[![xiaomeixw](http://i.imgur.com/trenQOC.png) ***xiaomeixw***](https://github.com/xiaomeixw) 

## Index `(quick look)`
* [2015/10/22 day1](#day1)
* [2015/10/23 day2](#day2)
* [2015/10/24 day3](#day3)
* waitting for upload
* [2015/10/26 day5](#day5)

----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 

## Day5
> ![](https://img.shields.io/badge/AndroidEveryday-Day5-green.svg?style=flat)   
> ***Time : October 26th,2015*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[PagerSlidingTabStrip](https://github.com/astuetz/PagerSlidingTabStrip) --- (From [astuetz](https://github.com/astuetz)) : 
An interactive indicator to navigate between the different pages of a ViewPager. [ViewPage指示器]._

    ![](https://camo.githubusercontent.com/e39d7a7c9c815b737d15ee1a62863425579b6446/68747470733a2f2f6c68332e67677068742e636f6d2f50585337456d4868515a6454314f613337396979393148583342795741516e465a4174684d4146615f5148414f484e436c45615855356e784445416a3146326571626b)

- _[PagerSlidingTabStrip](https://github.com/jpardogo/PagerSlidingTabStrip) --- (forked from [astuetz/PagerSlidingTabStrip](https://github.com/astuetz/PagerSlidingTabStrip) & Author [jpardogo](https://github.com/jpardogo)) : 
An interactive indicator to navigate between the different pages of a ViewPager but this library can change the tab's color.. [ViewPage指示器,能改变tab的颜色]._

    ![](https://raw.githubusercontent.com/jpardogo/PagerSlidingTabStrip/master/art/material_tabs.gif)

- _[AndroidRubberIndicator](https://github.com/LyndonChin/AndroidRubberIndicator) --- (From [LyndonChin](https://github.com/LyndonChin)) : 
A rubber indicator for ViewPager. [View滑动指示器]._

    ![](https://camo.githubusercontent.com/2ea6152b06aa5f9ca21ab7ff0a83830f73f48fbe/68747470733a2f2f6431337961637572716a676172612e636c6f756466726f6e742e6e65742f75736572732f3330333233342f73637265656e73686f74732f323039303830332f70616765696e64696361746f722e676966)

- _[rubber-loader](https://github.com/greenfrvr/rubber-loader) --- (From [greenfrvr](https://github.com/greenfrvr)) : 
Android indeterminate loader widget with rubber shape and color transitions. [loading时的橡胶动画效果]._

    ![](http://i.imgur.com/9ISSPVp.gif)

- _[hashtag-view](https://github.com/greenfrvr/hashtag-view) --- (From [greenfrvr](https://github.com/greenfrvr)) : 
Android fully customizable widget for representing data like hashtags collection and similiar. [自定义的标签View]._

    ![](https://github.com/greenfrvr/hashtag-view/raw/master/screenshots/screen1.png)


2.Logic：

- _[quitnow-cache](https://github.com/Fewlaps/quitnow-cache) --- (From [Fewlaps](https://github.com/Fewlaps) & Tag  is [Caching](https://github.com/Fewlaps/quitnow-cache)) : 
A memcached-like Java cache, focused on portability. [可限时销毁的cache]._

	![](http://i.imgur.com/pFkx7Mm.png)

		QNCache cache = new QNCacheBuilder().createQNCache();
		
		cache.set("key", "value", 60 * 1000); // It can store things for a minute,
		cache.set("key", "value", 60 * 60 * 1000); // for an hour,
		cache.set("key", "value", 0); // or forever.
		cache.set("key", "value"); // And also for the short version of forever.
		
		cache.get("key"); // It can get them again,
		cache.remove("key"); // and remove it if you want.
		
		cache.get("unExistingKey"); // If something doesn't exists, it returns null
		cache.get("tooOldKey"); // The same if a key is too old
		
		cache.set("AnInteger", new Integer(42)); // You can save all kind of Objects...
		cache.set("ACollection", new ArrayList()); // ...whatever you want
		
		cache.removeAll(); // You can also clean it,
		cache.size(); // and ask it how many elements it has

- _[tray](https://github.com/grandcentrix/tray) --- (From [grandcentrix](https://github.com/grandcentrix) & Tag  is [Caching](https://github.com/grandcentrix/tray)) : 
a SharedPreferences replacement for Android with multiprocess support. [对系统的SharedPreferences添加多进程支持]._

	
	Tray is this mentioned explicit cross-process data management approach powered by a ContentProvider. Tray also provides an advanced API which makes it super easy to access and maintain your data with upgrade and migrate mechanisms. Welcome to SharedPreferences 2.0 aka Tray.

	![](https://cloud.githubusercontent.com/assets/1096485/9990484/fe61888c-6061-11e5-890d-a76f1ef60304.png)

		// create a preference accessor. This is for global app preferences.
		final AppPreferences appPreferences = new AppPreferences(getContext()); // this Preference comes for free from the library
		// save a key value pair
		appPreferences.put("key", "lorem ipsum");
		
		// read the value for your key. the second parameter is a fallback (optional otherwise throws)
		final String value = appPreferences.getString("key", "default");
		Log.v(TAG, "value: " + value); // value: lorem ipsum
		
		// read a key that isn't saved. returns the default (or throws without default)
		final String defaultValue = appPreferences.getString("key2", "default");
		Log.v(TAG, "value: " + defaultValue); // value: default


- _[Stanley](https://github.com/iambmelt/Stanley) --- (From [iambmelt](https://github.com/iambmelt) & Tag  is [Caching](https://github.com/iambmelt/Stanley)) : 
Convenient stashing of simple data formats on Android with SharedPreferences（A small library for study Annotation & Proxy）. [使用注解&代理模式来操作SharedPreferences]._

	![](http://i.imgur.com/d6v8gbv.png)

		//Define an interface		
		@Proxy(name = "Prefs", mode = Context.MODE_PRIVATE)
		public interface Person {
		    @Accessor
		    void setLastName(String name);
		}

	    //Make an instance		
		Person elvis = new ProxyGenerator().create(context, Person.class);

		//And go!		
		elvis.setLastName("presley");

- _[SharedSqlite](https://github.com/Jhonnyc/SharedSqlite) --- (From [Jhonnyc](https://github.com/Jhonnyc) & Tag  is [Caching](https://github.com/Jhonnyc/SharedSqlite)) : 
A Sqlite class library implementation of the android 'SharedPreferences' object. [一个用Sqlite构建的SharedPreferences类库]._

	![](http://i.imgur.com/F5lQEdz.png)

		//To create a new instance simply call
		SharedSqlite.initialize(context);

		//Then you are free to add
		SharedSqlite.addValue(key, value);
		
		//Then get
		getStringValue(key, defaultValue)
		getIntValue(key, defaultValue)
		getLongValue(key, defaultValue)
		getDoubleValue(key, defaultValue)
		getFloatValue(key, defaultValue)
		getBooleanValue(key, defaultValue)

- _[hawk](https://github.com/orhanobut/hawk) --- (From [orhanobut](https://github.com/orhanobut) & Tag  is [Caching](https://github.com/orhanobut/hawk)) : 
Secure Simple Key-Value Storage for Android & Support for RxJava. [安全简单的key-value存储]._

	![](http://i.imgur.com/6smSK9t.png)

		//Initialize the hawk
		Hawk.init(this)
		    .setEncryptionMethod(HawkBuilder.EncryptionMethod.MEDIUM)
		    .setStorage(HawkBuilder.newSqliteStorage(this))
		    .setLogLevel(LogLevel.FULL)
		    .build();

		//save
		Hawk.put(key, T); // Returns the result as boolean

		//get
		T result = Hawk.get(key);

- _[Remember](https://github.com/tumblr/Remember) --- (From [tumblr](https://github.com/tumblr) & Tag  is [Caching](https://github.com/tumblr/Remember)) : 
A preferences-backed key-value store. [tumblr出品的key-value存储,必属精品]._

	![](http://i.imgur.com/u6gYwTJ.png)

		//initialize Remember in  Application
		@Override
		public void onCreate() {
		    super.onCreate();
		    Remember.init(getApplicationContext(), "com.mysampleapp.whatever");
		}

		//Now you can freely use Remember from anywhere in your app:
		Remember.putString("some key", "some value");
		String value = Remember.getString("some key", "");

- _[android-easy-cache](https://github.com/vincentbrison/android-easy-cache) --- (From [vincentbrison](https://github.com/vincentbrison) & Tag  is [Caching](https://github.com/vincentbrison/android-easy-cache)) : 
This android library provide a cache with 2 layers, one in RAM in top of one disk. [两层缓存，一层是内存RAM一层是磁盘Disk]._

	![](http://i.imgur.com/DfGrhfr.png)

		//A cache with default serializer in RAM and disk disable
		DualCache<AbstractVehicule> cache = new DualCacheBuilder<AbstractVehicule>(CACHE_NAME, TEST_APP_VERSION, AbstractVehicule.class)
				.useDefaultSerializerInRam(RAM_MAX_SIZE)
		               .noDisk();

		//To put an object into your cache, simply call put
		DummyClass object = new DummyClass();
 		object = cache.put("mykey", object);

		//To get an object from your cache, simply call get
		DummyClass object = null;
 		object = cache.get("mykey");

3.Architecture:

- _[picasso](https://github.com/square/picasso) --- (From [square](https://github.com/square)) : 
A powerful image downloading and caching library for Android. [图片加载框架,square出品,必属精品]._

	![](https://github.com/square/picasso/raw/master/website/static/sample.png)

There are some libraries let picasso become stronger：

- _[picasso-transformations](https://github.com/wasabeef/picasso-transformations) --- (From [wasabeef](https://github.com/wasabeef)) : 
An Android transformation library providing a variety of image transformations for Picasso. [给picasso添加各种图像效果]._

	<img src="https://github.com/wasabeef/picasso-transformations/raw/master/art/demo-org.jpg" width="52%">![](https://github.com/wasabeef/picasso-transformations/raw/master/art/demo.gif)
	
- _[picasso-transformations](https://github.com/TannerPerrien/picasso-transformations) --- (From [TannerPerrien](https://github.com/TannerPerrien)) : 
A transformation library for Picasso. [给picasso添加各种图像效果]._	

	![](https://github.com/TannerPerrien/picasso-transformations/raw/master/picasso-transformations-sample.png)

- _[PicassoPalette](https://github.com/florent37/PicassoPalette) --- (From [florent37](https://github.com/florent37)) : 
Android Lollipop Palette is now easy to use with Picasso. [picasso&Android L的采色板Palette]._	

	![](https://raw.githubusercontent.com/florent37/PicassoPalette/master/screenshot/nyancat_small_2.png)

- _[CatKit](https://github.com/cesarferreira/CatKit) --- (From [cesarferreira](https://github.com/cesarferreira)) : 
<img src="http://i.imgur.com/fIdwUcw.png" width="2%"> Android kit for cat placeholders. [结合picasso实现图片的占位]._	

	<img src="http://i.imgur.com/YpE8Qfr.png" width="85%">




#### article ####

- _[Percent Support Library: Bring dimension in % to RelativeLayout and FrameLayout](http://inthecheesefactory.com/blog/know-percent-support-library/en) --- (From Author  [nuuneoi](https://github.com/nuuneoi) blog [http://www.nuuneoi.com](http://www.nuuneoi.com/)) --- [No Source]_ 

	It is not a problem anymore since the few days ago on the day Android M is officially announced its name: Marshmallow, Android team launched many Support Library to help developer fighting with fragmentation. One of those is Percent Support Library which add an capbility to set RelativeLayout's and FrameLayout's dimension in % !! [Percent Support Library：带来布局%号权重]. 
 
	Chinese Translation Address : [Thanks To mrfu](http://mrfu.me/android/2015/08/31/percent_support_library/)
	
	![](http://i.imgur.com/YbWyf6E.png)

- _[Architecting Android…The evolution](http://fernandocejas.com/2015/07/18/architecting-android-the-evolution/) --- (From Author  [android10](https://github.com/android10) blog [http://fernandocejas.com](http://fernandocejas.com/)) --- [Source in [Github](https://github.com/android10/Android-CleanArchitecture)]_ 

	Evolution stands for a gradual process in which something changes into a different and usually more complex or better form.
	Said that, software evolves and changes over the time and indeed an architecture. Actually a good software design must help us grow and extend our solution by keeping it healthy without having to rewrite everything.  [Android架构演化之路]. 
 
	Chinese Translation Address : [Thanks To android-tech-frontier](http://www.devtf.cn/?p=1083)
	
	![](https://camo.githubusercontent.com/0bf8c53baf9bf62f8c85b983d49cef4e23539188/687474703a2f2f6665726e616e646f63656a61732e636f6d2f77702d636f6e74656e742f75706c6f6164732f323031352f30372f636c65616e5f6172636869746563747572655f65766f6c7574696f6e2e706e67)


#### website 	

- _[https://tinypng.com](https://tinypng.com/) : Advanced lossy compression for PNG images that preserves full alpha transparency. [在线PNG压缩神器]._

	![](http://i.imgur.com/tNG7Efv.png)

	![](https://img.shields.io/badge/The%20Day5-End%20!-ED1C24.svg?style=flat)

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

- _[A small leak will sink a great ship](https://corner.squareup.com/2015/08/a-small-leak.html) --- (From Author  [Piwai](https://github.com/pyricau) blog [http://www.piwai.info/](http://www.piwai.info/)) --- [No Source]_ 

	This post started as an internal email thread when I was building LeakCanary. I found a strange memory leak and started digging in order to figure out what was happening.
	TL;DR: Prior to Android Lollipop, alert dialogs may cause memory leaks in your Android apps. [Translation：Square工程师 : 一个内存泄漏引发的悲惨结果]. 
 
	Chinese Translation Address : [Thanks To android-tech-frontier](http://www.devtf.cn/?p=1065)

	![](http://i.imgur.com/AHA60WS.png)![](http://i.imgur.com/WpHtwuM.png)

	A super cool man in Android , This is his resume website : [http://www.piwai.info/cv.html#/welcome](http://www.piwai.info/cv.html#/welcome)


#### website 	

- _[https://medium.com/android-news](https://medium.com/android-news) --- (Build By [Evan Williams,2012](https://en.wikipedia.org/wiki/Medium_(publishing_platform))) : Medium is a blog-publishing platform.The platform has evolved into a hybrid of non-professional contributions and professional, paid contributions. [基于主题的协作型媒体Blog文章消费写作平台]._

	![](http://i.imgur.com/wbgsH2m.jpg)

	![](https://img.shields.io/badge/The%20Day3-End%20!-ED1C24.svg?style=flat)


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

- _[http://stackoverflow.com](http://stackoverflow.com/) --- (Build By [Jeff Atwood & Joel Spolsky ,2008](http://stackoverflow.com/)) :Stack Overflow is a question and answer site for professional and enthusiast programmers. [程序猿BUG的维基百科Wiki]._

	![](http://i.imgur.com/2vFzulA.jpg)


	![](https://img.shields.io/badge/The%20Day2-End%20!-ED1C24.svg?style=flat)








----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 
## Day1 
> ![](https://img.shields.io/badge/AndroidEveryday-Day1-green.svg?style=flat)   
> ***Time : October 22th,2015*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[SendEmailAnimation](https://github.com/cooltechworks/SendEmailAnimation) --- (From [cooltechworks](https://github.com/cooltechworks)) : 
This is a small attempt to attract users when they are using in app feature to send out an email. [一个发送Email的动画效果]._

    ![](https://cloud.githubusercontent.com/assets/13122232/10564092/9f6f8be0-75c3-11e5-94bd-801aef62c529.gif)

- _[BitmapMerger](https://github.com/cooltechworks/BitmapMerger) --- (From [cooltechworks](https://github.com/cooltechworks)) : 
Play with bitmaps [bitmaps动画]._

	![](https://cloud.githubusercontent.com/assets/13122232/8438305/9f7c2644-1f82-11e5-8f51-25ba7cca0711.gif)

- _[ZeroGravityAnimation](https://github.com/cooltechworks/ZeroGravityAnimation) --- (From [cooltechworks](https://github.com/cooltechworks)) : 
random object fly on your screen [屏幕随机物件飞动]._

	![](https://cloud.githubusercontent.com/assets/13122232/9293580/3521f486-444e-11e5-9de2-3b9cab9a13f6.gif)

- _[AppIntroAnimation](https://github.com/TakeoffAndroid/AppIntroAnimation) --- (From [TakeoffAndroid](https://github.com/TakeoffAndroid)) : 
AppIntroAnimation is a set of code snippets to make cool intro screen for your app with special Image Translation and Transformation animation effects [一个引导页]._

	![](https://cloud.githubusercontent.com/assets/11768239/9027657/600244d6-397b-11e5-916f-409d4ab3de28.gif)


2.Logic：

- _[smash](https://github.com/appformation/smash) --- (From [appformation](https://github.com/appformation) & Tag  is [Networking](https://github.com/appformation/smash)) : 
Smash is Volley inspired networking library that's using OkHttp in its core [结合OkHttp的类Volley网络请求library]._

	![](https://github.com/appformation/smash/raw/master/assets/logo.png)

- _[ThinDownloadManager](https://github.com/smanikandan14/ThinDownloadManager) --- (From [smanikandan14](https://github.com/smanikandan14) & Tag  is [Networking](https://github.com/smanikandan14)) : 
Thin DownloadManager is an android library primary to download files and to avoid using DOWNLOAD_WITHOUT_NOTIFICATION permission when using Android provided DownloadManager in your application. [一个类volley架构思想的下载框架,无需 DownloadManager permission]._
	
	![](http://i.imgur.com/2PdsasQ.png)


3.Architecture:

- _[Base](https://github.com/thiagokimo/Base) --- (From [thiagokimo](https://github.com/thiagokimo)) : 
Base is a lightweight library that gives you a clean architecture foundation for your Android MVP's [探索MVP架构]._

	![](https://camo.githubusercontent.com/26703d84f95849e173d8c04c05b1708e32ddfc36/687474703a2f2f6b696d6f2e696f2f696d616765732f616e64726f69642d6469616772616d2e706e67)

- _[rx-android-architecture](https://github.com/tehmou/rx-android-architecture) --- (From [tehmou](https://github.com/tehmou)) : An example project of an Android architecture built on RxJava [基于RxJava架构的Simple]._

	![](https://camo.githubusercontent.com/b5024164a5784e6bb2a2857a8af41f4499298051/687474703a2f2f7465686d6f752e6769746875622e696f2f72782d616e64726f69642d6172636869746563747572652f696d616765732f617263686974656374757265322e312e706e67)

- _[EffectiveAndroid](https://github.com/rallat/EffectiveAndroid) --- (From [rallat](https://github.com/rallat)) :This sample project shows how to apply MVP and Clean architecture on an Android app [Twitter工程师rallat的MVP进化之旅]._

	![](https://github.com/rallat/EffectiveAndroid/raw/master/assets/clean.png)



#### article ####

- _[When the Avengers meet Dagger2, RxJava and Retrofit in a clean way](http://saulmm.github.io/when-Thor-and-Hulk-meet-dagger2-rxjava-1/) --- (From Author  [saulmm](https://github.com/saulmm) blog [http://saulmm.github.io](https://github.com/saulmm)) --- [Source in [Github](https://github.com/saulmm/Avengers)]_ 

	Today, if you are an Android developer and don't recognize the words Dagger 2, RxJava or Retrofit, you are missing something, this series will put some focus on giving the basic ideas of how to use these frameworks together with a Clean Architecture perspective. [Translation：当复仇者联盟遇上Dagger2、RxJava和Retrofit的巧妙结合]. 
 
	Chinese Translation Address : [Thanks To android-tech-frontier](http://www.devtf.cn/?p=565)
	
	![](http://i.imgur.com/QWvjQuq.png)![](http://i.imgur.com/8xZuRgm.png)

	### When Avengers meet Dagger2, RxJava & Retrofit in a clean way

	This is the blog's source code of a series focused on giving some basic ideas about how to use [Retrofit](http://square.github.io/retrofit/), [Dagger2](http://google.github.io/dagger/) & [RxJava](https://github.com/ReactiveX/RxJava) together with a [Clean Architecture](http://blog.8thlight.com/uncle-bob/2012/08/13/the-clean-architecture.html).

	##### [Part 1 - Dagger 2](http://saulmm.github.io/when-Thor-and-Hulk-meet-dagger2-rxjava-1/) 

	In this first part it explains how Dagger 2 can help the decoupling of the layers in a project, removing dependencies so that it is easily scalable and testable.

	##### [Part 2 - RxJava, RxAndroid, Reactive Extensions & operators](http://saulmm.github.io/when-Iron-Man-becomes-Reactive-Avengers2/)

	This part focuses on the understanding of what are the Reactive Extensions, its Java implementation, and use RxJava operators, all it integrated with a clean architecture 

- _[Introduce RxJava To Android developer](http://gank.io/post/560e15be2dca930e00da1083) --- (From Author  [rengwuxian](https://github.com/rengwuxian) blog [http://gank.io/](http://gank.io/)) --- [No Source & Translation： 给 Android 开发者的 RxJava 详解]_ 

	我从去年开始使用 RxJava ，到现在一年多了。今年加入了 Flipboard 后，看到 Flipboard 的 Android 项目也在使用 RxJava ，并且使用的场景越来越多 。而最近这几个月，我也发现国内越来越多的人开始提及 RxJava 。有人说『RxJava 真是太好用了』，有人说『RxJava 真是太难用了』，另外更多的人表示：我真的百度了也谷歌了，但我还是想问： RxJava 到底是什么？. 
 
	English translation Address : Have No One translated it At the moment  (If You are interested In this article，please translate it to English).
	
	![](http://i.imgur.com/5w4I6L2.png)


#### website 	

- _[http://gank.io/](http://gank.io/) --- (Build By [daimajia](https://github.com/daimajia)) :To start a serious writing For Android developer [重新开始一次认真的写作]._

	![](http://i.imgur.com/c69XTPO.png)

	![](https://img.shields.io/badge/The%20Day1-End%20!-ED1C24.svg?style=flat)














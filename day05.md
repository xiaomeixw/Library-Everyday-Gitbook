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

	<img src="https://camo.githubusercontent.com/2ea6152b06aa5f9ca21ab7ff0a83830f73f48fbe/68747470733a2f2f6431337961637572716a676172612e636c6f756466726f6e742e6e65742f75736572732f3330333233342f73637265656e73686f74732f323039303830332f70616765696e64696361746f722e676966" width="70%">

- _[rubber-loader](https://github.com/greenfrvr/rubber-loader) --- (From [greenfrvr](https://github.com/greenfrvr)) : 
Android indeterminate loader widget with rubber shape and color transitions. [loading时的橡胶动画效果]._

	<img src="http://i.imgur.com/9ISSPVp.gif" width="70%">

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


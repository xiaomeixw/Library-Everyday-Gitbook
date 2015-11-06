----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 

## Day13
> ![](https://img.shields.io/badge/AndroidEveryday-Day13-green.svg?style=flat)   
> ***Time : November 06st,2015*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[AndroidSwipeableCardStack](https://github.com/wenchaojiang/AndroidSwipeableCardStack) --- (From [wenchaojiang](https://github.com/wenchaojiang)) : 
A tinder like swipeable card stack component. [图片左右滑动]._

    <img src="https://raw.githubusercontent.com/wenchaojiang/AndroidSwipeableCardStack/master/pics/image2.png" width="35%">

- _[TinderView](https://github.com/GadgetCheck/TinderView) --- (From [GadgetCheck](https://github.com/GadgetCheck)) : 
Created a Tinder like Card Deck & Captain Train like Toolbar. [图片左右滑动]._

    <img src="https://camo.githubusercontent.com/b07859d3a8df4095f33daf2d32b38e573c807fa1/687474703a2f2f73342e706f7374696d672e6f72672f783962616d7733796c2f696d6167652e706e67" width="35%"><img src="https://camo.githubusercontent.com/e06c7e6ad7e719116f2f6d670385a2f194b0da95/687474703a2f2f73342e706f7374696d672e6f72672f3762376f67757968392f696d6167652e706e67" width="35%">

- _[MaterialPatternllockView](https://github.com/AmniX/MaterialPatternllockView) --- (From [AmniX](https://github.com/AmniX)) : 
A View which is lookalike Lollipop Pattern View. [九宫格解锁]._

    <img src="https://raw.githubusercontent.com/AmniX/MaterialPatternllockView/master/raw/screen.jpg" width="35%">

- _[android-patternview](https://github.com/geftimov/android-patternview) --- (From [geftimov](https://github.com/geftimov)) : 
Pattern view for android.That one using lock or unlock. [多宫格解锁]._

    <img src="https://github.com/geftimov/android-patternview/raw/master/art/rsz_pattern_correct.png" width="30%"> <img src="https://github.com/geftimov/android-patternview/raw/master/art/rsz_empty_pattern.png" width="30%"> <img src="https://github.com/geftimov/android-patternview/raw/master/art/rsz_mm.png" width="30%">

- _[PatternLock](https://github.com/DreaminginCodeZH/PatternLock) --- (From [DreaminginCodeZH](https://github.com/DreaminginCodeZH)) : 
Android pattern lock library. [九宫格解锁]._

    <img src="https://github.com/DreaminginCodeZH/PatternLock/raw/master/image/sample_small.png" width="35%">

- _[Android-Lock9View](https://github.com/TakWolf/Android-Lock9View) --- (From [TakWolf](https://github.com/TakWolf)) : 
An Android grid lock screen view with a callback interface. [九宫格解锁]._

    <img src="https://github.com/TakWolf/Android-Lock9View/raw/master/art/screenshot.png" width="35%">

2.Logic：

- _[ReactiveNetwork](https://github.com/pwittchen/ReactiveNetwork) --- (From [pwittchen](https://github.com/pwittchen) & Tag  is [Networking](https://github.com/pwittchen/ReactiveNetwork)) : 
Android library listening network connection state and change of the WiFi signal strength with RxJava Observables. [结合RXJava实现的网络状态的监听]._

	<img src="http://i.imgur.com/JKhLfOj.png" width="100%">

- _[NetworkEvents](https://github.com/pwittchen/NetworkEvents) --- (From [pwittchen](https://github.com/pwittchen) & Tag  is [Networking](https://github.com/pwittchen/NetworkEvents)) : 
Android library listening network connection state and change of the WiFi signal strength with event bus. [结合各种EventBus实现的网络状态的监听]._

	<img src="http://i.imgur.com/4HB7bZk.png" width="100%">

3.Architecture:

- _[AndroidSocialNetworks](https://github.com/antonkrasov/AndroidSocialNetworks) --- (From [antonkrasov](https://github.com/antonkrasov)) : 
Library for easy work with Facebook, Twitter, LinkedIn and Google on Android. [封装好的一套使用FB\TW\LN\G的API接口]._

	<p>
	<img src="https://raw.githubusercontent.com/antonkrasov/AndroidSocialNetworks/master/other/asn.png" width="200px" height="200px" align="left" hspace="15px" />
	Android Social Networks is library which makes working with social networks easier.
	If you sometime tried to work with social networks on android you should remember that this is a hell.
	You should read documentation for every social network, download SDK or use some libraries for OAuth and make
	http calls by yourself. This library should makes your life easier, it contains common interface for
	Twitter, LinkedIn, Facebook and Google Plus, just build SocialNetworkManager and configure your AndroidManiferst and you can login users, or post messages or photos or add / remove friends.
	</p>

- _[afinal](https://github.com/yangfuhai/afinal) --- (From [yangfuhai](https://github.com/yangfuhai) A Developer from China) : 
A Library with ioc & orm & http，there are four modules ：FinalAcitivity,FinalBitmap,FinalDb and FinalHttp. [Afinal是一个android的ioc&orm框架]._

	![](https://camo.githubusercontent.com/c6e3b3f79af58e45555a754cf0814f0e5eb32b9a/687474703a2f2f636f64652e676f6f676c652e636f6d2f702f6166696e616c2f6c6f676f3f6363743d31333531353136353335)
	
	FinalDB：
	
		FinalDb db = FinalDb.create(this);
		User user = new User(); //need id or use @ID
		user.setEmail("mail@tsz.net");
		user.setName("michael yang");
		db.save(user);

	FinalActivity:
	
		@ViewInject(id=R.id.button,click="btnClick") Button button;
	    @ViewInject(id=R.id.textView) TextView textView;

	FinalHttp:
	
		FinalHttp fh = new FinalHttp();
	    fh.get("http://www.yangfuhai.com", callback);

	FinalBitmap:
	
		FinalBitmap fb = FinalBitmap.create(this);
		fb.display(iv,Images.imageUrls[position]);

#### App-Demo ####

- _[9GAG](https://github.com/stormzhang/9GAG) --- (From [stormzhang](https://github.com/stormzhang) A Developer from China) : 
Android unofficial REST Client of 9GAG. [使用众多知名library实现的app-demo]._

	<img src="https://camo.githubusercontent.com/14097fc0e119ead1fd4777e9f3c317319dd15380/687474703a2f2f7777342e73696e61696d672e636e2f6d77313032342f6166363363306533677731656738616866346231796a32316b7730737a7163382e6a7067" width="100%">

	Check the Source in [Github](https://github.com/stormzhang/9GAG).Want to know more about the App-Demo download [APK](https://github.com/stormzhang/9GAG/releases/download/v1.0.0/9GAG_v1.0.0.apk)

	## the APP-Demo With these Open source projects

	* [Volley](https://android.googlesource.com/platform/frameworks/volley)
	
	* [ButterKnife](http://jakewharton.github.io/butterknife/)
	
	* [UniversalImageLoader](https://github.com/nostra13/Android-Universal-Image-Loader)
	
	* [ListViewAnimations](https://github.com/nhaarman/ListViewAnimations)
	
	* [NineOldAndroid](http://nineoldandroids.com/)
	
	* [PhotoView](https://github.com/chrisbanes/PhotoView)
	
	* [FoldingLayout](https://github.com/tibi1712/Folding-Android)
	
	* [ProgressWheel](https://github.com/Todd-Davies/ProgressWheel)
	
	* [AndroidStaggeredGrid](https://github.com/etsy/AndroidStaggeredGrid)

	* [BlurEffectForAndroidDesign](https://github.com/PomepuyN/BlurEffectForAndroidDesign)
	
	* [Shimmer-android](https://github.com/RomainPiel/Shimmer-android)
	
	* [Titanic](https://github.com/RomainPiel/Titanic)

#### article ####

- _[Getting Started with RxJava and Android](http://www.captechconsulting.com/blogs/getting-started-with-rxjava-and-android) --- (From Author  [alex-townsend](https://github.com/saulmm) blog [http://www.captechconsulting.com/](http://www.captechconsulting.com/)) --- [Source in [Github](https://github.com/alex-townsend/GettingStartedRxAndroid)]_ 

	<p>
	<img src="http://i.imgur.com/9ADH9hP.png" width="200px" height="200px" align="left" hspace="15px" />
	ReactiveX is an API that focuses on asynchronous composition and manipulation of observable streams of data or events by using a combination of the Observer pattern, Iterator pattern, and features of Functional Programming. Handling real-time data is a common occurrence, and having an efficient, clean, and extensible approach to handling these scenarios is important. Using Observables and operators to manipulate them, ReactiveX offers a composable and flexible API to create and act on streams of data while simplifying the normal concerns of asynchronous programming like thread creation and concurrency issues.[Translation：开始使用RxJava]
	</p>

	Chinese Translation Address : Waiting for someone Translation it.

	<img src="http://i.imgur.com/Q77N5dJ.png" width="100%">


	![](https://img.shields.io/badge/The%20Day13-End%20!-ED1C24.svg?style=flat)














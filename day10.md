----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 

## Day10
> ![](https://img.shields.io/badge/AndroidEveryday-Day10-green.svg?style=flat)   
> ***Time : October 31th,2015*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[GestureViews](https://github.com/alexvasilkov/GestureViews) --- (From [alexvasilkov](https://github.com/alexvasilkov)) : 
ImageView and FrameLayout with gestures control and position animation. [手势控制图片查看]._

    <img src="https://github.com/alexvasilkov/GestureViews/raw/master/sample/art/demo.gif" width="35%">

- _[MaskProgressView](https://github.com/iammert/MaskProgressView) --- (From [iammert](https://github.com/iammert)) : 
Yet another android custom progress view for your music player. [音乐进读条]._

    <img src="https://raw.githubusercontent.com/iammert/MaskProgressView/master/art/art.png" width="65%"> 

- _[MusicPlayerView](https://github.com/iammert/MusicPlayerView) --- (From [iammert](https://github.com/iammert)) : 
Android custom view and progress for music player,A good simple to learn custom view. [音乐播放旋转效果,是学习自定义View的非常好的范例]._

    <img src="https://raw.githubusercontent.com/iammert/MusicPlayerView/master/art/art2.gif" width="35%"> 

- _[InteractivePlayerView](https://github.com/iammert/InteractivePlayerView) --- (From [iammert](https://github.com/iammert)) : 
Custom android music player view. [作者的又一个自定义音乐播放view]._

    <img src="https://raw.githubusercontent.com/iammert/InteractivePlayerView/master/art/art.png" width="65%">

- _[PhotoPicker](https://github.com/donglua/PhotoPicker) --- (From [donglua](https://github.com/donglua)) : 
A picture pick and view library like chinese what'app : wechat. [类似微信的图片选择、预览组件]._

    <img src="https://camo.githubusercontent.com/37d5d2dd5d523c06979fdd1c160ceb6044bf4ead/687474703a2f2f7777322e73696e61696d672e636e2f6c617267652f35653961383164626777316574726135697538306c6a3230367a3063657438722e6a7067" width="35%"><img src="https://camo.githubusercontent.com/d250513e87edf279ef8a4df874f46613216a063e/687474703a2f2f7777322e73696e61696d672e636e2f6c617267652f3565396138316462677731657472613631726e72396a3230367a3063653379752e6a7067" width="35%">   

	<img src="https://camo.githubusercontent.com/fdfbd6a029ad0f17e8cb782b1fc2cc579ca99e19/687474703a2f2f7777342e73696e61696d672e636e2f6c617267652f3565396138316462677731657472613665666c31686a3230367a3063657765742e6a7067" width="35%"><img src="https://camo.githubusercontent.com/065515c927ed02a3dd5dac50da4b5fdeb598cbcd/687474703a2f2f7777332e73696e61696d672e636e2f6c617267652f35653961383164626777316574726136713265647a6a3230367a3063656467672e6a7067" width="35%">  

- _[bubbles-for-android](https://github.com/txusballesteros/bubbles-for-android) --- (From [txusballesteros](https://github.com/txusballesteros)) : 
Bubbles for Android is an Android library to provide chat heads capabilities on your apps. With a fast way to integrate with your development. [桌面展示头像view]._

    <img src="https://github.com/txusballesteros/bubbles-for-android/raw/master/assets/bubbles_demo.gif" width="35%">

2.Logic：

- _[SharedPreferencesGenerator](https://github.com/noties/SharedPreferencesGenerator) --- (From [noties](https://github.com/noties) & Tag  is [Annotation ](https://github.com/noties/SharedPreferencesGenerator)) : 
Android annotation based SharedPreferences Generator. [编译时注解,实现SharedPreferences]._

	<img src="http://i.imgur.com/l7X4t5D.png" width="90%">

		@SPGPreference
		class Simplest {
		    String someString;
		    long someLong;
		    int someInt;
		    boolean someBool;
		}

		@SPGPreference(imports = "com.example.SomeClass")
		public class MyPrefs {
		    @SPGKey(defaultValue = "${SomeClass.getString()}")
		    String someKey;
		}

- _[dexposed](https://github.com/alibaba/dexposed) --- (From [alibaba](https://github.com/alibaba) & Tag  is [AOP](https://github.com/alibaba/dexposed)) : 
dexposed enable 'god' mode for single android application, can hotfix app and Performance Monitoring,base on xposed. [Android平台免Root无侵入AOP框架,性能监控、在线热补丁]._

	<img src="http://i.imgur.com/DHGYpWE.png" width="90%">

		//application：initialization 
		public class MyApplication extends Application {
	        @Override public void onCreate() {        
	            // Check whether current device is supported (also initialize Dexposed framework if not yet)
	            if (DexposedBridge.canDexposed(this)) {
	                // Use Dexposed to kick off AOP stuffs.
	                ...
	            }
	        }
	        ...
	    }
		
		//Basic usage
		DexposedBridge.findAndHookMethod(Activity.class, "onCreate", Bundle.class, new XC_MethodReplacement() {

            @Override protected Object replaceHookedMethod(MethodHookParam param) throws Throwable {
                // Re-writing the method logic outside the original method context is a bit tricky but still viable.
                ...
            }

        });
		
	Follow is support status.

	Runtime | Android Version | Support
	------  | --------------- | --------
	Dalvik  | 2.2             | Not Test
	Dalvik  | 2.3             | Yes
	Dalvik  | 3.0             | No
	Dalvik  | 4.0-4.4         | Yes
	ART     | 5.0             | Testing
	ART     | 5.1             | No
	ART     | M               | No

- _[Paper](https://github.com/pilgr/Paper) --- (From [pilgr](https://github.com/pilgr) & Tag  is [Caching](https://github.com/pilgr/Paper)) : 
Paper is a fast NoSQL data storage for Android that lets you save/restore Java objects by using efficient Kryo serialization and handling data structure changes automatically. [NoSQL型数据存取]._

	<img src="http://i.imgur.com/sq570pd.png" width="90%">

		//application：Initialize Paper
		Paper.init(context);

		//Save:
		Paper.book().write("city", "Lund"); // Primitive
		Paper.book().write("task-queue", queue); // LinkedList
		Paper.book().write("countries", countryCodeMap); // HashMap

		//Read
		String city = Paper.book().read("city");
		LinkedList queue = Paper.book().read("task-queue");
		HashMap countryCodeMap = Paper.book().read("countries");

	Running [Benchmark](https://github.com/pilgr/Paper/blob/master/paperdb/src/androidTest/java/io/paperdb/benchmark/Benchmark.java) on Nexus 4, in ms:

	| Benchmark                 | Paper    | [Hawk](https://github.com/orhanobut/hawk) | [sqlite](http://developer.android.com/reference/android/database/sqlite/package-summary.html) |
	|---------------------------|----------|----------|----------|
	| Read/write 500 contacts   | 187      | 447      |          |
	| Write 500 contacts        | 108      | 221      |          |
	| Read 500 contacts         | 79       | 155      |          |


3.Architecture:

- _[xUtils](https://github.com/wyouflf/xUtils) --- (From [wyouflf](https://github.com/wyouflf) A developer from China) : 
 a lightweight Android Architecture with  orm/bitmap/http/view inject. One Line can call API. [一个android框架,含有:Http/View/DB/Bitmap,一行代码调用]._

	<img src="http://i.imgur.com/sKUKNgZ.png" width="90%"> 

		//DbUtils:
		DbUtils db = DbUtils.create(this);
		db.save(user);
	
		//ViewUtils:
		@ViewInject(R.id.textView)
		TextView textView;

		//HttpUtils:Get
		HttpUtils http = new HttpUtils();
		http.send(HttpRequest.HttpMethod.GET,
		    "http://www.lidroid.com",
		    new RequestCallBack<String>(){
		        @Override
		        public void onLoading(long total, long current, boolean isUploading) {
		            testTextView.setText(current + "/" + total);
		        }
		
		        @Override
		        public void onSuccess(ResponseInfo<String> responseInfo) {
		            textView.setText(responseInfo.result);
		        }
		
		        @Override
		        public void onStart() {
		        }
		
		        @Override
		        public void onFailure(HttpException error, String msg) {
		        }
		});

		//BitmapUtils：
		BitmapUtils bitmapUtils = new BitmapUtils(this);
		bitmapUtils.display(testImageView, "http://bbs.lidroid.com/static/image/common/logo.png");



#### article ####

- _[FRAGMENTARGS](http://hannesdorfmann.com/android/fragmentargs/) --- (From Author  [sockeqwe](https://github.com/sockeqwe) blog [http://hannesdorfmann.com](http://hannesdorfmann.com/)) --- [Source in [Github](https://github.com/sockeqwe/fragmentargs)]_ 

	Developing for Android is sometimes painful. You have to write lot of code to do simple things like setting up a Fragment. Fortunately java supports a powerful tool: Annotation Processors. 

	The Problem with Fragments is that you have to set arguments (the parameters) for a fragment to make them work correctly. Many new android developers that write the first fragment do something like this:[Translation：FragmentArgs(让你的Fragment的代码更少)讲解]. 
 
	Chinese Translation Address : [Thanks To KEVIN_CHEN](http://blog.csdn.net/dkdjfkdjfk/article/details/42295107)

	<img src="http://i.imgur.com/Dxc6WSR.png" width="90%"> 

	<img src="http://i.imgur.com/ttvUWyz.png" width="90%"> 

#### App-Demo ####

- _[android-UniversalMusicPlayer](https://github.com/googlesamples/android-UniversalMusicPlayer) --- (From [googlesamples](https://github.com/googlesamples) ) : 
This sample shows how to implement an audio media app that works across multiple form factors and provide a consistent user experience on Android phones, tablets, Auto, Wear and Cast devices. [一个google开源音乐播放器,适配不同的安卓系统环境,手机、手表和web端]._

	<img src="https://github.com/googlesamples/android-UniversalMusicPlayer/raw/master/screenshots/phone.png" width="35%"><img src="https://github.com/googlesamples/android-UniversalMusicPlayer/raw/master/screenshots/phone_lockscreen.png" width="35%">

	<img src="https://github.com/googlesamples/android-UniversalMusicPlayer/raw/master/screenshots/android_tv.png" width="90%">

	<img src="https://github.com/googlesamples/android-UniversalMusicPlayer/raw/master/screenshots/android_wear_1.png" width="35%"><img src="https://github.com/googlesamples/android-UniversalMusicPlayer/raw/master/screenshots/android_wear_2.png" width="35%">

	Check the Source in [Github](https://github.com/googlesamples/android-UniversalMusicPlayer).

#### Video ####

- _[Animation to Guide Us All](https://www.youtube.com/watch?v=SwcJu6fnwjo) --- (From [touchlab](https://www.youtube.com/channel/UC_LIW0OUdsRI21D0xnWkexw) on Youtube) : 
Animation to Guide Us All - How animations can improve the User Experience of your application[2015 Droidcon NYC开发者大会,聚焦Android-material design动画表现形态的演讲视频]._

	<img src="http://i.imgur.com/Qkdv13U.png" width="90%">

	<img src="http://i.imgur.com/vPn8zMY.png" width="90%">

	<img src="http://i.imgur.com/SKliMXJ.png" width="90%">


#### website 	

- _[www.youtube.com](https://www.youtube.com) --- (Build By [Steve Chen&Chad Hurley&Jawed Karim](https://en.wikipedia.org/wiki/YouTube),February 14, 2005) :YouTube is a video-sharing website headquartered in San Bruno, California, United States. The service was created by three former PayPal employees in February 2005. In November 2006, it was bought by Google for US$1.65 billion. YouTube now operates as one of Google's subsidiaries. [全球最大视频分享网站]._

	<img src="http://i.imgur.com/KAQxenH.jpg" width="90%"> 

	![](https://img.shields.io/badge/The%20Day10-End%20!-ED1C24.svg?style=flat)



----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 

## Day17
> ![](https://img.shields.io/badge/AndroidEveryday-Day17-green.svg?style=flat)   
> ***Time : November 21th,2015*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[DWCinemaAnimation-Android](https://github.com/DavidWangTM/DWCinemaAnimation-Android) --- (From [DavidWangTM](https://github.com/DavidWangTM)) : 
An Android native implementation of a Cinema Animation Application. [电影购票的动效实现]._

    <img src="https://raw.githubusercontent.com/DavidWangTM/DWCinemaAnimation-Android/master/animation.gif" width="35%">

- _[DWCorePhoto_Android](https://github.com/DavidWangTM/DWCorePhoto_Android) --- (From [DavidWangTM](https://github.com/DavidWangTM)) : 
use rebound,nineoldandroids,universalimageloader achieve photolibrary like photoview. [图片点击滑动缩放操作]._

    <img src="https://raw.githubusercontent.com/DavidWangTM/DWCorePhoto_Android/master/GridShow.gif" width="35%">

- _[Blurry](https://github.com/wasabeef/Blurry) --- (From [wasabeef](https://github.com/wasabeef)) : 
Blurry is an easy blur library for Android. [图片高斯效果]._

    <img src="https://github.com/wasabeef/Blurry/raw/master/art/blurry.gif" width="35%">

- _[android-stackblur](https://github.com/kikoso/android-stackblur) --- (From [kikoso](https://github.com/kikoso)) : 
Android StackBlur is a library that can perform a blurry effect on a Bitmap based on a gradient or radius, and return the result. The library is based on the code of Mario Klingemann. [图片高斯效果]._

    <img src="https://camo.githubusercontent.com/821ae0abdf62af50624fc429f79b2d47f4f22d53/68747470733a2f2f7261772e6769746875622e636f6d2f6b696b6f736f2f616e64726f69642d737461636b626c75722f6d61737465722f6172742f73637265656e73686f74322e706e67" width="90%">

- _[GaussPager](https://github.com/kot32go/GaussPager) --- (From [kot32go](https://github.com/kot32go)) : 
blur effect with scroll. [高斯模糊渐变的滑动效果]._

    <img src="https://camo.githubusercontent.com/e8bf04872a33ebdbeae018d05c3d2a7634e90a56/687474703a2f2f696d61676531372d632e706f636f2e636e2f6d79706f636f2f6d7970686f746f2f32303135303930362f31372f31373432353430333732303135303930363137303331373031335f3634302e6a70673f333030783437355f313130" width="35%">

2.Logic：

- _[rx-realm](https://github.com/mulab/rx-realm) --- (From [mulab](https://github.com/mulab) & Tag  is [NoSQL](https://github.com/mulab/rx-realm)) : 
A lightweight wrapper around realm-java, which introduces reactive stream semantics to SQL operations. (Inspired by square/sqlbrite). [RXjava结合NoSql存储方案]._

	<img src="http://i.imgur.com/U1XTCQs.png" width="90%">

		//Query
		RealmDatabase.createQuery(new Query()<Foo>{
		    @Override
		    public RealmResults<Foo> call(Realm realm) {
		        return realm.where(Foo.class).findAll();
		    }
		}, Foo.class).subscribe(this);
	
		//Exec
		RealmDatabase.exec(new Exec() {
	    @Override
		    public void run(Realm realm) {
		        realm.where(Foo.class).findAll().clear();
		    }
		}, Foo.class).subscribe(this);

- _[MaterialColdStart](https://github.com/DreaminginCodeZH/MaterialColdStart) --- (From [DreaminginCodeZH](https://github.com/DreaminginCodeZH) & Tag  is [System](https://github.com/DreaminginCodeZH/MaterialColdStart)) : 
Utilize the window background during cold start time to make your app look faster. [冷启动,加速APP启动速度]._

	<img src="https://github.com/DreaminginCodeZH/MaterialColdStart/raw/master/preview/blank_cold_start.gif" width="35%"><img src="https://github.com/DreaminginCodeZH/MaterialColdStart/raw/master/preview/material_cold_start.gif" width="35%">

	<img src="https://github.com/DreaminginCodeZH/MaterialColdStart/raw/master/preview/normal_case.gif" width="70%">

		//Make a new theme for your main activity
		<style name="AppTheme.MaterialColdStart">
		    <item name="android:windowBackground">@drawable/window_background_statusbar_toolbar_tab</item>
		</style>
	
		//And set the new theme in your AndroidManifest.xml
		<activity
		    android:name=".MainActivity"
		    android:theme="@style/AppTheme.MaterialColdStart">
		
		    <intent-filter>
		        <action android:name="android.intent.action.MAIN" />
		        <category android:name="android.intent.category.LAUNCHER" />
		    </intent-filter>
		</activity>

- _[medescope](https://github.com/bemobi/medescope) --- (From [bemobi](https://github.com/bemobi) & Tag  is [Download](https://github.com/bemobi/medescope)) : 
This a is a ready-to-use library that encapsulate the Android Download Manager. Using an interface you can easily connect to your Activity or Fragment and used it. It runs on other process as an independent service. [异步线程下载方案]._

	<img src="http://i.imgur.com/UAjNXZh.png" width="90%">

		Medescope
		        .getInstance(this)
		            .enqueue("DOWNLOAD_ID",
		                "http://somefileiwanttodownload.com/file",
		                "file_name",
		                "Name that you appear on notification",
		                "{some:'samplejson'}"
		                );

- _[AspectLogger](https://github.com/shaunkawano/AspectLogger) --- (From [shaunkawano](https://github.com/shaunkawano) & Tag  is [Annotation ](https://github.com/shaunkawano/AspectLogger)) : 
Simple aspect oriented annotation debugging library for Android development. [结合注解实现Log展示]._

	<img src="http://i.imgur.com/9Yst6gq.png" width="90%">

		//Use @Reveal
		@Reveal
	    private static void toJson() {
	        String json = "";
	        for (int i = 0; i < 1000; i++) {
	            json = GSON.toJson(newObject());
	        }
	    }

		//logcat
	  	V/AspectRevealer﹕ MainActivity#toJson :: [62 ms]

3.Architecture:

- _[Presentation](https://github.com/StanKocken/Presentation) --- (From [StanKocken](https://github.com/StanKocken)) : 
An architecture for Android as a replacement of MVC. [探索MVC架构]._

	<img src="https://raw.githubusercontent.com/StanKocken/Presentation/master/img_references.png" width="90%">

		//Each public method of the modules are defined into an interface:
		public interface FormDef {
		
		    interface IPresenter extends Base.IPresenter {
		
		        void onClickSaveButton(String value);
		    }
		
		    interface IDataProvider extends Base.IDataProvider {
		
		        String getValueSaved();
		
		        void saveValue(String value);
		    }
		
		    interface IView extends Base.IView {
		
		        void setValueSaved(String text);
		    }
		
		}

- _[PermissionHelper](https://github.com/k0shk0sh/PermissionHelper) --- (From [k0shk0sh](https://github.com/k0shk0sh)) : 
Android Library to help you with your runtime Permissions. [Android M动态权限管理]._

	Nexus 6 (M):

	<img src="https://camo.githubusercontent.com/acdedd12c3dcef45a80dc62f6632d50a0536468b/68747470733a2f2f7261772e6769746875622e636f6d2f6b3073686b3073682f5065726d697373696f6e48656c7065722f6d61737465722f6172742f6e65787573362e6a7067" width="90%">

	Nexus 7 (L):

	<img src="https://camo.githubusercontent.com/d2951454bd3842d346323bbdcb0b0f87d9374b64/68747470733a2f2f7261772e6769746875622e636f6d2f6b3073686b3073682f5065726d697373696f6e48656c7065722f6d61737465722f6172742f6e65787573372e6a7067" width="90%">

	Nexus 10 (L)

	<img src="https://camo.githubusercontent.com/bb0af5050c4d72e19a86cb782bfe3d2a2a55a138/68747470733a2f2f7261772e6769746875622e636f6d2f6b3073686b3073682f5065726d697373696f6e48656c7065722f6d61737465722f6172742f6e6578757331302e6a7067" width="90%">
	
#### App-Demo ####

- _[GankIO](https://github.com/maoruibin/GankIO) --- (From [maoruibin](https://github.com/maoruibin) A Developer from China) : 
Simple Girls Client Use MVP. [使用MVP架构写的简易版妹纸客户端]._

	<img src="https://github.com/maoruibin/GankIO/raw/master/art/gank_index.png" width="90%">

	Check the Source in [Github](https://github.com/stormzhang/9GAG).Want to know more about the App-Demo download [APK](https://github.com/stormzhang/9GAG/releases/download/v1.0.0/9GAG_v1.0.0.apk)

	#### the app-demo with these open source projects

	- _RxJava_
	- _OkHttp_
	- _Picasso_
	- _Retrofit_
	- _Logger_

- _[GankIO](https://github.com/maoruibin/GankIO) --- (From [maoruibin](https://github.com/maoruibin) A Developer from China) : 
Simple Girls Client Use MVP. [使用MVP架构写的简易版妹纸客户端]._

	<img src="https://github.com/maoruibin/GankIO/raw/master/art/gank_index.png" width="90%">

	Check the Source in [Github](https://github.com/stormzhang/9GAG).Want to know more about the App-Demo download [APK](https://github.com/stormzhang/9GAG/releases/download/v1.0.0/9GAG_v1.0.0.apk)

	#### the app-demo with these open source projects

	- _RxJava_
	- _OkHttp_
	- _Picasso_
	- _Retrofit_
	- _Logger_

#### resource ####

- _[react-native-guide](https://github.com/ele828/react-native-guide) --- (From [ele828](https://github.com/ele828) A Developer from China) : 
Awesome React-Native Study resource. [React-Native学习资料]._

	![](http://i.imgur.com/q4jEC5S.png)

#### article ####

- _[Prism Fundamentals](https://blog.stylingandroid.com/prism-fundamentals-part-1/) --- (From Author  [Styling Android](https://github.com/StylingAndroid) blog [https://blog.stylingandroid.com](https://blog.stylingandroid.com)) --- [Source in [Github](https://github.com/StylingAndroid/Prism)]_ 

	<p>
	<img src="http://i.imgur.com/GH1do6k.png" width="150px" height="150px" align="left" hspace="15px" />
	I am extremely excited to announce the release of Prism – an all-new dynamic theming library for Android. This is an initial release to get the basic functionality out there, but it is already pretty powerful. However there are some exciting additions in the pipeline which will make it more powerful still. In this series of articles we’ll cover the various aspects of prism to enable you to make use of it and even extend it yourself to meet the requirements of your project.
	Before we begin – a little background. I didn’t set out to create a library. I was working on some code for a series of Styling Android posts around dynamic UI colouring based upon a ViewPager. While writing this code, I refactored it in to easy to explain components which would easy to write about. Following this refactoring I saw quite a clean API emerging and it was from this that the concept of Prism began to emerge. I showed it to a couple of people whose opinion I value and they agreed that it looked a nice, clean, simple API. I then started the process of turing it in to a library and kept referring back the the API and felt that I was adding lots of power without making the API any more complex. So now the time to release it!
	</p>

	[Translation：Android主题动态切换]. 
 
	Chinese Translation Address : [Thanks To android-tech-frontier](http://www.devtf.cn/?p=1056)
	
	<img src="http://i.imgur.com/R562pLW.png" width="90%">

	<img src="http://i.imgur.com/NXmVTKz.png" width="90%">

	<img src="http://i.imgur.com/JWIVc15.gif" width="90%">

	![](https://img.shields.io/badge/The%20Day17-End%20!-ED1C24.svg?style=flat)















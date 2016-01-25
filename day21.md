----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 

## Day21
> ![](https://img.shields.io/badge/AndroidEveryday-Day21-green.svg?style=flat)   
> ***Time : Jan 25th,2016*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[XhsEmoticonsKeyboard](https://github.com/w446108264/XhsEmoticonsKeyboard) --- (From [w446108264](https://github.com/w446108264)) : 
android emoticonsKeyboard support emoji and user-defined emoticon. easy to integrated into your project. [emoji表情]._

    <img src="https://raw.githubusercontent.com/w446108264/XhsEmoticonsKeyboard/master/output/simple.png" width="32%">

- _[MagicViews](https://github.com/ikocijan/MagicViews) --- (From [ikocijan](https://github.com/ikocijan)) : 
Set custom font in Android application. [Android字体设置]._

    <img src="https://camo.githubusercontent.com/26f40d6e55b84289b77464068ad743e90027c643/68747470733a2f2f7261772e6769746875622e636f6d2f696b6f63696a616e2f4d6167696356696577732f6d61737465722f73637265656e73686f742e6a7067" width="32%"><img src="https://camo.githubusercontent.com/1d8460e3cdd22442ee0a9a1a08899f8243eea6c9/68747470733a2f2f7261772e6769746875622e636f6d2f696b6f63696a616e2f4d6167696356696577732f6d61737465722f73637265656e73686f6f745f322e706e67" width="32%">

- _[Dragger](https://github.com/ppamorim/Dragger) --- (From [ppamorim](https://github.com/ppamorim)) : 
Animate your activity. [Activity跳转动起来]._

    <img src="https://github.com/ppamorim/Dragger/raw/master/art/app_sample_uncompressed.gif?raw=true" width="90%">

- _[SmartTabLayout](https://github.com/ogaclejapan/SmartTabLayout) --- (From [ogaclejapan](https://github.com/ogaclejapan)) : 
A custom ViewPager title strip which gives continuous feedback to the user when scrolling. [TabLayout]._

    <img src="https://raw.githubusercontent.com/ogaclejapan/SmartTabLayout/master/art/demo1.gif" width="32%"><img src="https://raw.githubusercontent.com/ogaclejapan/SmartTabLayout/master/art/demo4.gif" width="32%"><img src="https://raw.githubusercontent.com/ogaclejapan/SmartTabLayout/master/art/demo1.gif" width="32%">

2.Logic：

- _[indirect-injector](https://github.com/sys1yagi/indirect-injector) --- (From [sys1yagi](https://github.com/sys1yagi) & Tag  is [Injector](https://github.com/sys1yagi/indirect-injector)) : 
The indirect-injector simplify confusion of communication between activity and fragment, and dependencies. [注入框架]._

	<img src="https://camo.githubusercontent.com/a6dfa644893ae682cee072aa9772f339b168d03e/68747470733a2f2f7261772e6769746875622e636f6d2f73797331796167692f696e6469726563742d696e6a6563746f722f6d61737465722f6172742f70726f626c656d2e706e67" width="32%">

Activity：

		public class MainActivity extends FragmentActivity {
		
		  ItemListFragment.Callbacks mCallback = new ItemListFragment.Callbacks() {
		    @Override
		    public void onItemSelected(int id) {
		        //Called from fragment.
		    }
		  }
		
		  @Override
		  protected void onCreate(Bundle savedInstanceState) {
		    super.onCreate(savedInstanceState);
		
		    IndirectInjector.addDependency(this, mCallback);
		
		    //initialize
		    //...
		 }

Fragment：

		public class ItemListFragment extends ListFragment {
		
		  public interface Callbacks {
		    public void onItemSelected(int id);
		  }
		
		  @Inject
		  private Callbacks mCallbacks;
		
		  @Override
		  public void onActivityCreated(Bundle savedInstanceState) {
		    super.onActivityCreated(savedInstanceState);
		
		    IndirectInjector.inject(getActivity(), this);
		
		    mCallbacks.onItemSelected(0);
		  }
		}


3.Architecture:

- _[anvil](https://github.com/zserge/anvil) --- (From [zserge](https://github.com/zserge)) : 
A minimal reactive UI library for Android. [一套reactive方案的UI书写架构]._

	<img src="http://i.imgur.com/JVIQ2BD.png" width="90%">

		public int ticktock = 0;
		public void onCreate(Bundle b) {
		    super.onCreate(b);
		    setContentView(new RenderableView(this) {
		        @Override
		        public void view() {
		            linearLayout(() -> {
		                size(MATCH, MATCH);
		                padding(dip(8));
		                orientation(LinearLayout.VERTICAL);
		
		                textView(() -> {
		                    size(MATCH, WRAP);
		                    text("Tick-tock: " + ticktock);
		                });
		
		                button(() -> {
		                    size(MATCH, WRAP);
		                    text("Close");
		                    // Finish current activity when the button is clicked
		                    onClick(v -> finish());
		                });
		            });
		        }
		    });
		}

#### App-Demo ####

- _[Qiitanium](https://github.com/ogaclejapan/Qiitanium) --- (From [ogaclejapan](https://github.com/ogaclejapan) Qiitanium is an unofficial Android application of Qiita. [非日本官方Qiita客户端]._

	<img src="https://raw.githubusercontent.com/ogaclejapan/Qiitanium/master/art/qiitanium.gif" width="45%">

	Check the Source in [Github](https://github.com/ogaclejapan/Qiitanium).Want to know more about the App-Demo see [qiita of Janpan](https://qiita.com/)

	#### the app-demo with these open source projects

		  compile fileTree(dir: 'libs', include: ['*.jar'])
		
		  // Android support library
		  compile 'com.android.support:appcompat-v7:22.1.+'
		  compile 'com.android.support:support-v4:22.1.+'
		  compile 'com.android.support:support-v13:22.0.+'
		
		  // DI
		  compile 'com.google.dagger:dagger:2.0'
		  apt 'com.google.dagger:dagger-compiler:2.0'
		  provided 'org.glassfish:javax.annotation:10.0-b28'
		
		  // Logger
		  compile 'com.jakewharton.timber:timber:3.1.0'
		
		  // HTTP client
		  compile 'com.squareup.okhttp:okhttp:2.3.0'
		  compile 'com.squareup.okhttp:okhttp-urlconnection:2.3.0'
		
		  // Image downloader & transformer
		  compile 'com.squareup.picasso:picasso:2.5.2'
		  compile 'com.makeramen:roundedimageview:2.0.1'
		
		  // JSON library
		  compile 'com.google.code.gson:gson:2.3.1'
		
		  // Reactive library
		  compile 'io.reactivex:rxjava:1.0.10'
		  compile 'com.ogaclejapan:rxbinding:1.1.1@aar'
		
		  // View library
		  compile 'com.ogaclejapan.arclayout:library:1.0.1@aar'
		  compile 'com.ogaclejapan.smarttablayout:library:1.1.3@aar'
		  compile 'com.ogaclejapan.smarttablayout:utils-v13:1.1.3@aar'
		  compile 'com.twotoasters.jazzylistview:library:1.2.1'
		  compile 'com.sothree.slidinguppanel:library:3.0.0@aar'
		  compile 'com.nispok:snackbar:2.10.8'
		
		  // Custom font library
		  compile 'com.norbsoft.typefacehelper:library:0.9.0@aar'
		
		  // HTML Parser
		  compile 'org.jsoup:jsoup:1.8.1'
		
		  // Crash analytics
		  compile('com.crashlytics.sdk.android:crashlytics:2.2.0@aar') {
		    transitive = true;
		  }
		
		  // Memory leak detection
		  debugCompile 'com.squareup.leakcanary:leakcanary-android:1.3'
		  releaseCompile 'com.squareup.leakcanary:leakcanary-android-no-op:1.3.1'
		
		  // Debug bridge
		  debugCompile 'com.facebook.stetho:stetho:1.1.1'
		  debugCompile 'com.facebook.stetho:stetho-okhttp:1.1.1'
		  debugCompile 'com.facebook.stetho:stetho-timber:1.1.1'



#### resource ####

- _[awesome-android-ui](https://github.com/wasabeef/awesome-android-ui) --- (From [wasabeef](https://github.com/wasabeef) A curated list of awesome Android UI/UX libraries. [Android UI 开源控件]._

	![](http://i.imgur.com/9t0ZLtv.png)

- _[android-open-project](https://github.com/Trinea/android-open-project) --- (From [Trinea](https://github.com/Trinea) Collect and classify android open source projects. [Android 开源项目分类汇总]._

	![](http://i.imgur.com/oFXb848.png)

#### article ####

- _[Introducing uCrop, Our Own Image Cropping Library for Android ](https://yalantis.com/blog/introducing-ucrop-our-own-image-cropping-library-for-android/) --- (From Author  [yalantis](https://github.com/yalantis) blog [https://yalantis.com/blog/](https://yalantis.com/blog/)) --- [Source in [Github](https://github.com/Yalantis/uCrop)]_ 

	<p>
	<img src="http://i.imgur.com/7bLM5eo.png" width="150px" height="150px" align="left" hspace="15px" />
	We develop lots of different Android apps at Yalantis, and our experience shows that almost every application we deal with needs image cropping functionality. Image cropping can be used for various purposes, from ordinary adjustment of user profile images to more complex features that involve aspect ratio cropping and flexible image transformations.

	Since we want to provide all our customers with the best set of tools for image editing functionality, we decided to create uCrop, an image cropping library for Android.

	You might be wondering why we couldn’t just use one of the existing solutions for image cropping for Android. After all, you can find lots of them on Github and on the Android Arsenal. But here is the thing: none of these solutions could satisfy our requirements. Let’s take a quick look at the most popular open-source image cropping libraries and explain why they don’t quite fit the bill.
	</p>

	[Translation：uCrop介绍，我们自己的安卓版图片裁剪库]. 
 
	Chinese Translation Address : [Thanks To jcodecraeer](http://jcodecraeer.com/a/anzhuokaifa/androidkaifa/2016/0123/3909.html)

#### website 	

- _[https://yalantis.com/blog/](https://yalantis.com/blog/) --- (Build By [Yalantis](https://github.com/Yalantis)) : Yalantis's Blog [Yalantis技术博客]._

	<img src="http://i.imgur.com/BnCTxv1.png" width="90%">


	![](https://img.shields.io/badge/The%20Day25-End%20!-ED1C24.svg?style=flat)













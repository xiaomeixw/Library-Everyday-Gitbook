----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 

## Day19
> ![](https://img.shields.io/badge/AndroidEveryday-Day19-green.svg?style=flat)   
> ***Time : December 22th,2015*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[AndroidImageSlider](https://github.com/daimajia/AndroidImageSlider) --- (From [daimajia](https://github.com/daimajia)) : 
An amazing and convenient Android image slider. [图片左右滑动]._

    <img src="https://camo.githubusercontent.com/f64413139bbaa918131384d3597c33e39333aa7f/687474703a2f2f7777332e73696e61696d672e636e2f6d773639302f36313064633033346a773165677a6f7236366f6a64673230393530666b6e70652e676966" width="32%">

- _[DropListView](https://github.com/ufo22940268/DropListView) --- (From [ufo22940268](https://github.com/ufo22940268)) : 
Another PullToRefreshList with drop effect. [PullToRefreshList]._

    <img src="https://github.com/ufo22940268/DropListView/raw/master/slide2.gif" width="32%">

- _[android-layout-samples](https://github.com/lucasr/android-layout-samples) --- (From [lucasr](https://github.com/lucasr)) : 
Explorations around Android custom layouts.so perfect Article,the author join Facebook now. [自定义View方案，很棒的文章,原Firefox工程师,作者现在加入了Facebook]._

	<img src="http://i.imgur.com/wNjfCDO.png" width="90%">

	Explorations around Android custom layouts, including off main thread View measure/layout passes.
	
	Sample code for:
	* Composite View
	* Custom Composite View
	* Flat Custom View
	* Async Custom View
	
	For more information, read: [http://lucasr.org/?p=3920](http://lucasr.org/?p=3920)


2.Logic：

- _[common_adapter_viewholder](https://github.com/bboyfeiyu/common_adapter_viewholder) --- (From [bboyfeiyu](https://github.com/bboyfeiyu) & Tag  is [Adapter](https://github.com/bboyfeiyu/common_adapter_viewholder)) : 
simplify adapter code like JoanZapata 's [base-adapter-helper](https://github.com/JoanZapata/base-adapter-helper) [简化adapter书写]._

	<img src="http://i.imgur.com/XooDCZA.png" width="90%">

- _[base-adapter-helper](https://github.com/JoanZapata/base-adapter-helper) --- (From [JoanZapata](https://github.com/JoanZapata) & Tag  is [Adapter](https://github.com/JoanZapata/base-adapter-helper)) : 
Abstraction for the usual BaseAdapter "ViewHolder" pattern.[简化adapter书写]._

	<img src="https://camo.githubusercontent.com/94372fad90c2de4c6612d0e396440ebf15298abc/68747470733a2f2f7261772e6769746875622e636f6d2f4a6f616e5a61706174612f626173652d616461707465722d68656c7065722f6d61737465722f6865616465722e706e67" width="90%">

- _[AndroidUtils](https://github.com/zhengxiaopeng/AndroidUtils) --- (From [zhengxiaopeng](https://github.com/zhengxiaopeng) & Tag  is [Utils](https://github.com/zhengxiaopeng/AndroidUtils)) : 
some useful code for android.[一些android代码片段]._

	<img src="http://i.imgur.com/sKmKpfD.png" width="90%">

- _[simple_net_framework](https://github.com/bboyfeiyu/simple_net_framework) --- (From [bboyfeiyu](https://github.com/bboyfeiyu) & Tag  is [AsyncTask](https://github.com/bboyfeiyu/simple_net_framework)) : 
write some code like volley just study do not use in your Commercial projects.[仿volley框架,不推荐实际生产,只供学习]._

	<img src="https://camo.githubusercontent.com/525b1b56a9cd67dfce3dfc39a00883f729106704/687474703a2f2f6176617461722e6373646e2e6e65742f626c6f677069632f32303135303131353136313933363837352e6a7067" width="32%">

	    // 1
	    RequestQueue queue = SimpleNet.newRequestQueue();  
	
	    // 2
	    MultipartRequest multipartRequest = new MultipartRequest("你的url", new   RequestListener<String>() {
	                    @Override
	                    public void onComplete(int stCode, String response, String errMsg) {
	                        // UI THREAD
	                    }
	                }); 
	
	    // 3
	    // header  
	    multipartRequest.addHeader("header-name", "value");  
	
	    // MultipartEntity 
	    MultipartEntity multi = multipartRequest.getMultiPartEntity();  

	    multi.addStringPart("location", "模拟的地理位置");  
	    multi.addStringPart("type", "0");  
	
	    Bitmap bitmap = BitmapFactory.decodeResource(getResources(), R.drawable.thumb);  

	    multi.addBinaryPart("images", bitmapToBytes(bitmap));  

	    multi.addFilePart("imgfile", new File("storage/emulated/0/test.jpg"));  
	
	
	    // 4
	    queue.addRequest(multipartRequest); 

3.Architecture:

- _[AndroidViewModel](https://github.com/inloop/AndroidViewModel) --- (From [inloop](https://github.com/inloop)) : 
Separating data and state handling from Fragments or Activities without lots of boilerplate-code. [探索一种VM架构,分离view和model层]._

	<img src="https://github.com/inloop/AndroidViewModel/raw/master/website/static/viewmodel_architecture.png" width="90%">
	
#### App-Demo ####

- _[AppCodeArchitecture](https://github.com/Frank-Zhu/AppCodeArchitecture) --- (From [Frank-Zhu](https://github.com/Frank-Zhu) A Developer from China) : 
App Code Architecture,Use some famous libraries. [安卓APP代码架构,常用的开源库构建]._

	Check the Source in [Github](https://github.com/Frank-Zhu/AppCodeArchitecture).Want to know more about the App-Demo see [Frank-Zhu's Blog](http://frank-zhu.github.io/2014-11-22-android-app-code-architecture.html)

	#### the app-demo with these open source projects

	- _[Retrofit](https://github.com/square/retrofit)_
	- _[OKHTTP](https://github.com/square/okhttp)_
	- _[Picasso](https://github.com/square/picasso)_
	- _[UIL](https://github.com/nostra13/Android-Universal-Image-Loader)_
	- _[Butterknife](https://github.com/JakeWharton/butterknife)_
	- _[GSON](https://code.google.com/p/google-gson/)_
	- _[EventBus](https://github.com/greenrobot/EventBus)_
	- _[otto](https://github.com/square/otto)_
	- _[AppMsg](https://github.com/johnkil/Android-AppMsg)_
	- _[CircleImageView](https://github.com/hdodenhof/CircleImageView)_



#### resource ####

- _[android_design_patterns_analysis](https://github.com/simple-android-framework-exchange/android_design_patterns_analysis) --- (From [simple-android-framework-exchange](https://github.com/simple-android-framework-exchange) A Developer from China) : 
Android design patterns analysis resource. [android设计模式]._

	<img src="http://i.imgur.com/jW9PdqU.png" width="90%">

- _[android-open-project-demo](https://github.com/android-cn/android-open-project-demo) --- (From [android-cn](https://github.com/android-cn) A Developer from China) : 
Demo of android open source project. [著名框架的使用范例]._

	<img src="http://i.imgur.com/aXLwepR.png" width="90%">

#### article ####

- _[Custom Layouts on Android](http://lucasr.org/2014/05/12/custom-layouts-on-android/) --- (From Author  [Lucas Rocha](https://github.com/lucasr) blog [http://lucasr.org/](http://lucasr.org/)) --- [Source in [Github](https://github.com/lucasr/android-layout-samples)]_ 

	<p>
	<img src="http://i.imgur.com/nScECov.jpg" width="150px" height="150px" align="left" hspace="15px" />
	If you ever built an Android app, you have definitely used some of the built-in layouts available in the platform—RelativeLayout, LinearLayout, FrameLayout, etc. They are our bread and butter for building Android UIs.

	The built-in layouts combined provide a powerful toolbox for implementing complex UIs. But there will still be cases where the design of your app will require you to implement custom layouts.

	There are two main reasons to go custom. First, to make your UI more efficient—by reducing the number of views and/or making faster layout traversals. Second, when you are building UIs that are not naturally possible to implement with stock widgets.

	In this post, I will demonstrate four different ways of implementing custom layouts and discuss their respective pros and cons: composite view, custom composite view, flat custom view, and async custom views.

	The code samples are available in my android-layout-samples repo. This app implements the same UI with each technique discussed here and uses Picasso for image loading. The UI is a simplified version of Twitter app’s stream—no interactions, just the layouts.

	Ok, let’s start with the most common type of custom layout: composite view.
	</p>

	[Translation：听FackBook工程师讲Custom ViewGroups]. 
 
	Chinese Translation Address : [Thanks To android-tech-frontier](http://www.devtf.cn/?p=515)

	<img src="http://i.imgur.com/z2YHAC8.png" width="90%">
	

#### website 	

- _[http://codekk.com/](http://codekk.com/open-source-project-analysis) --- (Build By [Trinea](https://github.com/Trinea)) :A super famous website about Android project Analysis in China[Android blog]._

	<img src="http://i.imgur.com/6ubIDAS.png" width="90%">

	![](https://img.shields.io/badge/The%20Day19-End%20!-ED1C24.svg?style=flat)













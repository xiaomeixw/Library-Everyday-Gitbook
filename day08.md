----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 

## Day8
> ![](https://img.shields.io/badge/AndroidEveryday-Day1-green.svg?style=flat)   
> ***Time : October 29th,2015*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[FoldableLayout](https://github.com/worldline/FoldableLayout) --- (From [worldline](https://github.com/worldline)) : 
An Android demo of a foldable layout implementation,The author say: This code is a demo and not a library. [一个折叠效果]._

	<img src="https://raw.githubusercontent.com/worldline/FoldableLayout/dev/screenshots/demo.gif" width="40%">

- _[FoldableLayout](https://github.com/alexvasilkov/FoldableLayout) --- (From [alexvasilkov](https://github.com/alexvasilkov)) : 
Android widgets to implement folding animation,It was wonderful library. [一个折叠效果,效果很棒]._

	<img src="http://i.imgur.com/CiSnMIa.jpg" width="100%">

- _[Android-FoldingLayout](https://github.com/elementsinteractive/Android-FoldingLayout) --- (From [elementsinteractive](https://github.com/elementsinteractive)) : 
A layout to switch over its children using a page folding animation,LIKE Flipboard application.  [一个折叠效果,类似Flipboard的翻页效果]._

	<img src="http://i.imgur.com/EckUyKB.png" width="40%">

- _[android-FlipView](https://github.com/emilsjolander/android-FlipView) --- (From [emilsjolander](https://github.com/emilsjolander)) : 
A small, easy to use android library for implementing flipping between views as seen in the popular Flipboard application,very smoothly. [一个折叠效果,类似Flipboard的翻页效果,很流畅,API比较丰富]._

	<img src="http://i.imgur.com/tpHRbSe.png" width="40%">

- _[FlipViewPager.Draco](https://github.com/Yalantis/FlipViewPager.Draco) --- (From [Yalantis](https://github.com/Yalantis)) : 
This project aims to provide a working page flip implementation for usage in ListView. [ListView联系人翻页效果]._

	<img src="https://camo.githubusercontent.com/db312e031e5f5a445b548d35986b0498caa261d3/68747470733a2f2f6431337961637572716a676172612e636c6f756466726f6e742e6e65742f75736572732f3132353035362f73637265656e73686f74732f313735383239382f39396d696c65732d66696e642d667269656e64732d696e746572666163652d616e696d6174696f6e2e676966" width="40%">

- _[android-flip](https://github.com/openaphid/android-flip) --- (From [openaphid](https://github.com/openaphid)) : 
A component for flip animation on Android, which is similar to the effect in Flipboard iPhone/Android. [一个类似Flipboard翻页效果]._

	<img src="http://openaphid.github.io/images/flipview-horizontal-demo.gif" width="40%">


2.Logic：

- _[Favor](https://github.com/soarcn/Favor) --- (From [soarcn](https://github.com/soarcn) & Tag  is [Caching](https://github.com/soarcn/Favor)) : 
A easy way to use android sharepreference. [使用注解简单操作sharepreference]._

	<img src="http://i.imgur.com/rgCiW3M.png" width="100%">

		//1 Define a interface.
		@AllFavor
		public interface Account {
		    @Default("No Name")
		    String getUserName();
		    String setPassword(String password);
		}

		//2 The FavorAdatper class generates an implementation of the interface.
		account = new FavorAdapter.Builder(getContext()).build().create(Account.class);
		account.setPassword("Passw0rd");
		String username = account.getUserName();

- _[AndroidChannel](https://github.com/skyfe79/AndroidChannel) --- (From [skyfe79](https://github.com/skyfe79) & Tag  is [AsyncTask](https://github.com/skyfe79/AndroidChannel)) : 
AndroidChannel is helper library for thread communication between mainthread and workerthread. [异步调度,主线程和工作线程通信]._

	<img src="http://i.imgur.com/jHTGpJj.png" width="100%">

		channel = new AndroidChannel(new AndroidChannel.UiCallback() {
		    @Override
		    public boolean handleUiMessage(Message msg) {
		
		        if(msg.what == PING) {
		            Log.d("TAG", "PING");
		            channel.toWorker().sendEmptyMessageDelayed(PONG, 1000);
		        }
		        return false;
		    }
		}, new AndroidChannel.WorkerCallback() {
		    @Override
		    public boolean handleWorkerMessage(Message msg) {
		
		        if(msg.what == PONG) {
		            Log.d("TAG", "PONG");
		            channel.toUI().sendEmptyMessageDelayed(PING, 1000);
		        }
		        return false;
		    }
		});
		channel.toUI().sendEmptyMessage(PING);

3.Architecture:

- _[Backeasy](https://github.com/Pierry/Backeasy) --- (From [Pierry](https://github.com/Pierry)) : 
Android - DI, DDD, Specification Pattern, Repository Pattern, IoC. [探索JAVA成熟模式在Android上的分层架构]._

	![](https://raw.githubusercontent.com/Pierry/Backeasy/master/art/patterns-diagram.png)

	- Domain driven-design start
	- Domain entities
	- Contracts (Interfaces)
	- Repository Pattern
	- Specification Pattern
	- ActiveAndroid (Database)
	- Dependency Injection - IoC (RoboGuice)
	- View Injection & Threads (Android Annotations)
	- SOLID

- _[droidparts](https://github.com/yanchenko/droidparts) --- (From [yanchenko](https://github.com/yanchenko)) : 
a carefully crafted Android framework:DI, ORM, JSON.... [封装一套可复用的Android框架]._

	![](http://droidparts.org/_images/droidparts_logo.png)

	a carefully crafted Android framework that includes:
	* *DI* - injection of Views, Fragments, Services, etc.
	* *ORM* - efficient persistence utilizing Cursors & fluent API.
	* *EventBus* for posting event notifications.
	* Simple *JSON* (de)serialization capable of handling nested objects.
	* Improved *AsyncTask* & *IntentService* with Exceptions & result reporting support.
	* *Logger* that figures out tag itself & logs any object.
	* *RESTClient* for GETting, PUTting, POSTing, DELETing & InputStream-getting,
	  also speaks JSON.
	* *ImageFetcher* to asynchronously attach images to ImageViews, with caching,
	  cross-fade & transformation support.
	* Numerous *Utils*.


#### article ####

- _[ANNOTATION PROCESSING 101](http://hannesdorfmann.com/annotation-processing/annotationprocessing101/) --- (From Author  [sockeqwe](https://github.com/sockeqwe) blog [http://hannesdorfmann.com](http://hannesdorfmann.com/)) --- [Source in [Github](https://github.com/sockeqwe/annotationprocessing101)]_ 

	 (Editor's note : A wonderful article to learn ANNOTATION PROCESSING in android. A lot of famous library is based on it like ParcelableGenerator、butterknife and androidannotaion).

	 In this blog entry I would like to explain how to write an annotation processor. So here is my tutorial. First, I am going to explain to you what annotation processing is, what you can do with that powerful tool and finally what you cannot do with it. In a second step we will implement a simple annotation processor step by step.

	 To clarify a very important thing from the very beginning: we are not talking about evaluating annotations by using reflections at runtime (run time = the time when the application runs). Annotation processing takes place at compile time (compile time = the time when the java compiler compiles your java source code).[Translation：Java注解处理器使用详解]. 
 
	Chinese Translation Address : [Thanks To codeceo](http://www.codeceo.com/article/java-annotation-processor.html)
	
	![](http://i.imgur.com/717nTmj.png)

	![](http://i.imgur.com/lIoqtH2.png)

	![](http://i.imgur.com/luA5H2Q.png)
	

	DroidconDE 2015: Hannes Dorfmann – Annotation Processing 101. Want to see the video , See [Youtube](https://www.youtube.com/watch?v=43FFfTyDYEg). Want to see the Author's PDF in [DroidconDE 2015](http://droidcon.de/sites/droidcon.de/files/media/documents/Hannes%20Dorfmann-Annotation%20Processing%20101.pdf).

#### website 	

- _[http://droidcon.de/](http://gank.io/) --- (started in 2008 in Berlin) : Droidcon is the franchise name for a series of commercial conferences in Europe, focused on software development for Google's Android smartphone framework. The Droidcon conferences are the largest Android developer conferences held outside the USA. [Android技术交流公开活动组织]._

	![](http://i.imgur.com/KwZofxt.png)

	![](https://img.shields.io/badge/The%20Day8-End%20!-ED1C24.svg?style=flat)















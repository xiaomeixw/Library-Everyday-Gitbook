----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 

## Day6
> ![](https://img.shields.io/badge/AndroidEveryday-Day6-green.svg?style=flat)   
> ***Time : October 27th,2015*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[AVLoadingIndicatorView](https://github.com/81813780/AVLoadingIndicatorView) --- (From [81813780](https://github.com/81813780)) : 
Nice loading animations for Android. [多个酷炫的loading动画]._

	<img src="https://github.com/81813780/AVLoadingIndicatorView/raw/master/Demo.gif" width="45%">   

- _[android-slidingactivity](https://github.com/klinker41/android-slidingactivity) --- (From [klinker41](https://github.com/klinker41)) : 
Android library which allows you to swipe down from an activity to close it. [下拉关闭Activity]._

    ![](https://github.com/klinker41/android-slidingactivity/raw/master/preview.gif)

- _[pull-back-layout](https://github.com/oxoooo/pull-back-layout) --- (From [oxoooo](https://github.com/oxoooo)) : 
Pull down to finish an Activity. [下拉关闭Activity]._

    ![](https://github.com/oxoooo/pull-back-layout/raw/master/screenshot.gif)

- _[SwipableLayout](https://github.com/SerhatSurguvec/SwipableLayout) --- (From [SerhatSurguvec](https://github.com/SerhatSurguvec)) : 
Swipe up or down to close view or activity or anything. [下拉或上拉关闭界面]._

    ![](https://github.com/SerhatSurguvec/SwipableLayout/raw/master/screenshot.gif)

- _[SwipeBack](https://github.com/sockeqwe/SwipeBack) --- (From [sockeqwe](https://github.com/sockeqwe)) : 
SwipeBack for Android Activities to do pretty the same as the android "back-button" will do, but in a really intuitive way by using a swipe gesture. [下拉或上拉关闭界面]._

    ![](https://camo.githubusercontent.com/a8ca00fe3f9e4aa65d902ad873c3f7ef77a2b418/687474703a2f2f696d672e796f75747562652e636f6d2f76692f54366d62675f77716c6b632f302e6a7067)

- _[SwipeBack](https://github.com/liuguangqiang/SwipeBack) --- (From [liuguangqiang](https://github.com/liuguangqiang)) : 
SwipeBack is an android library that can finish a activity by using gesture. [右滑关闭Activity]._

	<img src="https://github.com/liuguangqiang/SwipeBack/raw/master/Images/swipeback_demo.gif" width="50%">

- _[SwipeBackLayout](https://github.com/ikew0ng/SwipeBackLayout) --- (From [ikew0ng](https://github.com/ikew0ng)) : 
An Android library that help you to build app with swipe back gesture. [滑动关闭Activity]._

	<img src="https://github.com/Issacw0ng/SwipeBackLayout/raw/master/art/screenshot.png?raw=true" width="50%">


- _[ParallaxSwipeBack](https://github.com/bushijie/ParallaxSwipeBack) --- (From [bushijie](https://github.com/bushijie)) : 
Swipe back to finish the activity with Parallax effect. [带视差滑动布局]._

	<img src="http://i.imgur.com/PcsMQWR.png" width="50%"> 


- _[SwipeBackHelper](https://github.com/Jude95/SwipeBackHelper) --- (From [Jude95](https://github.com/Jude95)) : 
Swipe back to finish the activity with Parallax effect. [带视差滑动布局]._

	<img src="https://github.com/Jude95/SwipeBackHelper/raw/master/swipeback.gif" width="50%">


2.Logic：

- _[android-job](https://github.com/evernote/android-job) --- (From [evernote](https://github.com/evernote) & Tag  is [AsyncTask](https://github.com/evernote/android-job)) : 
Android library to handle jobs in the background,Evernote 's Library would never disappointed you. [后台执行Job的线程调度,Evernote出品,必属精品]._

	<img src="http://i.imgur.com/8DiprEJ.png" width="90%"> 

		public class MyActivity extends Activity {
		
		    @Override
		    protected void onCreate(Bundle savedInstanceState) {
		        super.onCreate(savedInstanceState);
		
		        Task myTask = new MyTask();
		        int taskId = TaskExecutor.getInstance().execute(myTask, this);
		    }
		
		    @TaskResult
		    public void onResult(Integer result) {
		        // handle result, this method gets called on the UI thread and only if the activity is visible
		    }
		}
		
		public class MyTask extends Task<Integer> {
		
		    @Override
		    protected Integer execute() {
		        return 5;
		    }
		}

3.Architecture:

- _[libraryofalexandria](https://github.com/rallat/libraryofalexandria) --- (From [rallat](https://github.com/rallat)) : 
sample android project to show how to refactor legacy code. [Twitter工程师Trallat的MVP进化之旅]._

	<img src="http://i.imgur.com/tNfivZ8.png" width="90%">
	<img src="http://i.imgur.com/KxlWvIk.png" width="90%">


#### article ####

- _[Android Basic Project Architecture for MVP](https://medium.com/mobiwise-blog/android-basic-project-architecture-for-mvp-72f4b33252d0#.rh1shuz45) --- (From Author  [MuratCanBur](https://github.com/muratcanbur) blog [http://muratcanbur.com/](http://muratcanbur.com/)) --- [No Source]_ 

	Nowadays, I read lots of articles about how to create a basic project structure for our Android applications. As far as I understand from them, the main approach is implementing MVP (Model View Presenter) pattern which is also important in the development of Android community.

	After I learned some useful things from other developers, blog posts and example projects, I decided to create a basic project structure approach so that I can implement it to our client applications for mobiwise. I have choosen MVP pattern for main app structure. Let’s start with it and try to understand. [Translation：探索android MVP架构]. 
 
	Chinese Translation Address : waitting for someone to translate it.
	

	![](http://i.imgur.com/IAcPagy.png)


- _[Custom view- Part 1 & Part 2](https://medium.com/@shemag8/custom-view-part-1-9a9c4ae80845#.ujyzbi2gd) --- (From Author  [shem8](https://github.com/shem8) blog [https://shem8.wordpress.com](https://shem8.wordpress.com/)) --- [Source in [Github](https://github.com/shem8/customviewpager)]_ 

	Until couple of months ago I’ve been a bit afraid writing custom views. I thought it’s too complicated and had a lot of overhead with handling all layouting and interactions, I felt there is not enough documentation out there, not mention the edge cases and performance. I had my default Android view component in my toolbox and thought that everything I needed can be composed from those.

	The last part is true for most cases. Most of Android apps can be built only with the basic layouts and views out there, so why do we still need to build custom views sometimes?

	Chinese Translation Address : waitting for someone to translate it.

	<img src="http://i.imgur.com/BEsT4ib.gif" width="57%">


#### website 	

- _[https://dribbble.com](https://dribbble.com) --- (Build By [Dan Cederholm and Rich Thornett ,2009](https://en.wikipedia.org/wiki/Dribbble)) :Dribbble is an online community for showcasing user-made artwork. It functions as a self-promotion and networking platform for graphic design, web design, illustration, photography, and other creative areas. [设计喵群体聚集地]._

	<img src="http://i.imgur.com/kgUVneZ.png" width="80%">

	![](https://img.shields.io/badge/The%20Day6-End%20!-ED1C24.svg?style=flat)


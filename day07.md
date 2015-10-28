----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 

## Day7
> ![](https://img.shields.io/badge/AndroidEveryday-Day7-green.svg?style=flat)   
> ***Time : October 28th,2015*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[FAImageView](https://github.com/skyfe79/FAImageView) --- (From [skyfe79](https://github.com/skyfe79)) : 
FAImageView is a Frame Animation ImageView for Android. [自定义帧动画View]._

    ![](https://github.com/skyfe79/FAImageView/raw/master/FAImageView.gif)

- _[CircleImageView](https://github.com/hdodenhof/CircleImageView) --- (From [hdodenhof](https://github.com/hdodenhof)) : 
A circular ImageView for Android. [圆形图片]._

	<img src="https://camo.githubusercontent.com/e17a2a83e3e205a822d27172cb3736d4f441344d/68747470733a2f2f7261772e6769746875622e636f6d2f68646f64656e686f662f436972636c65496d616765566965772f6d61737465722f73637265656e73686f742e706e67" width="35%"> 



- _[RoundedImageView](https://github.com/vinc3m1/RoundedImageView) --- (From [vinc3m1](https://github.com/vinc3m1)) : 
A fast ImageView that supports rounded corners, ovals, and circles. [各种自定义形状图片]._


	<img src="https://camo.githubusercontent.com/ed1e075be6ed97fa9091d3702e9b96d3e85b7a35/68747470733a2f2f7261772e6769746875622e636f6d2f6d616b6572616d656e2f526f756e646564496d616765566965772f6d61737465722f73637265656e73686f742e706e67" width="35%"><img src="https://camo.githubusercontent.com/d4970a90842c50a708f94b7bd996657c41ab62fb/68747470733a2f2f7261772e6769746875622e636f6d2f6d616b6572616d656e2f526f756e646564496d616765566965772f6d61737465722f73637265656e73686f742d6f76616c2e706e67" width="35%">

- _[android-crop](https://github.com/jdamcd/android-crop) --- (From [jdamcd](https://github.com/jdamcd)) : 
Android library project for cropping images. [裁剪图片]._

	<img src="https://github.com/jdamcd/android-crop/raw/master/screenshot.png" width="35%"> 

- _[cropper](https://github.com/edmodo/cropper) --- (From [edmodo](https://github.com/edmodo)) : 
Android widget for cropping and rotating an image. [裁剪图片]._

	<img src="https://camo.githubusercontent.com/e4fde77bf41d4a60b234b4e268e5cfa8c17d9b6f/687474703a2f2f692e696d6775722e636f6d2f334668735467666c2e6a7067" width="35%"> 

- _[SimpleCropView](https://github.com/IsseiAoki/SimpleCropView) --- (From [IsseiAoki](https://github.com/IsseiAoki)) : 
A simple image cropping library for Android. [裁剪图片]._

	<img src="https://camo.githubusercontent.com/7ef872746a0181356ea0b44d94b7bd939f28c5ae/68747470733a2f2f7261772e6769746875622e636f6d2f77696b692f4973736569416f6b692f53696d706c6543726f70566965772f696d616765732f6769662f64656d6f5f62617369635f75736167652e676966" width="35%"> 

- _[CropImageView](https://github.com/cesards/CropImageView) --- (From [cesards](https://github.com/cesards)) : 
Widget allows you crop from whatever side in an ImageView. Currently Android only supports centerCrop type of cropping. [各种不同的角度中间centerCrop截取图片]._

	<img src="https://github.com/cesards/CropImageView/raw/master/art/cropping.png" width="35%"> 

- _[Masaccio](https://github.com/Subito-it/Masaccio) --- (From [Subito-it](https://github.com/Subito-it)) : 
An Android library providing a useful widget class which automatically detects the presence of faces in the source image and crop it accordingly so to achieve the best visual result. [自动识别图片中人脸并截取出来]._

	<img src="https://github.com/Subito-it/Masaccio/raw/master/masaccio_demo.gif" width="35%"> 


2.Logic：

- _[android-priority-jobqueue](https://github.com/path/android-priority-jobqueue) --- (From [path](https://github.com/path) & Tag  is [AsyncTask](https://github.com/path/android-priority-jobqueue)) : 
A Job Queue specifically written for Android to easily schedule jobs (tasks) that run in the background, improving UX and application stability. [后台异步线程调度,Path出品,必属精品]._

	![](https://camo.githubusercontent.com/89e4b9be8eecdd350c42a2b666dcbd4f764bb58c/687474703a2f2f646f776e6c6f6164732e706174682e636f6d2f6c6f676f2e706e67)

		// A job to send a tweet
		public class PostTweetJob extends Job {
		    public static final int PRIORITY = 1;
		    private String text;
		    public PostTweetJob(String text) {
		        // This job requires network connectivity,
		        // and should be persisted in case the application exits before job is completed.
		        super(new Params(PRIORITY).requireNetwork().persist());
		    }
		    @Override
		    public void onAdded() {
		        // Job has been saved to disk.
		        // This is a good place to dispatch a UI event to indicate the job will eventually run.
		        // In this example, it would be good to update the UI with the newly posted tweet.
		    }
		    @Override
		    public void onRun() throws Throwable {
		        // Job logic goes here. In this example, the network call to post to Twitter is done here.
		        webservice.postTweet(text);
		    }
		    @Override
		    protected boolean shouldReRunOnThrowable(Throwable throwable) {
		        // An error occurred in onRun.
		        // Return value determines whether this job should retry running (true) or abort (false).
		    }
		    @Override
		    protected void onCancel() {
		        // Job has exceeded retry attempts or shouldReRunOnThrowable() has returned false.
		    }
		}


3.Architecture:

- _[mv2m](https://github.com/fabioCollini/mv2m) --- (From [fabioCollini](https://github.com/fabioCollini)) : 
Android MVVM lightweight library based on Android Data Binding. [基于google的Android Data Binding基础的MVVM架构探索]._

	Model:	

	A Model class contains the data used to populate the user interface using Data Binding library. It's saved automatically in Actvity/Fragment state, for this reason it must implement Parcelable interface.
	
	View:
	
	The View is an Activity or a Fragment, the user interface is managed using Android Data Binding. You need to extend ViewModelActivity or ViewModelFragment class and implement createViewModel method returning a new ViewModel object.
	
	ViewModel:	

	The ViewModel is a subclass of ViewModel class, it is automatically saved in a retained fragment to avoid the creation of a new object on every configuration change. The ViewModel is usually the object bound to the layout using the Data Binding framework. It manages the background tasks and all the business logic of the application.

	<img src="https://github.com/fabioCollini/mv2m/raw/master/demo-mv2m.png" width="65%"> 
	<img src="https://github.com/fabioCollini/mv2m/raw/master/mv2m-class-diagram.png" width="65%"> 


#### App-Demo ####

- _[GEM](https://github.com/Substance-Project/GEM) --- (From [Substance-Project](https://github.com/Substance-Project) A Organization from United States) : 
A music player for Android, in stunning Material Design. [带Material Design设计风格的音乐App-Demo]._

	<img src="https://camo.githubusercontent.com/53118bf8ba812c1776c998ba272d4eff47bf0143/687474703a2f2f7375627374616e636570726f6a6563742e6e65742f696d616765732f67656d2f67656d5f616c62756d5f766965775f736d616c6c2e706e67" width="35%">

	Check the Source in [Github](https://github.com/Substance-Project/GEM).Want to know more about the App-Demo see [http://substanceproject.net](http://substanceproject.net/)


- _[StickerCamera](https://github.com/Skykai521/StickerCamera) --- (From [Skykai521](https://github.com/Skykai521) A Developer from China) : 
This is an Android application with camera,picture cropping,collage sticking and tagging. [图片裁剪图片标签App-Demo]._

	<img src="https://github.com/Skykai521/StickerCamera/raw/master/screenshot/Screenshot_01.gif" width="35%"><img src="https://github.com/Skykai521/StickerCamera/raw/master/screenshot/Screenshot_2015-07-19-11-23-22.png" width="35%"> 

	<img src="https://github.com/Skykai521/StickerCamera/raw/master/screenshot/Screenshot_2015-07-19-11-21-39.png" width="35%"><img src="https://github.com/Skykai521/StickerCamera/raw/master/screenshot/Screenshot_2015-07-19-11-23-04.png" width="35%">

	Check the Source in [Github](https://github.com/Skykai521/StickerCamera).


#### article ####

- _[JOE'S GREAT ADAPTER HELL ESCAPE](http://hannesdorfmann.com/android/adapter-delegates/) --- (From Author  [sockeqwe](https://github.com/sockeqwe) blog [http://hannesdorfmann.com](http://hannesdorfmann.com/)) --- [Source in [Github](https://github.com/sockeqwe/AdapterDelegates)]_ 

	 Favor composition over inheritance!

	 Let me tell you a story about Joe Somebody an android developer at MyLittleZoo Inc. and how he walked through the hell while trying to create reusable RecyclerView Adapters with different view types and how he finally managed to implement reusable Adapters painlessly. [Translation：组合优于继承,逃离Adapter-Type的地狱]. 
 
	<div style="text-align: center;"><img src="https://camo.githubusercontent.com/d0758c90c7363cf8fbfac03df8b1d0b7a41614dc/687474703a2f2f692e696d6775722e636f6d2f50325a675759342e706e67" width="25%"></div>

		public class AdapterDelegatesManager<T> {
    
		    SparseArrayCompat<AdapterDelegate<T>> delegates = new SparseArrayCompat();
		    
		    public AdapterDelegatesManager<T> addDelegate(@NonNull AdapterDelegate<T> delegate) {
		        return addDelegate(delegate, false);
		    }
		
		
		    public AdapterDelegatesManager<T> addDelegate(@NonNull AdapterDelegate<T> delegate,boolean allowReplacingDelegate) {
		        return this;
		    }
		
		
		    public AdapterDelegatesManager<T> removeDelegate(@NonNull AdapterDelegate<T> delegate) {
		        return this;
		    }
		
		
		    public AdapterDelegatesManager<T> removeDelegate(int viewType) {
		        delegates.remove(viewType);
		        return this;
		    }
		
		
		    public int getItemViewType(@NonNull T items, int position) {
		        for (int i = 0; i < delegatesCount; i++) {
		            AdapterDelegate<T> delegate = delegates.valueAt(i);
		            if (delegate.isForViewType(items, position)) {
		                return delegate.getItemViewType();
		            }
		        }
		        
		    }
		
		
		    @NonNull public RecyclerView.ViewHolder onCreateViewHolder(ViewGroup parent, int viewType) {
		        AdapterDelegate<T> delegate = delegates.get(viewType);
		        RecyclerView.ViewHolder vh = delegate.onCreateViewHolder(parent);
		        return vh;
		    }
		
		
		    public void onBindViewHolder(@NonNull T items, int position, @NonNull RecyclerView.ViewHolder viewHolder) {
		        AdapterDelegate<T> delegate = delegates.get(viewHolder.getItemViewType());
		        delegate.onBindViewHolder(items, position, viewHolder);
		    }
		}

	
	

#### website 	

- _[jsonschema2pojo](http://www.jsonschema2pojo.org/) --- (Build By [joelittlejohn](https://github.com/joelittlejohn/jsonschema2pojo)) :Generates Java types from JSON Schema (or example JSON) and annotates those types for data-binding with Jackson 1.x or 2.x, Gson, etc. [自动将json转成pojo对象,简化JavaBean对象书写]._

	![](http://i.imgur.com/02FbM44.png)

	![](https://img.shields.io/badge/The%20Day7-End%20!-ED1C24.svg?style=flat)


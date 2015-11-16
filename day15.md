----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 

## Day15
> ![](https://img.shields.io/badge/AndroidEveryday-Day15-green.svg?style=flat)   
> ***Time : November 14th,2015*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[TSnackBar](https://github.com/AndreiD/TSnackBar) --- (From [AndreiD](https://github.com/AndreiD)) : 
Android Snackbar from the Top (similar to Crouton). [从顶部而下的Snackbar]._

    <img src="https://raw.githubusercontent.com/AndreiD/TSnackBar/master/app/snackbar.gif" width="35%"> 

- _[CharacterPickerView](https://github.com/alafighting/CharacterPickerView) --- (From [alafighting](https://github.com/alafighting)) : 
An Android wheel view like ios system. [仿ios滚轮view]._

    <img src="https://github.com/alafighting/CharacterPickerView/raw/master/Screenshot/Screenshot_2015-11-13-154813.gif" width="50%"> 

- _[WheelView](https://github.com/LukeDeighton/WheelView) --- (From [LukeDeighton](https://github.com/LukeDeighton)) : 
An Android Widget for selecting items that rotate on a wheel. [滚轮盘]._

    <img src="https://github.com/LukeDeighton/WheelView/raw/master/Graphics/center_wheel.gif" width="50%"> 

- _[WheelView](https://github.com/wangjiegulu/WheelView) --- (From [wangjiegulu](https://github.com/wangjiegulu)) : 
An Android wheel view. [滚动view]._

    <img src="https://raw.githubusercontent.com/wangjiegulu/WheelView/master/image/image03.png" width="35%"> 

- _[WheelView-Android](https://github.com/lantouzi/WheelView-Android) --- (From [lantouzi](https://github.com/lantouzi)) : 
An Android wheel view. [滚动选择view]._

    <img src="https://raw.githubusercontent.com/lantouzi/WheelView-Android/master/preview/demo.jpg" width="35%"> 

- _[droidicon](https://github.com/theDazzler/droidicon) --- (From [theDazzler](https://github.com/theDazzler/)) : 
Over 1600 customizable icons for Android including 750+ Google Material Design icons, 25 ready-made social badges, and more!. [Material Design icons图标]._

    <img src="https://github.com/theDazzler/droidicon/raw/master/screenshots/screen4_framed.jpg" width="30%"><img src="https://github.com/theDazzler/droidicon/raw/master/screenshots/screen7_framed.jpg" width="30%"><img src="https://github.com/theDazzler/droidicon/raw/master/screenshots/screen2_framed.jpg" width="30%"> 

2.Logic：

- _[Renderers](https://github.com/pedrovgs/Renderers) --- (From [pedrovgs](https://github.com/pedrovgs) & Tag  is [Adapter](https://github.com/pedrovgs/Renderers)) : 
Renderers is an Android library created to avoid all the boilerplate needed to use a RecyclerView/ListView with adapters. [封装的一套ListView和RecyclerView]._

	<img src="https://camo.githubusercontent.com/01e7f01a6d6f31d936966d4572187a4e7a1083a0/687474703a2f2f7261772e6769746875622e636f6d2f706564726f7667732f52656e6465726572732f6d61737465722f6172742f53637265656e73686f745f64656d6f5f312e706e67" width="35%"> 

		//1.Create your Renderer or Renderers extending Renderer<T>
		public abstract class VideoRenderer extends Renderer<Video> {
			......
		}	

		//2.Create a RendererBuilder with a Renderer prototypes collection and declare the mapping between the content to render and the Renderer used.
		public class VideoRendererBuilder extends RendererBuilder<Video> {
			......
		}

		//3.Initialize your ListView/RecyclerView with your RendererBuilder and your AdapteeCollection inside Activities and Fragments.
		private void initListView() {
    		listView.setAdapter(adapter);
		}

		private void initListView() {
    		recyclerView.setAdapter(adapter);
		}

- _[materialup](https://github.com/Alelak/materialup) --- (From [Alelak](https://github.com/Alelak)) : 
Unofficial MaterialUp API Wrapper for Android. [MaterialUp(一个UI灵感设计分享网站)的一个非官方的API]._

    <img src="https://github.com/Alelak/materialup/raw/master/screenshots/screenshot.png" width="35%"> 

		//Get popular posts:
		MaterialUp.getPosts(context, page, MaterialUp.SORT.POPULAR, new MaterialUpCallback() {
		    @Override
		    public void onSuccess(List <Post> posts, Response response) {
		        // do stuff with posts!
		    }
		
		    @Override
		    public void onFailure(Request request, IOException e) {
		        // show a toast!
		
		    }
		});

		//Get latest posts:
		MaterialUp.getPosts(context, page, MaterialUp.SORT.LATEST, new MaterialUpCallback() {
		    @Override
		    public void onSuccess(List <Post> posts, Response response) {
		        // do stuff with posts!
		    }
		
		    @Override
		    public void onFailure(Request request, IOException e) {
		        // show a toast!
		
		    }
		});

3.Architecture:

- _[screenplay](https://github.com/weefbellington/screenplay) --- (From [weefbellington](https://github.com/weefbellington)) : 
A minimalist, View-based application framework for Android. [极简view框架]._

	<img src="http://i.imgur.com/NPvkNSG.png" width="90%"> 

		public class ExampleStage extends Stage {
		
		    private final ExampleApplication application;
		    private final Rigger animationRigger;
		
		    public ExampleStage(ExampleApplication application) {
		        animationRigger = new CrossfadeRigger(application);
		        addComponents(new ClickBindingComponent());
		    }
		
		    @Override
		    public int getLayoutId() {
		        return R.layout.example_scene;
		    }
		
		    @Override
		    public Rigger getRigger() {
		        return animationRigger;
		    }
		
		    private class ClickBindingComponent implements Component {
		        @Override
		        public void afterSetUp(Stage stage, boolean isInitializing) {
		            View parent = stage.getView();
		            View nextButton = parent.findViewById(R.id.next);
		            nextButton.setOnClickListener(showNextStage);
		        }
		
		        @Override
		        public void beforeTearDown(Stage stage, boolean isFinishing) {}
		
		        private View.OnClickListener showNextStage = new View.OnClickListener() {
		            @Override
		            public void onClick(View v) {
		                // add a new scene to the history and trigger a transition
		                Flow flow = application.getMainFlow();
		                flow.set(new NextStage(application));
		            }
		        };
		    }
		}

#### article ####

- _[What is all this Clean Architecture jibber-jabber about?](http://pguardiola.com/blog/clean-architecture-part-1/) --- (From Author  [Pablo Guardiola](http://pguardiola.com/) blog [http://pguardiola.com/blog](http://pguardiola.com/blog)) --- [No Source]_ 

	Tately, there are a lot of people in the Android community, talking about Architecture, especially about Clean. That's good news! 

	I'm pretty sure some of you are familiar with terms like layers, Ports and Adapters, boundaries, etc. but others aren't.

	Although Architecture is not new in Mobile development, (E.g. Forgetting Android by Jorge J. Barroso and Software Design patterns on Android by Pedro Vicente Gómez), we developers, after years of hard work, are realising that it's an important aspect if we want our apps to succeed.

	So... What's the problem?? [Translation：所有关于Clean Architecture的思考]. 
 
	Chinese Translation Address : Waiting for someone to Translation it.

#### App-Demo ####

- _[UltimateAndroidAppTemplate](https://github.com/AndreiD/UltimateAndroidAppTemplate) --- (From [AndreiD](https://github.com/AndreiD) ) : 
A ready to use android app template. Powered by Android Annotations Retrofit API ready to be used Picasso for image loading Snackbar, RecyclerView, Pull to Refresh etc. Feedback contact by email for feedback / Settings Page with some dummy settings etc. [使用一些知名的Library组成的模板类型App-Demo]._

	<img src="https://github.com/AndreiD/UltimateAndroidAppTemplate/raw/master/app/the_gif_1.gif" width="90%">

	
		dependencies {
		    compile fileTree(include: ['*.jar'], dir: 'libs')
		    apt "org.androidannotations:androidannotations:$AAVersion"
		    compile "org.androidannotations:androidannotations-api:$AAVersion"
		    compile 'com.android.support:appcompat-v7:23.0.1'
		    compile 'com.android.support:support-v4:23+'
		    compile 'com.android.support:support-annotations:23+'
		    compile 'com.android.support:recyclerview-v7:23+'
		    compile 'com.android.support:design:23+'
		    compile 'de.greenrobot:eventbus:2.4.0'
		    compile 'com.squareup.retrofit:retrofit:1.9.0'
		    compile 'com.squareup.okhttp:okhttp:2.3.0'
		    compile 'com.squareup.picasso:picasso:2.5.2'
		    compile 'com.android.support:recyclerview-v7:23+'
		    compile 'com.android.support:design:23+'		
		    //-------- app fonts -----------
		    compile 'uk.co.chrisjenx:calligraphy:2.1.0'	
		    //----- nice progress app ----
		    compile 'com.akexorcist:RoundCornerProgressBar:2.0.3'	
		}


	![](https://img.shields.io/badge/The%20Day15-End%20!-ED1C24.svg?style=flat)















----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 

## Day9
> ![](https://img.shields.io/badge/AndroidEveryday-Day9-green.svg?style=flat)   
> ***Time : October 30th,2015*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[FlippableStackView](https://github.com/blipinsk/FlippableStackView) --- (From [blipinsk](https://github.com/blipinsk)) : 
An Android library introducing a stack of Views with the first item being flippable. [显示view堆栈效果的库]._

    <img src="https://github.com/blipinsk/FlippableStackView/raw/master/FlippableStackView.gif" width="35%"> 

- _[PhotoView](https://github.com/chrisbanes/PhotoView) --- (From [chrisbanes](https://github.com/chrisbanes)) : 
Implementation of ImageView for Android that supports zooming, by various touch gestures. [图片手势控件、缩放,老牌优质控件]._

     <img src="https://camo.githubusercontent.com/cf5bfb6d896604aa9156e3e1beee89e0754de7db/68747470733a2f2f7261772e6769746875622e636f6d2f636872697362616e65732f50686f746f566965772f6d61737465722f6865616465725f677261706869632e706e67" width="55%"><img src="http://i.imgur.com/OfkCFAP.png" width="33%"> 

- _[PinchImageView](https://github.com/boycy815/PinchImageView) --- (From [boycy815](https://github.com/boycy815)) : 
An Android library introducing Picture gesture control like photoview supports zooming, can use with viewpager. [图片手势控制、缩放]._

    <img src="https://github.com/boycy815/PinchImageView/raw/master/gif/pager.gif" width="35%"> 

- _[subsampling-scale-image-view](https://github.com/davemorrissey/subsampling-scale-image-view) --- (From [davemorrissey](https://github.com/davemorrissey)) : 
Highly configurable, easily extendable view with pan and zoom gestures for displaying huge images without loss of detail. Perfect for photo galleries, maps, building plans etc. [缩放和显示大图(加载超1MB大图片)的Android类库]._

    <img src="http://i.imgur.com/M6xNCiW.png" width="65%"> 

2.Logic：

- _[fragmentargs](https://github.com/sockeqwe/fragmentargs) --- (From [sockeqwe](https://github.com/sockeqwe) & Tag  is [Annotation](https://github.com/sockeqwe/fragmentargs)) : 
Annotation Processor for setting arguments in android fragments. [编译时注解,用于activity和Fragment的参数传值]._

	<img src="http://i.imgur.com/5CLKoIv.png" width="90%">

		//Fragment：
		public class MyFragment extends Fragment {

		    @Arg
		    int id;	
		    @Arg
		    String title;
		
		    @Override
		    public void onCreate(Bundle savedInstanceState){
		        super.onCreate(savedInstanceState);
		        FragmentArgs.inject(this); // read @Arg fields
		    }
		
		    @Override
		    public View onCreateView(LayoutInflater inflater, 
		        ViewGroup container, Bundle savedInstanceState) {	
		            Toast.makeText(getActivity(), "Hello " + title, 
		                Toast.LENGTH_SHORT).show();		
		            return null;
		      }		
		}

		//Activity:
		public class MyActivity extends Activity {
		    public void onCreate(Bundle savedInstanceState){
		        super.onCreate(savedInstanceState);	
		        int id = 123;
		        String title = "test";	
		        // Using the generated Builder
		        Fragment fragment = 
		            new MyFragmentBuilder(id, title)
		            .build();	
		
		        // Fragment Transaction
		        getFragmentManager()
		            .beginTransaction()
		            .replace(R.id.container, fragment)
		            .commit();		
		    }	
		}

	Want to know more see Tomorrow's article.

- _[auto](https://github.com/google/auto) --- (From [google](https://github.com/google) & Tag  is [APT](https://github.com/google/auto)) : 
A collection of source code generators for Java. [google出品的Java 源代码生成器集合]._

	<img src="http://i.imgur.com/OAiVgrt.png" width="90%">

  * [AutoFactory](https://github.com/google/auto/tree/master/factory) - JSR-330-compatible factories.(兼容 JSR-330 的工厂)

  * [AutoService](https://github.com/google/auto/tree/master/service) - Provider-configuration files for [`ServiceLoader`](http://docs.oracle.com/javase/7/docs/api/java/util/ServiceLoader.html)(ServiceLoader 的 Provider-configuration 文件)

  * [AutoValue](https://github.com/google/auto/tree/master/value) - Immutable [value-type](http://en.wikipedia.org/wiki/Value_object) code generation for Java 1.6+.(Java 1.6+ 的不可变 value-type 代码生成)

  * [Common](https://github.com/google/auto/tree/master/common) - Helper utilities for writing annotation processors.(Helper 实用工具，用来编写注释处理器)

			
	E.g:AutoService will generate the file META-INF/services/javax.annotation.processing.Processor in the output classes folder. 

		@AutoService(Processor.class) 
		public class FactoryProcessor extends AbstractProcessor {
				...
		}	

- _[GAlette](https://github.com/uPhyca/GAlette) --- (From [uPhyca](https://github.com/uPhyca) & Tag  is [Annotation](https://github.com/uPhyca/GAlette)) : 
Annotation-triggered tracking along with Google Analytics for Android. [编译时注解,结合Google Analytics追踪统计]._

	<img src="http://i.imgur.com/06WMbOw.png" width="90%">

		//Application:
		public class MyApplication extends Application implements TrackerProvider {	
		    private Tracker mTracker;		
		    @Override
		    public void onCreate() {
		        super.onCreate();
		        GoogleAnalytics ga = GoogleAnalytics.getInstance(this);
		        mTracker = ga.newTracker(R.xml.your_tracker_resource);
		    }	
		    @Override
		    public Tracker getByName(String trackerName) {
		        return mTracker;
		    }
		}

		//track appView:@SendScreenView
		public class MainActivity extends Activity {
		    @Override
		    @SendScreenView(screenName = "main")
		    protected void onCreate(Bundle savedInstanceState) {
		        ...
		    }
		}	

		//track event:@SendEvent
		public class MainActivity extends Activity {
		    @Override
		    protected void onCreate(Bundle savedInstanceState) {
		        ...	
		        findViewById(R.id.button).setOnClickListener(new View.OnClickListener() {
		            @Override
		            @SendEvent(category = "button", action = "click")
		            public void onClick(View v) {
		                onButtonClicked();
		            }
		        });
		    }	
		}	
	
3.Architecture:

- _[cube-sdk](https://github.com/liaohuqiu/cube-sdk) --- (From [liaohuqiu](https://github.com/thiagokimo) A Developer from China) : 
A light package for Android development, it handles loading image and network request. [一套图片网络请求的框架]._

	<img src="https://raw.githubusercontent.com/etao-open-source/cube-sdk/dev/screen-shot.png" width="90%">  

	<img src="http://i.imgur.com/gQV9MpD.png" width="90%"> 

	Want See more imformation check this [website](http://cube-sdk.liaohuqiu.net/)

	DEMO project has been moved to [HERE](https://github.com/liaohuqiu/android-cube-app).

- _[android-flux-todo-app](https://github.com/lgvalle/android-flux-todo-app) --- (From [lgvalle](https://github.com/lgvalle)) : 
Example of how to implement an Android TODO App using Facebook Flux Architecture. [在android上探索Flux架构]._
 
	<img src="https://raw.githubusercontent.com/lgvalle/lgvalle.github.io/master/public/images/flux-graph-simple.png" width="90%"> 

	There are two **key features** to understand Flux:

	* The data flow is always **unidirectional**.
	
		An [unidirectional data flow][unidirectional] is the **core** of the Flux architecture and is what makes it so easy to learn. 
	It also provides great advantages when testing the application as discussed below.
	
	* The application is divided into **three main parts**:
	
		-  **View**: Application interface. It create actions in response to user interactions.
		- **Dispatcher**: Central hub through which pass all actions and whose responsibility is to make them arrive to every Store.
		- **Store**: Maintain the state for a particular application domain. They respond to actions according to current state, execute business logic and emit a _change_ event when they are done. This event is used by the view to update its interface.
	
	This three parts communicate through **Actions**: Simple plain objects, identified by a type, containing the data related to that action.

	Want See more imformation check today's article.


#### article ####

- _[flux-architecture](http://lgvalle.xyz/2015/08/04/flux-architecture/) --- (From Author  [lgvalle](https://github.com/lgvalle) blog [http://lgvalle.xyz/](http://lgvalle.xyz/)) --- [Source in [Github](https://github.com/lgvalle/android-flux-todo-app)]_ 

	Finding a good architecture for Android applications is not easy. Google seems to not care much about it, so there is no official recommendation on patterns beyond Activities lifecycle management.

	But defining an architecture for your application is important. Like it or not, every application is going to have an architecture. So you'd better be the one defining it than let it just emerge. [Translation：探索Facebook的Web-Flux 架构在android上的尝试]. 
 
	Chinese Translation Address : [Thanks To android-tech-frontier](http://www.devtf.cn/?p=1028)
	
	Introducing Flux Architecture:

	<img src="https://raw.githubusercontent.com/lgvalle/lgvalle.github.io/master/public/images/flux-graph-simple.png" width="90%"> 

	Stores:

	<img src="http://i.imgur.com/xmP9yZi.png" width="90%"> 

	Network requests and asynchronous calls：

	<img src="http://i.imgur.com/NuEYT9J.png" width="90%">

#### App-Demo ####

- _[plaid](https://github.com/nickbutcher/plaid) --- (From [nickbutcher](https://github.com/nickbutcher) Design news and inspiration) : 
Plaid is a showcase of material design that we hope you will keep installed. It pulls in news & inspiration from Designer News, Dribbble & Product Hunt. [带Material Design设计风格的App-Demo,从Designer News, Dribbble 以及 Product Hunt中获取内容]._

	<img src="https://github.com/nickbutcher/plaid/raw/master/screenshots/plaid_demo.gif" width="35%">

	Check the Source in [Github](https://github.com/nickbutcher/plaid).Want to know more about the App-Demo see [GooglePlay](https://play.google.com/apps/testing/io.plaidapp)

#### website 	

- _[http://www.8thlight.com](http://www.8thlight.com/) --- :Every Friday at noon, 8th Light hosts a lunch and talk on various software topics. Talks are given by 8th Light craftsmen or the occasional guest speaker, and they can range from discussions to hands-on exercises. All talks are recorded and available online. [一个轻量级的Blog]._

	<img src="http://i.imgur.com/WIHDngn.png" width="90%"> 

	![](https://img.shields.io/badge/The%20Day9-End%20!-ED1C24.svg?style=flat)


----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 

## Day18
> ![](https://img.shields.io/badge/AndroidEveryday-Day1-green.svg?style=flat)   
> ***Time : December 03th,2015*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[ChromeLikeSwipeLayout](https://github.com/ashqal/ChromeLikeSwipeLayout) --- (From [ashqal](https://github.com/ashqal)) : 
Pull down, and execute more action. [带贝塞尔曲线左右动画效果的下拉刷新]._

    <img src="https://raw.githubusercontent.com/ashqal/ChromeLikeSwipeLayout/master/screenshot/screenshot.png" width="90%"> 

- _[android-card-slide-panel](https://github.com/xmuSistone/android-card-slide-panel) --- (From [xmuSistone](https://github.com/xmuSistone)) : 
sliding around infinite loop. [模仿探探首页卡片左右滑动效果]._

    <img src="https://github.com/xmuSistone/android-card-slide-panel/raw/master/capture2.gif" width="32%"> 

- _[android-vertical-slide-view](https://github.com/xmuSistone/android-vertical-slide-view) --- (From [xmuSistone](https://github.com/xmuSistone)) : 
vertical slide to switch to the next fragment page, looks like vertical viewpager. [向下拖动加载下一页]._

    <img src="https://github.com/xmuSistone/android-vertical-slide-view/raw/master/capture.gif" width="32%"> 

2.Logic：

- _[android-task](https://github.com/vRallev/android-task) --- (From [vRallev](https://github.com/vRallev) & Tag  is [AsyncTask](https://github.com/vRallev/android-task)) : 
A library to execute tasks in the background for Android. [后台异步线程调度]._

	<img src="http://i.imgur.com/LEhacZT.png" width="90%"> 

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


- _[Android-scaex](https://github.com/petitviolet/Android-scaex) --- (From [petitviolet](https://github.com/petitviolet/) & Tag  is [Utils-PatternMatch](https://github.com/petitviolet/Android-scaex)) : 
A library to execute tasks in the background for Android. [一些基础的正则表达式]._

	<img src="http://i.imgur.com/ELGsbxo.png" width="90%"> 

	IF:

		/** returns primitive value pattern **/
		String result = IF.<String>x(false).then("hoge")
		        .ElseIf(false).then("foo")
		        .Else("bar");
		assert result == "bar";

		/** returns value the result of given method invoked **/
		String result4 = IF.<String>x(false).then(new Action<String>() {
		    @Override
		    public String run() {
		        return "hoge";
		    }
		}).ElseIf(true).then(new Action<String>() {
		    @Override
		    public String run() {
		        return "foo";
		    }
		}).Else(new Action<String>() {
		    @Override
		    public String run() {
		        Log.d(TAG, "in else condition!");
		        return "bar";
		    }
		});

	Match:

		/** pattern match by value condition **/
		int target = 100;
		String result1 = Match.<String, Integer>x(target)
		        .Case(target < 100).then("down")
		        .Case(target > 100).then("up")
		        .Case(target == 100).then("draw")
		        .eval();
		assert result1.equals("draw") == true;

	/** lazy pattern-match using Function interface in Case **/
	int result3 = Match.<Integer, Object>x(100)
	        .Case(String.class).then(1)
	        .Case(Boolean.class).then(2)
	        .Case(new Function.F1<Object, Boolean>() {
	            @Override
	            public Boolean apply(Object integer) {
	                return integer == 100;
	            }
	        }).then(3)
	        .Case(new Function.F1<Object, Boolean>() {
	            @Override
	            public Boolean apply(Object integer) {
	                // not evaluate
	                return integer == 999;
	            }
	        }).then(4)
	        .Case(Integer.class).then(5)
	        .eval();
	assert result3 == 3;

- _[JavaVerbalExpressions](https://github.com/VerbalExpressions/JavaVerbalExpressions) --- (From [VerbalExpressions](https://github.com/VerbalExpressions) & Tag  is [Utils-PatternMatch](https://github.com/VerbalExpressions/JavaVerbalExpressions)) : 
Java regular expressions made easy. [正则表达式]._

	![](http://i.imgur.com/QBrHZXV.png)

		VerbalExpression testRegex = VerbalExpression.regex()
		                                                .startOfLine().then("http").maybe("s")
		                            .then("://")
		                            .maybe("www.").anythingBut(" ")
		                            .endOfLine()
		                            .build();
		
		// Create an example URL
		String url = "https://www.google.com";
		
		// Use VerbalExpression's testExact() method to test if the entire string matches the regex
		testRegex.testExact(url); //True
		
		testRegex.toString(); // Outputs the regex used:
		                      // ^(?:http)(?:s)?(?:\:\/\/)(?:www\.)?(?:[^\ ]*)$

- _[rxsnappy](https://github.com/team-supercharge/rxsnappy) --- (From [team-supercharge](https://github.com/team-supercharge) & Tag  is [NoSQL](https://github.com/team-supercharge/rxsnappy)) : 
RxSnappy is a thread safe rxjava wrapper for the great SnappyDB fast key-value database for Android. [基于RXJava和SnappyDB优秀的NoSql数据操作方案]._

	<img src="http://i.imgur.com/9yQev8D.png" width="90%"> 

	1.Application onCreate():

		RxSnappy.init(context);

	2.Create RxSnappyClient:

		RxSnappyClient rxSnappyClient = new RxSnappyClient();

	3.Usage:

		public Observable<FooResponse> getFooResponse(String token, BarRequest barRequest){
		
			//Generate unique key 
			final String key = RxSnappyUtils.generateKey("fooresponse", token, barRequest);
			
			//Look for in cache with a time interval (ms)
			//If the data in cache is older than 15 sec it throws an exception
			return rxSnappyClient.getObject(key, 15000L, FooResponse.class)
			    .onErrorResumeNext(retrofitApi.getFooResponse(token, barRequest)
			        .flatMap(fooResponse -> rxSnappyClient.setObject(key, fooResponse));
		}





3.Architecture:

- _[whiskey](https://github.com/twitter/whiskey) --- (From [twitter](https://github.com/twitter)) : 
HTTP library for Android . [twitter开源的基于nio的HTTP请求框架]._


	<p>
	<img src="http://i.imgur.com/bMeNhxZ.png" width="150px" height="150px" align="left" hspace="15px" />
	This is beta software. Bug reports and contribution are welcome, but caution should be exercised in deployment.

	Whiskey is a Java HTTP library based on nio and intended especially to address the needs of Android mobile clients. It has no external dependencies.

	The library shares some code with Netty's codec implementations, but adopts a client performance-focused approach to handling HTTP requests. It has also been developed specifically for support of newer protocols: SPDY, HTTP/2 and QUIC.

	The application interface is designed to be extremely flexible, and supports both streaming and atomic operations, with both synchronous and asynchronous interaction.

	The internals of the library are built to support lock-free and zero-copy operation, with most logic executing on a single internal run loop managing many sockets.
	</p>


	<img src="http://i.imgur.com/28DKVA3.png" width="90%"> 


#### article ####

- _[Why I Don't Use Realm Anymore](http://johnpetitto.com/no-more-realm/) --- (From Author  [John Petitto](https://github.com/jpetitto) blog [http://johnpetitto.com/](http://johnpetitto.com/)) --- [No Source]_ 

	<p>
	<img src="http://i.imgur.com/6Sd9N7V.png" width="200px" height="200px" align="left" hspace="15px" />
	If you haven’t heard of Realm before, it’s a mobile database technology for Android (iOS too). Opposed to SQLite, it allows you to work with data objects directly at the persistence layer. On top of that, there is a powerful functional-style query API and effort has been made to make it even faster than traditional SQLite operations. It was for these reasons I decided to give Realm a try.

	When I first used Realm around a year ago, my initial impressions were quite good. I needed to persist some user data locally on the phone, but it was a bit too complex for SharedPreferences. Realm allowed me to quickly and cleanly write the necessary code to do this. There was no need to write any of the extra cruft that would have been required with SQLite.

	The next project I worked on needed a sophisticated offline mode for when the user lacked a network connection. The data that I grabbed over the network would have to be stored locally on the phone. I decided to go all in with Realm and see how it would scale as my project grew.
	</p>

	[Translation：为什么我不再使用Realm]. 
 
	Chinese Translation Address : [Thanks To jcodecraeer](http://jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/1203/3743.html)
	
#### App-Demo ####

- _[meiShi](https://github.com/sungerk/meiShi) --- (From [sungerk](https://github.com/sungerk) ) : 
Use some famous libraries build a video app dmo. [一个开源的视频类app-demo]._

	<img src="http://i.imgur.com/Hkc5dsh.png" width="47%"><img src="http://i.imgur.com/jE8p1p0.png" width="38.5%">

    compile 'com.android.support:appcompat-v7:23.1.1'
    compile 'com.android.support:design:23.1.1'
    compile 'com.android.support:cardview-v7:23.1.1'
    compile 'com.squareup.okhttp:okhttp:2.5.0'
    compile 'com.github.bumptech.glide:glide:3.6.1'
    compile 'com.github.bumptech.glide:okhttp-integration:1.3.1@aar'
    compile 'cn.bingoogolapple:bga-badgeview:1.0.2'
    compile 'com.github.traex.rippleeffect:library:1.3'
    compile 'com.soundcloud.android:android-crop:1.0.1@aar'
    compile 'com.github.dmytrodanylyk.android-process-button:library:1.0.4'

#### website 	

- _[https://coding.net](https://coding.net):A Chinese famous code management website like github [中国的GitHub]._

	<img src="http://i.imgur.com/3n5LV7W.jpg" width="90%"> 

	![](https://img.shields.io/badge/The%20Day18-End%20!-ED1C24.svg?style=flat)













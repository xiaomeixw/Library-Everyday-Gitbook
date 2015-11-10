----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 

## Day14
> ![](https://img.shields.io/badge/AndroidEveryday-Day14-green.svg?style=flat)   
> ***Time : November 10th,2015*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[ProgressWheel](https://github.com/Todd-Davies/ProgressWheel) --- (From [Todd-Davies](https://github.com/Todd-Davies)) : 
A progress wheel for android, intended for use instead of the standard progress bar. [loading加载]._

    <img src="https://github.com/Todd-Davies/ProgressWheel/raw/master/sample_image.png" width="30%"><img src="https://github.com/Todd-Davies/ProgressWheel/raw/master/sample_image_4.png" width="30%"><img src="https://github.com/Todd-Davies/ProgressWheel/raw/master/sample_image5.png" width="40%">

- _[SmoothProgressBar](https://github.com/castorflex/SmoothProgressBar) --- (From [castorflex](https://github.com/castorflex)) : 
A small Android library allowing you to have a smooth and customizable horizontal indeterminate ProgressBar. [loading加载]._

    <img src="https://github.com/castorflex/SmoothProgressBar/raw/master/screenshots/SPB_sample.gif" width="90%">

- _[MaterialProgressBar](https://github.com/DreaminginCodeZH/MaterialProgressBar) --- (From [DreaminginCodeZH](https://github.com/DreaminginCodeZH)) : 
Material design ProgressBar with consistent appearance. [Material design风格的loading加载]._

    <img src="https://github.com/DreaminginCodeZH/MaterialProgressBar/raw/master/screenshot/android_4_4_4.png" width="35%"><img src="https://github.com/DreaminginCodeZH/MaterialProgressBar/raw/master/screenshot/android_5_0_1_samsung.png" width="35%">

- _[MaterialLoadingProgressBar](https://github.com/lsjwzh/MaterialLoadingProgressBar) --- (From [lsjwzh](https://github.com/lsjwzh)) : 
MaterialLoadingProgressBar provide a styled ProgressBar which looks like SwipeRefreshLayout's loading indicator(support-v4 v21+). [类谷歌SwipeRefreshLayout风格的loading加载]._

    <img src="https://github.com/lsjwzh/MaterialLoadingProgressBar/raw/master/screen.gif" width="35%">

- _[android-square-progressbar](https://github.com/mrwonderman/android-square-progressbar) --- (From [mrwonderman](https://github.com/mrwonderman)) : 
An android library to display a progressbar that goes around an image. [图片loading提示]._

    <img src="https://camo.githubusercontent.com/3ddc0a0d9ed3c39f806f1459d49e46e87be81e29/68747470733a2f2f6d61766868772d626e313330362e66696c65732e316472762e636f6d2f793270386e736e3035354b30583172663935725743634375686f6b583451453542313953506f686c74513735386174513948635632694b334b5f773830325765673668794d70624c507770574745476f62385f7a5f62725651536e4c572d50664e43773274554e6132672d5930786b344279344c6a4a316e564f7445394a7a6a5737535f6251716c4833796668657a793847646a744d4b717a6e5832486a74463834363163456536394b532d6f512f636f7665725f6769746875622e706e67" width="90%">

- _[GoogleProgressBar](https://github.com/jpardogo/GoogleProgressBar) --- (From [jpardogo](https://github.com/jpardogo)) : 
Android library to display progress like google does in some of his services. [类谷歌风loading]._

    <img src="https://raw.githubusercontent.com/jpardogo/GoogleProgressBar/master/art/GoogleProgressBar.gif" width="25%"><img src="https://raw.githubusercontent.com/jpardogo/GoogleProgressBar/dev/art/GoogleDices.gif" width="25%"><img src="https://raw.githubusercontent.com/jpardogo/GoogleProgressBar/master/art/NexusRotationCross.gif" width="25%"><img src="https://raw.githubusercontent.com/MewX/google-progress-bar/gpb-chrome/art/ChromeFloatingCircles.gif" width="25%">

2.Logic：

- _[jackdaw](https://github.com/vbauer/jackdaw) --- (From [vbauer](https://github.com/vbauer) & Tag  is [Annotation](https://github.com/vbauer/jackdaw)) : 
Java Annotation Processor which allows to simplify development. [减少开发的常用注解关键词]._

	<p>
	<img src="https://github.com/vbauer/jackdaw/raw/master/jackdaw-misc/jackdaw.png" width="200px" height="200px" align="left" hspace="15px" />
	Jackdaw is a Java Annotation Processor which allows to simplify Java/Android development and prevents writing of tedious code.Jackdaw was inspired by Lombok project, but in comparison with Lombok:it does not need to have an extra plugin in IDE & it does not modify the existing source code.Jackdaw uses JitPack.io for distribution, so you need to configure JitPack's Maven repository to fetch artifacts (dependencies).It is necessary to make dependency on jackdaw-core. This module contains compile time annotations which will be used to give a hints for APT. Module jackdaw-apt contains annotation processor and all correlated logic.
	</p>



	**Jackdaw** supports the following compile time annotations:
	
	<ul>
	    <li>@JAdapter</li>
	    <li>@JBean</li>
	    <li>@JBuilder</li>
	    <li>@JClassDescriptor</li>
	    <li>@JComparator</li>
	    <li>JFactoryMethod/li>
	    <li>@JFunction</li>
	    <li>@JMessage</li>
	    <li>@JPredicate</li>
	    <li>@JRepeatable</li>
	    <li>@JService</li>
	    <li>@JSupplier</li>
	</ul>


    <img src="http://i.imgur.com/WTt4hEb.png" width="90%">

	EX: @JAdapter 

		//Original class MouseListener
		@JAdapter
		public interface MouseListener {
		    void onMove(int x, int y);
		    void onPressed(int button);
		}

		//Generated class MouseListenerAdapter
		public class MouseListenerAdapter implements MouseListener {
		    public void onMove(final int x, final int y) {
		    }
		    public void onPresses(final int button) {
		    }
		}

	EX: @JBuilder

		//Original class Company:
		@JBuilder
		public class Company {
		    private int id;
		    private String name;
		    private Set<String> descriptions;
		
		    public int getId() { return id; }
		    public void setId(final int id) { this.id = id; }
		
		    public String getName() { return name; }
		    public void setName(final String name) { this.name = name; }
		
		    public Set<String> getDescriptions() { return descriptions; }
		    public void setDescriptions(final Set<String> descriptions) { this.descriptions = descriptions; }
		}

		//Generated class CompanyBuilder:
		public class CompanyBuilder {
		    private int id;
		    private String name;
		    private Set<String> descriptions;
		
		    public static CompanyBuilder create() {
		        return new CompanyBuilder();
		    }
		    public CompanyBuilder id(final int id) {
		        this.id = id;
		        return this;
		    }
		    public CompanyBuilder name(final String name) {
		        this.name = name;
		        return this;
		    }
		    public CompanyBuilder descriptions(final Set<String> descriptions) {
		        this.descriptions = descriptions;
		        return this;
		    }
		    public Company build() {
		        final Company object = new Company();
		        object.setId(id);
		        object.setName(name);
		        object.setListed(listed);
		        object.setDescriptions(descriptions);
		        return object;
		    }
		}

3.Architecture:

- _[Carpaccio](https://github.com/florent37/Carpaccio) --- (From [florent37](https://github.com/florent37)) : 
Data Mapping & Smarter Views framework for android. [各种View和Data绑定]._

	<img src="https://raw.githubusercontent.com/florent37/Carpaccio/master/screenshot/carpaccio_small.png"/>
	
	Data Mapping & Smarter Views framework for android.

	With Carpaccio, your views became smarter, instead of calling functions on views, now your views can call functions ! You no longer need to extend a view to set a custom behavior

	Carpaccio also come with a beautiful mapping engine !
	



	##ImageViewController
	
	```xml
	<com.github.florent37.carpaccio.Carpaccio
	        app:register="
	            com.github.florent37.carpaccio.controllers.ImageViewController;
	        ">
	
	        <ImageView
	             android:tag="
	                 url(http://i.imgur.com/DvpvklR.png)
	             " />
	</com.github.florent37.carpaccio.Carpaccio>
	```
	
	![url](https://raw.githubusercontent.com/florent37/Carpaccio/master/screenshot/url_small.png)
	
	**WORKS WITH ANDROID STUDIO PREVIEW !!!**, don't hesitate to refresh your preview.
	
	Preview an url image
	
	```xml
	<ImageView
	     android:tag="
	        enablePreview();
	        url(http://i.imgur.com/DvpvklR.png);
	     " />
	```
	
	![url](https://raw.githubusercontent.com/florent37/Carpaccio/master/screenshot/preview_image_url_small.png)
	
	And some awesome customisations
	
	
	![circle](https://raw.githubusercontent.com/florent37/Carpaccio/master/screenshot/circle_small_2.png)
	![blur](https://raw.githubusercontent.com/florent37/Carpaccio/master/screenshot/blur_small.png)
	![greyscale](https://raw.githubusercontent.com/florent37/Carpaccio/master/screenshot/greyscale_small.png)
	
	```xml
	<ImageView
	      android:tag="
	
	           circle();
	           blur(); OR willBlur();
	           greyScale(); OR willGreyScale();
	
	           url(http://i.imgur.com/DvpvklR.png);
	      " />
	```
	
	[![Video](http://share.gifyoutube.com/mGz9OZ.gif)](https://youtu.be/A0eyvpNh5wM)
	[![Video](http://share.gifyoutube.com/vpMYjp.gif)](https://youtu.be/4b84gswKGkA)
	
	
	```xml
<ImageView
      android:tag="
           animateMaterial(6000);
           kenburns();
           url(http://i.imgur.com/DvpvklR.png);
      " />
```


#### article ####

- _[speed-up-your-app](http://blog.udinic.com/2015/09/15/speed-up-your-app) --- (From Author  [udinic](https://github.com/udinic) blog [http://blog.udinic.com/](http://blog.udinic.com/)) --- [No Source]_ 

	<p>
	<img src="http://i.imgur.com/uZcjj36.png" width="200px" height="200px" align="left" hspace="15px" />
	A few weeks ago, I gave a talk about Android Performance Optimization, at Droidcon NYC.
	I invested a lot of time in this presentation, since I wanted to show real examples for performance issues, and how to identify them with the available tools. I had to cut down about a half of my slides because I didn’t have enough time to show everything. In this post, I’ll summarize everything I was talking about, and show examples I didn’t have time to go over..
	</p>


	My Rules
	Everytime I approach a performance problem, or looking for performance problems, I follow these rules:
	
	- _Always Measure - Optimizing with your eyes is never a good idea. After looking at the same animation for a few times, you’ll start imagining it’s running faster. Numbers don’t lie. Use the tools we’ll go over soon, and measure how your app performs a few times before and after you make your change._
	
	- _Use slow devices - If you really want to expose all the weak spots, slower devices will help you more. Newer and stronger devices might not get too excited about performance issues you may have, but not all your users use the latest and greatest._
	
	- _Trade-offs - Performance optimization is all about trade-offs. You optimize one thing - it comes on the expense of another. In many cases, that other thing can be your time spent finding and fixing it, but it can also be the quality of your bitmaps or the amount of data you should store in a specific data structure. Prepare yourself to make sacrifices._
	
	[加速你的APP]. 
	Chinese Translation Address : [Thanks To android-tech-frontier](http://www.devtf.cn/?p=1097)
	
	<img src="http://i.imgur.com/cyGEUrC.png" width="90%">

	<img src="http://i.imgur.com/FHdb7dt.png" width="90%">

	<img src="http://i.imgur.com/x7N3sB9.png" width="90%">


	![](https://img.shields.io/badge/The%20Day14-End%20!-ED1C24.svg?style=flat)













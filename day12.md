----------------
<img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> <img src="http://i.imgur.com/DJgzbkd.gif" width="32%">  <img src="http://i.imgur.com/DJgzbkd.gif" width="32%"> 

## Day12
> ![](https://img.shields.io/badge/AndroidEveryday-Day12-green.svg?style=flat)   
> ***Time : November 1th&2th,2015*** / ***Author : [xiaomeixw](https://github.com/xiaomeixw)***

#### library ####

1.UI:

- _[TabbedCoordinatorLayout](https://github.com/vitovalov/TabbedCoordinatorLayout) --- (From [vitovalov](https://github.com/vitovalov)) : 
TabbedCoordinatorLayout is a Sample project demostrating the usage of TabLayout (ViewPager with Tabs) inside of CollapsingToolbarLayout all together in CoordinatorLayout. [基于Android Design Support Library兼容控件实现视差Tab效果]._

    <img src="https://github.com/vitovalov/TabbedCoordinatorLayout/raw/master/art/demo.gif" width="35%"> 

- _[BlurZoomGallery](https://github.com/fafaldo/BlurZoomGallery) --- (From [fafaldo](https://github.com/fafaldo)) : 
Extended CoordinatorLayout, that helps creating background galleries. [继承自 CoordinatorLayout,实现背景缩放与模糊效果]._

    <img src="https://github.com/fafaldo/BlurZoomGallery/raw/master/blurzoomgallery.gif" width="35%"> 

- _[Lab-Android-DesignLibrary](https://github.com/nuuneoi/Lab-Android-DesignLibrary) --- (From [nuuneoi](https://github.com/nuuneoi)) : 
A full tutorial on how to use Android Design Support Library. (60 mins). [基于Android Design Support Library兼容控件实现的Simple]._

    <img src="https://camo.githubusercontent.com/1fffe842f6aee3dcb0944365b9f7015c265ec63d/687474703a2f2f696e746865636865657365666163746f72792e636f6d2f75706c6f6164732f736f757263652f64657369676e6c6962726172792f7461726765742e676966" width="35%"> 

- _[LargeImage](https://github.com/LuckyJayce/LargeImage) --- (From [LuckyJayce](https://github.com/LuckyJayce)) : 
Loading big Image,Maximum support 10000ps x 10000ps. [Android 加载大图 可以高清显示10000*10000像素的图片]._

    <img src="http://i.imgur.com/ODUwRat.png" width="100%"> 

2.Logic：

- _[enroscar-async](https://github.com/stanfy/enroscar-async) --- (From [stanfy](https://github.com/stanfy) & Tag  is [AsyncTask](https://github.com/stanfy/enroscar-async)) : 
Makes it easy to put your asynchronous operations behind Android's Loader. [使用注解异步线程调度]._

	<img src="http://i.imgur.com/Pp3wTOH.png" width="100%">
	
		//1.Describe an asynchronous operation.
		class Foo {
		  @Load Async<String> loadGreeting(final String name) {
		    return Tools.async(new Callable<String>() {
		      public String call() {
		        try { Thread.sleep(1000); } catch (InterruptedException ignored) { }
		        return "Hello " + name;
		      }
		    });
		  }
		} 
	
		//2.Use it
		// this an object that provides operations
		Foo foo = new Foo();
		
		// prepare the operator
		// FooOperator is a generated class
		FooOperator operator = FooOperator.build()
		    .withinActivity(activity)
		    .operations(foo)
		    .get();
		
		// subscribing
		operator.when().loadGreetingIsFinished()
		    .doOnResult(new Action<String>() {
		      @Override
		      public void act(final String greeting) {
		        Log.i("Async", "Greeting loaded: " + greeting);
		      }
		    });
		
		// starting
		operator.loadGreeting();
		
		// cancelling
		operator.cancelLoadGreeting(); 

- _[feather](https://github.com/zsoltherpai/feather) --- (From [zsoltherpai](https://github.com/zsoltherpai) & Tag  is [Annotation](https://github.com/zsoltherpai/feather)):Lightweight dependency injection for Java and Android (JSR-330). [Java和android轻量级的依赖注入]._

	<img src="http://i.imgur.com/0RQHo15.png" width="100%">

		public class A {
		    @Inject
		    public A(B b) {
		        // ...
		    }
		}
		
		public class B {
		    @Inject
		    public B(C c, D d) {
		        // ...
		    }
		}
		
		public class C {}
		
		@Singleton
		public class D {
		    // something expensive or other reasons for being singleton
		}

- _[secure-preferences](https://github.com/scottyab/secure-preferences) --- (From [scottyab](https://github.com/scottyab) & Tag is [Encryption](https://github.com/zsoltherpai/feather)): Android Shared preference wrapper than encrypts the values of Shared Preferences. It's not bullet proof security but rather a quick win for incrementally making your android app more secure. [给Shared Preferences存储的数据进行AES的加密]._

	<img src="https://camo.githubusercontent.com/29a9bb9967b7584cce1341c726817284cae1cd7a/68747470733a2f2f7261772e6769746875622e636f6d2f73636f74747961622f7365637572652d707265666572656e6365732f6d61737465722f646f63732f696d616765732f73735f6672616d655f7365637572655f707265662e706e67" width="35%">

	<img src="http://i.imgur.com/WqJicmm.png" width="100%">

		SecurePreferences securePrefs = new SecurePreferences(context, "userpassword","my_user_prefs.xml");
		securePrefs.handlePasswordChange("newPassword", context);

- _[java-aes-crypto](https://github.com/tozny/java-aes-crypto) --- (From [tozny](https://github.com/tozny) & Tag  is [Encryption](https://github.com/tozny/java-aes-crypto)):A simple Android class for encrypting & decrypting strings, aiming to avoid the classic mistakes that most such classes suffer from. [使用AES加解密]._

	<img src="http://i.imgur.com/hjZWLkD.png" width="100%">

		//1.Generate new key
		AesCbcWithIntegrity.SecretKeys keys = AesCbcWithIntegrity.generateKey();

		//2.Encrypt
		AesCbcWithIntegrity.CipherTextIvMac cipherTextIvMac = AesCbcWithIntegrity.encrypt("some test", keys);
   		//store or send to server
   		String ciphertextString = cipherTextIvMac.toString();

		//3.Decrypt
		String plainText = AesCbcWithIntegrity.decryptString(cipherTextIvMac, keys);

- _[AESCrypt-Android](https://github.com/scottyab/AESCrypt-Android) --- (From [scottyab](https://github.com/scottyab) & Tag  is [Encryption](https://github.com/scottyab/AESCrypt-Android)):Simple API to perform AES encryption on Android. This is the Android counterpart to the AESCrypt library Ruby and Obj-C (with the same defaults) created by Gurpartap Singh. [使用AES加解密]._

	<img src="http://i.imgur.com/oy0SiL8.png" width="100%">

		//Encrypt
		String password = "password";
	    String message = "hello world"; 
	    try {
	        String encryptedMsg = AESCrypt.encrypt(password, message);
	    }catch (GeneralSecurityException e){
	      //handle error
	    }	
	
		//Decrypt
		String password = "password";
	    String encryptedMsg = "2B22cS3UC5s35WBihLBo8w==";
	    try {
	        String messageAfterDecrypt = AESCrypt.decrypt(password, encryptedMsg);
	    }catch (GeneralSecurityException e){
	     //handle error - could be due to incorrect password or tampered encryptedMsg
	    }

3.Architecture:

- _[powermock](https://github.com/jayway/powermock) --- (From [jayway](https://github.com/jayway)) : 
PowerMock is a Java framework that allows you to unit test code normally regarded as untestable. [超强的测试框架]._

	<img src="https://github.com/jayway/powermock/raw/master/powermock.png" width="35%"> 



	![](https://img.shields.io/badge/The%20Day12-End%20!-ED1C24.svg?style=flat)













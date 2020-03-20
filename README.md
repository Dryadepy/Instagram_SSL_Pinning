# Instagram SSL Pinning
Bypass Instagram SSL Pinning on Android (`ARM and x86`) Version **133.0.0.32.120** 

## Requirements

* Latest version of JDK ([Download](https://www.oracle.com/technetwork/java/javase/downloads/jdk11-downloads-5066655.html))

* Burp Suite **v1.7.36** (***.jar version**) ([Download](https://portswigger.net/burp/releases/download?product=community&version=1.7.36&type=Jar))   
  ***!!! Please DON'T USE CHARLES, FIDDLER OR MITMPROXY. Only use \*.JAR VERSION of Burp Suit and ONLY VERSION 1.7.36, NOT v2 or v2020. And please run it with the LATEST VERSION OF JAVA !!!***  
  
* Instagram APK ([ARM](https://www.apkmirror.com/apk/instagram/instagram-instagram/instagram-instagram-133-0-0-32-120-release/instagram-133-0-0-32-120-3-android-apk-download/) - [x86](https://www.apkmirror.com/apk/instagram/instagram-instagram/instagram-instagram-133-0-0-32-120-release/instagram-133-0-0-32-120-4-android-apk-download/)) - ***For root method only***  
  ***Download only from this links, not Google Play or somewhere else***  
  
* a **rooted** Android device (Physical or virtual) - ***For root method only***  
   *[Genymotion](https://www.genymotion.com/) Android 8+ recommended.*  
   *Genymotion virtual devices is x86 and rooted by default.*
   
* ADB ([Download](https://developer.android.com/studio/releases/platform-tools.html)) - ***For root method only***  
    *Genymotion will install ADB automatically and you can find it on `<Genymotion Installation path>/tools`*
  
## Non-Root Method (Easier way, Recommended)

### Usage

1. Download and install patched APK ([ARM](https://github.com/itsMoji/Instagram_SSL_Pinning/tree/master/non-root/arm) - [x86](https://github.com/itsMoji/Instagram_SSL_Pinning/tree/master/non-root/x86)). (*ARM on physical device or ARM on Genymotion Android 8-Oreo with [ARM Translation](https://mega.nz/#F!JhcFwKpC!yfhfeUzvIZoSdBgfdZ9Ygg) recommended!*)

    1.2. **For x86 only,** Open Instagram app (wait a few seconds) and close it.  
           ***It's important to run Instagram app once, before setting the proxy!***  

2. Run Burp Suite with `/<JDK Installation path>/bin/java -jar burpsuite_community.jar` and setting up proxy on your Android device.  
    *You should [install Burp Suite certificate on your Android device](https://distributedcompute.com/2017/12/12/tech-note-installing-burp-certificate-on-android/)* 

3. That's it! Now open the Instagram app on your device and intercept the requests in Burp Suite !  

## Root Method

[Watch tutorial video](https://youtu.be/gmYzlpy2Ii4) 

### Usage (**It's important to do step by step**)

1. Install Genymotion or your virtual device and start it.  

2. Download and install Instagram apk on your device.  

3. Open Instagram app (wait a few seconds) and close it.  
  ***It's important to run Instagram app once, before start patching!***  
  
4. Download the patched file ([ARM](https://github.com/itsMoji/Instagram_SSL_Pinning/tree/master/arm) - [x86](https://github.com/itsMoji/Instagram_SSL_Pinning/tree/master/x86)) and push it to the device:  
  ARM: `adb push libliger.so /data/data/com.instagram.android/lib-superpack-zstd/libliger.so`  
  x86: `adb push libliger.so /data/data/com.instagram.android/lib-zstd/libliger.so`  
  
5. Open Instagram app again (wait a few seconds) and close it.  
  
6. Run Burp Suite with `/<JDK Installation path>/bin/java -jar burpsuite_community.jar` and setting up proxy on your Android device.  
    ***You must set the proxy in this step***  
    *You should [install Burp Suite certificate on your Android device](https://distributedcompute.com/2017/12/12/tech-note-installing-burp-certificate-on-android/)* 
    
7. That's it! Now open the Instagram app and intercept the requests in Burp Suite !

## Instagram Signature Key for ARM and x86

* **v133.0.0.32.120:** `3ab43afe09a883498054ae3584340e4a27b900e4f296e411a8f98ecf6db2bbc4`  

## Donations

If you want to show your appreciation, you can donate via [PayPal](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=its13moji%40gmail%2ecom&lc=US&item_name=Instagram_SSL_Pinning_Donation).  
Bitcoin: `1GhTaq5HqEj4xpP42drPxT4FNzxp8zUTfK`  
Iranian users can donate via [IDPay](https://idpay.ir/itsmoji).  
  
Thanks.
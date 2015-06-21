#android-webview-boilerplate
webview boilerplate for Android Studio

Hello! This is a fork of slymax's Android Webview boilerplate. I removed a couple of things to make it a pure and simple "drag n drop your website in and go" boilerplate.

I've written a Swift boilerplate for iOS too, which you can find here.

Armed with these tools, you can release your web app/game onto iOS and Android with very little effort!

The readme stuff below was written by slymax...

### Getting Started

1. [Install Android Studio](http://developer.android.com/sdk/index.html), make sure that the [Android SDK Tools](http://developer.android.com/sdk/index.html#Other) are properly installed and install the [appropriate packages](http://developer.android.com/sdk/installing/adding-packages.html) for the platforms you want to target.

2. Download or clone this repository and import it into Android Studio.

### Using a remote source

If you want to create an app that simply displays the contents of a remote website

1. uncomment **line 31** in `MainActivity.java` and change `http://example.com/` to match your remote source

	```
	mWebView.loadUrl("http://example.com");
	```

2. uncomment **line 34**

	```
	mWebView.setWebViewClient(new MyAppWebViewClient());
	```

3. open the `MyAppWebViewClient.java` file and replace `example.com` in **line 12** with your custom url

	```
	if (Uri.parse(url).getHost().endsWith("example.com")) {
	```

### Using a local source

If you want to create a local HTML5 android app

1. uncomment **line 37** in `MainActivity.java`

	```
	mWebView.loadUrl("file:///android_asset/www/index.html");
	```

2. replace the boilerplate website in `src/main/assets/www/` with your own HTML, CSS and JavaScript files

# DxLoadingButton

android button to loading view with animation,and load successful/failed animation


[![](https://jitpack.io/v/StevenDXC/DxLoadingButton.svg)](https://jitpack.io/#StevenDXC/DxLoadingButton)

Demo:
---
   
![image](https://github.com/StevenDXC/DxLoadingButton/blob/master/image/loadingButton.gif)

with activity transition animation demo:

![image](https://github.com/StevenDXC/DxLoadingButton/blob/master/image/loadingButton2.gif)

Usage:
---

layout:

```xml
<com.dx.dxloadingbutton.lib.LoadingButton
     android:id="@+id/loading_btn"
     android:layout_gravity="center"
     android:layout_width="228dp"
     android:layout_height="wrap_content"
     app:lb_resetAfterFailed="true"
     app:lb_btnRippleColor="#000000"
     app:lb_btnText="@string/button_text" 
/>
```
code:

```java
LoadingButton lb = (LoadingButton)findViewById(R.id.loading_btn);
lb.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                lb.startLoading(); //start loading 
            }
});
```
show successful animation:

```java
 lb.loadingSuccessful();
```
show failed animation:

```java
 lb.loadingFailed();
```
cancel loading:

```java
 lb.cancelLoading();
```

reset:

```java
 lb.reset();
```

dependency
---
Add it in your root build.gradle at the end of repositories:

```java
allprojects {
    repositories {
	...
	maven { url 'https://jitpack.io' }
    }
}
```
add dependency：

```java
dependencies {
    compile 'com.github.StevenDXC:DxLoadingButton:1.5'
}
```

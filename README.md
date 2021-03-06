<h1 align="center">Super Toolbar</h1>
<p align="center">Android native toolbar on steroids 💪</p>
<p align="center">
  <a href="https://travis-ci.org/andrefrsousa/SuperToolbar"><img src="https://travis-ci.org/andrefrsousa/SuperToolbar.svg?branch=master" alt="Build Status"></a>
  <a href="https://jitpack.io/#andrefrsousa/SuperToolbar"><img src="https://jitpack.io/v/andrefrsousa/SuperToolbar.svg" alt="jitpack"></a>
  <a href="https://android-arsenal.com/api?level=14"><img src="https://img.shields.io/badge/API-14%2B-orange.svg?style=flat" alt="api"></a>
  <a href="https://android-arsenal.com/details/1/7261"><img src="https://img.shields.io/badge/Android%20Arsenal-SuperBottomSheet-green.svg?style=flat" alt="Android Arsenal"></a>
</p>
  
### Summary  

* Animate the toolbar elevation when scrolling
* Center horizontal the toolbar title
* Use light title font

Also, it has been written **100% in Kotlin**. ❤️  

## Download  
  
This library is available in **jitpack**, so you need to add this repository to your root build.gradle at the end of repositories:
   
```groovy  
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```
	
Add the dependency:

```groovy 
dependencies {
    implementation 'com.github.andrefrsousa:SuperToolbar:1.1.0'
}
```  

## Sample Project  

We have a sample project in Kotlin that demonstrates the lib usages [here](https://github.com/andrefrsousa/SuperToolbar/blob/master/demo/src/main/java/com/andrefrsousa/supertoolbar/demo/DemoActivity.kt).

![](/raw/example.gif)

## Usage  

It is recommended to check the sample project to get a complete understanding of all the features offered by the library.  
In order to show the toolbar elevation you just need to call:

```kotlin
fun setElevationVisibility(show: Boolean)
```  

If what to have the same effect found in Google Messages app for example, you to add a scroll listener to your RecyclerView or ScrollView. Like this:

```kotlin

myRecyclerView.addOnScrollListener(object : RecyclerView.OnScrollListener() {
    override fun onScrolled(recyclerView: RecyclerView, dx: Int, dy: Int) {
        super.onScrolled(recyclerView, dx, dy)
        toolbar.setElevationVisibility(recyclerView.canScrollVertically(-1))
    }
})

```

  
## Customization
  
You can costumize your toolber using the following attributes:

```xml

// The duration of the elevation animation. By default is 250 miliseconds.
<attr name="superToolbar_animationDuration" format="integer"/>

// If you want to show the toolbar elevation when created. By default is false.
<attr name="superToolbar_showElevationAtStart" format="boolean"/>

// Center the toolbar title. By default is false.
<attr name="superToolbar_centerTitle" format="boolean"/>

// Use a light font as the toolbar title. Default is false.
<attr name="superToolbar_useLightFont" format="boolean"/>

```

## Project Maintained By

### [André Sousa](https://andrefrsousa.github.io)

Design-focused Engineer | Front-end Developer | Open-Source Enthusiast | Android | Husband | Foodie

<a href="https://www.linkedin.com/in/andrefrsousa/"><img src="https://github.com/andrefrsousa/social-icons/blob/master/linkedin.png?raw=true" width="40" style="margin-right:8px"></a>
<a href="https://stackoverflow.com/users/1574250/andré-sousa"><img src="https://github.com/andrefrsousa/social-icons/blob/master/stackoverflow.png?raw=true" width="40" style="margin-right:8px"></a>
<a href="https://medium.com/andré-sousa"><img src="https://github.com/andrefrsousa/social-icons/blob/master/medium.png?raw=true" width="40" style="margin-right:8px"></a>
<a href="https://twitter.com/andrefrsousa"><img src="https://github.com/andrefrsousa/social-icons/blob/master/twitter.png?raw=true" width="40" style="margin-right:8px"></a>
  
## License  
  
```  
The MIT License (MIT)  
  
Copyright (c) 2018 André Sousa  
  
Permission is hereby granted, free of charge, to any person obtaining a copy  
of this software and associated documentation files (the "Software"), to deal  
in the Software without restriction, including without limitation the rights  
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell  
copies of the Software, and to permit persons to whom the Software is  
furnished to do so, subject to the following conditions:  
  
The above copyright notice and this permission notice shall be included in all  
copies or substantial portions of the Software.  
  
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR  
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,  
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE  
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER  
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,  
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE  
SOFTWARE.

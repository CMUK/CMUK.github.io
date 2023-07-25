---
date: 2022-07-22 13:58:10+00:00
title: Ionic Framework v6.0 with ReactJs 17.0.2 Vs .NET MAUI 17.3 Preview 4
categories:
  - Mobile Apps
tags:
  - Android
  - Ionic framework 6
  - MAUI
  - Mobile
  - NET
  - Programming
  - ReactJs
---

.NET MAUI, which stands for Multi-platform App UI, enables developers to write C# code using .NET 6. It is an evolution of Xamarin.Forms, offering a unified approach to code and UI sharing across multiple platforms.

Having previously used XAML for my [Games Collection ](https://mckellar.wordpress.com/2016/07/10/xamarin-games-collection-wip/)work in progress, I was eager to explore the capabilities of MAUI. I worked on porting a camera/gallery baby app, which I had initially developed using Ionic and ReactJS ([baby-photo-gallery)](https://mckellar.wordpress.com/2022/03/25/baby-photo-gallery/).

It is worth noting that at the time of writing this blog entry, MAUI is still in the preview stage and approaching its final release. The version used for this project was Visual Studio 2022 Version 17.3 Preview 4, released on July 19th, 2022.

The main objective was to replicate the existing app, ensuring feature parity, while also familiarizing myself with MAUI. The app itself is a simple Baby Photo Gallery that includes the following features:

- Native Camera Access, Saving photos to device

- Side Menu/Flyout

- Photo List loading, Large data sets of photos, smooth scrolling

- View Photos/Favourite/Share

Overall I am impressed with MAUI built with .NET 6 you get access to features such as Dependency Injection, Async/Await, Observables, C#10 features global using statements and file scoped namespaces. The front end is built with XAML this was tricky to begin with learning the syntax but once you get the hang out of the layouts you can do everything without CSS

Comparison of the two:

<table ><tbody ><tr >
<td >**Ionic Framework v6.0 with ReactJs 17.0.2**
</td>
<td >**.NET MAUI 17.3 Preview 4**
</td></tr><tr >
<td >Highly Customisable UI, CSS, JS libraries
</td>
<td >MVVM decouples logic from the page making unit testable, source generators reduce binding code
</td></tr><tr >
<td >More ReactJs front end code
</td>
<td >Less Frontend code, more back end focused
</td></tr><tr >
<td >More portable as its written in JavaScript less risk of becoming outdated, ignoring Ionic code
</td>
<td >Lacking customisation compared to JS libraries, some controls lack customisation
</td></tr><tr >
<td >Image library needed for manipulation, have to generate images per platform
</td>
<td >Tightly coupled to .NET will need upgrading more often
</td></tr><tr >
<td >Fast to debug, run in browser
</td>
<td >Built in Image support, svg, auto sizing
</td></tr><tr >
<td >
</td>
<td >Slow to debug/launch via Emulator (still has some bugs), WSA missing some features didn't always start on demand
</td></tr><tr >
<td >
</td>
<td >Hot reload is great when it works
</td></tr><tr >
<td >5mb release package
</td>
<td >40mb release package lots of big DLLs
</td></tr><tr >
<td >13,417 devices supported
</td>
<td >1,708 devices supported
</td></tr></tbody></table>

**Preview Bugs**:  
The two main bugs that gave me the most headache:

Java.Lang.RuntimeException: 'Canvas: trying to use a recycled bitmap android.graphics.Bitmap@2e5b880'  
This error throws randomly when swapping pages with edited images, there is an active PR to resolve it

Toolbar icons not showing  
ToolbarItem.IconImageSource does not currently work with FontImageSource even though the code does not error

There are active PR for each so I hope they will be resolved in the next preview version

**Closing thoughts**  
.NET MAUI is clean modern and feels right at home working with .NET, I was pleasantly surprised at how easy and fun it is to work with, having ported over the app I will be going forwards with the MAUI version over the Ionic react, one simple reason, its less code, easier to maintain, develop, test. While the app is simple it would be interesting to see how you would recreate some of the more advanced JS controls libraries in MAUI I think it will be an effort from the community such as .NET MAUI Community Toolkit.

Below is a video of side by side apps running:  
Left is Ionic, Right is .NET MAUI

{% include video id="1FVq1Q9hp18" provider="youtube" %}

[![](/assets/images/2022/07/maui-home.jpg?w=491)](/assets/images/2022/07/maui-home.jpg)

[![](/assets/images/2022/07/maui-gallery.jpg?w=489)](/assets/images/2022/07/maui-gallery.jpg)

[![](/assets/images/2022/07/ionic-home.jpg?w=490)](/assets/images/2022/07/ionic-home.jpg)

[![](/assets/images/2022/07/ionic-gallery.jpg?w=491)](/assets/images/2022/07/ionic-gallery.jpg)

+++
title = "Write Once, Run Anywhere - Are We There Yet?"
author = "Claudiu Tomescu"
date = "2014-07-16"
categories = ["Mobile","Development","Xamarin"]
description = ""
linktitle = ""
featured = ""
featuredpath = ""
featuredalt = ""
type = "post"
draft = false
+++

For a number of years the software development industry has struggled to find a solution to a rather old idea: write once, run everywhere. First, there was Java, which for a little while seemed to be the answer, however for numerous reasons it didn’t live up to the dream. For a while it looked like everyone gave in, and the chase was off, however Microsoft released the .NET Framework and the game was on, once again. Soon after, a group of developers sponsored by Novell started project Mono, with the idea of porting the Microsoft .NET Framework to Linux (and implicitly other platforms such as OSX). This was the foundation Xamarin’s products (Xamarin iOS, Xamarin for Android, Xamarin for Mac) was built on. Fast forward to May 2014 and Xamarin just released Xamarin.Forms: a new technology for building cross-platform native mobile application using C# and .NET Framework. With Xamarin.Forms a developer can create mobile native applications for iOS, Android and Windows Phone (please note that you have to hold the appropriate developer licenses in order to create applications for all three platforms) Let’s take a closer look at how Xamarin.Forms delivers on the write once, run everywhere promise.

Before Xamarin.Forms, developers were writing application using shared business logic in the form of Portable Class Libraries (PCLs) and designing the user interface (UI) specific to each platform using either Xamarin.iOS (Xcode or Xamarin Studio’s built-in iOS designer) or Xamarin.Android tooling. Xamarin.Forms goes one step further enabling developers to share UI code as well; the developer uses Xamarin.Forms controls to create the UI, and the resulting applications render the UI using elements native to each platform. Further, the developer can further customize the UI using platform-specific Renderers, to create rich user experiences tailored to each platform.

As far as writing the shared UI code, the developer has two choices: create the user interface programmatically in code, or using XAML, which found its greatest utility in defining user interfaces within the Windows Presentation Foundation (WPF), Silverlight and Windows Runtime. Each approach has pros and cons, and ultimately it comes down to what you’re comfortable with. It’s worth mentioning though, that currently the major drawback to using XAML in Xamarin.Forms solutions is the lack of tooling, notably a designer similar to Visual Studio’s WPF designer or Blend. Also, please note that Xamarin.Forms solutions that include XAML must use a shared PCL project type, rather than the Shared Project type. Despite this the Xamarin.Forms is rapidly becoming a favourite choice among developers building mobile cross-platform applications; and given the great deal of support that Xamarin team gets from Microsoft, I have no doubt Xamarin platform is already well positioned to take the lead in this space.

While we’re talking about solutions to “write once, run everywhere” idea, it’s worth mentioning the availability, in the form of a developer preview, of Microsoft’s ASP.NET vNext, which exhibit the ability to run virtually on any platform: Windows, Linux, Mac. What that means, is that soon we’ll be able to run web applications build on .NET stack on any platform… But more on that on a future article.

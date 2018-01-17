+++
title = "Xamarin, PCLs, and iOS projects"
author = "Claudiu Tomescu"
date = "2013-12-03"
categories = ["Mobile","Xamarin"]
description = "Fixing PCL issues in Xamarin iOS projects"
linktitle = ""
featured = ""
featuredpath = "date"
featuredalt = ""
type = "post"
draft = false
+++

This posts is motivated by my personal struggle fixing PCL (Portable Class Libraries) project support in latest version of Xamarin Studio (4.2.1 stable).

I've been working for a while on a iOS project where some of the core components are built in a PCL project. Before the Xamarin Studio version 4.2.1 a hack was required in order to be able to correctly build and use PCL projects in iOS solutions using Xamarin Studio. This hack involved copying the PCL Microsoft reference assemblies into the /Library/Frameworks/Mono.framework/External/xbuild-frameworks/.NETPortable folder. This works okay, although this was a hack. On November 20, 2013 Xamarin announced full support for PCLs across the development environments. This meant that the hack that made things work before (for PCLs) no longer function. Starting with Xamarin Studio 4.2.1 if you try to open and compile a solution which includes PCLs referenced from iOS projects, there would be an error message compiling the PCL. Also, if one tries to create a PCL and reference it from an iOS project, the following error message would show in the Edit References dialog box `Incompatible target framework (.NET for Windows Store apps, .NET Framework 4)` The actual message depends on the Profile selected in the Project Options -> Build section.

After searching the Xamarin forums I've come across a post by Nicola Iarocci which was dealing with the same issue I was dealing with. The solution proposed by one of the respondents was a bit too radical for me, so I've posted a bug on the Xamarin bug tracking system. The solution offered there is much simpler and works very well. It basically involves removing any manually installed PCL assemblies by deleting the /Library/Frameworks/Mono.framework/External/xbuild-frameworks/.NETPortable folder; and installing the Mono MDK from http://www.go-mono.com/mono-downloads/download.html This will add proper PCL support into Xamarin Studio by adding Xamarin.Android and Xamarin.iOS profiles.
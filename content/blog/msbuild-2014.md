+++
title = "A glimpse into MS Build 2014"
author = "Claudiu Tomescu"
date = "2014-04-09"
categories = ["Conferences"]
description = "Thoughts after MS Build 2014"
linktitle = ""
featured = ""
featuredpath = "date"
featuredalt = ""
type = "post"
draft = false
+++

Build is Microsoft’s annual developer conference and is probably one of the biggest developers’ conference around; this year’s Build has been a truly remarkable one. Microsoft has made a ton of announcements and released a great deal of interesting updates and preview products. It really is a very exciting time to be a Microsoft .NET developer, and I personally am looking forward to building new cool applications with these technologies. So, without further due let’s take a look at the major things announced at Build 2014.

## Windows 8.1 & Windows Phone 8.1 Update
Reportedly Microsoft is working already on the next version of the Windows OS, unsurprisingly named Windows 9, which is slated for release sometime next year. In the meanwhile, the already recently released Windows 8.1 it’s receiving an update, along with a Windows Phone 8.1 update.

The Windows Phone 8.1 update brings Microsoft’s answer to Apple’s Siri and Google’s Google Now: the Windows Phone personal assistant Cortana. Although a late arrival in the smartphone space Microsoft seems to learn fast; Cortana inherits the best of Siri and Google Now. This service is backed by Microsoft Bing platform and it’s running in the Windows Azure cloud. Demos during the Build sessions were pretty impressive, and showcased a lot of new features to the mobile operating system in addition to Cortana. Microsoft also announced two new device partners and new Nokia phones: Lumia 930, 630 and 635.

The Windows 8.1 update is less impressive than the Windows Phone update, however it brings a lot of improvements in terms of usability for Windows 8.1’s mouse-and-keyboard users. One of the most interesting news about Windows 8.1 was availability of Windows 8.1 for every device 9” or less for $0. Obviously this is part of Microsoft’s plan to create a rich eco-system around Windows 8.1 and push the operating system to as many devices as possible. Which reminds me of the motto that put Microsoft on the map: “A computer on every desk, on every home, running Microsoft software”; the only difference is that now with the Internet of Things, Microsoft is targeting a lot more devices, and not only those running a flavor of Windows.

## Microsoft Roslyn
One of the big announcements during Build 2014 was open-sourcing of C# and VB.NET compilers under Project Roslyn. Live on stage Anders Hejlsberg made the Roslyn Codeplex repository public and available to anyone to play around with. Why is this important you may ask? Well, first all anyone can peek how a state of the art compiler such as C# and VB.NET compilers are built, but more importantly because anyone can now have access to intimate information about your code that only a compiler has. Tools such as FxCop or code analysis utilities can benefit most from Roslyn project; also new additions to the language itself can be made by anyone who wishes to contribute.

## Windows everywhere
Microsoft is introducing universal Windows apps, a special breed of applications that run on devices powered by Windows operating system ranging from phones to Xbox One consoles. Universal Windows apps are a new way for developers to build apps that run on phones, tablets, PCs and the Xbox One with as much code reuse as possible. The latest update to the Visual Studio 2013 (which has also announced during Build 2014) includes support for building universal Windows apps. Developers would start with a common source code base and tweak the application’s user interface for different screen factors. This is one step forward toward what seems to be Microsoft’s desire to enable developers to build apps that would run on all devices with Windows OS.

## Visual Studio Online
Another big announcement at Build 2014 was general availability for Visual Studio Online (VSO). Visual Studio Online has been in private beta testing for a while now, and Microsoft has finally released it to the general public. What exactly is VSO? VOS provides a lightweight, code focused development environment, running in the Azure cloud. It integrates nicely with source control systems such as TFS and Git, and as a complement of the desktop IDE it’s focused toward building Azure websites. VS Online  has a continuous integration feature available where you can schedule automatic deployments to Azure websites directly from your TFS or Git repository. VS Online is available to everyone, free (although with some limitations on the functionality) for teams up to 5 members.

## Visual Studio 2013 Update 2 RC
For Microsoft .NET developers VS updates are ubiquitous, so the VS 2013 Update 2 RC is not a biggie, however it’s worth noting some of the things that would make your life as a .NET developer more interesting.

Web Essentials for Visual Studio 2013 Update 2 RC - Mads Kristensen introduced the new and improved Web Essentials with tons of goodies such as new or improved editors for Saas, Less, Browser Link menu directly injected into the webpage, Markdown support, improved stylesheet support, and many more. Head to the official Web Essentials website (http://vswebessentials.com) for a complete list.
Integration with Microsoft Azure websites - ASP.NET project template creates direct creation of Azure websites, as well as artefacts such as PowerShell scripts for deployment, etc. Also, part of the new support for Azure websites is ability to remotely debug an Azure website directly from Visual Studio.
Universal Applications project template: allows creation of applications that run across all devices powered by Windows 8.1 OS.

## Microsoft Azure
Microsoft Azure news are probably the biggest thing at this year’s Build. In his Keynote the newly appointed EVP of Cloud and Enterprise group Scott Guthrie talked about no less than 44 announcements. Here is a list of most notable ones:

* A preview version of the new Azure Portal - brings together management, operations,  and development tools (VSO)
* Basic tier for compute instances - similar in CPU and memory with the Standard ones but cost roughly 26% less.
* General availability (GA) of Azure websites basic tier 
* Scheduler now generally available
* Read-Access geographically redundant storage now generally available
* Auto Scale now generally available
* Azure automation public preview now available


This is just a summary of the announcements at this year’s Build conference. If you are interested in details about any of the topics, please head to the [Channel 9](http://channel9.msdn.com/events/Build/2014) where you can find the complete list of sessions and the recordings available.
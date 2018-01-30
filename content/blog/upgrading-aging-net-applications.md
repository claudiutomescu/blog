+++
title = "Upgrading Aging .NET Applications"
author = "Claudiu Tomescu"
date = "2014-03-30"
categories = [".NET Transformation","Developmemt"]
description = ""
linktitle = ""
featured = ""
featuredpath = ""
featuredalt = ""
type = "post"
draft = false
+++

Upgrading a functional line of business application built on Microsoft .NET stack is considered a risk and/or unnecessary expense by some businesses, and for good reasons: as with any upgrade process this may introduce unexpected errors and bugs due to changes in the newer version of the .NET stack. That being said, here are some of the reasons why your business should strongly consider upgrading an aging application.

## Security fixes

Microsoft constantly updates the .NET framework to fix security issues discovered in previous versions; at the same time newer versions of the framework contain better implementations of the security features based on advances made in the cryptographic domain. If you decide to postpone an upgrade consider the fact that your line of business applications might be at risk, exposed to threats that may prove more costly down the road. To give you just an idea of sort of threats your applications are facing head to Microsoft’s Security Bulletin page [1] and browse the list of fixes released each month. You’re going to read about things like vulnerabilities in .NET Framework that allow elevation of privileges, execution of remote code, etc. If security of your and your client’s data is one of your top priorities - and it should be, then updating an aging application should be a must and not a nice to have item on your to-do list.

## Performance improvements

In order to respond to market demands for faster processing and increased runtime performance, almost every new version of Microsoft’s .NET Framework contains performance improvements; with each release of the .NET stack these improvements cover one or multiple areas of the framework: ASP.NET, mobile, etc.

For example the latest version of .NET Framework (4.5.1) contains among others the following improvements: better performance through background garbage collection for servers, background just-in-time (JIT) compilation, better performance when retrieving resources and improved performance for asynchronous operations. Choose not to upgrade and you’re already missing out on some of these performance enhancements. Perform the upgrade and your application automatically gains in performance, possibly saving you some planned budget for hardware upgrade.

## Vendor support

Microsoft stops support for older versions of the framework after a certain period of time, which leaves you alone and without support in case something happens. As an example, support for Microsoft .NET Framework 3.x prior to 3.5 Service Pack 1 ended on July 12th 2011 [2] If you are still running applications built against this or an earlier version of .NET framework you’re already out of support from Microsoft, and should consider an upgrade immediately.

## Operating system support

Microsoft’s Windows operating system is regularly updated to include performance and security improvements, which are especially important for servers running line of business applications. Newer versions of the .NET Framework are taking advantage of these low-level and architectural changes in the operating system to improve performance and security. Moreover, from version 3.5 Service Pack the .NET Framework is part of and tightly integrated with the operating system, increasing the performance and security. If you decide to continue run based on older versions of the framework, your applications are not fully taking advantage of the operating system and you’re not maximizing the investment made in upgrading your OS.

Another point to consider is the OS support for earlier versions of the .NET Framework. For example it’s possible to run applications built for versions 2.0 to 3.5 of the .NET Framework on Windows 8 or 8.1, however this requires special steps to enable/install .NET Framework 3.5. Microsoft recommends upgrading your applications to version 4.5 of the .NET framework which is included by default with Windows 8 OS.

## New features

This is a tricky one since in general taking advantage of new features requires code changes, which are more than a simple .NET framework upgrade. However, there are features that can be activated by the means of configuration files or with minimal code changes. These are worth evaluated and implemented if deemed so. As a simple example consider the support for new versions of browsers; this can be mitigated through the improved support included with the latest version of the ASP.NET framework. This is extremely important feature to have, as most browser vendors are on a fast-paced release cycle and some are automating the browser updates (Microsoft starting with IE10).

These are just a few of the reasons why newer versions of the .NET Framework should not be dismissed right away based on the popular belief “if works why change it?” At the same time a .NET Framework upgrade should be properly evaluated, planned and executed to ensure a successful and painless transition for your applications.

[1][microsoft security bulletin](http://technet.microsoft.com/en-us/security/dn481339)

[2][microsoft product lifecycle search]( http://support.microsoft.com/lifecycle/search/?sort=pn&alpha=.net+framework&wa=wsignin1.0)

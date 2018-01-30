+++
title = "How To Add EF Core To VS2017 projects"
author = "Claudiu Tomescu"
date = "2017-03-26"
categories = ["EF Core","Visual Studio"]
description = "EF Core issues in VS2017"
linktitle = ""
featured = ""
featuredpath = ""
featuredalt = ""
type = "post"
draft = false
+++

Visual Studio 2017 has been released a few weeks ago, so I'm tinkering with the .NET Core tooling in VS2017 as I'm following [Julie's Pluralsight course](https://app.pluralsight.com/library/courses/entity-framework-core-getting-started/table-of-contents) on EF Core. In doing so, I've come across a few things, which I though I would write a blog about, so that other may benefit from.

EF Core comes with command line tools that you can use outside Visual Studio. This is an alternative to the PowerShell commands you can use from VS's Package Manager's Console.

My solution consists of 2 .NET Core (.NET Standard Library) projects: SamuraiAppCore.Domain contains the domain classes, which are essentially plain C# classes, and SamuraiAppCode.Data which contains all the EF related code: context class, EF fluent configurations, etc.

I've already added the `Microsoft.EntityFrameworkCore.SqlServer` Nuget package to the SamuraiAppCore.Data project, and now in order to use the EF Core migrations, I need to add the `Microsoft.EntityFrameworkCore.Tools.DotNet` Nuget package. However, when I try to add it I'm getting an error in Visual Studio 2017:

`Package 'Microsoft.EntityFrameworkCore.Tools.DotNet 1.0.0' has a package type 'DotnetCliTools' that is not supported by project 'SamuraiAppCore.Data'`

![EFCore NuGet Error Message](https://nrz3xw.by3301.livefilestore.com/y4meC53cFs6nlxtYlSCQm91lmOvBPvPp9rqc3gcyb_uBcV08vpPAJsKFYUrCWP2gUnhAwWAApcPXvtqhDRO1bngu3f5uOd4ckNFG8w8gzfJjddzYPv5TOJSm1lmEDnhR6Pb77LwS6rkChziiIZU3JcK0xpVEwcdE1trBGE3TbG3HY8vyY4ggroy2PceR0Hid-rZ0wN2GlJh1zy0IPaUaedFiA?width=680&height=471&cropmode=none)

I've tried different options, by changing the project the project type, or even the target .NET Standard version, but I wasn't able to do get around this issue. The only way to solve it was to manually edit the SamuraiAppCore.Data.csproj file and add the required references:

![.csproj EF Tools References](https://nrbc6g.by3301.livefilestore.com/y4mNny_hJZv5S3EYaU3Mdlj5t4g8FdhbDTbQtxFw4Q4hp_mNx2kVzYsbRRhAEPlvT2KKI2GeYRApbly9yhPGx1gB3kux7rz5rS_Tghk-WF7yPEs8Us8RmoWp9jCzvvgbP2D6URXYTBohw9wIHYIlJ7jmcDl0NgPab8KMnpD_BS73FEeXZY7VFe55y01CbgRe4Y6l-sdCizyLZO5ze2Y1CoV9w?width=680&height=416&cropmode=none)

Now, if we open a terminal in the SamuraiAppCore.Data project folder and type dotnet ef command we get proper access to EF Core tooling:

![EFCore CLI working properly](https://nrbvow.by3301.livefilestore.com/y4mqU1CX9f5IO3BZ16kaaksJ29FycLMpKWjiYSmdNSiClsEa-rAA5Y1x9vUhB8vfYeShC_sy7S1Vwh65qHXwtyJTnCeNOeG2AvKbJYpzcCqSGGIBPJdYkxPF8R3oyKBu6sy7kSG-IF0CuqQqvy5-mYjg2-w2Wt_oWjzA3hJ6gOlCUFbEl6V_umrR0dTl96MS5xiKkrvRn64SNhSUSCRpdohmQ?width=680&height=458&cropmode=none)

I recommend you see [Julie's Pluralsight course](https://app.pluralsight.com/library/courses/entity-framework-core-getting-started/table-of-contents) on how to use EF Core migrations.

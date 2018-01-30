+++
title = "VS Code + Microsoft SQL Server on Linux"
author = "Claudiu Tomescu"
date = "2017-11-27"
categories = ["VS Code","Docker","MSSQL"]
description = "Getting started with MS SQL on Linux & VS Code"
linktitle = ""
featured = ""
featuredpath = ""
featuredalt = ""
type = "post"
draft = false
+++

This is the first article in a series I'm starting about using VS Code on Mac to work with MS SQL Server on Linux running in a Docker container.

First, if you don't have already Docker for Mac installed, go ahead and install it. At the time of writing this article I'm using Docker for Mac Community Edition verison 17.03.1-ce-rc1-mac3 (15924).

After installing Docker make sure you don't sign in using your Docker ID. If you do so, you are going to get an error when trying to pull the MS SQL server image:

`docker: Error response from daemon: Get https://registry-1.docker.io/v2/microsoft/mssql-server-linux/manifests/latest: unauthorized: incorrect username or password`

Make sure you configure your Docker with the minimum prerequisites for MS SQL Server for Linux. That is, a minimum of 4GB of RAM, and 4GB of disk space.

Next, you have to pull the MS SQL Server on Linux Docker image and start a container. You can do this in one step by attempting to start the container. Docker will automatically pull the image for you, if it doesn't exist locally.

In order to start up a MS SQL Server container I used the following command:

`docker run -v /Users/claudiu/Documents:/Documents -i -e ACCEPT_EULA=Y -e SA_PASSWORD=SaPa55w0rd -p 1433:1433 -d microsoft/mssql-server-linux`

As you can see I'm using a few Docker run options:

**-v** for VS Code to be able to access local files when talking to MS SQL Server

**-i** for interactive mode

**-e** to specify 2 environment variables required by MS SQL Server: ACCEPT_EULA and SA_PASSWORD

**-p** to specify the SQL Server port

**-d** to specify the Docker image to use to start up the container

If the container starts successfully you'll get a container ID similar to one in the screenshot below:

![Sample Docker Container ID](https://nry6lw.by3301.livefilestore.com/y4mV1dRT-cr2BDiecSfpa30-C_jkTMhjZdIVM_xmeRoOh6iEwLlIlYH96L21bKua_Vkh0WiCD5nGRyUhC8XlYLTH1a_Xf6HjpnINRPRxOeiTpbJDdHvGSkuijW4AvUom9XpaZwAkp4pVEppqHOPltsMOaybqS47J3QUOUUnVzaN4-NSbHh7uXlTY72A8w941BRAiEpu8_OzqCbAyxsr9WmZNg?width=680&height=26&cropmode=none)

Make sure you meet the complexity requirements for password, otherwise the container won't start. Also, make sure you're not using special characters in the password (I used $ in my password and I wasn't able to establish a connection to SQL Server instance)

Now, with the container started let's focus on VS Code. First, you need the [MSSQL extension for VS Code](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql)

With the extension installed, open the command palette and type:

`>MS SQL: Connect`

Follow the prompts to create a connection profile. Use 127.0.0.1 for the server name/IP. For username use sa with the password you specified when you started the Docker container.

If everything worked properly, you should see the connection info in VS Code status bar:

`127.0.0.1:master:sa`

Now you can try a simple T-SQL query in VS Code, for example something like:

`SELECT * FROM INFORMATION_SCHEMA.TABLES;`

You can see how you get the results in a nicely formatted grid, similar to MS SQL Server Management Studio on Windows:

![VSCode MSSQL SELECT results](https://mqefpg.by3301.livefilestore.com/y4m9I0FivxaljTvAvJfg-GHLvIYrTvBkU8PKX0U7-MeHUgzV746J8Atz5n018ZnlqPm-9fVdTLfHATYjd4vXxafbxV4yuOsclO5Me7sT7R_KcwqraOluk_0pVy_YAa18TYi4VKch-06v8KhcbbL2OL5hDrIjKQoALhGwVfq3A-Xx3uXJhAXtTa2t1LG6DKxcWdArwrHVWohIpYbkGhBchYsFQ?width=680&height=338&cropmode=none)

This is it! You now have a MS SQL Server instance running on your Mac, and VS Code configured to work with it. In the next articles we'll look at using .NET Core and EF Core to create a simple application which uses SQL Server on Linux as persistence store.

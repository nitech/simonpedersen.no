---
ID: 361
post_title: Configuring jspm with Github
author: nitech
post_excerpt: ""
layout: post
permalink: >
  http://simonpedersen.no/2015/06/23/configuring-jspm-with-github/
published: true
post_date: 2015-06-23 06:13:45
---
[jspm.io][1] is a *frictionless browser package manager*. If you haven't heard about package managers, they are nifty little tools that organize the packages your software is depending on. So instead of downloading the same favourite script package every time you need it, you can configure the project to depend on the script and then stay in sync with the latest version using `jspm install`. However, when downloading packages from github, there is a limit as to how many requests you can issue. You'll quickly get the message github rate limit reached. To fix this do: 
1.  Go to github.com, login and click `settings`
2.  Click `Personal access tokens` and then `Generate new token`
3.  Copy the token and start command line inside the project folder
4.  Type `jspm registry config github` During the config process, you will be asked to enter the token. Do so, and you're good to go. 

[<img class="alignnone size-full wp-image-362" src="http://simonpedersen.no/wp-content/uploads/2015/06/2015-06-23-08-00-03-C__Windows_System32_cmd.exe_.png" alt="2015-06-23 08-00-03 - C__Windows_System32_cmd.exe" width="677" height="187" />][2]

 [1]: http://jspm.io/
 [2]: http://simonpedersen.no/wp-content/uploads/2015/06/2015-06-23-08-00-03-C__Windows_System32_cmd.exe_.png
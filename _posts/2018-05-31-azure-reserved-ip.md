---
ID: 493
post_title: >
  Lesson learned when deploying a new
  Azure Classic Web Service
author: nitech
post_excerpt: ""
layout: post
permalink: >
  http://simonpedersen.no/2018/05/31/azure-reserved-ip/
published: true
post_date: 2018-05-31 06:13:29
---
For anyone else that might be experiencing difficulties assigning a reserved IP-address to a Microsoft Azure Classic Web Service, here are a few tips: 
## Why I didn't use deployment slots I was running a production service at azure, and wanted a staging server where I could - yea - stage the next version before pushing it into production. Azure has something called 

[deployment slots][1], which lets you deploy your site to different slots and then swap the slots whenever you're ready to publish. Azure Classic Web Services seem to have two slots: Production and Staging. I didn't end up using slots though. I could not find a good way to have the two slots share the same IP-address, which was what I needed at the time. 
## Why would I need a reserved IP-address? If you just publish an Azure Service, you'll get a public IP-address for sure, but you will not be guaranteed ownership forever. To mitigate the risk of losing your IP-address, you can create a reserved IP-address and assign it to the service. Here comes the recipe: (You can administer Azure from the web portal or via PowerShell, the latter being full fledged. In this case, however, I was able to do what I needed through the web portal) 

### 1\. Publish your site without a reserved IP-address Initially I tried creating an IP-address first - and then assigning it to my service. This didn't work. The error message was: 

<pre>Error: The Reserved IP TheNameOfYourReservedIpAddress does not exist. Http Status Code: BadRequest</pre> I think the reason was that I had assigned the IP-address to a custom resource group. When I later converted an existing IP-address to a reserved one, I noticed the resource group had been set to "Default Networking". Maybe my first attempt would have worked, had I assigned the new IP to that resource group. Anyway, I ended up first publishing the site - and thus getting a non-reserved IP-address. 

### 2\. Convert the IP-address to a reserved IP-address Using the PowerShell Command Line, I converted the IP-address of my service to a reserved IP address thus: 

<pre>New-AzureReservedIP –ReservedIPName TheNameOfYourReservedIpAddress –Location "West Europe" -ServiceName NameOfYourService</pre> If you haven't used PowerShell for Azure before, don't panick. I'd never used it before either. Just 

[watch the first few minutes of this introduction][2], and you'll be up and running in no time. 
### 3\. Edit your ServiceConfiguration-file (.cscfg) After this, I edited the <ServiceConfiguration> node of my ServiceConfiguration file and added the following chunk: 

<pre>&lt;NetworkConfiguration&gt;
&lt;AddressAssignments&gt;
&lt;ReservedIPs&gt;
&lt;ReservedIP name="TheNameOfYourReservedIpAddress" /&gt;
&lt;/ReservedIPs&gt;
&lt;/AddressAssignments&gt;
&lt;/NetworkConfiguration&gt;</pre>

### 4\. Republish When you now republish, the site will use the reserved IP-address. 

## Wrap up Did this help you? Great! Did it lead you astray? Not so great! If there are mistakes in the text, please tell me, so I can correct and perhaps help others :-)

 [1]: https://blogs.msdn.microsoft.com/mvpawardprogram/2017/05/16/deploy-app-azure-app-service/
 [2]: https://www.youtube.com/watch?v=3Q0jG1Doa-s
# Azure Cloud Models and Service Types

`Public Cloud Model`
Widely Used
All resources are owned, operated, and managed by a third party service provider like Azure.
Cheapest

`Private Cloud Model`
Extra Security
More Compliance Adhering
Financial Institutions, Goverment Agencies

`Private Cloud Infrastructure`
Dedicated Data Center or Dedicated Network

`Hybrid Cloud Model`
Combinatation of Public and Private

# Full Featured Services

`Software As A Service (Saas)`
They are web based applications that require a subscription
Azure Batch
Azure AI

`Platform as a Service (PaaS)`
Operating systems that are hosted and managed for you, on top of which you can develop apps and services.

# Azure Support Services

Azure App Services
Azure Search

`Infrastructure as a Service (Iaas)`
Computing, storage and networking services that are hosted and managed for you, on top of which you can install operating systems and store data.

`Summary`
Consume Software as a Service
Build on Platform as a Service
Host on Infrastructure as a Service

# Azure Subscription

Allows creating and hosting cloud native applications with Azure App Services or Migrate SQL Database to an Azure SQL Database and let complex scaling and updating for you.
Azure High Performance Computing is available for those that do a lot of Graphics processing.

`Event-Driven Architecture`
Has a serverless compute platform

# Azure Resource Group

`What is an Azure Resource Group?`
Resource groups are logical groupings of related resources.
Related resources can mean those that belong to a single application, resources that are shared within the same team or a number of any other groupings. Say you have an eCommerce platform that sells dessert T-shirts. Now imagine wanting to manage the Azure app service it runs on, the SQL server and database storing its data, and the Azure blob storage account hosting its media files, all in a single place.
By putting them all in the same resource group, you can do just that. Or what if your networking team needed a consolidated and separated way to access your organization's application gateways, firewalls and virtual networks.
Because we know each team wants ownership of their own resources, let's say your DBA's also required exclusive access to your organization's SQL server instances and databases. Setting up this kind of separation is simple with resource groups. That's the beauty of resource groups. You decide what those logical groupings are and what works for your team in applications.
Besides organizing resources, one of the best things about resource groups is that you can handle them as a group. When resources are no longer needed, you can get rid of them all in one fell swoop. Need to update all of your dev environment resources? As long as they're within the same resource group, you can update them all in one go. One thing to be mindful of though, is that resource groups can't share a resource.
Resources can only be assigned to a single resource group at a time. And it makes sense. I can't put these objects in two boxes at the same time.
It's the same with resource groups. Restricting resources in this way preserves the integrity of the resource group and truly keeps it isolated from other groups. As we touched on earlier, resource groups are also a great way to manage your users access to resources. The role-based access control for example, you can grant access to specific resource groups or specific resources themselves. My team likes to separate resources by environment and application. And we control access to production with roles. With resource groups, you can similarly configure your team's access to fit your organization's policies.
Finally, Azure resource groups also takes advantage of tagging, which can be a powerful way to work with resources. By tagging resource groups with meaningful context like environment, workload, or owner, you can make it easier to identify how you use your resources, separate cost by departments that incur them, and take advantage of automation opportunities when used with continuous integration and continuous deployment processes. No matter what kind of applications you build, resources you use, or strategy you implement to manage resources within your team, resource groups give you the flexibility to maintain them that makes sense to you.

# Azure Resource Manager (ARM)
`Using the Azure Resource Manager`
Creating more and more resources, it can get time consuming to manage them. Especially if you had to do that one resource at a time.
Even with the help of resource groups, we'll realistically deal with several versions of our applications, different environments, and other configurations that increase the number of resources we use.
Azure provides the Azure Resource Manager as a convenient way to deal with this in a reliable and scalable way. the Azure Resource Manager is a collection of rest API endpoints that are used to create, update, and delete resources. Each request is authenticated and authorized by the same management layer. This results in a consistent experience for you no matter which tool or service you use to interact with the Azure Resource Manager. Most importantly, the Azure Resource Manager plays a critical role in scaling your deployment processes.
Due to its significance to resource management and deployment, it even has its own templates which are abbreviated and nicknamed ARM templates. These are JSON files that you can use to state your resource needs as code. By using these templates, you can repeat deployments and get the same results each time. Common tasks done at scale, like deploying 300 Windows VMs with tags or creating several manage clusters with Azure Container Service, are also easier because of these templates. This is due to the declarative syntax use.

`Declaritive Syntax`
With declarative syntax comes the ability to validate our templates and, ultimately, our deployments. If our templates are invalid, we never have to worry as only templates passing validation ever go through with deployment. ARM will even take care of deploying resources in parallel, if possible. It will also deploy interdependent resources in the correct order. ARM templates are great for consistently deploying one or more resources to a resource group or subscription.
ARM templates are the preferred way of managing resources in a production environment. Note, there are many developers preferring to use the Azure CLI instead. The main reason, ARM templates can quickly become overly verbose, large, and difficult to maintain especially as resources increase or become more interdependent. When ARM templates are this long and complicated, it takes much longer to interpret and edit, making it more likely for us to introduce it to errors. Rewritten as an Azure CLI script, however, many of these ARM templates can be translated into much shorter, legible, and maintainable files, which translates into a better experience for us.
Since the Azure Resource Manager is essentially a restful API, we can use it in a few different ways. Through the Azure portal, with the Azure CLI, or with PowerShell. The Azure portal, as you may have already experienced, is the central hub for managing you applications and resources. Many guided wizards, step by steps instructions, and informational descriptions are in the portal, which help you become more familiar with each resource.
Because of this, it's also a great way to become familiar with the Azure Resource Manager, especially if you're just getting started.
It's also simpler to use when managing and understanding complex infrastructures and deployment processes.

`Portal`
When using the Azure Resource Manager through the portal, you'll see that resources are organized into resource groups and by Azure services. These distinctions make infrastructure management at the application level, or by service type, possible and much more intuitive. One caveat to keep in mind, though, is that the portal is usually last when it comes to feature parody. That means that any functionality initially released through the Azure Resource Manager's original API may not be fully represented in the portal. It can also take up to 180 days after the initial release for it to be supported. If this is a concern, the following options may be more ideal. Another way to interact with the Azure Resource Manager is through the command line using PowerShell. This is a great option if you're already familiar with PowerShell, primarily work in a Windows environment, or want the option to imperatively write deployment scripts. On the other hand, if you work with multiple platforms and require cross-platform tooling that works exactly the same on all platforms, the Azure CLI is the best way to use the Azure Resource Manager. If you can't decide between the Azure CLI and PowerShell, the Azure CLI generally has shorter commands that are easier to remember. For me, that seals the deal with the Azure CLI. As a final factor, the Azure CLI is also the fastest tool to use for prototyping and exploration. This makes it my favorite way to use the Azure Resource Manager. No matter which way you choose to use the Azure Resource Manager, you'll reap the benefits of managing your resources in a consistent and scalable manner. Check out this code sample to see how easy it is to deploy a database with the Azure CLI. Then, you can explore the rest of the commands in the Azure CLI reference.


# What is an Azure Region?
Azure offers 55 regions worldwide, spread across 140 different countries. These regions are key to scaling your applications to your users around the world, fulfilling different compliance or data residency standards, and helping your applications stay online, even during outages or disasters. Regions also define how resources are divided and billed in Azure. So it's worth noting that some regions can have different operating costs. 
`Paired Regions`
With Azure Regions, you could also take advantage of a strategy called paired regions, which are two Azure Regions that are contained within a specific geographic boundary. East Asia and Southeast Asia, West India and South India, and West US to and West Central US, are some of the regional pairs available, with many more around the globe. The only exception to this geographic rule is Brazil South, as it's regional pair, South Central US is outside of it's geography. 
`Automatic Replication`
By using paired regions, your applications can take advantage of many features to help keep them online. One of them is automatic replication, which means your apps get replicated into both regions. So if you happen to have an outage in one region, your apps will still be online thanks to the other region. Or if you need to do some scheduled maintenance, it is strategically executed on one region within a pair at a time. Meaning no, or very minimal downtime for your applications, at all. 
When choosing which regions to host your applications, it's important to consider the following. If you are replacing your on-premises infrastructure, a closer region would be better to reduce network latency. Alternatively, if you are keeping your on-premises infrastructure, choosing a father region can provide the geographic redundancy benefits you need at a much lower cost. Your companies data requires also play a large role in choosing a region. And there may be legal reasons to choose a particular region as well. 
Stricter companies usually prefer data to be closer to home, forbidding storage outside of their geographic region. As a general rule, US companies require data within the US. European companies require their data within Europe and so on. Following similar rules, government access policies also influence the regions to choose. When it comes to your customers, the common practice is to choose regions that are closest to them, which is a good practice to follow. But, if you have multiple locations or locations that span across the country, what then? In this case, targeting your largest customer base and choosing the closest region to that base is ideal. Another option is to choose an Azure Region that is in between your customers' physical locations to provide the same performance for each location. When you create resources in Azure, be sure to keep these practices in mind when selecting the Azure Region they will be hosted on. Regions can be changed later on, but depending on the resource, it can be a major hassle to do so. And by hassle I mean, you have to open a ticket with Azure Support to make the change. When you're planning your applications and services, check out the Azure geographies pages for more details on each specific region.

# What is an Azure Availability Zone
Azure Availability Zones are unique physical locations within an Azure region. Each zone is comprised of one or more data centers that have their own power, cooling, and networking. All regions have at least three separate Availability Zones enabled, which makes them more reliable in case one zone fails. Since Availability Zones are physically separated, applications and data shouldn't be affected by other data center failures in the region. 
Every Availability Zone combines the capabilities of both a fault domain and an update domain, which are just fancy names for server racks set up to do specific things. 
The difference between them is that "fault domains" are used in unexpected outages, like when a rack's power is lost. While "update domains" are used to purposely take down an instance of your app in order to perform maintenance or apply patches. 
If you create five Azure functions across five zones in an Azure region, your functions would be distributed across five fault and update domains. By understanding how your resources are distributed, Azure can make sure that updates or deployments don't happen to different zones at the same time. Zones also offer zonal services and zone-redundant services. Zonal services allow you to host specific resources in a specific zone. So, if your legacy apps, the ones running on VMs, happen to be used the most within West US Two region, you could assign those VMs to a specific zone within that region or to have granular control with your "Azure Kubernetes Service Cluster", you could also specify which zones they are allowed to be distributed on. 
`Zone-Redundant Services` 
Zone-Reduntant Services are what enables automatic replication of your applications and data across zones. For your SQL database backups and redundancies or replicating your Azure Redis caches across zones, this service is invaluable. When you combine Availability Zones with region pairs, you can rest easy knowing that your high-availability strategy is reinforced. 
With your applications and data replicated on different zones within a region, and further replication across your region pairs, you can be sure that your applications are always available, thanks to the large network of redundancies you've just created. Almost all service and region combinations support Availability Zones. The only exception is Azure Cosmos DB in the Japan East, France Central, and North Europe regions. It's actually pretty easy to take advantage of all the benefits Availability Zones offer you. To see for yourself, check out this quick tutorial on how to create a Linux VM in an Availability Zone with the Azure CLI.


# What is an Azure App Service?
An Azure App Service is an HTTP based service that allows you to build and host web applications, mobile backends, and RESTful APIs. 
Azure App Service has support for .NET, .NET Core, Node JS, Python, Ruby, Java, and PHP, so there's a high likelihood that you can develop in your favorite language. 
You can also run PowerShell scripts or other executables as background services. This is great for handling legacy applications or parts of your app that can't be migrated to Azure App Service immediately, and once you're ready to deploy you can do so on either Windows or Linux environments. By building and hosting your applications with Azure App Service you can take advantage of so many services within Azure to make them better. 
`Azure DevOps`
One of the best services to use with your Azure App Service is Azure DevOps. From your commits, using whichever source control platform you prefer, all the way to deployment, Azure DevOps can fully automate your continuous integration and continuous delivery processes. 
Using Azure DevOps also allows you to set up multiple environments like Dev, QA, and Staging, which can be used to promote features and fixes through a validated process. If security and compliance are concerns for your application which we all know can be quite cumbersome then don't worry. Azure App Services are conformed to ICO, SOC and PCI standards by default. You can also setup IP restrictions, configure subdomains, or create blacklists and whitelists, among other compliance focused requirements. And as an extra convenience Azure App Services integrates natively with Azure Active Directory so you don't have to re-write any authentication mechanisms from scratch. 
`Hosting`
When hosting your apps with Azure App Services you can manage scale through the Azure CLI or the Azure portal. You can scale up or out, depending on your needs. Scale up to increase your CPU usage, memory, or disk space. This is great for enhancing your existing infrastructure. By scaling up I can now play my favorite game on ultra high video settings without the game stuttering or crashing and by scaling up your application it can handle higher loads and result in a better, faster experience for your users. Scaling out, on the other hand increases the number of instances we have to work with. So instead of replacing our existing graphics card with a better one, in this strategy we combine multiple lower end graphics cards to work together to help us play our game at an acceptable rate. 
This strategy is common in big data processing where multiple machines are linked together to collectively provide processing power. Depending on your pricing tier you can scale out anywhere from 20 instances to 100 instances. You can even do so automatically using pre-defined rules that you set up. If you're lucky enough to work on the Greenfield, Azure App Services also makes it simple to create new applications. Azure has a vast library of quick start templates. Using one of those templates you can literally create and deploy a web app, an Azure function, a REST API, or one of many other common applications with a single click. This is my favorite part about using Azure App Services as it allows me to get up and running quickly, especially when I'm prototyping or experimenting with new features. As developers Azure App Services helps us offload the management scaling and monitoring of the applications we build. Which means we can focus more on the code. That's all we really want, right? 

# Creating An App Service To Host An API Using Azure Cloud Shell. 
Using the Azure Cloud Shell we can quickly create an Azure app service to host an API. 
Open the Azure Cloud Shell by clicking on its icon located on the top menu. 
`AppService Plan`
To host an Azure app service we first need to create a plan. 
We can do this by using the AZ app service plan create command. 
Type az appservice plan create

Next, we will need to add some parameters about our plan. 
First, will be the name so type "--dev-apps-api" 
Next, we'll need to assign it to a resource group so use the resource group parameter. That's --resource-group. 
Also, since this is a dev API I will also tie it to my dev resource group. 

Lastly, we'll need to use the --sku parameter which is the pricing tier. 
In this case, I just want to use the FREE tier since this will be a dev instance. Done. 

`Creating The Web App To Host The API`
Next, we'll need to create the web app itself. The one that's going to host the api. 
Type az webapp create and then specify the resource group which will be dev for me, the plan which is the name of the plan I just created. 
So for me that's dev-cakes-api. The name of the web app itself which will be cakes for all. 
Finally, add the deployment local git parameter so that we can use git to deploy our app. 
That'll be --deployment-local-git. Then press Enter. 
Once this command finishes successfully you should receive some JSON output. 
All that's left is to find the deployment local git URL. 
Go ahead and copy that URL and you'll be able to add it as a git remote where you can push your API.

# What is Azure Blob Storage?
At the heart of many applications, Azure Blob Storage gives you a place to store large amounts of readily accessible data in the cloud. 
`One of five Azure storage types, blob storage deals primarily with large, unstructured data.`
Think videos, images, audio, text or even virtual hard drives for VMs. 
We use blob storage quite a bit. When do I choose blob storage versus file storage. Both sound like the same thing and they're both Azure storage types. Well blob storage is better suited for streaming video and audio. It's also great for serving images or large documents directly to a browser. 
If you need to provide availability to your storage account anywhere in the world, but with an HTTPS connection, well you guessed it. Blob storage is the better option. Because it's optimized for storing massive amounts of unstructured data, blob storage is also the better option for backups, disaster recovery and archiving of data. As the final deciding factor, blob storage is usually cheaper than Azure File Storage. 
`On the other hand, Azure File Storage is the preferred option in two primary scenarios.`
If your solutions are already integrated with the native file system APIs, and you're just looking to migrate to the cloud without having to re-architect your entire data storage model, files is the best option. 
Since it supports the standard server message blob protocol, Azure Files allow you to migrate to any other platform that uses the same standard. 
`SMB Protocol`
The SMB protocol also allows you to mount Azure Files Storage as a native share on a VM. Something you can't do with blob storage. 
Files storage is also the better option for network file shares. Many companies have internal file shares that store documents and files for easy distribution among employees. My company uses an internal file share to store company logos, job description templates and employee handbooks, among other things. 
With Azure File Storage, you can mount a file share in the cloud to the same drive loader that your on-premise application uses and it would work seamlessly. In general, applications or humans, that need to share files would benefit the most with Azure files storage. 
If you decided on blob storage, the next thing you'll need to think about is how often you'll need to access that data and help perform what that process should be. 
`Tiers`
With blob storage, there's this concept of access tiers and performance tiers. These tiers determine your costs, how easily you'll be able to access your data, and how performant your data store will be. Access tiers come in three forms, Hot, Cool and Archive. 
If I were to guess, GIPHY stores all of the office GIFs in the Hot access tier, which is perfect for storing data that is accessed frequently and actively. The storage cost are higher than the Cool and Archive tiers but it also has the lowest access cost. In other words, data marked at this tier is the easiest and quickest to access from blob storage. 
The cool access tier is better for data that is not accessed as frequently but is still expected to be available when it is. Think old high school photos on social media or short term backups of your applications data. Because of the longer access time frames, storage costs are lower than the Hot tier. However data in the Cool tier is expected to remain there for at least 30 days. 
Finally there's the Archive access tier. As the name implies, this data access tier is best suited for long term data storage. Think original data sets, full application backups and compliance data that needs to be kept but rarely accessed. This has the lowest storage cost of the three tiers. But the highest access cost. AKA this data takes the longest to retrieve. For the most cost effective way to store your data, it's a good idea to organize it into the appropriate tiers when implementing blob storage. Once you've categorized your data into the right access tiers, the next option to consider is its performance tier. 
`Performance Tiers`
Blob storage offers two performance tiers, standard and premium. Both offer high capacity and high throughput on large amounts of data. And in most cases, the standard tier will be just fine. There are however, a few scenarios where the premium performance tier makes more sense. Premium performance is optimized for high-transaction rates and consistent low-latency storage. Applications that require a lot of interactivity, user feedback and quick responsive updates are better suited to utilize the premium performance tier. Use cases like a mapping tool where massive amounts of data need to be instantly available based on user feedback, IoT analytics where thousands of write operations can occur a second or AI and ML processes, where massive amounts of different data types need to be consumed and processed in a rapid time frame. These would all be ideal candidates for the premium performance tier. Check out the Azure storage introduction page to learn more about the other three storage types, Queue, Table and Disk. Understanding the differences will help you choose the right storage type for your app.

# What is Cosmos DB?
Azure Cosmos DB is Microsoft's globally distributed database service. It was created to accommodate the high responsiveness and always on nature of most modern applications that live in the cloud. Cosmos DB is considered a NoSQL database and primarily works with four data models. 
`Four Data Models`
Document Store
  Data is schema-less and most likely stored as json documents 
Graph Oriented Model
  Data is represented as graph structures like nodes and edges
Key Value Store
  Which is the simplest form of a database management system and only stores pairs of keys and values
Wide Column Store
  Allows data with vast numbers of dynamic columns to be stored
Because of Cosmos DB's focus on high availability, geographic distribution, and speed, it comes with some pretty neat advantages. To start, Cosmos DB is classified as a foundational service within Azure, which means it's available in every Azure region. And with a literal click of a region on a map, you can add additional regions to replicate your data to. This makes scaling in new regions super simple. 
Cosmos DB also automatically indexes your data. This was especially helpful for smaller teams, like my own, where the responsibilities of database administration were usually left to us as developers. For most teams, the indexing Cosmos DB provides is enough, but if finer grain tuning and maintenance are needed, Cosmos DB gives you the option to do so. Another cool feature is that Cosmos DB can scale storage and throughput independently, something that's not as easy to do on other database models. 
This is because Cosmos DB uses something called request units to manage its level of performance. You can think of request units as Cosmos DB's performance currency, one that you have explicit control over. If your application suddenly had the need to store an additional terabyte of new product SKU's for example, you could easily add additional storage without having to pay for additional throughput. And alternatively, if your throughput needed to increase during weekends as your traffic spikes during these times, you could scale up your request units to maintain acceptable throughput levels without having to purchase additional storage. 
Lastly, Cosmos DB supports many popular open source API's and access methods. These include the Cassandra, Mongo DB, and Gremlin API's. Now, if you're like me, you may be excited to hear about all of these highlights and are beginning to wonder how to start using it. One thing must be made clear though. 
`Cosmos DB is not an alternative or replacement for SQL server.` 
There are very rare exceptions where you'd ever migrate your existing SQL server database to Cosmos DB. The only cases that come to mind would be if you were storing enormous chunks of json in a SQL server database, and improperly while you're at it. Or, if you were trying to achieve the CM globally distributed high transaction rate architecture with SQL server. Even then, migration to Cosmos DB is probably not the right answer unless a full rewrite of your data model and architecture comes first. With that out of the way, let's look into why you'd choose Cosmos DB over SQL server. 
The first thing to be aware of is that Cosmos DB is solely based in the cloud, while SQL server is obviously not. 
If you're creating cloud-first, globally available applications, Cosmos DB might be the better option for you. Another significant factor to keep in mind is that Cosmos DB supports a SQL like language to query your data. At first glance, this seemed to be a non issue and worked out well. I mean, who wants to learn yet another language? However, while your normal selects, joins, and basic SQL queries will work, many complex ones will not. For example, you can use the order by clause as you normally would, but many baffling restrictions apply. Sorting on multiple attributes are not possible, sorting on aliases are not possible, nor is it possible to sort by a computed value or anything other than a field name. These kinds of restrictions span many other normal scenarios that we've come to expect from the SQL language, making it a pain point of Cosmos DB. One of the most important distinctions however, between Cosmos DB and SQL server, is their scaling options. 
With SQL server, data consistency and integrity are the top priorities, so in order to scale with these assurances, SQL server handles transactions sequentially and usually commits them to a single server. This acts as the source of truth, which can then be replicated to other regions. To handle higher throughput, you would scale out and add more CPU or memory to hopefully make things faster. This only goes so far though as the performance scans you get from scaling out, only apply to read only activities. Inserts, updates, and deletes are not affected by these performance gains. By contrast, Cosmos DB scales out by adding more regions and subsequently, more machines. And then, mirrors its structure geographically. 
Because of this architecture, every node connects at both reads and writes, which makes it much faster. However, this also means that no single database can reject a change because of a violated policy, order cannot be ensured, and rollbacks to a certain point in time, say before some issues started occurring, are difficult to do. Despite these features, Cosmos DB is still a great choice for a highly available and always online database. Check out Cosmos DB global distribution overview page to learn more about the benefits of a globally distributed data store.

# Using Azure SQL
As SQL Database and SQL Server have evolved over the years, so have their deployment options. With Azure SQL Database, the SQL databases and SQL server instances you know can now be hosted and managed completely in the cloud. By going cloud first on your databases, you get the same benefits as any other cloud-first resource you use, like easy scaling, global availability, or hands-off administration. 
The two primary ways Azure SQL can be used to fit your data needs. Each determine how much control you have over the infrastructure resources and the cost. 
  The first option is through hosted infrastructure. Here SQL Server runs on Azure VMs. With this approach you have greater control over the data base engine, since you have access to the infrastructure it runs on. This option is great if you need the ability to fully customize your SQL server instance. It's also great for existing applications that require a quick migration to the cloud with barely any changes. And it's the best option if you need custom development or test environments and don't want to buy additional on-premise hardware, which can get real expensive. 
  The alternative options are to use Azure SQL databases or managed SQL instances. With these options, you give all the database maintenance tasks, like applying patches or upgrading SQL Server versions, to Azure instead of doing them yourself. You also get to use the latest stable SQL Server features, as the hardware and software you use will be fully managed, owned, and hosted by Microsoft.
`Deployment Options`  
For Azure SQL databases, there are three deployment options to choose from. 

First, there's the single database, which has its own set of resources managed by a database server. Single-database deployments are built for cloud-native applications and even have hyperscale and serverless tiers. Hyperscale is a special service tier in Azure SQL Database that basically removes any of the practical limits set on normal cloud databases. With hyperscale database deployments, a hundred terabyte databases, minute-long restores, and almost instantaneous backups are all possible. Serverless, within the context of Azure SQL Database, is a compute tier that's build for serverless applications. It scales compute resources based on workload demand and even pauses the database when it's not active, just like serverless apps do. 
Second, there's the elastic pool, which is a collection of databases with a shared set of resources. This is also managed by a database server. Elastic pool deployments provide a more cost-effective way to deal with multiple databases that have different usage patterns. This includes single-database types.  
Finally, there's the database server itself, which is used to manage the groups of single databases and elastic pools you may have. As you start thinking about potential database migrations to the cloud, or creating new ones, check out the Feature Comparison page for Azure SQL Database to see the full list of differences and to find the ones that matter to you.
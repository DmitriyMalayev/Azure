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

`What is an Azure Resource Group?`
Resource groups are logical groupings of related resources. 
Related resources can mean those that belong to a single application, resources that are shared within the same team or a number of any other groupings. Say you have an eCommerce platform that sells dessert T-shirts. Now imagine wanting to manage the Azure app service it runs on, the SQL server and database storing its data, and the Azure blob storage account hosting its media files, all in a single place. 
By putting them all in the same resource group, you can do just that. Or what if your networking team needed a consolidated and separated way to access your organization's application gateways, firewalls and virtual networks. 
Because we know each team wants ownership of their own resources, let's say your DBA's also required exclusive access to your organization's SQL server instances and databases. Setting up this kind of separation is simple with resource groups. That's the beauty of resource groups. You decide what those logical groupings are and what works for your team in applications. 
Besides organizing resources, one of the best things about resource groups is that you can handle them as a group. When resources are no longer needed, you can get rid of them all in one fell swoop. Need to update all of your dev environment resources? As long as they're within the same resource group, you can update them all in one go. One thing to be mindful of though, is that resource groups can't share a resource. 
Resources can only be assigned to a single resource group at a time. And it makes sense. I can't put these objects in two boxes at the same time. 
It's the same with resource groups. Restricting resources in this way preserves the integrity of the resource group and truly keeps it isolated from other groups. As we touched on earlier, resource groups are also a great way to manage your users access to resources. The role-based access control for example, you can grant access to specific resource groups or specific resources themselves. My team likes to separate resources by environment and application. And we control access to production with roles. With resource groups, you can similarly configure your team's access to fit your organization's policies. 
Finally, Azure resource groups also takes advantage of tagging, which can be a powerful way to work with resources. By tagging resource groups with meaningful context like environment, workload, or owner, you can make it easier to identify how you use your resources, separate cost by departments that incur them, and take advantage of automation opportunities when used with continuous integration and continuous deployment processes. No matter what kind of applications you build, resources you use, or strategy you implement to manage resources within your team, resource groups give you the flexibility to maintain them that makes sense to you.

`Using the Azure Resource Manager`
Creating more and more resources, it can get time consuming to manage them. Especially if you had to do that one resource at a time. 
Even with the help of resource groups, we'll realistically deal with several versions of our applications, different environments, and other configurations that increase the number of resources we use. 
Azure provides the Azure Resource Manager as a convenient way to deal with this in a reliable and scalable way. the Azure Resource Manager is a collection of rest API endpoints that are used to create, update, and delete resources. Each request is authenticated and authorized by the same management layer. This results in a consistent experience for you no matter which tool or service you use to interact with the Azure Resource Manager. Most importantly, the Azure Resource Manager plays a critical role in scaling your deployment processes. 
Due to its significance to resource management and deployment, it even has its own templates which are abbreviated and nicknamed ARM templates. These are JSON files that you can use to state your resource needs as code. By using these templates, you can repeat deployments and get the same results each time. Common tasks done at scale, like deploying 300 Windows VMs with tags or creating several manage clusters with Azure Container Service, are also easier because of these templates. This is due to the declarative syntax use. 
`Declaritive Syntax`
With declarative syntax comes the ability to validate our templates and, ultimately, our deployments. And if our templates are invalid, we never have to worry as only templates passing validation ever go through with deployment. ARM will even take care of deploying resources in parallel, if possible. It will also deploy interdependent resources in the correct order. ARM templates are great for consistently deploying one or more resources to a resource group or subscription. 
ARM templates are the preferred way of managing resources in a production environment. It is worth noting, though, that there are many developers preferring to use the Azure CLI instead. The main reason, ARM templates can quickly become overly verbose, large, and difficult to maintain especially as resources increase or become more interdependent. When ARM templates are this long and complicated, it takes much longer to interpret and edit, making it more likely for us to introduce it to errors. Rewritten as an Azure CLI script, however, many of these ARM templates can be translated into much shorter, legible, and maintainable files, which translates into a better experience for us. 
Since the Azure Resource Manager is essentially a restful API, we can use it in a few different ways. Through the Azure portal, with the Azure CLI, or with PowerShell. The Azure portal, as you may have already experienced, is the central hub for managing you applications and resources. Many guided wizards, step by steps instructions, and informational descriptions are in the portal, which help you become more familiar with each resource. 
Because of this, it's also a great way to become familiar with the Azure Resource Manager, especially if you're just getting started. 
It's also simpler to use when managing and understanding complex infrastructures and deployment processes. 
`Portal`
When using the Azure Resource Manager through the portal, you'll see that resources are organized into resource groups and by Azure services. These distinctions make infrastructure management at the application level, or by service type, possible and much more intuitive. One caveat to keep in mind, though, is that the portal is usually last when it comes to feature parody. That means that any functionality initially released through the Azure Resource Manager's original API may not be fully represented in the portal. It can also take up to 180 days after the initial release for it to be supported. If this is a concern, the following options may be more ideal. Another way to interact with the Azure Resource Manager is through the command line using PowerShell. This is a great option if you're already familiar with PowerShell, primarily work in a Windows environment, or want the option to imperatively write deployment scripts. On the other hand, if you work with multiple platforms and require cross-platform tooling that works exactly the same on all platforms, the Azure CLI is the best way to use the Azure Resource Manager. If you can't decide between the Azure CLI and PowerShell, the Azure CLI generally has shorter commands that are easier to remember. For me, that seals the deal with the Azure CLI. As a final factor, the Azure CLI is also the fastest tool to use for prototyping and exploration. This makes it my favorite way to use the Azure Resource Manager. No matter which way you choose to use the Azure Resource Manager, you'll reap the benefits of managing your resources in a consistent and scalable manner. Check out this code sample to see how easy it is to deploy a database with the Azure CLI. Then, you can explore the rest of the commands in the Azure CLI reference.
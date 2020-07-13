# evolveLab

Deploying an ASP.NET web application to Azure App Service.

# Instructions for Visual Studio Code

## Prequisites

> ### 1 [Install Visual Studio Code](https://code.visualstudio.com/download)

> ### 2 Add the Azure Account Extension in VS Code

> ![](images/RackMultipart20200713-4-hutiz8_html_d7ba2fb5f3b689a2.png)

> [https://marketplace.visualstudio.com/items?itemName=ms-vscode.azure-account](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azure-account)

> ![](images/RackMultipart20200713-4-hutiz8_html_39eef746e40dd02d.png)

> [https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azureappservice](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azureappservice)

## Steps 
> ### I. Clone the evolveLab

>> If you have an existing local folder for your repos change to that folder, otherwise you can create the repo at the root of &quot;C:&quot;

>> Clone the evolveLab repo using the VS Code terminal (View, Terminal) the following URL

>> [https://github.com/1scscott/evolveLab.git](https://github.com/1scscott/evolveLab.git)

>> ![](images/RackMultipart20200713-4-hutiz8_html_b24391c61d0d67e8.png)

> ### II. Deploy the App Service from Infrastructure as Code

>> In the VS Code terminal, set the Azure Subscription context by running:

>>>**Select-AzSubscription -Subscription &quot;eea4815d-680b-4180-91f3-da0793ee5279&quot;**

>> Run the App Service Web App deployment template using the following command.

>>> **New-AzResourceGroupDeployment -ResourceGroupName &quot;rnb6138&quot; -TemplateFile .\ArmTemplates\azuredeploy.json**

>> Replace &quot;**myResourceGroup**&quot; parameter with your ¾ ID.

>> You may use any name for the deployment, in place of &quot;**mywebapp**&quot;

>>>![](images/RackMultipart20200713-4-hutiz8_html_b8ef2185de3d64c9.png)

>Once the command completes:

>>visit the [Azure Portal](https://portal.azure.com) to view your resources.

>>Click resource groups and filter by your ¾ ID  

> ### III. Compile the ASP .net Code
>> **Next run a build of the Dot Net version of the sample app to a folder named &quot;publish&quot; in the &quot;NetCoreSampleApp&quot; directory in the repo**

>>> dotnet publish –c Release –o ./publish

>>>![](images/RackMultipart20200713-4-hutiz8_html_2af7c41f31418e59_4.png)

> ### IV. Deploy the ASP .net Code

>> Once the build is complete, browse to the **./evolveLab/NetCoreSampleApp/publish** folder in the VS Code folder view. Right click the publish folder and choose &quot;Deploy to Web App&quot;

>>> ![](images/RackMultipart20200713-4-hutiz8_html_ccf3f15e74f60138.png)

>> Select subscription '[14203-788] Public Cloud Exploration'

>>> ![](images/RackMultipart20200713-4-hutiz8_html_ad03fcd3f1e9b479.png)

>> Select your webapp identified by the name you used in Step 2 above

>>>![](images/RackMultipart20200713-4-hutiz8_html_19101e7f1349b8d0.png)

>> Agree to the deployment

>>> ![](images/RackMultipart20200713-4-hutiz8_html_2af7c41f31418e59_1.png)

>> You may dismiss the Always deploy to web app message

>>> ![](images/RackMultipart20200713-4-hutiz8_html_2af7c41f31418e59_2.png)

>> Once the deployment completes you will see a message giving you the option to browse to the deployed sample app. Click the Browse Website button.

>>> ![](images/RackMultipart20200713-4-hutiz8_html_2af7c41f31418e59_3.png)

>> You should see the following page. Take note of the URL and copy it for use later. 

>>> ![](images/RackMultipart20200713-4-hutiz8_html_d0e8172fb37a1201.png)

> ### V Customize the web app code, build and deploy update

>> Open the Index.cshtml view file in the Views folder

>> Update the value for ViewData["Title"] to "Evolve Cloud Lab Home"

>> Save your changes

>>>![](images/RackMultipart20200713-4-hutiz8_html_616be628aa5eb00f.png)

>> Repeat the compile steps from Section 3 above after making the change to the index file.

>> Repeat the deploy steps from Section 4 to deploy and see the new code.

![](images/RackMultipart20200713-4-hutiz8_html_6edd387a4f942f54.png)

# Instructions for Visual Studio Code

(In progress)

## Prequisites

(In progress)

## Steps 

(In progress)

> ### I. Clone the evolveLab

Resources

[Publish an ASP.NET Web App to Azure App Service using Visual Studio Code](https://docs.microsoft.com/en-us/aspnet/core/tutorials/publish-to-azure-webapp-using-vscode?view=aspnetcore-3.1)

[Publish an ASP.NET Web App to Azure App Service using Visual Studio](https://docs.microsoft.com/en-US/visualstudio/deployment/quickstart-deploy-to-azure?view=vs-2019)

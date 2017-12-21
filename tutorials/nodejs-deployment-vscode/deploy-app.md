---
Order: 3
TOCTitle: Deploy the Application
PageTitle: Deploy the Application
MetaDescription: Node.js Deployment to Azure App Services with Visual Studio Code
DateApproved: 12/18/2017
---

# Deploy the Website

In this step, you will deploy your Node.js website using Visual Studio Code and
the Azure App Service extension. You will use the most basic deployment model
where your app is zipped and deployed to the Website.

# Deploy using the Azure App Service Extension

In the Azure App Service extension viewlet, click the blue up arrow icon to
deploy your app to Azure.

![Deploy to Web App](images/nodejs-deployment-vscode/deploy.png)

> **Tip:** You can also deploy from the command pallet, open the command pallet and type `deploy to web app`.

From here follow the prompts. Choose the directory that you currently have open,
`myExpressApp`; select your active Azure subscription; then choose "Create New
Web App".

![Create New Web App](images/nodejs-deployment-vscode/create-app.png)

Next, you'll give your app a **unique** name and set up a resource group and
App Service Plan. For this tutorial, we'll use the default names for the
resource group and plan to keep things simple and launch the app in `West US`.

Once created, your app will be accessible via
http://**unique-name**.azurewebsites.net. In this example, we'll call it
`practical-mustache`.

![Create and Deploy](images/nodejs-deployment-vscode/create.gif)

A "Resource Group" is essentially a named collection of all our application's
resources in Azure. For example, a Resource Group can contain a reference to a
website, a database, and an Azure function.

An "App Service Plan" defines the physical resources that will be used to host
our Website. In this walkthrough, we will use a **Basic** hosting plan on
**Linux** infrastructure, which means our site will be hosted on a Linux
machine alongside other websites. You can scale up and be the only site running
on a machine later in the Azure Portal.

Once created, you'll be prompted to deploy the app, choose yes.

![Deploy the App](images/nodejs-deployment-vscode/deploy-prompt.png)

The output window will open during deployment to indicate the status of the
operation. Once completed, find the app that you just created in the Azure App
Service explorer, right-click, and choose "Browse Website" to open the site in
your browser.

> **Tip:** You can deploy changes to this app by using the same process and choosing the existing app rather than creating a new one.

----

<a class="tutorial-next-btn" href="/tutorials/nodejs-deployment-vscode/tailing-logs">My site is on Azure</a> <a class="tutorial-feedback-btn" onclick="reportIssue('node-deployment-vscode', 'deploy-app')" href="javascript:void(0)">I ran into an issue</a>

## [Steps](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/sharepoint-framework-overview)

### **Step 1 :** Setup development enviromet

> Create an app catalog site

> Create a new site collection

> Install [Node.js LTS version 10](https://nodejs.org/download/release/v10.20.1/)

> Install development toolchain prerequisites

> - Install Gulp
> - Install Yeoman
> - Install Yeoman SharePoint generator

```bash
npm install gulp yo @microsoft/generator-sharepoint --global
```
> Trusting the self-signed developer certificate

```bash
gulp trust-dev-cert
```
### **Step 2 :** Create a new web part project
```bash
md helloworld-webpart
cd helloworld-webpart
yo @microsoft/sharepoint

```
1. When prompted:

    - **What is your solution name?**: helloworld-webpart
    - **Which baseline packages do you want to target for your component(s)?**: SharePoint Online only (latest)
    - **Where do you want to place the files?**: Use the current folder
    - **Do you want to allow the tenant admin the choice of being able to deploy the solution to all sites immediately without running any feature deployment or adding apps in sites?**: N
    - **Will the components in the solution require permissions to access web APIs that are unique and not shared with other components in the tenant?**: N
    - **Which type of client-side component to create?**: WebPart

1. The next set of prompts ask for specific information about your web part:

    - **What is your Web part name?**: HelloWorld
    - **What is your Web part description?**: HelloWorld description
    - **Which framework would you like to use?**: No JavaScript web framework

### **Step 3 :** Preview the web part
```bash
gulp serve
```

# CopilotStudio SAP
Getting started with Copilot Studio and SAP
## Create & configure a SAP Copilot in Microsoft Copilot Studio
## Prerequisites
### Power Platform Environment
> [!TIP]
> In a guided workshop, you will get these details from the instructor. If you are going through this exercise on your own, go to [Copilot Studio](https://www.microsoft.com/en-us/microsoft-copilot/microsoft-copilot-studio) and sign-up for a free trial

* Tenant: 
* Environment: 
* User: 
* Initial Password:


### SAP Environment 
> [!TIP]
> In a guided workshop, you will get these details from the instructor. If you are going through this exercise on your own, sign-up to the [SAP Gateway Demo System](https://developers.sap.com/tutorials/gateway-demo-signup..html) and create your own P-User to access demo SAP OData Services.
* SAP-User:
* SAP-Password:
* SAP OData Service URL: 

# Exercise 1: Sign in and create a copilot from a template
In this step, you will use the provided credentials to log into Microsoft Copilot Studio.

## Step 1: Setup your browser experience

To avoid conflicting with your existing logged-in experiences, you can do this workshop by using one of these 3 options:

1.	Set up a new work profile specific to that workshop 
2.	Or browse as a guest.
3.	Or start an InPrivate session.
![New Private Windows](images/NewInPrivateWindows.jpg)


## Step 2: Log into Copilot Studio
1.	Navigate to [aka.ms/CopilotStudioStart](https://aka.ms/CopilotStudioStart) 
2.	Enter the provided user name, click Next
![First Sign-In](images/FirstSignIn.jpg)

3.	Enter the provided password, click Sign in
4.	If prompted, choose whether to stay signed in.
5.	The first time you access Microsoft Copilot Studio, you’ll be prompted to choose your country/region. You can choose a value or leave the default option and click Get Started.

## Step 3: Create a copilot from template

1.	From the Microsoft Copilot Studio Home page, Explore Agents and click Website Q&A Copilot.
![SelectQ&A](images/WebsiteQA.jpg)
2.	You will get redirected to an experience to further customize your copilot before creating. To ensure uniqueness and avoiding conflicts with others in this environment, only update the default Name by suffixing your Initial and Last Name to the end (e.g. Website Q&A Copilot-hobruche)
3.	Click Create at the top right corner and wait a few minutes until the copilot is fully created noted by the Description and Instructions no longer showing Loading. 
![Create Agent](images/Create.jpg)

> [!Note]
> Sometimes the Copilot creation takes a little bit longer and you get a message to wait for an email, normally it comes back as created after few mins.

4.	Test your copilot by clicking some of the prompts like "What can you tell me about Copilot Studio".
![First Question](images/FirstQuestion.jpg)
5.	Congrats, you just created and deployed your first generative AI Website Q&A copilot!


# Exercise 2: Take a quick tour of the user interface
Microsoft Copilot Studio makes it easier for you to build basic to advanced Copilots. The following section reviews the main pages of the maker experience for Microsoft Copilot Studio.
## Main interface
![Copilot Studio Overview](images/CopilotStudioOverview.jpg)
A.	*Home* – Displays Microsoft Copilot Studio home page. This is the page where you initially landed. You can start creating new copilots from here, it contains the list of recent copilots, a list of templates to avoid creating new copilots from scratch, as well as learning resources. 
Create – This menu gets you to the conversational copilot creation experience.

*Agents/Copilots* – List of all the agents (f.k.a copilots) your user has access to in the environment.
Library – List of connectors available for the extension of Microsoft 1st-party copilots.

B.	*Agents/Copilots* – List of available agents/copilots that you can customize and quickly navigate to. 

> [!TIP]
> When you work on a single agent/copilot, you should unpin the list of agents to get more screen real estate for your authoring.

C.	*Menu* – Tabbed navigation between the most useful Copilot Studio capabilities.

*Overview* – Description of the copilot, its instructions, and quick view of its configuration (knowledge sources, topics, actions, publish status, etc.)

*Knowledge* – Where you manage the copilot knowledge sources (website, files, etc.)

*Topics* - Where you manage custom and system topics. Topics are the core building blocks of a copilot. Topics can be seen as the copilot competencies: they define how a conversation dialog plays out. Topics are discrete conversation paths that, when used together, allow for users to have a conversation that feels natural and flows appropriately.

*Actions* – Where you manage action. Actions are pieces of logic with inputs and outputs. They leverage Power Platform components such as connectors, Power Platform cloud flows, AI Builder custom prompts, or Bot Framework skills. Actions are useful to leverage generative AI to both prompt the user for the necessary inputs but also to summarize the output of the action in the desired format.

*Analytics* – Where you can view metrics to monitor how well your copilot is serving your users and identify ways to improve it.

*Channels* – Where you configure how your copilot is being made available to your users (e.g. Teams, website, etc.)

D.	*Overview* – Where you can edit the copilot description, its generative AI instructions, and also where you can have a quick view of its configuration (knowledge sources, topics, actions, publish status, etc.)

E.	*Environment* – Where you can identify the Power Platform environment you’re working from. You would typically create and author a copilot in a development environment and deploy it to test and production environments.

F.	*Publish* – Where you can make the latest version of your copilot available to your users. Apart from the test pane, changes are not reflected to your end-users as long as you have not published the copilot.

*Settings* – Where you can managed your copilot configuration (advanced settings, security, language, etc.)

G.	*Test your agent* – The test pane allows you to immediately test your agent/copilot and your customizations, even without needing to save.

## Settings interface
![Settings](images/Settings.jpg)
(1) *Agent details* – Where you can update the copilot display name, icon

(2) *Generative AI* – Where you can choose to replace the more classic natural language understanding approach for topic triggering and entity extraction with one that’s based on a large language model to do multi-intent detection and more complex entity extraction. This is also where you can configure content moderation setting for knowledge sources (to reduce risks of hallucinations).

(3) *Security* – Where you can share your copilot with other users (to co-author it) or with security groups (to use it). This is also where you configure end-user authentication settings (the type of authentication and whether it is enforced or not), and web channel security, that allows you to further secure the Direct Line channel that is used for any web or custom application deployment.

(4). *Authoring Canvas*: Enable Optimized Canvas for topics with a high number of nodes, improving performance and usability.

(5) *Entities* – Copilot Studio comes with a lot of pre-built entities to help identify key information in a user utterance (e.g. a city, date, number, etc.). This menu is also where you can define your own closed-list entities or regular expression entities.

(6) *Skills* – Where you register external Bot Framework skills that your Copilot Studio copilot can call, or where you can configure how existing Azure Service Bot can use your Copilot Studio copilot as a skill.

(7) *Voice*: Make sure your agent works for you with voice-first features like advanced speech recognition and dual-tone multi-frequency (DTMF) input

(8) *Languages* – Where you can configure additional languages your copilot can be used in and localized into.

(9) *Language understanding* – Where you can configure custom language models developed and trained on Azure AI Language, in Azure Conversational Language Understanding (CLU). When configured, this effectively replaces the out-of-the-box natural language understanding model (NLU) for intent detection, and can also replace entity detection and extraction.

(10) *Component collection*: Component collections can be used by multiple agents

(11) *Advanced*: To modify advanced settings (e.g. configure the Azure Application Insights integration, metadata or define solution)

## Exercise 3: Update instructions & knowledge sources
### Step 1: Change knowledge sources
Knowledge in Microsoft Copilot Studio allows you to add enterprise data from Power Platform, Dynamics 365 data, and external systems, so your copilots provide relevant information and insights for your end users. In addition, knowledge can be incorporated with [Generative answers](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-copilot-studio) in copilots. Published copilots that contain knowledge use the configured knowledge sources to ground the published copilot.

#### Supported knowledge sources
| Name | Source | Description | Number of inputs supported in general answers | Authentication |
| --- | --- | --- | --- | --- |
| Public Website | xxx | xxx | xxx | xxx |
| Documents | xxx | xxx | xxx | xxx |
| SharePoint | xxx | xxx | xxx | xxx |
| OneDrive for Business | xxx | xxx | xxx | xxx |
| Dataverse | xxx | xxx | xxx | xxx |
| Enterprise data via graph connections | xxx | xxx | xxx | xxx |

1. Navigate to the Knowledge tab of your copilot
![Knowledge Tab](images/Knowledge.jpg)
2. Select the 3 dot elipsis next to the existing Microsoft knowledge sources and choose Delete, once again confirming to delete when prompted. 
![Delete Knowledge Source](images/DeleteKS.jpg)
3. Click on *+ Add knowledge* 
![Add new knowledge](images/AddKnowledge.jpg)
4. Click on *Browse* 
![Browse for content](images/BrowseContent.jpg)
5. Select *Files*
![Select Files](images/SelectFiles.jpg)
6. Click on *Add*
![Add Files](images/ClickOnAdd.jpg)




### Step 2: Turn off the ability for copilot to use it’s own general knowledge
We would like to get answers from the defined knowledge based only
1. Go to the Overview pane and click on the Allow the AI to use its own general knowledge option
![Unable GenAI Content](images/UnableKnowledge.jpg)

2. Click continue in the Disabling the default AI knowledge warning
![Confirm](images/ConfirmDisable.jpg)

3. It should be now Disabled 

### Step 3: Test the changes
Let’s see how responses to general questions now behave with changes to instructions and public knowledge sources that align to the uploaded documents
1. Launch the Test pane
2. Ask a question that doesn’t match an existing topic to trigger the Conversational boosting topic.
3. Notice that it generates an answer and includes citations to ground its answer on and offer the user the option to navigate to the sources that were used to generate this answer.
4. Ask a follow-up question regarding policies and support
5. Ensure that the instructions are behaving correctly by not allowing the user to ask about another company’s products.

## Exercise 4: Create an action and review a topic
Microsoft Copilot Studio makes it easy to integrate with various 1st and 3rd party systems both generatively and directly via either the 1600+ out of the box Power Platform Connectors or embedded Power Automate Cloud flows in the form of configured actions. Topics allow for another level of prescribed flow and logic to control conversation paths further.

### Step 1: Create an trading lookup action
When you turn on generative mode, your copilot can automatically select the most appropriate action or topic, to respond to a user at runtime. In classic mode, a copilot can only use topics to respond to the user. However, you can still design your copilot to call actions explicitly from within topics.

Actions are based on one of the following core action types:

* Prebuilt connector action
* Custom connector action
* Power Automate cloud flow
* AI Builder prompts
* Bot Framework skill

Each core action has additional information that describes its purpose, allowing the copilot to use generative AI to generate questions. These questions are required to fill the inputs needed to perform the action. Therefore, you don't need to manually author question nodes to gather all inputs needed, such as the inputs on a flow. Inputs are handled for you during runtime.

Actions can generate a contextual response to a user's query, using the results of the action. Alternatively, you can explicitly author a response for the action.

In this first task, you manually create a new action by following these steps:
1. Select Actions 
2. Choose + Add an action
3. Scroll down and choose Create a new flow which will launch make.powerautomate.com
4. Rename your flow title, by clicking on upper left and renaming it to Get Tradingcontract <YOURNAME>.
5. Select on the Run a flow from Copilot trigger step and select to + Add an input
6. Select Text as the type and update the name to be TradingcontractNumber and description to be *Unique number for the trading contract of the new parameter*
7. Choose the + icon between the Run a flow from Copilot and Respond to Copilot and select to Add an action
8. Search for SAP, from the SAP OData connector select Read OData entity
9. Choose Add new connection, enter the details bellow and then click Create New
* Connection Name Tradingcontract<YOURNAME>
* Authentication Type: Anonymous
* OData Base URI through BTP: xxx
* API Name: from the pre-requisites step
* API Key: from the pre-requisites step

10. In the OData Entity Name choose zFD-Trading Contract
11. Since this OData service currently does not support *Get Details* we will add a query that allows us to filter for a specific trading contract

12. Choose Save draft and then Publish from the menu bar
13. Test the flow by choosing Test from the menu bar
Choose Manually as method to test the flow, click Test
Enter xxx as the TradingContractNumber and choose Run Flow
Click Done and you should see the successfully run. Select the Read OData entity action and look at the body
14. Copy the body by clicking the icon below
15. Click on the Edit button to edit the flow
16. Select the + sign between the Read OData entity and the Respond to Copilot action and add a Parse JSON action
17. In the Parse JSON action, select Use sample payload to generate schema and paste the body you copied from the run, select Done
18. In the Content parameter choose the body from the Read OData entity action. If you don’t see it choose See more to display all the parameters.
19. Select on the Respond to Copilot trigger step and select to + Add an output
20. Select Text as the type and update the name to be *TradingContractDetails*, for value select the lightening icon on right and select Body from the Parse JSON action which contains the SAP response in JSON format. In the description enter Contains trading contract details
Note: Make sure you choose the Body under the Parse JSON action.
21. Choose Save draft and then Publish from the menu bar 
22. Optionally you can test again the flow by choosing Test from the menu bar
Choose Manually as method to test the flow, click Test
Enter xxx as the TradingContractNumber and choose Run Flow
Click Done and you should see the successfully run. Select the Read OData entity action and look at the body
23. Click Back to go to the Flow overview page 
24. On the right side of the screen scroll down until you find the Run only Users and choose Edit. 
25. Choose your connection name and click OK in the warning:
26. Save
27. Go back to Copilot Studio and refresh the browser
28. Select to + Add an action again
29. Search on the flow you just created Get SAP Trading Contract <YOUR NAME> and select it
30. Select Next leaving the default Inputs and Outputs inherited from the flow.
31. Select Finish after all 3 steps have been completed

## Step 2: Review and disable the track order topic
Where you manage custom and system topics. Topics are the core building blocks of a copilot. Topics can be seen as the copilot competencies: they define how a conversation dialog plays out. Topics are discrete conversation paths that, when used together, allow for users to have a conversation that feels natural and flows appropriately.

In this case, though, we are actually going to disable the Track order topic and rely more heavily on generative AI to plan and summarize the right action. There are multiple advantages to this as well as some disadvantages.

1. Select Topics and then select Track order
2. Observe the types of nodes that came preconfigured as part of the template to surface order details in a programmatic and predictive way:

a. *Trigger Phrases* – utterances that would trigger this topic such as track order

b. *Question* – to capture information like order number and store in a variable response

c. *Action* – placeholder to query SAP order details using that captured order number either using a flow or connector action

d. *Set Variable* – to ultimately parse a JSON response into structured objects making data accessible for further processing

e. *Message (Adaptive Card)* – to post a small UX experience summarizing order data elements

3. Click on Topics again and choose to disable the Track order topic

## Step 3: Test looking up order details
Let’s see if you can lookup the status of an order directly from an SAP system now using this new action and extended topic.
1. Launch the Test pane
2. Ask a question to check on the status of an trading contract.
Ask other questions about some orders. Some other valid order numbers:
* xxx
* xx
* xx
* x
* ...
* xx

Sample Questions:

•	what's the overall trading contract xxx value?
•	Give me order details for order 0500000007

3. Observe the generative response on trading contract data retrieved from SAP real time


# Exercise 5: Publish your copilot to Teams
## Step 1: Validate authentication
There are 3 configurable means for copilots to authenticate:

* *No authentication* – publicly available in any channel and often used for external means
* *Authenticate with Microsoft* – Entra ID authentication in Teams and Power Apps often used for internal deployments using Microsoft 1rst party workloads
* *Authenticate manually* – used for either external means and/or authenticating with other 3rd party workloads

The Store Operations templates ships by default with Authenticate with Microsoft enabled to support seamless integration with Teams.

1. Go to Settings in the top-right navigation
2. Go to Security 
3. Select Authentication
4. Validate Authenticate with Microsoft is selected

## Step 2: Publish the copilot
Publishing is where you can make the latest version of your copilot available to your users. Apart from the test pane, changes are not reflected to your end-users as long as you have not published the copilot. Publishing is different than making the copilot available in a channel as seen in the next step.

We need to publish all the changes we have made from the default Store Operations template to this point.

1. Select Publish in the top-right navigation and confirm to publish

## Step 3: Configure Microsoft Teams publishing channel
Channels are where you configure how your copilot is being made available to your users (e.g. Teams, website, etc.). Multiple channels are available to support hosting your copilot experience. By default, the Stores Operations template ships with the Microsoft Teams channel to support a retail store employee’s experience. Depending on the tenant’s governance model, the Copilot Studio Maker will need to work with their Teams tenant administrator to make it available for the whole org to use.

1. Go to Channels in the top navigation
2. Select Microsoft Teams
3. Select Turn on Teams
4. Select Availability options
5. Select Copy link
6. Open another tab in the same browser session that you are currently logged in under, paste the link
7. Click to Cancel on the open application dialog
8. Select to Use the web app instead
9. Select Add

## Step 4: Test the experience in Teams
Test the experience from a retail store employee (e.g. C2) perspective in Teams by executing many of the same prompts used in previous lab steps.

1. Possible prompts to test:
* What deals are available today?	
* What is the policy on refunds?	
* What is the status of order 0500000007?	
* Does PlayStation have good deals right now?

Congratulations, you've now built and published your first copilot! 



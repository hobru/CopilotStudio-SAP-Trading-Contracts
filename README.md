# Copilot Studio & SAP - Trading Contracts
Getting started with Copilot Studio and SAP

This tutorial walks through two simple scenarios:
* Knowledge Grounding with documents you can upload
* Reading and interacting with data from an SAP system exposed via SAP OData. In this specific case we are leveraging a service that returns information about Trading Contracts

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

The easiest way to go through this workshop is to open up a browser in a Private window:


![New Private Windows](images/NewInPrivateWindows.jpg)


## Step 2: Log into Copilot Studio
1.	Navigate to [aka.ms/CopilotStudioStart](https://aka.ms/CopilotStudioStart) 
2.	Enter the provided user name, click Next
![First Sign-In](images/FirstSignIn.jpg)

3.	Enter the provided password, click Sign in
4.	If prompted, choose whether to stay signed in.
5.	The first time you access Microsoft Copilot Studio, you’ll be prompted to choose your country/region. You can choose a value or leave the default option and click Get Started.

## Step 3: Create a copilot from template

1.	From the Microsoft Copilot Studio Homepage, Explore Agents and click Website Q&A Copilot.
![SelectQ&A](images/WebsiteQA.jpg)
2.	Update the default Name by suffixing a unique name to the end (e.g. *Website Q&A Copilot-hobruche*)
3.	Click Create at the top right corner and wait a few minutes until the copilot is fully created noted by the Description and Instructions no longer showing Loading. 
![Create Agent](images/Create.jpg)

> [!Note]
> Sometimes the Copilot creation takes a little bit longer and you get a message to wait for an email, normally it comes back as created after few minutes. Feel free to check the emails in [Outlook](https://outlook.office.com/), messages in [Teams](https://teams.microsoft.com/go#) (in the browser) and [Power Automate](https://make.powerautomate.com/) which we will use later. 

4.	Test your Copilot by clicking some of the prompts like "What can you tell me about Copilot Studio".
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
| Public Website | External | Searches the query input on Bing, only returns results from provided websites | Generative mode: Unlimited Classic mode: Four public URLs (for example, microsoft.com) | None |
| Documents | Internal | Searches documents uploaded to Dataverse, returns results from the document contents | Generative mode: Unlimited Classic mode: Limited by the Dataverse file storage allocation | None |
| SharePoint | Internal | Connects to a SharePoint URL, uses GraphSearch to return results | Generative mode: Unlimited Classic mode: Four URLs per generative answers topic node | Agent user's Microsoft Entra ID authentication |
| Dataverse | Internal | Connects to the configured Dataverse environment and uses a retrieval-augmented generative technique in Dataverse to return results | Generative mode: Unlimited Classic mode: Two Dataverse knowledge sources (and up to 15 tables per knowledge source) | Agent user's Microsoft Entra ID authentication |
| Enterprise data via graph connections | Internal | Connects to Copilot connectors where your organization data is indexed by Microsoft Search | Generative mode: Unlimited Classic mode: Two per custom agent | Agent user's Microsoft Entra ID authentication |

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
2. Ask a question from the Document that you have uploaded, e.g. *Was sind die Hauptanbaugebiete von Naturkautschuk?*
![Second question](images/SecondQuestion.jpg)
> [!Note]
> Make sure that the Status of the uploaded document is actually "Ready"

3. Notice that it generates an answer and includes citations to ground its answer on and offer the user the option to navigate to the sources that were used to generate this answer.
4. Upload additional documents and ask further questions. 
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

1. Choose + Add an action
![Add an Action](images/AddAnAction.jpg)

2. Scroll down and choose *Create a new Power Automate* which will launch make.powerautomate.com
![New Power Automate Flow](images/NewPowerAutomateFlow.jpg)

4. Rename your flow title, by clicking on upper left and renaming it to *Get Tradingcontract-\<YOURNAME\>*.
![New Power Automate Flow](images/ChangeFlowname.jpg)

5. Choose the + icon between the Run a flow from Copilot and Respond to Copilot and select to Add an action
![Add New Action](images/AddNewAction.jpg)

8. Search for SAP, from the SAP OData connector select Query OData entity
![Query SAP OData](images/QueryOData.jpg)

> [!TIP]
> If required, click on *Change Connection Reference* and *Add New*
> ![Change Connection Reference](images/ChangeConnectionReference.jpg)
> ![Add new](images/AddNew.jpg)

9. Choose Add new connection, enter the details bellow and then click Create New

|Property|Value|
|---|---|
|Connection Name|Tradingcontract-\<YOURNAME\>|
|Authentication Type|Anonymous|
|OData Base URI through Azure APIM|https://api.integration-ninjas.co.in/adventas/graph/api/s4hadv/my.s4/|
|API Name|API-Key|
|API Key|will be handed out|

![Create Connection](images/CreateConnection.jpg)

10. In the OData Entity Name choose zFD-Trading Contract
![Select Entity](images/Selectzp_gtcf_FrameContract.jpg)

> [!TIP]
> Since this OData service currently does not support *Get Details* and also does not contain hundreds of contracts, we will just query the full list. 

12. Choose Save draft and then Publish from the menu bar
![Save and Publish](images/SaveAndPublish.jpg)

13. Test the flow by choosing Test from the menu bar
![Select manually](images/TestFlow-Manually.jpg)

14. Choose Manually as method to test the flow, click Test
![Select manually](images/TestFlow-Manually.jpg)
![Run Test Flow](images/RunTestFlow.jpg)

> [!TIP]
> If it doesn't work and the wheel keeps spinning, just click on Cancel and try again. 


15. Click Done and you should see the successfully run. Select the Read OData entity action and look at the body
![Click on Done](images/DoneFlow.jpg)

16. Look at the body and click on the Edit button to edit the flow
![Edit the Flow](images/CopyBody.jpg)


17. Select on the Respond to Copilot trigger step and select to + Add an output
![Add an Output](images/AddAnOutput.jpg)

18. Select Text as the type 
![Select Text](images/SelectText.jpg)

19. and update the name to be *TradingContractDetails*. 
For the value select the lightening icon on right and select Body from the *Query OData entities*. 
In the description enter "Retrieve a list of trading contracts and their status from the SAP system"
![Enter Parameter Name](images/EnterParameterName.jpg)



20. Choose Save draft and then Publish from the menu bar 
![Enter Description, Save as Draft and Publish](images/DescriptionDraftPublish.jpg)

21. Optionally you can test again the flow by choosing Test from the menu bar
Choose Manually as method to test the flow, click Test
Click Done and you should see the successfully run. Select the Read OData entity action and look at the body

22. Click Back to go to the Flow overview page 
![Click on Back](images/ClickOnBack.jpg)


23. On the right side of the screen scroll down until you find the Run only Users and choose Edit. 
![Edit Run Only Users](images/RunOnlyUsersEdit.jpg)

24. Choose your connection name and click OK in the warning. Then click on Save
![Select Connection and Save](images/SelectOKSave.jpg)


25. Go back to Copilot Studio and Click on Refresh
![Click on Refresh](images/ClickOnRefresh.jpg)

> [!TIP]
> If your Flow does not show up, then cancel and perform the following steps again:
> Select to + Add an action again


26. Search on the flow you just created *Get Tradingcontract-<YOUR NAME>* and select it
![Select the new flow](images/SelectTheNewFlow.jpg)

27. Leave the Name as is, but add the following text to the *Description for the agent to know when to use this action*. Then click on *Add Action*


Description for the agent to know then to use this action:
```text
This action retrieves a list of trading contracts and their status from the SAP system. As a results of this query you get an array of multiple trading documents. For each trading document, you get the Trading Document number, the Document item, the trading document type, the products, the trading document item text, the product group, the plant, the trading sales quantity, the unit and the Open Sales Quantities and the creation date. Each element looks like this:
{
  "TradingDocument": "3110000000",
  "TradingDocumentItem": "10",
  "createCalloff_ac": true,
  "TradingDocumentType": "ZS11",
  "Product": "2224",
  "TrdgDocItemText": "Glycol",
  "ProductGroup": "L001",
  "Plant": "DE01",
  "CreatedByUser": "PLANGNER",
  "CreationDate": {
    "Year": 2024,
    "Month": 2,
    "Day": 6
  },
  "CreationTime": {
    "Hours": 5,
    "Minutes": 53,
    "Seconds": 10,
    "Milliseconds": 0,
    "Ticks": 211900000000
  },
  "TrdgDocSalesQuantity": 240,
  "TrdgDocSlsQuantityUnit": "MT",
  "OpenSalesQuantity": 0
}
```
![Add Description](images/AddDescription.jpg)

> [!TIP]
> Creating the a good description is important. Via this description Copilot Studio decides which action to call when a user asks a questions.

28. Select Next leaving the default Inputs and Outputs inherited from the flow. Select Finish after all 3 steps have been completed

29. Once the Action is successfully added, click on the 
![Enable Generative AI](images/GenerativeAI.jpg)

30. Select *Generative (Preview)*, click on *Save* and close the Setting screen.
![Enable Generative](images/EnableAI.jpg)






## Step 3: Test looking up trading contracts
Let’s see if you can query some information about trading contracts. 
1. Launch the Test pane
![Toggle Test Pane](images/SelectTestPane.jpg)

2. Ask a question to check how many trading contracts are in the system: ````
How many trading contracts do we have in the system?````
![How many trading contracts](images/HowManyTrading.jpg)

> [!TIP]
> Notice how the bug screen shows you what action or triggers have been executed. 

3. Test with other questions:

* ````how many trading contracts do we have in our system?````
* ````what's the overall trading contract value?````
* ````Give me details on trading contract 3110000001````

> [!TIP]
> Since we did not specify the description of the knowledge source, this can lead to confusion. Either optimise the description or -- for this test -- delete the added content
 > ![Remove knoweldge source](images/RemoveKnowledgeSource.jpg)

3. Observe the generative response on trading contract data retrieved from SAP real time


# Exercise 5: Publish your copilot to Teams
## Step 1: Validate authentication
There are 3 configurable means for copilots to authenticate:

* *No authentication* – publicly available in any channel and often used for external means
* *Authenticate with Microsoft* – Entra ID authentication in Teams and Power Apps often used for internal deployments using Microsoft 1rst party workloads
* *Authenticate manually* – used for either external means and/or authenticating with other 3rd party workloads

1. Go to Settings in the top-right navigation
![Go to Settings](images/GoToSettings.jpg)

2. Go to Security -> Authentication
![Go to Settings](images/Security-Authentication.jpg)

3. Validate Authenticate with Microsoft is selected
![Authenticate with Microsoft](images/AutheWithMSFT.jpg)

## Step 2: Publish the copilot
Publishing is where you can make the latest version of your copilot available to your users. Apart from the test pane, changes are not reflected to your end-users as long as you have not published the copilot. Publishing is different than making the copilot available in a channel as seen in the next step.

We need to publish all the changes we have made from the default Store Operations template to this point.

1. Select Publish in the top-right navigation and confirm to publish
![Publish Copilot](images/Publish.jpg)

## Step 3: Configure Microsoft Teams publishing channel
Channels are where you configure how your copilot is being made available to your users (e.g. Teams, website, etc.). Multiple channels are available to support hosting your copilot experience. By default, this template ships with the Microsoft Teams channel. Depending on the tenant’s governance model, the Copilot Studio Maker will need to work with their Teams tenant administrator to make it available for the whole org to use.

1. Go to Channels in the top navigation and select Microsoft Teams
![Select Teams](images/Channels-Teams.jpg)


3. Select Turn on Teams
![Turn on Teams](images/TurnOnTeams.jpg)

4. Select Availability options
![Availabilty Options](images/AvailabilityOptions.jpg)

5. Select Copy link
![Copy Link](images/CopyLink.jpg)

6. Open another tab in the same browser session that you are currently logged in under, paste the link

> [!TIP]
> You might need to manually select "Use the web app instead"
9. Select Add

10. Now you can interact with the agent directly from Teams
![Agent in Teams](images/Inteams.jpg)

Congratulations, you've now built and published your first copilot! 

# Exercise 6: Test the same with other SAP OData Services
The SAP ES5 System provides an easy access to SAP OData services. Get a P-User and test the service using this URL: https://sapes5.sapdevcenter.com/sap/opu/odata/iwbep/GWSAMPLE_BASIC/

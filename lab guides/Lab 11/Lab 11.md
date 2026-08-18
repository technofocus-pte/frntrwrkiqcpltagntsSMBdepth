> **Lab 8 - Create an agent in Copilot Studio with Dataverse MCP
> Server**
>
> Create and configure a Copilot Agent in Copilot Studio with Dataverse
> MCP Server integration to streamline business workflows.
>
> After completing this lab, participants will be able to create and
> configure a Copilot Agent in Copilot Studio, integrate the Dataverse
> MCP Server to read and update account information from the Account and
> Contact table, structure agent responses for clarity and business
> value, and apply these skills to solve common business challenges.
>
> **Task 1: Create and Configure Copilot Agent**
>
> Build a Copilot Agent that connects to Dataverse through the MCP
> Server for seamless data access.
>
> In this section, you’ll learn how to create a new Copilot Agent in
> Copilot Studio, configure it with proper instructions and suggested
> prompts, and integrate the Dataverse MCP Server for live data
> connectivity

1.  Open a browser and navigate to
    +++[<u>https://admin.powerplatform.microsoft.com/+++</u>](https://admin.powerplatform.microsoft.com/+++).
    Select **Manage** from the left pane and then select the **Tenant
    Settings** option.

2.  Select **Manage** -\> **Environments** -\> **User1** environment.

3.  Select **Settings** from the top menu bar.

4.  Select **Product** -\> **Features**.

5.  Scroll down to the **Dataverse Model Context Protocol** section and
    select the checkbox against **Allow MCP clients to interact with
    Dataverse MCP Server (Preview version)** and select **Save**.

> <img src="media/81b0d387b2e0beff9d6713c728b8bb54a34beb1f.png"
> style="width:6.27116in;height:3.83353in" />

6.  Back in the Copilot Studio, select Home page.

> <img src="media/54ce62088a5db68d61595db92d0a9a541bf973f9.png"
> style="width:6.5in;height:3.38542in" />

7.  Select **Create an agent** tile to create a new agent.

> <img src="media/32c4ad8de839022cb2c20aab6bf7d3f306eb6cb6.png"
> style="width:6.5in;height:3.28125in" />

8.  Once the agent is provisioned, select Edit against the **Details**
    pane.

> <img src="media/1c9ad2f9bb854ddb58e241d2b84cd240038e477d.png"
> style="width:6.5in;height:3.94792in" />

9.  Enter the below details and select **Save**.

    1.  Name - +++Zava Agent+++

    2.  Description - +++This agent will help Contoso sales reps update
        their accounts and contacts using the Dataverse MCP Server+++

> <img src="media/7bc3a81c5a74d10fb7d25ed8d21edbc9047c3eea.png"
> style="width:6.39616in;height:4.95859in" />

10. **Edit** Instructions and enter the below set of instructions and
    select **Save**.

> This agent will: Read accounts and contact information from the
> Account  
> and Contact Tables in Dataverse using the Dataverse MCP Server.
> Update  
> accounts and contact information from the Account and Contact Tables
> in  
> Dataverse using the Dataverse MCP Server. Create new accounts and  
> contact information in the Account and Opportunity Tables in
> Dataverse  
> using the Dataverse MCP Server. Do not use outside knowledge. Only
> use  
> the Dataverse MCP Tool to create, read, update and delete.
>
> <img src="media/b7e0ddc603d9e0dc3a5dcf9047211503eca4e006.png"
> style="width:6.5in;height:5.0625in" />
>
> <img src="media/b0bb69f48826f9736aa59e590652e59d3e1eb11c.png"
> style="width:6.5in;height:4.92708in" />

11. Select **+ Add knowledge** to add a knowledge source. Browse and
    choose **Account data.xlsx** from C:\LabFiles and seelct **Add to
    agent**.

> <img src="media/83ad05d5243b6b6f442e42b0a32fc78d339e7e29.png"
> style="width:6.5in;height:4.40625in" />
>
> <img src="media/ad83cfd6289966fa7a22778770da5a71e3cd76f1.png"
> style="width:6.5in;height:4.23958in" />

12. Scroll down and select **+ Add suggested prompts** in the Suggested
    prompts section.

> <img src="media/bd6f05d8e207d8d6779bcc34d88e49d8ce9c0903.png"
> style="width:6.25032in;height:4.91692in" />

13. Add the following prompts and then click **Save**.

    1.  **Title**: +++Account Search+++ **Prompt**: +++List all accounts
        in Redmond+++

    2.  **Title**: +++Contact Search+++ **Prompt**: +++List all contacts
        from Coho Winery+++

> <img src="media/21c5b894b2c662c3714696f7bc5daa6761b1a369.png"
> style="width:6.5in;height:4.4375in" />

14. Select **+ Add tool** from the Tools section.

> <img src="media/0bbfb92ee84da47f9c73b5cf613af395c10839a5.png"
> style="width:6.417in;height:5.06276in" />

15. Select the **Model Context Protocol** tab, search for +++Microsoft
    Dataverse MCP Server (Preview)+++ and select **Microsoft Dataverse
    MCP Server (Preview)**.

> <img src="media/1b4a817b69ec04d05f4c7b031318bb4e0368dcec.png"
> style="width:6.5in;height:3.80208in" />

16. Create new connection if prompted and then select **Add and
    configure**.

> <img src="media/5f0472793dcb3ab1b24b98a185a10ec514ee93d8.png"
> style="width:6.5in;height:3.78125in" />
>
> <img src="media/5c3df26273081b46b1b446796e1e2c0f153b0549.png"
> style="width:6.5in;height:3.875in" />
>
> <img src="media/21324a1dc28cef333db08f37269a770f467f1fe5.png"
> style="width:6.5in;height:3.83333in" />
>
> **Note:** The Dataverse MCP Server will allow you natural language
> access to your tables in Dataverse. We have sample data in the
> Accounts and Contacts tables that we will use. The tools available
> are: list tables, describe table, read data, create record, update
> record, list prompts, execute prompt, list knowledge sources, and
> retrieve knowledge

17. Review the tools available for the Dataverse MCP Server. You can
    select and deselect which tools are available to the agent. When the
    tool is executed, the list is dynamically updated from the MCP
    Server. You cannot call an MCP Server from a Topic for this reason.

> <img src="media/e235b3600e688e7e4bef7155c4019481198e110b.png"
> style="width:6.5in;height:4.79167in" />

18. Ensure that the **knowledge source** you had added earlier is in the
    **Ready** state. Open the **Test** pane and enter +++Upload data to
    Accounts table using the Account data tracker+++

> <img src="media/22f89e86a5063fa7eba14e5eda7401849b71fc69.png"
> style="width:3.9377in;height:5.02109in" />

19. For the first run, you would get a Consent dialog as by default the
    tool is configured to use “End user credentials”. Please click
    **Allow** to continue.

> <img src="media/be93a432a1edbdb877e7bb8d36fa14d1142637f6.png"
> style="width:3.99326in;height:4.97942in" />

20. If the knowledge source takes a very long time to get to the Ready
    state, copy few rows from the tracker and send it in the Test pane
    to be added to he Account table.

> <img src="media/16691c88d8cfdb5af11b5864bfdadd017772e0b9.png"
> style="width:4.14605in;height:4.49329in" />

21. Now, enter +++List the accounts in the state of WA+++ in the
    **Test** pane and click **Send**.

> <img src="media/b38d8781506b0730474dfa47e926f3c6e24e8ad9.png"
> style="width:3.70158in;height:4.24327in" />

22. See the series of actions that take place and the output from the
    MCP server.

> <img src="media/4a3425ea800e3e378d8edcbebb963bea0f29657e.png"
> style="width:4.37523in;height:5.68779in" />
>
> <img src="media/f7ee1aaf20ec384ee4b0cad893077c7d7c9350b9.png"
> style="width:6.5in;height:3.5in" />
>
> **Task 2: Structure Agent Responses with Custom Prompts**
>
> Create custom prompts to ensure consistent, structured responses from
> your agent that provide business-relevant information.

1.  To have a more structured response, you can create a **prompt** in
    the **Tools**. In the **Tools** tab, click **+ Add a tool** then,
    select **Prompt**.

> <img src="media/ecbaeca7a8ebb811901d668c456ef3d60f961ea3.png"
> style="width:6.5in;height:3.02083in" />
>
> <img src="media/28d6d2e7a69a9e77be901fd9080ac6fc4517bece.png"
> style="width:6.5in;height:3.69792in" />

2.  Rename the **prompt** **name** at the top to +++Show Account
    Details+++ .

> Then in the **instructions** enter, +++Find account which contains+++
> and then click **+ Add content** to pass in the name of the account we
> are searching for. Select **Text** for the Input and call it
> +++**Account Name**+++ . Click **close**.
>
> <img src="media/bdf6e2fcbacc7f7316f96ac2271746de723ef02e.png"
> style="width:6.5in;height:2.85417in" />
>
> <img src="media/442d5181702c796fc25c47e8a939991bff3c6ab9.png"
> style="width:6.5in;height:3.78125in" />

3.  We can now grab specific fields from Dataverse to show to our end
    users in the chat. Click back in the instructions and enter +++and
    find relevant details like:+++ click **+ Add content**. This time we
    will select **Dataverse** and some of the fields in the **Account**
    table which we feel our end users would like to see about the
    account.

> <img src="media/801f4ed7fd453a3fa428ab5e6aa11c049e6bc45c.png"
> style="width:6.5in;height:3.1875in" />

4.  Let’s select the following by clicking on the dropdown: **Account
    Name**, **Account Number**, **Address 1**, **Annual Revenue**,
    **Email** and **Main Phone**. Click **Add** and then **Save**.

> <img src="media/96d6685bb51137edd1dc806e119f9ddb1a4ef0a4.png"
> style="width:6.5in;height:3.22917in" />
>
> <img src="media/fdb314cd2fb911d3182a9c5882786ac53c6d4ef2.png"
> style="width:6.5in;height:3.44792in" />
>
> <img src="media/de61db213e1cb939de7880d8c4e99c27593fbd8e.png"
> style="width:6.5in;height:3.1875in" />

5.  Select **Add and configure**.

> <img src="media/1de3ada604feb487a14e9110834034900e1e004f.png"
> style="width:6.5in;height:4.17708in" />

6.  Now we can test out our prompt. Let’s go back over to our agent and
    test again. Go to the test pane.

7.  Enter +++Show account Details for Northwind Traders+++ and click
    **Send**. You can see that the response is in the structured
    response with the custom prompt created.

> <img src="media/b6eedf434b818336ebce47c89555aac47d2fd176.png"
> style="width:4.34745in;height:4.85442in" />
>
> **Summary**
>
> In this lab, you built a Copilot Agent in Microsoft Copilot Studio
> that integrates with the **Dataverse MCP Server** to securely access
> and manage business data using natural language. You configured the
> agent to read, create, and update records across Dataverse tables such
> as **Accounts, Contacts, and Opportunities**, without relying on
> external knowledge or custom APIs.
>
> You also learnt how to **structure agent responses** using custom
> prompts, ensuring consistent, business-friendly outputs that surface
> the most relevant data fields for end users. Now, you can design an
> agent that streamlines sales and account management workflows,
> delivers clear and structured insights, and demonstrates how
> MCP-powered agents can solve real-world business challenges with live
> enterprise data.

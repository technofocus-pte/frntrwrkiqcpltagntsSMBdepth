# **Lab 12 - Build an autonomous financial data retrieval agent with Computer-Using Agents (CUA)**

> **Introduction**
>
> Legacy systems without APIs create major roadblocks for automation.
> Traditional RPA often relies on fragile screen-scraping or manual
> workarounds, which slow down decision-making, increase errors, and
> reduce productivity. This lab introduces Microsoft Copilot Studio and
> Computer Using Agents (CUA) as a smarter solution. By simulating human
> interaction with internal systems, CUAs can securely access and
> process data - without needing API integration. You’ll learn to build
> an autonomous agent that delivers faster responses, reduces manual
> workload, and enables real-time, informed decisions.
>
> Objective
>
> In this lab, you’ll learn how to build an autonomous agent using
> Microsoft Copilot Studio. This agent will simulate human interaction
> with a legacy internal system to retrieve financial portfolio data
> without requiring direct API access.

## **Task 0: Create an environment in the United States Region**

> In this task, you will check the region where your Dev One environment
> was created. If it is not in the United States, then you will create
> an environment in the United States region since the Computer-Using
> Agents is not available in all the regions by default. You will use
> the newly created environment for this lab alone.

1.  From a browser, open the **Copilot Studio** portal -
    +++[<u>https://copilotstudio.microsoft.com+++</u>](https://copilotstudio.microsoft.com+++/)
    and select Get Started in the trial activation dialog.

> <img src="media/9df51d40e5637b6a5ec4850735e2ed5226ea16e9.png"
> style="width:6.26042in;height:3.88542in" />

2.  Once the **Copilot Studio** opens, it will take a few minutes for
    the environment updates to reflect in the **Power Platform** admin
    center.

3.  After few mins, in a new tab, open
    +++[<u>https://admin.powerplatform.microsoft.com/+++</u>](https://admin.powerplatform.microsoft.com/+++).
    Select **Manage** from the left pane and then select the environment
    that starts with **User1**.

> <img src="media/9e082a693b488118cad01d340fda0071cf1091b8.png"
> style="width:6.26042in;height:3.28125in" />

4.  Check the **Region** of the environment. If it is **United States**,
    please start with the **Task 1: Create and Configure an Autonomous
    Agent**. Else, please execute the remaining steps of this **Task
    0**.

> <img src="media/003f31c6a243689ed57c226d59152acd16c77dfd.png"
> style="width:4.97248in;height:4.97942in" />

5.  From the **Environments** page, select **+ New**.

> <img src="media/70407fdb7ea1bab56eed67fc1f88a4bb7f79634d.png"
> style="width:6.26042in;height:3.91667in" />

6.  Enter the below details and select **Next**.

    1.  Name - +++CUA+++

    2.  Region - United States - Default

    3.  Type - Developer

> <img src="media/1c3c7b6e09429f8be9a771e652891ff16d599824.png"
> style="width:2.5418in;height:5.04193in" />

7.  Select **Save** in the next screen.

> <img src="media/9a623363eb337cb5021d35f75e7fb5a9c38f9945.png"
> style="width:2.51402in;height:5.04193in" />

## **Task 1: Create and Configure an Autonomous Agent**

> In this task, you will create a new autonomous agent in Microsoft
> Copilot Studio, configure its identity, and set up an email trigger
> using the Microsoft 365 Outlook connector.
>
> To automate portfolio lookups, the agent must be able to detect
> incoming email requests and initiate the appropriate automation flow
> based on subject line filtering.

2.  In the Copilot Studio page, Select the **User1** or **CUA** (if you
    have created it in the last Task) environment from the top right.

> <img src="media/5c0b46ce72f7ce48ebf8160b9cfced8514270ec0.png"
> style="width:6.26042in;height:3.30208in" />

3.  Select **Create an agent**.

> <img src="media/3069d911a270a59485b87783b122bd9654bfbb59.png"
> style="width:6.26042in;height:3.27083in" />

4.  Once the agent is created, select **Edit** against the **Details**.

> <img src="media/03b228b3272d74315f3b284316201aa1f986fad4.png"
> style="width:6.26042in;height:4.375in" />

5.  Enter the Name as +++Portfolio Lookup Agent+++ and select Save to
    rename the default name of the agent.

> <img src="media/c013656d1ee25082a4cdfd72099dd490e2403a3e.png"
> style="width:6.26042in;height:4.35417in" />

6.  Scroll down to the triggers section and click **+Add trigger**.

> <img src="media/9c1ed520db9127e642e6b8d0b54c3d1d63ef664c.png"
> style="width:6.26042in;height:4.82292in" />

7.  Search and select **When a new email arrives (V3) (Office 365
    Outlook** and click on **Next**.

> <img src="media/98492d289737b4a5ffdf98dc8814acf6af1f1d62.png"
> style="width:6.26042in;height:3.97917in" />

8.  Rename the trigger to +++When a portfolio lookup email arrives+++,
    ensure that the connection is established for Copilot Studio and
    Outlook and then click on **Next**.

> <img src="media/8716c217e9d65f0845b9e4e44eed8d86dc1e4626.png"
> style="width:6.26042in;height:3.9375in" />

9.  In the **Subject Filter (Optional)** field, enter +++Portfolio+++ in
    the subject line.

> <img src="media/62276b6b7fcc0ffa4153da711ced8d9e621fd7a1.png"
> style="width:6.26042in;height:4.125in" />

10. Once the trigger is created, you can **Close** the Time to test your
    trigger dialog.

> <img src="media/05db9dd6a2de6bf0bf7f14ea57835e2dfa7b5a59.png"
> style="width:6.26042in;height:3.78125in" />

## **Task 2: Add Computer Use tool**

> In this task, you will configure a Computer use tool that logs into a
> computer, navigates through a website, searches and retrieves
> financial portfolio data. Then use the Office 365 Outlook connector to
> reply with the requested data.

1.  Navigate to **Tools** in the top-level menu.

> <img src="media/581b26b65f68c5a6283d3ebbbcd901e54ce8ab88.png"
> style="width:6.26042in;height:3.16667in" />

2.  Select **+ Add a tool.**

> <img src="media/a1b616126ea542718939cde72368e27d1c7d80e5.png"
> style="width:6.26042in;height:4.09375in" />

3.  Select **+ New tool**.

> <img src="media/9afb7c1d292b86f6c7819237771a72e6bbcf9e4e.png"
> style="width:6.26042in;height:3.77083in" />

4.  Select **Computer use (preview)**.

> <img src="media/2b6078f899c06adbb95c1daf1a472d29259dde80.png"
> style="width:6.26042in;height:3.96875in" />

5.  Add the following Instructions, and then select **Add and
    configure**.

> 1\. Go to
> <https://computerusedemos.blob.core.windows.net/web/Portfolio/index.html>.  
>   
> 2. Enter the Portfolio ID in the "Enter Portfolio ID" search field and
> click on the "Search" button.  
>   
> 3. Retrieve the "Client Name", "Portfolio Value" and "Manager" values
> exactly as shown.  
>   
> 4. Return those three values as the final output. If no portfolio data
> is found, reply that you couldn't find a portfolio with the specified
> ID.
>
> <img src="media/958ede832329bcee86ca633540259e8ca3a7d88b.png"
> style="width:6.26042in;height:4.02083in" />

6.  Update the **Name** of the Computer use tool as +++Look up portfolio
    data+++

7.  Update the **Description** as +++Search and retrieve financial
    portfolio data+++

> <img src="media/5cbeadc7cf990df6fe4bd046c67edb14e1158405.png"
> style="width:6.26042in;height:3.16667in" />

8.  In the Inputs section select **+ Add input**.

> <img src="media/d56b8eb46b92010bd71f1892c1d4eaaee8070d04.png"
> style="width:6.26042in;height:3.55208in" />

9.  Enter name as +++Portfolio ID+++ and description +++The ID of the
    portfolio+++ and select **Done**.

> <img src="media/605451aaf9c4f2ea917894900ec63cec9f4392ad.png"
> style="width:6.02114in;height:3.45851in" />

10. Select **Save**.

> <img src="media/4d6a4aaf8c13bb47c0a448a8f11287990de0cdc6.png"
> style="width:6.26042in;height:2.57292in" />

## **Task 3: Test the Computer use tool**

1.  In the **Instructions** section, select the **Test** button on the
    right.

> <img src="media/466bc6391a22c0d3bc9aaf80b9b472cdd0bbf16d.png"
> style="width:6.26042in;height:3.11458in" />

2.  Add the sample value +++44123BCD+++ and select **Test now**.

> <img src="media/2b2b107b92f9e3c415b96065a9cda2157add1e6f.png"
> style="width:6.26042in;height:3.375in" />

3.  Observe the Computer use tool logging into the computer and
    performing the requested actions:

    1.  The left panel shows your instructions and a step-by-step log of
        the tool’s reasoning and actions.

    2.  The right panel shows a preview of the actions on the machine
        you set up for computer use.

> <img src="media/9a1b202c7aef1eabd8a4df62a59039565d459700.png"
> style="width:6.26042in;height:3.61458in" />
>
> <img src="media/dfba9d84e2541650b463bf6dfa1eaba2d60d513d.png"
> style="width:6.26042in;height:2.85417in" />
>
> <img src="media/820f101d94a25465ea6509c02632867aba110a56.png"
> style="width:6.26042in;height:2.85417in" />
>
> <img src="media/455b6732f5ad103674eadfe1ccfc168e83f7c97d.png"
> style="width:6.26042in;height:2.82292in" />
>
> <img src="media/0882b195fef30dbab508056fc47587e9483fa582.png"
> style="width:6.26042in;height:2.85417in" />
>
> <img src="media/d90099a38da61e8836bd6ee03b3de509c8f94fa8.png"
> style="width:6.26042in;height:2.83333in" />

4.  Select **Finish testing**.

> <img src="media/2a12a06fcf9a9f75ad80ebf9ed34aa512d0ef1c6.png"
> style="width:6.26042in;height:2.78125in" />

## **Task 4: Setting up email response capabilities**

> In this task, you will set up the email capability.

1.  Return to the **Tools** tab and select **+ Add a tool** .

> <img src="media/be4122e94c57af2d5e061f1c92249e654fac7a0a.png"
> style="width:6.26042in;height:2.30208in" />

2.  Search for +++**Send an email (V2) (Office 365 Outlook)**+++ and
    select it.

> <img src="media/7937c5c8b48448bcfdc6220e05e8a5c145891a12.png"
> style="width:6.26042in;height:3.77083in" />

3.  Select **Add and configure**.

> <img src="media/6489798f9b0f85b74197eaf50fb0b82397cfda15.png"
> style="width:6.26042in;height:3.82292in" />

4.  Update its **Name** to +++Reply to email+++ and **Description** to,
    +++Use this operation to reply to the email received+++ and then
    select **Additional details**.

> <img src="media/4ad07c15b7a1e8d4d57a7463c9f3183a3aa5b226.png"
> style="width:6.26042in;height:3.21875in" />

5.  Under **Additional details**, set **Credentials to use** to
    **Maker-provided credentials.**

> <img src="media/d2b0559f93b1ab6443b45fab18ab217de711b64b.png"
> style="width:6.26042in;height:3.73958in" />

6.  Under the **Inputs** section, click on **customize** against the
    **To** input and set its **Description** to +++Use the "from" email
    of the triggering received email+++.

> <img src="media/22a66ad00ff1df1d2f6e2a5b174e71978061b48b.png"
> style="width:6.26042in;height:4.1875in" />
>
> <img src="media/51b72adfb03f5c4ae8a259cb1215d775956b4971.png"
> style="width:6.26042in;height:3.375in" />

7.  **Customize** the **Subject** input and set its **Description** to
    +++Write the email subject+++.

> <img src="media/f83ead93728b6927bca081ff5d707d3ac55635e0.png"
> style="width:6.26042in;height:4.625in" />

8.  Customize the **Body** input and set its **Description** to +++Write
    the email body using HTML and highlight the requested data+++.

> <img src="media/f1c00040f71c8860d5e98121b3d2c24c5ffbdda1.png"
> style="width:6.26042in;height:3.40625in" />

9.  Click **Save** to finalize the tool configuration.

> <img src="media/4fbfd70c118f399ea9d1aa840d01e36b8f02099d.png"
> style="width:6.26042in;height:3.07292in" />

10. Navigate to **Overview** tab and then **Edit** the Instructions.

> <img src="media/80bb1161e8c0deff3dab17ada1095ddde718452e.png"
> style="width:6.26042in;height:3.45833in" />

11. Paste the following instruction.

> When a financial portfolio related request is received, identify the
> Portfolio ID and search for the requested data using \< Look up
> portfolio data \>. Once you have gathered the financial portfolio
> information, use the \< Reply to email \> tool to reply to the
> original email you received. Do not respond with data beyond what was
> requested.
>
> <img src="media/3c7739d5dc04df828fe87911145b88e9fd3aa880.png"
> style="width:6.26042in;height:4.76042in" />

12. Select \< Look up portfolio data \>, enter / and select the **tool**
    **Look up portfolio data**.

> <img src="media/c1cad91e408a06b29bf0d635f3b5be2db5088f8b.png"
> style="width:6.02114in;height:5.00026in" />
>
> <img src="media/6f258765ae3547bdb796dfd909c43831f86072e0.png"
> style="width:5.9517in;height:4.95859in" />

13. Similarly, replace \< Reply to email \> with the **tool**, **Reply
    to email**.

14. Once the replacements are done, as in the screenshot below, select
    **Save**.

> <img src="media/c3385c2cb3066b719929e0e15c79c84210b2319e.png"
> style="width:6.12531in;height:4.95859in" />

15. Select **Settings** from the top right.

> <img src="media/b0b79dd88fc385f7f8a782ac75401e74320ae146.png"
> style="width:6.26042in;height:3.44792in" />

16. **Disable** **Use general knowledge option** under the **Knowledge**
    section, and select **Save**.

> <img src="media/12d859720722214701c9669129eecc9a03a9fc98.png"
> style="width:6.26042in;height:4.22917in" />

17. Close the **Settings** pane.

> <img src="media/00ff3a7adc4da14efd3e2ec9d100310299fe0c17.png"
> style="width:6.26042in;height:3.1875in" />

## **Task 5: Testing your complete agent**

> In this agent, you will test the complete working of the agent that
> you have created.

1.  Send a test email from an email address of your preference to your
    training user’s email account with

> Subject: +++Portfolio data request+++
>
> Body:
>
> Hi!  
> I hope you're doing well!  
> I'm looking for the portfolio manager and value of portfolio
> \#44123BCD. Much appreciated.  
>   
> Thanks!
>
> <img src="media/4764e01d718e39dce03432a9c7391bbac90e9c57.png"
> style="width:6.26042in;height:2.6875in" />

2.  Make sure you receive the email in your training user’s inbox.

3.  In the **Overview** tab, go to the **Triggers** section and select
    **Test trigger**.

> <img src="media/98f5fce33cc6fad3638e1080b7d0f0ca2e2f4b47.png"
> style="width:6.26042in;height:4.67708in" />

4.  Select the **trigger instance** and then **Start testing.**

> <img src="media/41f1f837be2c73f0e2571b08f6ef813a70b940a4.png"
> style="width:5.83363in;height:2.93765in" />

5.  The execution happens and you can see the updates and the flow in
    the Test pane.

> <img src="media/8320caf90d144be13fbfe2b47fe7d44858700dde.png"
> style="width:6.26042in;height:3.19792in" />
>
> <img src="media/76bd0f02de2a1392e7bf6facacf0547d0ff62ff2.png"
> style="width:6.26042in;height:3.34375in" />

6.  Once the execution is completed, check your email for the agent’s
    reply.

> <img src="media/c0f5f240a4741c2718ba82b80f7f27c4275b6c73.png"
> style="width:6.26042in;height:3.79167in" />

## **Summary**

> In this lab, you built an autonomous financial data retrieval agent
> using Microsoft Copilot Studio and Computer-Using Agents (CUA). You
> configured an event-driven agent that automatically responds to email
> requests, simulates human interaction with a legacy system to retrieve
> portfolio data, and returns accurate results without relying on APIs.
>
> You learned how to:

- Design an autonomous agent that operates without direct user
  interaction

- Use email-based triggers to initiate automated workflows

- Configure Computer-Using Agents to securely navigate and extract data
  from legacy web applications

- Integrate action tools to return results via email

- Reduce reliance on fragile RPA patterns by using AI-driven computer
  interaction

> This lab demonstrates how autonomous agents with CUA can modernize
> legacy system access, streamline operational workflows, and enable
> faster, more reliable decision-making in environments where APIs are
> unavailable.

**Introduction**

Modern users expect intelligent, contextual responses that go beyond
simple keyword matching. This lab will guide you through creating an
intelligent agent that can reason across multiple knowledge sources and
perform real-time actions to deliver comprehensive, accurate answers.

**Objective**

In this lab, you’ll build an intelligent assistant that goes beyond
simple Q&A to deliver contextual, multi-part responses. By the end of
the lab, you will

Create an intelligent agent using the conversational creation
experience. Configure agent tone, behavior, and instructions to reflect
your brand. Add public websites like Wikipedia as knowledge sources for
factual grounding. Disable general knowledge to reduce hallucinations
and ensure accuracy.

## **Task 1: Create a new agent and add knowledge**

Create Nova AI with custom instructions and Wikipedia knowledge
integration using Copilot Studio’s conversational setup experience.

1.  Open a browser and navigate to Copilot Studio at
    +++[*https://copilotstudio.microsoft.com+++*](https://copilotstudio.microsoft.com+++/)
    if not logged in already.

    1.  Username -
        [*+++@lab.CloudPortalCredential*](mailto:+++@lab.CloudPortalCredential)(User1).Username+++

    2.  TAP -
        [*+++@lab.CloudPortalCredential*](mailto:+++@lab.CloudPortalCredential)(User1).AccessToken+++

2.  From the Home page, select **Agent**.

![](./774d832d45041c9ec1b9a10a54172e40d5857d29.png)

3.  Enter the Name as +++Researcher agent+++ and select **Create**.

![](./c4345492ac48c8c19a7f270b77bfa5c6fc2b0a38.png)

4.  Once the agent is created, select **Edit** against **Details**.

![](./3dc8e476a2cf2a3495426c58dd81bd5f626c46ae.png)

5.  Enter the below **Description** and select **Save**.

    1.  +++Answers multi-part questions by combining historical facts,
        biographical data, and real-time information like weather. Ideal
        for deep research, exploration, and knowledge synthesis+++

![](./2035c85f5e1d60b45c0671c6950c5898cbe234f0.png)

6.  Select **Edit** against **Instructions**, enter the below content
    and select **Save**.

\[!Note\] **Note:** Use the **Copy** option and then **Paste** it in the
required place in the VM (Instructions Text area in this case)

You should answer complex questions using verified public information
and real-time lookups like weather or conversions. You should give
clear, concise answers and handle multiple questions one at a time. You
must not speculate, share unverified or sensitive information, or
compare products or companies. You should communicate clearly and
professionally, using a friendly tone and light emojis when appropriate.

![](./67537fde563b2a7aa72a2660c884b236a9bb0808.png)

7.  Scroll down and select **+ Add knowledge** to add a knowledge
    source.

![](./ac28a6ea00b1ffeb801553a2f424f0cb667befad.png)

8.  Select the **Public Website** option form the list.

![](./1576b864e5871388e40052b826a462b0f899c44f.png)

9.  Enter
    +++[*https://en.wikipedia.org+++*](https://en.wikipedia.org+++/),
    select **Add**, and then select **Add to agent**.

![](./b2180f797e98d411346b9ad9e07ebc5b22cf7599.png)

![](./bedc0a9afa3f4ab6ef6702b0d680044a0d7929c4.png)

10. Enter the below message in the Test pane and click **Send** and
    observe the output.

+++Write a draft email to request refund from a toaster that is not
working properly (bread keeps burning)+++

![](./1f5f5d034b5835a568df0403b06050af9d9f7b2a.png)

![](./87b2d92db593dbc32dd42c35de222e2bb9a3b55f.png)

## **Task 2: Add weather connector**

In this task, you will add a weather connector to enable real-time data
retrieval and test generative orchestration. Ensure that the agent
provides only fact-based, controlled responses while enabling it to
perform real-time actions like weather lookups for comprehensive,
multi-step answers.

1.  Select **Tools** tab from the top menu.

![](./4f2b32e5e9969bca7537dc23afa51da7dfbf1a36.png)

2.  Enter +++MSN Weather+++ in the search box and select **Get current
    weather**.

![](./ae32fe10d2706d5221ae0ee52bbec7ddbb2c2fb1.png)

3.  Select the drop down next to the **Not connected** message and
    select **Create new connection**. Then, select **Create** in the
    next screen.

![](./3bcea4f1c2035858a0369843148538465aa88d44.png)

![](./7dee4c535da638bc2b4c9ea038b708e5f1284016.png)

4.  Select **Add and configure** to add the tool to the agent and
    configure it as required.

![](./b9af97a0e5a1da49b1cb703d016c45b645ea1260.png)

5.  Once added, select **Additional details**.

![](./52c1e9b3ddc9dcf61740d0313dbd62c704a4580b.png)

6.  Under Credentials to use, select **Maker-provided credentials**.

**Note:** When using Maker-provided credentials, the end-user of the
agent isn’t prompted to use its own context and connection to connect to
the service. Instead, it’s using the context and connection of the
person who has configured the agent. - Only use author authentication
for actions that don’t need user-specific data, as using the credentials
from someone else can expose to data exfiltration risks. - Use user
authentication for role based access scenarios - Always review security
implications of authentication choices

![](./85efbd14a44661ad0d597192d2e8e7bcdadc3a69.png)

7.  Under **Inputs**, **Units**, -\> **Fill using** -\> select **Custom
    value**, and choose **Metric**.

![](./faa7176c58271bab36d31846f6e4c39fe64b2632.png)

8.  Under **Inputs**, for **Location**, leave **Fill using to
    Dynamically fill with AI**, and select **Customize** to set
    description.

![](./f1b15635cdbbad699a8bb38819b7dd98060b9b08.png)

9.  Set the description as below and then select **Save**.

The location for the weather query. Valid inputs are City, State,
Country. Always include city and country, and state only for locations
where appropriate (e.g., in the US)

![](./5d555294001a3054b90ed3860115c3192a1129f8.png)

![](./c83b5a36c6b81b48f3827a7264c865dcbcdb2735.png)

10. Test your enhanced agent with this complex question:

+++Who is the current CEO of the company that owns GitHub? Where did
they earn their MBA? What's the average rent for a one-bedroom apartment
near that campus? What's the air quality index in that area today?+++

![](./47d560b45e7b0f5da5809b1d879d4e8101ff6b8b.png)

11. Notice how generative orchestration performs multiple searches and
    triggers the weather connector to provide a comprehensive answer

![](./5989aec56a274efe53cdca8aa3cd20013b7c76c8.png)

## **Task 3: Fine-tune your AI assistant for smoother conversations**

Customize system topics to enhance interactions and deliver a smoother
user experience.

In this section, you’ll customize built-in system topics to improve user
interactions and create a more seamless experience beyond just knowledge
sources.

Customize your assistant’s welcome message to make it more engaging, add
suggested start prompts to guide users effectively, and refine system
topics like Escalate to ensure they align with your organization’s
needs.

1.  From the top menu, select **Topics**.

![](./94124065e31467809d06abc8885c5d546dbf2eb1.png)

2.  Select the **Conversation Start** topic under **System**.

![](./34682b4114acd7e35dc2a1bbf6796d50a3e6d5bc.png)

3.  In the topic’s **Message** node, enter the below message.

+++Hi there! I'm Researcher agent, your intelligent assistant for deep
research and discovery. I can break down complex questions and combine
insights from historical facts, biographies, and real-time data like the
weather. What are you curious about today?+++

![](./71973cac510955af687891add0d97e7a59aeb35e.png)

4.  Still in the same node, select **+ Add** -\> **Quick reply**.

![](./be32b6d1e00c0e9c7c13f3411b58f404a1607932.png)

5.  Add the below question.

+++What caused the fall of the Roman Empire?+++

![](./c195cbf154c50ff96ff17334ddc04c014f077a6f.png)

6.  Similarly add 2 more (Select **+ Add** in the quick reply
    **Properties** pane that gets opened).

![](./b93721c40bd5f564ef87efb8d333e2b613743401.png)

+++Who is the current CEO of the company that owns GitHub? Where did
they earn their MBA? What's the average rent for a one-bedroom apartment
near that campus? What's the air quality index in that area today?+++

+++What's the temperature in the city that hosted the last Olympic
Games?+++

![](./675bd41aaba62b49d46ddd01b400d7a8d1a9ea49.png)

7.  Once added, select **Save** to save the topic.

![](./6a494a2b4fb457585b12d5dfe8e2fcc268da5da8.png)

8.  Customize the escalation experience. Select **Topics** -\>
    **System** -\> **Escalate**.

![](./74e6679ea39d3629a0d9f5f936427892aabc8a7b.png)

9.  Update the text to the below, that will more meaningfully unblock
    the end user and select **Save**.

+++I'm sorry, but I can't seem to be able to help you. I recommend
reaching out to our Microsoft Copilot Studio community at
[*https://aka.ms/CopilotStudioCommunity*](https://aka.ms/CopilotStudioCommunity)
or submitting a support request at
[*https://learn.microsoft.com/en-us/power-platform/admin/get-help-support.+++*](https://learn.microsoft.com/en-us/power-platform/admin/get-help-support.+++)

![](./62ca6c67f411b63f25c2b0bd69d5f047d7868cf5.png)

## **Task 4: Make your agent public and publish it to the demo website**

In this section, you’ll remove authentication to make your agent
publicly accessible, then publish it to the demo website for testing and
sharing.Since the Researcher agent provides general information and
doesn’t handle private data, you’ll disable authentication for a
seamless user experience and publish it to the demo website to gather
feedback before deploying to your real site.

\[!Alert\] **Important:** Since this is a test environment used for
training purposes, there might be issues in getting the agent published,
based on any recent changes to the product. If that happens, there will
be issues in executing the exercises that follow. This will not be the
case in the production.

1.  Go to **Settings** .

![](./c5b479799c7c13f46e7a5da7c228c823e155cc70.png)

2.  Select **Security** -\> **Authentication**. Select **No
    authentication** and then select **Save**.

![](./bcac74072a816d11b800c43d380da2b7317e363c.png)

3.  Select **Save** in the confirmation prompt.

![](./6e42fa4c55c4d8d489534f939b52f40262d0f02c.png)

4.  You can now close the Settings pane.

![](./4a63d551bbc66d3f35fe0ad34ec035dd3c40b904.png)

5.  Select **Publish** to make your changes live.

![](./01bd070b6af71fa47ce28672b04ae15ee26a3efb.png)

6.  Select **Publish** in the confirmation dialog.

![](./be2c6f49a4d28c959439b74878586df1b4038901.png)

7.  You will get a success message once the publish is done.

![](./a3f8533f7bebbf6d1076904c018b18de98119811.png)

8.  Now, select **Channels** from the top menu.

![](./981e4c8b75f65061c48350274cbdbfdaad682086.png)

9.  Select **Demo website** from the list of channels available.

![](./bd0998c18a3193158bb8066ffcf8c93fceca76f2.png)

10. Enter the Welcome message as +++Welcome to your demo website+++ and
    select **Save**.

![](./0d6cd19bfa211d200ac814be807e2e49864e9b8c.png)

11. Click on **Open demo website** to open your site.

![](./a68e99dbdffcf33e035dc454de2ab3765d702982.png)

12. You can now interact with your agent.

![](./77aa579b8216018fb5cd7ad72b26223ef1d8dd3d.png)

## **Summary**

In this lab, you successfully delivered a public-facing intelligent
agent that:

- Answers complex, multi-part research questions

- Uses verified public knowledge and real-time connectors

- Minimizes hallucinations through controlled knowledge sources

- Provides a polished, user-friendly conversational experience

- Is deployed and accessible via a live demo website

This lab demonstrates how to design, enhance, and publish a
**production-ready intelligent agent** that goes beyond simple Q&A to
deliver trustworthy, real-time, and context-aware insights.

**Estimated Duration:** 40 minutes

## **Lab objectives**

In this lab, you will create a Frontline Operations Agent using
Microsoft 365 Copilot Agent Builder. The agent will help frontline
workers, store managers, and supervisors handle daily operations,
customer service, shift readiness, compliance, and escalation workflows.
You will configure agent instructions, upload enterprise knowledge
sources, test prompts, validate outputs, and optimize responses. After
completing this lab, you will be able to:

- Create a Microsoft 365 Copilot custom agent

- Configure frontline retail agent instructions

- Upload knowledge sources for grounding

- Test store operations prompts

- Improve frontline productivity with AI

- Build reusable retail frontline agent templates

## **Scenario**

Zava Retail is a rapidly expanding multi-format retail chain operating:

- 250 stores across urban, suburban, and tier-2 markets

- 8,000 employees including cashiers, floor associates, warehouse staff,
  supervisors, and managers

- Presence across multiple regions, each with different staffing
  patterns and customer behavior

- Heavy seasonal demand spikes during festivals, clearance sales, school
  openings, and holiday promotions

- Thousands of frontline operational requests every week

Zava Retail has invested in Microsoft 365 and wants to modernize store
execution using a Microsoft 365 Copilot Frontline Agent.

**Key Challenges:**

- Managers spend too much time answering repetitive questions

- Store processes are inconsistent across locations

- Seasonal sales create staffing and service pressure

- New hire onboarding takes too much manual effort

- Operational issues are escalated at a slow pace

To solve these challenges, Zava Retail deploys a **Microsoft 365 Copilot
Frontline Agent** accessible in Copilot chat, Microsoft Teams, and
mobile devices for store workers. The agent becomes a 24x7 AI operations
Assistant for multiple retail stores. The Zava Frontline Agent will help
8,000 employees across 250 stores work more efficiently by giving
instant, consistent answers and reducing dependence on managers.

**Key Personas:**

**Patricia Gray – Operations Head**

The regional operations manager at Zava Retail oversees multiple stores
and ensures consistent execution across locations. The major challenges
include:

- Needs visibility into recurring issues across stores

- Tracks store performance and staffing gaps

- Requires faster escalation handling across regions

**Marie Brown – Store / Sales Associate**

The store associate at Zava Retail supports customers on the sales
floor, manages shelf availability, and assists with promotions. The
major challenges include:

- Needs quick answers on product locations and promotions

- Faces stock shortage questions from customers

- Requires guidance during peak store traffic

**David Turner – Cashier**

The cashier at Zava Retail handles billing transactions, customer
payments, and checkout queues. The major challenges include:

- Needs support resolving pricing or discount issues

- Manages long queues during rush hours

- Requires quick access to refund and return policies

**Fratini Greens – Store Manager**

The store manager at Zava Retail is responsible for store performance,
customer satisfaction, and team productivity. The major challenges
include:

- Receives repetitive operational questions from staff

- Needs visibility into daily store priorities

- Must balance staffing, sales, and service quality

## **Exercise 1: Create the Frontline Agent**

Patricia logs into Copilot to review Festive Campaign readiness.

1.  Navigate to +++<https://m365copilot.com/+++> to open Microsoft 365
    copilot page.

2.  Enter the **Username -
    <+++@lab.CloudPortalCredential>(User1).Username+++** in the field
    and then click on the **Next** button to proceed.

<img src="media/844c61a330084246354a0a376d5f6c1785857ecf.png"
style="width:6.5in;height:5.08333in" />

3.  Enter **TAP Token -
    <+++@lab.CloudPortalCredential>(User1).AccessToken+++** in the field
    and then click on the **Sign in** button and click on the **Yes** to
    stay Signed in.

<img src="media/759f3189305c2abb9ff76509d1b17e67f3e1c4fc.png"
style="width:6.5in;height:5.3125in" />

4.  Explore the Copilot chat environment.

<img src="media/5fa148b44ecc923bf50803992e53a35ea5c10afd.png"
style="width:6.5in;height:3.80208in" />

5.  Expand **navigation pane**, and look for **More agents**.

<img src="media/b4a5fd7ea58a142598a394e6c431658446082e54.png"
style="width:6.5in;height:3.83333in" />

6.  Select **+ Create Agent** to start building a new agent.

<img src="media/da523dda91f0cd24f5969605836fdec37e61840c.png"
style="width:6.5in;height:3.83333in" />

7.  Click **Skip** to move to configure page.
    <img src="media/1f3601fbc94c66b3055ed787f2116061b08c1510.png"
    style="width:6.5in;height:3.83333in" />

8.  When the **Agent creation panel** opens, paste the following details
    in respective fields to build the agent.

    1.  **Name:** +++Frontline Operations Assistant+++

    2.  **Description:** +++Supports store staff, field workers,
        frontline teams with schedules, SOPs, customer help, daily
        operations.+++

    3.  **Instructions:**

You are a frontline operations assistant for employees.  
Help workers with shift guidance, store procedures, customer service  
responses, escalation steps, daily checklists, safety reminders, and  
quick answers.  
Keep responses concise and mobile-friendly.

<img src="media/b28183b9a35b9d2ffff5efea4017627523aa852e.png"
style="width:6.5in;height:3.69792in" />

9.  Navigate to **Knowledge** section to add knowledge sources. Select
    **Upload from device**.

<img src="media/63143f8421fe92b842c73d19b12b15654bc536cf.png"
style="width:6.5in;height:4.09375in" />

10. Select the below files from **C:\Labfiles\Lab5-Lab files** and
    select **Open**.

    1.  SOP PDFs

    2.  Employee handbook

    3.  Store checklist

    4.  FAQ docs

    5.  Policy docs

    6.  Shift guides

<img src="media/fc744db4e07a8b671ed0b7bd07a508f3451adf78.png"
style="width:6.5in;height:3.33333in" />

11. Verify that all the selected files are uploaded in the Knowledge
    sources.

<img src="media/7ef7b22ef7ef86af2d5b82bd88c0a02fa9acff1a.png"
style="width:6.5in;height:3.69792in" />

12. Click **Create** to publish the agent.

\[!Note\] Wait for 5-10 minutes for the agent building process
completion.

<img src="media/99ca218f690f3c403f90d45c17112bd2d0501544.png"
style="width:6.5in;height:3.70833in" />
<img src="media/2e97b6ddf7373b4c4ae3f52ee1fb57d3937c59c9.png"
style="width:6.5in;height:4.02083in" />

13. Once the agent is created successfully, click **Start Chat** to
    start using the agent.

<img src="media/97bc700b8677ca1384192054227d02845f1dacd0.png"
style="width:6.5in;height:3.66667in" />
<img src="media/f95b8366b8f5bad434048a1d3edb23ec9104fc58.png"
style="width:6.5in;height:3.54167in" />

## **Exercise 2: Access Frontline Operations Agent in Microsoft Teams**

Patricia Gray (Regional operations manager) is seeking for an overview
of the operational activities and get the key operations related queries
of Zava Retail on Microsoft Teams for better visibility.

1.  Navigate to Microsoft Teams
    +++[https://teams.microsoft.com+++](https://teams.microsoft.com+++/)
    and sign in with your credentials if needed.

    1.  Username - <+++@lab.CloudPortalCredential>(User1).Username+++

    2.  TAP Token -
        <+++@lab.CloudPortalCredential>(User1).AccessToken+++

<img src="media/844c61a330084246354a0a376d5f6c1785857ecf.png"
style="width:6.5in;height:5.08333in" />

<img src="media/759f3189305c2abb9ff76509d1b17e67f3e1c4fc.png"
style="width:6.5in;height:5.3125in" />

2.  Open Microsoft Teams. Select **Copilot** icon from the left
    navigation pane.

<img src="media/b031821f67935f4b1a9a565ef3e82eaa14def8c3.png"
style="width:6.26848in;height:2.11374in" />

3.  Go to **Expand Navigation** icon to open the menu. Select
    **Frontline Operations Agent** to open and access the agent.

<img src="media/52e3280d06a923ff6081ee7a345b11d0c740c466.png"
style="width:6.26848in;height:2.20011in" />

4.  Now, Patricia can use the agent directly inside Teams. **Frontline
    Operations Agent** can be accessed under Microsoft Teams.

<img src="media/61f7f6e657e1b83fdf2faeead901237b1b056884.png"
style="width:6.26394in;height:2.07737in" />

## **Exercise 3: Action and Decision Intelligence**

This exercise will help Frontline Operations Agent perform a task or
take a specific action based on the data, findings, or situation.

### **Task 1: Identify Startup Checklist**

1.  Navigate to +++<https://m365copilot.com/+++> Microsoft 365 copilot
    page.

2.  David Turner, Cashier at Zava Retail is starting the day and looking
    for a quick checklist. To execute this step, go to the Frontline
    Operations agent, paste the below given prompt in the field, and
    then click on the **Send** button.

I am opening cashier. Give me first 20-minute startup checklist.

<img src="media/124e6a90183cc5c9caee47382f98024e13fc4033.png"
style="width:6.5in;height:4.36458in" />

3.  Review the output:

<img src="media/fe24a33754c6e87c9291ad5cf30878c640ee5784.png"
style="width:6.5in;height:4.73958in" />
<img src="media/1adf9b1ad2757b69a39f676f517a1eaa58712338.png"
style="width:6.5in;height:4.71875in" />

Note: Generated outputs are non-deterministic and may vary across users,
sessions, and environments.

### **Task 2: Resolve Customer Issues**

1.  Marie Brown, Store Associate wants to resolve recurring issues faced
    by customers at the Zava Retail store. To execute this step, go to
    the Frontline Operations Agent, paste the below given prompt in the
    field and then click on the **Execute** button.

Customer says wrong discount applied. What should I do?

<img src="media/867489f7393d0d7a50772d5edae617cca5959ab1.png"
style="width:6.5in;height:4.71875in" />

2.  Review the output:

    1.  The agent will fetch the official policies and SOPs from
        knowledge source and provide the response.

<img src="media/bdc71519e2872ffc0648ca4aa3e2341cde8d2e22.png"
style="width:6.5in;height:4.77083in" />

<img src="media/d5cd4b12cc5f6da85cce48dc529424417d0ed8ec.png"
style="width:6.5in;height:4.80208in" />

Note: Generated outputs are non-deterministic and may vary across users,
sessions, and environments.

3.  Paste the below given prompt in the field and then click on the
    **Send** button.

Product out of stock during sale. What are the next steps?

<img src="media/9268a609deca2aa637fec8c3c66a90aacae44f22.png"
style="width:6.5in;height:4.75in" />

4.  Review the output:

<img src="media/074cd598a33ec34ec89c81a607abd971685949b7.png"
style="width:6.27303in;height:2.5274in" />

<img src="media/7fdfc1b757a22d22e7a9153068529d67f682e821.png"
style="width:6.26394in;height:2.63195in" />

Note: Generated outputs are non-deterministic and may vary across users,
sessions, and environments.

### **Task 3: Store Manager Scenario**

1.  Fratini Greens, Store Manager wants to understand the top priorities
    during weekend rush at retail store, retrieve new hires onboarding
    checklist, and resolve other managerial concerns. To execute this
    step, go to the Frontline Operations Agent, paste the below given
    prompt in the field, and then click on the **Send** button.

Create my top 5 priorities for Store \\118 during weekend rush.

<img src="media/99fe1ed7873eba401bd67f9e93ee91319b127209.png"
style="width:6.27303in;height:3.08197in" />

2.  Review the output:

<img src="media/b41ba49c16d232767c95e6911a418940771daaae.png"
style="width:6.27758in;height:2.46376in" />

<img src="media/2fecaa5eb27a0760a8a01ac8f909c49dc18246a5.png"
style="width:6.27303in;height:2.5774in" />

3.  Paste the below given prompt in the field, and then click on the
    **Send** button.

A new hire joined today as sales associate. Give Day 1 onboarding
checklist.

<img src="media/d57294caefd9eabb50707eeea2697c5deed6ba27.png"
style="width:6.27303in;height:2.93196in" />

4.  Review the output:

<img src="media/1840f5939857b00c82fed387183978529c76e5cf.png"
style="width:6.26848in;height:2.55921in" />

<img src="media/006790dfa8d1aeab8a38c707a2bde0b887c2313b.png"
style="width:6.27303in;height:2.51376in" />

### **Task 4: Multi-persona Role Testing**

1.  Patricia Gray, Operations Head is looking for query resolution from
    multiple roles including cashier, store associate, and new hire. To
    execute this step, go to the Frontline Operations Agent, paste the
    below given prompt in the field and then click on the **Send**
    button.

As a regional operations manager, identify top recurring operational  
issues likely across 250 Zava stores and recommend fixes.  
  
Cashier: Help with queue rush handling  
Supervisor: Closing checklist  
Manager: Weekly priorities  
New Hire: First shift guidance  
Regional Lead: Store risk summary

<img src="media/a485597872cbe94028ba742ef06b4749dbc6cb12.png"
style="width:6.26394in;height:2.9365in" />

2.  Review the output:

<img src="media/2d6d8e5f1f8b1140fa6bbac954e67f096133e7a9.png"
style="width:6.26394in;height:2.55921in" />

<img src="media/6862a4e6c52e054f253d88dbd04a600e949e159f.png"
style="width:6.27303in;height:2.49558in" />

<img src="media/55418fa1037f1d98db5609c4f965df65a21752c7.png"
style="width:6.26394in;height:2.55921in" />

<img src="media/51a4e4793878adfc732ec2ac4b86f445e04e1c48.png"
style="width:6.27303in;height:2.6774in" />

### **Task 5: Review and Refine the Output** 

1.  Evaluate whether the Frontline Operations Agent’s summary meets your
    expectations.

2.  If results are too broad or missing key details, refine your prompt.

**Example**: “Narrow this summary to focus only on critical risks and
delivery blockers.”

3.  Export or copy the summary for documentation, reports, or meeting
    notes.

<img src="media/555586be0332f69003a5d961dc1f091d408deaef.png"
title="A screenshot of a computer AI-generated content may be incorrect."
style="width:6.5in;height:3.38542in" />

\[!Note\] Here is a brief overview of the tasks associated with each
icon shown in the screenshot:

<img src="media/94e715cb1965a0242bdc3092217897b3aeba7308.png"
style="width:6.5in;height:0.6875in" />

1.  **Clipboard Icon** – Likely used for **copying or pasting** content.

2.  **Thumbs-Up Icon** – Typically indicates **liking or approving** an
    item or action.

3.  **Thumbs-Down Icon** – Generally used to **dislike or disapprove**
    something.

4.  **Speaker Icon** – Represents **audio settings or volume control**.

5.  **Pencil Icon** – Commonly used for **editing or writing** tasks.

6.  **Clock with Arrow Icon** – Tooltip says **"Add to recent page"**,
    which means it adds the current item to your **recently accessed
    pages** for quick reference.

**Summary**

In this lab, learners explored how Zava Retail can improve store
operations using a **Microsoft 365 Copilot Frontline Operations Agent**.
With 250 stores, 8,000 employees, and high seasonal demand, Zava Retail
needed a scalable solution to reduce manager workload, improve
consistency, and support frontline staff in real time.

In this lab, you created a custom agent to help store associates,
cashiers, supervisors, and managers with daily tasks such as opening and
closing procedures, shift readiness, promotions, returns, stock issues,
safety incidents, and escalations.

The agent was grounded using SOPs, policies, FAQs, checklists, and
training documents, then tested through real retail scenarios and
persona-based prompts.

By the end of the lab, learners demonstrated how the Zava Frontline
Agent can:

- Reduce repetitive questions to managers

- Improve consistency across stores

- Speed up onboarding for new hires

- Enable faster issue resolution

- Improve frontline productivity and customer service

This lab showed how AI-powered frontline agents can help Zava Retail
scale operations while empowering employees with instant support.

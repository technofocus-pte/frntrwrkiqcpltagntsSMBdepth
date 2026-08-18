**Estimated Duration:** 30 minutes

## **Lab objectives**

In this lab, you will explore how to build a Workforce Upskilling Agent
using Microsoft 365 Copilot Agent Builder. You will learn how to
configure the agent aligned to workforce transformation goals, ground it
in organizational context using Work IQ principles, and enrich it with
enterprise knowledge sources. By the end of this lab, you will be able
to:

- Build a custom Workforce Upskilling Agent using Microsoft 365 Copilot
  Agent Builder

- Configure agent instructions aligned to retail workforce
  transformation goals

- Ground the agent in organizational context using Work IQ principles

- Add enterprise knowledge sources to improve agent relevance

- Diagnose employee skill gaps using operational behavior signals

- Generate personalized learning plans for multiple workforce personas

- Use the agent to simulate coaching conversations and leadership
  role-play

- Produce workforce readiness briefings for executive stakeholders

## **Scenario**

You are Jordan Mercer, Chief Operating Officer of Zava Retail — a
mid-sized retail chain specializing in consumer electronics and home
goods, operating across four regional store clusters in the Midwest.
Zava Retail is eighteen months into a digital transformation initiative:

- A new Retail Management System (RMS) is being rolled out company-wide

- AI-powered inventory forecasting is active in two regional store
  clusters

- Customer behavior analytics tools are being adopted by store
  supervisors

- ERP migration completes next quarter

Technology adoption is accelerating faster than employee readiness. To
address this challenge, you will build and deploy a Workforce Upskilling
Agent that helps identify skill gaps, personalize employee learning
journeys, and improve workforce readiness across operations.

**Key Personas**

1.  Jordan Mercer (COO – Primary Persona): Leads digital transformation
    strategy and oversees workforce capability planning.

2.  Alex Chen (Store Operations Supervisor)- Frequently overrides AI
    inventory alerts without reviewing them.

3.  Maria Santos (Supply Chain Analyst)- Leaving in 60 days with
    undocumented critical supplier knowledge.

4.  Derek Okonkwo (Operations Coordinator)- Low RMS adoption despite
    extensive legacy systems experience.

## **Exercise 1: Creating the Workforce Upskilling Agent**

Before the agent can support workforce development, you must first build
and configure it inside Microsoft 365 Copilot.

### **Task 1: Open Agent Builder**

1.  Navigate to +++<https://m365copilot.com/+++> to open Microsoft 365
    copilot page. Sign in with your credentials.

    1.  Username - <+++@lab.CloudPortalCredential>(User1).Username+++

    2.  TAP Token -
        <+++@lab.CloudPortalCredential>(User1).AccessToken+++

![](./d6f9bc5840002fa0172e0ad12196892737eae7dc.png)
![](./370181bec556d226f2ab1c716438b89ff011cdc5.png)
![](./8fe1bb8e06347326fe438aae04c93189109f5cb1.png)

2.  From the left navigation panel, click **More agents**, then click
    **Create Agent**.

![](./3dae86f741f77a1652a01a23b626af86d25ebf18.png)

3.  The **New Agent** page will be opened. Now click **Skip**.

![](./2b54e11ae6654c80d95493e66cf1e7602eab1482.png)
![](./5d375c6e6d9319a887bf14486d13a720fc7e777d.png)

## **Task 2: Define and Configure Agent**

1.  Paste the following details to define and configure the agent:

**Agent Name**: +++Zava Retail Workforce Coach+++

**Agent description**: Supports workforce capability development by
diagnosing skill gaps, generating personalized learning plans, and
assisting leaders with workforce readiness decisions during digital
transformation

![](./89cdf988749a189021fa5fa40ec41dcd04e8c1da.png)

2.  Paste the below given prompt in the field and then click on the
    **Execute** button.

You are Zava Retail’s Workforce Coach.  
  
Your purpose is to help leaders identify workforce capability gaps,  
generate personalized learning plans, support coaching simulations,  
and recommend interventions during digital transformation.  
  
Focus on:  
  
- RMS adoption  
  
- AI inventory forecasting literacy  
  
- Customer analytics interpretation  
  
- Supply chain risk management  
  
- Change adoption coaching  
  
Always tailor recommendations based on:  
  
- Employee role  
  
- Operational urgency  
  
- Experience level  
  
- Retail store cluster context

![](./3ba2d9145d3a9a3cc9302f36f1dcc869206b8eef.png)

3.  In the Knowledge Sources, upload or connect the below mentioned
    organizational resources. Select **Upload from device** icon to
    upload the files. The required files for this lab are available at
    **C:\Lab Files\Lab 3 - Lab files**

    1.  RMS onboarding guide

    2.  AI inventory forecasting SOP

    3.  Store operations handbook

    4.  Supply chain transition playbook

    5.  ERP migration training documentation

![](./d927693bb7a985343a5a60fd3fa0164f49e7c82c.png)
![](./a01330b22da1f52912afc1db734c7bd050f0a1a5.png)

![](./203c0b354c685f5751bab4088f4a1d932d0b1ab3.png)

4.  Click **Create** and then, select **Start Chat**.

![](./998a8b8c7ef8a27dd3bb1226faf34cf374db6da9.png)
![](./6d22230ef569a1df7bbf913974d8881ba7e9328e.png)
![](./424024d29715b7c6e556f04056548676f8f33d00.png)

## **Exercise 2: Grounding the Agent in Organizational Context**

Once the agent is built, provide the transformation context of Zava
Retail.

### **Task 1: Initialize Agent Context**

1.  Paste the following prompt in the chat panel of Zava Retail
    Workforce Coach agent and click on the **Send** button.

I am the COO of Zava Retail, a mid-sized retail chain specializing  
in consumer electronics and home goods, with 4 regional store clusters  
and approximately 600 employees across store operations, supply chain,  
customer experience, and merchandising.  
  
We are currently migrating to a new Retail Management System (RMS)  
and deploying AI-powered inventory forecasting and customer analytics  
tools.  
  
Our key upskilling priorities are:  
1. RMS system adoption  
2. AI inventory and analytics supervisory skills  
3. Supply chain risk management for mid-career analysts

![](./074e1154840fb7563f870a1ca025e2329e5756c4.png)

2.  Review the output:

![](./7916e2736f5f0a34adf19d828376a4d545189405.png)
![](./9b579e5ad6d65a77e6d79fec9bdc0509b10a0235.png)
![](./f862773865084b03e9dcd25130be8d221cdeea1b.png)

**Note:** AI-generated responses are non-deterministic and may vary
across environments, sessions, and prompts.

### **Task 2: Validate Agent Understanding**

1.  To test the agent, enter the following prompt and click on the
    **Send** button.

What are the most critical workforce skill domains I should prioritize
during this retail digital transformation?

![](./3cb3093256dd5653adb05dc885eea2022bc7dcde.png)

2.  Review the output:

![](./9bfe3a8b0aae7c8614860bc70f3273dbeabe8413.png)
![](./37a320bb536457114f2e59aecb645d03516d0e56.png)

**Note:** AI-generated responses are non-deterministic and may vary
across environments, sessions, and prompts.

## **Exercise 3: Diagnosing Workforce Skill Gaps**

### **Task 1: Diagnose Alex Chen**

1.  Paste the following prompt and click on the **Send** button to
    diagnose workforce skills gaps:

I have a Store Operations Supervisor named Alex who is consistently  
overriding AI-powered inventory replenishment alerts without reviewing  
them — approximately 3 times per week over the past month. Based on this
behavioral signal, what skill gaps should I hypothesize, and what
targeted learning plan should I create?

![](./80d4d4acbf449f1f81877ae8708e2b3b8fbc2c80.png)

2.  Review the output:

![](./643ea7d439e9f3145311d8ebc60f0da806611a5d.png)
![](./5e044ca9694ee1077cdd49b307c99ddc41464b71.png)

### **Task 2: Diagnose Maria Santos**

1.  Paste the following prompt and click on the **Send** button to
    diagnose workforce skills gaps:

One of our supply chain analysts, Maria, is leaving in 60 days. She  
owns four sole-source supplier relationships with no documented
handover  
process.  
What urgent learning and knowledge transfer plan should I implement?

![](./ec5bc9e94b76606f8a1461074e27825d82aad933.png)

2.  Review the output:

![](./0781d01f50d6d95f209a9bef6c929f09fa345684.png)
![](./18d1448c7d0c2c8ab6179914c3d779939d8ccd10.png)

### **Task 3: Diagnose Derek Okonkwo**

1.  Paste the following prompt to diagnose workforce skills gaps:

Our RMS went live 6 months ago. Derek is at 31% system utilization —  
lowest on his team.  
He has 11 years of legacy system experience.  
What resistance patterns and skill gaps should I address?

![](./d00ed49f430c4ecb15235a1a61140dbef35e38c6.png)

2.  Review the output:

![](./22fa8174c09bba9ce7bbf3ef504e0a9467d34e1e.png)
![](./917eeb684382e06a1501eabbeef5be658fa5f3be.png)

## **Exercise 4: Generating Personalized Learning Plans**

### **Task 1: Generate Alex’s 6-Week Plan**

1.  To generate plan for Alex, paste the following prompt and click on
    the **Send** button.

Generate a structured 6-week learning plan for Alex with:  
- Learning objectives  
- Weekly activities  
- Resources  
- Checkpoints  
- Success metrics

![](./0916a796d54672de320ee120b50429df1d293186.png)

2.  Review the output:

![](./3b9ce52879646acb96ae73e8b5bdbb6cb6f789e5.png)
![](./eca3cb1e6fa10b3d3a859fcc060ecf0dc7a4e748.png)

### **Task 2: Maria’s 60-Day Transition Plan**

1.  To generate plan for Maria, paste the following prompt:

Generate a 60-day knowledge transfer and upskilling plan for Maria’s  
transition scenario.  
Include parallel tracks for:  
1. Knowledge transfer  
2. Analyst upskilling

![](./e1196aaff4862a4ff747b2134ffe3a998fc406e8.png)

2.  Review the output:

![](./dc56254a6fb4fd2faf65151ec1aa699265270d1c.png)

### **Task 3: Derek’s RMS Adoption Plan**

1.  To generate plan for Derek, paste the following prompt and select
    **Send** button.

Create an 8-week adoption-focused learning plan for Derek that positions
RMS mastery as a career growth opportunity.

![](./e63c0a29c6dbab0d80761ca48e9b2b2875487ee7.png)

2.  Review the output:

![](./dcaf8583cdb391f09e84e1463295bf04ee2364e7.png)

## **Exercise 5: Workforce Readiness Briefing**

### **Task 1: Generate Executive Briefing**

1.  To test the workforce readiness and generate a briefing plan, paste
    the below prompt, and click on the **Send** button.

Generate a workforce readiness briefing for Zava Retail covering:  
1. Current risk summary  
2. Intervention status  
3. What I need from Store Managers  
4. 30-day watch list

![](./c6ad0dc05aeb5964549df0c629711d40f07f5b7a.png)

2.  Review the output:

![](./72b67fa64d2af1a15a3a76c0da1880301ef47513.png)

### **Task 2: Tailor for VP of HR**

1.  To test the workforce readiness and generate a summary for the VP,
    paste the below prompt and click on the **Send** button.

Condense this into a 5-bullet summary for my VP of HR focused only on HR
action items.

![](./753428f8695f153b141c940b13cecb5b22aa6cf3.png)

2.  Review the output:

![](./770d4067964b5f3f0df7fc23990109ba0539296b.png)

## **Summary**

In this lab, you built a custom Workforce Upskilling Agent in Microsoft
365 Copilot designed to support retail workforce transformation. You
configured the agent’s behavior to align with workforce development
goals, grounded it in organizational context for more relevant and
accurate responses, and used operational signals to diagnose workforce
skill gaps. The lab also guided you through generating personalized
learning plans tailored to employee needs, refining agent responses
through prompt engineering for improved effectiveness, and producing
workforce readiness briefings to support decision-making and training
strategy.

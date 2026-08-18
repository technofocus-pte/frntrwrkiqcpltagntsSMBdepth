**COPILOT COWORK · LAB 5**

**Intelligent file organiser**

[TABLE]

**How to read this guide**

[TABLE]

# By the end of this lab, you will be able to:

> • Classify and rename enterprise files using AI-generated naming
> conventions.
>
> • Apply the YYYY-MM-DD_Topic_DocType rename convention across an
> entire OneDrive folder.
>
> • Execute a governance audit covering duplicates, staleness, sharing
> risks, and ownership gaps.
>
> • Use human-in-the-loop approval gates before every bulk file
> operation.
>
> • Generate an Excel governance tracker and post a Teams summary from a
> single instruction.
>
> • Reorganise healthcare documents into clinical category subfolders
> with a department-aware naming scheme.
>
> • Apply responsible AI principles, understanding which governance
> actions require human approval.

You are a Power User or IT Administrator at Contoso Operations,
overseeing a shared OneDrive environment of 28 mixed files across
retail, healthcare, finance, and project folders. File naming is
inconsistent, governance is weak, and a compliance review is
approaching. You'll use Copilot Cowork, an agentic AI layer that
orchestrates OneDrive, SharePoint, Excel, and Teams, to classify,
rename, audit, report on, and reorganise these files. Every bulk action
requires your explicit approval before it executes.

# Prerequisites

Complete the following setup before starting (about 15–20 minutes).

**Required Microsoft 365 environment**

> • Microsoft 365 Copilot with Copilot Cowork enabled.
>
> • Microsoft Teams with permission to post to channels.
>
> • OneDrive for Business and SharePoint Online.
>
> • Microsoft Excel (Web or Desktop).
>
> • A Microsoft Graph-connected M365 tenant.

**Required OneDrive folder structure**

Create a Lab Files folder in OneDrive with four subfolders:

> • **Lab Files / Healthcare** — upload the provided clinical document
> samples.
>
> • **Lab Files / Retail** — upload the provided retail document
> samples.
>
> • **Lab Files / Shared Files** — configure “Anyone with the link”
> sharing on at least three files.
>
> • **Lab Files / Archive Candidates** — optional pre-populated stale
> documents.

**Required Teams environment**

> • Team: Contoso Operations (or equivalent).
>
> • Channel: General (Standard), the target for the Exercise 3 Teams
> post.

## Exercise 1: Automated file classification and renaming

Use AI to classify all files in your Lab Files folder, propose a
YYYY-MM-DD_Topic_DocType renaming scheme, preview the full mapping, then
approve and execute the batch rename into topic-organised subfolders.

### Step 1 — Open Cowork and submit the classification prompt

1.  Open your browser, go to **m365.cloud.microsoft**, and sign in with
    your lab account.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image1.png) 
>
>  
>
> ![A screenshot of a login box AI-generated content may be
> incorrect.](./media/image2.png) 
>
> ![A screenshot of a login screen AI-generated content may be
> incorrect.](./media/image3.png) 

- Click Yes to stay signed in.  

>    ![A screenshot of a computer screen AI-generated content may be
> incorrect.](./media/image4.png) 
>
> **2.** Open Microsoft 365 Copilot from the launcher, then click the
> **Cowork** tab, NOT the Chat tab. Click inside the prompt bar and
> enter the classification prompt below.

[TABLE]

[TABLE]

![](./media/image5.png)

*Classification prompt typed and ready to send.*

### Step 2 — Cowork discovers the folder and analyses content

No action needed, Cowork begins immediately. Watch the Workspace panel
open on the right.

> **3.** Workspace shows Step 1 “Finding your Lab Files folder” with a
> spinner.
>
> **4.** In the chat, read “I'll start by locating your Lab Files folder
> in OneDrive.” Click “Thought process \>” to expand Cowork's reasoning.
>
> **5.** Watch the Workspace counter advance from 0/3 to 1/3 once the
> folder is found.
>
> **6.** Cowork then lists all subfolders in parallel, you'll see
> “Executing tasks…” with multiple folder scans running at once.

![](./media/image6.png)

*OneDrive discovery begins; Workspace shows Steps and skill activation.*

![](./media/image7.png)

*Lab Files found; parallel subfolder listing begins (Retail and
Healthcare).*

![](./media/image8.png)

*Step 2 active; content extraction from all 28 files starts.*

![](./media/image9.png)

*Adaptive extraction: empty spreadsheets detected, PDF fallback
applied.*

### Step 3 — Review the rename mapping and approve

After analysis, Cowork produces the full old-name → new-name mapping and
stops, it renames nothing until you approve.

> **7.** Cowork completes all three steps (3/3). Read the output “Lab
> Files — Analysis & Proposed Renaming,” one row per file.
>
> • Read the date-basis legend: \[c\] = date in file content; \[p\] =
> period from filename (Q1 -\> Jan 1); \[m\] = modified date; \[s\] =
> inferred season.

[TABLE]

> **8.** Scroll through all sections (Shared Files, Archive, Retail,
> Healthcare). Note any name you want to adjust.
>
> **9.** In the message box, type the approval below and press the send
> arrow:

[TABLE]

![](./media/image10.png)

*All three steps complete; rename mapping displayed, approval gate
open.*

![](./media/image11.png)

*Rename table: Shared Files and Archive Candidates sections.*

![](./media/image12.png)

*Rename table: Retail section showing season inference \[s\] and
duplicate flags.*

![](./media/image13.png)

*Healthcare section, “Things worth knowing” disclosure, and approval
prompt.*

### Step 4 — Approve folder creation and execute the batch rename

> **10.** After you send the approval, the Workspace expands from 3/3 to
> 3/5, two new steps appear: “Create new consolidated folder” and
> “Rename and move all 28 files.”

![](./media/image14.png)

*Workspace expands to five steps; “Create folder?” dialog appears.*

![](./media/image15.png)

*Approval message sent; execution mode begins.*

> **11.** A **Create folder?** dialog appears with the name “Renamed
> Files 2026-06-19”, it uses today's date for audit traceability.
>
> **12.** Click the dark **Create** button to approve.

[TABLE]

![](./media/image16.png)

*Create-folder dialog; the full five-step plan is visible in the
Workspace.*

![](./media/image17.png)

*Cursor on Create; about to approve folder creation.*

> **13.** A **Use Microsoft Graph?** dialog appears for the first
> rename. Click the dropdown next to Approve and choose **Always allow
> Call graph** to grant batch permission.
>
> **14.** If a **Failed 1 action** error appears (a locked file), note
> it and continue, Cowork retries later. Watch for 5/5 in the Workspace
> when all renames complete.

![](./media/image18.png)

*Folder created; file-ID retrieval begins, test-first validation
announced.*

![](./media/image19.png)

*“Use Microsoft Graph?” first rename + move approval for the test file.*

![](./media/image20.png)

*Test file approved; the 27 remaining files queued for batch
processing.*

![](./media/image21.png)

*Test success confirmed; “Always allow Call graph” presented.*

![](./media/image22.png)

*“Always allow Call graph”: session-scoped batch permission granted.*

![](./media/image23.png)

*“Failed 1 action”: the locked file is isolated, the batch continues.*

![](./media/image24.png)

*Exercise 1 complete: structured completion report with a “Still
pending” section.*

### Step 5 — Create topic subfolders and verify in OneDrive

> **15.** In the message box, type the prompt below and send it:

[TABLE]

> **16.** The Workspace grows from 5/5 to 5/7, two steps are appended:
> “Creating topic subfolders” and “Move files into topic subfolders.”
>
> **17.** A **Create folder?** dialog appears for each subfolder
> (Retail, Healthcare, Finance, Project Planning, Archive). Choose
> **Always allow Create folder** in the dropdown.

![](./media/image25.png)

*“Create subfolders by topic” typed; Workspace about to grow to seven
steps.*

![](./media/image26.png)

*“Create folder?” for the first topic subfolder; “Always allow” option.*

![](./media/image27.png)

*All five topic subfolders created; step 7 file-move operations begin.*

![](./media/image28.png)

*Complete: all 28 files renamed and sorted by topic.*

![](./media/image29.png)

*Transition: the Exercise 2 governance-audit prompt typed and ready.*

> **18.** Open OneDrive in a new tab: **My files \> Lab Files \> Renamed
> Files 2026-06-19**. Verify five topic subfolders exist with correct
> file counts.
>
> **19.** Verify all folders show “Private” in the Sharing column,
> Cowork did NOT alter any sharing settings.

![](./media/image30.png)

*OneDrive verification: all five topic subfolders confirmed.*

![](./media/image31.png)

*Archive subfolder: three correctly identified legacy files.*

![](./media/image32.png)

*Finance subfolder: VendorPricing correctly classified under Finance,
not Retail.*

![](./media/image33.png)

*Healthcare subfolder: 10 renamed clinical files consolidated.*

## Exercise 2: OneDrive and SharePoint governance audit

Audit the Lab Files folder for governance issues, duplicate files, stale
content, external-sharing risks, and ownership gaps. Produce a
structured audit report with recommendations, then execute one approved
action.

### Step 1 — Submit the governance-audit prompt

> **20.** In the same session from Exercise 1, enter the prompt below
> and send it:

[TABLE]

> **21.** The Workspace expands: three governance steps are appended to
> the existing seven (check sharing/permissions, analyse
> duplicates/staleness/ownership, produce audit report).
>
> **22.** Cowork confirms “I already have the inventory, hashes, and
> metadata from our earlier work”, no re-scanning needed. Sharing checks
> use read-only Graph calls, so no files are modified.

![](./media/image34.png)

*Transition: governance prompt queued in the message box.*

![](./media/image35.png)

*Prompt submitted: three governance steps appended to the existing
plan.*

![](./media/image36.png)

*Workspace at 7/10: sharing-permission checks running with read-only
tools.*

![](./media/image37.png)

*Parallel sharing checks: incremental audit building underway.*

![](./media/image38.png)

*Sharing scan complete: all 28 files confirmed owner-only.*

### Step 2 — Review the audit report

Read each section carefully before proceeding.

> • **Section 1 — Duplicate files (biggest issue):** three exact
> duplicates by byte-identical hash, plus two versioned near-duplicate
> pairs.
>
> • **Section 2 — Stale files:** archive candidates identified from
> filename-embedded dates (metadata dates were updated by the Exercise 1
> renames).
>
> • **Section 3 — External shares:** all 28 files show owner-only
> permissions (clean, no action needed).
>
> • **Section 4 — No clear owner:** LegacyPolicy and all 13 empty .xlsx
> placeholders flagged.
>
> • Read the *“Suggested next steps (on your go-ahead)”* numbered menu
> at the bottom.

![](./media/image39.png)

*Section 1 Duplicate files: exact and near-duplicate findings.*

![](./media/image40.png)

*Section 2 Stale files: honest metadata-date disclosure.*

![](./media/image41.png)

*Sections 2–4: sharing clean, ownership weak cases.*

![](./media/image42.png)

*Five recommended actions: numbered menu with deletion-staging
disclosure.*

### Step 3 — Execute one governance recommendation

> **23.** In the message box, type the number below to approve action
> \#2 (archive the 2024/2025/legacy items) and send it:

[TABLE]

> **24.** Cowork executes ONLY action \#2. Actions \#1, \#3, \#4, and
> \#5 stay pending, approving one does not authorise all.
>
> **25.** When complete, verify in OneDrive that the Archive subfolder
> now holds seven items (three pre-existing + four newly moved).
>
> **26.** Ask the responsible-AI question below and read Cowork's
> response:

[TABLE]

> **27.** Note Cowork's autonomy boundary: “Safe without approval” =
> read-only analysis only; “Needs human approval” = any action that
> changes state.

![](./media/image43.png)

*“2” sent: action \#2 only being executed, others remain pending.*

![](./media/image44.png)

*Archive action complete: seven legacy items now in the Archive
subfolder.*

![](./media/image45.png)

*OneDrive Archive folder: all seven items confirmed with timestamps.*

![](./media/image46.png)

*Responsible-AI question typed: proactive remaining-work surfacing.*

![](./media/image47.png)

*Responsible-AI question submitted: reasoning mode active.*

![](./media/image48.png)

*Responsible-AI framework: “Safe without approval” vs “Needs human
approval.”*

![](./media/image49.png)

*Framework complete: the Exercise 3 prompt is visible in the message
box.*

## Exercise 3: AI-generated Excel tracking and Teams reporting

Generate an Excel governance tracker with one row per file, then post a
three-line summary to Teams with a workbook link, demonstrating a
OneDrive -\> Excel -\> Teams cross-app workflow from a single
instruction.

### Step 1 — Submit the Excel and Teams prompt

> **28.** In the same session, enter the prompt below and send it:

[TABLE]

> **29.** In the Workspace, the Skills & Plugins section activates the
> Excel plugin alongside the existing Microsoft Graph permission.
>
> **30.** Cowork prepares the workbook while identifying the target
> Teams channel (“List teams”), both tasks run in parallel.
>
> **31.** A **Post to channel?** dialog appears, read the
> three-paragraph Teams message carefully before clicking Send.
>
> **32.** Verify the “Sent by Copilot Cowork” footer is included, this
> attribution is mandatory for all AI-generated Teams posts.

![](./media/image50.png)

*Exercise 3 begins: Excel plugin activates, Teams discovery runs in
parallel.*

![](./media/image51.png)

*Workbook generated; Teams post beginning, “Post to channel?” about to
appear.*

![](./media/image52.png)

*“Post to channel?” dialog: three-paragraph Teams message with AI
attribution.*

### Step 2 — Verify the workbook and Teams post

> **33.** Open **File Governance Tracker.xlsx** from the Workspace
> Output panel. Verify 28 rows (one per file) and six columns (File
> Name, Type, Topic, Last Modified, Sharing Status, Action Taken).
>
> **34.** Confirm yellow-highlighted rows identify duplicate/flagged
> files, these carry forward from the Exercise 2 analysis.
>
> **35.** Go to **Teams \> General channel** and verify the governance
> post is live with three paragraphs and the “Sent by Copilot Cowork”
> footer.
>
> **36.** Click the “Lab Files folder” hyperlink in the Teams post to
> confirm it opens the correct OneDrive location.
>
> **37.** The Workspace should show 12/12, all Exercise 3 steps
> complete.

![](./media/image53.png)

*File Governance Tracker.xlsx: open and verify all 28 rows.*

![](./media/image54.png)

*“Post to channel?” full dialog: Output + Skills + Always-allowed
shown.*

![](./media/image55.png)

*“Both done”: Workspace 12/12, workbook and Teams post confirmed.*

![](./media/image56.png)

*Teams General channel: governance post live with “Sent by Copilot
Cowork.”*

![](./media/image57.png)

*Teams post full view: three paragraphs with accurate governance data.*

![](./media/image58.png)

*Teams post permanent record: “Reply in thread” visible.*

![](./media/image59.png)

*Teams channel with compose box: ready for human replies.*

## Exercise 4: Healthcare documents reorganisation

Classify healthcare files by clinical business function, reorganise the
Healthcare folder into five clinical category subfolders using a
department-aware naming convention, and update the governance tracker
workbook.

### Step 1 — Review the Healthcare folder and classify

> **38.** Open **OneDrive \> My files \> Lab Files \> Renamed Files
> 2026-06-19 \> Healthcare**. Verify eight active clinical files are
> present (the two compliance/HIPAA files archived in Exercise 2 should
> not be here).
>
> **39.** Return to Cowork and enter the healthcare classification
> prompt below.

[TABLE]

> **40.** Read the classification table Cowork produces, it uses a real
> clinical taxonomy (HIM, Clinical Policy, Revenue Cycle,
> Quality/Safety, Clinical Engineering).
>
> **41.** When asked to choose between subfolder reorganisation or
> adding a tracker column, enter the follow-up below:

[TABLE]

> **42.** Watch Cowork regenerate the workbook as v2 with the new
> seven-column layout. Verify both v1 and v2 appear in the Workspace
> Output panel.

![](./media/image60.png)

*Healthcare folder: eight active files confirmed before Exercise 4.*

![](./media/image61.png)

*Transition: healthcare classification prompt queued.*

![](./media/image62.png)

*Healthcare classification table: standard clinical business-function
taxonomy.*

![](./media/image63.png)

*Classification continued: PHI awareness noted, user choice offered.*

![](./media/image64.png)

*“Add a Business Function column” instruction typed.*

![](./media/image65.png)

*Instruction sent: workbook regeneration begins.*

![](./media/image66.png)

*Workbook regeneration: three-step parallel validation running.*

![](./media/image67.png)

*Workbook v2 complete: cross-domain taxonomy applied to all 28 files.*

![](./media/image68.png)

*File Governance Tracker v2 open in Excel: seven-column layout.*

![](./media/image69.png)

*v2 completion summary: version-management transparency and follow-ups.*

![](./media/image70.png)

*v2 workbook summary with microphone-paused indicator.*

![](./media/image71.png)

*File Governance Tracker v2 full workbook view: all 28 rows.*

### Step 2 — Reorganise the Healthcare folder into five subfolders

[TABLE]

> **43.** Cowork finds your Healthcare folder and presents the full
> proposed plan, nothing has changed yet. Read all proposed renames
> carefully.
>
> **44.** Note that “(still an exact duplicate)” appears next to the
> InsuranceClaims v2 file, the duplicate flag from Exercise 2 carries
> forward.
>
> **45.** When ready, enter the single-word approval below. This
> triggers a new two-step plan: create five subfolders, then rename and
> move eight files.

[TABLE]

> **46.** When the completion banner appears, open **OneDrive \>
> Healthcare** to verify five category subfolders exist with the correct
> files in each.

![](./media/image72.png)

*Reorganisation plan: YYYY-MM-DD_Department_DocumentType format.*

![](./media/image73.png)

*Cowork searching for the Healthcare Documents folder.*

![](./media/image74.png)

*Folder found: proposed categorisation plan with duplicate
disambiguation.*

![](./media/image75.png)

*Proposed plan: Patient Care and Insurance Claims sections.*

![](./media/image76.png)

*Proposed plan: Medical Equipment, Administration, and “Three things to
confirm.”*

![](./media/image77.png)

*“proceed” typed: single-word approval triggers execution.*

![](./media/image78.png)

*New two-step plan (0/2): subfolder creation begins.*

![](./media/image79.png)

*Step 1/2 complete: five subfolders created, parallel rename batch
begins.*

![](./media/image80.png)

*Rename batch continuing: drive-alias workaround applied
systematically.*

![](./media/image81.png)

*Workspace 1/2: subfolders done, rename batch with progress indicators.*

![](./media/image82.png)

*2/2 complete: all eight healthcare files renamed and sorted, open items
noted.*

![](./media/image83.png)

*Healthcare folder reorganised: Exercise 4 complete.*

## Lab summary

You used Copilot Cowork to run a complete enterprise file-governance
workflow from natural-language prompts, applying AI classification with
a preview-before-action safety gate, a full governance audit across 28
files using cross-exercise memory, and a cross-app reporting workflow
spanning OneDrive, Excel, and Teams.

Key capabilities demonstrated:

> • **Multi-step workflow decomposition** — a natural-language prompt
> becomes a structured plan in the Workspace panel.
>
> • **Human-in-the-loop preview gates** — mandatory approval dialogs
> before every bulk operation.
>
> • **Progressive batch permission** — “Always allow Call graph” grants
> session-scoped consent for repeated Graph calls.
>
> • **Cross-exercise context retention** — Exercise 1 hashes and
> metadata reused in Exercises 2 and 4.
>
> • **Graceful failure isolation** — locked files are flagged and
> retried without aborting the batch.
>
> • **Responsible-AI self-articulation** — Cowork describes its own
> “safe vs needs-approval” boundary.
>
> • **Cross-app orchestration** — OneDrive data -\> Excel tracker -\>
> Teams communication.

## Validation checklist

> ☐ Exercise 1 — All 28 files were renamed with the
> YYYY-MM-DD_Topic_DocType convention and sorted into five topic
> subfolders under Renamed Files 2026-06-19.
>
> ☐ Exercise 1 — Every folder shows “Private” sharing; Cowork did not
> alter sharing settings.
>
> ☐ Exercise 2 — The four-section audit report was produced and only the
> approved action (#2, archive) was executed; the Archive subfolder
> holds seven items.
>
> ☐ Exercise 3 — File Governance Tracker.xlsx has 28 rows and six
> columns, and the three-paragraph Teams post is live with the “Sent by
> Copilot Cowork” footer.
>
> ☐ Exercise 4 — The tracker was regenerated as v2 (seven columns) and
> the Healthcare folder was reorganised into five clinical subfolders.

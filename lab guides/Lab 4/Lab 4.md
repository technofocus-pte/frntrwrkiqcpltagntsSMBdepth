LAB 4 Executive meeting coordinator

[TABLE]

**How to read this guide**

[TABLE]

**Lab overview**

In this lab you act as an executive's assistant and use Cowork to run a
meeting end to end. You will build an AI-generated prep brief from live
Calendar, Email, OneDrive / SharePoint, and Teams data and save it to
OneDrive; refine that brief in place with a Risks section; collect every
artefact for a meeting into a single Meeting Pack folder with a
hyperlinked index; and attempt post-meeting follow-up from a transcript.
Along the way you'll see how Cowork asks for approval before writing to
storage, discloses failures instead of hiding them, and refuses to
fabricate content when no source material exists.

By the end of the lab you will be able to:

> •Prompt Cowork to gather data from multiple M365 sources in parallel
> and produce a Word deliverable.
>
> •Approve, scope, and troubleshoot Cowork actions using approval and
> disambiguation cards.
>
> • Refine an existing document in place rather than creating
> duplicates.
>
> •Organise related files, emails, and chats into a structured Meeting
> Pack with an index.
>
> •Recognise correct grounding behaviour when source material is
> missing.

**Prerequisites**

> • Access to the lab M365 tenant, signed in with your lab credentials.
>
> •Cowork is available and you are on the Cowork tab, not Chat.
>
> • These skills and plugins are active: Word (docx skill), Calendar
> Management, Scheduling, OneDrive / SharePoint connector, Microsoft
> Graph API, Teams connector, and Transcript connector.
>
> •Outlook Calendar contains the Project Planning Workshop and Project
> Sync meetings used in Exercises 1 and 2.
>
> •OneDrive is accessible so Cowork can create the Lab Files and Meeting
> Pack folders. Do not pre-create them, Exercise 1 tests folder
> creation.
>
> • Word Online is available for opening and verifying the generated
> documents.
>
> •Completion of Labs 1–3 is recommended but not required.

**Exercise 1: AI-generated meeting preparation**

**Goal:** Build a cross-app meeting prep brief as a Word document saved
to the OneDrive Lab Files folder, with data gathered from Calendar,
Email, OneDrive / SharePoint, and Teams in parallel.

- Open your browser and go to **m365.cloud.microsoft** (or your
  organisation's M365 entry point). Sign in with your lab account.

> ![](./0fbc2d9fdb78238879bf3935c187cff86f7ff9cf.png "A screenshot of a computer
>
> AI-generated content may be incorrect.")
>
> ![](./f9cd79b1dcc65b9d99ef7867b62a150793d8fd1d.png "A screenshot of a login box
>
> AI-generated content may be incorrect.")
>
> ![](./7fd48db773983127b47e2d5107175ac9266addad.png "A screenshot of a login screen
>
> AI-generated content may be incorrect.")

- Click Yes to stay signed in.

> ![](./70e1fccbb8b023ba36d3d0b5638faee1f3f9a18e.png "A screenshot of a computer screen
>
> AI-generated content may be incorrect.")

**Step 1 — Send the preparation prompt**

1.  Go to the Cowork tab (not Chat).

![](./media/18e84db2ace698b5322d1e215a10753eb497bf2a.png)

*The Cowork tab, ready for a new task.*

2.  In the prompt bar, type the prompt below and press **Enter**:

[TABLE]

![](./media/c41e0b600d5d2aa93dd5c71afdf19fdafd13ef35.png)

*Prompt submitted, Cowork begins processing.*

3.  Cowork auto-names the session and shows “Narrowing down the
    approach” before opening the Workspace panel.

![](./media/67fb4b554b340ba79e9a36f91679d35f3013690e.png)

*Workspace opens, Step 1 complete, calendar accessed.*

Cowork read Outlook Calendar and found “Project Planning Workshop today,
8:00 AM–12:00 PM UTC.” The plan is still expanding.

![](./media/24ddea3298012db3f1c21c42801c8f48b4e21ba2.png)

*The plan expands to five steps, parallel lookups begin.*

4.  Steps 2–4 (attendee profile, emails and files, transcripts) run in
    parallel; step 5 (document build) waits for all data.

![](./media/a94870cb5f85365e19a57c6e9be8d819f727b9db.png)

*Data gathering complete, transitioning to the document build.*

5.  Cowork notes the “Lab Files” folder doesn't exist yet and will
    create it rather than fail.

**Step 2 — Approve folder creation**

1.  A **Create folder?** card appears. Click **Create** to approve.

[TABLE]

![](./media/7a71d134cb560df6a7165b98cb6e636d51698bee.png)

*Approval card: “Create folder?” for Lab Files in OneDrive.*

2.  Cowork requests approval before writing to OneDrive and confirms the
    exact folder name from your prompt. This approve-before-write
    pattern means Cowork never modifies storage silently.

3.  Click **Create** to proceed.

![](./media/d59faeef3b78b832a2c96beaed40743d263dfddb.png)

*Cursor on the Create button, about to approve.*

![](./media/2d54dad8d7b8e1fded6a89c8e57bcf8c6fddf22f.png)

*Folder created, the Word plugin activates.*

4.  “Approved 1 action” confirms the Lab Files folder was created, and
    the Word plugin activates, required to generate the .docx.

**Step 3 — Watch the document build**

1.  Cowork now builds the Word document. No action is required, just
    observe the sequence.

![](./media/7a72bfdda9146ae1f66e05980df0da2796c7b6d9.png)

*Word document build starts, the agent narrates its plan.*

2.  Cowork uses a two-phase approach: it writes a content plan, then
    executes it to produce the .docx.

![](./media/fb2cbf6dffde88b14a64600aa33b37d79bfbea86.png)

*Folder confirmed, Word build in progress.*

![](./media/1a751a50330b0dbfe1da3e238d7b8bf851c99517.png)

*Four parallel sub-tasks enumerated.*

3.  Cowork lists four lookups (attendee, emails and files, transcripts,
    Teams chats) and confirms it is the meeting organiser.

![](./media/d02c2ba5462a5ef79c9d7f6e59dca1728e79f583.png)

*First parallel batch complete, deeper email search begins.*

4.  Three connectors ran simultaneously: Directory, Email + Files, and
    Outlook. Cowork now reads full email bodies.

![](./media/2c53dc348fcb16756085b6bd8b4bbbcb9a6bd7a8.png)

*Deepest data layer, email bodies, Teams chats, and transcripts.*

5.  Four simultaneous calls run. Empty transcript results are expected
    in a sandbox.

![](./media/14d3323507a75901400e0767e4b4c20427faa5a0.png)

*Build error detected and self-corrected, spacing optimised.*

6.  Cowork self-corrected a syntax error, then detected a two-page spill
    and began reducing spacing to meet the one-page requirement.

![](./media/e56f8a07dc58a4e56c3c41fcfe28d7ea57441200.png)

*Second round of spacing reduction, document close to one page.*

7.  Cowork targets the exact overflow elements (the alert box and
    questions table) for margin reduction.

![](./media/e51969c72550910ae2be7f014469375fa83ea204.png)

*Final fixes, smart quotes, trailing spacer, upload preparation.*

8.  Three quality fixes: questions shortened, smart quotes converted to
    ASCII, and the trailing blank spacer removed. The file is then
    encoded for upload.

**Step 4 — Approve the upload and open the brief**

1.  A **Use Microsoft Graph?** card appears. Click **Approve** to upload
    the document to OneDrive.

[TABLE]

![](./media/724f8b6b26e76c505fc331a4ca50797671bf12de.png)

*Upload approval card: “Use Microsoft Graph?” to save to Lab Files.*

2.  Every file write to OneDrive requires this approval. “Always allow”
    pre-approves future Graph calls this session.

![](./media/66b01ee548992b3665655cb0b0b0618dec4e78b9.png)

*Upload failed, document still accessible via the link card.*

3.  The upload failed due to sandbox permissions. The document is still
    reachable via the link card in the chat, Cowork reports the failure
    transparently rather than pretending it succeeded.

4.  Click the document link card to open the prep brief in Word Online
    and verify all sections.

![](./media/88264c416b56ae26a24aa3f3c07d5fcadb7cb479.png)

*Word Online, the completed prep brief.*

5.  All five sections are populated with real M365 data: Meeting
    Details, Attendees, Emails, Files, and 3 Questions.

![](./media/178900262459d6609c9ddc1b7a87f7e6898a1c8e.png)

*Cowork shows the 3 questions and a heads-up alert.*

6.  The three questions are grounded in the meeting's stated purpose.
    The heads-up alert proactively flags an invite bounce, a risk Cowork
    surfaced from email data without being asked.

![](./media/3bf14c6aabea9f47c525ad38d6ecedd9d0887403.png)

*The Word document's lower sections.*

7.  The Attendees table shows the last interaction, Related Emails shows
    the invitation and bounce notice, Related Files honestly reports “No
    related files found,” and the question table is present.

**Step 5 — Refine the brief in place (add a Risks section)**

1.  Send the refinement prompt below:

[TABLE]

![](./media/176e581e2a87622810f2ab100dfea40a88828a2e.png)

*Refinement prompt typed and ready to send.*

2.  This tests whether Cowork updates the existing document or creates a
    duplicate. No Risks section exists yet.

![](./media/4190a457b873be7432e428b24a41879224eaab0e.png)

*Refinement submitted, Cowork re-analyses email threads.*

3.  Cowork reuses the threads already gathered, no new API calls needed.
    The document stays unchanged while the update is prepared.

![](./media/db3ee4060113bb5ecbc2f330557165b18b3af127.png)

*The document before the update.*

It ends with “3 Questions to Ask,” Page 1 of 1, a useful before/after
comparison point.

![](./media/0e0e01bbfb8a37b0e8562aab43eda4a16bc8d711.png)

*Risks section added, grounded content confirmed.*

4.  The Risks / Blockers section is added with one grounded finding (the
    invite bounce). The document still fits on one page and was updated
    in place, not duplicated.

**Step 6 — Move the updated file to Lab Files**

1.  Send the prompt below:

[TABLE]

![](./media/02d2363c4717b2f9fd1e33b44c40ec94ccdf6c8d.png)

*Move prompt typed and sent.*

2.  Cowork must interpret “updated word file” as a specific OneDrive
    file ID, verify it contains the Risks section, then present an
    approval card.

![](./media/b9321c2913ba6de2743e80c9a7d2b9ea054eced1.png)

*Cowork searches OneDrive to locate the correct version.*

3.  It gets the OneDrive root path and searches by filename, selecting
    the updated file over the original.

4.  **Use Microsoft Graph?** card appears for the move. Click
    **Approve**.

![](./media/8f47ca9c45afeb42b4decd646952fcc0b09cdf27.png)

*File verified, “Use Microsoft Graph?” card for the move.*

5.  Cowork confirmed the file contains the Risks section before
    requesting the move.

![](./media/14417f787233888890455723897e34343b732c4e.png)

*Move blocked twice, Cowork pivots to a copy operation.*

6.  The move API was blocked by sandbox restrictions. Cowork reports
    both failures and autonomously falls back to a copy, no user input
    needed.

![](./media/606670fb9cff22ca60affadf4c2939aa83115a87.png)

*Copy succeeds, file verified in the Lab Files folder.*

7.  Cowork verifies the file appears in Lab Files by listing folder
    contents before confirming success.

![](./media/abb3bc11b414da5ea339109c8b20caa580fb2404.png)

*Housekeeping note about two copies.*

8.  Cowork discloses that a second copy remains in the working folder
    and honestly notes it cannot delete it from here.

![](./media/7b7a5c4edb0c764629a4143d755126b39872401b.png)

*Document thumbnail, v2 file confirmed in the Output panel.*

9.  The Output panel shows two files: v2 (with Risks) and the original.
    Use the v2 link to open the final document.

10. Open **OneDrive \> My files** and verify the Lab Files folder exists
    with one item.

![](./media/b248abdcbe1bdc94cd40c6ae5dac778bcb71820e.png)

*OneDrive web view, Lab Files folder with one item.*

11. External verification that the Cowork workflow produced a real,
    accessible OneDrive folder.

![](./media/58858fab6e4dcc0c0ad1665a2bff0cdd78e3141a.png)

*Two-file status table, v2 is correct, original is outdated.*

12. Cowork provides a clear status table: v2 (with Risks) is the correct
    file; the original is outdated. Click the v2 link.

![](./media/1058559671f4a90760cc36d13c4405b09069cf82.png)

*Word Online, the Risks / Blockers section in the final document.*

13. The Risks / Blockers section shows Blocker, Source (the actual email
    subject), and Recommended Action. Page 1 of 1, the one-page
    constraint is maintained. Exercise 1 complete.

**Exercise 2: Collect documents, emails, and action items**

**Goal:** Gather all content related to the Project Sync meeting and
organise it into a Meeting Pack folder in OneDrive with a hyperlinked
index document.

**Step 1 — Send the collection prompt**

1.  Send the prompt below:

[TABLE]

![](./media/6347fa3cbd7d295a2af71b438aad58b0eae5fe26.png)

*Exercise 2 prompt typed and ready to send.*

2.  This gathers content from four M365 sources and produces a
    hyperlinked index. The two Exercise 1 output files carry over in the
    Workspace panel.

![](./media/3c0aa11f29f1953b18b2dd2d4934ed0a0237272e.png)

*A new four-step Workspace plan, parallel search launched.*

3.  Cowork searches Outlook for the Project Sync event and Files +
    Email + Teams for related content. Graph API permissions from
    Exercise 1 carry over.

![](./media/eb08d85edd386720b258279bd9290026a278df95.png)

*Project Sync identified, false positives detected, deeper search
initiated.*

4.  Project Sync is found (June 23, 9:00–9:45 AM UTC). The initial
    search returned loose keyword matches, so Cowork flags the quality
    issue and deepens the search rather than filling the pack with
    irrelevant results.

**Step 2 — Scope the pack**

1.  A **Pack scope** card appears. Select option 1, **Project planning
    work**.

![](./media/a1b9458b86f4a006088f8380a6308864a6ee7152.png)

*Scope disambiguation card, three options for pack content.*

2.  “Project Sync” is too generic, Cowork found two content clusters and
    presents options rather than guessing. It also reports that open
    tasks couldn't be retrieved due to a permission gap.

- Confirm option 1 is selected (filled badge), then click **Submit**.

![](./media/da295cd196b2e71339f1d66ca074f17687f6c5fa.png)

*Option 1 selected: “Project planning work” scoped.*

3.  The pack will include the prep doc with Risks, the invitation and
    bounce emails, and the Teams chat. Active sales-deal threads are
    correctly excluded as unrelated.

**Step 3 — Approve the folder and build the index**

1.  A **Create folder?** card appears. Click **Create** to approve the
    Meeting Pack folder.

![](./media/65e14b77027db9609ea8fc1447c48028b8f342a8.png)

*“Create folder?” card for Meeting Pack – Project Sync.*

2.  Same folder-creation pattern as Exercise 1. Both Graph API
    permissions from Exercise 1 remain active.

![](./media/13ac1adc15597b8c4d6f2d8d5583337de16158ce.png)

*Meeting Pack folder created, prep brief being copied in.*

Cowork correctly selects the v2 prep brief (with Risks) to copy in,
demonstrating cross-exercise memory.

![](./media/24e7097b237fb485d7d888ebf8552493e46e257f.png)

*Step 3 complete, index-document creation starts.*

3.  Cowork waits for OneDrive sync confirmation before generating
    hyperlinks, so all links point to verified locations.

![](./media/26fab6a29c67f98947afe0412d54c1b67a5cdbb3.png)

*All four steps complete, a 5-item index confirmed with caveats.*

4.  The index links to five items with honest caveats (task-permission
    gap, scope limit). Cowork also flags two action items: the bounced
    invite and missing Project Sync attendees.

**Step 4 — Verify the index document**

1.  Click the Meeting Pack index link to open it in Word Online. Verify
    the first three rows and test the hyperlinks.

![](./media/2afa7b8b2a4cb625c1ef31666c4d9c3a5c6f2f5f.png)

*Word Online, the Meeting Pack index, first three items.*

The header shows “Meeting Pack – Index” with meeting details. Items 1–3
(calendar event, prep brief, invitation email) have hyperlinks and
source-type labels.

![](./media/5a6ab0ba25b1d4b8b0ae1480ff22912ef3444a18.png)

*Word Online, the complete index with all five items and Notes &
Coverage.*

2.  All five items have hyperlinks, source labels, and one-line
    descriptions. The Notes & Coverage section documents the
    task-permission gap, the scope limit, and the bounced-invite action.
    Page 1 of 1. Exercise 2 complete.

**Exercise 3: Post-meeting follow-up automation**

**Goal:** Generate a meeting summary, action items, follow-up email, and
tasks from a transcript. This demonstrates AI grounding, refusing to
fabricate content when no source material exists.

**Step 1 — Send the follow-up prompt**

1.  Send the prompt below:

[TABLE]

![](./media/3680805b10c43e9cdb5df94c816010c921518fcc.png)

*Exercise 3 prompt typed and ready to send.*

2.  The “Show me everything for review” safeguard tests whether Cowork
    defers all actions pending approval. Cowork will first search for a
    transcript.

![](./media/caf4d5e568f173c000b823c0d43692379598c313.png)

*Grounding enforced: “I won't invent meeting content.”*

3.  Cowork enforces grounding immediately: before writing anything it
    needs the actual transcript or notes. It searches for transcripts,
    finds none, then widens the search to notes files.

![](./media/8c6837b291574cc6588e23462e2781fc88234205.png)

*Complete refusal with three constructive forward paths.*

4.  After an exhaustive search, Cowork confirms no source material
    exists and declines to fabricate. It offers three alternatives:
    paste notes into chat, re-run after the meeting with transcription
    on, or point to a different meeting that has a transcript.

**Step 2 — Test in-loop correction**

1.  Send a correction to see how Cowork handles it when no output exists
    yet:

[TABLE]

![](./media/9e8127d3cfe4934027e71034bc6567d63b666377.png)

*Correction pre-registered, honest state disclosure.*

2.  Cowork acknowledges the correction and honestly discloses that no
    action items have been generated yet, so there is nothing to
    correct. The correction is pre-registered for when notes are
    provided. Exercise 3 complete.

**Validation checklist**

Confirm every item against your actual Cowork session.

> ☐ Exercise 1 — A prep brief exists as a Word file in the OneDrive Lab
> Files folder, combining calendar, email, and file context. The Risks /
> Blockers section is present and grounded in a real email thread.
>
> ☐ Exercise 1 — The document was updated, not duplicated, when the
> Risks section was added. Only one new section was inserted.
>
> ☐ Exercise 2 — A Meeting Pack folder with a working index exists in
> OneDrive. The index links to five items with source labels and
> one-line descriptions.
>
> ☐ Exercise 2 — The Notes & Coverage section honestly documents what
> was omitted and why (task-permission gap, scope limit).
>
> ☐Exercise 3 — Cowork refused to fabricate meeting content and stated
> it would not invent decisions. Three constructive alternatives were
> offered.
>
> ☐ Exercise 3 — The action-item correction was acknowledged and
> pre-registered, without creating phantom corrected outputs.

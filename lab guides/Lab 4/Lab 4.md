LAB 4 Executive meeting coordinator

|  |  |
|----|----|
| **Estimated time** | 20 minutes |
| **Objective** | Automate the full meeting lifecycle: AI-generated preparation, cross-app content collection, and post-meeting follow-up, all grounded in real M365 data. |
| **Skills & plugins** | Word (docx skill), Calendar Management, Scheduling, OneDrive / SharePoint connector, Microsoft Graph API, Teams connector, Transcript connector. |

**How to read this guide**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr>
<td><p><strong>PROMPT</strong></p>
<p>Type or paste into Cowork.</p></td>
<td><p><strong>FOLLOW-UP</strong></p>
<p>A prompt sent in the same task.</p></td>
<td><p><strong>CORRECTION</strong></p>
<p>A prompt that fixes something.</p></td>
</tr>
<tr>
<td><p><strong>NOTE</strong></p>
<p>Useful context to know.</p></td>
<td><p><strong>TIP</strong></p>
<p>An optional shortcut or extra.</p></td>
<td><p><strong>IMPORTANT</strong></p>
<p>Do this to avoid an error.</p></td>
</tr>
</tbody>
</table>

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

> <img src="media/0fbc2d9fdb78238879bf3935c187cff86f7ff9cf.png"
> title="A screenshot of a computer
>
> AI-generated content may be incorrect."
> style="width:6.5in;height:3.84375in" />
>
> <img src="media/f9cd79b1dcc65b9d99ef7867b62a150793d8fd1d.png"
> title="A screenshot of a login box
>
> AI-generated content may be incorrect."
> style="width:6.5in;height:4.13542in" />
>
> <img src="media/7fd48db773983127b47e2d5107175ac9266addad.png"
> title="A screenshot of a login screen
>
> AI-generated content may be incorrect."
> style="width:6.5in;height:4.5625in" />

- Click Yes to stay signed in.

> <img src="media/70e1fccbb8b023ba36d3d0b5638faee1f3f9a18e.png"
> title="A screenshot of a computer screen
>
> AI-generated content may be incorrect."
> style="width:6.5in;height:5.5625in" />

**Step 1 — Send the preparation prompt**

1.  Go to the Cowork tab (not Chat).

<img src="media/media/18e84db2ace698b5322d1e215a10753eb497bf2a.png"
style="width:5.60417in;height:3.70833in" />

*The Cowork tab, ready for a new task.*

2.  In the prompt bar, type the prompt below and press **Enter**:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr>
<td><strong>PROMPT · BUILD PREP BRIEF</strong></td>
</tr>
<tr>
<td><p>Prepare me for my next meeting. Build a one-page prep brief
containing:</p>
<p>attendee list with my last interaction with each, the stated
purpose,</p>
<p>related email threads and files, open action items from previous
related</p>
<p>meetings, and 3 questions I should ask. Save it as a Word document in
my</p>
<p>'Lab Files' folder named 'Prep - June 19, 2026 - Project Planning
Workshop'.</p></td>
</tr>
</tbody>
</table>

<img src="media/media/c41e0b600d5d2aa93dd5c71afdf19fdafd13ef35.png"
style="width:5.60417in;height:3.75in" />

*Prompt submitted, Cowork begins processing.*

3.  Cowork auto-names the session and shows “Narrowing down the
    approach” before opening the Workspace panel.

<img src="media/media/67fb4b554b340ba79e9a36f91679d35f3013690e.png"
style="width:5.60417in;height:3.80208in" />

*Workspace opens, Step 1 complete, calendar accessed.*

Cowork read Outlook Calendar and found “Project Planning Workshop today,
8:00 AM–12:00 PM UTC.” The plan is still expanding.

<img src="media/media/24ddea3298012db3f1c21c42801c8f48b4e21ba2.png"
style="width:5.60417in;height:2.70833in" />

*The plan expands to five steps, parallel lookups begin.*

4.  Steps 2–4 (attendee profile, emails and files, transcripts) run in
    parallel; step 5 (document build) waits for all data.

<img src="media/media/a94870cb5f85365e19a57c6e9be8d819f727b9db.png"
style="width:5.60417in;height:2.71875in" />

*Data gathering complete, transitioning to the document build.*

5.  Cowork notes the “Lab Files” folder doesn't exist yet and will
    create it rather than fail.

**Step 2 — Approve folder creation**

1.  A **Create folder?** card appears. Click **Create** to approve.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr>
<td><p><strong>▲ IMPORTANT</strong></p>
<p>Do NOT type in the message bar while an approval card is open, it
cancels the action.</p></td>
</tr>
</tbody>
</table>

<img src="media/media/7a71d134cb560df6a7165b98cb6e636d51698bee.png"
style="width:5.60417in;height:2.70833in" />

*Approval card: “Create folder?” for Lab Files in OneDrive.*

2.  Cowork requests approval before writing to OneDrive and confirms the
    exact folder name from your prompt. This approve-before-write
    pattern means Cowork never modifies storage silently.

3.  Click **Create** to proceed.

<img src="media/media/d59faeef3b78b832a2c96beaed40743d263dfddb.png"
style="width:5.60417in;height:2.73958in" />

*Cursor on the Create button, about to approve.*

<img src="media/media/2d54dad8d7b8e1fded6a89c8e57bcf8c6fddf22f.png"
style="width:5.60417in;height:2.67708in" />

*Folder created, the Word plugin activates.*

4.  “Approved 1 action” confirms the Lab Files folder was created, and
    the Word plugin activates, required to generate the .docx.

**Step 3 — Watch the document build**

1.  Cowork now builds the Word document. No action is required, just
    observe the sequence.

<img src="media/media/7a72bfdda9146ae1f66e05980df0da2796c7b6d9.png"
style="width:5.60417in;height:2.6875in" />

*Word document build starts, the agent narrates its plan.*

2.  Cowork uses a two-phase approach: it writes a content plan, then
    executes it to produce the .docx.

<img src="media/media/fb2cbf6dffde88b14a64600aa33b37d79bfbea86.png"
style="width:5.60417in;height:2.70833in" />

*Folder confirmed, Word build in progress.*

<img src="media/media/1a751a50330b0dbfe1da3e238d7b8bf851c99517.png"
style="width:5.60417in;height:2.69792in" />

*Four parallel sub-tasks enumerated.*

3.  Cowork lists four lookups (attendee, emails and files, transcripts,
    Teams chats) and confirms it is the meeting organiser.

<img src="media/media/d02c2ba5462a5ef79c9d7f6e59dca1728e79f583.png"
style="width:5.60417in;height:2.70833in" />

*First parallel batch complete, deeper email search begins.*

4.  Three connectors ran simultaneously: Directory, Email + Files, and
    Outlook. Cowork now reads full email bodies.

<img src="media/media/2c53dc348fcb16756085b6bd8b4bbbcb9a6bd7a8.png"
style="width:5.60417in;height:2.69792in" />

*Deepest data layer, email bodies, Teams chats, and transcripts.*

5.  Four simultaneous calls run. Empty transcript results are expected
    in a sandbox.

<img src="media/media/14d3323507a75901400e0767e4b4c20427faa5a0.png"
style="width:5.60417in;height:2.67708in" />

*Build error detected and self-corrected, spacing optimised.*

6.  Cowork self-corrected a syntax error, then detected a two-page spill
    and began reducing spacing to meet the one-page requirement.

<img src="media/media/e56f8a07dc58a4e56c3c41fcfe28d7ea57441200.png"
style="width:5.60417in;height:2.66667in" />

*Second round of spacing reduction, document close to one page.*

7.  Cowork targets the exact overflow elements (the alert box and
    questions table) for margin reduction.

<img src="media/media/e51969c72550910ae2be7f014469375fa83ea204.png"
style="width:5.60417in;height:2.69792in" />

*Final fixes, smart quotes, trailing spacer, upload preparation.*

8.  Three quality fixes: questions shortened, smart quotes converted to
    ASCII, and the trailing blank spacer removed. The file is then
    encoded for upload.

**Step 4 — Approve the upload and open the brief**

1.  A **Use Microsoft Graph?** card appears. Click **Approve** to upload
    the document to OneDrive.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr>
<td><p><strong>▲ IMPORTANT</strong></p>
<p>Do NOT type in the message bar while the card is open.</p></td>
</tr>
</tbody>
</table>

<img src="media/media/724f8b6b26e76c505fc331a4ca50797671bf12de.png"
style="width:5.60417in;height:2.70833in" />

*Upload approval card: “Use Microsoft Graph?” to save to Lab Files.*

2.  Every file write to OneDrive requires this approval. “Always allow”
    pre-approves future Graph calls this session.

<img src="media/media/66b01ee548992b3665655cb0b0b0618dec4e78b9.png"
style="width:5.60417in;height:2.72917in" />

*Upload failed, document still accessible via the link card.*

3.  The upload failed due to sandbox permissions. The document is still
    reachable via the link card in the chat, Cowork reports the failure
    transparently rather than pretending it succeeded.

4.  Click the document link card to open the prep brief in Word Online
    and verify all sections.

<img src="media/media/88264c416b56ae26a24aa3f3c07d5fcadb7cb479.png"
style="width:5.60417in;height:2.77083in" />

*Word Online, the completed prep brief.*

5.  All five sections are populated with real M365 data: Meeting
    Details, Attendees, Emails, Files, and 3 Questions.

<img src="media/media/178900262459d6609c9ddc1b7a87f7e6898a1c8e.png"
style="width:5.60417in;height:2.71875in" />

*Cowork shows the 3 questions and a heads-up alert.*

6.  The three questions are grounded in the meeting's stated purpose.
    The heads-up alert proactively flags an invite bounce, a risk Cowork
    surfaced from email data without being asked.

<img src="media/media/3bf14c6aabea9f47c525ad38d6ecedd9d0887403.png"
style="width:5.60417in;height:2.69792in" />

*The Word document's lower sections.*

7.  The Attendees table shows the last interaction, Related Emails shows
    the invitation and bounce notice, Related Files honestly reports “No
    related files found,” and the question table is present.

**Step 5 — Refine the brief in place (add a Risks section)**

1.  Send the refinement prompt below:

|  |
|----|
| **PROMPT · REFINE** |
| Add a Risks section listing anything in the email threads that sounds like a blocker. |

<img src="media/media/176e581e2a87622810f2ab100dfea40a88828a2e.png"
style="width:5.60417in;height:2.69792in" />

*Refinement prompt typed and ready to send.*

2.  This tests whether Cowork updates the existing document or creates a
    duplicate. No Risks section exists yet.

<img src="media/media/4190a457b873be7432e428b24a41879224eaab0e.png"
style="width:5.60417in;height:2.66667in" />

*Refinement submitted, Cowork re-analyses email threads.*

3.  Cowork reuses the threads already gathered, no new API calls needed.
    The document stays unchanged while the update is prepared.

<img src="media/media/db3ee4060113bb5ecbc2f330557165b18b3af127.png"
style="width:5.60417in;height:2.51042in" />

*The document before the update.*

It ends with “3 Questions to Ask,” Page 1 of 1, a useful before/after
comparison point.

<img src="media/media/0e0e01bbfb8a37b0e8562aab43eda4a16bc8d711.png"
style="width:5.60417in;height:2.75in" />

*Risks section added, grounded content confirmed.*

4.  The Risks / Blockers section is added with one grounded finding (the
    invite bounce). The document still fits on one page and was updated
    in place, not duplicated.

**Step 6 — Move the updated file to Lab Files**

1.  Send the prompt below:

|                                            |
|--------------------------------------------|
| **PROMPT · MOVE FILE**                     |
| move updated word file to lab files folder |

<img src="media/media/02d2363c4717b2f9fd1e33b44c40ec94ccdf6c8d.png"
style="width:5.60417in;height:2.69792in" />

*Move prompt typed and sent.*

2.  Cowork must interpret “updated word file” as a specific OneDrive
    file ID, verify it contains the Risks section, then present an
    approval card.

<img src="media/media/b9321c2913ba6de2743e80c9a7d2b9ea054eced1.png"
style="width:5.60417in;height:2.65625in" />

*Cowork searches OneDrive to locate the correct version.*

3.  It gets the OneDrive root path and searches by filename, selecting
    the updated file over the original.

4.  **Use Microsoft Graph?** card appears for the move. Click
    **Approve**.

<img src="media/media/8f47ca9c45afeb42b4decd646952fcc0b09cdf27.png"
style="width:5.60417in;height:2.70833in" />

*File verified, “Use Microsoft Graph?” card for the move.*

5.  Cowork confirmed the file contains the Risks section before
    requesting the move.

<img src="media/media/14417f787233888890455723897e34343b732c4e.png"
style="width:5.60417in;height:2.69792in" />

*Move blocked twice, Cowork pivots to a copy operation.*

6.  The move API was blocked by sandbox restrictions. Cowork reports
    both failures and autonomously falls back to a copy, no user input
    needed.

<img src="media/media/606670fb9cff22ca60affadf4c2939aa83115a87.png"
style="width:5.60417in;height:2.70833in" />

*Copy succeeds, file verified in the Lab Files folder.*

7.  Cowork verifies the file appears in Lab Files by listing folder
    contents before confirming success.

<img src="media/media/abb3bc11b414da5ea339109c8b20caa580fb2404.png"
style="width:5.60417in;height:2.71875in" />

*Housekeeping note about two copies.*

8.  Cowork discloses that a second copy remains in the working folder
    and honestly notes it cannot delete it from here.

<img src="media/media/7b7a5c4edb0c764629a4143d755126b39872401b.png"
style="width:5.60417in;height:2.71875in" />

*Document thumbnail, v2 file confirmed in the Output panel.*

9.  The Output panel shows two files: v2 (with Risks) and the original.
    Use the v2 link to open the final document.

10. Open **OneDrive \> My files** and verify the Lab Files folder exists
    with one item.

<img src="media/media/b248abdcbe1bdc94cd40c6ae5dac778bcb71820e.png"
style="width:5.60417in;height:2.72917in" />

*OneDrive web view, Lab Files folder with one item.*

11. External verification that the Cowork workflow produced a real,
    accessible OneDrive folder.

<img src="media/media/58858fab6e4dcc0c0ad1665a2bff0cdd78e3141a.png"
style="width:5.60417in;height:2.76042in" />

*Two-file status table, v2 is correct, original is outdated.*

12. Cowork provides a clear status table: v2 (with Risks) is the correct
    file; the original is outdated. Click the v2 link.

<img src="media/media/1058559671f4a90760cc36d13c4405b09069cf82.png"
style="width:5.60417in;height:2.625in" />

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

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr>
<td><strong>PROMPT · BUILD MEETING PACK</strong></td>
</tr>
<tr>
<td><p>For the Project Sync meeting, gather everything related: files
in</p>
<p>OneDrive/SharePoint, email threads, Teams messages, and any open
tasks.</p>
<p>Organise them into a single 'Meeting Pack' folder in OneDrive and
give me</p>
<p>an index document linking to each item with a one-line
description.</p></td>
</tr>
</tbody>
</table>

<img src="media/media/6347fa3cbd7d295a2af71b438aad58b0eae5fe26.png"
style="width:5.60417in;height:2.71875in" />

*Exercise 2 prompt typed and ready to send.*

2.  This gathers content from four M365 sources and produces a
    hyperlinked index. The two Exercise 1 output files carry over in the
    Workspace panel.

<img src="media/media/3c0aa11f29f1953b18b2dd2d4934ed0a0237272e.png"
style="width:5.60417in;height:2.625in" />

*A new four-step Workspace plan, parallel search launched.*

3.  Cowork searches Outlook for the Project Sync event and Files +
    Email + Teams for related content. Graph API permissions from
    Exercise 1 carry over.

<img src="media/media/eb08d85edd386720b258279bd9290026a278df95.png"
style="width:5.60417in;height:2.69792in" />

*Project Sync identified, false positives detected, deeper search
initiated.*

4.  Project Sync is found (June 23, 9:00–9:45 AM UTC). The initial
    search returned loose keyword matches, so Cowork flags the quality
    issue and deepens the search rather than filling the pack with
    irrelevant results.

**Step 2 — Scope the pack**

1.  A **Pack scope** card appears. Select option 1, **Project planning
    work**.

<img src="media/media/a1b9458b86f4a006088f8380a6308864a6ee7152.png"
style="width:5.60417in;height:2.6875in" />

*Scope disambiguation card, three options for pack content.*

2.  “Project Sync” is too generic, Cowork found two content clusters and
    presents options rather than guessing. It also reports that open
    tasks couldn't be retrieved due to a permission gap.

- Confirm option 1 is selected (filled badge), then click **Submit**.

<img src="media/media/da295cd196b2e71339f1d66ca074f17687f6c5fa.png"
style="width:5.60417in;height:2.6875in" />

*Option 1 selected: “Project planning work” scoped.*

3.  The pack will include the prep doc with Risks, the invitation and
    bounce emails, and the Teams chat. Active sales-deal threads are
    correctly excluded as unrelated.

**Step 3 — Approve the folder and build the index**

1.  A **Create folder?** card appears. Click **Create** to approve the
    Meeting Pack folder.

<img src="media/media/65e14b77027db9609ea8fc1447c48028b8f342a8.png"
style="width:5.60417in;height:2.69792in" />

*“Create folder?” card for Meeting Pack – Project Sync.*

2.  Same folder-creation pattern as Exercise 1. Both Graph API
    permissions from Exercise 1 remain active.

<img src="media/media/13ac1adc15597b8c4d6f2d8d5583337de16158ce.png"
style="width:5.60417in;height:2.72917in" />

*Meeting Pack folder created, prep brief being copied in.*

Cowork correctly selects the v2 prep brief (with Risks) to copy in,
demonstrating cross-exercise memory.

<img src="media/media/24e7097b237fb485d7d888ebf8552493e46e257f.png"
style="width:5.60417in;height:2.71875in" />

*Step 3 complete, index-document creation starts.*

3.  Cowork waits for OneDrive sync confirmation before generating
    hyperlinks, so all links point to verified locations.

<img src="media/media/26fab6a29c67f98947afe0412d54c1b67a5cdbb3.png"
style="width:5.60417in;height:2.71875in" />

*All four steps complete, a 5-item index confirmed with caveats.*

4.  The index links to five items with honest caveats (task-permission
    gap, scope limit). Cowork also flags two action items: the bounced
    invite and missing Project Sync attendees.

**Step 4 — Verify the index document**

1.  Click the Meeting Pack index link to open it in Word Online. Verify
    the first three rows and test the hyperlinks.

<img src="media/media/2afa7b8b2a4cb625c1ef31666c4d9c3a5c6f2f5f.png"
style="width:5.60417in;height:2.6875in" />

*Word Online, the Meeting Pack index, first three items.*

The header shows “Meeting Pack – Index” with meeting details. Items 1–3
(calendar event, prep brief, invitation email) have hyperlinks and
source-type labels.

<img src="media/media/5a6ab0ba25b1d4b8b0ae1480ff22912ef3444a18.png"
style="width:5.60417in;height:2.72917in" />

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

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr>
<td><strong>PROMPT · POST-MEETING FOLLOW-UP</strong></td>
</tr>
<tr>
<td><p>From this meeting's transcript/notes: (1) write a crisp summary
with</p>
<p>decisions made, (2) extract action items with owner and due date, (3)
draft</p>
<p>a follow-up email to all attendees, and (4) create tasks for the
items</p>
<p>assigned to me. Show me everything for review before creating or
sending</p>
<p>anything.</p></td>
</tr>
</tbody>
</table>

<img src="media/media/3680805b10c43e9cdb5df94c816010c921518fcc.png"
style="width:5.60417in;height:2.69792in" />

*Exercise 3 prompt typed and ready to send.*

2.  The “Show me everything for review” safeguard tests whether Cowork
    defers all actions pending approval. Cowork will first search for a
    transcript.

<img src="media/media/caf4d5e568f173c000b823c0d43692379598c313.png"
style="width:5.60417in;height:2.69792in" />

*Grounding enforced: “I won't invent meeting content.”*

3.  Cowork enforces grounding immediately: before writing anything it
    needs the actual transcript or notes. It searches for transcripts,
    finds none, then widens the search to notes files.

<img src="media/media/8c6837b291574cc6588e23462e2781fc88234205.png"
style="width:5.60417in;height:3.30208in" />

*Complete refusal with three constructive forward paths.*

4.  After an exhaustive search, Cowork confirms no source material
    exists and declines to fabricate. It offers three alternatives:
    paste notes into chat, re-run after the meeting with transcription
    on, or point to a different meeting that has a transcript.

**Step 2 — Test in-loop correction**

1.  Send a correction to see how Cowork handles it when no output exists
    yet:

|                                                           |
|-----------------------------------------------------------|
| **PROMPT · CORRECTION**                                   |
| Actually, the website task was assigned to Priya, not me. |

<img src="media/media/9e8127d3cfe4934027e71034bc6567d63b666377.png"
style="width:5.60417in;height:2.72917in" />

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

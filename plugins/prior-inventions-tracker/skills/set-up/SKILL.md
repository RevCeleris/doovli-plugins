---
name: set-up
description: "Sets up the Prior Inventions Tracker for the person: asks six short questions, finds what they built on their own in Claude, dates each item from a record, publishes their Prior Inventions page and turns on monthly updates. Use when someone asks to set up, install or build the Prior Inventions Tracker or a prior inventions list, to move or switch an existing Prior Inventions page or doc to the plugin, or to update their Prior Inventions Tracker."
---

# Set up the Prior Inventions Tracker

Version 2.1.0. (c) 2026 Rich Henderson. Shared under CC BY-NC 4.0: free to use and adapt for your own records, with credit. Not for resale or use in a paid product. Provided as is, with no warranty. Not legal advice.

You are setting up the Prior Inventions Tracker, version 2.1.0, for me, using the Prior Inventions Tracker plugin I added to Claude. A prior invention is something I created before starting a new job or contract that I believe I own: an app, a tool, a skill, a prompt, a method, or a design I have not built yet. Employment and contractor agreements often ask for a list of these. Your job is to find my candidates, date each one from a record, and save them to my own Prior Inventions Tracker page, where I approve them, keep them current and download the Exhibit for an employer.

Work through the steps in order. Ask me questions only in Step 1, and stop for my answer only where the steps say to. Write to me in plain language, with no em dashes. You are not a lawyer and none of this is legal advice. Say so once, in the message that ends Step 4.

If I already have a Prior Inventions page from the download version and want to switch to this plugin, or I ask to switch it, follow "Switching from the download version" at the end instead of the steps below.

## Step 0. Get the files

These files come with this skill, in its assets folder: prior-inventions.html (the page), a lib folder of script files the page loads, update.txt (the monthly update task) and version.json. Read prior-inventions.html and update.txt complete from the skill folder with your code tools. Never retype, summarize or edit them, and never download them from anywhere else.

Check that prior-inventions.html contains const APP_VERSION="2.1.0". If you cannot read the files, tell me in one sentence that the plugin's files are missing and that removing and adding the Prior Inventions Tracker plugin again should fix it, then stop. Otherwise go on to Step 1 without mentioning the files.

## Rules for everything you write

1. Never invent a date. Every date comes from a record you can link to or name. When the only record shows that something existed by a date, write "On or before" that date. When there is no dated record, write "Confirm" and ask me. I can give an exact date, or a range I am confident of, such as "Late Jan to early Feb 2026". Use whichever I give.
2. Each date links to its record, or says where the record is kept when there is no link. The link text says what the record is and its date, in neutral words, such as "Chat, 13 Mar 2026", "Page published, 2 Oct 2026" or "File created, 9 Sept 2026". Never use a chat's, file's or page's own title as link text, because titles often name companies, clients or confidential projects.
3. Only date the invention itself. Leave out records that show the item being used, shown to someone or reworked later, unless one of them is the earliest record of the item.
4. Name no people other than me. Say "legal counsel", "a manager", "a client" or "a contact" instead.
5. Company and client names appear only in the legal counsel list. They never appear in an item's name, description, Register fields, Exhibit description, related items or a design document. Where a company name would appear, describe the item in general terms instead. My own business name is fine anywhere.
6. Related items are listed by ID and item name only.
7. Exhibit descriptions are general, with nothing confidential and no links.
8. Before you tell me anything is ready, check everything you wrote for names of people and companies, and for titles used as link text, and fix what you find.
9. Write in plain, connected sentences, with no em dashes, no buzzwords and no dramatic one-line sentences.

## Step 1. Ask me first

Send one message with these questions, numbered, and tell me I can answer each in a few words. If you have a tool that shows me clickable choices, you may use it for the yes or no questions.

1. Is this a new setup, or am I moving from version 1, which built a Claude doc? If I am moving, ask for the link to my Prior Inventions doc.
2. What is my full name, as it should appear on the list?
3. What time zone am I in? A city is fine.
4. Am I about to sign an agreement? If so, the company's name and my start date. I can leave this blank and fill it in on the page later.
5. Should you also search my Google Drive? This needs the Google Drive connector turned on. I can name folders to skip. (Skip this question if I am moving from version 1.)
6. Do I want the list kept current as I build new things? If yes, you will save a short note to my Claude memory. The plugin's Keep It Current skill does the rest.

If I do not know an answer, treat it as blank and go on. If I am moving from version 1, follow "Moving from version 1" below instead of Steps 2, 4, 5 and 6.

## Step 2. Find my candidates

Look through everything you can reach. Use each tool that is available to you, and note any source you could not use, for the "Where the dates come from" note in Step 4.

- My past chats. Search them by topic, using words such as app, tool, build, skill, prompt, framework, method, process, design, prototype, artifact, page, agent, automation, tracker, template and workflow, plus words from my answers. Then list my chats by time, as far back as your tool allows, and open any that look like building or designing something. A chat's listed date is when it was last active, so treat it as "On or before" that date unless the chat itself shows an earlier one. If you could not reach my oldest chats, say how far back you got.
- My artifacts. List all of them and note each one's link and dates. An artifact's date shows only when it was last published, so use "On or before" unless you have an earlier record.
- My skills. List the skills I created or uploaded. Leave out skills that came with Claude or with a plugin.
- My Claude memory. Read it for projects, products, methods and their dates.
- My Google Drive, only if I said yes and the connector is on. Search for documents, prompts, specifications, designs and code I created. Use the file's created date as the record date.

For each candidate, note: a short name; what it is, in one or two sentences; its type; the earliest dated record of the idea (Conceived) and of a working version (Built), each with its link; who it was made for, if anyone; and whether it was shown or shared outside my own account.

Group candidates into three types, and give each an ID that never changes: M for methodologies (methods, frameworks and processes that people apply, with or without software), S for software built (apps, tools, agents, skills and prompts that work, at least in part), and D for designed, not built (ideas worked out in writing, with no working version yet). Number each group in order of Conceived date (M-01, M-02 and so on). A feature of a larger item gets a sub-ID under its parent (S-01.01). If two candidates are the same thing, merge them into one.

Leave off outputs and reference material: resumes, cover letters, reports, research, slides for a specific audience, client deliverables, and anything copied from someone else. Keep a short list of them for "Found, but not listed as inventions", so I can move one onto the list.

Suggest In, Out or Discuss for each candidate, with a one-line reason in its notes. Anything built as part of a job or for an employer is not a prior invention: suggest Out and say why. If it is unclear whether an item was my own work or done for an employer, suggest Discuss and add a question about it to the legal counsel list. If a record shows I shared an item with a company, for example while interviewing, suggest In and add a question about it to the legal counsel list. Suggest Discuss when you are not sure.

## Step 3. Publish my page

Publish a new artifact titled "[my name] - Prior Inventions Tracker" from files, using your artifact tool's option to publish from files: prior-inventions.html exactly as it is, served as index.html, and every file in the assets lib folder exactly as it is, served as lib/<file name>. Do not edit, shorten or restyle any of them. The page needs the lib files to make its Word and PDF downloads.

Give the page these capabilities, declaring them if your artifact tool asks for that:

- Database: one database. Anyone I share the page with can read it, and only I can write to it (rule: path "", read "view", write "owner").
- User: the page knows who is signed in.
- Sample: the page can ask Claude directly. It uses this to draft Register entries for items I add later.
- Downloads: the page can save the Exhibit as a Word file or PDF.
- Connectors: the scheduled-tasks connector, with the tool fire_trigger (it may be named "Claude Code Remote"). The page uses it for its Update now button.

If one capability is not available to me, publish the page anyway and tell me in one sentence which feature will not work. Pin the page to my Claude sidebar if your artifact tool can. Keep the link to the published page. The task text calls it {{PAGE_URL}}.

## Step 4. Save my candidates to the page

Use the artifact data tools (named ArtifactData in some sessions, and db_get, db_list and db_write in others; load them via ToolSearch if needed) with my page link for every write. Write these documents:

- settings/main: name, initials, timezone (as I said it), timezoneIana (the IANA name, such as America/Detroit), company and startDate (blank unless I gave them), docId ("[my initials]-PI-001") and docVersion ("0.1").
- items/<id>, one per candidate. The document ID is the item ID in lowercase with hyphens for dots (s-01, s-01-01). Fields: id ("S-01"), type ("M", "S" or "D"), parent (the parent ID for a sub-item, otherwise ""), name, what (one or two sentences), conceived and built (each {text, url, label}; leave out built for type D), include (your suggestion: "In", "Out" or "Discuss"), notes (the reason for your suggestion), status ("Built" for S, "In use" for M, "Designed, not built" for D) and createdAt (ISO now).
- In a date, text is "13 Mar 2026", "On or before 2 Oct 2026", a range I gave, or "Confirm". url is the record link, or "" when there is none. label is the neutral link text, or where the record is kept when there is no link.
- settings/lists: found (a list of short lines for "Found, but not listed as inventions"), counsel (a list of {label, question}; each label is a few words, and each question names the companies and item IDs involved and states what to settle; an empty list if there are none), and sources (the sources searched, any that could not be reached, and how far back the chat search went).
- revisions/r-0001: version "0.1", date (YYYY-MM-DD), time (HH:MM in my time zone), author "Claude, at [my name]'s direction", description "Initial draft: approval list of candidate inventions, with Register and Exhibit to follow.", approvedBy "Pending", order 1.

Apply rule 8, then send me a short message with: the link to my page; how many candidates you found of each type; how many dates need me to confirm; any source you could not reach; what to do next (open the page, go to the Approval List tab, set Include on each row to In, Out or Discuss, use Edit on a row to correct a date or fill in a Confirm, then come back to this chat and send "My approvals are done"); and this line: "This list is not legal advice. Review it with your own lawyer before you sign anything."

## Step 5. Wait for my approvals

Stop and wait for me. When I make changes in the chat, write them to the page. When I say my approvals are done, list the items again, since I will have changed them on the page. If any item still says Discuss or has no Include value, ask me about those items only, in one message.

## Step 6. Build the Register and Exhibit

For each item marked In, op "update" with if_version: problem (what was hard or missing before this item), value (what a person gains by using it), how (the mechanism, in plain steps), apart (how it differs from the usual way of doing the same job), related (IDs and item names only, adding "See the questions for legal counsel." when the item is on that list), and exhibitDesc (one or two general sentences with nothing confidential). Use only facts found in the records or given by me. If something is unknown, say what is unknown.

Update settings/main: docVersion "1.0". Update revisions/r-0001: approvedBy [my name]. Write revisions/r-0002: version "1.0", today, the current time, "Claude, at [my name]'s direction", "Approved. Register and Exhibit built from the items marked In.", [my name], order 2.

Apply rule 8 to everything on the page.

Tell me how many items are on the Exhibit by type, give me the page link, and tell me how to download the Exhibit: open the Exhibit tab and click Download Word or Download PDF. The company and start date can be filled in there with "Edit company, date and descriptions".

## Step 7. Keep it current (only if I said yes in Step 1)

Save this note to my Claude memory, word for word, with my page link filled in: "When I finish building or designing something new, such as an app, tool, skill, prompt or method, ask whether to add it to my Prior Inventions page at [LINK]. If I say yes, draft the entry with the next free ID and dates linked to their records, and wait for my approval before changing the page."

Tell me in one line that the plugin's Keep It Current skill drafts each new entry for my approval, so there is nothing else to install.

Ask whether I want a design document for any item marked In. If I do, create each one as a Claude doc titled "[my name] - [ID] [item name] - Design", using "Design document layout" below, and add its link to the item's designDocs list as {label: "Design document", url}.

## Step 8. Turn on updates

Ask me first, in one short message: "Create the monthly update check? It runs on the 1st of each month, tells you when a new version is out, and makes the Update now button on your page work. Reply yes." Wait for my answer. If I do not say yes, skip to the last item of this step.

Create a scheduled task named "Prior Inventions Tracker Updates" that runs on the 1st of each month, mid-morning in my time zone, on a minute that is not on the hour or half hour (10:17, not 10:00), with push notifications on. Use update.txt from Step 0 as its instructions, with every {{PAGE_URL}} replaced by my page link and every {{TIMEZONE}} by my time zone. Give it access to my artifact data and to the scheduled-tasks connector only. Turn off every other connector for this task.

Write the task ID to my page as document "settings/tasks": {update: the task ID}. The page's Update now button uses it. Also write document "settings/update": {installed: "2.1.0"}.

Tell me in one line that Claude checks for a new version once a month, sends me a notification when one is out, and that I install it by opening my page and clicking Update now.

If I said no, or you cannot create scheduled tasks here, tell me that I can still update any time by starting a new chat and sending "Update my Prior Inventions Tracker."

## Moving from version 1

Follow this instead of Steps 2, 4, 5 and 6 when I am moving from version 1. Never change, delete or rename anything in my old doc. Only read it.

1. Do Step 3 to publish my page.
2. Read every tab of my old doc with your docs tool: the Approval List (document control, revision history, the three item tables, "Found, but not listed as inventions", "For legal counsel before you sign" and "Where the dates come from"), the Register and the Exhibit.
3. Map them to the documents described in Step 4: each Approval List row becomes an item, with its Include value and notes as they are; each Register entry fills problem, value, how, apart, related and designDocs on its item; each Exhibit description becomes exhibitDesc; the company and start date go to settings/main; the three lists go to settings/lists; each revision history row becomes a revisions document, in order. Keep every date, link and link text exactly as it is. Keep docId and docVersion from the old document control.
4. Before writing anything, show me how many items you found by type, how many are In, and two sample items as they will look. Ask me to confirm, and wait for my answer.
5. Write the documents. Then add a revision: the next minor version, today, the current time, "Claude, at [my name]'s direction", "Moved to the Prior Inventions page. Content unchanged.", [my name]. Set docVersion to match.
6. Count the items on the page and tell me the old count and the new count. If they do not match, list what is missing and why.
7. Do Step 7 if I said yes to keeping the list current, using my page link in place of my doc link. Then do Step 8.
8. Tell me my old doc is unchanged and that I can keep it as a dated record.

## Switching from the download version

Follow this when I already have a Prior Inventions page built from the download (version 2.0 or later) and want it to run from this plugin. Ask me nothing unless something below is missing. Never change the page's data.

1. Find my page: list my artifacts and use the web page whose title ends in "Prior Inventions" or "Prior Inventions Tracker". If there is more than one, ask me which. Read its settings/main, settings/tasks and settings/update.
2. Publish a new version of that page from files, as in Step 3, keeping its title and its current capabilities. Do not create a new artifact.
3. If settings/tasks has an update task ID and that scheduled task still exists, replace its instructions with update.txt from Step 0, with {{PAGE_URL}} replaced by my page link and {{TIMEZONE}} by the timezone in settings/main, using update_trigger. Keep its name and schedule. If there is no task, do Step 8.
4. Update settings/update: installed "2.1.0", keeping its other fields.
5. If I have a saved skill of my own named prior-inventions-keep-current, tell me in one sentence that the plugin now includes the same skill, and that I can remove my own copy so the two do not both answer.
6. Tell me in one or two sentences that my page now runs from the plugin and that my list did not change, with the page link.

## Updating my page

When I say "Update my Prior Inventions Tracker" or "Update my Prior Inventions page": get document "settings/tasks" on my page. If it has an "update" task ID, write document "activity/a-<timestamp>" with kind "update", label "Update to the latest version", status "running" and startedAt ISO now, then start that scheduled task with a two-line message: "ACTIVITY ID: a-<timestamp>" on the first line and "MODE: APPLY UPDATE" on the second, and tell me to reload my page when the notification arrives. If there is no task, or you cannot start it, follow APPLY MODE in update.txt yourself, with my page link and time zone, skipping any step about a scheduled task.

## Design document layout

One Claude doc per item, titled "[my name] - [ID] [item name] - Design":

1. One sentence saying what the item is.
2. Heading "Document control", with the fields Document ID ([my initials]-DES-[the ID without its hyphen, such as S05]), Item, Owner, Classification (Confidential), Current version (0.1, Draft, becomes 1.0 on approval), Status, Review cycle ("Every material change to the item or this design") and Time zone.
3. Subheading "Revision history (oldest first)", with the columns Version, Date, Time, Author, Description of change and Approved by.
4. Heading "Dated milestones": a table with the columns Date, Milestone and Record that proves it, oldest first. Mark a row with no record "Confirm".
5. Headings "Purpose" (a short paragraph), "Value" (bullets) and "How it works" (numbered steps). When the item is a process run partly by AI and partly by people, label each step AI (no person involved), AI / HITL (AI produces it and a person approves it) or HITL (a person does it), and explain the labels in a small table. HITL stands for human in the loop.
6. Heading "Related items": a table with the columns ID and Item.
7. Heading "To confirm": a checklist of open questions.
8. Heading "Sources": a table with the columns Source (with neutral link text), Date of record and What it supports.

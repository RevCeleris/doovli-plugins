---
name: set-up
description: "Sets up the Career Opportunity Tracker for the person: asks four short questions, publishes their tracker page and creates its scheduled job and prospect searches, email check and update check. Use when someone asks to set up, install or upgrade the Career Opportunity Tracker or the Job Search Tracker, or to switch an existing tracker to the plugin."
---

# Set up the Career Opportunity Tracker

Version 4.4. (c) 2026 Rich Henderson. Shared under CC BY-NC 4.0: free to use and adapt for your own search, with credit. Not for resale or use in a paid product. Provided as is, with no warranty.

You are setting up the Career Opportunity Tracker, version 4.4, for me, using the Career Opportunity Tracker plugin I added to Claude. The tracker finds jobs that match my resume and companies that need my consulting or fractional services, drafts my applications and outreach, updates itself from my email if I allow it, and keeps my weekly work search log ready.

Work through the steps in order. Ask me questions only in Step 1, and stop for my confirmation only where Step 4 says to. Write to me in plain language, with no em dashes.

## Step 0. Get the files

These files come with this skill, in its assets folder: tracker.html (the page), a lib folder of script files the page loads, a tasks folder with jobs.txt, frac.txt, assist.txt, email.txt and update.txt (the scheduled task texts), and version.json. Read tracker.html and the five task texts complete from the skill folder with your code tools. Never retype, summarize or edit them, and never download them from anywhere else.

Check that tracker.html contains const APP_VERSION="4.4". If you cannot read the files, tell me in one sentence that the plugin's files are missing and that removing and adding the Career Opportunity Tracker plugin again should fix it, then stop. Otherwise go on to Step 1 without mentioning the files.

## Step 1. Ask me first

Send one message with these four questions, numbered, and tell me I can answer each in a few words. If you have a tool that shows me clickable choices, you may use it.

1. Is this a new setup, a switch from the downloaded Career Opportunity Tracker (version 3 or 4), or an upgrade from version 1 or 2 of the Job Search Tracker? For a switch or an upgrade, ask for the link to my current tracker. I can copy it from the address bar while it is open.
2. What time zone am I in? A city is fine.
3. Do I want the email check? It reads my Gmail twice each weekday for interview requests, rejections and replies, and updates my tracker for me to keep or undo. It never sends, deletes or changes an email. It needs the Gmail connector turned on in Claude's settings.
4. Do I use HubSpot and want an "Add deal to HubSpot" button on my fractional prospects? It needs the HubSpot connector. If I am not sure, treat the answer as no. I can add it later.

If I am switching from the downloaded Career Opportunity Tracker, follow "Switching from the download version" below, then go to Step 5.

## Step 2. Publish my tracker

Publish a new artifact titled "Career Opportunity Tracker" from files, using your artifact tool's option to publish from files: tracker.html exactly as it is, served as index.html, and every file in the assets lib folder exactly as it is, served as lib/<file name>. Do not edit, shorten or restyle any of them. The page needs the lib files to read resumes, make Word files, zip downloads and Excel exports.

Give the page these capabilities, declaring them if your artifact tool asks for that:

- Database: one database. Anyone I share the page with can read it, and only I can write to it (rule: path "", read "view", write "owner").
- User: the page knows who is signed in.
- Sample: the page can ask Claude directly. It uses this to draft IEPs, ICPs, my offer, outreach, answers to my questions, and tailored resumes and cover letters.
- Downloads: the page can save files for me.
- Connectors: the scheduled-tasks connector, with the tools fire_trigger, list_triggers and update_trigger (it may be named "Claude Code Remote"). Only if I said yes to HubSpot, also the HubSpot connector with the tools search_crm_objects, manage_crm_objects, get_properties and get_user_details.

If one capability is not available to me, publish the page anyway and tell me in one sentence which feature will not work. Pin the page to my Claude sidebar if your artifact tool can. Keep the link to the published page. The task texts call it {{TRACKER_URL}}.

## Step 3. Create the scheduled tasks

Create these scheduled tasks from the task texts in Step 0. In each text, replace every {{TRACKER_URL}} with my tracker link and every {{TIMEZONE}} with my time zone. Write each schedule in my time zone, on a minute that is not on the hour or half hour (6:52, not 7:00).

| Task name | When it runs | Text |
|---|---|---|
| Career Tracker Job Search | Mondays and Thursdays, early morning | jobs.txt |
| Career Tracker Prospect Search | Mondays and Thursdays, about 20 minutes after the job search | frac.txt |
| Career Tracker Assistant | No schedule. The page starts it when I ask a research question, request a deep check or draft from my website. | assist.txt |
| Career Tracker Email Check | Weekdays, once mid-morning and once early afternoon. Create it only if I said yes to the email check. | email.txt |
| Career Tracker Update Check | The 1st of each month, mid-morning | update.txt |

Give each task the connectors its text uses: every task needs access to my artifact data, the Email Check needs Gmail, and the Assistant and both searches need web search. Turn off every other connector for each task. If my plan will not let you create all of them, create them in the order listed above and tell me which ones could not be created and what that means.

Then write the task IDs into my tracker as document "settings/tasks": {jobs: Job Search ID, frac: Prospect Search ID, assist: Assistant ID, email: Email Check ID or "", update: Update Check ID}. The page uses these IDs for its "Run job search now", "Run prospect search now", "Check email now" and research buttons. Also write document "settings/update": {installed: "4.4"}.

## Step 4. Upgrade from the Job Search Tracker only: move my old data

Skip this step for a new setup. Never change, delete or rename anything in my old tracker. Only read it.

1. Read my old tracker's data with your artifact data tool, using the link I gave. Each old tracker was built by its owner's own chat, so field names vary from person to person. If you cannot read it, because some older trackers keep their data where this tool cannot reach it, tell me exactly this: "Open the chat where you built your old tracker and send: Export every job in my tracker, with every field and the full job description, as an Excel file I can download. Then attach that file here." Continue from item 2 with the file I attach.
2. Map each old job to these fields in the new "jobs" collection: company, title, location, pay, sector, url, postedDate, foundDate, lastVerified, status (one of new, reviewing, applied, interviewing, offer, rejected, not_pursuing, withdrawn, inactive), appliedDate, method (how I applied), contact, notes, fit, jd (the full job description), docs (a list of {label, url}), uiSubmitted (true or false) and uiSubmittedAt (the "Submitted to Unemployment" checkbox and its date). Dates are YYYY-MM-DD. Put any old field with no match, such as a role category, into notes with its label. Do not carry over old tailored drafts.
3. If the old tracker holds my Ideal Employment Profile (IEP), map it to one document in the "ieps" collection: name, color "#1d5d78", active true, titles (list), industries, focus, exclusions (list), roleKey "", searchNotes, order 1. Put pay, location and work type rules into document "settings/jobsearch" as location, employment and windowDays (30 unless the old tracker used another number).
4. Before writing anything, show me: how many jobs you found, a short table of old field to new field, and three sample jobs as they will look. Ask me to confirm. Wait for my answer.
5. Write the jobs with op "set". Doc IDs are lowercase company-title slugs (letters, digits and hyphens). Add source "Moved from old tracker", lastChange "Moved from old tracker" and lastUpdated (now, ISO). Never create two records for the same job.
6. Count the jobs in the new tracker and tell me the old count and the new count. If they do not match, list what is missing and why.

## Step 5. Finish

Send me one short message with:

- The link to my tracker.
- Which scheduled tasks were created or updated, and when each one runs, in my time zone.
- For an upgrade from the Job Search Tracker, the old and new job counts, and a reminder to turn off my old tracker's scheduled job search so I do not get two searches: in Claude, click Scheduled in the left sidebar, open the old task and turn it off.
- For a new setup or an upgrade from the Job Search Tracker, these next steps, word for word. Skip them when switching from the download version.
  1. Open your tracker. On the Jobs tab, click My resume, choose your resume's Word file, and click Save resume. Use your standard resume, not one tailored to a single job.
  2. Go to the Dashboard. Under Suggestions for you, your tracker shows the Ideal Employment Profiles (IEPs) it drafted from your resume. Click Add this IEP for each one you want, or No thanks. You can edit them any time under Profiles and settings.
  3. For consulting or fractional work, open Profiles and settings, find Your offer, and under Draft my offer and ICPs click Draft from my resume or Draft from my website. Approve the drafts on the Dashboard the same way.
  4. Only want one side? Use the Features box at the top right of the Dashboard to turn Jobs or Fractional off.
  5. Click Run job search now on the Jobs tab, and Run prospect search now on the Fractional tab, to get your first results today instead of waiting for Monday or Thursday.
- One line saying the plugin also includes the Apply to a job skill: with a posting open in Claude in Chrome, I can say "Add this job to my tracker and tailor my resume" and Claude does the rest.

## Switching from the download version

Follow this when I already have a Career Opportunity Tracker from the Doovli download (version 3 or 4) and want it to run from this plugin. My tracker keeps its link and all of its data.

1. Publish a new version of my existing tracker, using the link I gave, from files as in Step 2. Keep its title. Give it the capabilities listed in Step 2, adding any it does not already have.
2. Read document "settings/tasks" in my tracker to find my scheduled task IDs (jobs, frac, assist, email, update).
3. For each of those tasks that exists, read its current instructions with list_triggers. Take the matching task text from Step 0, with every {{TRACKER_URL}} replaced by my tracker link and every {{TIMEZONE}} by my time zone. If the current instructions contain anything specific to me that is not in the new text, such as a named company, a person's name or a rule I added, copy it to the end of the new text under the heading "My own additions". Then replace the task's instructions with the new text using update_trigger. Keep each task's name and schedule. Do not create new tasks unless one is missing, and if one is missing, tell me before creating it.
4. Update "settings/update": installed "4.4", keeping its other fields.
5. Do not change, move or delete any records in my tracker. Do not run Step 2, Step 3 or Step 4 beyond what this section says.
6. If I have a saved skill of my own named job-application-package, tell me in one sentence that the plugin now includes the same skill as Apply to a job, and that I can remove my own copy so the two do not both answer.
7. Tell me which tasks you updated. Remind me to check the bottom of my tracker, which should now say "Version 4.4".

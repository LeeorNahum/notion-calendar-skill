---
name: "notion-calendar"
description: "Use whenever any event Leeor attends or due date someone sets for him appears in any source (a transcript, recording, text, email, or conversation, in any project), or when he asks to add, move, or cancel one. Adds or corrects it in his Notion Events calendar the way he fills it in himself."
metadata:
  author: "Leeor Nahum"
  version: "1.2.0"
---

# Leeor's Notion Events Calendar

This is Leeor's own Notion Events calendar. It takes every event he attends and every due date someone else sets for him (a submission, payment, registration, or booking), added in the same session it appears. A self-imposed errand is not a row, even when it has a day. A plan that is still tentative is reported to him, not added as a firm event.

Database: https://app.notion.com/p/bc694c50e369465d891f4eb8f305ba77?v=35e418dd3ca943d5b31401b546c0bb6b

His fields are Name, Date, Location, Link, Leave Reminder, Future Planning, and Archive. There is no category, status, or attendee field, so the title carries the meaning. Do not touch Leave Reminder, Future Planning, or Archive unless he asks. Event Length and Event Timing are formulas, never typed into.

Examples below show shape only. Write the title and values that are accurate for the event in hand.

## Before Adding

Look at every row from the day before to the day after the event's date, archived and past rows included, since the calendar view can hide them, and the earlier date too when the source says the event was moved. Filter the database by date rather than searching for a title or scrolling the view. The same occurrence often sits under another name, such as an `(if <condition>)` row or one added before its time was known, so match by what the event is (its organizer, purpose, people, and session or booking), not by title. A prep session and the event it prepares for, or a deadline and a meeting about it, are separate events. If you cannot tell whether two rows are one event, add nothing and ask him.

If the event is there, update that row with the accurate title, date, time, location, link, and body instead of adding a second row. A row for the same occurrence on a nearby date has a wrong date, so fix it. Drop a row's `(if <condition>)` once the source shows the condition was met. The same event can legitimately repeat on other dates, so a different date alone is not a duplicate.

If two rows already cover one occurrence, carry every accurate detail into one of them, read it back, then move the other to Notion's trash. Name the trashed row in the reply.

## Fields

- **Name:** A short title-case noun phrase, led by the organization or program for formal series (`<Org> <Program> Meeting <n>`).
  - Put the person or group in the title when it matters (`<Person> <Org> Meeting`), and a secondary companion in parentheses (`<Appointment> (<Companion>)`).
  - Number a series (`<Series> Session <n>`, `<Thing> (<n>/<total>)`).
  - Name a deadline `<Thing> due` and a flight `Flight <city> to <city>`, one event per direction.
  - Put a condition in a trailing parenthetical (`<Thing> (if <condition>)`).
  - Add "(Cancelled)" after the title of an event that was cancelled, and keep the row.
  - Use no emoji, prefixes, or tags.
- **Date:** New York time, with Notion's default reminder kept.
  - Resolve "Thursday" or "next week" against when the source said it, not the day it is filed, and convert a source's other time zone to New York.
  - A deadline goes on its real due day, never a target day. With a stated hour it is timed at that hour. With none it is all-day.
  - All-day, no time, for holidays, school dates, and trips (a start and an end date).
  - Timed for anything with a start hour the source or Leeor states. Add an end only when the source gives a length or an end (a session, a flight from departure to final arrival, an overnight event ending the next day). Never guess one.
  - When the event is a visit to a place and neither the source nor Leeor states a time, it is all-day with no time. Only a stated time goes in the date.
- **Location:** A URL-typed field in which he types plain text, never a sentence.
  - The place name (`<building> <room>`), or, for an outside venue, a Google Maps link to the place itself (a place page or a search link such as `https://www.google.com/maps/search/?api=1&query=<place name>`, never a directions link with a start and an end.
  - "Zoom" or "Online" for a virtual event, with the meeting URL in Link.
  - A short route for a flight (`<city> to <city> via <city>`).
  - Empty when there is no real place.
- **Link:** The meeting URL for a virtual event, otherwise the event's reference page (a steps page, a booking, or the announcement), otherwise empty. Link holds one URL, and the event's reference page goes here and never in the body.
- **Body:** Empty by default. Where a fact is needed, write each separate piece of information as its own Notion bulleted-list item (`- ` plus the text), one per line, never several facts run together in one line (`- Leave <city> <time>`, `- Land <airport> <time>`, `- $<amount>`), with nothing he does not need, such as flight numbers or aircraft.
  - For a place he rarely goes to (a post office, an office, a store), add that day's opening hours as an item, taken from the place's own listing and never guessed. Add none for a place he goes to routinely.

## What Never Goes In The Body

Notes, tasks, reasoning, why the event matters, copied invitation or email text, any URL, and the agent's commentary. A to-do is not an event.

## Working The Page

This needs his signed-in Chrome, driven by whatever browser tool the harness provides. Open the database there, and read each row back from the page afterward to confirm what landed.

- Set Date and Location in the page UI. Notion's API and MCP page-update tools do not reliably persist them.
- Set Name, Link, and body in the same page UI pass, so one route fills the whole row.
- If that Chrome is not reachable, stop and tell him, with each event's title, date, location, and link ready for him to enter.

## Handoff

Leave each new or changed event open in its own tab for him to check. Closing a tab is his approval. Say in the reply which events were added, which were fixed, which were already there, and which were left out as tentative or self-imposed.

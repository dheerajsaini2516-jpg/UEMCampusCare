# UEM CampusCare

A simple, responsive campus issue-tracking web application for UEM. Students can submit and browse campus issues, while administrators can review reports, add resolution notes, and mark issues as resolved.

## Features

- Separate student and administrator login flows
- Submit issue reports with title, category, location, and details
- Browse active reports and filter them by category
- Search active reports by title, location, or category
- Admin dashboard with open/resolved issue counts
- Resolution notes for completed reports
- Recently resolved issue history visible to students
- Persistent demo data using browser `localStorage`
- Mobile-responsive interface

## Tech stack

- HTML5
- CSS3
- Vanilla JavaScript
- Google Fonts: DM Sans and Plus Jakarta Sans

## Project structure

```text
UEM campuscare/
├── index.html   # Application markup and screens
├── style.css    # Styling and responsive layout
├── script.js    # Application behaviour and local storage logic
└── README.md
```

## Run locally

No build step or package installation is required.

1. Download or clone the project.
2. Open `index.html` in a modern web browser.
3. Log in with one of the demo accounts below.

For the best development experience, open the folder in VS Code and run `index.html` using a local web server such as Live Server.

## Demo credentials

| Account type | Password |
| --- | --- |
| Student | `uemcampus` |
| Administrator | `uemcampusadmin` |

The name and Gmail address fields accept any valid values for this demo.

## How it works

### Student

1. Log in as **Student**.
2. Select **Report new issue**.
3. Fill in the issue details and submit the report.
4. Use category filters or search to find active issues.
5. Check **Recently resolved** for completed work and administrator notes.

### Administrator

1. Log in as **Administrator**.
2. Review the reports waiting for action.
3. Enter a resolution note for an issue.
4. Select **Mark problem solved**.
5. The issue moves to the resolved history and is removed from the active student list.

## Data storage

The app is a front-end demo; it does not use a server or database. Reports are saved only in the current browser using these `localStorage` keys:

- `cc-open-issues`
- `cc-resolved-issues`

Use **Reset demo data** in the admin dashboard to restore the initial sample reports. Clearing the browser's site data will also remove saved reports.

## Categories

- Maintenance
- Cleanliness
- Technology
- Safety

## Notes

The login credentials and role checks are implemented in client-side JavaScript for demonstration purposes only. For a production application, use a secure backend, real authentication, role-based authorization, and a persistent database.

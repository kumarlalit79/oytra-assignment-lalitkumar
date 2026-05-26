# Oytra Assignment Submission — Lalit Kumar

## Task 1 — QA Testing Report

For Task 1, I tested the RealWorld demo application locally and performed manual QA testing on the major user flows including:

* user registration
* login/logout
* article creation
* comments
* protected routes
* validation handling

During testing, I identified multiple issues related to:

* frontend crashes
* missing validation
* broken error handling
* empty input submission
* UI/UX problems

The detailed bug report and root cause analysis are included in:
`Task1_QA_Report_LalitKumar.pdf` and `Root_Cause_Analysis.pdf`

---

## Task 2 — n8n API Integration Workflow

For Task 2, I built an automated workflow using n8n.

### APIs Used

1. GitHub REST API
2. GitHub Repository Details Endpoint

### Why These APIs Were Chosen

I selected the GitHub API because it provides real-world public developer data, supports filtering/sorting, and allows meaningful transformations for automation workflows.

### Workflow Logic

* A Schedule Trigger runs the workflow automatically.
* The first HTTP Request fetches trending/open-source repositories related to AI.
* A transformation step filters and keeps the top 5 repositories based on popularity.
* A second API request enriches repository information.
* An IF node checks conditions such as repository popularity thresholds.
* Final processed data is stored inside Google Sheets.

### Error Handling

The workflow includes:

* retry handling
* continue-on-fail behavior
* fallback error logging using an Error Trigger workflow

This ensures the workflow does not fail silently.

---

## Bonus Task — Uptime Monitor

For the bonus task, I created a second n8n workflow that monitors website uptime every 5 minutes.

### Features

* periodic monitoring
* HTTP status checking
* conditional alerting
* Google Sheets logging
* retry handling
* workflow error logging

If the monitored endpoint returns anything other than the expected healthy response, an alert entry is automatically added to Google Sheets.

Thank you.

Add Raj Electronics full QA suite - manual + mock API + Selenium POM automation

## What this project is

This is a QA project where I tested a real business web app (Raj Electronics Ledger).

I covered:
	•	manual testing (test cases + edge cases)
	•	UI automation using Selenium
	•	basic data validation using mock/API tests

The goal was to test how the app behaves in real usage, not just check happy paths.

## Project Structure

	qa_suite/
	├── conftest.py
	├── requirements.txt
		├── mock_api_tests.py
	├── manual_test_cases.md
	│
	├── pages/
	│   ├── base_page.py
	│   ├── login_page.py
	│   ├── dashboard_page.py
	│   ├── client_page.py
	│   └── report_page.py
		│
	└── tests/
	    ├── test_login.py
	    ├── test_dashboard.py
	    └── test_clients_and_reports.py
	
  ## How to run

  Install dependencies: 
  
	  pip install -r requirements.txt

  Set credentials

	export RAJ_USERNAME="your_username"	
	export RAJ_PASSWORD="your_password"


## Other useful commands:

	pytest -m smoke -v	
	pytest tests/ --headed -v
	pytest tests/ --browser firefox -v
	pytest tests/ -n 4 -v

## How I approached testing

  •	Focused on core flows: login, clients, payments, reports
	•	Tested both valid and invalid scenarios
	•	Checked data consistency (totals, dues, updates)
	•	Used automation for repeatable flows
	•	Used mock tests to validate expected data structure

Not everything is automated. Some things are easier to catch manually, especially UI issues.

## Automation design

I used a simple Page Object Model:
	•	locators are kept inside page files
	•	tests only call actions (like login, add client, etc.)
	•	if UI changes, only one file needs update

Firebase loads data asynchronously, so I used explicit waits to avoid false failures.


## Test Coverage

  •	26 manual test cases
	•	~40+ automated UI tests
	•	~25 mock/API checks
  
  Covers:
	•	login & auth
	•	team & client management
	•	sales & payments
	•	reports & filters
	•	basic security and validation


  ## Known Issues (found during testing)
  
  •	Double-click on “Add Team” can create duplicates
	•	Dashboard values don’t refresh automatically after updates
	•	Sorting can behave incorrectly if values are treated as strings
	•	Login error sometimes shows raw Firebase message


## Final

This project is my attempt to combine:
	•	manual QA thinking
	•	automation basics


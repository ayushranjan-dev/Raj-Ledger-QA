Electronics Web App Testing - Manual Testing Project

What this project is

This is a manual QA testing project where I tested a real business web app:
https://electronics-ledger.netlify.app/

The focus was on validating real-world usage scenarios, not just ideal flows.

I covered:

* Functional testing
* Edge case testing
* Data validation
* UI behavior under different conditions

## Project Structure
	qa_suite/
	├── manual_test_cases.md
	├── Test_cases_ledger app.xlsx
	├── Preview.png
	├── Test cases preview.png


## Testing Approach

* Focused on core business flows: login, clients, payments, reports
* Covered both valid and invalid scenarios
* Verified data consistency (totals, dues, updates)
* Tested edge cases and user behavior patterns
* Identified UI and usability issues

This project emphasizes practical QA thinking - how an actual user interacts with the system.


## Test Coverage

* 26+ detailed manual test cases

Covers:

* Login and authentication
* Team and client management
* Sales and payment tracking
* Reports and filters
* Basic validation and error handling

## Known Issues (Found During Testing)

* Double-click on “Add Team” creates duplicate entries
* Dashboard values do not refresh automatically after updates
* Sorting issues when values are treated as strings
* Login error sometimes exposes raw backend message



## Final

This project demonstrates:

* Strong manual QA fundamentals
* Real-world test scenario design
* Ability to identify functional and UI issues
* Structured test case documentation

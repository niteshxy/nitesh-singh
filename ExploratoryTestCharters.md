# Exploratory test charters
---
#### 1. Explore the add/delete of expense and income features with realistic data to discover any issues (30 mins)
#### 2. Explore the charts with data in all categories to discover any design issues in charts (30 mins)
#### 3. Explore the settings feature with various options to discover any flaws (20 min)
#### 4. Explore all the components of the app with user scenarios to dicover usbalitiy issues (40 mins)
##### Findings
- No option to bulk delete entries , user has to go inside it and then delete
- When adding an expense or income it is immedeately saved on choosing the category and user would have to go back if its clicked by mistake.
- Message in clicking 'Restore' on the Monefy pro description page appears after a lag and sometimes doesnt appear at all.
#### 5. Explore the input components by entering large inputs to discover if something breaks (20 mins)
#### 6. Explore the account transfer feature to discover that transactions are updated correctly (30 mins)
##### Findings
- Transfers not shown in the chart
---
#### Prioritization of the charters
The charters listed above are numbered as per the priority. The top 3 charters are touching all the core functionalities of the app i.e. 
- Add/ Delete expense and income
- Viewing the charts with data in all the categories
- discovering any issues in 'Settings' menu.

These top 3 charters cover all the main functionalities of this app and doing the exploratory testing around these functionalities can help in finding issues which could immediatlely impact the application.
The bottom 3 charters i.e. 4, 5 and 6 are focussed on discovering the usability issues and are covering edge cases so their priority is lower than the top 3 charters
#### Risks which need to be mitigated for this applicaiton
- The type and quantity of data entered should not break the application.
- Calculation and charts in the app should not be impacted by any new development.
- Users should not be able to easily find workaround of paid features.


# CustomGPTassistant

Project to build a custom GPT for assisting users for emails, calendar, and task management by interfacing with Google Workspace APIs. This custom GPT is designed to only work someone's individual account. This assistant can read emails, parse out the event information, and add that to one's calendar.

# Prerequisites
- Have an OpenAI account with Plus, Team or Enterprise subscription. See this link for details: https://openai.com/chatgpt/pricing. No need for token credits for this project!
- Have a Google Workspace account **without** Advanced Protection. Google Workspace includes Gmail, Calendar, Task and other Google services. Advanced Protection blocks certain APIs and application from running on the account.
- Setup Google Cloud Console, https://console.cloud.google.com/.

# Directions
1. Setup OAuth 2.0 on Google Workspaces account. When specifying the Scope, specify email and calendar domains.
2. Get **Client ID** and **Client Secret**
3. Go to your OpenAI account, and create a custom GPT.
4. Go to the Configure Tab, and then lower down on the left panel, click Create new action. The left panel should change to **Add actions.**
5. Click on the box below or next to Authentication, which should say None. An Authentication pop-up window should appear.
6. Select OAuth
7. Paste **Client ID** and **Client Secret** into the Authentication windows, into their respective fields
8. Copy the Authorization URL and Toke URL from this image into the respective areas in the pop-up. ![image](https://github.com/zenmindai/CustomGPTassistant/assets/58801094/abdb7ac7-59b4-4847-968e-0046fca9ab0c)
9. Copy Scope URLs into the Authentication Scope empty text box, for the email and calendar domains.
10. Save the authentication window. This will take you back to the Edit actions page.
11. Copy and past the openAPIschema.yaml file into the Schema box.
12. Click the back arrow icon left of the Edit actions.
13. Copy the Callback URL, which should be on the left panel, below the Actions.
14. Go back to Google Workspace Console, and paste the Callback URI into the console.
15. Go back to the OpenAI website for building the CustomGPT.
16. Copy and paste the Instructions file into the Instruction window.
17. Click on the Update or Save green button on the upper right corner of the page. This will save your changes.
18. Test out the assistant in the right panel!


# Resources
- Setup OAuth 2.0 to Access Google APIs https://developers.google.com/identity/protocols/oauth2-
- Visual Guide to setup OAuth 2.0 for Google APIs, courtesy of Postman: https://blog.postman.com/how-to-access-google-apis-using-oauth-in-postman/

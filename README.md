
Auto Reply Gmail Bot using Node.js
Description
This repository contains the source code for the Auto_reply_gmail_api_app developed using Node.js and Google APIs. The application is designed to automatically respond to emails in your Gmail mailbox while you are away on vacation.

Features
Node.js clusters support.
Checks for new emails in a specified Gmail ID.
Sends replies to emails without prior responses.
Adds a label to the email and moves it to the labeled folder.
Periodically performs the above steps within a random time interval ranging from 45 to 120 seconds.
Libraries
googleapis: This package is imported from the googleapis module, providing essential functionality to interact with various Google APIs, including the Gmail API.
OAuth2: The OAuth2 class from the google.auth module is utilized to authenticate the application and obtain an access token for making requests to the Gmail API. It handles token refresh and retrying requests if necessary.
Getting Started
To set up OAuth 2.0 authentication for your application, follow these steps:

Go to the Google Cloud Console and create a new project.
Click on the project name to navigate to the project dashboard.
In the left sidebar, click on the "Credentials" tab under the "APIs & Services" section.
On the Credentials page, click on the "Create credentials" button and select "OAuth client ID" from the dropdown menu.
Choose "Web application" as the application type and provide a name for the OAuth 2.0 client ID.
Enter the authorized redirect URI (e.g., "https://developers.google.com/oauthplayground").
Click "Create" to obtain the client ID and client secret, and also enable the Gmail API.
Open the OAuth 2.0 Playground.
Enter the client ID and client secret in the playground settings.
In "Step 1: Select & authorize APIs," enter https://mail.google.com and select the appropriate Gmail API scope.
Click "Authorize APIs" and sign in with the Google account associated with the Gmail account.
Copy the authorization code, click "Exchange authorization code for tokens," and copy the refresh token.
Replace placeholder values in credentials.js with obtained values: CLIENT_ID, CLIENT_SECRET, REDIRECT_URI, and REFRESH_TOKEN.
Save the credentials.js file.
Installation and Running
bash
Copy code
# Get the latest snapshot
git clone https://github.com/Sahil-Sayyad/Auto_reply_gmail_api_app.git

# Install NPM dependencies
npm install

# Install googleapis and nodemon
npm install googleapis nodemon

# Start the app
npm start
Code Improvements
Note on areas where your code can be improved:

Error Handling: Enhance error handling for more robust execution.
Code Efficiency: Optimize the code to handle larger volumes of emails efficiently.
Security: Ensure secure storage of sensitive information, such as client secrets and refresh tokens.
User-specific Configuration: Allow users to provide their configuration options, such as email filters or customized reply messages.
Time Monitoring: Improve time monitoring by using the cron jobs package to schedule email tasks.

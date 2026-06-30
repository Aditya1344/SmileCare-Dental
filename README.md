# 1. Extract the zip and open in VS Code
cd smilecare-dental-ai
npm install
node app.js
Then open your browser → http://localhost:3000

Thunder Client (inside VS Code)
Step 1: Install Thunder Client

Press Ctrl+Shift+X → search Thunder Client → Install

Step 2: Open it

Click the thunder icon in the left sidebar

Step 3: New Request

Click New Request
Set method to POST
URL: http://localhost:3000/chat

Step 4: Set Body

Click Body tab
Select JSON
Paste:

json{
  "message": "I want to book a teeth cleaning appointment tomorrow."
}
Step 5: Click Send
You'll get back:
json{
  "success": true,
  "reply": "Sure! I can help you book a Dental Cleaning appointment on Tomorrow...",
  "intent": "BOOK_APPOINTMENT",
  "service": "Dental Cleaning",
  "date": "Tomorrow"
}

All 4 test cases to run one by one
Just change the message value each time:
json{ "message": "Book root canal tomorrow" }
json{ "message": "What are your timings?" }
json{ "message": "What services do you provide?" }
json{ "message": "Hello" }

Make sure node app.js is running in a separate terminal before sending requests. That's it — no Postman, no browser, everything inside VS Code. 

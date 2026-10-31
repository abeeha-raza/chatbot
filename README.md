# chatbot 
IT Course Assistant Chatbot

An AI chatbot for an IT training institute, built with n8n. It answers students' questions about courses, fees, admission, classes, certificates and jobs, using a ready-made dataset. When it does not know an answer, it asks for the customer's mobile number and saves the question in a Google Sheet so the team can follow up.

**Features**
Answers questions only from a 100-row dataset (no made-up fees, dates or details)
Covers 6 IT courses: Web Development, Python Programming, Graphic Designing, Cyber Security, Data Science and Mobile App Development
Replies in the same language as the user (English or Roman Urdu)
Detects unanswered questions and politely asks for the customer's mobile number
Saves the customer's name, mobile number, question and date/time to Google Sheets
Politely refuses questions unrelated to the institute
**HOW IT WORKS**
Customer message
      |
      v
 Chat Trigger  -->  AI Agent (system prompt + dataset)
                        |
          +-------------+----------------+
          |                              |
   Answer found in dataset       Answer NOT found
          |                              |
   Reply to customer          Ask for mobile number
                                         |
                              Google Sheets (Append Row)
                                         |
                              "Our team will contact you soon"
 **Repository Files**
**File	Description**
workflow.json	->  The exported n8n workflow
system_prompt.txt	->  The system message used by the AI Agent  
it_course_chatbot_data.xlsx	 ->  Same dataset in Excel / Google Sheets format

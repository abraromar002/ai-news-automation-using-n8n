# 🧠 AI News Auto-Notifier using n8n

This n8n workflow automates the process of fetching, classifying, formatting, emailing, and storing the latest Artificial Intelligence news.

---

## 🔄 Workflow Summary

- **⏰ Daily trigger:** Runs every day at 1 PM (Jordan time).
- **🌐 News Source:** Uses NewsAPI to fetch the 5 latest AI-related articles.
- **📋 Filtering:** Checks if there are any results before proceeding.
- **🧹 Cleaning:** Removes missing fields and formats articles for consistency.
- **🎨 Formatting:** Prepares a beautiful HTML layout for the email body with image previews.
- **🤖 OpenAI Integration:** Classifies articles into categories like: Tech, Legal, Educational...
- **📬 Gmail Node:** Sends the email with the AI news to a specified inbox.
- **📊 Google Sheets:** Stores each news article in a structured sheet for archiving.

---

## 🧩 Nodes Breakdown

| Node           | Purpose                                              |
|----------------|------------------------------------------------------|
| Schedule       | Trigger the workflow every day at a specific time.  |
| HTTP Request   | Calls NewsAPI to fetch AI news.                     |
| IF             | Checks if `totalResults > 0`.                        |
| Code1          | Cleans and normalizes the articles.                  |
| Code           | Builds the HTML email content.                       |
| OpenAI         | Classifies each article by topic.                    |
| Gmail          | Sends the email with classified AI news.            |
| Google Sheets  | Saves the articles for record-keeping.               |

---


![ai](https://github.com/user-attachments/assets/d4debb76-821f-4753-b37b-d9dbdebf37aa)

## 💡 Example Email Output

```html
🧠 آخر أخبار الذكاء الاصطناعي  

📎 Includes article image  

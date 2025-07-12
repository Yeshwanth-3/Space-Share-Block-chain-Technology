### Space Share-Block chain Technology####
SpaceShare is a secure file sharing and user-authenticated platform built with Flask, MongoDB, and GridFS. It offers OTP-based signup/login, individual file databases for each user, and email verification using SendGrid.

🔐 Built with a mindset toward decentralized and user-specific file security architecture.

📦 Features
🔐 OTP-based signup and login using email (via SendGrid)

📂 Upload, download, and delete files

👤 Separate MongoDB databases per user (mimicking decentralization)

🧾 File listing per user

🗑️ Admin-level user deletion (removes all user files and data)

📧 OTP-based email verification

🔒 Secure filename handling

🛠️ Tech Stack
Backend: Flask (Python)

Database: MongoDB + GridFS

Email Service: SendGrid

Environment Management: python-dotenv

Frontend: Static HTML (can be expanded)

🚀 Getting Started
📁 Clone the repository
----git clone https://github.com/yourusername/space-share.git
cd space-share

🔧 Environment Setup
Create a .env file in the root folder with:
----SENDGRID_API_KEY=your_sendgrid_api_key

📦 Install dependencies
--pip install flask pymongo python-dotenv sendgrid
---Ensure MongoDB is running locally at mongodb://localhost:27017/.

▶️ Run the app
 Make sure the if __name__ == '__main__': line is correct:
--->if __name__ == "__main__":
    app.run(debug=True, host="0.0.0.0", port=5001)
Then start the app:
----python app.py

  📡 API Endpoints
🔐 Auth
POST /send_otp
→ Send OTP for signup or login

POST /signup
→ Register a new user with OTP verification

POST /login
→ Login existing user with OTP verification

DELETE /delete_user/<username>
→ Delete user and their database

📁 File Management
POST /upload
→ Upload file with username in form-data

GET /download/<username>/<file_id>
→ Download file using username and file ID

GET /list_files?username=<username>
→ List files uploaded by the user

DELETE /delete_file/<username>/<file_id>
→ Delete a specific file by ID



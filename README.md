# mlb-tracker

## 📁 Project Directory Structure

```bash
mlb-hot-streaks/
├── backend/
│   ├── app.py                  # Flask entry point
│   ├── routes/
│   │   └── signup.py           # POST /signup endpoint
│   ├── utils/
│   │   └── hot_streaks.py      # MLB logic (API calls + filtering)
│   ├── templates/
│   │   └── email_template.html # Email body (HTML layout)
│   ├── services/
│   │   └── send_email.py       # SendGrid or SMTP integration
│   ├── models/
│   │   └── subscriber.py       # SQLAlchemy model for subscribers
│   ├── database.py             # DB setup and connection
│   ├── scheduler.py            # Daily task to fetch/send emails
│   └── .env                    # API keys and config

├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   └── SignupForm.jsx  # Form for email capture
│   │   ├── pages/
│   │   │   └── Home.jsx        # Landing page with call-to-action
│   │   ├── App.jsx
│   │   ├── index.js
│   └── package.json

├── .gitignore
├── README.md
└── requirements.txt            # Python dependencies

# Development Process for MLB Hot Streak Notification App

## 1. Set Up Your Development Environment
- **Install Python 3.x** and **Node.js** (for backend and frontend, respectively).
- **Create virtual environments** for the Python backend and install required packages (e.g., Flask, SQLAlchemy).
- **Create a React project** for the frontend.

## 2. Backend Development (Flask)
- **Initialize Flask app** with basic configurations (routes, database setup).
- **Create database models** (e.g., `Subscriber` for storing email addresses).
- **Develop routes** to handle sign-ups (POST `/signup` endpoint).
- **Integrate with external MLB API** to get hot streak player data.
- **Set up email service** (e.g., SendGrid or SMTP) to notify subscribers.
- **Create a background scheduler** to fetch hot streak data and send emails regularly (e.g., daily).
- **Test the backend** to ensure data is saved and emails are sent correctly.

## 3. Frontend Development (React)
- **Set up React project** using Create React App.
- **Create signup form** for users to input their email.
- **Connect React form to Flask API** for user sign-ups.
- **Develop a landing page** with information about the service and the signup form.
- **Test the frontend** to ensure it works as expected (form submissions, display of success/error messages).

## 4. Testing & Debugging
- **Test locally**: Check both frontend and backend interactions (sign-up, data fetching, email sending).
- **Fix bugs**: Ensure emails are being sent correctly and the frontend is displaying success/error messages.

## 5. Deployment
- **Deploy the backend** (e.g., Heroku, AWS) to make it publicly accessible.
- **Deploy the frontend** (e.g., Vercel, Netlify) to host the React app.
- **Configure environment variables** (API keys, database URIs) for production.

## 6. Ongoing Monitoring & Updates
- **Monitor the app** for any issues (e.g., email failures, broken signups).
- **Iterate and add features** as needed (e.g., subscriber preferences, player filtering).

---

## Tools/Technologies Needed:
- **Backend**: Python, Flask, SQLAlchemy, SendGrid/SMTP, MLB API
- **Frontend**: React, Axios (for API calls)
- **Deployment**: Heroku/Netlify/Vercel, PostgreSQL/MySQL/SQLite (database)

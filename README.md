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


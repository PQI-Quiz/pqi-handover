# PQI Quiz

An interactive online personality quiz built with React on the frontend and Node.js/Express on the backend. Includes email functionality to send quiz results to users.

## Features

- Multiple-choice personality quiz
- Custom results based on user answers
- Sends quiz results to user via email
- Responsive design for mobile & desktop
- Hosted frontend on Github Pages
- Hosted backend on Render

## Project Architecture

- **Frontend (React on GitHub Pages)**

  - Serves the quiz UI
  - Sends user answers to backend via `POST /send-results`

- **Backend (Node.js/Express on Render)**

  - Receives quiz answers
  - Calculates results
  - Sends result to user via email using Nodemailer

- **Email**
  - Configured using SMTP (Gmail)
  - Triggered by backend when results are submitted

## Live Site

[PQI Quiz](https://quiz.theschoolofplay.org)

## About

Frontend is currently hosted on [Github Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages) through this [repo](https://github.com/s111ew/pqi-frontend).

Backend is currently hosted on [Render](https://render.com) through this [repo](https://github.com/s111ew/pqi-backend).

## Pushing Updates

Frontend:

```
npm run deploy
```

Backend:

```
git push origin main
```

## Cloning the repository

If you need to make a copy of this code, to work on or to move hosting to a new provider for example:

### Clone the repositories

```
git clone https://github.com/s111ew/pqi-frontend.git
cd pqi-frontend
```

```
git clone https://github.com/s111ew/pqi-backend.git
cd pqi-backend
```

### Install Dependencies

```
cd pqi-frontend
npm install
npm run dev
```

```
cd pqi-backend
npm install
npm run dev
```

### Add Environment Variables

The backend repository has hidden environment variables used to configure the email functionality. They are added to the project on [Render](https://render.com) (Render.com > Service > Environment > Environment Variables) or can live in a .env file for some other hosting providers.

The (example) environment variables are as follows:

```
FROM_EMAIL=your@email.com
SMTP_HOST=smtp.mailprovider.com
SMTP_USER=your@email.com
SMTP_PORT=587
SMTP_PASS=yourpassword
```

## Troubleshooting

- CORS issues? Make sure frontend URL is allowed in backend settings.

- Emails not sending? Check SMTP credentials or logs in backend console.

- Render service not waking up? Free tier services may sleep after inactivity.

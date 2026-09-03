# planforinclusion
Landing Page for a PDF download

## Project Structure

```text
├── config/               # Database and app configurations (Non-public)
├── includes/             # Reusable header, footer, and helper functions (Non-public)
└── public/               # The Web Root (Only this folder is exposed to the internet)
    ├── assets/           # Frontend CSS, JS, and image files
    ├── index.php         # Homepage
    ├── about.php         # About Page
    └── contact.php       # Contact Page
```

## Security Design

The backend logic (`config/` and `includes/`) is isolated away from the `public/` directory. When deploying this project, ensure your web server configuration (Apache or Nginx) points its **Document Root** directly to the `public/` folder. This prevents users from accessing sensitive backend files via the URL.

## Setup Instructions

1. Clone the repository to your local server directory.
2. Duplicate the `.env.example` file and rename it to `.env`.
3. Open `.env` and fill in your local database credentials.
4. Point your local environment (like XAMPP, MAMP, or Docker) to the `public/` folder.

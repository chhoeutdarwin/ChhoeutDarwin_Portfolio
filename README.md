# Darwin Portfolio

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=fff)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=fff)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=000)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Node.js](https://img.shields.io/badge/Node.js-20%2B-339933?logo=node.js&logoColor=fff)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express.js-000?logo=express&logoColor=fff)](https://expressjs.com/)

A responsive personal portfolio website for **Chhoeut Darwin**, a Full-Stack Web Developer. The site presents selected projects, professional experience, technical skills, achievements, and ways to get in touch through a clean, modern interface.

## Overview

Darwin Portfolio is designed to make professional work easy to explore on any screen size. Visitors can learn about Darwin's background, browse featured work with project and repository links, download a CV, and send an inquiry through the contact form.

The current repository uses a static HTML/CSS/JavaScript frontend served by an Express.js server. The server also provides the contact form API and Gmail email delivery.

## Features

- Responsive, modern UI/UX for desktop and mobile devices
- Light and dark theme switching
- Hero section with professional introduction and social links
- About, experience, skills, projects, and contact sections
- Featured project cards with live and source-code links
- Downloadable CV
- Contact form with server-side validation
- Health-check endpoint for the backend
- Accessible navigation with skip-to-content support and semantic markup

## Technology Stack

### Current implementation

- **Frontend:** HTML5, CSS3, vanilla JavaScript
- **Backend:** Node.js, Express.js
- **Email delivery:** Nodemailer with Gmail SMTP
- **Development tools:** Git, GitHub, Figma

### Full-stack technologies

The portfolio highlights experience across the following technologies:

- **Frontend:** React, Next.js, Tailwind CSS
- **Backend:** Node.js, Express.js
- **Database and ORM:** MySQL, Prisma ORM
- **Tools and version control:** Git, GitHub, Figma

> React, Next.js, Tailwind CSS, MySQL, and Prisma are part of the broader technology profile presented by the portfolio; they are not required dependencies for the current static portfolio implementation.

## Project Structure

```text
my-portfolio/
├── assets/
│   ├── cv/              # CV and related files
│   └── img/             # Portfolio images and artwork
├── css/
│   └── styles.css       # Site styles and responsive layouts
├── js/
│   └── script.js        # Client-side interactions
├── index.html           # Main portfolio page
├── server.js            # Express server and contact API
├── package.json         # Scripts and dependencies
└── .env                 # Local environment variables (not committed)
```

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) 20 or newer
- npm

### Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd my-portfolio
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the development server:

   ```bash
   npm start
   ```

4. Open [http://localhost:5000](http://localhost:5000) in your browser.

## Contact Form Configuration

The portfolio can send contact form submissions through Gmail. To enable email delivery, create a `.env` file in the project root:

```env
PORT=5000
EMAIL_USER=your-gmail-address@gmail.com
EMAIL_PASS=your-16-character-gmail-app-password
EMAIL_TO=recipient@example.com
```

Use a Gmail App Password rather than your regular Gmail password. If these variables are not configured, the website still loads, but the contact API will report that the email service is unavailable.

## Available Endpoints

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/health` | Returns the server health status |
| `POST` | `/api/contact` | Validates and sends a contact form message |

The contact endpoint expects a JSON body containing `name`, `email`, and `message`.

## Customization

- Update content and links in `index.html`.
- Adjust visual design and responsive behavior in `css/styles.css`.
- Update theme controls and interactive behavior in `js/script.js`.
- Replace project images in `assets/img/`.
- Replace the downloadable CV at `assets/cv/Resume.pdf`.

## License

This project is maintained as a personal portfolio. Contact the author before reusing its content, images, or design assets.

## Contact

For professional inquiries, use the contact form on the website or connect through the social links displayed in the portfolio.

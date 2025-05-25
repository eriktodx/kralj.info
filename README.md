# kralj.info

[![Deploy to Firebase Hosting](https://github.com/eriktodx/kralj.info/actions/workflows/firebase-hosting-merge.yml/badge.svg)](https://github.com/eriktodx/kralj.info/actions/workflows/firebase-hosting-merge.yml)

My personal website and portfolio showcasing my work as a Freelance Full-Stack Software Developer and System Administrator.

## Overview

This repository contains the source code for my personal website, [kralj.info](https://kralj.info). The site serves as a portfolio to highlight my skills, experience, and contact information. It is a static website hosted on Firebase Hosting with automated deployments managed via GitHub Actions.

### Features

- **Responsive Design**: Optimized for both desktop and mobile devices with light/dark mode support.
- **SEO Optimization**: Includes meta tags, Open Graph, and Twitter Card data for better visibility on search engines and social media.
- **Structured Data**: Implements JSON-LD for improved search engine understanding.
- **Analytics**: Integrated with Firebase Analytics for tracking page views.
- **Public SSH Keys**: Provides access to my public SSH keys for secure communication.

## Project Structure

```
kralj.info/
├── .firebaserc                # Firebase project configuration
├── .github/                   # GitHub Actions workflows for deployment
│   └── workflows/
│       ├── firebase-hosting-merge.yml       # Deployment on merge to main
│       └── firebase-hosting-pull-request.yml # Preview deployment on PR
├── .gitignore                 # Git ignore file
├── firebase.json              # Firebase Hosting configuration
├── public/                    # Static files for hosting
│   ├── assets/                # Images and other assets
│   │   └── images/
│   │       ├── favicon.webp
│   │       ├── apple-touch-icon.webp
│   │       └── profile_picture.webp
│   ├── id_ed25519            # Public ED25519 SSH key
│   ├── id_rsa                # Public RSA SSH key
│   ├── index.html            # Main HTML file
│   └── sitemap.xml           # Sitemap for SEO
├── LICENSE                   # MIT License file
└── README.md                 # Project documentation
```

## Setup

This project is a static website and does not require a complex build process. However, if you wish to run or modify it locally, follow these steps:

### Prerequisites

- [Firebase CLI](https://firebase.google.com/docs/cli) (optional, for local development or deployment)
- A modern web browser for testing

### Local Development

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/eriktodx/kralj.info.git
   cd kralj.info
   ```

2. **Serve Locally**:
   You can use any static file server to preview the site locally. For example, using Python's built-in server:
   ```bash
   python3 -m http.server 8080 --directory public
   ```
   Then, open your browser and navigate to `http://localhost:8080`.

3. **Firebase Emulator (Optional)**:
   If you have the Firebase CLI installed, you can use the Firebase Hosting emulator:
   ```bash
   firebase emulators:start
   ```
   This will serve the site at `http://localhost:5000`.

## Deployment

Deployment is fully automated via GitHub Actions. Every push to the `main` branch triggers a deployment to Firebase Hosting.

### GitHub Actions Workflows

- **Deploy on Merge**: Defined in `.github/workflows/firebase-hosting-merge.yml`, this workflow deploys the site to the live channel on Firebase Hosting when changes are pushed to the `main` branch.
- **Deploy on Pull Request**: Defined in `.github/workflows/firebase-hosting-pull-request.yml`, this workflow creates a preview deployment for pull requests.

### Manual Deployment

If you need to deploy manually, ensure you have the Firebase CLI installed and are logged in:

1. Install Firebase CLI (if not already installed):
   ```bash
   npm install -g firebase-tools
   ```

2. Login to Firebase:
   ```bash
   firebase login
   ```

3. Deploy to Firebase Hosting:
   ```bash
   firebase deploy
   ```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

Feel free to reach out to me through any of the following channels:

- **Email**: [erik@kralj.info](mailto:erik@kralj.info)
- **LinkedIn**: [linkedin.com/in/kraljerik](https://www.linkedin.com/in/kraljerik)
- **GitHub**: [github.com/eriktodx](https://github.com/eriktodx)
- **Twitter**: [x.com/KraljErik](https://x.com/KraljErik)
- **Company Page**: [linkedin.com/company/erik-kralj-sp](https://linkedin.com/company/erik-kralj-sp)

## SSH Public Keys

For secure communication or collaboration, you can access my public SSH keys:

- **ED25519**: [id_ed25519](https://kralj.info/id_ed25519)
- **RSA**: [id_rsa](https://kralj.info/id_rsa)

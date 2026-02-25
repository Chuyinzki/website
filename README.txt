Jesus Villegas - Personal Website

This repository contains my personal website and portfolio.

About
- Senior Software Engineer profile site with experience, competencies, and contact information.
- Built as a static website for reliability, fast global delivery, and low maintenance.

Tech Stack
- Frontend: HTML, CSS, JavaScript (static site template customized with my content)
- Hosting: AWS S3
- CDN: AWS CloudFront
- SSL: AWS Certificate Manager (ACM)
- DNS: AWS Route 53
- Domain Registrar: Namecheap
- CI/CD: GitHub Actions using OIDC to assume an AWS IAM role (no long-lived AWS secrets in repo)

Repository Structure
- site/                  Deployable static files
- site/index.html        Main page
- site/assets/           CSS, JS, fonts
- site/images/           Images
- .github/workflows/     Deployment workflow (not deployed to S3)

Deployment Flow
GitHub -> OIDC -> AWS IAM Role -> S3 -> CloudFront -> Route 53 -> User

Deployment Notes
- GitHub Actions deploys only the `site/` folder to S3.
- CloudFront invalidation runs after deployment so updates are visible quickly.

Local Preview
- Open `site/index.html` in a browser.

Repository
- Source: https://github.com/Chuyinzki/website

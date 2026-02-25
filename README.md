# Jesus Villegas - Personal Website

Senior software engineer portfolio site focused on speed, reliability, and low operational overhead.

[![Site Type](https://img.shields.io/badge/Site-Static-blue)](#)
[![Hosting](https://img.shields.io/badge/Hosting-AWS%20S3-orange)](#)
[![CDN](https://img.shields.io/badge/CDN-CloudFront-9cf)](#)
[![CI/CD](https://img.shields.io/badge/CI%2FCD-GitHub%20Actions-black)](#)

## Overview

- Personal website and portfolio repository
- Highlights experience, competencies, and contact details
- Built as a static site for simple maintenance and global delivery

## Tech Stack

| Area | Tools/Services |
| --- | --- |
| Frontend | HTML, CSS, JavaScript |
| Hosting | AWS S3 |
| CDN | AWS CloudFront |
| SSL | AWS Certificate Manager (ACM) |
| DNS | AWS Route 53 |
| Domain Registrar | Namecheap |
| CI/CD | GitHub Actions + OIDC -> AWS IAM Role |

> Security note: No long-lived AWS secrets are stored in this repository.

## Repository Structure

```text
site/                  Deployable static files
site/index.html        Main page
site/assets/           CSS, JS, fonts
site/images/           Images
.github/workflows/     Deployment workflow (not deployed to S3)
```

## Deployment Flow

```text
GitHub -> OIDC -> AWS IAM Role -> S3 -> CloudFront -> Route 53 -> User
```

## Deployment Notes

- GitHub Actions deploys only the `site/` folder to S3
- CloudFront invalidation runs after deployment so updates appear quickly

## Local Preview

Open `site/index.html` in your browser.

## Repository

- Source: [github.com/Chuyinzki/website](https://github.com/Chuyinzki/website)

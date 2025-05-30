# Frontend CI/CD Pipeline with DevSecOps

![GitLab CI/CD](https://img.shields.io/badge/GitLabCI-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)

A secure CI/CD pipeline for React applications implementing DevSecOps best practices with GitLab CI/CD.

## Features

- **Automated Build & Test Pipeline**
- **Security Scanning** (SAST, Dependency Scanning)
- **Docker-based Execution**
- **GitLab Pages Deployment**
- **Vulnerability Management**

## Pipeline Stages

| Stage | Tools | Description |
|-------|-------|-------------|
| Install | npm | Dependency installation with audit |
| Build | React Scripts | Production-optimized build |
| Test | Jest | Unit test execution |
| Security | GitLab SAST, npm audit | Vulnerability scanning |
| Deploy | GitLab Pages | Static hosting |

## Setup

### Prerequisites
- GitLab account
- Node.js 18+
- Docker (for local testing)

### Installation
```bash
git clone https://gitlab.com/fawry-intern1/anas_ayman_elgalad/q2_frontend-cicd-project_finale.git
cd q2_frontend-cicd-project_finale/frontend
npm install
```

## Pipeline Configuration

Key configurations in `.gitlab-ci.yml`:
```yaml
variables:
  APP_DIR: "frontend"
  NODE_VERSION: "18"
  
stages:
  - install
  - build
  - test
  - security
  - deploy
```

## Security Features
- Dependency scanning with `npm audit`
- GitLab SAST integration
- Container scanning (future implementation)
- **Note:** Linting will be implemented in future iterations

## Pipeline Flow Success
Succeeded Pipeline & RepoLink: https://gitlab.com/fawry-intern1/anas_ayman_elgalad/q2_frontend-cicd-project_finale
![alt text](<Screenshot from 2025-05-26 00-37-07.png>)

## Future Improvements
- [ ] Implement ESLint integration
- [ ] Add DAST scanning
- [ ] Kubernetes deployment
- [ ] Performance testing


### Recommended Repository Structure:
```
README.md
frontend/
├── src/
├── package.json
.gitlab-ci.yml
```

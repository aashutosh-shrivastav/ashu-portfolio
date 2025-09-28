
# DevOps & Deployment Guide

## Purpose
Document how to build, test, and deploy the Candidate's portfolio project for both UI and API.

## Local Development
- Run Angular UI: `npm start` in `/ui`
- Run Spring Boot API: `./mvnw spring-boot:run` in `/api`
- Use Docker Compose for local orchestration (optional)

## Deployment
- UI: Vercel, Netlify, or static hosting
- API: Render, Fly.io, or cloud VM
- Dockerize both UI and API for portability

## CI/CD
- GitHub Actions for build, test, deploy
- Separate workflows for UI and API
- Environment variables and secrets management

## Monitoring & Maintenance
- Basic health checks
- Logging best practices
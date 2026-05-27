# mvp-launch-checklist
The checklist we wish we had before launching our first MVP. Architecture, security, testing, deployment and more.
# MVP Launch Checklist

A practical checklist for founders and engineering teams building their first product. Based on real experience shipping MVPs across fintech, AI, and SaaS industries.

No fluff. Just the things that actually matter before you go live.

> Compiled by the team at [Pollume](https://pollume.com) — a software development company that helps startups build and ship products.

---

## Table of Contents

- [Before You Write a Single Line of Code](#before-you-write-a-single-line-of-code)
- [Architecture Decisions](#architecture-decisions)
- [Database](#database)
- [API Design](#api-design)
- [Security Basics](#security-basics)
- [Frontend](#frontend)
- [Testing](#testing)
- [Deployment and Infrastructure](#deployment-and-infrastructure)
- [Before Launch](#before-launch)
- [After Launch](#after-launch)

---

## Before You Write a Single Line of Code

- [ ] You can describe the core problem in one sentence
- [ ] You know exactly who your first 10 users are
- [ ] You have defined what "done" looks like for v1
- [ ] You have stripped the feature list down to the absolute minimum
- [ ] You have mapped out the data your product needs to store and process
- [ ] You have chosen a tech stack based on your team's strengths, not trends
- [ ] You have set a deadline and a budget, even rough ones

> The biggest mistake teams make is building features nobody asked for. Define your one core action the user needs to complete, and build only that.

---

## Architecture Decisions

- [ ] You have decided between monolith and microservices (hint: start with a monolith)
- [ ] Your codebase is organized into clear modules with separated business logic
- [ ] You have avoided premature optimization and over-engineering
- [ ] Dependencies between modules are explicit and minimal
- [ ] You have a plan for how the architecture scales if traffic spikes 10x
- [ ] Configuration is separated from code (env variables, not hardcoded values)
- [ ] You are not building microservices for a team of 2-3 people

> Shopify ran on a Rails monolith and handled 173 billion requests during Black Friday 2024. You do not need distributed architecture on day one.

---

## Database

- [ ] Your data models reflect actual business logic, not just what felt natural to code
- [ ] Relationships between tables are clearly defined
- [ ] Indexes are added on columns you will query frequently
- [ ] You have thought about what happens when a table has 1 million rows
- [ ] You are not storing things you will never need
- [ ] Migrations are version controlled and reversible
- [ ] You have set up regular automated backups
- [ ] Sensitive data is encrypted at rest

> Poor database design is one of the most common reasons teams end up rewriting everything 6 months in. Take an extra day to get the schema right.

---

## API Design

- [ ] Endpoints follow a consistent naming convention (REST or GraphQL, pick one)
- [ ] API responses use a consistent structure across all endpoints
- [ ] Versioning is in place from day one (`/api/v1/...`)
- [ ] Error responses include meaningful messages, not just status codes
- [ ] Authentication is required on all non-public endpoints
- [ ] You have documented what each endpoint accepts and returns
- [ ] Rate limiting is configured
- [ ] Your internal database schema is not directly exposed through the API

---

## Security Basics

- [ ] Passwords are hashed with bcrypt or argon2 (never stored in plain text)
- [ ] All user input is validated and sanitized
- [ ] SQL injection is not possible (use parameterized queries or an ORM)
- [ ] HTTPS is enforced everywhere
- [ ] API keys and secrets are stored in environment variables, not in the codebase
- [ ] CORS is configured to allow only trusted origins
- [ ] Authentication tokens have expiry dates
- [ ] You have a plan for what happens if credentials are leaked

---

## Frontend

- [ ] The app works on mobile and desktop
- [ ] Core user flow is under 3 steps
- [ ] Loading states are handled (users see feedback when something is happening)
- [ ] Error states are handled (users see a useful message when something goes wrong)
- [ ] Forms validate input before sending it to the server
- [ ] The app does not break with slow internet
- [ ] Images are compressed and assets are optimized
- [ ] You have tested the app in at least 2 different browsers

---

## Testing

- [ ] Critical business logic has unit tests
- [ ] The main user flow has at least one end-to-end test
- [ ] You can run the full test suite in under 5 minutes
- [ ] Tests run automatically on every pull request
- [ ] You have tested what happens when the database is unavailable
- [ ] You have tested what happens when a third-party API is down

> You do not need 100% test coverage. You need coverage on the parts that would hurt most if they broke.

---

## Deployment and Infrastructure

- [ ] The app deploys from a single command or a CI/CD pipeline
- [ ] Production and staging environments are separate
- [ ] You can roll back a deployment if something goes wrong
- [ ] Application logs are collected somewhere you can actually search them
- [ ] You have uptime monitoring and it will alert you if the app goes down
- [ ] You know your expected cloud costs for the first 3 months
- [ ] Database backups are automated and you have tested restoring from one

---

## Before Launch

- [ ] You have done a full walkthrough of the product as a new user
- [ ] There are no broken links or placeholder text visible to users
- [ ] Error tracking is set up (Sentry or similar)
- [ ] Analytics are in place so you can measure the core action users take
- [ ] Terms of service and privacy policy exist
- [ ] You have a way for users to contact you or report a bug
- [ ] At least 5 real people outside your team have used the product and given feedback
- [ ] You know what metric you are watching in the first 30 days after launch

---

## After Launch

- [ ] You are watching error logs daily for the first 2 weeks
- [ ] You have a process for collecting and reviewing user feedback
- [ ] You have allocated time in your sprint to address technical debt (even 10% helps)
- [ ] You are not adding new features until you understand why users drop off
- [ ] You have a plan for your next iteration based on real usage data

---

## Further Reading

- [How to Build an MVP: Architecture Guide for 2026](https://pollume.com/blog/build-an-mvp-architecture-guide) by Pollume
- [No-Code vs Custom Development for MVPs](https://pollume.com/blog/no-code-vs-custom-development-mvp) by Pollume
- [The True Cost of Software Rewrites](https://8thlight.com/insights/the-true-cost-of-rewrites) by 8th Light

---

## Contributing

Found something missing or outdated? Open a PR. This checklist is meant to grow with real-world experience.

---

## About Pollume

[Pollume](https://pollume.com) is a software development company that helps startups and businesses build scalable web applications, integrate AI, and ship MVPs. We work as a dedicated technical partner from concept to launch.

Want help shipping your MVP? [Book a free call](https://calendly.com/pollume/30min).

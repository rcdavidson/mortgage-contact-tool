# Dev Notes for Mortgage Broker Lender Contact Tool

## Project Overview

This project is a web-based tool designed specifically for mortgage brokers to access, manage, and interact with lender contact information. It includes features for team collaboration, user-specific notes and contact history, and multiple access levels for data management.

## Objectives

- Build a database of lenders and associated BDMs (Business Development Managers)
- Enable easy access to lender contact options
- Support team and user-specific notes and preferences
- Provide a modern, responsive front-end interface for desktop and mobile use

## Project Structure

```
project-root/
├── frontend/                   # Frontend application (React/Tailwind preferred)
├── backend/                    # Backend (Node.js/Express or Django/FastAPI)
├── database/                  # DB schema and seed files (PostgreSQL preferred)
├── docs/                      # Documentation
├── .env                       # Environment variables (never commit)
├── .gitignore
├── README.md
└── dev-notes.md               # This file
```

## UI/UX Design Recommendations

- Use TailwindCSS for fast, modern, responsive UI
- Mobile-first design, with grid layout for lender cards
- Framer Motion for animations and microinteractions
- Light/Dark mode support
- Accessibility (WCAG AA compliance)
- Use ShadCN UI or similar component libraries

## Data Models

### Lenders

- `id`
- `name`
- `logo_url`
- `website_url`
- `email`
- `criteria_url`
- `livetalk_url`
- `notes`

### BDMs (Business Development Managers)

- `id`
- `lender_id` (foreign key)
- `name`
- `email`
- `phone_number`
- `contact_type` ("Field" | "Telephone")
- `notes`
- `team_id` or `user_id` (ownership)

### Users

- `id`
- `name`
- `email`
- `team_id`
- `role` ("Admin", "Editor", "Viewer")

### Teams

- `id`
- `name`
- `admin_user_id`

### Enquiries

- `id`
- `user_id`
- `lender_id`
- `contact_method` ("Email", "LiveTalk", etc.)
- `result` ("Yes", "No", "Maybe")
- `notes`
- `timestamp`

## Permissions & Access

- Admin: Full access, team-wide editing/saving
- Editor: Can edit and save to team or self
- Viewer: Can only view and save to self

## Features

- User onboarding (select/join team or create new)
- Lender grid view with filtering
- Contact options: mailto link, live chat, etc.
- Compose form: email-style with BCC support
- Click tracking and enquiry history
- Notes storage per user/team context
- Responsive web design

## Dev Standards & Rules

- Use semantic HTML and clean, readable code
- Use Git for version control
  - Follow `main` and `dev` branches
  - Use `feat/`, `fix/`, `docs/`, `refactor/` naming
  - Include clear commit messages and version tags
- Use `.env` files for configuration (keep out of version control)
- Use Prettier + ESLint for code consistency
- Add unit tests where relevant (e.g., Jest)
- Document endpoints and DB schemas

## Versioning & Housekeeping

- Initial version: `v0.1.0`
- Use semantic versioning: `MAJOR.MINOR.PATCH`
- Add changelog in `docs/CHANGELOG.md`
- Regular commits to GitHub/GitLab
- Document setup and run instructions in `README.md`

## TODO

-

## Notes

- Prioritize simplicity and clarity for everyday users
- Ensure scalability for large teams and multiple users per lender
- Consider GDPR compliance for user data and contact info

---

**Cursor Instructions:**

- Adhere to the structure and standards above
- Create a `v0.1.0` tag on the first working commit
- Track all tasks and progress with version control
- Focus on modular, scalable architecture
- Prioritize user experience, speed, and data security 
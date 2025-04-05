# Mortgage Contact Tool

A tool for managing mortgage lender contacts and business development managers (BDMs).

## Project Structure

```
mortgage-contact-tool/
├── frontend/     # React + TailwindCSS frontend
├── backend/      # Node.js/Express or FastAPI backend
├── database/     # Database migrations and schemas
├── docs/         # Project documentation
├── dev-notes.md  # Development notes and guidelines
├── .gitignore    # Git ignore rules
└── README.md     # This file
```

## Tech Stack

- Frontend: React + TailwindCSS
- Backend: Node.js/Express or FastAPI
- Database: PostgreSQL/Supabase
- Authentication: TBD

## Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn
- Python 3.8+ (if using FastAPI)
- PostgreSQL (if using local database)

### Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   # Frontend
   cd frontend
   npm install

   # Backend
   cd ../backend
   npm install  # or pip install -r requirements.txt
   ```

3. Set up environment variables:
   - Copy `.env.example` to `.env`
   - Fill in the required environment variables

4. Start the development servers:
   ```bash
   # Frontend
   cd frontend
   npm run dev

   # Backend
   cd ../backend
   npm run dev  # or python main.py
   ```

## Development Guidelines

See `dev-notes.md` for detailed development guidelines, including:
- Code style standards
- Git workflow
- API documentation
- Database schema
- UI/UX guidelines

## License

[Add your license here] 
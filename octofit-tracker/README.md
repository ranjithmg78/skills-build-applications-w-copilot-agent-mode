# 🐙 OctoFit Tracker

A modern multi-tier fitness tracking application built with React 19, Express, Node.js, and MongoDB.

## Project Structure

```
octofit-tracker/
├── frontend/           # React 19 + Vite application
│   ├── src/
│   ├── vite.config.ts
│   ├── tsconfig.json
│   └── package.json
├── backend/            # Express + TypeScript API
│   ├── src/
│   │   ├── index.ts
│   │   └── models/
│   ├── tsconfig.json
│   └── package.json
└── .env.example        # Environment variables
```

## Prerequisites

- Node.js 18+ 
- npm or yarn
- MongoDB (local or Docker)

## Port Configuration

- **Frontend**: http://localhost:5173 (Vite dev server)
- **Backend**: http://localhost:8000 (Express API)
- **MongoDB**: localhost:27017 (Default MongoDB port)

## Installation

### 1. Setup MongoDB

Using Docker:
```bash
docker run -d -p 27017:27017 --name mongodb mongo:latest
```

Or install locally: [MongoDB Community Edition](https://docs.mongodb.com/manual/installation/)

### 2. Setup Backend

```bash
cd octofit-tracker/backend
npm install
npm run dev
```

The backend API will be available at `http://localhost:8000`

### 3. Setup Frontend

```bash
cd octofit-tracker/frontend
npm install
npm run dev
```

The frontend will be available at `http://localhost:5173`

## Development

### Backend Development

```bash
cd backend
npm run dev      # Start development server with hot reload
npm run build    # Compile TypeScript
npm run watch    # Watch TypeScript changes
```

### Frontend Development

```bash
cd frontend
npm run dev      # Start Vite dev server
npm run build    # Build for production
npm run preview  # Preview production build
```

## API Endpoints

### Health Check
- `GET /api/health` - API health status

### Features (To be implemented)
- User management
- Workout tracking
- Goal setting
- Progress reports

## Technologies

- **Frontend**: React 19, Vite, TypeScript
- **Backend**: Express.js, Node.js, TypeScript
- **Database**: MongoDB with Mongoose ODM
- **Styling**: CSS3

## Models

### User
- `username`: Unique username
- `email`: User email
- `goals`: Array of fitness goals
- `timestamps`: Created and updated dates

### WorkoutSession
- `userId`: Reference to User
- `exerciseName`: Name of the exercise
- `duration`: Duration in minutes
- `calories`: Calories burned
- `intensity`: Low, Medium, or High
- `notes`: Optional notes
- `timestamps`: Created and updated dates

## Environment Variables

Copy `.env.example` to `.env` and update as needed:

```bash
cp .env.example .env
```

## Contributing

1. Create a new branch for your feature
2. Make your changes
3. Push to your branch
4. Create a Pull Request

## License

MIT

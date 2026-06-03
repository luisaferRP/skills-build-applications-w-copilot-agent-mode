# OctoFit Tracker

A modern multi-tier fitness tracking application built with React 19, Node.js/Express, and MongoDB.

## Architecture

```
octofit-tracker/
├── frontend/          # React 19 + Vite frontend application
│   ├── src/
│   ├── package.json
│   └── vite.config.ts
└── backend/           # Node.js + Express + TypeScript backend API
    ├── src/
    │   └── index.ts   # Main server entry point
    ├── package.json
    └── tsconfig.json
```

## Technology Stack

### Frontend
- **React 19**: Latest React framework with modern hooks and features
- **Vite**: Lightning-fast build tool and dev server
- **Port**: 5173

### Backend
- **Node.js + Express**: RESTful API server
- **TypeScript**: Type-safe backend development
- **Mongoose**: MongoDB object modeling
- **Port**: 8000

### Database
- **MongoDB**: NoSQL database for flexible data storage
- **Port**: 27017

## Setup Instructions

### Prerequisites
- Node.js (v18+)
- npm (v10+)
- MongoDB (running locally or remote connection)

### Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

The frontend will be available at `http://localhost:5173`

### Backend Setup

```bash
cd backend
npm install
npm run dev
```

The backend API will be available at `http://localhost:8000`

### Environment Configuration

Copy `.env.example` files to `.env` in both directories:

**Backend (.env)**
```
NODE_ENV=development
PORT=8000
MONGODB_URI=mongodb://localhost:27017/octofit-tracker
```

**Frontend (.env.local)**
```
VITE_API_URL=http://localhost:8000
```

## Development

### Frontend Development
```bash
cd frontend
npm run dev      # Start dev server
npm run build    # Build for production
npm run preview  # Preview production build
```

### Backend Development
```bash
cd backend
npm run dev      # Start with hot reload (nodemon + ts-node)
npm run build    # Compile TypeScript to JavaScript
npm run start    # Run compiled version
```

## Project Structure

### Frontend
- `src/`: React components, pages, and utilities
- `public/`: Static assets
- `vite.config.ts`: Vite configuration
- `index.html`: HTML entry point

### Backend
- `src/`: TypeScript source files
- `dist/`: Compiled JavaScript output
- `tsconfig.json`: TypeScript configuration
- `package.json`: Dependencies and scripts

## API Endpoints

- `GET /api/health`: Health check endpoint

## MongoDB Connection

Default MongoDB connection: `mongodb://localhost:27017/octofit-tracker`

To use a remote MongoDB (e.g., MongoDB Atlas), update the `MONGODB_URI` in your `.env` file.

## Next Steps

1. Start MongoDB locally or connect to a remote instance
2. Run `npm run dev` in the backend directory
3. Run `npm run dev` in the frontend directory
4. Begin building your fitness tracking features!

## License

MIT

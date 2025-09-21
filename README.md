# React Events Management

A full-stack events management application built with React and Express.js that allows users to view, create, edit, and search for events. The application features a modern React frontend with routing capabilities and a RESTful Express.js backend that stores data in JSON files.

## Features

- **View Events**: Browse a list of recently added events with details like title, date, location, and images
- **Create Events**: Add new events with a comprehensive form including title, description, date, time, location, and image selection
- **Edit Events**: Modify existing event details through an intuitive editing interface
- **Search & Filter**: Find specific events using search functionality with filtering capabilities
- **Event Details**: View detailed information about individual events
- **Image Management**: Upload and manage event images through a built-in image picker
- **Responsive Design**: Modern, responsive UI that works across different screen sizes

## Tech Stack

### Frontend
- **React 19** - Modern React with latest features
- **React Router v6.15.0** - Client-side routing and navigation
- **Vite** - Fast build tool and development server
- **ESLint** - Code linting and quality assurance
- **CSS** - Custom styling with modern CSS features

### Backend
- **Express.js** - Web application framework for Node.js
- **Body-parser** - Middleware for parsing request bodies
- **CORS** - Cross-origin resource sharing support
- **JSON File Storage** - Simple file-based data persistence

## Installation

### Prerequisites
- Node.js (version 14 or higher)
- npm or yarn package manager

### Frontend Setup
1. Clone the repository and navigate to the project root:
```bash
git clone <repository-url>
cd React_Query
```

2. Install frontend dependencies:
```bash
npm install
```

### Backend Setup
1. Navigate to the backend directory:
```bash
cd backend
```

2. Install backend dependencies:
```bash
npm install
```

## Usage

### Starting the Application

#### 1. Start the Backend Server
From the `backend` directory:
```bash
npm start
```
The backend server will start on `http://localhost:3000`

#### 2. Start the Frontend Development Server
From the project root directory:
```bash
npm run dev
```
The frontend will be available at `http://localhost:5173` (or another port if 5173 is occupied)

### Available Scripts

#### Frontend Scripts
- `npm run dev` - Start the development server
- `npm run build` - Build the application for production
- `npm run preview` - Preview the production build
- `npm run lint` - Run ESLint for code quality checks

#### Backend Scripts
- `npm start` - Start the Express.js server

## Project Structure

```
React_Query/
├── src/                          # Frontend source code
│   ├── components/               # React components
│   │   ├── Events/              # Event-related components
│   │   │   ├── Events.jsx       # Main events page
│   │   │   ├── EventDetails.jsx # Event details view
│   │   │   ├── NewEvent.jsx     # New event creation
│   │   │   ├── EditEvent.jsx    # Event editing
│   │   │   ├── EventForm.jsx    # Reusable event form
│   │   │   ├── EventItem.jsx    # Individual event display
│   │   │   ├── NewEventsSection.jsx # Recently added events
│   │   │   ├── FindEventSection.jsx # Search functionality
│   │   │   └── EventsIntroSection.jsx # Introduction section
│   │   ├── UI/                  # UI components
│   │   ├── Header.jsx           # Application header
│   │   └── ImagePicker.jsx      # Image selection component
│   ├── assets/                  # Static assets
│   ├── App.jsx                  # Main application component
│   ├── main.jsx                 # Application entry point
│   └── index.css                # Global styles
├── backend/                     # Backend source code
│   ├── data/                    # JSON data files
│   │   ├── events.json          # Events data storage
│   │   └── images.json          # Available images data
│   ├── public/                  # Static files served by Express
│   ├── app.js                   # Express server configuration
│   └── package.json             # Backend dependencies
├── public/                      # Frontend public assets
├── index.html                   # HTML template
├── package.json                 # Frontend dependencies
└── vite.config.js              # Vite configuration
```

## API Endpoints

The Express.js backend provides the following RESTful API endpoints:

### Events
- **GET** `/events` - Retrieve all events
  - Query parameters:
    - `search` - Filter events by search term
    - `max` - Limit the number of results
  - Response: `{ events: [...] }`

- **GET** `/events/:id` - Retrieve a specific event by ID
  - Response: `{ event: {...} }`
  - Returns 404 if event not found

- **POST** `/events` - Create a new event
  - Request body: `{ event: {...} }`
  - Response: `{ message: "Event saved.", event: {...} }`

### Images
- **GET** `/events/images` - Retrieve available event images
  - Response: `{ images: [...] }`

### Event Data Structure
```json
{
  "id": "string",
  "title": "string",
  "description": "string",
  "date": "YYYY-MM-DD",
  "time": "HH:MM",
  "location": "string",
  "image": "string"
}
```

## Development

### Code Quality
The project uses ESLint for maintaining code quality. Run linting with:
```bash
npm run lint
```

### Data Storage
Events are stored in `/backend/data/events.json` and images metadata in `/backend/data/images.json`. The backend serves static image files from the `/backend/public` directory.

### CORS Configuration
The backend is configured to accept requests from any origin during development. For production deployment, consider restricting CORS to specific domains.

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the ISC License.


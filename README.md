# Events Management App

A React + Express.js application for managing events with CRUD operations.

## Purpose

This project serves as a comprehensive learning platform for implementing React Query (TanStack Query) in a real-world scenario. It demonstrates how to manage server state, handle caching, and optimize data fetching in a full-stack events management system.

## Features

- **View Events**: Browse a list of recently added events with detailed information
- **Create New Events**: Add new events with title, description, date, time, location, and image selection
- **Edit Existing Events**: Modify event details through an intuitive form interface
- **Delete Events**: Remove events from the system
- **Search Functionality**: Find events by searching through titles, descriptions, and locations
- **Image Selection**: Choose from a curated collection of event images
- **Responsive Design**: Modern UI with loading states and error handling

## Technology Stack

### Frontend
- **React 19**: Latest React version with modern hooks and features
- **React Router DOM**: Client-side routing for single-page application navigation
- **Vite**: Fast build tool and development server with Hot Module Replacement (HMR)

### Backend
- **Express.js**: Web application framework for Node.js
- **Node.js**: JavaScript runtime for server-side development
- **Body Parser**: Middleware for parsing JSON request bodies

### Data Storage
- **JSON Files**: Simple file-based storage for events and images data
- **File System API**: Node.js fs/promises for asynchronous file operations

## Setup Instructions

### Prerequisites
- Node.js (version 14 or higher)
- npm or yarn package manager

### Backend Setup
1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Install backend dependencies:
   ```bash
   npm install
   ```

3. Start the backend server:
   ```bash
   npm start
   ```
   
   The backend server will run on `http://localhost:3000`

### Frontend Setup
1. Navigate to the project root directory:
   ```bash
   cd ..
   ```

2. Install frontend dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```
   
   The frontend application will be available at `http://localhost:5173`

### Running Both Servers
For the application to work properly, both the backend API server and the frontend development server must be running simultaneously in separate terminal windows.

## API Endpoints

The backend provides the following REST API endpoints:

### Events
- **GET /events** - Retrieve all events
  - Query parameters:
    - `search`: Filter events by title, description, or location
    - `max`: Limit the number of events returned
  
- **GET /events/:id** - Retrieve a specific event by ID
  - Returns event details with a 1-second delay (simulates network latency)

- **POST /events** - Create a new event
  - Request body: `{ event: { title, description, date, time, location, image } }`
  - Generates a unique ID for the new event

- **PUT /events/:id** - Update an existing event
  - Request body: `{ event: { title, description, date, time, location, image } }`
  - Returns updated event with a 1-second delay

- **DELETE /events/:id** - Delete an event
  - Returns success message with a 1-second delay

### Images
- **GET /events/images** - Retrieve available event images
  - Returns a list of image filenames for the image picker

## Development Workflow

1. **Start Backend**: Run `npm start` in the `/backend` directory
2. **Start Frontend**: Run `npm run dev` in the project root
3. **Development**: Make changes to React components in `/src`
4. **Testing**: Use the browser to test CRUD operations
5. **API Testing**: Backend endpoints can be tested with tools like Postman or curl

## Project Structure

```
├── backend/                 # Backend API server
│   ├── data/               # JSON data files
│   │   ├── events.json     # Events data storage
│   │   └── images.json     # Available images list
│   ├── public/             # Static assets served by Express
│   ├── app.js              # Express server configuration
│   └── package.json        # Backend dependencies
├── src/                    # Frontend React application
│   ├── components/         # React components
│   │   ├── Events/         # Event-related components
│   │   │   ├── Events.jsx          # Main events page layout
│   │   │   ├── EventDetails.jsx    # Event details view
│   │   │   ├── EventForm.jsx       # Reusable event form
│   │   │   ├── EventItem.jsx       # Individual event display
│   │   │   ├── NewEvent.jsx        # Create event page
│   │   │   ├── EditEvent.jsx       # Edit event page
│   │   │   ├── NewEventsSection.jsx # Recent events list
│   │   │   ├── FindEventSection.jsx # Search functionality
│   │   │   └── EventsIntroSection.jsx # Introduction section
│   │   ├── UI/             # Reusable UI components
│   │   │   ├── LoadingIndicator.jsx # Loading spinner
│   │   │   ├── ErrorBlock.jsx      # Error display
│   │   │   └── Modal.jsx           # Modal dialog
│   │   ├── Header.jsx      # Application header
│   │   └── ImagePicker.jsx # Image selection component
│   ├── App.jsx             # Main application with routing
│   ├── main.jsx            # Application entry point
│   └── index.css           # Global styles
└── README.md               # This file
```

## Component Descriptions

- **Events.jsx**: Main layout component that renders the events page with navigation
- **NewEventsSection.jsx**: Displays a list of recently added events with loading and error states
- **EventDetails.jsx**: Shows detailed information for a specific event (currently with placeholder content)
- **EventForm.jsx**: Reusable form component for creating and editing events
- **ImagePicker.jsx**: Allows users to select images from a predefined collection
- **LoadingIndicator.jsx**: Provides visual feedback during data loading
- **ErrorBlock.jsx**: Displays error messages with consistent styling

## Next Steps

This project is set up for implementing React Query to replace the current traditional state management approach. The existing components use `useState` and `useEffect` patterns that can be enhanced with React Query's powerful caching and synchronization features.

## Contributing

This is a learning project. Feel free to experiment with different React Query patterns and implementations to explore the library's capabilities.



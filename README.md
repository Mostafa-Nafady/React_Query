# React Events Management Application

A full-stack web application for managing events with complete CRUD (Create, Read, Update, Delete) functionality. Users can browse events, view event details, create new events, edit existing ones, and search through the event catalog.

## ✨ Features

- **Event Listing**: Browse all available events with a clean, organized interface
- **Event Details**: View comprehensive information about individual events
- **Create Events**: Add new events with title, description, date, time, location, and images
- **Edit Events**: Modify existing event information
- **Search Functionality**: Find specific events using search filters
- **Image Management**: Upload and manage event images
- **Responsive Design**: Works seamlessly across desktop and mobile devices
- **Loading States**: Smooth loading indicators for better user experience
- **Error Handling**: Comprehensive error handling with user-friendly messages

## 🛠️ Technology Stack

### Frontend
- **React 19** - Modern React with latest features
- **Vite** - Fast build tool and development server
- **React Router DOM v6.15.0** - Client-side routing
- **Custom CSS** - Styled with comprehensive custom stylesheets

### Backend
- **Express.js** - Node.js web framework
- **Body Parser** - Request body parsing middleware
- **File System API** - JSON-based data storage
- **CORS** - Cross-origin resource sharing support

### Development Tools
- **ESLint** - Code linting and quality assurance
- **Vite Dev Server** - Hot module replacement for development

## 📁 Project Structure

```
React_Query/
├── src/                          # Frontend source code
│   ├── components/               # React components
│   │   ├── Events/              # Event-related components
│   │   │   ├── Events.jsx       # Main events page
│   │   │   ├── EventDetails.jsx # Individual event details
│   │   │   ├── NewEvent.jsx     # Create new event
│   │   │   ├── EditEvent.jsx    # Edit existing event
│   │   │   ├── EventForm.jsx    # Reusable event form
│   │   │   ├── EventItem.jsx    # Event list item
│   │   │   └── ...              # Other event components
│   │   ├── UI/                  # Reusable UI components
│   │   ├── Header.jsx           # Application header
│   │   └── ImagePicker.jsx      # Image selection component
│   ├── App.jsx                  # Main application component
│   ├── main.jsx                 # Application entry point
│   └── index.css                # Global styles
├── backend/                     # Backend server
│   ├── data/                    # JSON data storage
│   │   ├── events.json          # Events data
│   │   └── images.json          # Image references
│   ├── public/                  # Static assets
│   ├── app.js                   # Express server
│   └── package.json             # Backend dependencies
├── public/                      # Frontend static assets
├── package.json                 # Frontend dependencies
└── vite.config.js              # Vite configuration
```

## 🚀 Installation & Setup

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn package manager

### Frontend Setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd React_Query
   ```

2. **Install frontend dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```

   The frontend will be available at `http://localhost:5173`

### Backend Setup

1. **Navigate to the backend directory**
   ```bash
   cd backend
   ```

2. **Install backend dependencies**
   ```bash
   npm install
   ```

3. **Start the backend server**
   ```bash
   npm start
   ```

   The backend API will be available at `http://localhost:3000`

### Running Both Servers

For full functionality, you need to run both the frontend and backend servers simultaneously:

1. **Terminal 1 - Backend**:
   ```bash
   cd backend
   npm start
   ```

2. **Terminal 2 - Frontend**:
   ```bash
   npm run dev
   ```

## 📖 Usage

### Browsing Events
- Navigate to the main page to see all available events
- View recently added events in the dedicated section
- Click on any event to see detailed information

### Creating Events
1. Click the "New Event" button
2. Fill in the event form with:
   - Event title
   - Description
   - Date and time
   - Location
   - Optional image
3. Submit the form to create the event

### Editing Events
1. Navigate to an event's detail page
2. Click the "Edit" button
3. Modify the event information
4. Save changes

### Searching Events
- Use the search functionality to find specific events
- Filter events based on various criteria

## 🔧 Development

### Available Scripts

#### Frontend Scripts
- `npm run dev` - Start development server with hot reload
- `npm run build` - Build the application for production
- `npm run preview` - Preview the production build locally
- `npm run lint` - Run ESLint for code quality checks

#### Backend Scripts
- `npm start` - Start the Express server

### API Endpoints

The backend provides the following REST API endpoints:

- `GET /events` - Retrieve all events
  - Query parameters:
    - `max` - Limit number of results
    - `search` - Search term for filtering events

- `GET /events/:id` - Get a specific event by ID
- `POST /events` - Create a new event
- `PUT /events/:id` - Update an existing event
- `DELETE /events/:id` - Delete an event

### Data Storage

Events are stored in JSON files located in the `backend/data/` directory:
- `events.json` - Contains all event data
- `images.json` - Contains image references and metadata

### Development Notes

- The application uses traditional fetch API with React hooks (useState, useEffect) for data management
- CORS is enabled on the backend to allow frontend-backend communication
- The project includes comprehensive error handling and loading states
- All routes are handled client-side using React Router

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the ISC License.

## 👨‍💻 Author

Backend developed by Maximilian Schwarzmüller (Academind GmbH)


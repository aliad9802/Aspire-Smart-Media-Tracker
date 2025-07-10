# My Media Tracker

A beautiful, full-stack web application for managing your personal media collection (movies, music, games) with AI-powered features and user authentication.

## Features

### Core Features
- **Complete Media Management**: Add, edit, delete, and organize your media collection
- **Status Tracking**: Track items as "Owned", "Wishlist", "Currently Using", or "Completed"
- **Advanced Search & Filtering**: Find media by title, creator, genre, type, and status
- **AI-Powered Metadata**: Auto-fill movie information using OMDB API
- **User Authentication**: Secure JWT-based authentication with registration and login
- **Real-time Analytics**: Visual dashboard with collection statistics and insights
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices

### Design Features
- **Modern Glass Morphism UI**: Beautiful backdrop blur effects and translucent elements
- **Smooth Animations**: Micro-interactions and transitions throughout the app
- **Dark Theme**: Elegant dark theme with gradient backgrounds
- **Typography**: Clean, readable fonts with proper hierarchy
- **Visual Feedback**: Hover states, loading states, and status indicators

## Tech Stack

- **Frontend**: React 18, TypeScript, Tailwind CSS
- **Backend**: Node.js, Express.js
- **Authentication**: JWT tokens, bcryptjs
- **Storage**: In-memory (easily upgradeable to PostgreSQL/MongoDB)
- **AI Integration**: OMDB API for movie metadata
- **Build Tool**: Vite
- **Icons**: Lucide React

## Getting Started

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd Media-Tracker
```
Note: don't forget to unzip the file

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

This will start both the backend server (port 3001) and frontend development server (port 5173).

4. Open your browser and navigate to `http://localhost:5173`

### Usage

1. **Register/Login**: Create an account or log in with existing credentials
2. **Add Media**: Click "Add Media" to add items to your collection
3. **AI Auto-fill**: Enter a movie title and type, then click "AI Auto-fill" to fetch metadata
4. **Track Status**: Update the status of your media items as you use them
5. **Search & Filter**: Use the search bar and filters to find specific items
6. **View Analytics**: Check your dashboard for collection insights

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user

### Media Management
- `GET /api/media` - Get user's media items
- `POST /api/media` - Add new media item
- `PUT /api/media/:id` - Update media item
- `DELETE /api/media/:id` - Delete media item

### AI Features
- `GET /api/metadata/:title?type=movie` - Fetch metadata for media item
-  intelligent title search and suggestions for movies

### Analytics
- `GET /api/analytics` - Get collection statistics

## Data Structure

Each media item contains:
- `title`: Name of the media
- `creator`: Director, artist, or developer
- `type`: movie, music, or game
- `releaseYear`: Year of release
- `genre`: Genre/category
- `status`: owned, wishlist, currently-using, or completed
- `notes`: Personal notes
- `rating`: 1-10 rating (optional)
- `plot`: Description or plot summary
- `poster`: Cover image URL
- `runtime`: Duration

## Environment Variables

The application uses default values for development. For production, set:
- `JWT_SECRET`: Secret key for JWT tokens
- `PORT`: Server port (default: 3001)

## Deployment

### Build for Production
```bash
npm run build
```

### Deploy to Netlify/Vercel
The frontend can be deployed to any static hosting service. The backend needs to be deployed separately to a service like Heroku, Railway, or DigitalOcean.

## Future Enhancements

- Database integration (PostgreSQL/MongoDB)
- Export/import functionality
- Social features (sharing collections)
- Mobile app version
- More AI integrations (music, games APIs)
- Advanced analytics and recommendations
- Offline support with PWA features

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, please open an issue on the GitHub repository or contact the development team.
# ShkeharVerse - Futuristic Real-time Chat Application

## Overview

This is a futuristic real-time chat application called "ShkeharVerse" built with React frontend and Express.js backend, featuring WebSocket communication for instant messaging. The application provides a sleek hacker lounge aesthetic with dark theme, neon accents, emoji reactions, message replies, and responsive design optimized for both desktop and mobile.

## User Preferences

Preferred communication style: Simple, everyday language.
Design aesthetic: Futuristic hacker lounge with dark theme, neon blue/purple accents, gaming stream vibe.
UI Requirements: Mobile and desktop friendly, floating message bubbles, glowing elements.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **Styling**: Tailwind CSS with shadcn/ui component library
- **State Management**: React Query (@tanstack/react-query) for server state
- **Routing**: Wouter for lightweight client-side routing
- **UI Components**: Radix UI primitives with custom styling

### Backend Architecture
- **Runtime**: Node.js with Express.js server
- **WebSocket**: ws library for real-time communication
- **Database**: PostgreSQL with Drizzle ORM
- **Session Storage**: connect-pg-simple for PostgreSQL session store
- **Data Validation**: Zod schemas for type-safe validation

### Project Structure
- `client/` - React frontend application
- `server/` - Express.js backend with WebSocket server
- `shared/` - Common schemas and types shared between frontend and backend

## Key Components

### Frontend Components
1. **Chat Interface**
   - `JoinModal` - User registration/join form
   - `ChatHeader` - Connection status and user count display
   - `MessageList` - Real-time message display with typing indicators
   - `MessageInput` - Message composition with typing detection
   - `UserSidebar` - Online users list with status indicators

2. **WebSocket Hook**
   - `useWebSocket` - Custom hook managing WebSocket connection, message handling, and reconnection logic

3. **UI Components**
   - Complete shadcn/ui component library integration
   - Responsive design with mobile-first approach
   - Dark mode support (configured but not actively used)

### Backend Components
1. **WebSocket Server**
   - Real-time message broadcasting
   - User presence management
   - Typing indicator coordination
   - Connection health monitoring

2. **Storage Layer**
   - `IStorage` interface for data operations
   - `MemStorage` in-memory implementation (development)
   - Database operations for users and messages

3. **Message Types**
   - User messages with rich metadata
   - System messages for join/leave notifications
   - Typing indicators
   - User status updates

## Data Flow

### User Join Flow
1. User enters display name in join modal
2. WebSocket connection established
3. User validation and avatar generation
4. Broadcast user join to all clients
5. Load recent message history

### Message Flow
1. User types in message input
2. Typing indicator sent to other users
3. Message validation on submission
4. Message stored in database
5. Message broadcasted to all connected clients
6. Message displayed in real-time

### Presence Management
1. Connection tracking for online status
2. Heartbeat mechanism for connection health
3. Automatic cleanup on disconnect
4. Status updates broadcasted to all users

## External Dependencies

### Frontend Dependencies
- **React Ecosystem**: React 18+ with TypeScript support
- **UI Framework**: Radix UI primitives for accessible components
- **Styling**: Tailwind CSS for utility-first styling
- **Date Handling**: date-fns for message timestamps
- **State Management**: TanStack Query for server state caching

### Backend Dependencies
- **Database**: Neon PostgreSQL database (@neondatabase/serverless)
- **ORM**: Drizzle ORM with PostgreSQL dialect
- **WebSocket**: ws library for WebSocket server implementation
- **Session Management**: express-session with PostgreSQL store

### Development Tools
- **Build Tools**: Vite for frontend, esbuild for backend
- **Database Migrations**: Drizzle Kit for schema management
- **Type Safety**: TypeScript throughout the stack
- **Code Quality**: ESLint and Prettier configurations

## Deployment Strategy

### Development Setup
- Frontend served by Vite dev server with HMR
- Backend runs with tsx for TypeScript execution
- Database migrations applied via Drizzle Kit
- Environment variables for database connection

### Production Build
1. Frontend built to `dist/public` directory
2. Backend compiled with esbuild to `dist/index.js`
3. Static files served by Express server
4. Database schema pushed to production PostgreSQL

### Environment Configuration
- `DATABASE_URL` required for PostgreSQL connection
- WebSocket connections upgrade from HTTP server
- CORS and security headers configured for production
- Session store configured with PostgreSQL backend

### Scalability Considerations
- WebSocket server runs on single instance (horizontally scalable with Redis adapter)
- Database operations optimized with proper indexing
- Message history pagination for performance
- Connection pooling for database efficiency
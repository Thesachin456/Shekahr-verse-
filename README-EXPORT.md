# ShkeharVerse - Futuristic Real-time Chat Application

## 🚀 Complete Source Code Export

This is the complete source code for **ShkeharVerse**, a futuristic real-time chatroom with dark theme, neon accents, and gaming stream aesthetic.

## ✨ Features

- **Real-time messaging** with WebSocket connections
- **Futuristic dark theme** with neon blue/purple accents
- **Mobile-optimized** with touch-friendly controls
- **Emoji reactions** (❤️ 👍 😂) - Now working!
- **User presence system** with online status
- **Responsive design** for desktop and mobile
- **PostgreSQL database** with Drizzle ORM
- **TypeScript** throughout the stack

## 🛠 Tech Stack

### Frontend
- **React 18** with TypeScript
- **Vite** - Fast build tool
- **Tailwind CSS** - Utility-first styling
- **shadcn/ui** - Modern component library
- **TanStack Query** - Server state management
- **Wouter** - Lightweight routing

### Backend
- **Node.js** with Express.js
- **WebSocket (ws)** - Real-time communication
- **PostgreSQL** - Database
- **Drizzle ORM** - Type-safe database operations
- **Zod** - Schema validation

## 📁 Project Structure

```
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── hooks/          # Custom React hooks
│   │   ├── lib/            # Utility functions
│   │   ├── pages/          # Page components
│   │   └── main.tsx        # App entry point
│   └── index.html
├── server/                 # Express backend
│   ├── index.ts            # Server entry point
│   ├── routes.ts           # API and WebSocket routes
│   ├── storage.ts          # Database operations
│   └── db.ts               # Database connection
├── shared/                 # Shared types and schemas
│   └── schema.ts           # Database schema & types
└── Configuration files...
```

## 🔧 Setup Instructions

### Prerequisites
- Node.js 18+ 
- PostgreSQL database

### 1. Install Dependencies
```bash
npm install
```

### 2. Environment Variables
Create a `.env` file:
```env
DATABASE_URL=postgresql://username:password@host:port/database
NODE_ENV=development
```

### 3. Database Setup
```bash
# Push schema to database
npm run db:push
```

### 4. Development
```bash
# Start development server
npm run dev
```
- Frontend: http://localhost:5000
- Backend API: http://localhost:5000/api
- WebSocket: ws://localhost:5000/ws

### 5. Production Build
```bash
# Build for production
npm run build

# Start production server
npm start
```

## 🎮 Key Features Fixed

### ✅ Working Emoji Reactions
- Click ❤️ 👍 😂 buttons on messages
- Real-time reaction updates via WebSocket
- Mobile-optimized touch targets

### ✅ Database Stability
- Fixed foreign key constraint issues
- Proper user status management
- Message persistence

### ✅ Mobile Optimization
- 44px minimum touch targets
- Always-visible message actions
- No-zoom input fields for iOS
- Responsive sidebar and layout

## 🚀 Deployment Options

### Replit (Recommended)
1. Import this code to Replit
2. Click "Deploy" button
3. Choose deployment type
4. Your app will be live at `your-repl.username.replit.app`

### Other Platforms
- **Vercel**: Deploy with PostgreSQL addon
- **Railway**: Automatic database provisioning
- **Heroku**: Add PostgreSQL addon
- **DigitalOcean**: App Platform with managed database

## 🎨 Customization

### Theme Colors (index.css)
```css
:root {
  --neon-blue: #00f3ff;
  --neon-purple: #b300ff;
  --neon-cyan: #00ffff;
  --neon-green: #39ff14;
}
```

### Database Schema (shared/schema.ts)
- Users table with status and display names
- Messages table with reactions and replies
- Proper foreign key relationships

## 📱 Mobile Experience

- **Touch-friendly** - All buttons are 44px minimum
- **Always-visible actions** - No need to hover on mobile
- **Responsive design** - Works on all screen sizes
- **iOS optimized** - Prevents zoom on input focus

## 🔒 Security Features

- Input validation with Zod schemas
- XSS protection in message rendering
- Database prepared statements
- Session management
- CORS configuration

## 🌟 Advanced Features

- **Real-time typing indicators**    
- **Message reactions system**
- **User presence tracking**
- **Mobile-first responsive design**
- **Accessibility support**
- **Error handling and reconnection**

## 📞 Support

This is a complete, production-ready chat application. All major features are implemented and tested on both desktop and mobile devices.

**Ready to deploy and scale!** 🚀

---
*Generated from ShkeharVerse - The Future of Digital Communication*
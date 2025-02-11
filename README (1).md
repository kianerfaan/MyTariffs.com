# MyTariffs.com - Tariff Rate Information System

A modern web application for retrieving and displaying international tariff rates, powered by GROQ's Mixtral-8x7b-32768 model for accurate tariff classification and rate determination.

## Tech Stack

### Frontend
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack Query (React Query) v5
- **Form Handling**: React Hook Form with Zod validation
- **UI Components**: ShadcN UI components with Tailwind CSS
- **Styling**: 
  - Tailwind CSS for utility-first styling
  - CSS Variables for theming
  - Custom theme configuration via theme.json

### Backend
- **Runtime**: Node.js 20
- **Server**: Express.js
- **Database**: PostgreSQL with Drizzle ORM
  - Drizzle Kit for schema management
  - Connection via @neondatabase/serverless
- **API Integration**: GROQ Cloud API (Mixtral-8x7b-32768 model)

### Development Environment
- **Build Tool**: Vite
- **Type Checking**: TypeScript
- **Development Server**: Custom Express + Vite setup for unified backend/frontend development
- **Package Management**: npm

## Features

- Real-time tariff rate lookups between countries
- AI-powered tariff classification
- User feedback system
- Responsive design
- Historical query tracking
- Error handling and validation

## Project Structure

```
├── client/
│   ├── src/
│   │   ├── components/    # Reusable UI components
│   │   ├── hooks/        # Custom React hooks
│   │   ├── lib/          # Utility functions and API clients
│   │   ├── pages/        # Route components
│   │   └── App.tsx       # Root component
├── server/
│   ├── routes.ts         # Express routes
│   ├── storage.ts        # Database operations
│   └── db.ts            # Database configuration
├── shared/
│   ├── schema.ts        # Shared TypeScript types and Zod schemas
│   └── groq.ts          # GROQ API integration
```

## Prerequisites

- Node.js 20 or later
- PostgreSQL database
- GROQ API key

## Environment Variables

```env
DATABASE_URL=postgresql://user:password@host:port/database
GROQ_API_KEY_3=your_groq_api_key
```

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/mytariffs.com.git
   cd mytariffs.com
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up the database:
   ```bash
   npm run db:push
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

The application will be available at `http://localhost:5000`.

## Development

- The development server runs both the frontend and backend on port 5000
- Frontend hot reloading is enabled via Vite
- Backend changes trigger automatic server restart
- Database schema changes are managed through Drizzle

## API Documentation

### Tariff Query Endpoint
```typescript
POST /api/tariff/query
Body: {
  importerCountry: string;
  exporterCountry: string;
  productDescription: string;
}
```

### Feedback Endpoint
```typescript
POST /api/tariff/feedback
Body: {
  queryId: number;
  isPositive: boolean;
}
```

## Deployment

The application is designed to be deployed on platforms supporting Node.js and PostgreSQL. Make sure to:

1. Set up the required environment variables
2. Run database migrations
3. Build the frontend assets:
   ```bash
   npm run build
   ```
4. Start the production server:
   ```bash
   npm start
   ```

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License

MIT License - see LICENSE file for details

## Acknowledgments

- GROQ Cloud for providing the Mixtral-8x7b-32768 model API
- ShadcN UI for the component library
- The Drizzle ORM team

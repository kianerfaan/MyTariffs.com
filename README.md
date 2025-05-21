# MyTariffs-replit.app

Domain mytariffs.com was sold to Namecheap user loganweaver1818 on May 17, 2025.

![MIT License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)

A responsive web application for retrieving and displaying international trade tariff information, leveraging Groq AI to provide accurate tariff rates between countries for specific products.

![MyTariffs.com Screenshot](./docs/screenshot.png)

## 🌟 Features

- **Instant Tariff Rate Lookup**: Quickly find tariff rates for products being traded between countries
- **AI-Powered Analysis**: Uses Groq's Mixtral-8x7b-32768 model to analyze and determine appropriate tariff rates
- **Recent Queries History**: View recently searched tariff information
- **Query Feedback System**: Provide feedback on the accuracy of returned tariff information
- **Responsive Design**: Works seamlessly on desktop and mobile devices

## 🚀 Getting Started

### Prerequisites

- Node.js (v18 or later)
- PostgreSQL database
- Groq API key

### Installation

1. Clone the repository:
   ```
   git clone https://github.com/kianerfaan/MyTariffs.com.git
   cd MyTariffs.com
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Set up environment variables by creating a `.env` file:
   ```
   DATABASE_URL=postgresql://username:password@localhost:5432/mytariffs
   GROQ_API_KEY_3=your_groq_api_key
   ```

4. Initialize the database:
   ```
   npm run db:push
   ```

5. Start the development server:
   ```
   npm run dev
   ```

6. Open your browser and visit `http://localhost:5000`

## 📚 Technology Stack

- **Frontend**: React, TypeScript, Tailwind CSS, shadcn/ui
- **Backend**: Express.js, PostgreSQL
- **AI Integration**: Groq API (Mixtral-8x7b-32768 model)
- **API Management**: TanStack Query
- **Form Handling**: React Hook Form with Zod validation
- **Database ORM**: Drizzle ORM

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines

- Follow the existing code style and organization
- Write unit tests for new features
- Update documentation as needed
- Make sure all tests pass before submitting a PR

## 📋 Project Structure

```
/
├── client/                  # Frontend code
│   ├── src/
│   │   ├── components/      # UI components
│   │   ├── hooks/           # Custom React hooks
│   │   ├── lib/             # Utility functions
│   │   ├── pages/           # Page components
│   │   └── App.tsx          # Main application component
├── server/                  # Backend code
│   ├── routes.ts            # API routes
│   ├── storage.ts           # Database interaction
│   └── index.ts             # Server setup
├── shared/                  # Shared code
│   ├── groq.ts              # Groq API integration
│   └── schema.ts            # Database schema
└── .env                     # Environment variables
```

## 📄 License

This project is licensed under the Apache 2.0 License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact

Project Link: [https://github.com/kianerfaan/MyTariffs.com](https://github.com/kianerfaan/MyTariffs.com)

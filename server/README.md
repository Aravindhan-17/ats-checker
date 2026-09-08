# ATS Checker - Server

Backend server for the ATS Checker application. This service provides APIs for resume analysis, keyword optimization, and scoring metrics.

## 📋 Overview

The server is built with Node.js and TypeScript, providing a robust RESTful API for the ATS Checker platform. It handles resume processing, validation, analysis algorithms, and data persistence.

## ✨ Features

- 🔄 **RESTful API** - Clean and documented API endpoints
- 📤 **File Upload** - Secure resume file handling (PDF, DOCX, TXT)
- 🔍 **Resume Analysis** - Advanced parsing and analysis algorithms
- 📊 **Scoring Engine** - Comprehensive ATS compatibility scoring
- 🔐 **Data Validation** - Input validation and security measures
- 📝 **Logging** - Comprehensive logging for debugging
- ⚡ **Performance** - Optimized processing pipelines

## 🛠️ Tech Stack

- **Runtime**: Node.js (v16+)
- **Language**: TypeScript & JavaScript
- **Framework**: Express.js (or as configured)
- **Package Manager**: npm/yarn

## 📦 Prerequisites

- **Node.js**: v16 or higher
- **npm** or **yarn** package manager
- **Git** for version control

## 🚀 Getting Started

### Installation

1. Navigate to the server directory:
   ```bash
   cd server
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file with required environment variables:
   ```bash
   cp .env.example .env
   ```

### Development

Start the development server with auto-reload:

```bash
npm run dev
```

The server will typically start at `http://localhost:3000`

### Build for Production

```bash
npm run build
```

### Run Production Build

```bash
npm run start
```

### Linting

Check code quality:

```bash
npm run lint
```

## 📁 Project Structure

```
server/
├── src/
│   ├── routes/           # API route definitions
│   ├── controllers/       # Request handlers and business logic
│   ├── models/           # Data models and database schemas
│   ├── middleware/       # Custom middleware (auth, validation, etc.)
│   ├── services/         # Business logic services
│   ├── utils/           # Utility functions
│   ├── types/           # TypeScript type definitions
│   └── index.ts         # Application entry point
├── public/              # Static files (if needed)
├── .env.example         # Environment variables template
├── tsconfig.json        # TypeScript configuration
├── package.json         # Dependencies and scripts
└── README.md           # This file
```

## 🔌 API Endpoints

### Resume Analysis
- `POST /api/resume/upload` - Upload and analyze resume
- `GET /api/resume/:id` - Get analysis results for a resume
- `DELETE /api/resume/:id` - Delete a resume record

### Scoring
- `GET /api/score/:resumeId` - Get ATS compatibility score
- `POST /api/score/batch` - Batch scoring for multiple resumes

### Keywords
- `POST /api/keywords/extract` - Extract keywords from resume
- `GET /api/keywords/suggestions` - Get keyword suggestions

### Job Descriptions
- `POST /api/jobs/analyze` - Analyze job description for required keywords
- `POST /api/jobs/match` - Match resume against job description

## 🔐 Environment Variables

Create a `.env` file in the server directory:

```env
# Server Configuration
PORT=3000
NODE_ENV=development

# Database (if applicable)
DB_URL=your_database_url
DB_NAME=ats_checker

# File Upload
MAX_FILE_SIZE=5000000
UPLOAD_DIR=./uploads

# CORS
CORS_ORIGIN=http://localhost:5173

# JWT (if using authentication)
JWT_SECRET=your_secret_key
JWT_EXPIRY=24h

# Logging
LOG_LEVEL=debug
```

## 📊 API Response Format

All API responses follow a consistent format:

### Success Response
```json
{
  "success": true,
  "data": {
    "resumeId": "123",
    "score": 85,
    "keywords": ["JavaScript", "React", "Node.js"]
  },
  "message": "Analysis completed successfully"
}
```

### Error Response
```json
{
  "success": false,
  "error": "Invalid file format",
  "code": "INVALID_FILE",
  "statusCode": 400
}
```

## 🔍 Resume Analysis Process

1. **File Upload** - Accept and validate resume file
2. **Parsing** - Extract text from PDF/DOCX/TXT
3. **Text Processing** - Clean and normalize text
4. **Keyword Extraction** - Identify key terms and skills
5. **Scoring** - Calculate ATS compatibility score
6. **Analysis** - Generate recommendations
7. **Response** - Return results to client

## 🛡️ Security Features

- Input validation on all endpoints
- File type and size validation
- CORS configuration for frontend access
- Rate limiting (if configured)
- Error handling without exposing internal details
- Secure file handling and temporary storage cleanup

## 📝 Logging

The server implements comprehensive logging:

```typescript
// Logs are generated in different levels
DEBUG  - Development information
INFO   - General application information
WARN   - Warning messages
ERROR  - Error messages and stack traces
```

Logs help with:
- Debugging issues
- Monitoring performance
- Tracking user actions
- Error investigation

## 🧪 Testing

To add tests (if testing framework is configured):

```bash
npm run test        # Run tests
npm run test:watch  # Run tests in watch mode
```

## 🚀 Deployment

### Deployment Checklist

- [ ] Set production environment variables
- [ ] Build the application (`npm run build`)
- [ ] Run production server (`npm run start`)
- [ ] Configure reverse proxy (nginx/Apache)
- [ ] Set up SSL/TLS certificates
- [ ] Monitor logs and performance
- [ ] Set up database backups

### Supported Hosting Platforms

- Heroku
- AWS EC2 / Elastic Beanstalk
- Google Cloud Run
- DigitalOcean
- Railway
- Render

## 🐛 Troubleshooting

### Port Already in Use
```bash
# Change port in .env
PORT=3001 npm run dev

# Or kill the process using the port
lsof -i :3000  # Find process
kill -9 <PID>  # Kill the process
```

### Database Connection Issues
- Verify `DB_URL` in `.env`
- Check database service is running
- Verify credentials and permissions

### File Upload Errors
- Check `UPLOAD_DIR` exists and is writable
- Verify `MAX_FILE_SIZE` setting
- Check disk space availability

### CORS Issues
- Verify `CORS_ORIGIN` matches frontend URL
- Check frontend and backend are not on restricted networks

## 📚 Related Documentation

- **[Root README](../README.md)** - Project overview
- **[Client README](../client/README.md)** - Frontend documentation
- **API Documentation** - Available at `/api/docs` (if Swagger/OpenAPI configured)

## 🤝 Contributing

For contribution guidelines, see the [Root README](../README.md#contributing)

## 📞 Support

For issues or questions about the server:

1. Check the troubleshooting section above
2. Review logs for error details
3. Open an issue on [GitHub Issues](https://github.com/Aravindhan-17/ats-checker/issues)

## 📝 License

This project is currently unlicensed. See the repository for more details.

## 👤 Author

**Aravindhan-17** - [GitHub Profile](https://github.com/Aravindhan-17)

---

**Last Updated**: September 8, 2026

Need help? Check the [Root README](../README.md) for general project information.

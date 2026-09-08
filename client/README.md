# ATS Checker

A modern web application to analyze and optimize resumes for Applicant Tracking Systems (ATS). This tool helps job seekers improve their resume's compatibility with ATS systems used by most companies.

## Features

- 📄 **Resume Analysis** - Upload and analyze your resume for ATS compatibility
- 🔍 **Keyword Optimization** - Identify missing keywords and skills relevant to job descriptions
- 📊 **Score & Metrics** - Get detailed scoring metrics for your resume
- 🎨 **Modern UI** - Clean and intuitive user interface with real-time feedback
- 💾 **Easy Export** - Generate optimized resume suggestions

## Tech Stack

- **Frontend**: React 18+ with TypeScript
- **Build Tool**: Vite
- **Styling**: CSS
- **Language**: TypeScript (43.5%), CSS (47.5%), JavaScript (5.6%)

## Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn package manager

### Installation

1. Clone the repository:
```bash
git clone https://github.com/Aravindhan-17/ats-checker.git
cd ats-checker
```

2. Navigate to the client directory:
```bash
cd client
```

3. Install dependencies:
```bash
npm install
```

### Development

To run the development server with Hot Module Replacement (HMR):

```bash
npm run dev
```

The application will start at `http://localhost:5173`

### Building for Production

```bash
npm run build
```

The optimized build will be generated in the `dist` folder.

### Running ESLint

To check code quality:

```bash
npm run lint
```

## Project Structure

```
ats-checker/
├── client/               # React frontend application
├── src/
│   ├── components/      # React components
│   ├── pages/          # Page components
│   └── styles/         # CSS stylesheets
├── public/             # Static assets
├── vite.config.ts      # Vite configuration
├── tsconfig.json       # TypeScript configuration
└── package.json        # Project dependencies
```

## Development Guidelines

### ESLint Configuration

This project includes ESLint for code quality. For production applications, consider enabling type-aware lint rules in your ESLint configuration by modifying `eslint.config.js`.

### React Compiler

The React Compiler is enabled to optimize component rendering. Note that this may impact Vite dev and build performance.

## Contributing

1. Create a feature branch (`git checkout -b feature/amazing-feature`)
2. Commit your changes (`git commit -m 'Add amazing feature'`)
3. Push to the branch (`git push origin feature/amazing-feature`)
4. Open a Pull Request

## License

This project is currently unlicensed. See the repository for more details.

## Author

[Aravindhan-17](https://github.com/Aravindhan-17)

## Support

For issues, questions, or feature requests, please open an issue on the [GitHub repository](https://github.com/Aravindhan-17/ats-checker/issues).

---

**Last Updated**: June 29, 2026

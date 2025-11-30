<div align="center">

# tutera

**Your Brand, Your Rules - A Multi-Tenant Learning Management System**

<img src="https://img.shields.io/badge/License-ISC-blue.svg" alt="License" />
<img src="https://img.shields.io/badge/node-%3E%3D18.0.0-brightgreen" alt="Node.js Version" />
<img src="https://img.shields.io/badge/TypeScript-5.9+-blue" alt="TypeScript" />
<img src="https://img.shields.io/badge/Next.js-16.0+-black" alt="Next.js" />
<img src="https://img.shields.io/badge/React-19.2+-blue" alt="React" />
<img src="https://img.shields.io/badge/Frontend-tutera--frontend-informational" alt="Frontend" />
<img src="https://img.shields.io/badge/Backend-tutera--backend-critical" alt="Backend" />

</div>

## Table of Contents

- [About Tutera](#about-tutera)
- [Key Features](#key-features)
- [Architecture](#architecture)
- [Quick Start](#quick-start)
- [Project Structure](#project-structure)
- [Technology Stack](#technology-stack)
- [Development](#development)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)

## About tutera

tutera is a comprehensive, multi-tenant Learning Management System (LMS) designed to empower educational institutions, independent creators, and enterprise training programs. Built with modern web technologies, tutera provides a scalable, secure, and feature-rich platform for creating, managing, and delivering educational content.

### What Makes tutera Special

- **Multi-Tenant Architecture**: Support for multiple institutions with complete data isolation
- **White-Label Solution**: Custom branding and domain support for each tenant
- **Role-Based Access Control**: Granular permissions for different user types
- **Modern Tech Stack**: Built with Next.js, React, TypeScript, and Node.js
- **Secure & Scalable**: Enterprise-grade security with horizontal scaling capabilities

## Key Features

### Multi-Tenant System
- **Institution Management**: Create and manage educational institutions with custom branding
- **Independent Creators**: Support for solo educators and content creators
- **Data Isolation**: Complete separation of tenant data with robust security
- **Custom Branding**: Tenant-specific logos, colors, and domain customization

### User Management
- **Authentication & Authorization**: JWT-based secure authentication with refresh tokens
- **Multiple User Roles**: Super Admin, Institution Admin, Creator, and Learner roles
- **Profile Management**: Comprehensive user profile system with avatars and preferences
- **Password Security**: OTP-based password reset and secure change flows

### Course Management
- **Course Creation**: Rich course creation with metadata, categories, and tags
- **Module Organization**: Structured content with modules and lessons
- **Content Types**: Support for video, PDF, audio, and text content
- **Publishing Control**: Draft and published course states with version control
- **Course Analytics**: Detailed engagement and performance metrics

### Media Management
- **Secure Upload**: Direct multipart upload to AWS S3/Wasabi cloud storage
- **Media Processing**: Automatic video transcoding and image optimization
- **Streaming Support**: Secure video streaming with signed URLs
- **File Management**: Complete CRUD operations for media assets
- **Content Protection**: Prevention of unauthorized downloads

### Learning Experience
- **Course Enrollment**: Seamless enrollment process with payment integration
- **Progress Tracking**: Real-time learning progress monitoring
- **Interactive Content**: Support for quizzes and assessments
- **Reviews & Ratings**: Student feedback system with ratings
- **Certificates**: Automated certificate generation upon course completion

### Creator Dashboard
- **Analytics**: Comprehensive dashboard with course performance metrics
- **Earnings**: Revenue tracking and financial insights
- **Student Management**: Tools to manage and engage with students
- **Course Management**: Intuitive interface for course creation and editing

### Customization & Branding
- **Brand Setup**: Step-by-step brand customization wizard
- **Color Themes**: Customizable color palettes for each tenant
- **Logo & Assets**: Upload and manage brand assets
- **Landing Pages**: Custom public landing pages for each institution

### Communication System
- **Email Templates**: Customizable email designs for notifications
- **Automated Notifications**: Course enrollment, completion, and system alerts
- **Email Analytics**: Delivery tracking and performance metrics

## Architecture

```
┌──────────────────────────────────────────────────────────────┐
│                     Frontend Layer                           │
│  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐ ┌─────────┐ │
│  │   Next.js   │ │    React    │ │   Tailwind  │ │ Zustand │ │
│  │   App Router│ │   Components│ │     CSS     │ │  Store  │ │
│  └─────────────┘ └─────────────┘ └─────────────┘ └─────────┘ │
├──────────────────────────────────────────────────────────────┤
│                     Backend Layer                            │
│  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐ ┌─────────┐ │
│  │  Express.js │ │  TypeScript │ │  JWT Auth   │ │  Zod    │ │
│  │    API      │ │   Services  │ │ Middleware  │ │ Validation│ │
│  └─────────────┘ └─────────────┘ └─────────────┘ └─────────┘ │
├──────────────────────────────────────────────────────────────┤
│                    Data & Storage Layer                      │
│  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐ ┌─────────┐ │
│  │   MongoDB   │ │    Redis    │ │   AWS S3    │ │ SendGrid│ │
│  │  Database   │ │    Cache    │ │   Storage   │ │  Email  │ │
│  └─────────────┘ └─────────────┘ └─────────────┘ └─────────┘ │
└──────────────────────────────────────────────────────────────┘
```

### Design Principles

- **Microservice-ready**: Modular architecture for future microservice migration
- **Event-driven**: Async processing for media and email operations
- **Secure by Default**: Security-first approach to all implementations
- **Scalable**: Horizontal scaling capabilities with stateless design
- **Maintainable**: Clean code with comprehensive testing and documentation

## Quick Start

### Prerequisites

- **Node.js** 18.0.0 or higher
- **npm** 8.0.0 or higher
- **MongoDB** 5.0 or higher
- **Redis** 6.0 or higher
- **AWS S3** or **Wasabi** bucket (for media storage)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/tutera-org/tutera.git
   cd tutera
   ```

2. **Install dependencies**
   ```bash
   # Install frontend dependencies
   cd tutera-frontend
   npm install
   
   # Install backend dependencies
   cd ../tutera-backend
   npm install
   ```

3. **Set up environment variables**
   ```bash
   # Backend environment
   cd tutera-backend
   cp .env.example .env
   # Edit .env with your configuration
   
   # Frontend environment
   cd ../tutera-frontend
   cp .env.example .env
   # Edit .env with your configuration
   ```

4. **Start the development servers**
   ```bash
   # Start backend server (terminal 1)
   cd tutera-backend
   npm run dev
   
   # Start frontend server (terminal 2)
   cd tutera-frontend
   npm run dev
   ```

5. **Access the application**
   - Frontend: `http://localhost:3000`
   - Backend API: `http://localhost:5000`
   - API Documentation: `http://localhost:5000/api/v1/docs`

## Project Structure

```
tutera/
├── tutera-frontend/          # Next.js frontend application
│   ├── app/                  # App Router pages and layouts
│   │   ├── [tenant]/         # Multi-tenant routes
│   │   ├── auth/             # Authentication pages
│   │   └── api/              # API routes
│   ├── components/           # Reusable React components
│   ├── hooks/                # Custom React hooks
│   ├── lib/                  # Utility libraries
│   └── public/               # Static assets
├── tutera-backend/           # Node.js backend API
│   ├── src/
│   │   ├── controllers/      # Route controllers
│   │   ├── models/           # MongoDB models
│   │   ├── routes/           # API routes
│   │   ├── services/         # Business logic
│   │   ├── middlewares/      # Express middlewares
│   │   ├── utils/            # Utility functions
│   │   └── validations/      # Request validation schemas
│   └── templates/            # Email templates
└── org/                      # Organization documentation
    ├── .github/              # GitHub templates and workflows
    └── README.md             # This file
```

## Technology Stack

### Frontend Technologies
- **Framework**: Next.js 16.0+ with App Router
- **UI Library**: React 19.2+ with TypeScript
- **Styling**: Tailwind CSS 4.1+ with custom components
- **State Management**: Zustand for global state
- **Forms**: React Hook Form with Zod validation
- **HTTP Client**: Axios with custom instances
- **Animations**: AOS (Animate On Scroll)
- **Charts**: Recharts and React Chart.js 2
- **Notifications**: Sonner for toast notifications
- **Icons**: React Icons

### Backend Technologies
- **Runtime**: Node.js 18+ with TypeScript 5.9+
- **Framework**: Express.js 5.1+ with comprehensive middleware
- **Database**: MongoDB with Mongoose ODM
- **Cache**: Redis for session and data caching
- **Authentication**: JWT with refresh token mechanism
- **Validation**: Zod schemas for request validation
- **File Upload**: Multer with multipart support
- **Media Processing**: FFmpeg for video transcoding
- **Image Processing**: Sharp for image optimization
- **Email**: SendGrid and Nodemailer with Handlebars templates
- **Queue**: BullMQ for background job processing
- **Real-time**: Socket.io for WebSocket connections
- **Logging**: Winston with daily rotate files

### Development Tools
- **Package Manager**: npm
- **Build Tools**: tsx for TypeScript execution
- **Linting**: ESLint with TypeScript support
- **Formatting**: Prettier with consistent code style
- **Git Hooks**: Husky for pre-commit checks
- **Testing**: Jest with TypeScript support
- **API Documentation**: Swagger/OpenAPI 3.0 with interactive UI
- **API Testing**: Postman collections for comprehensive testing

### Security & Performance
- **Security**: Helmet, CORS, Rate Limiting, Input Sanitization
- **Authentication**: Bcrypt password hashing, JWT tokens
- **Validation**: Comprehensive request validation with Zod
- **Sanitization**: Express-mongo-sanitize for NoSQL injection prevention
- **Compression**: Response compression middleware
- **Secure Headers**: XSS protection, content type options, frame options

### Storage & Infrastructure
- **Cloud Storage**: AWS S3 / Wasabi for media files
- **CDN Ready**: Static asset optimization
- **Environment**: Development and production configurations
- **Monitoring**: Health check endpoints and structured logging

## Development

### Scripts and Commands

#### Frontend (tutera-frontend)
```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run start        # Start production server
npm run lint         # Run ESLint
```

#### Backend (tutera-backend)
```bash
npm run dev          # Start development server with hot reload
npm run build        # Build for production
npm start            # Start production server
npm test             # Run tests
npm run lint         # Run ESLint
npm run swagger      # Generate Swagger documentation
```

### Environment Configuration

#### Backend (.env)
```env
# Server Configuration
NODE_ENV=development
PORT=5000
API_VERSION=v1

# Database
MONGODB_URI=mongodb://localhost:27017/tutera
REDIS_URL=redis://localhost:6379

# JWT Configuration
JWT_SECRET=your-super-secret-jwt-key
JWT_REFRESH_SECRET=your-refresh-token-secret
JWT_EXPIRE=24h
JWT_REFRESH_EXPIRE=7d

# Cloud Storage
AWS_ACCESS_KEY_ID=your-access-key
AWS_SECRET_ACCESS_KEY=your-secret-key
AWS_REGION=us-east-1
S3_BUCKET_NAME=your-bucket-name

# Email Configuration
SENDGRID_API_KEY=your-sendgrid-api-key
FROM_EMAIL=noreply@tutera.com
```

#### Frontend (.env)
```env
# API Configuration
NEXT_PUBLIC_API_BASE_URL=http://localhost:5000/api/v1
NEXT_PUBLIC_APP_URL=http://localhost:3000

# Stripe (for payments)
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=your-stripe-key
STRIPE_SECRET_KEY=your-stripe-secret
```

## Documentation

### API Documentation
- **Interactive Swagger UI**: `http://localhost:5000/api/v1/docs`
- **API Reference**: Comprehensive endpoint documentation
- **Postman Collections**: Ready-to-use API testing collections

### Development Documentation
- **Frontend**: Component documentation and usage examples
- **Backend**: Service architecture and data models
- **Deployment**: Production deployment guides

### User Documentation
- **Creator Guide**: How to create and manage courses
- **Student Guide**: How to enroll and learn
- **Admin Guide**: Platform administration

## Contributing

We welcome contributions to the Tutera project! Please follow our comprehensive contributing guidelines.

### Development Workflow

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Make your changes with proper testing**
4. **Follow our commit message conventions**
5. **Submit a Pull Request with detailed description**

### Code Standards

- **TypeScript**: All new code must be typed
- **ESLint**: Follow our linting rules
- **Prettier**: Use consistent formatting
- **Testing**: Add tests for new features
- **Documentation**: Update relevant documentation

### Commit Message Format

Follow the Conventional Commits specification:
```
type(scope): description

[optional body]

[optional footer]
```

Types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

## Acknowledgments

- **Next.js Team** - For the amazing React framework
- **MongoDB** - For the flexible database solution
- **AWS** - For reliable cloud infrastructure
- **SendGrid** - For email delivery services
- **Open Source Community** - For the amazing tools and libraries

## Support

- **Documentation**: [API Docs](https://tutera-backend.onrender.com/api/v1/docs)
- **Issues**: [GitHub Issues](https://github.com/tutera-org/tutera/issues)
- **Email**: tuteralms@gmail.com
- **Discussions**: [GitHub Discussions](https://github.com/tutera-org/tutera/discussions)

---

<div align="center">

**Built with love by the Tutera Team**

[Back to top](#tutera)

</div>

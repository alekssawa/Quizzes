# 💡 Meduzzen Internship Project: QuizHub

A comprehensive full-stack web application built for managing and interacting with a professional Quiz Platform. It leverages modern technologies to provide a user-friendly dark-themed interface, secure authentication, real-time communication, comprehensive analytics, and efficient data management.

---

## 🖥️ Frontend Architecture

The frontend is built to deliver a seamless, responsive, and highly interactive user experience for taking quizzes, viewing analytics, and managing company roles.

**Repository:** 🔗 [GitHub - Meduzzen-intership-frontend](https://github.com/alekssawa/meduzzen-intership-frontend)

### ✨ Frontend Features

- 🔑 User authentication and authorization
- 👤 Dashboard for viewing personal information and statistics
- 💬 Real-time notifications and requests UI
- ⚙️ Admin & Company dashboard for managing users, roles, and permissions
- 📊 Visual analytics for tracking quiz progress and score dynamics
- 🎨 Customizable, dark-themed UI built with utility-first CSS
- 🔍 Search functionality for quick access to data and companies
- 🔄 Internationalization support for multiple languages

### 🛠️ Frontend Tech Stack

- Next.js (React framework)
- TypeScript
- Tailwind CSS (utility-first CSS framework)
- Emotion (CSS-in-JS library)
- Chart.js + React-Chartjs-2 (data visualization library)
- Axios (HTTP client for API requests)
- Next Intl (internationalization support)

**Dependencies:**

- `@emotion/cache`, `@emotion/react`, `@emotion/styled`: For styling and theming
- `@icons-pack/react-simple-icons`: Icon library
- `chart.js`: Charting library
- `class-variance-authority`, `clsx`: Utility libraries for classnames
- `cmdk`: Command palette library
- `js-cookie`, `jwt-decode`: Cookie management and token decoding
- `lucide-react`: SVG icon library
- `next-intl`: Internationalization support
- `radix-ui`: Accessible UI components built with shadcn
- `react-chartjs-2`: React wrapper for Chart.js
- `react-toastify`: Toast notifications
- `shadcn`: Tailwind utility library
- `tailwind-merge`: Utility for merging classnames
- `tw-animate-css`: CSS animations with Tailwind

### 📂 Frontend Folder Structure

- **`src/`**: Contains the main source code.
  - `components/`: Reusable React components.
  - `config/`: Configuration files for cookies, locales, pagination, and routes.
  - `hooks/`: Custom React hooks.
  - `i18n/`: Internationalization utilities.
  - `lib/`: Utility functions and libraries.
  - `pages/`: Next.js pages corresponding to different routes.
  - `services/`: API services for interacting with the backend.
  - `styles/`: Global stylesheets and Tailwind configuration.
- **`public/`**: Contains static assets like images, fonts, and icons.

---

## ⚙️ Backend Architecture

A robust backend application built with NestJS, providing the core logic for the Quiz Platform, including secure authentication, real-time communication, analytics, and efficient data management.

**Repository:** 🔗 [GitHub - Meduzzen-intership-backend](https://github.com/alekssawa/meduzzen-intership-backend)

### ✨ Backend Features

- 🔑 Secure user authentication and authorization using Auth0 and JWT, stored safely via `httpOnly` cookies.
- 🧠 Core quiz mechanics, including creation, timed attempts, and automated scoring.
- 🏢 Company module for grouping users and managing participant roles.
- 📊 Built-in analytics and tracking, including user ratings, quiz attempt scores, and global platform statistics.
- 💬 Real-time notifications using Server-Sent Events (SSE).
- ⚙️ Extensible and maintainable architecture with modular design.

### 🛠️ Backend Tech Stack

- NestJS (framework for building efficient, scalable server-side applications)
- TypeORM (Object Relational Mapper) integrated with PostgreSQL for database management
- Redis for caching
- Auth0 for OAuth2 authentication
- Server-Sent Events (SSE) for real-time client updates
- bcrypt for password hashing

### 📂 Backend Folder Structure

- **`auth/`**: Handles user authentication and authorization. Includes integrations for Auth0 and local JWT strategies, as well as role-based guards (`company-admin.guard.ts`).
- **`common/`**: Contains shared resources used across the application. This includes custom decorators (`@CurrentUser`, `@AllowMember`), pagination utilities, global exception filters, and interceptors.
- **`companies/`**: Manages company-related data, company actions, and participant roles. Allows users to form groups and manage administrative rights within a company context.
- **`notifications/`**: Provides real-time event updates to the client using Server-Sent Events (SSE). It uses event listeners to trigger notifications for specific company and user actions.
- **`providers/`**: Manages external connections and configurations, including PostgreSQL database setups, TypeORM migrations, and the Redis module.
- **`quizzes/`**: The core module of the platform. It handles everything related to quizzes: creation, tracking user attempts, score calculation, and automated cron jobs (`quiz-reminder.service.ts`).
- **`users/`**: Handles user profiles (avatars, about sections), tracks user actions, and manages the analytical side of the platform, including user ratings and statistics.


### [View screenshots of the project](./GALLERY.md)

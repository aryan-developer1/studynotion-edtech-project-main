# StudyNotion - EdTech Platform

![StudyNotion](public/logo.png)

StudyNotion is a comprehensive EdTech platform built with the MERN stack that enables seamless learning experiences for students and course creation capabilities for instructors.

## 🚀 Features

### For Students
- **User Authentication**: Secure signup/login with OTP verification
- **Course Enrollment**: Browse and enroll in courses with integrated payment system
- **Interactive Learning**: Video lectures, progress tracking, and course completion certificates
- **Dashboard**: Personal dashboard to track enrolled courses and progress
- **Rating & Reviews**: Rate and review courses after completion

### For Instructors
- **Course Creation**: Create comprehensive courses with multiple sections and subsections
- **Content Management**: Upload videos, images, and course materials
- **Student Analytics**: Track student enrollment and course performance
- **Revenue Dashboard**: Monitor earnings and course statistics

### General Features
- **Responsive Design**: Fully responsive UI built with Tailwind CSS
- **Payment Integration**: Secure payments via Razorpay
- **Email Notifications**: Automated email system for OTP and notifications
- **Cloud Storage**: Media files stored on Cloudinary
- **Search & Filter**: Advanced course search and filtering options

## 🛠️ Tech Stack

### Frontend
- **React 18** - Modern React with hooks and functional components
- **Redux Toolkit** - State management
- **React Router DOM** - Client-side routing
- **Tailwind CSS** - Utility-first CSS framework
- **React Hook Form** - Form handling and validation
- **React Hot Toast** - Toast notifications
- **Axios** - HTTP client for API calls

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT** - Authentication tokens
- **Bcrypt** - Password hashing
- **Nodemailer** - Email service
- **Cloudinary** - Media storage
- **Razorpay** - Payment gateway

## 📁 Project Structure

```
studynotion/
├── public/                 # Static files
├── src/
│   ├── components/         # React components
│   │   ├── Common/         # Shared components
│   │   └── core/           # Feature-specific components
│   ├── data/              # Static data and constants
│   ├── hooks/             # Custom React hooks
│   ├── pages/             # Page components
│   ├── services/          # API services
│   ├── slices/            # Redux slices
│   └── utils/             # Utility functions
├── server/
│   ├── config/            # Database and service configurations
│   ├── controllers/       # Route controllers
│   ├── mail/              # Email templates
│   ├── middleware/        # Custom middleware
│   ├── models/            # Database models
│   ├── routes/            # API routes
│   └── utils/             # Server utilities
└── package.json
```

## 🚀 Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- MongoDB
- Git

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/studynotion-edtech-project.git
cd studynotion-edtech-project
```

### 2. Install Dependencies

**Frontend:**
```bash
npm install
```

**Backend:**
```bash
cd server
npm install
```

### 3. Environment Configuration

Create `.env` file in the root directory:
```env
REACT_APP_BASE_URL=http://localhost:4000/api/v1
```

Create `server/.env` file:
```env
# Server Configuration
PORT=4000

# JWT Secret
JWT_SECRET=your_jwt_secret_key_here

# Database
MONGODB_URL=mongodb://localhost:27017/studynotion

# Email Configuration (Gmail)
MAIL_HOST=smtp.gmail.com
MAIL_USER=your_email@gmail.com
MAIL_PASS=your_app_password

# Razorpay (Payment Gateway)
RAZORPAY_KEY=your_razorpay_key
RAZORPAY_SECRET=your_razorpay_secret

# Cloudinary (Media Storage)
CLOUD_NAME=your_cloudinary_name
API_KEY=your_cloudinary_api_key
API_SECRET=your_cloudinary_api_secret
```

### 4. Database Setup
Make sure MongoDB is running on your system. The application will automatically create the required collections.

### 5. Run the Application

**Development Mode (Both Frontend & Backend):**
```bash
npm run dev
```

**Or run separately:**

**Frontend:**
```bash
npm start
```

**Backend:**
```bash
cd server
npm run dev
```

The application will be available at:
- Frontend: http://localhost:3000
- Backend: http://localhost:4000

## 📧 Email Configuration

For Gmail users:
1. Enable 2-factor authentication
2. Generate an "App Password" (not your regular password)
3. Use the app password in `MAIL_PASS`

## 💳 Payment Integration

This project uses Razorpay for payment processing. To set up:
1. Create a Razorpay account
2. Get your API keys from the dashboard
3. Add them to your environment variables

## 🗄️ Database Models

- **User**: Student and instructor profiles
- **Course**: Course information and content
- **Section**: Course sections
- **SubSection**: Individual lectures/videos
- **Category**: Course categories
- **CourseProgress**: Student progress tracking
- **Payment**: Payment records
- **OTP**: Email verification codes

## 🔗 API Endpoints

### Authentication
- `POST /api/v1/auth/signup` - User registration
- `POST /api/v1/auth/login` - User login
- `POST /api/v1/auth/sendotp` - Send OTP for verification
- `POST /api/v1/auth/changepassword` - Change password

### Courses
- `GET /api/v1/course/getAllCourses` - Get all courses
- `POST /api/v1/course/createCourse` - Create new course (Instructor)
- `POST /api/v1/course/getCourseDetails` - Get course details
- `POST /api/v1/course/editCourse` - Edit course (Instructor)

### Profile
- `GET /api/v1/profile/getUserDetails` - Get user profile
- `PUT /api/v1/profile/updateProfile` - Update profile
- `GET /api/v1/profile/getEnrolledCourses` - Get enrolled courses

### Payments
- `POST /api/v1/payment/capturePayment` - Process payment
- `POST /api/v1/payment/verifyPayment` - Verify payment

## 🎨 UI Components

The project includes reusable components:
- **IconBtn**: Customizable icon buttons
- **Upload**: File upload with drag-and-drop
- **ConfirmationModal**: Confirmation dialogs
- **Tab**: Tab navigation
- **ProgressBar**: Progress indicators

## 🔒 Security Features

- JWT-based authentication
- Password hashing with bcrypt
- Input validation and sanitization
- CORS configuration
- Environment variable protection

## 🚀 Deployment

### Frontend (Netlify/Vercel)
1. Build the project: `npm run build`
2. Deploy the `build` folder
3. Set environment variables in deployment platform

### Backend (Heroku/Railway)
1. Set up environment variables
2. Deploy the `server` folder
3. Ensure MongoDB connection is configured

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit changes: `git commit -m 'Add feature'`
4. Push to branch: `git push origin feature-name`
5. Submit a pull request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Aryan Soni**
- Email: aryansoni9875@gmail.com
- GitHub: [@aryansoni](https://github.com/aryansoni)

## 🙏 Acknowledgments

- Thanks to all contributors and the open-source community
- Special thanks to the MERN stack developers
- Icons and images from various open-source resources

---

Made with ❤️ by Aryan © 2023 StudyNotion

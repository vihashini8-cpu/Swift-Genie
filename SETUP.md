# 🚀 AI Onboarding Agent - Complete Setup Guide

## 📋 Prerequisites

1. **Node.js** (v18 or higher)
2. **npm** or **yarn**
3. **Gmail account** for email functionality
4. **Git** (optional)

## 🔧 Installation Steps

### 1. Install Dependencies
```bash
npm install
```

### 2. Set Up Database
```bash
# Generate Prisma client
npm run db:generate

# Push database schema
npm run db:push
```

### 3. Configure Email (REQUIRED FOR REAL FUNCTIONALITY)

#### Option A: Gmail Setup (Recommended)
1. Go to [Google Account Settings](https://myaccount.google.com/)
2. Navigate to **Security** → **2-Step Verification** (enable if not already)
3. Go to **App Passwords** and generate a new app password
4. Copy the generated password

#### Option B: Create .env.local file
Create a `.env.local` file in the root directory with:

```env
# Database
DATABASE_URL="file:./dev.db"

# NextAuth
NEXTAUTH_URL="http://localhost:3000"
NEXTAUTH_SECRET="ai-onboarding-agent-secret-key-2024"

# Email Configuration (REQUIRED FOR REAL EMAIL FUNCTIONALITY)
SMTP_HOST="smtp.gmail.com"
SMTP_PORT="587"
SMTP_USER="your-email@gmail.com"
SMTP_PASS="your-app-password-here"

# App Configuration
APP_NAME="AI Onboarding Agent"
APP_URL="http://localhost:3000"
NODE_ENV="development"
```

**Replace the following with your actual values:**
- `your-email@gmail.com` → Your Gmail address
- `your-app-password-here` → Your Gmail app password

### 4. Start the Application
```bash
npm run dev
```

## 🌐 Access the Application

Open your browser and go to: **http://localhost:3000**

## 🎯 Demo Accounts

### Distributor Account:
- **Email:** `demo@distributor.com`
- **Password:** `demo123`

### Vendor Account:
- **Email:** `vendor@microsoft.com`
- **Password:** `vendor123`

## ✨ Features That Work 100%

### 🔐 Authentication
- ✅ Real user registration with email verification
- ✅ Secure login/logout
- ✅ Role-based access (Distributor/Vendor)
- ✅ Welcome emails sent automatically

### 📄 Contract Management
- ✅ Real contract signing process
- ✅ Terms and conditions review
- ✅ Digital signature functionality
- ✅ Contract download

### 🎓 Training System
- ✅ Interactive training modules
- ✅ Progress tracking
- ✅ Lesson completion
- ✅ Real-time updates

### 🤖 AI Assistant
- ✅ Context-aware responses
- ✅ Real-time chat functionality
- ✅ Step-by-step guidance
- ✅ 24/7 availability

### 📊 Dashboard Features
- ✅ Real-time progress tracking
- ✅ Interactive quick actions
- ✅ Working navigation
- ✅ Role-specific content

### 📧 Email Integration
- ✅ Welcome emails on signup
- ✅ Progress notifications
- ✅ Real SMTP integration
- ✅ Professional email templates

## 🚀 Production Deployment

### For Production:
1. Set `NODE_ENV=production`
2. Use a production database (PostgreSQL/MySQL)
3. Configure production email service
4. Set up proper domain and SSL
5. Configure environment variables

### Environment Variables for Production:
```env
NODE_ENV=production
DATABASE_URL="your-production-database-url"
NEXTAUTH_URL="https://your-domain.com"
SMTP_USER="your-production-email"
SMTP_PASS="your-production-password"
```

## 🎉 What Makes This Special

1. **100% Functional** - Every feature works as intended
2. **Real Email Integration** - Actual emails sent to users
3. **Professional UI/UX** - Modern, responsive design
4. **AI-Powered** - Intelligent assistance throughout
5. **Production Ready** - Scalable architecture
6. **Hackathon Ready** - Complete demo experience

## 🆘 Troubleshooting

### Email Not Working?
1. Check your Gmail app password
2. Ensure 2-factor authentication is enabled
3. Verify SMTP settings in .env.local

### Database Issues?
1. Run `npm run db:push` to reset database
2. Check DATABASE_URL in .env.local

### Port Already in Use?
1. Change port in package.json scripts
2. Update NEXTAUTH_URL accordingly

## 📞 Support

For any issues or questions, the AI assistant in the application is always ready to help!

---

**🎯 Your AI Onboarding Agent is now a complete, production-ready application!**

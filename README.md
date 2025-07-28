# 🚀 ProActive - Productivity App

A clean and minimalistic productivity app designed to help users overcome procrastination through an integrated to-do list, daily scheduler, and calendar interface. Built with React Native, Expo, and Supabase.

![ProActive App](https://img.shields.io/badge/React%20Native-0.79.4-blue)
![Expo](https://img.shields.io/badge/Expo-53.0.13-lightgrey)
![TypeScript](https://img.shields.io/badge/TypeScript-5.8.3-blue)
![Supabase](https://img.shields.io/badge/Supabase-2.50.2-green)

## 📱 App Store Publishing

### iOS App Store Process
- **Apple Developer Account** - Registered developer account with Apple
- **TestFlight Distribution** - Beta testing through TestFlight for internal and external testing
- **App Store Review** - Submission and review process through App Store Connect
- **Production Release** - Live deployment on the App Store

### Build and Distribution Process
- **Development Builds** - Created using Expo EAS Build service
- **TestFlight Upload** - Automated uploads for beta testing
- **App Store Submission** - Final builds submitted for review
- **Version Management** - Semantic versioning for app updates

### Support and Legal Links
- **📞 Support Portal**: [ProActive Support Portal](https://www.notion.so/PROActive-Support-Portal-2243549982b780668edfd6d355ef3e1d)
- **🔒 Privacy Policy**: [Privacy Policy](https://www.freeprivacypolicy.com/live/3e73c01d-9975-463b-a111-01b42175bcdb)

## 📞 Support

If you have any questions or need help with the app:

- **📞 Official Support Portal**: [ProActive Support Portal](https://www.notion.so/PROActive-Support-Portal-2243549982b780668edfd6d355ef3e1d)
- **🔒 Privacy Policy**: [Privacy Policy](https://www.freeprivacypolicy.com/live/3e73c01d-9975-463b-a111-01b42175bcdb)
- Create an issue on GitHub
- Check the documentation in the `docs/` folder
- Review the setup guides in the project

## ✨ Features

### 🎯 Core Functionality
- **📋 To-Do List Management** - Create, edit, and track tasks with status updates
- **🗓️ Calendar Integration** - Schedule events and view them in a calendar interface
- **⏱️ Habit Tracking** - Build and maintain daily/weekly habits with progress tracking
- **🏠 Smart Home Dashboard** - Overview of tasks, events, and habits in one place
- **⚙️ Settings & Customization** - User profiles, theme preferences, and app settings

### 🎨 User Experience
- **Dark/Light Mode** - Automatic theme switching with user preferences
- **Clean Minimal Design** - Purple-themed, clutter-free interface
- **Responsive Layout** - Optimized for both iOS and Android
- **Haptic Feedback** - Enhanced user interaction with tactile responses

### 🔐 Authentication & Data
- **Supabase Backend** - Secure user authentication and data storage
- **Real-time Sync** - Automatic data synchronization across devices
- **User Profiles** - Customizable user settings and preferences

## 🛠️ Tech Stack

### Frontend
- **React Native** (0.79.4) - Cross-platform mobile development
- **Expo** (53.0.13) - Development platform and tools
- **TypeScript** (5.8.3) - Type-safe JavaScript
- **Expo Router** (5.1.1) - File-based routing system

### Backend & Database
- **Supabase** (2.50.2) - Backend-as-a-Service with PostgreSQL
- **Real-time Database** - Live data synchronization
- **Authentication** - Secure user management

### UI/UX Libraries
- **React Navigation** - Navigation framework
- **Expo Vector Icons** - Icon library
- **React Native Calendars** - Calendar component
- **Expo Haptics** - Haptic feedback

## 📱 Screenshots

*[Screenshots will be added here]*

## 🚀 Getting Started

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn
- Expo CLI
- iOS Simulator (for iOS development)
- Android Studio (for Android development)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/sxiayuan/PROActive.git
   cd PROActive
   ```

2. **Install dependencies**
   ```bash
   cd proactive
   npm install
   ```

3. **Set up environment variables**
   ```bash
   # Create a .env file in the proactive directory
   cp .env.example .env
   ```
   
   Add your Supabase credentials to the `.env` file:
   ```
   EXPO_PUBLIC_SUPABASE_URL=your_supabase_url
   EXPO_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

4. **Start the development server**
   ```bash
   npm start
   ```

5. **Run on your device**
   - Scan the QR code with Expo Go app (iOS/Android)
   - Or press `i` for iOS simulator or `a` for Android emulator

### Database Setup

1. **Create a Supabase project** at [supabase.com](https://supabase.com)

2. **Run the database setup script**
   ```bash
   # Execute the SQL scripts in your Supabase SQL editor
   # Files: database-setup.sql, rls-policies-secure.sql
   ```

3. **Enable authentication** and configure user settings

## 📁 Project Structure

```
proactive/
├── app/                      # Expo Router app directory
│   ├── (tabs)/              # Main app tabs
│   │   ├── home.tsx         # Home dashboard
│   │   ├── todo.tsx         # To-do list
│   │   ├── calendar.tsx     # Calendar view
│   │   ├── habits.tsx       # Habit tracker
│   │   └── settings.tsx     # Settings
│   └── _layout.tsx          # Root layout
├── components/               # Reusable components
│   ├── AuthSetup.tsx        # Authentication setup
│   ├── ProfileContext.tsx   # User profile context
│   └── ui/                  # UI components
├── services/                 # API services
│   ├── supabaseService.ts   # Supabase client
│   └── userService.ts       # User management
├── hooks/                    # Custom React hooks
├── constants/                # App constants
├── types/                    # TypeScript types
├── assets/                   # Static assets
└── docs/                     # Documentation
```

## 🎯 Key Features Explained

### Home Dashboard
- Overview of daily tasks, upcoming events, and habit progress
- Quick access to all app sections
- Motivational quotes and progress tracking

### To-Do List
- Create tasks with titles and descriptions
- Mark tasks as complete, in progress, or incomplete
- Edit and delete existing tasks
- Filter and organize tasks

### Calendar Integration
- Schedule events with time and location
- View events in calendar format
- Navigate between dates easily

### Habit Tracker
- Create daily or weekly habits
- Track completion for each day of the week
- Add notes and feedback for habit progress

### Settings & Profile
- User profile management
- Theme preferences (dark/light mode)
- Notification settings
- App customization options

## 🔧 Development

### Available Scripts

```bash
# Start development server
npm start

# Run on specific platforms
npm run ios
npm run android
npm run web

# Build for production
npm run build:ios
npm run build:android

# Submit to app stores
npm run submit:ios
npm run submit:android

# Lint code
npm run lint
```

## 📱 App Store Publishing

### iOS App Store
The ProActive app is published on the iOS App Store through the following process:

1. **Apple Developer Account** - Registered developer account with Apple
2. **TestFlight Distribution** - Beta testing through TestFlight for internal and external testing
3. **App Store Review** - Submission and review process through App Store Connect
4. **Production Release** - Live deployment on the App Store

### Build and Distribution Process
- **Development Builds** - Created using Expo EAS Build service
- **TestFlight Upload** - Automated uploads for beta testing
- **App Store Submission** - Final builds submitted for review
- **Version Management** - Semantic versioning for app updates

### Support and Legal
- **📞 Support Portal**: [ProActive Support Portal](https://www.notion.so/PROActive-Support-Portal-2243549982b780668edfd6d355ef3e1d)
- **🔒 Privacy Policy**: [Privacy Policy](https://www.freeprivacypolicy.com/live/3e73c01d-9975-463b-a111-01b42175bcdb)

### Database Schema

The app uses the following main tables:
- **users** - User accounts and preferences
- **tasks** - To-do items and their status
- **events** - Calendar events and schedules
- **habits** - Habit definitions and tracking
- **user_settings** - User preferences and theme settings

## 🎨 Design System

### Colors
- **Primary**: Purple (#8e44ad)
- **Secondary**: Light purple (#9260db)
- **Background**: White (#fff) / Dark (#151718)
- **Text**: Dark (#222) / Light (#fff)

### Typography
- Clean, minimal font choices
- Consistent sizing and spacing
- High contrast for accessibility

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow TypeScript best practices
- Use functional components with hooks
- Maintain consistent code formatting
- Write meaningful commit messages
- Test on both iOS and Android

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with [Expo](https://expo.dev/)
- Backend powered by [Supabase](https://supabase.com/)
- Icons from [Expo Vector Icons](https://expo.github.io/vector-icons/)
- Calendar component from [React Native Calendars](https://github.com/wix/react-native-calendars)

## 📞 Support

If you have any questions or need help with the app:

- **📞 Official Support Portal**: [ProActive Support Portal](https://www.notion.so/PROActive-Support-Portal-2243549982b780668edfd6d355ef3e1d)
- **🔒 Privacy Policy**: [Privacy Policy](https://www.freeprivacypolicy.com/live/3e73c01d-9975-463b-a111-01b42175bcdb)
- Create an issue on GitHub
- Check the documentation in the `docs/` folder
- Review the setup guides in the project

---

**Made with ❤️ for productivity enthusiasts** 

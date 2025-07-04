## 🎯 Overview

ProActive is a clean and minimalistic productivity app designed to help users overcome procrastination through an integrated to-do list, daily scheduler, and calendar interface. The app includes motivational elements and smart reminders to keep users engaged and on track.

##colour/style
purple, minimal clean

## Tech Stack
- Frontend: React Native with TypeScript, Expo, and Expo Router
- Backend/Database: Supabase
- UI Framework: React Native Paper
- AI Processing: DeepSeek

## 📊 Database Schema

### Users Table
```sql
users (
  id: uuid primary key
  email: text unique
  created_at: timestamp
  updated_at: timestamp
  full_name: text
  avatar_url: text
  preferences: jsonb {
    theme: text
    notifications_enabled: boolean
    language: text
  }
)
```

### Tasks Table
```sql
tasks (
  id: uuid primary key
  user_id: uuid references users(id)
  title: text
  description: text
  status: text enum ('pending', 'in_progress', 'completed')
  created_at: timestamp
  updated_at: timestamp
  due_date: timestamp
  priority: text enum ('low', 'medium', 'high')
  category: text
  is_deleted: boolean default false
)
```

### Scheduled Tasks Table
```sql
scheduled_tasks (
  id: uuid primary key
  user_id: uuid references users(id)
  task_id: uuid references tasks(id)
  start_time: timestamp
  end_time: timestamp
  recurrence: text enum ('none', 'daily', 'weekly', 'monthly')
  created_at: timestamp
  updated_at: timestamp
)
```

### Habits Table
```sql
habits (
  id: uuid primary key
  user_id: uuid references users(id)
  title: text
  description: text
  created_at: timestamp
  updated_at: timestamp
  frequency: text enum ('daily', 'weekly')
  category: text
)
```

### Habit Logs Table
```sql
habit_logs (
  id: uuid primary key
  habit_id: uuid references habits(id)
  user_id: uuid references users(id)
  date: date
  status: text enum ('completed', 'incomplete')
  notes: text
  feedback: text
  created_at: timestamp
  updated_at: timestamp
)
```

### Notifications Table
```sql
notifications (
  id: uuid primary key
  user_id: uuid references users(id)
  title: text
  message: text
  type: text enum ('task', 'habit', 'reminder')
  scheduled_for: timestamp
  is_read: boolean default false
  created_at: timestamp
)
```

### Motivational Quotes Table
```sql
motivational_quotes (
  id: uuid primary key
  quote: text
  author: text
  category: text
  created_at: timestamp
)
```

## 📁 Project Structure

```
proactive/
├── app/                      # Expo Router app directory
│   ├── (auth)/              # Authentication routes
│   │   ├── login.tsx
│   │   ├── register.tsx
│   │   └── forgot-password.tsx
│   ├── (tabs)/              # Main app tabs
│   │   ├── home.tsx
│   │   ├── todo.tsx
│   │   ├── schedule.tsx
│   │   └── habits.tsx
│   ├── settings/            # Settings routes
│   │   ├── index.tsx
│   │   ├── notifications.tsx
│   │   └── preferences.tsx
│   └── _layout.tsx          # Root layout
├── src/
│   ├── components/          # Reusable components
│   │   ├── common/         # Shared components
│   │   ├── todo/          # Todo-specific components
│   │   ├── schedule/      # Schedule-specific components
│   │   └── habits/        # Habit-specific components
│   ├── hooks/             # Custom React hooks
│   ├── services/          # API and external services
│   │   ├── supabase.ts
│   │   ├── ai.ts
│   │   └── notifications.ts
│   ├── store/             # State management
│   │   ├── atoms/
│   │   └── selectors/
│   ├── types/             # TypeScript types/interfaces
│   ├── utils/             # Helper functions
│   └── constants/         # App constants
├── assets/                # Static assets
│   ├── images/
│   ├── fonts/
│   └── icons/
├── docs/                  # Documentation
├── tests/                 # Test files
├── .env.example          # Environment variables example
├── app.json              # Expo config
├── babel.config.js       # Babel config
├── tsconfig.json         # TypeScript config
└── package.json          # Dependencies and scripts
```

## 🧭 Core Features

### 1. Welcome Experience
- Clean, clutter-free welcome screen
- Branded logo and tagline
- "Get Started"  button

### 2. Main Interface
- **Home Page** with three primary sections:
  - 📋 To-Do List
  - 🗓 Schedule
  - ⏱️ Weekly Habit Tracker
- Quick access to settings via corner icon

### 3. To-Do List Features
- **Task Management**
  - Add tasks title, below have the option to type a description
  - Mark tasks as complete, in progress, or incomplete
  - Edit existing tasks
  - Delete tasks
- **UI Elements**
  - Minimal card view for tasks
  - Daily rotating motivational quote header
  - Quick-add button for instant task creation

### 4. Schedule Management
- **Task Scheduling**
  - Add tasks with:
    - Title
    - Description (optional)
    - Time
    - Category/Label (optional)
- **Viewing Options**
  - Daily task view
  - Calendar integration
  - Date selection for schedule review

### 5. Calendar Integration
- Seamless connection with daily scheduler
- Historical schedule review
- Current date highlighting
- Easy date navigation

### 6. Weekly Habit Tracker
- Add habit to a habit tracker and have the user indicate how many times a week they wish to complete this task 
- show week calender monday to sunday
- User mark habit has complete or incomplete for everyday by clicking onto that week day and clicking complete 
- User able to write notes about that day's habit


### 7. Smart Notifications
- **Reminder Types**
  - Upcoming scheduled tasks
  - Overdue to-do items
  - Optional push notifications
- Customizable notification settings

### 8. AI Assistant Integration
- Natural language task creation
- Smart suggestions based on user history
- Available in both To-Do and Schedule views

### 9. Motivational Features
- Daily rotating quotes
- Achievement celebrations
- Customizable display settings

## Starting page
- Says "Welcome to Proactive!" in the middle, right below there is a "Get Started" button
- the "Get Started" button leads to a registration page

##Registration page
- the registration page is where the user signs up for the app 

## ⚙️ Settings & Customization

### Core Settings
- user profile (name, email, birthday)
- Notification preferences
- Theme selection (light/dark mode)
- Do not disturb option

## 🚀 Future Roadmap

### Planned Enhancements
- Cloud synchronization
- User account system
- Task priority system
- Focus time blocking
- Analytics dashboard

---

*This document serves as the primary reference for developers implementing ProActive's core features and user interface design.*

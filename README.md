# BookMyTurf Mobile App

A scalable **React Native (Expo) application** for discovering and booking sports turfs.
The platform supports **Customers**, **Turf Owners**, and **Admins** with a modular architecture designed for **production-level scalability**.

---

# Features

## Customer

* OTP Login
* Google Sign In
* Search turfs
* Filter by location, rating, price
* Turf details page
* Live slot booking
* Booking history
* Profile management
* Reviews

## Turf Owner

* Owner dashboard
* Manage turfs
* Accept / Reject bookings
* Earnings analytics
* Export earnings reports
* Manage slots

## Admin

* Manage users
* Turf approval system
* Platform analytics

---

# Tech Stack

### Mobile

* Expo
* React Native
* TypeScript
* React Navigation
* Zustand (State Management)
* React Query (Server State)
* Axios

### Backend

* Node.js
* Express.js
* PostgreSQL / MySQL
* Redis
* Cashfree (Payments)
* MSG91 (OTP)

---

# Project Folder Structure

Below is the **production-ready folder structure** of the application.

```
bookmyturf-app
│
├── app.json
├── package.json
├── tsconfig.json
├── babel.config.js
├── .env
│
├── assets
│   ├── icons
│   ├── images
│   ├── fonts
│   └── animations
│
├── src
│
│   ├── app
│   │   ├── navigation
│   │   │   ├── RootNavigator.tsx
│   │   │   ├── AuthNavigator.tsx
│   │   │   ├── CustomerNavigator.tsx
│   │   │   ├── OwnerNavigator.tsx
│   │   │   └── AdminNavigator.tsx
│   │   │
│   │   ├── providers
│   │   │   ├── AuthProvider.tsx
│   │   │   ├── ThemeProvider.tsx
│   │   │   └── QueryProvider.tsx
│   │   │
│   │   └── App.tsx
│
│   ├── config
│   │   ├── env.ts
│   │   ├── api.ts
│   │   └── constants.ts
│
│   ├── core
│   │   ├── hooks
│   │   │   ├── useAuth.ts
│   │   │   ├── useLocation.ts
│   │   │   ├── useDebounce.ts
│   │   │   └── usePagination.ts
│   │   │
│   │   ├── utils
│   │   │   ├── date.ts
│   │   │   ├── currency.ts
│   │   │   ├── validators.ts
│   │   │   └── helpers.ts
│   │   │
│   │   └── services
│   │       ├── apiClient.ts
│   │       ├── storage.ts
│   │       └── logger.ts
│
│   ├── components
│   │   ├── common
│   │   │   ├── Button.tsx
│   │   │   ├── Input.tsx
│   │   │   ├── Loader.tsx
│   │   │   ├── Avatar.tsx
│   │   │   └── Modal.tsx
│   │   │
│   │   ├── turf
│   │   │   ├── TurfCard.tsx
│   │   │   ├── TurfGallery.tsx
│   │   │   ├── TurfAmenities.tsx
│   │   │   └── TurfReviews.tsx
│   │   │
│   │   ├── booking
│   │   │   ├── SlotPicker.tsx
│   │   │   ├── BookingCard.tsx
│   │   │   └── BookingSummary.tsx
│   │   │
│   │   └── charts
│   │       ├── EarningsChart.tsx
│   │       └── BookingStats.tsx
│
│   ├── features
│   │
│   │   ├── auth
│   │   │   ├── screens
│   │   │   │   ├── LoginScreen.tsx
│   │   │   │   ├── OTPScreen.tsx
│   │   │   │   ├── GoogleLoginScreen.tsx
│   │   │   │   └── CreateProfileScreen.tsx
│   │   │   │
│   │   │   ├── components
│   │   │   │   ├── OTPInput.tsx
│   │   │   │   └── SocialLoginButton.tsx
│   │   │   │
│   │   │   ├── services
│   │   │   │   └── authService.ts
│   │   │   │
│   │   │   └── store
│   │   │       └── authStore.ts
│   │
│   │   ├── customer
│   │   │   ├── screens
│   │   │   │   ├── HomeScreen.tsx
│   │   │   │   ├── SearchScreen.tsx
│   │   │   │   ├── TurfDetailsScreen.tsx
│   │   │   │   ├── BookingScreen.tsx
│   │   │   │   ├── MyBookingsScreen.tsx
│   │   │   │   └── ProfileScreen.tsx
│   │   │
│   │   │   ├── components
│   │   │   │   ├── SearchFilters.tsx
│   │   │   │   ├── TurfList.tsx
│   │   │   │   └── BookingCalendar.tsx
│   │   │
│   │   │   ├── services
│   │   │   │   ├── turfService.ts
│   │   │   │   └── bookingService.ts
│   │   │
│   │   │   └── store
│   │   │       ├── turfStore.ts
│   │   │       └── bookingStore.ts
│   │
│   │   ├── owner
│   │   │   ├── screens
│   │   │   │   ├── DashboardScreen.tsx
│   │   │   │   ├── ManageTurfsScreen.tsx
│   │   │   │   ├── BookingRequestsScreen.tsx
│   │   │   │   ├── EarningsScreen.tsx
│   │   │   │   └── OwnerProfileScreen.tsx
│   │   │
│   │   │   ├── components
│   │   │   │   ├── BookingTable.tsx
│   │   │   │   ├── EarningsSummary.tsx
│   │   │   │   └── SlotManager.tsx
│   │   │
│   │   │   ├── services
│   │   │   │   ├── ownerService.ts
│   │   │   │   └── earningsService.ts
│   │   │
│   │   │   └── store
│   │   │       └── ownerStore.ts
│   │
│   │   ├── admin
│   │   │   ├── screens
│   │   │   │   ├── AdminDashboard.tsx
│   │   │   │   ├── UsersScreen.tsx
│   │   │   │   ├── TurfApprovalScreen.tsx
│   │   │   │   └── AnalyticsScreen.tsx
│   │   │
│   │   │   ├── services
│   │   │   │   └── adminService.ts
│   │   │
│   │   │   └── store
│   │   │       └── adminStore.ts
│   │
│   │   ├── payments
│   │   │   ├── screens
│   │   │   │   └── PaymentScreen.tsx
│   │   │
│   │   │   ├── services
│   │   │   │   └── paymentService.ts
│   │   │
│   │   │   └── components
│   │   │       └── PaymentSummary.tsx
│   │
│   │   └── notifications
│   │       ├── hooks
│   │       │   └── useNotifications.ts
│   │       │
│   │       └── services
│   │           └── notificationService.ts
│
│   ├── store
│   │   ├── rootReducer.ts
│   │   └── middleware.ts
│
│   ├── theme
│   │   ├── colors.ts
│   │   ├── spacing.ts
│   │   └── typography.ts
│
│   └── types
│       ├── auth.ts
│       ├── user.ts
│       ├── turf.ts
│       ├── booking.ts
│       └── payment.ts
```

---

# Folder Explanation

### assets

Stores static resources like images, fonts, icons.

### src/app

Application bootstrap and navigation.

### src/config

Application configuration such as API base URL and environment variables.

### src/core

Reusable utilities, hooks, and global services.

### src/components

Reusable UI components shared across features.

### src/features

Feature-based modules such as:

* Authentication
* Customer flows
* Owner dashboard
* Admin panel
* Payments
* Notifications

### src/store

Global state management.

### src/theme

Centralized design system.

### src/types

Global TypeScript types.

---

# Installation

Clone repository

```
git clone https://github.com/yourusername/bookmyturf-app.git
```

Install dependencies

```
npm install
```

Run the project

```
npx expo start
```

---

# Future Improvements

* Real-time slot locking using Redis
* Push notifications
* AI turf recommendations
* Dynamic pricing
* Advanced analytics

---

# License

MIT License

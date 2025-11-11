# Smart Employee Portal - Frontend

## Enterprise-Grade HR Management React Application

A production-ready React 18+ TypeScript frontend for the Smart Employee Portal HR management system. Features responsive design, real-time notifications, role-based UI, and comprehensive employee management interfaces.

## Features

### User Interface
- Responsive design (Mobile, Tablet, Desktop)
- Role-based UI rendering (ADMIN, HR, MANAGER, EMPLOYEE)
- Dark/Light theme support
- Sidebar navigation
- Loading indicators and skeleton screens
- Toast notifications for feedback
- Confirmation dialogs for actions

### Authentication
- Login/Register pages
- JWT token management
- Persistent authentication
- Secure token refresh
- Password reset flow
- Session timeout handling

### Employee Management
- Employee list with pagination
- Advanced search and filtering
- Employee profile details
- Add/Edit/Delete employees
- Bulk operations
- Export to CSV
- Profile picture upload

### Leave Management
- Leave request submission
- Leave approval workflow
- Leave balance tracker
- Leave calendar view
- Leave history
- Status filtering
- Email notifications

### Performance Management
- Performance reviews
- Rating system (1-5 stars)
- Self-assessment
- Goal tracking
- Review history
- Performance charts

### Dashboard & Analytics
- Key statistics cards
- Employee count
- Department distribution
- Leave statistics charts
- Performance overview
- Real-time updates
- Export reports

### Real-Time Notifications
- WebSocket notifications
- Notification bell with badge
- Notification history
- Mark as read/unread
- Notification filtering
- Sound alerts

## Tech Stack

- **Framework**: React 18+
- **Language**: TypeScript
- **State Management**: Redux Toolkit
- **UI Library**: Material-UI (MUI) v5
- **HTTP Client**: Axios
- **Routing**: React Router v6
- **Forms**: React Hook Form + Yup
- **Real-Time**: Socket.io-client
- **Charts**: Recharts
- **Notifications**: React Toastify
- **Build Tool**: Vite
- **Testing**: Jest + React Testing Library

## Prerequisites

- Node.js 16+ and npm/yarn
- Git
- Backend API running (see backend README)
- Modern web browser

## Installation

### 1. Clone Repository

```bash
git clone https://github.com/yourusername/smart-employee-portal-frontend.git
cd smart-employee-portal-frontend
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment

Create `.env.local` file:

```env
VITE_API_URL=http://localhost:8080/api
VITE_WEBSOCKET_URL=ws://localhost:8080/ws
VITE_APP_NAME=Smart Employee Portal
VITE_APP_VERSION=1.0.0
```

### 4. Start Development Server

```bash
npm run dev
```

App will be available at `http://localhost:5173`

## Project Structure

```
src/
├── components/
│   ├── common/
│   │   ├── Navbar.tsx
│   │   ├── Sidebar.tsx
│   │   ├── Footer.tsx
│   │   └── ProtectedRoute.tsx
│   ├── auth/
│   │   ├── Login.tsx
│   │   ├── Register.tsx
│   │   ├── ForgotPassword.tsx
│   │   └── ResetPassword.tsx
│   ├── employee/
│   │   ├── EmployeeList.tsx
│   │   ├── EmployeeForm.tsx
│   │   ├── EmployeeProfile.tsx
│   │   ├── EmployeeSearch.tsx
│   │   └── EmployeeTable.tsx
│   ├── leave/
│   │   ├── LeaveRequestForm.tsx
│   │   ├── LeaveApprovalList.tsx
│   │   ├── LeaveCalendar.tsx
│   │   ├── LeaveBalance.tsx
│   │   └── LeaveHistory.tsx
│   ├── performance/
│   │   ├── ReviewForm.tsx
│   │   ├── ReviewHistory.tsx
│   │   ├── RatingDisplay.tsx
│   │   └── GoalTracker.tsx
│   ├── dashboard/
│   │   ├── AdminDashboard.tsx
│   │   ├── EmployeeDashboard.tsx
│   │   ├── StatCard.tsx
│   │   ├── Charts.tsx
│   │   └── QuickActions.tsx
│   └── notifications/
│       ├── NotificationBell.tsx
│       ├── NotificationPanel.tsx
│       └── NotificationItem.tsx
├── pages/
│   ├── Dashboard.tsx
│   ├── Employees.tsx
│   ├── Leaves.tsx
│   ├── Performance.tsx
│   ├── Profile.tsx
│   └── NotFound.tsx
├── services/
│   ├── api.ts
│   ├── authService.ts
│   ├── employeeService.ts
│   ├── leaveService.ts
│   ├── performanceService.ts
│   ├── notificationService.ts
│   └── webSocketService.ts
├── store/
│   ├── store.ts
│   ├── slices/
│   │   ├── authSlice.ts
│   │   ├── employeeSlice.ts
│   │   ├── leaveSlice.ts
│   │   ├── performanceSlice.ts
│   │   └── notificationSlice.ts
│   └── middleware/
├── hooks/
│   ├── useAuth.ts
│   ├── useNotification.ts
│   ├── useApi.ts
│   ├── useWebSocket.ts
│   └── useForm.ts
├── utils/
│   ├── constants.ts
│   ├── dateUtils.ts
│   ├── formatters.ts
│   ├── validators.ts
│   └── errorHandler.ts
├── types/
│   ├── index.ts
│   ├── models.ts
│   ├── api.ts
│   └── redux.ts
├── styles/
│   ├── theme.ts
│   ├── globalStyles.ts
│   └── variables.ts
├── App.tsx
├── main.tsx
└── vite-env.d.ts
```

## Available Scripts

```bash
# Development
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Run tests
npm run test

# Run tests with coverage
npm run test:coverage

# Lint code
npm run lint

# Format code
npm run format
```

## Key Components

### Protected Routes
- Role-based route protection
- Automatic redirect to login
- Permission checking

### API Integration
- Axios instance with interceptors
- Request/response transformation
- Error handling
- Token refresh logic

### State Management
- Redux Toolkit for global state
- Async thunks for API calls
- Slice-based architecture
- DevTools integration

### Real-Time Features
- WebSocket connection management
- Automatic reconnection
- Message broadcasting
- Notification handling

## Styling

- Material-UI components
- CSS-in-JS with MUI
- Responsive breakpoints
- Theme customization
- Dark mode support

## Form Handling

- React Hook Form for efficiency
- Yup schema validation
- Error messages
- Loading states
- Async validation

## Authentication Flow

1. User login
2. JWT token received
3. Token stored securely
4. Automatic token refresh before expiry
5. Logout clears tokens
6. Protected routes check authentication

## Deployment

### Build

```bash
npm run build
```

### Deploy to Vercel

1. Push code to GitHub
2. Connect repository to Vercel
3. Configure environment variables
4. Deploy

### Deploy to Netlify

1. Push code to GitHub
2. Connect repository to Netlify
3. Configure build settings:
   - Build command: `npm run build`
   - Publish directory: `dist`
4. Set environment variables
5. Deploy

## Environment Variables

```
VITE_API_URL=Backend API URL
VITE_WEBSOCKET_URL=WebSocket URL
VITE_APP_NAME=Application name
VITE_APP_VERSION=Version
```

## Performance Optimization

- Code splitting with React lazy
- Image optimization
- Bundle size analysis
- Caching strategies
- Memoization for components
- Virtual scrolling for large lists

## Testing

```bash
# Run all tests
npm run test

# Watch mode
npm run test:watch

# Coverage report
npm run test:coverage
```

## Accessibility

- Semantic HTML
- ARIA labels
- Keyboard navigation
- Color contrast
- Screen reader support

## Browser Support

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers

## Error Handling

- Global error boundary
- API error handling
- Form validation errors
- Network error recovery
- Toast notifications

## Security

- XSS protection
- CSRF token handling
- Secure token storage
- Input sanitization
- HTTPS in production

## Documentation

- Storybook for components (optional)
- JSDoc comments
- README files
- TypeScript interfaces
- Environment setup guide

## Troubleshooting

### Port already in use

```bash
npm run dev -- --port 3000
```

### Dependencies conflict

```bash
rm -rf node_modules package-lock.json
npm install
```

### Build issues

```bash
npm run build -- --verbose
```

## Contributing

1. Create feature branch
2. Commit changes
3. Push to GitHub
4. Create Pull Request

## License

MIT License

## Support

For issues and questions, please create an issue on GitHub.

## Related Repositories

- Backend API: https://github.com/srihasa19/smart-employee-portal-backend

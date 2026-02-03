# PRD: Delivery Platform with Real-Time Tracking

**Version:** 1.0
**Date:** January 28, 2026
**Author:** Product Team
**Status:** Planning

---

## 1. Purpose & Problem

**Problem:**
Small businesses and individual customers struggle to find reliable, affordable delivery services with transparent tracking. Existing solutions are either too expensive, lack real-time visibility, or require complex enterprise contracts. Couriers, on the other hand, lack flexible platforms that allow them to manage deliveries efficiently while maximizing their earnings.

**Solution:**
A streamlined, mobile-first delivery platform that connects customers with couriers, enabling seamless delivery scheduling, real-time GPS tracking, and transparent pricing. The platform provides three distinct user experiences—customers requesting deliveries, couriers fulfilling orders, and admins managing operations—all unified through a single, intuitive interface.

**Why This Matters:**
- Democratizes last-mile delivery for small businesses and individuals
- Provides gig economy opportunities for independent couriers
- Offers complete transparency through real-time tracking
- Reduces delivery costs through optimized routing and pricing
- Builds trust through ratings, reviews, and verified profiles

---

## 2. Target Users

**Primary:** Three distinct user personas

**User Personas:**

*Customer (Sender):*
- Individuals or small business owners needing delivery services
- Values transparency, reliability, and real-time updates
- Expects competitive pricing and multiple payment options
- Needs flexible scheduling (same-day and scheduled deliveries)

*Courier (Driver):*
- Independent contractors seeking flexible work
- Needs efficient route planning and clear delivery instructions
- Values fair compensation and quick payouts
- Requires mobile-first interface for on-the-go management

*Admin (Platform Manager):*
- Oversees platform operations and user management
- Monitors delivery metrics and resolves disputes
- Manages courier verification and customer support
- Analyzes business performance and trends

**Prerequisites (for students building this):**
- React fundamentals (components, JSX, props, state)
- React Router
- useState & useEffect hooks
- Tailwind CSS
- Basic JavaScript ES6+
- Understanding of REST APIs
- Basic understanding of geolocation APIs

**Goals:**
- Build production-ready delivery platform capstone project
- Practice complex multi-role state management
- Implement real-time tracking patterns
- Create responsive, accessible interfaces
- Handle complex user flows and permissions

---

## 3. Success Metrics

**Technical Completion:**
- 12+ navigable routes with React Router
- 25+ reusable components created
- 3 state management patterns (useState, useContext, localStorage)
- 100% data persistence (no loss on refresh)
- Fully responsive (375px - 1920px+)
- Role-based access control implemented

**Feature Completion:**
- Complete CRUD for deliveries, users, couriers
- Working search/filter on all list views
- Real-time delivery tracking simulation
- Multi-step delivery request flow
- Order assignment and management system
- Rating and review system
- Notification center with alerts
- Analytics dashboard for admins

**Quality Metrics:**
- Clean, commented code
- No console errors
- Sub-200ms search/filter response
- Passes keyboard navigation test
- Form validation on all inputs
- Smooth map interactions and updates

---

## 4. Functional Requirements

### FR-1: User Registration & Authentication
- [ ] **Customer Sign Up:** Email, password, full name, phone number, profile picture URL
- [ ] **Courier Sign Up:** Email, password, full name, phone, vehicle type, license plate, profile picture URL
- [ ] **Admin Sign Up:** Email, password, full name (invite-only simulation)
- [ ] **Sign In:** Email/password authentication with role detection
- [ ] **Password Recovery:** Reset via email link (simulated)
- [ ] **Profile Management:** Update personal info, change password, upload documents
- [ ] Session persistence using localStorage
- [ ] Form validation with error messages
- [ ] Protected routes based on user role
- [ ] Role-based redirects after login

### FR-2: Customer Dashboard
- [ ] Welcome message with user name
- [ ] Quick action: "Schedule New Delivery" button
- [ ] Active deliveries summary (count and status breakdown)
- [ ] Recent deliveries list (last 5)
- [ ] Saved addresses quick access
- [ ] Spending summary (this month, total)
- [ ] Notification bell with unread count

### FR-3: Delivery Request Flow
- [ ] **Step 1 - Pickup Details:** Address (autocomplete simulation), contact name, phone, pickup instructions, pickup time (now or scheduled)
- [ ] **Step 2 - Drop-off Details:** Address, recipient name, phone, delivery instructions, preferred time window
- [ ] **Step 3 - Package Details:** Size (Small/Medium/Large/Extra Large), weight range, category (Documents/Food/Fragile/Electronics/Other), special handling notes
- [ ] **Step 4 - Review & Price:** Distance calculation, price breakdown (base + distance + size + urgency), estimated delivery time
- [ ] **Step 5 - Payment:** Select payment method, apply promo code, confirm order
- [ ] Progress indicator showing current step
- [ ] Back navigation between steps
- [ ] Save as draft functionality
- [ ] Price updates in real-time as options change

### FR-4: Pricing Calculator
- [ ] Base fare calculation
- [ ] Distance-based pricing (simulated using coordinates)
- [ ] Package size multiplier (Small: 1x, Medium: 1.5x, Large: 2x, XL: 2.5x)
- [ ] Urgency pricing (Express: +50%, Same-day: +25%, Scheduled: 0%)
- [ ] Peak hour surcharge simulation
- [ ] Promo code discounts (percentage or fixed amount)
- [ ] Display price breakdown to customer
- [ ] Minimum and maximum fare limits

### FR-5: Address Management
- [ ] **Create:** Label (Home/Work/Other), full address, city, state, zip, contact name, phone, delivery instructions
- [ ] **Read:** List saved addresses with labels
- [ ] **Update:** Edit address details
- [ ] **Delete:** Remove with confirmation
- [ ] Set default pickup and delivery addresses
- [ ] Quick select from saved addresses in delivery flow
- [ ] Maximum 10 saved addresses per user

### FR-6: Order Tracking (Customer View)
- [ ] Real-time map display with courier location (simulated movement)
- [ ] Delivery status timeline: Placed → Accepted → Picked Up → In Transit → Delivered
- [ ] Estimated time of arrival (ETA) display
- [ ] Courier details: Name, photo, vehicle, rating
- [ ] Contact courier button (simulated)
- [ ] Live distance remaining
- [ ] Delivery route visualization on map
- [ ] Status change notifications
- [ ] Cancel delivery option (if not picked up)

### FR-7: Courier Dashboard
- [ ] Availability toggle (Online/Offline)
- [ ] Earnings summary (Today, This Week, This Month)
- [ ] Active delivery details (if any)
- [ ] New delivery requests feed (when online)
- [ ] Accept/Decline delivery interface
- [ ] Navigation to pickup/drop-off (external maps link)
- [ ] Completed deliveries count
- [ ] Rating display

### FR-8: Courier Delivery Management
- [ ] View incoming delivery requests with details
- [ ] Accept delivery with confirmation
- [ ] Decline delivery with optional reason
- [ ] Update delivery status: Heading to Pickup → Arrived at Pickup → Package Collected → In Transit → Arrived at Destination → Delivered
- [ ] Upload proof of delivery (URL simulation)
- [ ] Add delivery notes
- [ ] Report issue with delivery
- [ ] View customer contact info
- [ ] Earnings calculation per delivery

### FR-9: Order Assignment System
- [ ] Auto-assignment to nearest available courier (simulated)
- [ ] Manual assignment by admin
- [ ] Broadcast to multiple couriers (first to accept gets it)
- [ ] Reassignment if courier declines/cancels
- [ ] Assignment timeout (2 minutes to accept)
- [ ] Assignment history log

### FR-10: Admin Dashboard
- [ ] Platform overview stats: Total Users, Active Couriers, Deliveries Today, Revenue Today
- [ ] Real-time activity feed
- [ ] Alerts: Delayed deliveries, Unassigned orders, Low-rated couriers
- [ ] Quick actions: View all orders, Manage users, View reports
- [ ] System health indicators

### FR-11: Admin User Management
- [ ] View all customers with filters (status, registration date, order count)
- [ ] View all couriers with filters (status, verification, rating)
- [ ] User detail view with activity history
- [ ] Suspend/Activate user accounts
- [ ] Verify courier documents (simulated)
- [ ] Search users by name, email, phone
- [ ] Export user data as CSV/JSON

### FR-12: Admin Order Management
- [ ] View all deliveries with status filters
- [ ] Search by order ID, customer name, courier name
- [ ] Sort by date, status, amount
- [ ] Order detail view with full timeline
- [ ] Manually reassign courier
- [ ] Cancel order with refund note
- [ ] Resolve disputes between customer and courier
- [ ] Add admin notes to orders

### FR-13: Notifications System
- [ ] In-app notification center
- [ ] Notification types: Order updates, Assignment alerts, Payment confirmations, System announcements
- [ ] Mark as read/unread
- [ ] Mark all as read
- [ ] Delete notifications
- [ ] Notification preferences in settings
- [ ] Real-time notification simulation (polling)
- [ ] Unread badge count in header

### FR-14: Payment System
- [ ] **Payment Methods:** Add card details (simulated - card number mask, expiry, CVV)
- [ ] Save multiple payment methods
- [ ] Set default payment method
- [ ] Delete payment method
- [ ] **Checkout:** Select method, apply promo, confirm payment
- [ ] Payment status: Pending, Completed, Failed, Refunded
- [ ] Transaction history
- [ ] Download receipt as PDF (print view)

### FR-15: Courier Earnings & Payouts
- [ ] Earnings dashboard: Daily, Weekly, Monthly breakdowns
- [ ] Earnings per delivery breakdown
- [ ] Pending vs. Paid earnings
- [ ] Payout history
- [ ] Request payout (simulated)
- [ ] Earnings chart visualization
- [ ] Export earnings report

### FR-16: Reviews & Ratings
- [ ] Customer rates courier after delivery (1-5 stars + comment)
- [ ] Courier rates customer (1-5 stars + comment)
- [ ] Display average rating on profiles
- [ ] Review moderation by admin
- [ ] Filter reviews by rating
- [ ] Report inappropriate review
- [ ] Response to review (one response allowed)

### FR-17: Order History
- [ ] List all past deliveries with status
- [ ] Filter by date range, status
- [ ] Search by order ID, address
- [ ] Order detail view with full information
- [ ] Reorder from past delivery (pre-fill addresses)
- [ ] Download receipt
- [ ] Pagination (20 items per page)

### FR-18: Analytics Dashboard (Admin)
- [ ] Revenue metrics: Total, Daily Average, Growth rate
- [ ] Delivery metrics: Total, Success rate, Average delivery time
- [ ] User metrics: Total customers, Total couriers, New signups
- [ ] Top performing couriers list
- [ ] Delivery heatmap by area (simulated)
- [ ] Revenue by time chart (line graph)
- [ ] Deliveries by status (pie chart)
- [ ] Export reports as CSV/JSON

### FR-19: Promo Code Management (Admin)
- [ ] **Create:** Code, discount type (percentage/fixed), value, minimum order, max uses, expiry date, user type restriction
- [ ] **Read:** List all codes with usage stats
- [ ] **Update:** Edit code details
- [ ] **Delete:** Deactivate code
- [ ] Apply code validation in checkout
- [ ] Track usage per code
- [ ] Auto-expire past expiry date

### FR-20: Settings
- [ ] **Profile Settings:** Update name, email, phone, profile picture
- [ ] **Security:** Change password, session management
- [ ] **Notifications:** Toggle email/push for different event types
- [ ] **Payment:** Manage payment methods
- [ ] **Addresses:** Manage saved addresses (customers)
- [ ] **Vehicle:** Update vehicle info (couriers)
- [ ] **App Preferences:** Theme (light/dark), default map view
- [ ] **Data:** Export my data, delete account

### FR-21: Navigation & Layout
- [ ] **Header:** Logo, navigation links, notification bell, user menu
- [ ] **Customer Nav:** Dashboard, My Deliveries, Track, History, Settings
- [ ] **Courier Nav:** Dashboard, Deliveries, Earnings, Settings
- [ ] **Admin Nav:** Dashboard, Orders, Users, Couriers, Analytics, Promotions, Settings
- [ ] Mobile: Hamburger menu with slide-out drawer
- [ ] Bottom navigation for mobile (key actions)
- [ ] Breadcrumb navigation on detail pages
- [ ] Active route highlighting
- [ ] Role-based menu items

### FR-22: Data Persistence & Management
- [ ] All data stored in localStorage
- [ ] Separate storage keys per data type
- [ ] Auto-save on create/update/delete
- [ ] Data validation on load
- [ ] Export all data (JSON)
- [ ] Import data (JSON) - admin only
- [ ] Clear all data option with confirmation
- [ ] Handle corrupted data gracefully
- [ ] Demo data seeding option

---

## 5. Non-Functional Requirements

### NFR-1: Performance
- Initial page load: < 2 seconds
- Route transitions: < 300ms
- Form submissions: Feedback within 100ms
- Search/filter: Updates within 200ms
- Map rendering: < 500ms
- Real-time updates: Polling every 3 seconds (tracking page)
- Bundle size: < 700KB gzipped

### NFR-2: Usability
- All primary actions within 3 clicks
- Clear, specific error messages
- Loading states for all async operations
- Empty states with call-to-action
- Form validation with inline errors
- Tooltips for complex features
- Confirmation dialogs for destructive actions
- Progress indicators for multi-step flows

### NFR-3: Accessibility
- WCAG 2.1 Level AA compliance
- Color contrast ≥ 4.5:1 for normal text
- All interactive elements keyboard accessible
- Proper heading hierarchy (h1 → h2 → h3)
- ARIA labels for icons and interactive elements
- Focus management in modals and drawers
- Skip navigation links
- Screen reader announcements for status changes

### NFR-4: Compatibility
- Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- Desktop screens (1920x1080+)
- Tablets (768x1024)
- Mobile (375x667 minimum)
- Portrait and landscape orientations
- Touch-friendly interface for mobile/tablet

### NFR-5: Reliability
- Application works offline (view cached data, queue actions)
- Data persists across browser sessions
- Handles localStorage quota errors gracefully
- No data loss on browser crashes
- Graceful degradation for unsupported features
- Error boundaries for component failures

### NFR-6: Maintainability
- Component-based architecture
- Consistent naming conventions (PascalCase components, camelCase utilities)
- Well-commented complex logic
- Reusable components with props
- No magic numbers/strings (use constants)
- Separation of concerns (UI, logic, data)
- Custom hooks for shared functionality

### NFR-7: Scalability
- Handle up to 1000 deliveries without performance degradation
- Handle up to 500 users (customers + couriers)
- Handle up to 100 concurrent "active" deliveries
- localStorage usage < 5MB for typical usage
- Pagination for large data sets (20 items per page default)
- Virtualized lists for long data sets

### NFR-8: Security
- Input sanitization on all forms
- XSS prevention
- Secure password handling (hashing simulation)
- Protected routes by role
- Sensitive data masking (card numbers, etc.)
- Session timeout handling
- CSRF protection patterns

---

## 6. Technical Specification

### Tech Stack
- **Framework:** React 18+ (Functional components, hooks)
- **Routing:** React Router 6+
- **Styling:** Tailwind CSS 3+
- **Build Tool:** Vite
- **Data Storage:** localStorage
- **Icons:** Lucide React or Heroicons
- **Charts:** Recharts (for analytics)
- **Maps:** Leaflet with React-Leaflet (or static map simulation)
- **Date Handling:** date-fns
- **UUID:** uuid package

### Architecture

```
src/
├── components/
│   ├── common/           # Button, Card, Modal, Input, SearchBar, Badge, Alert, Spinner, EmptyState
│   ├── delivery/         # DeliveryCard, DeliveryForm, DeliveryTimeline, StatusBadge, PriceBreakdown
│   ├── tracking/         # TrackingMap, CourierMarker, RouteDisplay, ETADisplay
│   ├── orders/           # OrderCard, OrderDetail, OrderFilters, OrderList
│   ├── users/            # UserCard, UserDetail, UserList, ProfileForm
│   ├── couriers/         # CourierCard, CourierDetail, AvailabilityToggle, EarningsCard
│   ├── payments/         # PaymentMethodCard, PaymentForm, TransactionList, Receipt
│   ├── reviews/          # ReviewCard, ReviewForm, RatingStars, ReviewList
│   ├── notifications/    # NotificationItem, NotificationList, NotificationBell
│   ├── analytics/        # StatCard, RevenueChart, DeliveryChart, TopCouriers
│   └── layout/           # Header, Sidebar, Footer, MobileNav, Breadcrumb
├── pages/
│   ├── auth/             # Login, Register, ForgotPassword
│   ├── customer/         # Dashboard, NewDelivery, TrackDelivery, History, Settings
│   ├── courier/          # Dashboard, ActiveDelivery, Earnings, Settings
│   └── admin/            # Dashboard, Orders, Users, Couriers, Analytics, Promotions, Settings
├── context/              # AuthContext, DeliveryContext, NotificationContext, ThemeContext
├── hooks/                # useLocalStorage, useAuth, useDelivery, useNotifications, useGeolocation
├── utils/                # validators, formatters, calculations, generators, constants
├── constants/            # config, enums, defaultData, routes
├── services/             # deliveryService, userService, paymentService (localStorage abstractions)
└── assets/               # images, icons
```

### Routes

**Public Routes:**
```
/                         → Landing page (redirect based on auth)
/login                    → Login page
/register                 → Registration page (role selection)
/register/customer        → Customer registration
/register/courier         → Courier registration
/forgot-password          → Password reset
```

**Customer Routes (Protected):**
```
/customer                 → Redirect to /customer/dashboard
/customer/dashboard       → Customer Dashboard
/customer/new-delivery    → New Delivery Flow (multi-step)
/customer/deliveries      → Active Deliveries List
/customer/deliveries/:id  → Delivery Detail
/customer/track/:id       → Real-time Tracking Page
/customer/history         → Order History
/customer/addresses       → Saved Addresses
/customer/payments        → Payment Methods
/customer/settings        → Account Settings
```

**Courier Routes (Protected):**
```
/courier                  → Redirect to /courier/dashboard
/courier/dashboard        → Courier Dashboard
/courier/deliveries       → My Deliveries (active + completed)
/courier/deliveries/:id   → Delivery Detail
/courier/earnings         → Earnings Dashboard
/courier/payouts          → Payout History
/courier/reviews          → My Reviews
/courier/settings         → Account Settings
```

**Admin Routes (Protected):**
```
/admin                    → Redirect to /admin/dashboard
/admin/dashboard          → Admin Dashboard
/admin/orders             → All Orders
/admin/orders/:id         → Order Detail
/admin/users              → Customer Management
/admin/users/:id          → Customer Detail
/admin/couriers           → Courier Management
/admin/couriers/:id       → Courier Detail
/admin/analytics          → Analytics Dashboard
/admin/promotions         → Promo Code Management
/admin/settings           → Platform Settings
```

### State Management
- **useState:** Local component state, form inputs, UI toggles, modal visibility
- **useContext:** Auth state, user role, theme settings, notifications
- **useReducer:** Complex delivery flow state, order management
- **localStorage:** All persistent data (users, deliveries, payments, settings)

### Data Models

**User (Base):**
```javascript
{
  id: string,                    // UUID
  email: string,                 // Unique, valid email
  passwordHash: string,          // Simulated hash
  firstName: string,             // Max 50 chars
  lastName: string,              // Max 50 chars
  phone: string,                 // Valid phone format
  profilePicture?: string,       // URL
  role: "customer" | "courier" | "admin",
  status: "active" | "suspended" | "pending",
  createdAt: string,             // ISO timestamp
  updatedAt: string
}
```

**Customer (extends User):**
```javascript
{
  ...User,
  role: "customer",
  savedAddresses: Address[],
  defaultPickupAddressId?: string,
  defaultDeliveryAddressId?: string,
  paymentMethods: PaymentMethod[],
  defaultPaymentMethodId?: string,
  totalOrders: number,
  totalSpent: number              // In cents
}
```

**Courier (extends User):**
```javascript
{
  ...User,
  role: "courier",
  vehicleType: "Bicycle" | "Motorcycle" | "Car" | "Van",
  vehiclePlate?: string,
  vehicleColor?: string,
  isOnline: boolean,
  isVerified: boolean,
  currentLocation?: {
    lat: number,
    lng: number,
    updatedAt: string
  },
  rating: number,                 // 0-5, 2 decimal places
  totalRatings: number,
  totalDeliveries: number,
  totalEarnings: number,          // In cents
  pendingEarnings: number         // In cents
}
```

**Address:**
```javascript
{
  id: string,
  label: "Home" | "Work" | "Other",
  customLabel?: string,           // If label is "Other"
  streetAddress: string,
  apartment?: string,
  city: string,
  state: string,
  zipCode: string,
  country: string,                // Default "USA"
  contactName: string,
  contactPhone: string,
  instructions?: string,          // Max 200 chars
  coordinates: {
    lat: number,
    lng: number
  },
  isDefault: boolean
}
```

**Delivery:**
```javascript
{
  id: string,                     // Format: DEL-XXXXXX
  customerId: string,
  courierId?: string,             // Null until assigned

  pickup: {
    address: Address,
    scheduledTime: string,        // ISO timestamp
    actualTime?: string,          // When actually picked up
    instructions?: string
  },

  dropoff: {
    address: Address,
    scheduledTime?: string,       // Estimated delivery window
    actualTime?: string,          // When actually delivered
    instructions?: string,
    proofOfDelivery?: string      // Image URL
  },

  package: {
    size: "Small" | "Medium" | "Large" | "Extra Large",
    weight: "Under 1kg" | "1-5kg" | "5-10kg" | "10-20kg" | "Over 20kg",
    category: "Documents" | "Food" | "Fragile" | "Electronics" | "Clothing" | "Other",
    description?: string,         // Max 200 chars
    specialHandling?: string[]    // ["Fragile", "Keep Upright", "Temperature Sensitive"]
  },

  pricing: {
    baseFare: number,             // In cents
    distanceFare: number,
    sizeFare: number,
    urgencyFare: number,
    peakHourFare: number,
    subtotal: number,
    discount: number,
    promoCode?: string,
    total: number
  },

  distance: number,               // In kilometers
  estimatedDuration: number,      // In minutes

  status: "Pending" | "Accepted" | "Picking Up" | "Picked Up" | "In Transit" | "Arriving" | "Delivered" | "Cancelled",
  paymentStatus: "Pending" | "Paid" | "Failed" | "Refunded",

  timeline: StatusUpdate[],

  customerRating?: Review,
  courierRating?: Review,

  notes?: string,                 // Admin notes
  cancellationReason?: string,

  createdAt: string,
  updatedAt: string
}
```

**StatusUpdate:**
```javascript
{
  status: string,
  timestamp: string,
  location?: {
    lat: number,
    lng: number
  },
  note?: string,
  updatedBy: string               // User ID
}
```

**PaymentMethod:**
```javascript
{
  id: string,
  type: "card" | "mobile_money" | "cash",
  cardBrand?: "Visa" | "Mastercard" | "Amex",
  lastFour?: string,              // Last 4 digits
  expiryMonth?: number,
  expiryYear?: number,
  holderName?: string,
  isDefault: boolean,
  createdAt: string
}
```

**Transaction:**
```javascript
{
  id: string,                     // Format: TXN-XXXXXX
  deliveryId: string,
  userId: string,
  amount: number,                 // In cents
  type: "payment" | "refund" | "payout",
  status: "pending" | "completed" | "failed",
  paymentMethodId?: string,
  description: string,
  createdAt: string
}
```

**Review:**
```javascript
{
  id: string,
  deliveryId: string,
  reviewerId: string,             // Who wrote it
  revieweeId: string,             // Who it's about
  reviewerRole: "customer" | "courier",
  rating: number,                 // 1-5
  comment?: string,               // Max 500 chars
  response?: string,              // Max 300 chars
  status: "visible" | "hidden" | "flagged",
  createdAt: string,
  respondedAt?: string
}
```

**Notification:**
```javascript
{
  id: string,
  userId: string,
  type: "order_update" | "assignment" | "payment" | "review" | "system",
  title: string,
  message: string,
  data?: {                        // Related data
    deliveryId?: string,
    orderId?: string
  },
  isRead: boolean,
  createdAt: string
}
```

**PromoCode:**
```javascript
{
  id: string,
  code: string,                   // Uppercase, unique
  discountType: "percentage" | "fixed",
  discountValue: number,          // Percentage or cents
  minOrderAmount?: number,        // Minimum order in cents
  maxDiscount?: number,           // Cap for percentage discounts
  maxUses?: number,
  usedCount: number,
  validFrom: string,
  expiresAt: string,
  userType?: "customer" | "all",  // Who can use it
  isActive: boolean,
  createdAt: string
}
```

**CourierPayout:**
```javascript
{
  id: string,                     // Format: PAY-XXXXXX
  courierId: string,
  amount: number,                 // In cents
  deliveryIds: string[],          // Deliveries included
  status: "pending" | "processing" | "completed",
  requestedAt: string,
  processedAt?: string
}
```

---

## 7. User Flows

### Customer: Request Delivery Flow
1. Customer logs in and lands on dashboard
2. Clicks "Schedule New Delivery" button
3. **Step 1:** Enters pickup address (or selects saved) and pickup time
4. **Step 2:** Enters drop-off address and recipient details
5. **Step 3:** Selects package size, weight, and category
6. **Step 4:** Reviews route, pricing breakdown, and ETA
7. **Step 5:** Selects payment method, applies promo code
8. Clicks "Confirm & Pay"
9. System validates all data
10. System processes payment (simulated)
11. Delivery created with "Pending" status
12. System broadcasts to available couriers
13. Customer redirected to tracking page
14. Receives notification when courier accepts

### Customer: Track Delivery Flow
1. Customer navigates to "My Deliveries" or clicks notification
2. Selects active delivery
3. Tracking page loads with map
4. Map shows courier's current location (simulated)
5. Timeline shows current status
6. ETA updates as courier progresses
7. Customer receives status update notifications
8. When delivered, prompt to rate courier appears
9. Customer submits rating and optional comment

### Courier: Accept & Complete Delivery Flow
1. Courier logs in and toggles "Online"
2. Dashboard shows new delivery request
3. Courier views details: pickup, dropoff, package, earnings
4. Courier clicks "Accept Delivery"
5. Delivery assigned, status changes to "Accepted"
6. Courier clicks "Navigate to Pickup" (opens maps)
7. Courier arrives, clicks "Arrived at Pickup"
8. Customer notified of arrival
9. Courier collects package, clicks "Package Collected"
10. Status changes to "In Transit"
11. Courier navigates to drop-off
12. Courier clicks "Arrived at Destination"
13. Delivers package, uploads proof photo (URL)
14. Clicks "Mark as Delivered"
15. Delivery complete, earnings added to balance
16. Prompt to rate customer appears

### Admin: Manage Delayed Delivery Flow
1. Admin sees alert for delayed delivery on dashboard
2. Clicks to view delivery details
3. Reviews timeline and courier location
4. Contacts courier (simulated) or adds note
5. If needed, reassigns to different courier
6. Updates customer with explanation (notification)
7. Monitors until delivery completes
8. Reviews if dispute or complaint filed

### Customer: Cancel Delivery Flow
1. Customer opens active delivery
2. Clicks "Cancel Delivery" button
3. System checks if cancellation is allowed (not yet picked up)
4. Confirmation dialog explains refund policy
5. Customer confirms cancellation
6. System updates status to "Cancelled"
7. System processes refund (simulated)
8. Courier notified of cancellation
9. Customer receives confirmation

---

## 8. Design Guidelines

### Color Scheme

**Light Mode:**
- Background: Gray-50 (#F9FAFB)
- Surface: White (#FFFFFF)
- Primary: Indigo-600 (#4F46E5)
- Secondary: Gray-600 (#4B5563)
- Accent: Emerald-500 (#10B981)
- Error: Red-500 (#EF4444)
- Warning: Amber-500 (#F59E0B)
- Text Primary: Gray-900 (#111827)
- Text Secondary: Gray-500 (#6B7280)

**Dark Mode:**
- Background: Gray-900 (#111827)
- Surface: Gray-800 (#1F2937)
- Primary: Indigo-400 (#818CF8)
- Secondary: Gray-400 (#9CA3AF)
- Accent: Emerald-400 (#34D399)
- Error: Red-400 (#F87171)
- Warning: Amber-400 (#FBBF24)
- Text Primary: Gray-50 (#F9FAFB)
- Text Secondary: Gray-400 (#9CA3AF)

**Delivery Status Colors:**
- Pending: Gray-500
- Accepted: Blue-500
- Picking Up: Cyan-500
- Picked Up: Teal-500
- In Transit: Indigo-500
- Arriving: Purple-500
- Delivered: Green-500
- Cancelled: Red-500

**Role Colors:**
- Customer: Blue-500
- Courier: Emerald-500
- Admin: Purple-500

### Typography
- Font Family: Inter, system-ui, sans-serif
- H1: 2.25rem (36px) - Page titles
- H2: 1.875rem (30px) - Section titles
- H3: 1.5rem (24px) - Card titles
- H4: 1.25rem (20px) - Subsection titles
- Body: 1rem (16px)
- Small: 0.875rem (14px)
- XSmall: 0.75rem (12px)

### Spacing
- Base unit: 4px (0.25rem)
- Component padding: 16px
- Card padding: 24px
- Section margin: 32px
- Page padding: 24px (mobile), 48px (desktop)

### Components

**Buttons:**
- Primary: bg-indigo-600 text-white rounded-lg py-2.5 px-5 hover:bg-indigo-700
- Secondary: bg-gray-100 text-gray-700 rounded-lg py-2.5 px-5 hover:bg-gray-200
- Outline: border border-gray-300 rounded-lg py-2.5 px-5 hover:bg-gray-50
- Danger: bg-red-600 text-white rounded-lg py-2.5 px-5 hover:bg-red-700
- Success: bg-emerald-600 text-white rounded-lg py-2.5 px-5 hover:bg-emerald-700
- Sizes: sm (py-1.5 px-3), md (py-2.5 px-5), lg (py-3 px-6)

**Cards:**
- Background: white (dark: gray-800)
- Border-radius: rounded-xl (12px)
- Shadow: shadow-sm hover:shadow-md transition-shadow
- Padding: p-6

**Inputs:**
- Border: border border-gray-300 rounded-lg
- Padding: py-2.5 px-4
- Focus: ring-2 ring-indigo-500 border-transparent
- Error: border-red-500 ring-red-500

**Modals:**
- Max-width: 500px (sm), 700px (md), 900px (lg)
- Centered with backdrop blur
- Rounded-2xl with shadow-xl
- Close button in top-right

**Tables:**
- Header: bg-gray-50 text-gray-600 font-medium
- Rows: hover:bg-gray-50 transition
- Borders: divide-y divide-gray-200
- Pagination: bottom right

**Badges:**
- Rounded-full px-3 py-1 text-sm font-medium
- Colors based on status

**Map:**
- Full width within container
- Min height: 300px mobile, 400px desktop
- Rounded corners to match cards
- Loading state with skeleton

### Layout Specifications

**Customer Layout:**
- Header: Fixed, 64px height
- Max content width: 1280px
- Sidebar: None (top navigation)
- Mobile: Bottom tab navigation for key actions

**Courier Layout:**
- Header: Fixed, 64px height, includes availability toggle
- Max content width: 1024px
- Focus on mobile-first design
- Large touch targets for on-the-go use

**Admin Layout:**
- Sidebar: 256px width, collapsible to 64px (icons only)
- Header: Fixed, 64px height
- Main content: Fluid width with max-width 1400px

---

## 9. Development Plan

### Phase 1: Core Setup & Authentication (Week 1)
- Initialize React + Vite + Tailwind
- Set up React Router with all routes
- Create layout components (Header, Sidebar, Footer, MobileNav)
- Implement AuthContext with role-based login/register
- Build useLocalStorage hook
- Create common components (Button, Input, Card, Modal, Badge)
- Set up protected route wrapper with role checking
- Create demo data seeding utility

**Deliverable:** Working navigation, authentication flow, role-based routing

### Phase 2: Customer Delivery Flow (Week 1-2)
- Customer dashboard with stats and quick actions
- Multi-step delivery request form
- Address management CRUD
- Pricing calculator utility
- Delivery confirmation flow
- Active deliveries list
- Order detail view

**Deliverable:** Complete customer delivery request flow

### Phase 3: Tracking & Real-Time Updates (Week 2)
- Tracking page with map integration
- Courier location simulation (movement along route)
- Delivery status timeline component
- ETA calculation and display
- Status update notifications
- Simulated real-time polling

**Deliverable:** Working delivery tracking system

### Phase 4: Courier Dashboard & Delivery Management (Week 3)
- Courier dashboard with availability toggle
- Incoming delivery requests feed
- Accept/Decline flow
- Active delivery management
- Status update interface
- Proof of delivery upload (URL)
- Courier-side delivery detail view

**Deliverable:** Complete courier experience

### Phase 5: Admin Dashboard & Management (Week 3-4)
- Admin dashboard with platform stats
- Order management with filters and search
- User management (customers)
- Courier management with verification
- Manual order assignment
- Dispute handling interface

**Deliverable:** Complete admin management tools

### Phase 6: Payments & Earnings (Week 4)
- Payment method management (customer)
- Checkout integration in delivery flow
- Transaction history
- Courier earnings dashboard
- Payout request system
- Receipt generation (print view)

**Deliverable:** Complete payment system

### Phase 7: Reviews, Analytics & Notifications (Week 4-5)
- Review submission flow
- Rating display on profiles
- Review moderation (admin)
- Analytics dashboard with charts
- Notification system
- Notification preferences

**Deliverable:** Reviews, analytics, and notifications

### Phase 8: Promotions, Settings & Polish (Week 5)
- Promo code management (admin)
- Promo code application in checkout
- Settings pages for all roles
- Data export/import
- Error handling refinement
- Loading and empty states
- Final responsive fixes
- Accessibility audit

**Deliverable:** Complete, polished application

---

## 10. Testing Requirements

### Functional Testing
- [ ] Customer registration creates account correctly
- [ ] Courier registration creates account with vehicle info
- [ ] Login redirects to correct dashboard based on role
- [ ] Logout clears session and redirects
- [ ] All CRUD operations work for addresses
- [ ] Delivery request flow completes end-to-end
- [ ] Pricing calculates correctly with all factors
- [ ] Promo codes apply discounts correctly
- [ ] Courier can accept and decline deliveries
- [ ] Status updates reflect in tracking view
- [ ] Notifications appear for relevant events
- [ ] Payments process (simulated) correctly
- [ ] Reviews save and display correctly
- [ ] Analytics calculations are accurate
- [ ] Data export produces valid JSON
- [ ] Data import restores state correctly

### Role-Based Access Testing
- [ ] Customers cannot access courier routes
- [ ] Couriers cannot access admin routes
- [ ] Customers cannot access other customers' data
- [ ] Couriers can only manage their own deliveries
- [ ] Admins can access all data

### Responsive Testing
- [ ] Mobile (375px): Single column, bottom nav, hamburger menu
- [ ] Tablet (768px): Adapted navigation, 2 column grids
- [ ] Desktop (1024px+): Full layout, sidebar for admin

### Data Integrity
- [ ] No data loss on refresh
- [ ] Unique IDs generated for all entities
- [ ] Timestamps update correctly
- [ ] Order totals calculate accurately
- [ ] Earnings aggregate correctly for couriers
- [ ] Concurrent operations don't corrupt data

### Map & Tracking Testing
- [ ] Map loads without errors
- [ ] Courier marker displays correctly
- [ ] Simulated movement is smooth
- [ ] ETA updates during delivery
- [ ] Route displays correctly

### Accessibility
- [ ] Keyboard navigation works throughout
- [ ] Focus indicators visible
- [ ] Color contrast passes WCAG AA
- [ ] Screen reader compatible
- [ ] Form errors announced properly
- [ ] Modals trap focus correctly
- [ ] Skip navigation links work

### Edge Cases
- [ ] Empty states display with CTAs
- [ ] No available couriers handled gracefully
- [ ] Network errors show appropriate messages
- [ ] Large data sets paginate correctly
- [ ] Invalid promo codes show clear error
- [ ] Expired sessions redirect to login

---

## 11. Out of Scope

**NOT included in MVP:**
- Real payment processing (Stripe/PayPal integration)
- Real SMS/Email notifications
- Backend/database integration
- Real user authentication (JWT, OAuth)
- Real GPS tracking (requires native app)
- Real address autocomplete (Google Places API)
- Real route calculation (Google Directions API)
- Multi-language support
- Multi-currency support
- Real-time WebSocket updates
- Native mobile apps (iOS/Android)
- Driver background checks
- Insurance integration
- Multi-stop deliveries
- Scheduled recurring deliveries
- In-app messaging/chat

---

## 12. Risks & Mitigations

| Risk | Impact | Mitigation |
|------|--------|------------|
| localStorage quota exceeded | High | Monitor usage, warn at 4MB, provide data cleanup tools |
| Complex multi-role state | High | Clear role separation in components, thorough testing per role |
| Map performance issues | Medium | Lazy load map, use lightweight markers, throttle updates |
| Simulated tracking feels unrealistic | Medium | Implement smooth animations, realistic timing, proper status flow |
| Checkout flow abandonment | Medium | Save progress, allow back navigation, clear error messages |
| Scope creep with roles | Medium | Strict MVP adherence, document stretch goals separately |
| Data model changes mid-project | Medium | Version data schema, provide migration utilities |
| Complex pricing edge cases | Low | Comprehensive testing, clear minimum/maximum limits |

---

## 13. Stretch Goals (Optional)

For advanced students who finish early:

- [ ] Drag-and-drop delivery reordering (admin)
- [ ] Multi-stop delivery support
- [ ] Route optimization suggestions
- [ ] In-app chat between customer and courier
- [ ] Delivery scheduling calendar view
- [ ] Heat map of popular delivery areas
- [ ] Courier leaderboard and gamification
- [ ] Push notification simulation
- [ ] Dark mode map styling
- [ ] Animations with Framer Motion
- [ ] Print invoices and packing slips
- [ ] Batch delivery uploads via CSV
- [ ] Delivery time predictions with ML simulation
- [ ] Customer favorite couriers feature
- [ ] Surge pricing simulation

---

## 14. Definition of Done

Project is complete when:
- ✅ All functional requirements implemented
- ✅ All non-functional requirements met
- ✅ Three roles (customer, courier, admin) fully functional
- ✅ Responsive on mobile, tablet, desktop
- ✅ No console errors in production build
- ✅ All testing checklist items pass
- ✅ README documentation complete
- ✅ Code is clean and commented
- ✅ Demo data seeded for testing
- ✅ Application deployed (optional)

---

## 15. Resources

**Documentation:**
- React: https://react.dev
- React Router: https://reactrouter.com
- Tailwind CSS: https://tailwindcss.com
- Recharts: https://recharts.org
- Lucide Icons: https://lucide.dev
- React-Leaflet: https://react-leaflet.js.org

**Libraries:**
- UUID: `npm install uuid`
- Date formatting: `npm install date-fns`
- Icons: `npm install lucide-react`
- Charts: `npm install recharts`
- Maps: `npm install leaflet react-leaflet`

**Map Resources:**
- OpenStreetMap tiles (free)
- Leaflet documentation: https://leafletjs.com

**Demo Data:**
- Sample addresses: Use real city coordinates
- Sample users: Create 10-15 customers, 5-10 couriers
- Sample deliveries: Generate 20-30 with various statuses

**Estimated Time:** 5-6 weeks (30-40 hours)

---

**Document Status:** ✅ Approved for Development

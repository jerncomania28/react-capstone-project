# PRD: Laundry Service Management Platform

**Version:** 1.0
**Date:** January 28, 2026
**Author:** Product Team
**Status:** Planning

---

## 1. Purpose & Problem

**Problem:**
Laundry service providers struggle with manual order tracking, inefficient communication with customers, and disorganized workflow management. Customers face difficulties scheduling pickups, tracking order status, and making payments—leading to poor customer retention and operational inefficiencies for businesses.

**Solution:**
A comprehensive laundry service management platform that connects customers with service providers through an intuitive interface. The platform enables seamless order placement, real-time tracking, payment processing, and business analytics—all in one unified system that scales from single-location laundromats to multi-branch operations.

**Why This Matters:**
- Eliminates manual tracking and paperwork for businesses
- Provides customers with transparency and convenience
- Streamlines pickup and delivery logistics
- Enables data-driven business decisions through analytics
- Reduces operational costs through workflow optimization
- Builds customer loyalty through seamless experiences

---

## 2. Target Users

**Primary:** Laundry service providers and their customers

**User Personas:**

*Customer (End User):*
- Busy professionals needing convenient laundry services
- Values time-saving features and transparency
- Expects mobile-first experience with real-time updates
- Wants flexible scheduling and multiple payment options

*Business Owner (Admin):*
- Laundry shop owner managing daily operations
- Needs efficient order management and tracking
- Wants business performance insights and analytics
- Requires employee and inventory oversight

*Delivery Personnel:*
- Handles pickup and delivery of laundry orders
- Needs clear route planning and order assignments
- Requires real-time order information
- Values simple, mobile-friendly interface

**Prerequisites (for students building this):**
- React fundamentals (components, JSX, props, state)
- React Router
- useState & useEffect hooks
- Tailwind CSS
- Basic JavaScript ES6+
- Understanding of REST APIs

**Goals:**
- Build production-ready service management capstone project
- Practice role-based access control patterns
- Implement real-time status tracking workflows
- Create responsive, accessible interfaces

---

## 3. Success Metrics

**Technical Completion:**
- 10+ navigable routes with React Router
- 25+ reusable components created
- 3 state management patterns (useState, useContext, localStorage)
- 100% data persistence (no loss on refresh)
- Fully responsive (375px - 1920px+)
- Role-based access control implemented

**Feature Completion:**
- Complete CRUD for orders, services, customers
- Working search/filter on all modules
- Multi-step order placement flow
- Real-time order status tracking
- Business analytics dashboard
- Delivery management system
- Subscription plan management

**Quality Metrics:**
- Clean, commented code
- No console errors
- Sub-200ms search/filter response
- Passes keyboard navigation test
- Form validation on all inputs

---

## 4. Functional Requirements

### FR-1: User Authentication & Authorization
- [ ] **Customer Sign Up:** Email, password, full name, phone number, address
- [ ] **Business Sign Up:** Business name, email, password, phone, location, operating hours
- [ ] **Delivery Personnel:** Added by admin with name, email, phone, vehicle type
- [ ] **Sign In:** Email/password authentication for all user types
- [ ] **Password Recovery:** Reset via email link (simulated)
- [ ] **Profile Management:** Update personal/business info, change password
- [ ] Role-based access control (Customer, Admin, Delivery)
- [ ] Session persistence using localStorage
- [ ] Form validation with error messages
- [ ] Protected routes based on user role

### FR-2: Customer Portal

#### FR-2.1: Service Selection
- [ ] Display available service types (Washing, Dry Cleaning, Ironing, Folding, Express)
- [ ] Show service descriptions and base pricing
- [ ] Select multiple services per order
- [ ] View service-specific options (fabric type, special care instructions)

#### FR-2.2: Order Placement
- [ ] **Step 1:** Select services and item quantities
- [ ] **Step 2:** Add item details (clothing type, quantity, special instructions)
- [ ] **Step 3:** Schedule pickup date and time slot
- [ ] **Step 4:** Schedule delivery date and time slot
- [ ] **Step 5:** Review order summary with pricing
- [ ] **Step 6:** Select payment method and confirm
- [ ] Real-time price calculation based on items and services
- [ ] Apply promotional codes
- [ ] Save addresses for quick ordering
- [ ] Express service option (premium pricing)

#### FR-2.3: Order Tracking
- [ ] View all orders (Active, Completed, Cancelled)
- [ ] Real-time status updates with timeline view
- [ ] Status stages: Placed -> Picked Up -> In Process -> Ready -> Out for Delivery -> Delivered
- [ ] Estimated completion time display
- [ ] Delivery personnel contact info when out for delivery
- [ ] Order history with reorder option

#### FR-2.4: Customer Account
- [ ] View and edit profile information
- [ ] Manage saved addresses (add, edit, delete, set default)
- [ ] View order history with details
- [ ] Manage subscription plans (if subscribed)
- [ ] Payment method management
- [ ] Notification preferences

### FR-3: Business Admin Portal

#### FR-3.1: Dashboard
- [ ] Today's orders summary (new, in progress, completed)
- [ ] Revenue statistics (daily, weekly, monthly)
- [ ] Pending pickups count
- [ ] Active deliveries count
- [ ] Recent activity feed
- [ ] Quick action buttons

#### FR-3.2: Order Management
- [ ] View all orders with status indicators
- [ ] Filter by status (Pending, Picked Up, In Process, Ready, Delivered, Cancelled)
- [ ] Search by order ID, customer name, phone
- [ ] Sort by date, status, total amount
- [ ] Order detail view with full information
- [ ] Update order status with notes
- [ ] Assign orders to delivery personnel
- [ ] Print order receipts/labels
- [ ] Cancel orders with reason

#### FR-3.3: Service Management
- [ ] **Create:** Service name, description, base price, estimated duration, availability
- [ ] **Read:** Display all services with pricing
- [ ] **Update:** Edit service details and pricing
- [ ] **Delete:** Remove services (soft delete)
- [ ] Toggle service availability
- [ ] Set service-specific pricing rules

#### FR-3.4: Pricing Management
- [ ] Define item categories (Shirts, Pants, Dresses, Bedding, etc.)
- [ ] Set prices per item per service type
- [ ] Configure express service multiplier
- [ ] Set minimum order amount
- [ ] Manage promotional codes (create, edit, deactivate)
- [ ] Bulk price updates

#### FR-3.5: Customer Management
- [ ] View all customers with order statistics
- [ ] Search by name, email, phone
- [ ] Customer detail view with order history
- [ ] Add customer notes
- [ ] View customer lifetime value
- [ ] Filter by registration date, order frequency

#### FR-3.6: Delivery Personnel Management
- [ ] Add new delivery personnel
- [ ] View all personnel with status (available, on delivery, offline)
- [ ] Edit personnel details
- [ ] Deactivate personnel accounts
- [ ] View delivery history per personnel
- [ ] Performance metrics (deliveries completed, ratings)

#### FR-3.7: Analytics & Reports
- [ ] Revenue overview with charts (daily, weekly, monthly)
- [ ] Orders by status breakdown
- [ ] Top services by revenue
- [ ] Customer acquisition trends
- [ ] Peak hours analysis
- [ ] Delivery performance metrics
- [ ] Export reports as CSV/JSON

#### FR-3.8: Business Settings
- [ ] Business profile (name, logo, description)
- [ ] Operating hours configuration
- [ ] Service area/delivery zones
- [ ] Notification settings
- [ ] Tax rate configuration
- [ ] Receipt customization

### FR-4: Delivery Personnel Portal

#### FR-4.1: Dashboard
- [ ] Today's assignments overview
- [ ] Pending pickups list
- [ ] Pending deliveries list
- [ ] Completed tasks count
- [ ] Earnings summary (if applicable)

#### FR-4.2: Pickup Management
- [ ] View assigned pickup orders
- [ ] Customer address and contact info
- [ ] Navigation link to address (Google Maps)
- [ ] Mark pickup as completed
- [ ] Add pickup notes/photos
- [ ] Report pickup issues

#### FR-4.3: Delivery Management
- [ ] View assigned delivery orders
- [ ] Customer address and contact info
- [ ] Navigation link to address
- [ ] Mark delivery as completed
- [ ] Collect payment (if cash on delivery)
- [ ] Customer signature/confirmation (simulated)
- [ ] Report delivery issues

#### FR-4.4: Route Optimization
- [ ] View all assignments on map view
- [ ] Suggested optimal route order
- [ ] Estimated time per stop
- [ ] Reorder stops manually

### FR-5: Subscription Plans
- [ ] Display available subscription plans
- [ ] Plan details: items per month, price, savings
- [ ] Subscribe to a plan
- [ ] View subscription status and usage
- [ ] Cancel subscription
- [ ] Subscription renewal notifications

### FR-6: Notifications System
- [ ] In-app notification center
- [ ] Order status update notifications
- [ ] Pickup/delivery reminders
- [ ] Promotional notifications
- [ ] Mark notifications as read
- [ ] Clear all notifications

### FR-7: Payment Processing (Simulated)
- [ ] Multiple payment methods (Card, Mobile Wallet, Cash on Delivery)
- [ ] Secure card input form (simulated)
- [ ] Payment confirmation
- [ ] Payment history
- [ ] Refund processing (admin)
- [ ] Invoice generation

### FR-8: Navigation & Layout
- [ ] **Customer:** Bottom navigation (mobile), header nav (desktop)
- [ ] **Admin:** Sidebar navigation with collapsible sections
- [ ] **Delivery:** Bottom navigation optimized for mobile
- [ ] Responsive hamburger menu
- [ ] Breadcrumb navigation
- [ ] Active route highlighting
- [ ] Keyboard accessible

### FR-9: Data Persistence & Management
- [ ] All data stored in localStorage
- [ ] Auto-save on create/update/delete
- [ ] Data validation on load
- [ ] Export all business data (JSON)
- [ ] Import business data (JSON)
- [ ] Clear demo data option
- [ ] Handle corrupted data gracefully

---

## 5. Non-Functional Requirements

### NFR-1: Performance
- Initial page load: < 2 seconds
- Route transitions: < 300ms
- Form submissions: Feedback within 100ms
- Search/filter: Updates within 200ms
- Image lazy loading for order lists
- Bundle size: < 600KB gzipped

### NFR-2: Usability
- All primary actions within 3 clicks
- Clear, specific error messages
- Loading states for all async operations
- Empty states with call-to-action
- Form validation with inline errors
- Tooltips for complex features
- Confirmation dialogs for destructive actions

### NFR-3: Accessibility
- WCAG 2.1 Level AA compliance
- Color contrast >= 4.5:1 for normal text
- All interactive elements keyboard accessible
- Proper heading hierarchy (h1 -> h2 -> h3)
- ARIA labels where needed
- Focus management in modals
- Skip navigation links

### NFR-4: Compatibility
- Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- Desktop screens (1920x1080+)
- Tablets (768x1024)
- Mobile (375x667 minimum)
- Portrait and landscape orientations

### NFR-5: Reliability
- Application works offline (browse history, view orders)
- Data persists across browser sessions
- Handles localStorage quota errors gracefully
- No data loss on browser crashes
- Graceful degradation for unsupported features

### NFR-6: Maintainability
- Component-based architecture
- Consistent naming conventions (PascalCase components, camelCase utilities)
- Well-commented complex logic
- Reusable components with props
- No magic numbers/strings (use constants)
- Separation of concerns (UI, logic, data)

### NFR-7: Scalability
- Handle up to 500 orders without performance degradation
- Handle up to 1000 customers
- Handle up to 50 delivery personnel
- localStorage usage < 5MB for typical usage
- Pagination for large data sets (20 items per page default)

### NFR-8: Security
- Input sanitization on all forms
- XSS prevention
- Secure password handling (hashing simulation)
- Role-based route protection
- Session timeout handling

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
- **Date Handling:** date-fns
- **Maps:** Static map links (Google Maps URLs)

### Architecture

```
src/
├── components/
│   ├── common/           # Button, Card, Modal, Input, SearchBar, Badge, Alert, Stepper
│   ├── orders/           # OrderCard, OrderDetail, OrderTimeline, OrderForm, OrderFilters
│   ├── services/         # ServiceCard, ServiceForm, ServiceList, PricingTable
│   ├── customers/        # CustomerCard, CustomerDetail, CustomerList
│   ├── delivery/         # DeliveryCard, RouteMap, AssignmentList, DeliveryStatus
│   ├── analytics/        # StatCard, RevenueChart, OrdersChart, TopServices
│   ├── subscriptions/    # PlanCard, SubscriptionStatus, PlanComparison
│   └── layout/           # CustomerNav, AdminSidebar, DeliveryNav, Footer
├── pages/
│   ├── customer/         # Home, Services, PlaceOrder, MyOrders, OrderDetail, Account, Subscriptions
│   ├── admin/            # Dashboard, Orders, Services, Customers, Delivery, Analytics, Settings
│   └── delivery/         # Dashboard, Pickups, Deliveries, RouteView
├── context/              # AuthContext, OrderContext, ThemeContext
├── hooks/                # useLocalStorage, useAuth, useOrders, useServices
├── utils/                # validators, formatters, calculations, generators
├── constants/            # config, enums, defaultData, serviceTypes, statusTypes
└── assets/               # images, icons
```

### Routes

**Public Routes:**
```
/                         → Landing Page
/login                    → Login (role selection)
/register                 → Customer Registration
/register/business        → Business Registration
```

**Customer Routes (Protected):**
```
/customer                 → Redirect to /customer/home
/customer/home            → Customer Home/Services
/customer/services        → Browse Services
/customer/order/new       → Place New Order (multi-step)
/customer/orders          → My Orders List
/customer/orders/:id      → Order Detail & Tracking
/customer/subscriptions   → Subscription Plans
/customer/account         → Account Settings
/customer/addresses       → Manage Addresses
```

**Admin Routes (Protected):**
```
/admin                    → Redirect to /admin/dashboard
/admin/dashboard          → Admin Dashboard
/admin/orders             → Order Management
/admin/orders/:id         → Order Detail
/admin/services           → Service Management
/admin/pricing            → Pricing Management
/admin/customers          → Customer Management
/admin/customers/:id      → Customer Detail
/admin/delivery           → Delivery Personnel Management
/admin/analytics          → Analytics & Reports
/admin/promotions         → Promo Code Management
/admin/settings           → Business Settings
```

**Delivery Routes (Protected):**
```
/delivery                 → Redirect to /delivery/dashboard
/delivery/dashboard       → Delivery Dashboard
/delivery/pickups         → Pickup Assignments
/delivery/pickups/:id     → Pickup Detail
/delivery/deliveries      → Delivery Assignments
/delivery/deliveries/:id  → Delivery Detail
/delivery/route           → Route View
/delivery/history         → Completed Tasks History
```

### State Management
- **useState:** Local component state, form inputs, UI toggles
- **useContext:** Auth state, current user, theme settings
- **useReducer:** Complex order operations, cart management
- **localStorage:** All persistent data (users, orders, services, settings)

### Data Models

**User (Base):**
```javascript
{
  id: string,                    // UUID
  email: string,                 // Unique, valid email
  passwordHash: string,          // Simulated hash
  role: "customer" | "admin" | "delivery",
  createdAt: string,             // ISO timestamp
  updatedAt: string
}
```

**Customer:**
```javascript
{
  ...User,
  role: "customer",
  firstName: string,             // Max 50 chars
  lastName: string,              // Max 50 chars
  phone: string,
  addresses: Address[],
  defaultAddressId?: string,
  subscriptionId?: string,
  notificationPreferences: {
    email: boolean,
    sms: boolean,
    push: boolean
  }
}
```

**BusinessAdmin:**
```javascript
{
  ...User,
  role: "admin",
  businessName: string,          // Max 100 chars
  phone: string,
  address: string,
  operatingHours: OperatingHours,
  logo?: string,                 // URL
  taxRate: number,               // Percentage
  minimumOrderAmount: number     // In cents
}
```

**DeliveryPersonnel:**
```javascript
{
  ...User,
  role: "delivery",
  firstName: string,
  lastName: string,
  phone: string,
  vehicleType: "Bike" | "Scooter" | "Car" | "Van",
  status: "Available" | "On Delivery" | "Offline",
  isActive: boolean,
  totalDeliveries: number,
  rating: number                 // 0-5
}
```

**Address:**
```javascript
{
  id: string,
  label: string,                 // "Home", "Work", etc.
  fullName: string,
  phone: string,
  addressLine1: string,
  addressLine2?: string,
  city: string,
  state: string,
  zipCode: string,
  instructions?: string,         // Delivery instructions
  isDefault: boolean
}
```

**Service:**
```javascript
{
  id: string,
  name: string,                  // Max 100 chars
  slug: string,                  // URL-friendly
  description: string,           // Max 500 chars
  icon: string,                  // Icon name
  basePrice: number,             // In cents
  estimatedDuration: number,     // In hours
  isExpress: boolean,
  expressMultiplier: number,     // e.g., 1.5 for 50% more
  isActive: boolean,
  sortOrder: number,
  createdAt: string,
  updatedAt: string
}
```

**ItemCategory:**
```javascript
{
  id: string,
  name: string,                  // "Shirts", "Pants", etc.
  icon: string,
  pricing: {
    [serviceId: string]: number  // Price per service
  },
  createdAt: string,
  updatedAt: string
}
```

**Order:**
```javascript
{
  id: string,                    // Order number (e.g., ORD-001234)
  customerId: string,
  customerName: string,
  customerPhone: string,
  customerEmail: string,
  pickupAddress: Address,
  deliveryAddress: Address,
  items: OrderItem[],
  services: string[],            // Service IDs
  subtotal: number,              // In cents
  taxAmount: number,
  deliveryFee: number,
  discountAmount: number,
  promoCode?: string,
  total: number,
  status: OrderStatus,
  paymentStatus: "Pending" | "Paid" | "Refunded",
  paymentMethod: "Card" | "Mobile Wallet" | "Cash",
  isExpress: boolean,
  specialInstructions?: string,
  pickupSlot: TimeSlot,
  deliverySlot: TimeSlot,
  assignedPickupPersonId?: string,
  assignedDeliveryPersonId?: string,
  statusHistory: StatusUpdate[],
  estimatedCompletionDate: string,
  actualCompletionDate?: string,
  createdAt: string,
  updatedAt: string
}
```

**OrderStatus:**
```javascript
"Placed" | "Confirmed" | "Pickup Scheduled" | "Picked Up" |
"In Process" | "Ready" | "Out for Delivery" | "Delivered" | "Cancelled"
```

**OrderItem:**
```javascript
{
  id: string,
  categoryId: string,
  categoryName: string,
  quantity: number,
  pricePerItem: number,
  total: number,
  notes?: string
}
```

**TimeSlot:**
```javascript
{
  date: string,                  // YYYY-MM-DD
  startTime: string,             // HH:mm
  endTime: string                // HH:mm
}
```

**StatusUpdate:**
```javascript
{
  status: string,
  note?: string,
  updatedBy: string,             // User ID
  timestamp: string
}
```

**SubscriptionPlan:**
```javascript
{
  id: string,
  name: string,                  // "Basic", "Premium", etc.
  description: string,
  itemsPerMonth: number,
  pricePerMonth: number,         // In cents
  savings: number,               // Percentage saved
  features: string[],
  isPopular: boolean,
  isActive: boolean,
  createdAt: string
}
```

**CustomerSubscription:**
```javascript
{
  id: string,
  customerId: string,
  planId: string,
  status: "Active" | "Paused" | "Cancelled",
  itemsUsedThisMonth: number,
  renewalDate: string,
  startDate: string,
  endDate?: string,
  createdAt: string,
  updatedAt: string
}
```

**PromoCode:**
```javascript
{
  id: string,
  code: string,                  // Uppercase, unique
  discountType: "percentage" | "fixed",
  discountValue: number,
  minOrderAmount?: number,
  maxUses?: number,
  usedCount: number,
  validFrom: string,
  validUntil: string,
  isActive: boolean,
  createdAt: string
}
```

**OperatingHours:**
```javascript
{
  monday: { open: string, close: string, isClosed: boolean },
  tuesday: { open: string, close: string, isClosed: boolean },
  wednesday: { open: string, close: string, isClosed: boolean },
  thursday: { open: string, close: string, isClosed: boolean },
  friday: { open: string, close: string, isClosed: boolean },
  saturday: { open: string, close: string, isClosed: boolean },
  sunday: { open: string, close: string, isClosed: boolean }
}
```

**Notification:**
```javascript
{
  id: string,
  userId: string,
  type: "order_update" | "promotion" | "reminder" | "system",
  title: string,
  message: string,
  orderId?: string,
  isRead: boolean,
  createdAt: string
}
```

---

## 7. User Flows

### Customer: Place Order Flow
1. Customer logs in and lands on home page
2. Clicks "Place Order" or "Schedule Pickup"
3. **Step 1 - Services:** Selects desired services (Wash, Dry Clean, Iron)
4. **Step 2 - Items:** Adds items with quantities per category
5. System calculates real-time pricing
6. **Step 3 - Pickup:** Selects pickup address and time slot
7. **Step 4 - Delivery:** Selects delivery address and time slot
8. **Step 5 - Review:** Reviews order summary, adds promo code if any
9. **Step 6 - Payment:** Selects payment method, enters details
10. Clicks "Place Order"
11. System validates all information
12. System creates order with "Placed" status
13. Confirmation page displays with order number
14. Customer receives notification

### Customer: Track Order Flow
1. Customer navigates to "My Orders"
2. Views list of active and past orders
3. Clicks on an active order
4. Order detail page shows timeline with current status
5. Customer sees estimated completion date
6. When out for delivery, sees delivery person contact
7. Customer can contact support if issues

### Admin: Process Order Flow
1. Admin views dashboard with new orders count
2. Navigates to Orders page
3. Filters by "Placed" status
4. Clicks on new order to view details
5. Reviews items, addresses, special instructions
6. Confirms order (status -> "Confirmed")
7. Schedules pickup, assigns delivery personnel
8. Updates status as order progresses
9. When ready, assigns for delivery
10. Marks as delivered when confirmed

### Delivery: Complete Pickup Flow
1. Delivery person logs in, views dashboard
2. Sees assigned pickups for today
3. Clicks on pickup assignment
4. Views customer address and contact
5. Taps "Navigate" to open maps
6. Arrives at location, collects items
7. Marks pickup as completed, adds notes
8. Items count verified
9. Order status auto-updates to "Picked Up"
10. Moves to next assignment

### Delivery: Complete Delivery Flow
1. Delivery person views delivery assignments
2. Clicks on delivery order
3. Views customer address
4. Navigates to location
5. Delivers items to customer
6. If cash payment, collects and records amount
7. Customer confirms receipt (simulated signature)
8. Marks delivery as completed
9. Order status auto-updates to "Delivered"
10. Customer receives notification

---

## 8. Design Guidelines

### Color Scheme

**Light Mode:**
- Background: Gray-50 (#F9FAFB)
- Surface: White (#FFFFFF)
- Primary: Blue-600 (#2563EB)
- Secondary: Gray-600 (#4B5563)
- Accent: Teal-500 (#14B8A6)
- Error: Red-500 (#EF4444)
- Success: Green-500 (#22C55E)
- Warning: Amber-500 (#F59E0B)
- Text Primary: Gray-900 (#111827)
- Text Secondary: Gray-500 (#6B7280)

**Dark Mode:**
- Background: Gray-900 (#111827)
- Surface: Gray-800 (#1F2937)
- Primary: Blue-400 (#60A5FA)
- Secondary: Gray-400 (#9CA3AF)
- Accent: Teal-400 (#2DD4BF)
- Error: Red-400 (#F87171)
- Success: Green-400 (#4ADE80)
- Warning: Amber-400 (#FBBF24)
- Text Primary: Gray-50 (#F9FAFB)
- Text Secondary: Gray-400 (#9CA3AF)

**Order Status Colors:**
- Placed: Gray-500
- Confirmed: Blue-500
- Pickup Scheduled: Indigo-500
- Picked Up: Purple-500
- In Process: Yellow-500
- Ready: Teal-500
- Out for Delivery: Orange-500
- Delivered: Green-500
- Cancelled: Red-500

**Payment Status:**
- Pending: Yellow-500
- Paid: Green-500
- Refunded: Purple-500

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
- Page padding: 16px (mobile), 32px (desktop)

### Components

**Buttons:**
- Primary: bg-blue-600 text-white rounded-lg py-2.5 px-5
- Secondary: bg-gray-100 text-gray-700 rounded-lg py-2.5 px-5
- Outline: border border-gray-300 rounded-lg py-2.5 px-5
- Danger: bg-red-600 text-white rounded-lg py-2.5 px-5
- Sizes: sm (py-1.5 px-3), md (py-2.5 px-5), lg (py-3 px-6)

**Cards:**
- Background: white (dark: gray-800)
- Border-radius: rounded-xl (12px)
- Shadow: shadow-sm hover:shadow-md
- Padding: p-6

**Inputs:**
- Border: border border-gray-300 rounded-lg
- Padding: py-2.5 px-4
- Focus: ring-2 ring-blue-500 border-transparent
- Error: border-red-500 ring-red-500

**Modals:**
- Max-width: 500px (sm), 700px (md), 900px (lg)
- Centered with backdrop blur
- Rounded-2xl with shadow-xl
- Close button in top-right

**Stepper:**
- Horizontal on desktop, vertical on mobile
- Active step: Primary color
- Completed step: Green with checkmark
- Inactive step: Gray

**Status Badges:**
- Rounded-full px-3 py-1 text-sm font-medium
- Colors based on status

### Layout by Role

**Customer Layout:**
- Mobile: Bottom navigation bar (Home, Orders, Account)
- Desktop: Top header with navigation
- Full-width content area with max-width 1280px

**Admin Layout:**
- Sidebar: 256px width, collapsible to 64px (icons only)
- Top header: 64px height with user menu
- Main content: Fluid width with max-width 1400px

**Delivery Layout:**
- Mobile-first: Bottom navigation bar
- Large touch targets for mobile use
- Simplified interface with essential info

---

## 9. Development Plan

### Phase 1: Core Setup & Authentication (Week 1)
- Initialize React + Vite + Tailwind
- Set up React Router with all routes
- Create layout components (CustomerNav, AdminSidebar, DeliveryNav)
- Implement AuthContext with role-based access
- Build useLocalStorage hook
- Create common components (Button, Input, Card, Modal, Badge)
- Set up protected route wrappers per role

**Deliverable:** Working navigation, authentication flow, role-based layouts

### Phase 2: Service & Pricing Management (Week 1-2)
- Service CRUD operations (Admin)
- Item category management
- Pricing configuration
- ServiceCard component
- Service listing page (Customer)

**Deliverable:** Complete service management module

### Phase 3: Order Placement Flow (Week 2)
- Multi-step order form
- Service selection component
- Item quantity selection
- Address selection/creation
- Time slot picker
- Order summary component
- Price calculation logic
- Promo code application

**Deliverable:** Complete order placement flow for customers

### Phase 4: Order Management (Week 3)
- Order list with filters (Admin)
- Order detail view
- Status update functionality
- Order timeline component
- Order assignment to delivery
- Customer order tracking page
- Status history display

**Deliverable:** Complete order management for admin and tracking for customers

### Phase 5: Delivery Personnel Module (Week 3-4)
- Delivery personnel management (Admin)
- Delivery dashboard
- Pickup assignment view
- Delivery assignment view
- Complete pickup/delivery flows
- Route view with assignments

**Deliverable:** Complete delivery personnel portal

### Phase 6: Analytics & Subscriptions (Week 4)
- Analytics dashboard with charts
- Revenue reports
- Order statistics
- Subscription plans display
- Subscription management

**Deliverable:** Analytics and subscription features

### Phase 7: Settings & Polish (Week 4-5)
- Customer account settings
- Admin business settings
- Notification system
- Data export/import
- Error handling refinement
- Loading and empty states
- Final responsive fixes
- Accessibility audit

**Deliverable:** Complete, polished application

---

## 10. Testing Requirements

### Functional Testing
- [ ] User registration works for all roles
- [ ] Login/logout works with session persistence
- [ ] Role-based access control enforced
- [ ] All CRUD operations work for services
- [ ] Order placement flow completes successfully
- [ ] Price calculation is accurate
- [ ] Promo codes apply correctly
- [ ] Order status updates work
- [ ] Delivery assignment works
- [ ] Pickup/delivery completion works
- [ ] Search returns correct results
- [ ] Filters apply correctly
- [ ] Sort orders data properly
- [ ] Analytics calculations are accurate

### Responsive Testing
- [ ] Mobile (375px): Single column, bottom nav, touch-friendly
- [ ] Tablet (768px): 2 columns, adapted navigation
- [ ] Desktop (1024px+): Full layout, sidebar navigation

### Data Integrity
- [ ] No data loss on refresh
- [ ] Unique IDs generated for all entities
- [ ] Timestamps update correctly
- [ ] Order totals calculate accurately
- [ ] Status transitions are valid
- [ ] Role permissions enforced

### Accessibility
- [ ] Keyboard navigation works throughout
- [ ] Focus indicators visible
- [ ] Color contrast passes WCAG AA
- [ ] Screen reader compatible
- [ ] Form errors announced properly
- [ ] Modals trap focus correctly

### Edge Cases
- [ ] Empty orders list shows appropriate message
- [ ] Invalid promo codes show error
- [ ] Past time slots not selectable
- [ ] Maximum items per order enforced
- [ ] Large data sets don't crash app

---

## 11. Out of Scope

**NOT included in MVP:**
- Real payment processing (Stripe/PayPal integration)
- Real SMS/Email notifications
- Backend/database integration
- Real user authentication (JWT, OAuth)
- Real-time GPS tracking
- Push notifications
- Multi-business support
- Inventory management
- Employee scheduling
- Route optimization algorithm
- Customer reviews/ratings
- Chat support
- Multi-language support
- PWA/offline-first functionality

---

## 12. Risks & Mitigations

| Risk | Impact | Mitigation |
|------|--------|------------|
| localStorage quota exceeded | High | Monitor usage, warn at 4MB, provide data cleanup tools |
| Complex multi-step form state | High | Use useReducer, validate each step, save progress |
| Role-based routing complexity | Medium | Create role-specific route guards, clear access patterns |
| Order status sync issues | Medium | Single source of truth, validate transitions |
| Scope creep | Medium | Strict MVP adherence, document stretch goals separately |
| Performance with large orders | Medium | Pagination, virtualization, lazy loading |
| Browser compatibility issues | Low | Use standard APIs, test on major browsers |

---

## 13. Stretch Goals (Optional)

For advanced students who finish early:
- [ ] Real-time order tracking simulation
- [ ] Drag-and-drop route reordering for delivery
- [ ] SMS notification simulation
- [ ] Customer ratings and reviews
- [ ] Advanced analytics with date comparisons
- [ ] Bulk order import via CSV
- [ ] Print-friendly receipts and invoices
- [ ] Dark mode toggle
- [ ] Animations with Framer Motion
- [ ] PWA with offline support
- [ ] QR code for order tracking
- [ ] Recurring order scheduling

---

## 14. Definition of Done

Project is complete when:
- [ ] All functional requirements implemented
- [ ] All non-functional requirements met
- [ ] Responsive on mobile, tablet, desktop
- [ ] No console errors in production build
- [ ] All testing checklist items pass
- [ ] README documentation complete
- [ ] Code is clean and commented
- [ ] Demo data seeded for testing
- [ ] Role-based access working correctly
- [ ] Application deployed (optional)

---

## 15. Resources

**Documentation:**
- React: https://react.dev
- React Router: https://reactrouter.com
- Tailwind CSS: https://tailwindcss.com
- Recharts: https://recharts.org
- Lucide Icons: https://lucide.dev

**Libraries:**
- UUID: `npm install uuid`
- Date formatting: `npm install date-fns`
- Icons: `npm install lucide-react`
- Charts: `npm install recharts`

**Demo Data:**
- Sample services: Create 5-6 service types
- Sample items: Create 15-20 item categories
- Sample orders: Generate 20-30 sample orders
- Sample customers: Create 10-15 sample customers
- Sample delivery personnel: Create 3-5 delivery accounts

**Estimated Time:** 4-5 weeks (25-35 hours)

---

**Document Status:** Approved for Development

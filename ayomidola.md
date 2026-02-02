# PRD: Online Storefront for Small Business Owners

**Version:** 1.0
**Date:** January 28, 2026
**Author:** Product Team
**Status:** Planning

---

## 1. Purpose & Problem

**Problem:**
Small business owners face significant barriers when trying to establish an online presence. Traditional e-commerce platforms are often expensive, overly complex, or require technical expertise that many small business owners lack. This results in lost sales opportunities and difficulty competing with larger businesses.

**Solution:**
A streamlined, mobile-first storefront platform that empowers small business owners to create, customize, and manage their digital stores with minimal technical knowledge. The platform provides essential e-commerce features—product listings, payment processing, order management, and analytics—in an intuitive interface.

**Why This Matters:**
- Democratizes e-commerce for non-technical business owners
- Reduces time-to-market for small businesses going digital
- Consolidates essential business tools into one platform
- Provides actionable insights through integrated analytics

---

## 2. Target Users

**Primary:** Small business owners with 1-50 employees

**User Personas:**

*Business Owner (Store Admin):*
- Limited technical background
- Needs quick setup and easy management
- Values time-saving automation
- Requires mobile access to manage on-the-go

*Customer (Shopper):*
- Expects seamless shopping experience
- Values quick checkout process
- Wants order tracking and communication
- May return for repeat purchases

**Prerequisites (for students building this):**
- React fundamentals (components, JSX, props, state)
- React Router
- useState & useEffect hooks
- Tailwind CSS
- Basic JavaScript ES6+
- Understanding of REST APIs

**Goals:**
- Build production-ready e-commerce capstone project
- Practice complex state management patterns
- Implement secure payment workflows
- Create responsive, accessible interfaces

---

## 3. Success Metrics

**Technical Completion:**
- 8+ navigable routes with React Router
- 20+ reusable components created
- 3 state management patterns (useState, useContext, localStorage)
- 100% data persistence (no loss on refresh)
- Fully responsive (375px - 1920px+)

**Feature Completion:**
- Complete CRUD for products, orders, customers
- Working search/filter on product catalog
- Shopping cart with persistent state
- Checkout flow with validation
- Order management dashboard
- Analytics dashboard with charts
- Theme customization system

**Quality Metrics:**
- Clean, commented code
- No console errors
- Sub-200ms search/filter response
- Passes keyboard navigation test
- Form validation on all inputs

---

## 4. Functional Requirements

### FR-1: User Registration & Authentication
- [ ] **Sign Up:** Email, password, business name, phone number
- [ ] **Sign In:** Email/password authentication
- [ ] **Password Recovery:** Reset via email link (simulated)
- [ ] **Profile Management:** Update business info, change password
- [ ] Session persistence using localStorage
- [ ] Form validation with error messages
- [ ] Protected routes for authenticated users

### FR-2: Store Setup & Customization
- [ ] **Store Profile:** Business name, tagline, description, contact info
- [ ] **Branding:** Upload logo URL, select primary/secondary colors
- [ ] **Theme Selection:** Choose from 4 pre-built themes (Modern, Classic, Minimal, Bold)
- [ ] **Layout Options:** Grid or list product display
- [ ] **Social Links:** Facebook, Instagram, Twitter, WhatsApp URLs
- [ ] **Business Hours:** Set operating hours display
- [ ] Live preview of customizations

### FR-3: Product Management
- [ ] **Create:** Form with name, description, price, compare price, SKU, stock quantity, category, tags, images (URLs), status
- [ ] **Read:** Display in grid (4/3/2/1 cols) or list view
- [ ] **Update:** Edit existing products inline or via modal
- [ ] **Delete:** Remove with confirmation dialog
- [ ] **Bulk Actions:** Select multiple products for status change or deletion
- [ ] Filter by category, status, stock level
- [ ] Search by name, SKU, description
- [ ] Sort by price, name, date added, stock
- [ ] Image gallery with primary image selection
- [ ] Low stock alerts (configurable threshold)

### FR-4: Category Management
- [ ] **Create:** Category name, description, image URL, parent category (optional)
- [ ] **Read:** Display in hierarchical list
- [ ] **Update:** Edit category details
- [ ] **Delete:** Remove with product reassignment option
- [ ] Drag-and-drop reordering
- [ ] Category-based navigation for storefront

### FR-5: Shopping Cart
- [ ] Add products to cart with quantity selection
- [ ] Update quantity in cart
- [ ] Remove items from cart
- [ ] Cart persistence across sessions (localStorage)
- [ ] Display subtotal, taxes, shipping, total
- [ ] Apply promotional codes
- [ ] Cart item count badge in navigation
- [ ] Empty cart state with call-to-action
- [ ] Stock validation before checkout

### FR-6: Checkout Flow
- [ ] **Step 1:** Contact information (email, phone)
- [ ] **Step 2:** Shipping address (name, address, city, state, zip, country)
- [ ] **Step 3:** Shipping method selection (flat rate options)
- [ ] **Step 4:** Payment method (simulated - card details form)
- [ ] **Step 5:** Order review and confirmation
- [ ] Form validation at each step
- [ ] Progress indicator
- [ ] Order summary sidebar
- [ ] Guest checkout option
- [ ] Save address for registered customers

### FR-7: Order Management (Admin Dashboard)
- [ ] View all orders with status indicators
- [ ] Filter by status (Pending, Processing, Shipped, Delivered, Cancelled)
- [ ] Search by order ID, customer name, email
- [ ] Sort by date, total, status
- [ ] Order detail view with full information
- [ ] Update order status with notes
- [ ] Print packing slip (print-friendly view)
- [ ] Order timeline showing status history
- [ ] Customer communication log

### FR-8: Customer Management
- [ ] View all customers with order count and total spent
- [ ] Search by name, email, phone
- [ ] Customer detail view with order history
- [ ] Customer notes for admin reference
- [ ] Filter by registration date, order count

### FR-9: Customer Storefront
- [ ] Homepage with featured products, categories, promotions
- [ ] Product listing page with filters and search
- [ ] Product detail page with images, description, reviews
- [ ] Category pages
- [ ] Search results page
- [ ] About page with business info
- [ ] Contact page with form

### FR-10: Customer Accounts
- [ ] Registration with email and password
- [ ] Login/logout functionality
- [ ] Profile management (name, email, addresses)
- [ ] Order history view
- [ ] Order tracking with status updates
- [ ] Saved addresses for quick checkout
- [ ] Wishlist functionality

### FR-11: Product Reviews
- [ ] Submit review with rating (1-5 stars) and comment
- [ ] Display reviews on product page
- [ ] Average rating calculation
- [ ] Review moderation (approve/reject) for admin
- [ ] Filter reviews by rating
- [ ] Helpful votes on reviews

### FR-12: Analytics Dashboard
- [ ] Sales overview: Total revenue, orders, average order value
- [ ] Time-based charts: Daily, weekly, monthly sales
- [ ] Top-selling products list
- [ ] Low stock alerts
- [ ] Customer acquisition metrics
- [ ] Revenue by category breakdown
- [ ] Export data as CSV/JSON

### FR-13: Marketing & Promotions
- [ ] **Create Promo Code:** Code, discount type (percentage/fixed), value, min order, expiry date
- [ ] **Manage Codes:** View, edit, deactivate codes
- [ ] Usage tracking per code
- [ ] Featured products selection
- [ ] Banner management for homepage
- [ ] Social media share buttons on products

### FR-14: Navigation & Layout
- [ ] **Admin:** Sidebar navigation with collapsible sections
- [ ] **Storefront:** Header with logo, nav links, cart, account
- [ ] Mobile: Hamburger menu with slide-out drawer
- [ ] Breadcrumb navigation
- [ ] Footer with links, social media, contact info
- [ ] Active route highlighting
- [ ] Keyboard accessible

### FR-15: Data Persistence & Management
- [ ] All data stored in localStorage
- [ ] Auto-save on create/update/delete
- [ ] Data validation on load
- [ ] Export all store data (JSON)
- [ ] Import store data (JSON)
- [ ] Clear all data option with confirmation
- [ ] Handle corrupted data gracefully

---

## 5. Non-Functional Requirements

### NFR-1: Performance
- Initial page load: < 2 seconds
- Route transitions: < 300ms
- Form submissions: Feedback within 100ms
- Search/filter: Updates within 200ms
- Image lazy loading for product grids
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
- Color contrast ≥ 4.5:1 for normal text
- All interactive elements keyboard accessible
- Proper heading hierarchy (h1 → h2 → h3)
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
- Application works offline (browse products, manage cart)
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
- Handle up to 1000 products without performance degradation
- Handle up to 5000 orders
- Handle up to 2000 customers
- localStorage usage < 5MB for typical usage
- Pagination for large data sets (20 items per page default)

### NFR-8: Security
- Input sanitization on all forms
- XSS prevention
- Secure password handling (hashing simulation)
- Protected admin routes
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
- **Date Handling:** date-fns

### Architecture

```
src/
├── components/
│   ├── common/           # Button, Card, Modal, Input, SearchBar, Badge, Alert
│   ├── products/         # ProductCard, ProductForm, ProductGrid, ProductFilters
│   ├── cart/             # CartItem, CartSummary, CartDrawer
│   ├── checkout/         # CheckoutForm, AddressForm, PaymentForm, OrderSummary
│   ├── orders/           # OrderCard, OrderDetail, OrderTimeline, OrderFilters
│   ├── customers/        # CustomerCard, CustomerDetail, CustomerList
│   ├── analytics/        # StatCard, SalesChart, TopProducts, RevenueByCategory
│   ├── storefront/       # Hero, FeaturedProducts, CategoryNav, ProductReview
│   └── layout/           # AdminSidebar, StorefrontHeader, Footer
├── pages/
│   ├── admin/            # Dashboard, Products, Orders, Customers, Settings, Analytics
│   └── storefront/       # Home, ProductListing, ProductDetail, Cart, Checkout, Account
├── context/              # AuthContext, CartContext, ThemeContext, StoreContext
├── hooks/                # useLocalStorage, useAuth, useCart, useProducts, useOrders
├── utils/                # validators, formatters, calculations, generators
├── constants/            # config, enums, defaultData
└── assets/               # images, fonts
```

### Routes

**Admin Routes (Protected):**
```
/admin                    → Redirect to /admin/dashboard
/admin/dashboard          → Admin Dashboard
/admin/products           → Product Management
/admin/products/new       → Add Product
/admin/products/:id       → Edit Product
/admin/categories         → Category Management
/admin/orders             → Order Management
/admin/orders/:id         → Order Detail
/admin/customers          → Customer Management
/admin/customers/:id      → Customer Detail
/admin/analytics          → Analytics Dashboard
/admin/promotions         → Promo Code Management
/admin/settings           → Store Settings
```

**Storefront Routes:**
```
/                         → Storefront Home
/products                 → Product Listing
/products/:id             → Product Detail
/category/:slug           → Category Products
/cart                     → Shopping Cart
/checkout                 → Checkout Flow
/checkout/success         → Order Confirmation
/account                  → Customer Account (Protected)
/account/orders           → Order History
/account/orders/:id       → Order Detail
/login                    → Customer Login
/register                 → Customer Registration
/about                    → About Page
/contact                  → Contact Page
```

### State Management
- **useState:** Local component state, form inputs, UI toggles
- **useContext:** Auth state, cart state, theme settings, store config
- **useReducer:** Complex cart operations, order management
- **localStorage:** All persistent data (products, orders, customers, settings)

### Data Models

**User (Business Owner/Admin):**
```javascript
{
  id: string,                    // UUID
  email: string,                 // Unique, valid email
  passwordHash: string,          // Simulated hash
  businessName: string,          // Max 100 chars
  phone: string,
  role: "admin",
  createdAt: string,             // ISO timestamp
  updatedAt: string
}
```

**Customer:**
```javascript
{
  id: string,
  email: string,
  passwordHash: string,
  firstName: string,             // Max 50 chars
  lastName: string,              // Max 50 chars
  phone?: string,
  addresses: Address[],
  defaultAddressId?: string,
  wishlist: string[],            // Product IDs
  createdAt: string,
  updatedAt: string
}
```

**Address:**
```javascript
{
  id: string,
  firstName: string,
  lastName: string,
  address1: string,
  address2?: string,
  city: string,
  state: string,
  zipCode: string,
  country: string,
  phone: string,
  isDefault: boolean
}
```

**Product:**
```javascript
{
  id: string,                    // UUID
  name: string,                  // Max 150 chars
  slug: string,                  // URL-friendly
  description: string,           // Max 2000 chars
  price: number,                 // In cents
  comparePrice?: number,         // Original price for sales
  sku: string,                   // Unique
  stockQuantity: number,
  lowStockThreshold: number,     // Default 10
  categoryId: string,
  tags: string[],
  images: string[],              // URLs, first is primary
  status: "Active" | "Draft" | "Archived",
  featured: boolean,
  averageRating: number,         // 0-5
  reviewCount: number,
  createdAt: string,
  updatedAt: string
}
```

**Category:**
```javascript
{
  id: string,
  name: string,                  // Max 50 chars
  slug: string,
  description?: string,          // Max 500 chars
  imageUrl?: string,
  parentId?: string,             // For subcategories
  sortOrder: number,
  createdAt: string,
  updatedAt: string
}
```

**Order:**
```javascript
{
  id: string,                    // Order number (e.g., ORD-001234)
  customerId?: string,           // Null for guest checkout
  customerEmail: string,
  customerPhone: string,
  shippingAddress: Address,
  billingAddress: Address,
  items: OrderItem[],
  subtotal: number,              // In cents
  shippingCost: number,
  taxAmount: number,
  discountAmount: number,
  promoCode?: string,
  total: number,
  status: "Pending" | "Processing" | "Shipped" | "Delivered" | "Cancelled",
  paymentStatus: "Pending" | "Paid" | "Refunded",
  paymentMethod: string,
  notes?: string,
  statusHistory: StatusUpdate[],
  createdAt: string,
  updatedAt: string
}
```

**OrderItem:**
```javascript
{
  productId: string,
  productName: string,
  productImage: string,
  sku: string,
  price: number,                 // Price at time of purchase
  quantity: number,
  total: number
}
```

**StatusUpdate:**
```javascript
{
  status: string,
  note?: string,
  timestamp: string
}
```

**CartItem:**
```javascript
{
  productId: string,
  quantity: number,
  addedAt: string
}
```

**Review:**
```javascript
{
  id: string,
  productId: string,
  customerId: string,
  customerName: string,
  rating: number,                // 1-5
  comment: string,               // Max 1000 chars
  status: "Pending" | "Approved" | "Rejected",
  helpfulVotes: number,
  createdAt: string
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
  expiresAt?: string,
  isActive: boolean,
  createdAt: string
}
```

**StoreSettings:**
```javascript
{
  businessName: string,
  tagline?: string,
  description?: string,
  logo?: string,
  contactEmail: string,
  contactPhone: string,
  address?: string,
  socialLinks: {
    facebook?: string,
    instagram?: string,
    twitter?: string,
    whatsapp?: string
  },
  theme: {
    name: "Modern" | "Classic" | "Minimal" | "Bold",
    primaryColor: string,
    secondaryColor: string,
    mode: "light" | "dark" | "auto"
  },
  currency: string,              // Default "USD"
  taxRate: number,               // Percentage
  shippingRates: ShippingRate[],
  lowStockThreshold: number
}
```

**ShippingRate:**
```javascript
{
  id: string,
  name: string,                  // e.g., "Standard Shipping"
  price: number,
  estimatedDays: string          // e.g., "5-7 business days"
}
```

---

## 7. User Flows

### Business Owner: Add Product Flow
1. Admin navigates to Products page
2. Clicks "Add Product" button
3. Form page opens with required fields
4. Admin fills: name, description, price, SKU, stock, category
5. Admin optionally adds: compare price, tags, multiple images
6. Admin sets status (Draft/Active)
7. Admin clicks "Save Product"
8. System validates all fields
9. System generates slug from name
10. System saves to localStorage
11. Success notification appears
12. Redirects to product list with new product visible

### Customer: Purchase Flow
1. Customer browses storefront homepage
2. Clicks on a product category or searches
3. Views product listing with filters
4. Clicks on product to view details
5. Selects quantity and clicks "Add to Cart"
6. Cart drawer slides open showing item added
7. Customer continues shopping or clicks "Checkout"
8. Enters contact information
9. Enters shipping address
10. Selects shipping method
11. Enters payment details (simulated)
12. Reviews order summary
13. Clicks "Place Order"
14. System validates all information
15. System creates order with "Pending" status
16. System clears cart
17. Confirmation page displays with order number
18. Customer receives order details

### Business Owner: Process Order Flow
1. Admin sees notification of new order
2. Navigates to Orders page
3. Clicks on new order to view details
4. Reviews items, shipping address, payment status
5. Updates status to "Processing"
6. Adds note: "Preparing for shipment"
7. Prints packing slip
8. Updates status to "Shipped"
9. Enters tracking information (note)
10. Customer can view updated status in their account

### Customer: Search Products Flow
1. Customer types in search bar
2. System debounces input (300ms)
3. Search results page displays
4. Results show matching products by name/description
5. Customer applies category filter
6. Customer sorts by price (low to high)
7. Results update in real-time
8. Customer clicks product to view details

---

## 8. Design Guidelines

### Color Scheme

**Light Mode:**
- Background: Gray-50 (#F9FAFB)
- Surface: White (#FFFFFF)
- Primary: Blue-600 (#2563EB)
- Secondary: Gray-600 (#4B5563)
- Accent: Green-500 (#22C55E)
- Error: Red-500 (#EF4444)
- Text Primary: Gray-900 (#111827)
- Text Secondary: Gray-500 (#6B7280)

**Dark Mode:**
- Background: Gray-900 (#111827)
- Surface: Gray-800 (#1F2937)
- Primary: Blue-400 (#60A5FA)
- Secondary: Gray-400 (#9CA3AF)
- Accent: Green-400 (#4ADE80)
- Error: Red-400 (#F87171)
- Text Primary: Gray-50 (#F9FAFB)
- Text Secondary: Gray-400 (#9CA3AF)

**Status Colors:**
- Pending: Yellow-500
- Processing: Blue-500
- Shipped: Purple-500
- Delivered: Green-500
- Cancelled: Red-500

**Stock Status:**
- In Stock: Green-500
- Low Stock: Yellow-500
- Out of Stock: Red-500

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

**Tables:**
- Header: bg-gray-50 text-gray-600 font-medium
- Rows: hover:bg-gray-50 transition
- Borders: divide-y divide-gray-200
- Pagination: bottom right

**Badges:**
- Rounded-full px-3 py-1 text-sm font-medium
- Colors based on status/type

### Admin Layout
- Sidebar: 256px width, collapsible to 64px (icons only)
- Main content: Fluid width with max-width 1400px
- Header: Fixed height 64px

### Storefront Layout
- Header: Fixed, 64px height
- Max content width: 1280px
- Product grid: 4 cols (xl), 3 cols (lg), 2 cols (md), 1 col (sm)

---

## 9. Development Plan

### Phase 1: Core Setup & Authentication (Week 1)
- Initialize React + Vite + Tailwind
- Set up React Router with all routes
- Create layout components (AdminSidebar, StorefrontHeader, Footer)
- Implement AuthContext with login/register
- Build useLocalStorage hook
- Create common components (Button, Input, Card, Modal)
- Set up protected route wrapper

**Deliverable:** Working navigation, authentication flow, layout structure

### Phase 2: Product & Category Management (Week 1-2)
- Category CRUD operations
- ProductForm component with validation
- ProductCard component
- ProductGrid with grid/list toggle
- Search and filter functionality
- Bulk actions implementation
- Image gallery component

**Deliverable:** Complete product management module

### Phase 3: Storefront & Cart (Week 2)
- Storefront homepage with hero and featured products
- Product listing page with filters
- Product detail page
- CartContext with useReducer
- Cart drawer component
- Cart page with summary
- Wishlist functionality

**Deliverable:** Browsable storefront with cart functionality

### Phase 4: Checkout & Orders (Week 3)
- Multi-step checkout form
- Address management
- Order creation logic
- Order confirmation page
- Order management dashboard (admin)
- Order detail view with timeline
- Customer order history

**Deliverable:** Complete checkout and order management

### Phase 5: Customer Management & Reviews (Week 3-4)
- Customer list and detail views
- Customer account pages
- Product review system
- Review moderation (admin)

**Deliverable:** Customer features complete

### Phase 6: Analytics & Marketing (Week 4)
- Analytics dashboard with charts
- Sales reports
- Promo code management
- Featured products and banners
- Data export functionality

**Deliverable:** Analytics and marketing tools

### Phase 7: Settings & Polish (Week 4-5)
- Store settings page
- Theme customization
- Data import/export
- Error handling refinement
- Loading and empty states
- Final responsive fixes
- Accessibility audit

**Deliverable:** Complete, polished application

---

## 10. Testing Requirements

### Functional Testing
- [ ] User registration creates account correctly
- [ ] Login/logout works with session persistence
- [ ] All CRUD operations work for products
- [ ] All CRUD operations work for categories
- [ ] Cart add/update/remove functions correctly
- [ ] Cart persists across page refreshes
- [ ] Checkout flow completes successfully
- [ ] Order is created with correct totals
- [ ] Promo codes apply discounts correctly
- [ ] Search returns correct results
- [ ] Filters apply correctly
- [ ] Sort orders data properly
- [ ] Analytics calculations are accurate

### Responsive Testing
- [ ] Mobile (375px): Single column, hamburger menu, touch-friendly
- [ ] Tablet (768px): 2 columns, adapted navigation
- [ ] Desktop (1024px+): Full layout, sidebar navigation

### Data Integrity
- [ ] No data loss on refresh
- [ ] Unique IDs generated for all entities
- [ ] Timestamps update correctly
- [ ] Order totals calculate accurately
- [ ] Stock decrements on purchase
- [ ] Concurrent cart operations don't corrupt data

### Accessibility
- [ ] Keyboard navigation works throughout
- [ ] Focus indicators visible
- [ ] Color contrast passes WCAG AA
- [ ] Screen reader compatible
- [ ] Form errors announced properly
- [ ] Modals trap focus correctly

### Edge Cases
- [ ] Empty cart checkout prevented
- [ ] Out of stock items can't be added
- [ ] Invalid promo codes show error
- [ ] Maximum cart quantity enforced
- [ ] Large data sets don't crash app

---

## 11. Out of Scope

**NOT included in MVP:**
- Real payment processing (Stripe/PayPal integration)
- Real email notifications
- Backend/database integration
- Real user authentication (JWT, OAuth)
- Multiple store support
- Multi-currency support
- Inventory management across locations
- Shipping carrier integration (UPS, FedEx)
- Tax calculation by region
- Real-time notifications (WebSockets)
- PWA/offline-first functionality
- SEO optimization
- Multi-language support

---

## 12. Risks & Mitigations

| Risk | Impact | Mitigation |
|------|--------|------------|
| localStorage quota exceeded | High | Monitor usage, warn at 4MB, provide data cleanup tools |
| Complex cart state bugs | High | Use useReducer with immutable updates, thorough testing |
| Checkout flow abandonment | Medium | Save progress, allow back navigation, clear error messages |
| Performance with large catalogs | Medium | Pagination, virtualization for lists, lazy loading images |
| Scope creep | Medium | Strict MVP adherence, document stretch goals separately |
| Data model changes mid-project | Medium | Version data schema, provide migration utilities |
| Browser compatibility issues | Low | Use standard APIs, test on major browsers |

---

## 13. Stretch Goals (Optional)

For advanced students who finish early:

- [ ] Drag-and-drop product reordering
- [ ] Rich text editor for product descriptions
- [ ] Multiple product variants (size, color)
- [ ] Inventory tracking with low-stock notifications
- [ ] Customer segmentation and tags
- [ ] Email template previews
- [ ] Advanced analytics with date range comparisons
- [ ] Bulk product import via CSV
- [ ] Product recommendations ("You may also like")
- [ ] Recently viewed products
- [ ] Animations with Framer Motion
- [ ] Print invoices/receipts
- [ ] Multi-image upload simulation
- [ ] Store preview mode (customer view)

---

## 14. Definition of Done

Project is complete when:
- ✅ All functional requirements implemented
- ✅ All non-functional requirements met
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

**Libraries:**
- UUID: `npm install uuid`
- Date formatting: `npm install date-fns`
- Icons: `npm install lucide-react`
- Charts: `npm install recharts`

**Demo Data:**
- Sample product images: Use placeholder services (picsum.photos, placeholder.com)
- Sample products: Create 20-30 sample products across categories
- Sample orders: Generate 10-15 sample orders for testing

**Estimated Time:** 4-5 weeks (20-30 hours)

---

**Document Status:** ✅ Approved for Development

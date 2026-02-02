# PRD: Student Learning Portfolio Hub

**Version:** 1.0  
**Date:** January 28, 2026  
**Author:** Product Team  
**Status:** Planning

---

## 1. Purpose & Problem

**Problem:**  
React students completing fundamentals struggle to apply multiple concepts in one cohesive project. Typical learning projects (todo apps, weather dashboards) are too simple or artificial to demonstrate real-world skills.

**Solution:**  
A portfolio management app where students document their learning journey while practicing advanced React patterns—project showcases, learning journal, skill tracking, and timeline visualization.

**Why This Matters:**  
- Students build something they'll actually use
- Demonstrates professional React architecture skills
- Consolidates 6+ concepts in one project
- Creates a genuine portfolio piece

---

## 2. Target Users

**Primary:** Intermediate React students (3-6 months experience)

**Prerequisites:**
- React fundamentals (components, JSX, props, state)
- React Router
- useState & useEffect hooks
- Tailwind CSS
- Basic JavaScript ES6+

**Goals:**
- Build portfolio-worthy capstone project
- Practice architectural decision-making
- Prepare for technical interviews

---

## 3. Success Metrics

**Technical Completion:**
- 6 navigable routes with React Router
- 15+ reusable components created
- 3 state management patterns (useState, useContext, localStorage)
- 100% data persistence (no loss on refresh)
- Fully responsive (375px - 1920px+)

**Feature Completion:**
- Complete CRUD for projects, journal, skills
- Working search/filter on all modules
- Theme system (light/dark, 4 color schemes)
- Data export/import functionality
- Timeline aggregation working

**Quality Metrics:**
- Clean, commented code
- No console errors
- Sub-200ms search/filter response
- Passes keyboard navigation test

---

## 4. Functional Requirements

### FR-1: Dashboard
- [ ] Display user welcome with name
- [ ] Show 4 stat cards: Total Projects, Total Journal Entries, Total Skills, Learning Streak
- [ ] Recent activity feed (last 5 actions)
- [ ] Quick action buttons to add items

### FR-2: Projects Module
- [ ] **Create:** Form with title, description, technologies (array), GitHub URL, live URL, thumbnail URL, status, completion date
- [ ] **Read:** Display in grid (3/2/1 cols) or list view
- [ ] **Update:** Edit existing projects
- [ ] **Delete:** Remove with confirmation
- [ ] Filter by status and technology tags
- [ ] Search by title/description
- [ ] Sort by date, title, or last updated
- [ ] Modal detail view with full info

### FR-3: Learning Journal
- [ ] **Create:** Title, date, content (5000 char max), mood (5 emojis), tags, favorite flag
- [ ] **Read:** List view (chronological) or calendar view
- [ ] **Update:** Edit entries
- [ ] **Delete:** Remove with confirmation
- [ ] Search in title, content, tags
- [ ] Filter by date range, mood, tags, favorites
- [ ] Export single entry as markdown
- [ ] Export all entries as markdown ZIP

### FR-4: Skills Tracker
- [ ] **Create:** Name, category (5 options), proficiency (0-100), hours practiced, notes
- [ ] **Read:** Display grouped by category
- [ ] **Update:** Edit proficiency and hours
- [ ] **Delete:** Remove with confirmation
- [ ] Visual progress bars with color coding (Beginner: 0-33%, Intermediate: 34-66%, Advanced: 67-100%)
- [ ] Skills dashboard: total skills, total hours, average proficiency, distribution chart
- [ ] Filter by category, sort by proficiency/name/hours

### FR-5: Timeline View
- [ ] Aggregate activities from projects, journal, skills
- [ ] Display in reverse chronological order
- [ ] Vertical timeline with icons and date markers
- [ ] Filter by activity type and date range
- [ ] Click item to view details
- [ ] Responsive layout (vertical desktop, simplified mobile)

### FR-6: Settings
- [ ] Profile: Display name, tagline, profile picture URL
- [ ] Theme: Mode (light/dark/auto), color scheme (blue/purple/green/rose)
- [ ] Data Management: Export all data (JSON), import data (JSON), clear all data
- [ ] Display preferences: Default views, items per page

### FR-7: Navigation
- [ ] Responsive navbar with logo, links, theme toggle
- [ ] Desktop: Horizontal nav bar
- [ ] Mobile: Hamburger menu with slide-out drawer
- [ ] Active route highlighting
- [ ] Keyboard accessible

### FR-8: Data Persistence
- [ ] All data stored in localStorage
- [ ] Auto-save on create/update/delete
- [ ] Data validation on load
- [ ] Handle corrupted data gracefully

---

## 5. Non-Functional Requirements

### NFR-1: Performance
- Initial page load: < 2 seconds
- Route transitions: < 300ms
- Form submissions: Feedback within 100ms
- Search/filter: Updates within 200ms
- Bundle size: < 500KB gzipped

### NFR-2: Usability
- All primary actions within 3 clicks from dashboard
- Clear, specific error messages
- Loading states for all async operations
- Empty states with call-to-action
- Form validation with inline errors

### NFR-3: Accessibility
- WCAG 2.1 Level AA compliance
- Color contrast ≥ 4.5:1 for normal text
- All interactive elements keyboard accessible
- Proper heading hierarchy (h1 → h2 → h3)
- ARIA labels where needed

### NFR-4: Compatibility
- Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- Desktop screens (1920x1080+)
- Tablets (768x1024)
- Mobile (375x667 minimum)
- Portrait and landscape orientations

### NFR-5: Reliability
- Application works offline (no network required)
- Data persists across browser sessions
- Handles localStorage quota errors gracefully
- No data loss on browser crashes

### NFR-6: Maintainability
- Component-based architecture
- Consistent naming conventions (PascalCase components, camelCase utilities)
- Well-commented complex logic
- Reusable components with props
- No magic numbers/strings (use constants)

### NFR-7: Scalability
- Handle up to 500 projects without performance degradation
- Handle up to 1000 journal entries
- Handle up to 200 skills
- localStorage usage < 5MB for typical usage

---

## 6. Technical Specification

### Tech Stack
- **Framework:** React 18+ (Functional components, hooks)
- **Routing:** React Router 6+
- **Styling:** Tailwind CSS 3+
- **Build Tool:** Vite or Create React App
- **Data Storage:** localStorage
- **Icons:** Heroicons or Lucide React

### Architecture

```
src/
├── components/
│   ├── common/       # Buttons, Cards, Modals, SearchBar
│   ├── projects/     # ProjectCard, ProjectForm, ProjectList
│   ├── journal/      # JournalEntry, JournalForm, JournalList
│   ├── skills/       # SkillCard, SkillForm, ProgressBar
│   ├── timeline/     # TimelineItem
│   └── layout/       # Navbar, Layout
├── pages/            # Dashboard, Projects, Journal, Skills, Timeline, Settings
├── context/          # ThemeContext, (optional) DataContext
├── hooks/            # useLocalStorage, useTheme
├── utils/            # dateHelpers, validation
└── constants/        # Config, enums
```

### Routes
```
/              → Redirect to /dashboard
/dashboard     → Dashboard
/projects      → Projects
/journal       → Journal
/skills        → Skills
/timeline      → Timeline
/settings      → Settings
```

### State Management
- **useState:** Local component state, form inputs
- **useContext:** Theme settings, global preferences
- **localStorage:** All persistent data
- **Optional useReducer:** Complex state (projects/skills modules)

### Data Models

**Project:**
```javascript
{
  id: string,              // UUID
  title: string,           // Max 100 chars
  description: string,     // Max 1000 chars
  technologies: string[],  // Min 1 item
  githubUrl?: string,
  liveUrl?: string,
  thumbnailUrl?: string,
  status: "In Progress" | "Completed" | "Archived",
  completionDate: string,  // YYYY-MM-DD
  createdAt: string,       // ISO timestamp
  updatedAt: string        // ISO timestamp
}
```

**JournalEntry:**
```javascript
{
  id: string,
  title: string,           // Max 150 chars
  date: string,            // YYYY-MM-DD
  content: string,         // Max 5000 chars
  mood: "Happy" | "Neutral" | "Sad" | "Frustrated" | "Excited",
  tags: string[],
  isFavorite: boolean,
  createdAt: string,
  updatedAt: string
}
```

**Skill:**
```javascript
{
  id: string,
  name: string,            // Max 50 chars
  category: "Frontend" | "Backend" | "Tools" | "Soft Skills" | "Other",
  proficiency: number,     // 0-100
  hoursPracticed: number,  // Default 0
  notes?: string,          // Max 500 chars
  createdAt: string,
  updatedAt: string
}
```

---

## 7. User Flows

### Add Project Flow
1. User clicks "Add Project" from dashboard or projects page
2. Form modal opens with required fields
3. User fills: title, description, technologies, status, date
4. User optionally adds: GitHub URL, live URL, thumbnail
5. User clicks "Save"
6. System validates form
7. System saves to localStorage
8. Modal closes, redirects to projects page
9. New project visible in grid/list
10. Success notification appears

### Search Projects Flow
1. User types in search bar on projects page
2. System filters in real-time (debounced 200ms)
3. Results update as user types
4. User clears search → all projects show again

### View Timeline Flow
1. User navigates to timeline page
2. System aggregates all activities from projects, journal, skills
3. System sorts by date (newest first)
4. Timeline displays with icons and dates
5. User clicks filter dropdown
6. User selects "Projects Only"
7. Timeline updates to show only project activities

---

## 8. Design Guidelines

### Color Scheme
**Light Mode:**
- Background: Gray-50
- Card: White
- Primary: Blue-500
- Text: Gray-900

**Dark Mode:**
- Background: Gray-900
- Card: Gray-800
- Primary: Blue-400
- Text: Gray-50

**Proficiency Colors:**
- Beginner (0-33%): Red/Orange
- Intermediate (34-66%): Yellow/Amber
- Advanced (67-100%): Green

### Typography
- Font: Inter, system-ui, sans-serif
- H1: 2.25rem (page titles)
- H2: 1.875rem (section titles)
- H3: 1.5rem (card titles)
- Body: 1rem
- Small: 0.875rem

### Spacing
- Base unit: 4px (0.25rem)
- Card padding: 24px
- Section margin: 32px

### Components
- **Buttons:** Rounded-lg, py-3 px-6
- **Cards:** Rounded-xl, shadow-md, hover:shadow-lg
- **Inputs:** Rounded-lg, border, focus:ring
- **Modals:** Max-width 600px, centered, overlay backdrop

---

## 9. Development Plan

### Phase 1: Core Setup (Week 1)
- Initialize React + Tailwind
- Set up React Router
- Create layout components (Navbar, Layout)
- Implement ThemeContext
- Build useLocalStorage hook

**Deliverable:** Working navigation, theme switching, empty pages

### Phase 2: Projects Module (Week 1-2)
- ProjectForm component
- ProjectCard component
- ProjectList with grid/list toggle
- Search and filter functionality
- localStorage CRUD operations

**Deliverable:** Complete projects module

### Phase 3: Journal Module (Week 2)
- JournalForm component
- JournalEntry component
- JournalList with search/filter
- Markdown export

**Deliverable:** Complete journal module

### Phase 4: Skills Module (Week 3)
- SkillForm component
- ProgressBar component
- Skills dashboard
- Category grouping

**Deliverable:** Complete skills module

### Phase 5: Timeline & Dashboard (Week 3)
- Timeline aggregation logic
- TimelineItem component
- Dashboard statistics
- Activity feed

**Deliverable:** Complete timeline and dashboard

### Phase 6: Settings & Polish (Week 4)
- Settings page
- Data export/import
- Error handling
- Loading states
- Empty states
- Final bug fixes

**Deliverable:** Complete, polished application

---

## 10. Testing Requirements

### Functional Testing
- [ ] All CRUD operations work for each module
- [ ] Search returns correct results
- [ ] Filters apply correctly
- [ ] Sort orders data properly
- [ ] localStorage persists across refreshes
- [ ] Theme switches apply immediately
- [ ] Form validation catches errors
- [ ] Modal open/close works
- [ ] Navigation links work

### Responsive Testing
- [ ] Mobile (375px): Single column, hamburger menu
- [ ] Tablet (768px): 2 columns, collapsible nav
- [ ] Desktop (1024px+): 3 columns, full nav

### Data Integrity
- [ ] No data loss on refresh
- [ ] Unique IDs generated
- [ ] Timestamps update correctly
- [ ] Statistics calculate accurately

### Accessibility
- [ ] Keyboard navigation works
- [ ] Focus indicators visible
- [ ] Color contrast passes WCAG AA
- [ ] Screen reader compatible

---

## 11. Out of Scope

**NOT included in MVP:**
- Backend/database integration
- Real user authentication
- Multi-user functionality
- Real-time collaboration
- Third-party API integrations
- Cloud file storage
- Email notifications
- Social sharing features

---

## 12. Risks & Mitigations

| Risk | Impact | Mitigation |
|------|--------|------------|
| localStorage quota exceeded | High | Monitor usage, show warnings at 80%, provide data cleanup |
| Complex state management | Medium | Start with useState, add Context/Reducer as needed |
| Scope creep | Medium | Strict adherence to MVP features, defer stretch goals |
| Performance with large datasets | Low | Implement pagination if >20 items, debounce search |
| Browser compatibility | Low | Use standard APIs, test on major browsers |

---

## 13. Stretch Goals (Optional)

For advanced students who finish early:
- [ ] Drag-and-drop project reordering
- [ ] Rich text editor for journal (markdown support)
- [ ] Export portfolio as PDF
- [ ] Animations with Framer Motion
- [ ] Goal tracker module
- [ ] Pomodoro timer
- [ ] Charts with Recharts

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
- ✅ Application deployed (optional)

---

## 15. Resources

**Documentation:**
- React: https://react.dev
- React Router: https://reactrouter.com
- Tailwind CSS: https://tailwindcss.com

**Libraries:**
- UUID: `npm install uuid`
- Date formatting: `npm install date-fns`
- Icons: Heroicons or Lucide React

**Estimated Time:** 3-4 weeks (15-20 hours)

---

**Document Status:** ✅ Approved for Development

# Brightly — Employee Management System
### Documentation

## 1. Overview

Brightly is a self-contained, single-page Employee Management System with a dark-themed dashboard UI. It lets you add, edit, search, filter, and remove employee records, view summary analytics, charts, and browse staff grouped by department. All data is saved automatically and persists across sessions.

**File:** `roster.html` — open it directly, no installation or server required.

## 2. Data Model

Each employee record contains:

| Field | Description |
|---|---|
| `code` | Auto-generated unique ID, format `#EP0001` |
| `name` | Full name |
| `email` | Work email address |
| `phone` | Contact number |
| `gender` | Male / Female / Other |
| `department` | Engineering, Design, Sales, Marketing, Human Resources, Finance, Operations, Support |
| `title` | Job title (Role) |
| `status` | Full-time / Freelance / Part-time / On Leave / Inactive |
| `joined` | Date joined |
| `salary` | Annual salary (numeric, displayed in ₹) |

## 3. Features

### Dashboard
- **Stat cards:** Total Employee, New Employee (this month), Man Employee, Woman Employee (%)
- **Trend indicators:** month-over-month percentage change on each card
- **Work Performance:** interactive line/area chart (Last Month / Last Quarter)
- **Attendance Overview:** semi-circular gauge with On Time, Delay Time, and On Leave breakdown
- **All Employee table:** searchable preview with See All link

### Employee
- Full searchable, filterable table (search by name, email, or role; filter by department and status)
- **+ Add New** — create a record with auto-generated employee code
- **Edit / Delete** — from table or detail drawer
- Click any row to open a full detail view

### Projects (Departments)
- Auto-generated cards for every department in use, showing headcount and team preview

### Other Navigation
Schedule, Report, Notes, Job, and Hiring are placeholder sections for future modules.

## 4. How To

**Add an employee**
1. Click **+ Add New** (header or Employee page)
2. Fill in name, email, gender, department, title, status, join date, and salary
3. Click **Save Employee**

**Edit an employee**
1. Click a row to open their detail drawer, or click **Edit** from the table
2. Update fields and click **Save Employee**

**Delete an employee**
1. Click **Delete** from the table row or detail view
2. Confirm the prompt

**Search & filter**
- Use sidebar search (`Ctrl+K` / `⌘K`) to jump to Employee view with query applied
- Use dashboard or Employee page search boxes and dropdown filters

## 5. Data Storage & Privacy

- Data is stored in `localStorage` (or Cursor's built-in storage when available)
- Nothing is sent to an external server; all logic runs in the page
- The app ships with sample employees on first use; edit or delete them freely
- Existing records from older versions are migrated automatically (status and code format updated)

## 6. Design

- **Theme:** Dark mode inspired by the Brightly HR dashboard concept
- **Layout:** Fixed sidebar + top header + scrollable content area
- **Typography:** Inter (Google Fonts)
- **Charts:** Pure SVG, no external chart libraries
- **Status colors:** Green = Full-time, Cyan = Freelance, Orange = Part-time, Blue = On Leave, Red = Inactive

## 7. Possible Extensions

- CSV export/import
- Schedule and calendar module
- Hiring pipeline with candidate stages
- Report generation and PDF export
- Role-based access control

## 8. Support

This is a static, client-side app. For new fields, styling changes, or features, extend `roster.html` directly.

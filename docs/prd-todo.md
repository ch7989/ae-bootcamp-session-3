# Product Requirements Document (PRD) - Todo App Enhancements: Due Dates, Priorities, and Filters

## 1. Overview

We are upgrading the basic TODO app to support due dates, priorities, and filters so users can better organize tasks.

---

## 2. MVP Scope

- Add an optional `dueDate` field in ISO format (`YYYY-MM-DD`). Invalid dates are ignored (treated as absent).
- Add a `priority` field with three enum values: `"P1"` (high), `"P2"` (medium), `"P3"` (low), defaulting to `"P3"`.
- Implement three filter tabs/views: **All** (shows all tasks including completed), **Today** (shows incomplete tasks due today), **Overdue** (shows incomplete tasks past their due date).
- Define data model validation: `title` (required string), `priority` (required enum `"P1"`, `"P2"`, `"P3"`, defaults to `"P3"`), `dueDate` (optional ISO `YYYY-MM-DD` string; invalid values treated as absent).
- Maintain local storage (no backend or external storage changes).

---

## 3. Post-MVP Scope

- Visually highlight overdue tasks in red.
- Display priority levels as color-coded badges: P1 (red), P2 (orange), P3 (gray).
- Implement sorting logic: overdue tasks first, then by priority (P1 → P2 → P3), then by due date (ascending), tasks without due date last.
- Adjust filter behavior: hide completed tasks in "Today" and "Overdue" views (only incomplete tasks shown); "All" view includes completed tasks.

---

## 4. Out of Scope

- Notifications
- Recurring tasks
- Multi-user features
- Keyboard navigation or special accessibility features
- External storage (staying local-only)
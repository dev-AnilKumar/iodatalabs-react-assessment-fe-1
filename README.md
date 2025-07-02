# React Developer Assessment - Report Management System

Welcome to your React take-home assessment! You'll be working with a **Report Management System** that demonstrates real-world React patterns for handling data tables, filtering, and API integration.

## 🎯 Your Mission

Enhance this existing application (check [`CANDIDATE_INSTRUCTIONS.md`](CANDIDATE_INSTRUCTIONS.md)) by implementing advanced features that demonstrate your React development skills. You'll work with modern tools and patterns used in professional React applications.

## 🏗️ Current Application

You're starting with a functional app that includes:

- **🔍 Filter Form**: Search and filter reports by status, department, priority, and date range
- **📊 Data Table**: Sortable, paginated table built with TanStack Table  
- **🎨 Modern UI**: Responsive design with Tailwind CSS
- **⚡ Mock API**: Realistic data fetching with pagination and filtering

## 🛠️ Tech Stack

- **React 19** - Latest React with modern hooks
- **TanStack Table** - Powerful data table library
- **Tailwind CSS** - Utility-first CSS framework
- **Vite** - Fast build tool and dev server

## Project Structure

```
src/
├── components/
│   ├── DataTable.jsx       # Main data table component using TanStack Table
│   └── FiltersForm.jsx     # Filter form component
├── hooks/
│   └── useReportsData.js   # Custom hook for managing reports data
├── services/
│   └── reportsAPI.js       # API service for fetching reports
├── lib/
│   └── utils.js            # Utility functions
├── App.jsx                 # Main app component
├── App.css                 # Minimal custom styles
└── index.css               # Tailwind CSS imports
```

## Getting Started

1. **Install dependencies**:
   ```bash
   npm install
   ```

2. **Start development server**:
   ```bash
   npm run dev
   ```

3. **Open your browser** to `http://localhost:5173`

## Usage

1. **Filter Reports**: Use the filters form at the top to search and filter reports by:
   - Search term (searches title and content)
   - Status (draft, pending, approved, published, archived)
   - Department (Sales, Marketing, Finance, HR, Operations, IT)
   - Priority (low, medium, high)
   - Date range (from/to dates)

2. **View Results**: The data table below shows filtered results with:
   - Sortable columns (click column headers)
   - Pagination controls
   - Status and priority badges
   - Responsive design

3. **Sort Data**: Click on any column header to sort ascending/descending

4. **Navigate Pages**: Use pagination controls at the bottom of the table

## 🔧 API Architecture

The application uses a mock API service (`src/services/reportsAPI.js`) that simulates a real reporting backend:

- **Pagination Support**: Server-side pagination with page size controls
- **Sorting & Filtering**: Server-side data processing simulation
- **Report Generation**: Async report creation with status tracking
- **Data Export**: Multiple format support (CSV, JSON, PDF simulation)
- **Realistic Delays**: Network simulation for large datasets

```javascript
// Example API Response Format
{
  success: true,
  data: {
    reports: [/* array of report objects */],
    totalCount: 1250,
    pageSize: 50,
    currentPage: 1,
    totalPages: 25
  },
  message: "Reports retrieved successfully"
}
```

## 📝 Submission Guidelines

### Code Quality Expectations:

- **Clean, readable code** with meaningful variable names
- **Proper component structure** and separation of concerns
- **Consistent code formatting** (use the existing style)
- **Error handling** where appropriate
- **Comments** for complex logic
- **Responsive design** maintenance

### React Best Practices:

- Use functional components and hooks appropriately
- Proper state management with useState/useEffect
- Efficient re-rendering (avoid unnecessary renders)
- Component composition and reusability
- Proper event handling and form management

## 🎯 Evaluation Criteria

Your submission will be evaluated on:

1. **Functionality (40%)** - Do the implemented features work correctly?
2. **Code Quality (30%)** - Is the code clean, readable, and well-structured?
3. **React Knowledge (20%)** - Proper use of React patterns and best practices
4. **Problem Solving (10%)** - Creative solutions and handling edge cases

## 🤔 Need Help?

If you have questions about requirements or run into technical issues:

- Review the existing code to understand the current patterns
- Check the browser console for any errors
- Feel free to add comments explaining your approach

Good luck! We're excited to see your implementation. 🚀

---

*This assessment is designed to take 3-6 hours. Focus on code quality over quantity of features.*

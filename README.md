 README (README.md)
Document the setup and usage instructions.

Copy
# Portfolio Dashboard

A dynamic portfolio dashboard built with Next.js, TypeScript, Tailwind CSS, and Node.js, fetching real-time stock data from Yahoo Finance and Google Finance (mock data).

## Features
- Displays portfolio data in a table with real-time updates every 15 seconds.
- Groups stocks by sector with summaries (Total Investment, Present Value, Gain/Loss).
- Visualizes portfolio distribution with a pie chart using `recharts`.
- Handles errors gracefully with an `ErrorBoundary` component.
- Optimized with caching (`node-cache`) and memoization (`useMemo`).
- Responsive design with Tailwind CSS.

## Setup
1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd portfolio-dashboard
Install dependencies:
Copy
npm install
Run the development server:

Run:

npm run dev
Open http://localhost:3000 in your browser.


Dependencies:
react@18.3.1, react-dom@18.3.1 (downgraded for compatibility with react-table@7.8.0)
axios, react-table@7.8.0, recharts, yahoo-finance2, node-cache
Note: Downgraded React due to peer dependency conflict with react-table@7.8.0. Alternatively, @tanstack/react-table supports React 19.
Notes
Uses yahoo-finance2 for Current Market Price (CMP) from Yahoo Finance.
Uses mock data for Google Finance (P/E Ratio, Latest Earnings) due to lack of a public API.
Caching implemented with node-cache to handle API rate limits.
Real-time updates achieved with setInterval (15 seconds).

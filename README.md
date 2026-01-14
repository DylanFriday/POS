<h1>POS Web App (Sales Dashboard &amp; Journal)</h1>

<p>
  A front-end–only Point of Sale (POS) web application built with <strong>React</strong> and <strong>Vite</strong>.
  The app allows users to record sales transactions and visualize revenue data through an interactive dashboard.
</p>

<p>
  This project uses <strong>LocalStorage</strong> only (no backend) and is designed for deployment on
  <strong>GitHub Pages</strong>.
</p>

<hr />

<h2>✨ Features</h2>

<h3>Dashboard</h3>
<ul>
  <li>View <strong>Total Sales (All Time)</strong></li>
  <li>
    View <strong>Sales Summary for a Selected Period</strong>
    <ul>
      <li>Daily</li>
      <li>Weekly</li>
      <li>Monthly</li>
    </ul>
  </li>
  <li><strong>Line Chart</strong> — visualize sales trends</li>
  <li><strong>Pie Chart</strong> — visualize revenue proportion by category</li>
  <li><strong>Top 5 Best-Selling Items</strong> (selected period)</li>
  <li><strong>Sales by Product</strong> table (quantity + revenue)</li>
</ul>

<h3>Sales Journal</h3>
<ul>
  <li>Record new sales transactions</li>
  <li>Select product, quantity, and date</li>
  <li>Automatically calculate total price</li>
  <li>Display transaction history table (latest first)</li>
</ul>

<hr />

<h2>🧰 Tech Stack</h2>

<ul>
  <li><strong>React</strong> — UI framework</li>
  <li><strong>Vite</strong> — build tool</li>
  <li><strong>Tailwind CSS</strong> — styling</li>
  <li><strong>Recharts</strong> — charts &amp; data visualization</li>
  <li><strong>React Router</strong> — SPA routing</li>
  <li><strong>Lucide React</strong> — icons</li>
  <li><strong>LocalStorage</strong> — client-side persistence</li>
  <li><strong>GitHub Pages</strong> — hosting</li>
</ul>

<hr />

<h2>📁 Project Structure</h2>

<pre><code>src/
├── app/
│   ├── App.jsx
│   └── routes.jsx
├── pages/
│   ├── Dashboard.jsx
│   └── SalesJournal.jsx
├── components/
│   ├── Navbar.jsx
│   ├── StatCard.jsx
│   ├── PeriodSelector.jsx
│   ├── TransactionsTable.jsx
│   └── charts/
│       ├── SalesLineChart.jsx
│       └── CategoryPieChart.jsx
├── data/
│   └── pos_item.json
├── utils/
│   ├── storage.js
│   ├── date.js
│   └── aggregates.js
├── index.css
└── main.jsx
</code></pre>

<hr />

<h2>💾 Data Handling</h2>

<ul>
  <li>Product data is loaded from <code>src/data/pos_item.json</code></li>
  <li>Transactions are stored in <strong>LocalStorage</strong> (no backend)</li>
  <li>All calculations (totals, top items, category split, trend data) are computed on the client side</li>
</ul>

<hr />

<h2>🌐 Routing &amp; Deployment Notes</h2>

<ul>
  <li>Configured for <strong>GitHub Pages</strong> SPA routing</li>
  <li>Uses a SPA redirect strategy (<code>public/404.html</code>) to support client-side navigation</li>
  <li>Vite base path is configured for: <code>/POS/</code></li>
</ul>

<hr />

<h2>🚀 Getting Started (Local Development)</h2>

<h3>Install dependencies</h3>
<pre><code>npm install</code></pre>

<h3>Start dev server</h3>
<pre><code>npm run dev</code></pre>

<h3>Build for production</h3>
<pre><code>npm run build</code></pre>

<hr />

<h2>🌿 Git Flow (Branching Strategy)</h2>

<p>This project follows a Git Flow–style workflow to keep development clean and stable.</p>

<h3>Branches</h3>
<ul>
  <li>
    <strong>main</strong>
    <ul>
      <li>Stable, production-ready code</li>
      <li>Used for deployment (GitHub Pages)</li>
    </ul>
  </li>
  <li>
    <strong>develop</strong>
    <ul>
      <li>Active development branch</li>
      <li>Feature branches merge into this first</li>
    </ul>
  </li>
  <li>
    <strong>feature/*</strong>
    <ul>
      <li>Short-lived branches for new work</li>
      <li>Examples: <code>feature/dashboard-ui</code>, <code>feature/sales-journal-form</code></li>
    </ul>
  </li>
</ul>

<h3>Typical Workflow</h3>

<pre><code># Start feature
git checkout develop
git checkout -b feature/my-feature

# Work + commit
git add .
git commit -m "Implement my feature"

# Merge back to develop
git checkout develop
git merge feature/my-feature

# Release to production
git checkout main
git merge develop
</code></pre>

<hr />

<h2>🎨 UI Design Notes</h2>
<ul>
  <li>Glassmorphism + futuristic visual style</li>
  <li>Smooth hover and transition effects</li>
  <li>Readable typography and clear spacing for better UX</li>
</ul>

<hr />

<h2>⚠️ Limitations</h2>
<ul>
  <li>No authentication</li>
  <li>No backend / database</li>
  <li>Data is browser-specific (LocalStorage)</li>
  <li>Designed for learning and demonstration</li>
</ul>

<hr />

<h2>👤 Author</h2>
<p>Built as a learning and portfolio project focused on front-end architecture, state handling, and data visualization.</p>

<hr />

<h2>📄 License</h2>
<p>Educational use.</p>

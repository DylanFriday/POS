<h1>Sales Dashboard & Sales Journal</h1>
<p>
  A small React web app for recording sales and viewing simple analytics.
  Everything runs in the browser (no backend) and persists using Local Storage.
</p>

<p>
  <b>Built with:</b> React (Vite), Tailwind CSS v4, Recharts, React Router
</p>

<hr/>

<h2>What this app does</h2>
<ul>
  <li><b>Sales Journal</b>: record sales by choosing a product, quantity, and date</li>
  <li><b>Dashboard</b>: view totals and charts (daily / weekly / monthly)</li>
</ul>

<hr/>

<h2>Features</h2>

<h3>Sales Journal</h3>
<ul>
  <li>Loads products from a JSON seed file</li>
  <li>Records a transaction with <b>product + quantity + date</b></li>
  <li>Auto-calculates <b>total price</b></li>
  <li>Validates inputs (product required, quantity ≥ 1, date required)</li>
  <li>Shows a table of all transactions</li>
</ul>

<h3>Dashboard</h3>
<ul>
  <li><b>Total Sales (All Time)</b></li>
  <li><b>Selected Period Summary</b> (Daily / Weekly / Monthly)</li>
  <li><b>Sales by Product</b> for the selected period</li>
  <li><b>Top 5 Selling Items</b> for the selected period (ranked by quantity, revenue tie-break)</li>
  <li><b>Line Chart</b>
    <ul>
      <li>Daily/Weekly: shows daily trend with <code>MM-DD</code> labels</li>
      <li>Monthly: shows last 12 months with <code>Jan, Feb, ...</code> labels</li>
      <li>Auto-hides x-axis labels when there are too many points</li>
      <li>Tooltip shows currency like <code>฿1,200</code></li>
    </ul>
  </li>
  <li><b>Pie Chart</b>
    <ul>
      <li>Revenue proportion by category</li>
      <li>Tooltip shows currency like <code>฿1,200</code></li>
    </ul>
  </li>
</ul>

<hr/>

<h2>Data & storage</h2>

<h3>Product seed</h3>
<p>
  Products are loaded from:
  <code>src/data/pos_item.json</code>
</p>

<h3>Local Storage keys</h3>
<ul>
  <li><code>products_v1</code> — cached product list</li>
  <li><code>transactions_v1</code> — array of recorded transactions</li>
</ul>

<h3>Transaction shape</h3>
<p>Each transaction is stored with “snapshot” fields so analytics remain stable:</p>

<pre><code>{
  id: string,
  date: "YYYY-MM-DD",
  itemName: string,
  category: string,
  unitPrice: number,
  quantity: number,
  totalPrice: number,
  createdAt: string
}</code></pre>

<hr/>

<h2>How period filtering works</h2>
<ul>
  <li><b>Daily</b>: only the selected date</li>
  <li><b>Weekly</b>: Monday → Sunday (week containing the selected date)</li>
  <li><b>Monthly</b>: the selected month</li>
</ul>

<hr/>

<h2>Running the project</h2>

<h3>Install</h3>
<pre><code>npm install</code></pre>

<h3>Start dev server</h3>
<pre><code>npm run dev</code></pre>

<p>
  Open the URL printed in your terminal (usually
  <code>http://localhost:5173</code>).
</p>

<hr/>

<h2>Where things are in the code</h2>

<ul>
  <li>
    <b>Pages</b>:
    <code>src/pages/Dashboard.jsx</code>,
    <code>src/pages/SalesJournal.jsx</code>
  </li>
  <li>
    <b>Charts</b>:
    <code>src/components/charts/SalesLineChart.jsx</code>,
    <code>src/components/charts/CategoryPieChart.jsx</code>
  </li>
  <li>
    <b>Business logic (aggregations / summaries)</b>:
    <code>src/utils/aggregates.js</code>
  </li>
  <li>
    <b>Date + period helpers</b>:
    <code>src/utils/date.js</code>
  </li>
  <li>
    <b>Local Storage helpers</b>:
    <code>src/utils/storage.js</code>
  </li>
</ul>

<hr/>

<h2>Notes</h2>
<ul>
  <li>No backend is used — the entire app runs locally in the browser.</li>
  <li>This project is intended for educational / assignment use.</li>
</ul>

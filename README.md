# FIMS (Farm Information Management System) — Goat Farm & Investment Platform

A comprehensive, multi-role web application and agribusiness investment platform engineered from `FIMS_Goat_Farm_With_Construction.xlsx` with Role-Based Access Control (RBAC), self-investment workflows, livestock marketplace purchasing, and infrastructure capex management.

![FIMS Overview](https://images.unsplash.com/photo-1524024973431-2ad916746881?auto=format&fit=crop&w=1200&q=80)

---

## 👥 Role-Based Access Control (RBAC) & Personas

Switch between any account seamlessly using the **Persona Switcher** in the top navigation bar:

1. **👑 Admin Role (`Master Farm Administrator`):**
   - **User & Investor Management (`/admin/users`):** Full CRUD for all platform users, assigning approved investment caps and crediting liquid wallet balances.
   - **Infrastructure Capex Hub (`/construction`):** Log sheds, fencing, solar power, and utilities expenses with budget allocation progress bars.
   - **Full Herd Registry (`/goats`):** Oversee all breeding stock, lineage tracking, vaccinations, and market sales.
   - **Control & Governance Center (`/admin`):** System health diagnostics, bulk flock vaccinations, dividend payout simulators, and JSON/Excel backups.

2. **💼 Investor / Partner Role (`Partner 1` through `Partner 4`):**
   - **Personal Portfolio (`/dashboard`):** Real-time summary of Contributed Capital, Cash Wallet Balance, Value of Owned Livestock, and Proportional Share of Farm Profits.
   - **Self-Investment Portal (`/invest`):** Deposit funds directly up to admin-assigned capital caps.
   - **Livestock Marketplace (`/marketplace`):** Browse verified catalog of goats, check health/lineage, and buy goats directly using cash wallet funds.
   - **My Livestock Stable:** View personal goats with weight, tags, and growth history.

---

## 🌟 Core Financial Engine & Calculation Rules

- **Total Capital:** $\sum \text{Invested Capital} = \$20,000$ (across founding partners & user deposits).
- **Available User Cash Wallet:** $\text{Assigned/Deposited Capital} - \text{Purchased Goats}$.
- **Farm Cash Balance:**
  $$\text{Cash Balance} = \text{Total Capital} + \text{Total Sales Revenue} - (\text{Construction Capex} + \text{Goat Acquisition Costs})$$
- **Net Livestock Profit:**
  $$\text{Net Profit} = \sum (\text{Sale Price} - \text{Purchase Cost})$$
- **Proportional Investor Dividend Share:**
  $$\text{Investor Payout} = \text{Net Profit} \times \left( \frac{\text{User Invested Capital}}{\text{Total Farm Capital}} \right)$$

---

## 📱 Key Modules & Screen Directory

| Module | Route | Access | Key Capabilities |
|---|---|---|---|
| **Executive / Investor Dashboard** | `/dashboard` | Admin & Investor | High-level KPIs, Cash Allocation Donut Chart, Personal Portfolio |
| **User & Investor Management** | `/admin/users` | Admin | Add/Edit users, adjust capital caps, credit wallet balances |
| **Livestock Marketplace** | `/marketplace` | All Roles | Browse available goats, instant purchase workflow with wallet balance |
| **Self-Investment Portal** | `/invest` | Investor | Deposit funds up to limit, progress bar, transaction history |
| **Herd Registry & Stable** | `/goats` | All Roles | Table & Grid views, Lineage trees, Mark as Sold with profit preview |
| **Construction & Capex** | `/construction` | Admin & All | Budget allocation progress bar, category badges, supplier tracking |
| **Partner Capital & Equity** | `/capital` | All Roles | Equity donut chart, partner contribution ledger, deployment summary |
| **Control & Administration** | `/admin` | Admin | Health diagnostics, bulk vaccination, dividend modeling, backups |

---

## 🛠️ Tech Stack

- **Framework:** React 19 + Vite + TypeScript
- **Styling:** Tailwind CSS (Forest Greens, Slate Grays, Clean Whites)
- **Icons:** Lucide React
- **Data Visualization:** Recharts
- **Spreadsheet Engine:** SheetJS (`xlsx`)
- **State Management & Persistence:** React Context + `localStorage` with reactive updates

---

## 🚀 Running the Application

```powershell
cd C:\Users\BAFFO\fims-goat-farm
npm install
npm run dev
```

Visit **http://localhost:5173** in your browser.
"# fimswebapp" 

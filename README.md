# 🏪 S.N.A. Traders — POS System

A complete, lightweight Point of Sale (POS) system built for **S.N.A. Traders**, a stationery wholesale shop in Colombo, Sri Lanka. Built as a single HTML file with no frameworks, no build tools, and no server required.

> **Built by Ak** 🔥

---

## 🌐 Live Demo

**[sna-pos-system.vercel.app](https://sna-pos-system.vercel.app)**

---

## ✨ Features

### 💳 Sales & Billing
- Fast POS billing screen with product grid
- Search products by name or SKU — press **Enter** to instantly add to cart
- Customer selector with quick add option during billing
- Discount field per sale
- Payment methods: Cash, Card / Bank Transfer, Credit (Pay Later)
- Change amount calculation when customer overpays
- Invoice modal with print and WhatsApp share

### 🧾 Invoices
- Full invoice history with filters by date and status
- Status tracking: Paid / Partial / Credit
- View, reprint, or share any past invoice via WhatsApp
- Invoice numbering: SNA-0001, SNA-0002...

### 📦 Products
- Add, edit, and delete products
- Fields: Name, Category, SKU/Barcode, Unit, Cost Price, Selling Price, Wholesale Price
- Stock level with color-coded badges (Green / Amber / Red)
- Import vs Local stock type tagging
- Minimum stock alert threshold

### 📥 Stock In
- Manual stock entry linked to suppliers
- Tracks quantity, cost price, supplier, and stock type
- Recent entries log

### 🛒 Purchases / GRN
- Record purchases from suppliers with GRN numbering (GRN-0001...)
- Add multiple products per purchase with quantity and cost
- Edit or delete individual items before saving
- Auto-updates product stock on save
- Tracks payment status: Paid / Partial / Pending
- Updates supplier outstanding balance automatically

### 🏭 Suppliers
- Add and manage suppliers with full contact details
- Import vs Local supplier tagging
- Tracks outstanding balance owed to each supplier
- Links to purchase history

### 👥 Customers
- Customer profiles with phone and address
- Credit limit and outstanding balance tracking
- Outstanding balance auto-updates on credit sales
- Quick-add customer directly from the billing screen

### 💸 Expenses
- Record daily business expenses
- Categories: Rent, Electricity, Water, Transport, Staff Salary, Packaging, Maintenance, Miscellaneous
- Edit and delete any expense entry
- Monthly and all-time expense totals

### 📈 Reports
- **Revenue** — Monthly sales breakdown with invoice count
- **Purchases** — Total purchase cost
- **Expenses** — Breakdown by category
- **Net Profit** — Revenue minus Purchases minus Expenses
- **Top Products** — Best sellers ranked by revenue
- **Low Stock Alert** — Products at or below minimum stock level

### 🖨️ Invoice Printing
- Optimized for **80mm thermal receipt printers**
- Proper column layout — no cut-off text
- Shop name, address, phone on every receipt
- Shows: Items, Subtotal, Discount, Total, Paid, Change / Balance Due
- Dashed dividers for clean receipt look

### 📱 WhatsApp Sharing
- One-click WhatsApp invoice share
- Auto-formats invoice as a clean text message
- Pre-fills customer phone number if saved

### 🔥 Firebase Sync (Multi-device)
- Connect to Firebase Realtime Database for live sync across all devices
- Auto-syncs every 5 minutes
- Manual sync button in top bar with live status indicator
- Works offline using localStorage — syncs when back online

### 💾 Data Backup
- Export all data as a JSON file
- Import JSON backup on any device to restore data
- One-click export from Settings

---

## 🛠️ Tech Stack

| Layer | Tech |
|-------|------|
| Frontend | Vanilla HTML, CSS, JavaScript |
| Fonts | Inter (Google Fonts) |
| Storage | localStorage (primary) + Firebase Realtime DB (sync) |
| Hosting | Vercel |
| Print | Browser `window.print()` with `@page` CSS |
| WhatsApp | `wa.me` deep link API |

No frameworks. No build tools. No backend. Just one HTML file.

---

## 🚀 Setup & Deployment

### Option 1 — Use directly in browser
1. Download `index.html`
2. Open in any browser
3. Start using immediately — data saves to browser localStorage

### Option 2 — Deploy to Vercel (Recommended)
1. Fork or clone this repo
2. Go to [vercel.com](https://vercel.com) → Import GitHub repo
3. Deploy — live in under a minute

### Option 3 — Local network (3 devices, same WiFi)
1. Host the HTML file from one device using any static server
2. Other devices open the URL in their browser

---

## 🔥 Firebase Sync Setup (Multi-device)

To sync data across multiple devices in real-time:

1. Go to [firebase.google.com](https://firebase.google.com) → Create a project
2. Build → **Realtime Database** → Create Database → **Start in test mode** → Enable
3. Copy your Database URL (e.g. `https://your-project-default-rtdb.firebaseio.com`)
4. In the POS app → ⚙️ Settings → Paste the URL → **Save Firebase URL**
5. Repeat step 4 on every device — all devices will sync automatically

---

## 📁 Data Storage

All data is stored in `localStorage` under these keys:

| Key | Data |
|-----|------|
| `sna_p` | Products |
| `sna_s` | Stock entries |
| `sna_i` | Invoices |
| `sna_c` | Customers |
| `sna_sup` | Suppliers |
| `sna_pur` | Purchases / GRN |
| `sna_exp` | Expenses |
| `sna_cfg` | Settings |
| `sna_n` | Invoice counter |
| `sna_grn` | GRN counter |
| `sna_fb_url` | Firebase URL |

---

## 📸 Screenshots

> Dashboard, New Sale, Invoice Print, Reports — all in one single HTML file.

---

## 📋 Planned Features (Phase 3)

- [ ] Profit per product (sell price vs cost price)
- [ ] Customer purchase history view
- [ ] Supplier purchase history view
- [ ] Stock adjustment entries (damage / loss)
- [ ] Export reports as CSV
- [ ] Multi-user login (Owner vs Cashier)
- [ ] Date range filter for reports

---

## 👨‍💻 Author

**Ak (Mohammed Akram)**
Self-taught solo developer & entrepreneur — Colombo, Sri Lanka

- Runs [AI Collections](https://aicollections.lk) — online electronics & accessories store
- Builds and sells software products
- Freelance web developer

> *"Built simple. Works offline. No monthly fees."*

---

## 📄 License

MIT License — free to use, modify, and distribute.

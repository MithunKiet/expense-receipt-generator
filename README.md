# Billing & Receipt Studio (Unified Suite)

A clean, unified client-side suite of invoice and receipt generator tools. All tools run completely offline in your web browser with live previews, thermal printer typography, and instant print-to-PDF support.

---

## 📁 Clean Project Structure

```text
e:\New folder/
├── index.html                   # Central Dashboard & Portal
├── fuel.html                    # Tool 1: Fuel Receipt Studio (HPCL)
├── invoice.html                 # Tool 2: Computer & Retail Invoice Maker
├── airtel.html                  # Tool 3: Airtel Postpaid Mobile Bill Builder
├── generator.js                 # Fuel receipt generation logic & rates
├── navbar.css                   # Scoped stylesheet for the unified top menu
├── README.md                    # Project documentation
├── assets/                      # Consolidated images & fonts
│   ├── cn.png                   # Invoice company branding logo
│   ├── hplogo.png               # HPCL fuel receipt logo
│   └── fonts/                   # Thermal printer font
│       ├── PressStart2P-Regular.ttf
│       └── OFL-PressStart2P.txt
└── tests/                       # Unit tests
    └── generator.test.cjs
```

---

## 🛠 Included Tools

### 1. ⛽ Fuel Receipt Studio (`fuel.html`)
* **Purpose**: Generates authentic thermal dot-matrix receipts for HPCL fuel stations.
* **Fuel Types**: Petrol (`LTR`), Diesel (`LTR`), CNG (`KG`), and Electric Vehicle (`kWh`).
* **Features**:
  - Customizable date intervals (daily receipt generation up to 366 days).
  - Configurable random fuel quantity range.
  - Built-in fallback fuel rate schedule or configurable live endpoint lookup.
  - Press Start 2P true thermal dot-matrix typography.
  - Clean thermal paper preview and print layout (`@media print` with auto-hidden controls).

### 2. 📄 Computer & Retail Invoice Maker (`invoice.html`)
* **Purpose**: Generates itemized hardware, software, and repair invoices.
* **Features**:
  - Dynamic bill date setting and one-click new invoice reset.
  - Itemized tables with serial numbers, item descriptions, rates, and totals.
  - Standard terms & conditions, bank details, and authorized signature section.
  - Bootstrap 5 responsive UI with dedicated `@media print` clean layout.

### 3. 📱 Airtel Mobile Bill Builder (`airtel.html`)
* **Purpose**: Creates pixel-perfect Airtel postpaid tax invoices.
* **Features**:
  - **Dynamic Barcode**: Auto-renders Code-128 barcode directly from Bill Number.
  - **Automatic Math**: Real-time GST calculation, total amount, late fees, and amount in words.
  - **Live Preview Stage**: Auto-scaling A4 preview fitting any screen resolution.
  - **Toggleable Addons**: Option to show/hide BHIM UPI QR Code and Page numbers.
  - **Exact Typography**: Uses embedded TondoB & TondoR fonts for authentic look.

---

## 🚀 Getting Started

No build step, Node dependencies, or web servers required.

1. Open [index.html](file:///e:/New%20folder/index.html) in any browser to access the central dashboard.
2. Navigate between **Fuel Receipt**, **Invoice Maker**, and **Airtel Bill** using the top navigation bar.
3. To print or export as PDF, click **Print** or press `Ctrl + P`. All menus and controls are automatically hidden when printing.

---

## 🧪 Testing

To validate the fuel receipt generator logic, run:
```bash
node --test tests/generator.test.cjs
```
This runs the built-in Node.js test runner covering date edge cases, fuel volume calculations, API timeouts, and character escaping.

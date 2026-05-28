<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<title>Nan u Döner — POS</title>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --maroon: #7B1C2A;
    --maroon-dark: #5A1220;
    --maroon-light: #A02535;
    --accent: #E8A020;
    --accent-dark: #C07010;
    --bg: #1A1A1A;
    --surface: #242424;
    --surface2: #2E2E2E;
    --surface3: #383838;
    --text: #F0F0F0;
    --text-dim: #A0A0A0;
    --success: #2E7D32;
    --danger: #C62828;
    --radius: 14px;
    --radius-sm: 8px;
    --shadow: 0 4px 16px rgba(0,0,0,0.4);
  }

  html, body {
    height: 100%;
    background: var(--bg);
    color: var(--text);
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    overflow: hidden;
    -webkit-tap-highlight-color: transparent;
    -webkit-touch-callout: none;
    user-select: none;
  }

  /* ─── HEADER ─── */
  #app-header {
    height: 56px;
    background: var(--maroon-dark);
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 16px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.5);
    flex-shrink: 0;
    z-index: 10;
  }
  #app-header .brand {
    font-size: 1.25rem;
    font-weight: 700;
    letter-spacing: 0.5px;
    color: var(--accent);
  }
  #app-header .brand span { color: var(--text); }
  .header-btns { display: flex; gap: 8px; }
  .hbtn {
    padding: 7px 14px;
    border: none;
    border-radius: var(--radius-sm);
    cursor: pointer;
    font-size: 0.8rem;
    font-weight: 600;
    transition: opacity 0.15s;
  }
  .hbtn:active { opacity: 0.75; }
  .hbtn-admin { background: var(--surface3); color: var(--text); }
  .hbtn-sales { background: var(--accent); color: #1a1a1a; }
  .hbtn-export { background: var(--success); color: white; }

  /* ─── LAYOUT ─── */
  #layout {
    display: flex;
    height: calc(100vh - 56px);
    overflow: hidden;
  }

  /* ─── LEFT: MENU ─── */
  #menu-panel {
    flex: 1;
    display: flex;
    flex-direction: column;
    min-width: 0;
    overflow: hidden;
  }

  /* Category tabs */
  #category-bar {
    display: flex;
    gap: 8px;
    padding: 10px 12px;
    overflow-x: auto;
    background: var(--surface);
    flex-shrink: 0;
    scrollbar-width: none;
  }
  #category-bar::-webkit-scrollbar { display: none; }
  .cat-btn {
    padding: 8px 18px;
    border: 2px solid var(--maroon);
    border-radius: 50px;
    background: transparent;
    color: var(--text-dim);
    font-size: 0.85rem;
    font-weight: 600;
    cursor: pointer;
    white-space: nowrap;
    transition: all 0.15s;
    flex-shrink: 0;
  }
  .cat-btn.active {
    background: var(--maroon);
    color: var(--text);
  }
  .cat-btn:active { transform: scale(0.96); }

  /* Search */
  #search-bar {
    padding: 8px 12px;
    background: var(--surface);
    flex-shrink: 0;
  }
  #search-input {
    width: 100%;
    padding: 10px 14px;
    background: var(--surface2);
    border: 1px solid var(--surface3);
    border-radius: var(--radius-sm);
    color: var(--text);
    font-size: 0.95rem;
    outline: none;
    -webkit-appearance: none;
  }
  #search-input::placeholder { color: var(--text-dim); }
  #search-input:focus { border-color: var(--maroon-light); }

  /* Menu grid */
  #menu-grid {
    flex: 1;
    overflow-y: auto;
    padding: 10px 12px 16px;
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(145px, 1fr));
    gap: 10px;
    align-content: start;
    -webkit-overflow-scrolling: touch;
  }
  #menu-grid::-webkit-scrollbar { width: 4px; }
  #menu-grid::-webkit-scrollbar-track { background: transparent; }
  #menu-grid::-webkit-scrollbar-thumb { background: var(--surface3); border-radius: 4px; }

  .menu-card {
    background: var(--surface);
    border-radius: var(--radius);
    overflow: hidden;
    cursor: pointer;
    transition: transform 0.12s, box-shadow 0.12s;
    box-shadow: var(--shadow);
    border: 2px solid transparent;
    -webkit-tap-highlight-color: transparent;
  }
  .menu-card:active { transform: scale(0.95); border-color: var(--maroon-light); }
  .menu-card.in-cart { border-color: var(--maroon); }

  .card-img {
    width: 100%;
    aspect-ratio: 4/3;
    object-fit: cover;
    display: block;
    background: var(--surface2);
  }
  .card-img-placeholder {
    width: 100%;
    aspect-ratio: 4/3;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 2.5rem;
    background: linear-gradient(135deg, var(--maroon-dark), var(--surface2));
  }
  .card-body {
    padding: 8px 10px 10px;
  }
  .card-name {
    font-size: 0.85rem;
    font-weight: 600;
    line-height: 1.3;
    margin-bottom: 4px;
    color: var(--text);
  }
  .card-price {
    font-size: 0.9rem;
    font-weight: 700;
    color: var(--accent);
  }
  .card-badge {
    display: inline-block;
    background: var(--maroon);
    color: white;
    font-size: 0.65rem;
    font-weight: 700;
    padding: 2px 6px;
    border-radius: 50px;
    margin-bottom: 4px;
    text-transform: uppercase;
    letter-spacing: 0.3px;
  }

  /* ─── RIGHT: CART ─── */
  #cart-panel {
    width: 340px;
    min-width: 280px;
    max-width: 380px;
    background: var(--surface);
    border-left: 1px solid var(--surface3);
    display: flex;
    flex-direction: column;
    flex-shrink: 0;
    overflow: hidden;
  }

  #cart-header {
    padding: 12px 16px;
    background: var(--maroon-dark);
    font-size: 1rem;
    font-weight: 700;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-shrink: 0;
  }
  #cart-count-badge {
    background: var(--accent);
    color: #1a1a1a;
    border-radius: 50px;
    padding: 2px 10px;
    font-size: 0.8rem;
    font-weight: 700;
  }

  #cart-items {
    flex: 1;
    overflow-y: auto;
    padding: 8px;
    -webkit-overflow-scrolling: touch;
  }
  #cart-items::-webkit-scrollbar { width: 4px; }
  #cart-items::-webkit-scrollbar-thumb { background: var(--surface3); border-radius: 4px; }

  .cart-empty {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100%;
    color: var(--text-dim);
    font-size: 0.9rem;
    gap: 8px;
  }
  .cart-empty-icon { font-size: 2.5rem; opacity: 0.4; }

  .cart-item {
    background: var(--surface2);
    border-radius: var(--radius-sm);
    padding: 8px 10px;
    margin-bottom: 6px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .ci-info { flex: 1; min-width: 0; }
  .ci-name {
    font-size: 0.85rem;
    font-weight: 600;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }
  .ci-price { font-size: 0.8rem; color: var(--accent); }
  .ci-controls {
    display: flex;
    align-items: center;
    gap: 6px;
    flex-shrink: 0;
  }
  .qty-btn {
    width: 32px;
    height: 32px;
    border: none;
    border-radius: 50%;
    cursor: pointer;
    font-size: 1.1rem;
    font-weight: 700;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: opacity 0.1s;
    -webkit-tap-highlight-color: transparent;
  }
  .qty-btn:active { opacity: 0.7; }
  .qty-minus { background: var(--surface3); color: var(--text); }
  .qty-plus { background: var(--maroon); color: white; }
  .qty-num {
    font-size: 0.95rem;
    font-weight: 700;
    min-width: 22px;
    text-align: center;
  }
  .ci-remove {
    background: none;
    border: none;
    color: var(--text-dim);
    cursor: pointer;
    font-size: 1.1rem;
    padding: 4px;
    border-radius: 4px;
    -webkit-tap-highlight-color: transparent;
  }
  .ci-remove:active { color: var(--danger); }

  /* Cart footer */
  #cart-footer {
    padding: 12px;
    border-top: 1px solid var(--surface3);
    display: flex;
    flex-direction: column;
    gap: 8px;
    flex-shrink: 0;
    background: var(--surface);
  }

  .total-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 4px 0;
  }
  .total-label { font-size: 0.85rem; color: var(--text-dim); }
  .total-value { font-size: 1.1rem; font-weight: 700; color: var(--text); }
  .total-row.grand .total-label { font-size: 1rem; font-weight: 700; color: var(--text); }
  .total-row.grand .total-value { font-size: 1.3rem; color: var(--accent); }

  .cash-row {
    display: flex;
    gap: 8px;
    align-items: center;
  }
  .cash-row label { font-size: 0.8rem; color: var(--text-dim); white-space: nowrap; }
  #cash-input {
    flex: 1;
    padding: 10px 12px;
    background: var(--surface2);
    border: 1px solid var(--surface3);
    border-radius: var(--radius-sm);
    color: var(--text);
    font-size: 1rem;
    font-weight: 600;
    outline: none;
    -webkit-appearance: none;
    text-align: right;
  }
  #cash-input:focus { border-color: var(--accent); }

  .change-row {
    background: var(--surface2);
    border-radius: var(--radius-sm);
    padding: 8px 12px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .change-label { font-size: 0.8rem; color: var(--text-dim); }
  #change-display {
    font-size: 1.1rem;
    font-weight: 700;
    color: #4CAF50;
  }
  #change-display.insufficient { color: var(--danger); }

  #checkout-btn {
    width: 100%;
    padding: 15px;
    background: var(--maroon);
    color: white;
    border: none;
    border-radius: var(--radius);
    font-size: 1.1rem;
    font-weight: 700;
    cursor: pointer;
    letter-spacing: 0.5px;
    transition: background 0.15s, transform 0.1s;
    -webkit-tap-highlight-color: transparent;
  }
  #checkout-btn:hover { background: var(--maroon-light); }
  #checkout-btn:active { transform: scale(0.98); }
  #checkout-btn:disabled { background: var(--surface3); color: var(--text-dim); cursor: not-allowed; transform: none; }

  #clear-cart-btn {
    background: none;
    border: 1px solid var(--surface3);
    color: var(--text-dim);
    border-radius: var(--radius-sm);
    padding: 8px;
    font-size: 0.8rem;
    cursor: pointer;
    -webkit-tap-highlight-color: transparent;
  }
  #clear-cart-btn:active { border-color: var(--danger); color: var(--danger); }

  /* ─── MODALS ─── */
  .modal-overlay {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.75);
    z-index: 100;
    align-items: center;
    justify-content: center;
    padding: 16px;
    -webkit-backdrop-filter: blur(4px);
    backdrop-filter: blur(4px);
  }
  .modal-overlay.open { display: flex; }

  .modal {
    background: var(--surface);
    border-radius: var(--radius);
    width: 100%;
    max-width: 480px;
    max-height: 90vh;
    display: flex;
    flex-direction: column;
    box-shadow: 0 8px 40px rgba(0,0,0,0.6);
    overflow: hidden;
  }
  .modal-header {
    padding: 16px 20px;
    background: var(--maroon-dark);
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: 1.1rem;
    font-weight: 700;
    flex-shrink: 0;
  }
  .modal-close {
    background: none;
    border: none;
    color: var(--text-dim);
    font-size: 1.4rem;
    cursor: pointer;
    padding: 4px 8px;
    border-radius: 4px;
    line-height: 1;
    -webkit-tap-highlight-color: transparent;
  }
  .modal-close:hover { color: var(--text); }
  .modal-body {
    padding: 20px;
    overflow-y: auto;
    -webkit-overflow-scrolling: touch;
    flex: 1;
  }

  /* ─── RECEIPT MODAL ─── */
  #receipt-modal .receipt {
    background: white;
    color: #1a1a1a;
    border-radius: var(--radius-sm);
    padding: 20px;
    font-family: 'Courier New', monospace;
  }
  .receipt-header { text-align: center; margin-bottom: 16px; }
  .receipt-title { font-size: 1.3rem; font-weight: 700; }
  .receipt-sub { font-size: 0.75rem; color: #555; }
  .receipt-divider { border: none; border-top: 1px dashed #aaa; margin: 10px 0; }
  .receipt-row { display: flex; justify-content: space-between; font-size: 0.85rem; padding: 2px 0; }
  .receipt-total-row { display: flex; justify-content: space-between; font-size: 1rem; font-weight: 700; padding: 4px 0; }
  .receipt-change-row { display: flex; justify-content: space-between; font-size: 0.95rem; color: #2E7D32; font-weight: 600; padding: 2px 0; }
  .receipt-footer { text-align: center; margin-top: 12px; font-size: 0.75rem; color: #777; }
  #print-receipt-btn {
    width: 100%;
    margin-top: 12px;
    padding: 12px;
    background: var(--maroon);
    color: white;
    border: none;
    border-radius: var(--radius-sm);
    font-size: 1rem;
    font-weight: 600;
    cursor: pointer;
  }
  #new-order-btn {
    width: 100%;
    margin-top: 8px;
    padding: 12px;
    background: var(--accent);
    color: #1a1a1a;
    border: none;
    border-radius: var(--radius-sm);
    font-size: 1rem;
    font-weight: 700;
    cursor: pointer;
  }

  /* ─── ADMIN MODAL ─── */
  .admin-tabs { display: flex; gap: 6px; margin-bottom: 16px; flex-wrap: wrap; }
  .admin-tab {
    padding: 7px 14px;
    border: 2px solid var(--surface3);
    border-radius: 50px;
    background: transparent;
    color: var(--text-dim);
    font-size: 0.8rem;
    font-weight: 600;
    cursor: pointer;
  }
  .admin-tab.active { border-color: var(--maroon); background: var(--maroon); color: white; }
  .admin-panel { display: none; }
  .admin-panel.active { display: block; }

  .form-group { margin-bottom: 14px; }
  .form-group label { display: block; font-size: 0.8rem; color: var(--text-dim); margin-bottom: 6px; font-weight: 600; }
  .form-group input,
  .form-group select,
  .form-group textarea {
    width: 100%;
    padding: 10px 12px;
    background: var(--surface2);
    border: 1px solid var(--surface3);
    border-radius: var(--radius-sm);
    color: var(--text);
    font-size: 0.95rem;
    outline: none;
    -webkit-appearance: none;
    font-family: inherit;
  }
  .form-group input:focus,
  .form-group select:focus { border-color: var(--maroon-light); }
  .form-group select option { background: var(--surface2); }

  .btn-primary {
    width: 100%;
    padding: 12px;
    background: var(--maroon);
    color: white;
    border: none;
    border-radius: var(--radius-sm);
    font-size: 0.95rem;
    font-weight: 700;
    cursor: pointer;
    margin-top: 4px;
  }
  .btn-primary:active { opacity: 0.85; }
  .btn-success {
    background: var(--success);
  }

  .items-list { display: flex; flex-direction: column; gap: 8px; }
  .item-row {
    background: var(--surface2);
    border-radius: var(--radius-sm);
    padding: 10px 12px;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .item-row-img {
    width: 44px;
    height: 44px;
    border-radius: 6px;
    object-fit: cover;
    background: var(--surface3);
    flex-shrink: 0;
  }
  .item-row-img-placeholder {
    width: 44px;
    height: 44px;
    border-radius: 6px;
    background: var(--surface3);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.3rem;
    flex-shrink: 0;
  }
  .item-row-info { flex: 1; min-width: 0; }
  .item-row-name { font-size: 0.85rem; font-weight: 600; }
  .item-row-meta { font-size: 0.75rem; color: var(--text-dim); }
  .item-row-actions { display: flex; gap: 6px; flex-shrink: 0; }
  .btn-edit, .btn-delete {
    padding: 6px 12px;
    border: none;
    border-radius: var(--radius-sm);
    font-size: 0.75rem;
    font-weight: 600;
    cursor: pointer;
  }
  .btn-edit { background: var(--surface3); color: var(--text); }
  .btn-delete { background: rgba(198,40,40,0.2); color: #EF9A9A; }
  .btn-edit:active, .btn-delete:active { opacity: 0.75; }

  /* Image upload */
  .img-upload-area {
    border: 2px dashed var(--surface3);
    border-radius: var(--radius-sm);
    padding: 16px;
    text-align: center;
    cursor: pointer;
    transition: border-color 0.15s;
  }
  .img-upload-area:hover { border-color: var(--maroon); }
  .img-upload-area input[type="file"] { display: none; }
  .img-preview {
    width: 80px;
    height: 80px;
    border-radius: var(--radius-sm);
    object-fit: cover;
    margin: 0 auto 8px;
    display: block;
  }
  .img-upload-hint { font-size: 0.8rem; color: var(--text-dim); }

  /* Sales modal */
  .sales-summary {
    background: var(--surface2);
    border-radius: var(--radius-sm);
    padding: 14px;
    margin-bottom: 12px;
  }
  .sales-stat { display: flex; justify-content: space-between; padding: 4px 0; font-size: 0.9rem; }
  .sales-stat .val { font-weight: 700; color: var(--accent); }
  .sale-entry {
    background: var(--surface2);
    border-radius: var(--radius-sm);
    padding: 10px 12px;
    margin-bottom: 6px;
    font-size: 0.8rem;
  }
  .sale-entry-top { display: flex; justify-content: space-between; margin-bottom: 4px; }
  .sale-time { color: var(--text-dim); }
  .sale-amount { font-weight: 700; color: var(--accent); }
  .sale-items { color: var(--text-dim); font-size: 0.75rem; }

  /* Toast */
  #toast {
    position: fixed;
    bottom: 24px;
    left: 50%;
    transform: translateX(-50%) translateY(80px);
    background: var(--maroon-dark);
    color: white;
    padding: 10px 24px;
    border-radius: 50px;
    font-size: 0.9rem;
    font-weight: 600;
    z-index: 999;
    transition: transform 0.3s ease;
    box-shadow: var(--shadow);
    white-space: nowrap;
    pointer-events: none;
  }
  #toast.show { transform: translateX(-50%) translateY(0); }

  /* Category management */
  .category-chips { display: flex; gap: 6px; flex-wrap: wrap; margin-bottom: 12px; }
  .cat-chip {
    background: var(--surface3);
    border: none;
    color: var(--text);
    padding: 6px 12px;
    border-radius: 50px;
    font-size: 0.8rem;
    cursor: pointer;
    display: flex;
    align-items: center;
    gap: 6px;
  }
  .cat-chip .del { color: var(--danger); font-size: 1rem; line-height: 1; }

  /* Responsive */
  @media (max-width: 640px) {
    #cart-panel { width: 260px; min-width: 240px; }
    #menu-grid { grid-template-columns: repeat(auto-fill, minmax(120px, 1fr)); }
  }
  @media (max-width: 480px) {
    #layout { flex-direction: column; }
    #cart-panel { width: 100%; max-width: 100%; height: 300px; border-left: none; border-top: 1px solid var(--surface3); }
    #menu-panel { flex: 1; min-height: 0; }
    #menu-grid { grid-template-columns: repeat(auto-fill, minmax(110px, 1fr)); }
  }

  /* Print styles */
  @media print {
    body > *:not(#receipt-print-frame) { display: none !important; }
  }
</style>
</head>
<body>

<!-- HEADER -->
<div id="app-header">
  <div class="brand">Nan u <span>Döner</span></div>
  <div class="header-btns">
    <button class="hbtn hbtn-sales" onclick="App.openSales()">Sales</button>
    <button class="hbtn hbtn-export" onclick="App.exportCSV()">Export</button>
    <button class="hbtn hbtn-admin" onclick="App.openAdmin()">Admin</button>
  </div>
</div>

<!-- MAIN LAYOUT -->
<div id="layout">

  <!-- LEFT: MENU -->
  <div id="menu-panel">
    <div id="category-bar">
      <button class="cat-btn active" data-cat="All" onclick="App.filterCategory('All', this)">All</button>
    </div>
    <div id="search-bar">
      <input id="search-input" type="search" placeholder="Search menu…" oninput="App.searchMenu(this.value)" autocomplete="off" autocorrect="off" autocapitalize="off">
    </div>
    <div id="menu-grid"></div>
  </div>

  <!-- RIGHT: CART -->
  <div id="cart-panel">
    <div id="cart-header">
      <span>Order</span>
      <span id="cart-count-badge">0 items</span>
    </div>
    <div id="cart-items">
      <div class="cart-empty">
        <div class="cart-empty-icon">🛒</div>
        <div>Tap items to add</div>
      </div>
    </div>
    <div id="cart-footer">
      <div class="total-row grand">
        <span class="total-label">Total</span>
        <span class="total-value" id="cart-total">0 IQD</span>
      </div>
      <div class="cash-row">
        <label for="cash-input">Cash</label>
        <input id="cash-input" type="number" min="0" placeholder="0" oninput="App.updateChange()" inputmode="numeric">
      </div>
      <div class="change-row">
        <span class="change-label">Change</span>
        <span id="change-display">— IQD</span>
      </div>
      <div style="display:flex;gap:8px;">
        <button id="clear-cart-btn" onclick="App.clearCart()">Clear</button>
        <button id="checkout-btn" onclick="App.checkout()" disabled>Checkout</button>
      </div>
    </div>
  </div>

</div>

<!-- ─── RECEIPT MODAL ─── -->
<div class="modal-overlay" id="receipt-modal">
  <div class="modal">
    <div class="modal-header">
      <span>Receipt</span>
      <button class="modal-close" onclick="App.closeModal('receipt-modal')">×</button>
    </div>
    <div class="modal-body">
      <div class="receipt" id="receipt-content"></div>
      <button id="print-receipt-btn" onclick="App.printReceipt()">Print Receipt</button>
      <button id="new-order-btn" onclick="App.newOrder()">New Order</button>
    </div>
  </div>
</div>

<!-- ─── ADMIN MODAL ─── -->
<div class="modal-overlay" id="admin-modal">
  <div class="modal" style="max-width:520px;">
    <div class="modal-header">
      <span>Admin Panel</span>
      <button class="modal-close" onclick="App.closeModal('admin-modal')">×</button>
    </div>
    <div class="modal-body">
      <div class="admin-tabs">
        <button class="admin-tab active" onclick="App.adminTab('add', this)">Add Item</button>
        <button class="admin-tab" onclick="App.adminTab('items', this)">Manage Items</button>
        <button class="admin-tab" onclick="App.adminTab('cats', this)">Categories</button>
      </div>

      <!-- Add/Edit Item Form -->
      <div class="admin-panel active" id="panel-add">
        <input type="hidden" id="edit-id">
        <div class="form-group">
          <label>Item Name *</label>
          <input type="text" id="item-name" placeholder="e.g. Meat Döner" autocomplete="off">
        </div>
        <div class="form-group">
          <label>Price (IQD) *</label>
          <input type="number" id="item-price" placeholder="0" min="0" inputmode="numeric">
        </div>
        <div class="form-group">
          <label>Category *</label>
          <select id="item-category"></select>
        </div>
        <div class="form-group">
          <label>Photo (optional)</label>
          <div class="img-upload-area" onclick="document.getElementById('item-img-file').click()">
            <input type="file" id="item-img-file" accept="image/*" onchange="App.handleImageUpload(this)">
            <img id="img-preview" class="img-preview" style="display:none;" alt="">
            <div class="img-upload-hint" id="img-hint">Tap to upload photo</div>
          </div>
        </div>
        <input type="hidden" id="item-img-data">
        <button class="btn-primary" id="save-item-btn" onclick="App.saveItem()">Add Item</button>
        <button class="btn-primary" id="cancel-edit-btn" style="display:none;margin-top:8px;background:var(--surface3);color:var(--text);" onclick="App.cancelEdit()">Cancel Edit</button>
      </div>

      <!-- Manage Items -->
      <div class="admin-panel" id="panel-items">
        <div id="admin-items-list" class="items-list"></div>
      </div>

      <!-- Categories -->
      <div class="admin-panel" id="panel-cats">
        <div class="form-group">
          <label>Add Category</label>
          <div style="display:flex;gap:8px;">
            <input type="text" id="new-cat-input" placeholder="Category name" style="flex:1;" autocomplete="off">
            <button class="btn-primary" style="width:auto;padding:10px 16px;margin-top:0;" onclick="App.addCategory()">Add</button>
          </div>
        </div>
        <div id="cat-chips-list" class="category-chips"></div>
      </div>
    </div>
  </div>
</div>

<!-- ─── SALES MODAL ─── -->
<div class="modal-overlay" id="sales-modal">
  <div class="modal" style="max-width:520px;">
    <div class="modal-header">
      <span>Daily Sales</span>
      <button class="modal-close" onclick="App.closeModal('sales-modal')">×</button>
    </div>
    <div class="modal-body">
      <div class="sales-summary" id="sales-summary"></div>
      <div id="sales-list"></div>
      <button class="btn-primary btn-success" style="margin-top:8px;" onclick="App.exportCSV()">Export as CSV</button>
      <button class="btn-primary" style="margin-top:8px;background:var(--danger);" onclick="App.clearSales()">Clear Today's Sales</button>
    </div>
  </div>
</div>

<!-- TOAST -->
<div id="toast"></div>

<script>
// ═══════════════════════════════════════════════════════════════
//  NAN U DÖNER — POS SYSTEM
//  Pure JS, no dependencies, single file
// ═══════════════════════════════════════════════════════════════

var App = (function() {
  'use strict';

  // ── State ──────────────────────────────────────────────────
  var state = {
    menu: [],
    cart: [],   // [{id, name, price, qty, category, img}]
    categories: ['Döner', 'Drinks', 'Extras'],
    activeCategory: 'All',
    searchQuery: '',
    sales: [],
    lastReceipt: null,
    editingId: null
  };

  // ── Default menu ──────────────────────────────────────────
  var DEFAULT_MENU = [
    { id: 'meat-doner',    name: 'Meat Döner',    price: 4500, category: 'Döner',  img: '', emoji: '🥙' },
    { id: 'chicken-doner', name: 'Chicken Döner', price: 3500, category: 'Döner',  img: '', emoji: '🥙' },
    { id: 'kebab-durum',   name: 'Kebab Dürüm',   price: 5000, category: 'Döner',  img: '', emoji: '🌯' },
    { id: 'double-kebab',  name: 'Double Kebab',  price: 6000, category: 'Döner',  img: '', emoji: '🌯' },
    { id: 'fries',         name: 'Fries',         price: 1500, category: 'Extras', img: '', emoji: '🍟' },
    { id: 'soft-drink',    name: 'Soft Drink',    price:  750, category: 'Drinks', img: '', emoji: '🥤' },
    { id: 'water',         name: 'Water',         price:  250, category: 'Drinks', img: '', emoji: '💧' },
    { id: 'extra-nan',     name: 'Extra Nan',     price:  350, category: 'Extras', img: '', emoji: '🫓' }
  ];

  // ── localStorage helpers ────────────────────────────────────
  function lsGet(key, fallback) {
    try {
      var raw = localStorage.getItem(key);
      if (raw === null) return fallback;
      return JSON.parse(raw);
    } catch (e) { return fallback; }
  }

  function lsSet(key, val) {
    try { localStorage.setItem(key, JSON.stringify(val)); } catch (e) {}
  }

  // ── Load persisted data ─────────────────────────────────────
  function loadData() {
    var savedMenu = lsGet('pos_menu', null);
    if (savedMenu && Array.isArray(savedMenu) && savedMenu.length > 0) {
      state.menu = savedMenu;
    } else {
      state.menu = DEFAULT_MENU.map(function(item) {
        return Object.assign({}, item);
      });
    }
    var savedCats = lsGet('pos_cats', null);
    if (savedCats && Array.isArray(savedCats) && savedCats.length > 0) {
      state.categories = savedCats;
    }
    state.sales = lsGet('pos_sales', []);
    if (!Array.isArray(state.sales)) state.sales = [];
  }

  function saveMenu() { lsSet('pos_menu', state.menu); }
  function saveCats()  { lsSet('pos_cats', state.categories); }
  function saveSales() { lsSet('pos_sales', state.sales); }

  // ── Format ───────────────────────────────────────────────────
  function fmt(n) {
    return Number(n).toLocaleString() + ' IQD';
  }

  function fmtDate(ts) {
    var d = new Date(ts);
    var pad = function(n){ return String(n).padStart(2,'0'); };
    return d.getFullYear() + '-' + pad(d.getMonth()+1) + '-' + pad(d.getDate())
      + ' ' + pad(d.getHours()) + ':' + pad(d.getMinutes()) + ':' + pad(d.getSeconds());
  }

  // ── Unique ID ─────────────────────────────────────────────
  function uid() {
    return 'item_' + Date.now() + '_' + Math.floor(Math.random() * 10000);
  }

  // ── Render category bar ───────────────────────────────────
  function renderCategoryBar() {
    var bar = document.getElementById('category-bar');
    // Rebuild
    bar.innerHTML = '';
    var allBtn = document.createElement('button');
    allBtn.className = 'cat-btn' + (state.activeCategory === 'All' ? ' active' : '');
    allBtn.setAttribute('data-cat', 'All');
    allBtn.textContent = 'All';
    allBtn.onclick = function() { filterCategory('All', allBtn); };
    bar.appendChild(allBtn);

    var cats = getCategoriesFromMenu();
    cats.forEach(function(cat) {
      var btn = document.createElement('button');
      btn.className = 'cat-btn' + (state.activeCategory === cat ? ' active' : '');
      btn.setAttribute('data-cat', cat);
      btn.textContent = cat;
      btn.onclick = (function(c, b){ return function(){ filterCategory(c, b); }; })(cat, btn);
      bar.appendChild(btn);
    });
  }

  function getCategoriesFromMenu() {
    var seen = {};
    var cats = [];
    state.menu.forEach(function(item) {
      if (item.category && !seen[item.category]) {
        seen[item.category] = true;
        cats.push(item.category);
      }
    });
    // Add any stored categories not yet in menu
    state.categories.forEach(function(cat) {
      if (!seen[cat]) { seen[cat] = true; cats.push(cat); }
    });
    return cats;
  }

  // ── Render menu grid ──────────────────────────────────────
  function renderMenu() {
    var grid = document.getElementById('menu-grid');
    var q = state.searchQuery.toLowerCase().trim();
    var filtered = state.menu.filter(function(item) {
      var catOk = state.activeCategory === 'All' || item.category === state.activeCategory;
      var searchOk = !q || item.name.toLowerCase().indexOf(q) !== -1;
      return catOk && searchOk;
    });

    grid.innerHTML = '';

    if (filtered.length === 0) {
      var empty = document.createElement('div');
      empty.style.cssText = 'grid-column:1/-1;text-align:center;padding:40px;color:var(--text-dim);font-size:0.9rem;';
      empty.textContent = q ? 'No items match "' + q + '"' : 'No items in this category';
      grid.appendChild(empty);
      return;
    }

    filtered.forEach(function(item) {
      var inCart = state.cart.some(function(c){ return c.id === item.id; });
      var card = document.createElement('div');
      card.className = 'menu-card' + (inCart ? ' in-cart' : '');
      card.setAttribute('data-id', item.id);

      var imgHtml;
      if (item.img) {
        imgHtml = '<img class="card-img" src="' + escAttr(item.img) + '" alt="' + escAttr(item.name) + '" onerror="this.style.display=\'none\';this.nextElementSibling.style.display=\'flex\';">'
          + '<div class="card-img-placeholder" style="display:none;">' + (item.emoji || '🍽️') + '</div>';
      } else {
        imgHtml = '<div class="card-img-placeholder">' + (item.emoji || '🍽️') + '</div>';
      }

      card.innerHTML = imgHtml
        + '<div class="card-body">'
        + '<div class="card-badge">' + esc(item.category) + '</div>'
        + '<div class="card-name">' + esc(item.name) + '</div>'
        + '<div class="card-price">' + fmt(item.price) + '</div>'
        + '</div>';

      card.onclick = (function(it){ return function(){ addToCart(it); }; })(item);
      grid.appendChild(card);
    });
  }

  // ── Cart ──────────────────────────────────────────────────
  function addToCart(item) {
    var existing = null;
    for (var i = 0; i < state.cart.length; i++) {
      if (state.cart[i].id === item.id) { existing = state.cart[i]; break; }
    }
    if (existing) {
      existing.qty += 1;
    } else {
      state.cart.push({ id: item.id, name: item.name, price: item.price, qty: 1, category: item.category, img: item.img || '', emoji: item.emoji || '🍽️' });
    }
    renderCart();
    // Update card border
    var card = document.querySelector('.menu-card[data-id="' + item.id + '"]');
    if (card) card.classList.add('in-cart');
    showToast(item.name + ' added');
  }

  function changeQty(id, delta) {
    for (var i = 0; i < state.cart.length; i++) {
      if (state.cart[i].id === id) {
        state.cart[i].qty += delta;
        if (state.cart[i].qty <= 0) {
          state.cart.splice(i, 1);
          var card = document.querySelector('.menu-card[data-id="' + id + '"]');
          if (card) card.classList.remove('in-cart');
        }
        break;
      }
    }
    renderCart();
  }

  function removeFromCart(id) {
    state.cart = state.cart.filter(function(c){ return c.id !== id; });
    var card = document.querySelector('.menu-card[data-id="' + id + '"]');
    if (card) card.classList.remove('in-cart');
    renderCart();
  }

  function clearCart() {
    state.cart = [];
    document.querySelectorAll('.menu-card.in-cart').forEach(function(el){ el.classList.remove('in-cart'); });
    document.getElementById('cash-input').value = '';
    renderCart();
  }

  function cartTotal() {
    return state.cart.reduce(function(sum, c){ return sum + c.price * c.qty; }, 0);
  }

  function renderCart() {
    var container = document.getElementById('cart-items');
    var total = cartTotal();
    var count = state.cart.reduce(function(s, c){ return s + c.qty; }, 0);

    document.getElementById('cart-count-badge').textContent = count + (count === 1 ? ' item' : ' items');
    document.getElementById('cart-total').textContent = fmt(total);

    if (state.cart.length === 0) {
      container.innerHTML = '<div class="cart-empty"><div class="cart-empty-icon">🛒</div><div>Tap items to add</div></div>';
      document.getElementById('checkout-btn').disabled = true;
      updateChange();
      return;
    }

    container.innerHTML = '';
    state.cart.forEach(function(item) {
      var row = document.createElement('div');
      row.className = 'cart-item';
      row.innerHTML = '<div class="ci-info">'
        + '<div class="ci-name">' + esc(item.name) + '</div>'
        + '<div class="ci-price">' + fmt(item.price * item.qty) + '</div>'
        + '</div>'
        + '<div class="ci-controls">'
        + '<button class="qty-btn qty-minus" data-id="' + item.id + '" data-delta="-1">−</button>'
        + '<span class="qty-num">' + item.qty + '</span>'
        + '<button class="qty-btn qty-plus" data-id="' + item.id + '" data-delta="1">+</button>'
        + '</div>'
        + '<button class="ci-remove" data-remove="' + item.id + '">✕</button>';
      container.appendChild(row);
    });

    // Delegate events for qty and remove buttons
    container.onclick = function(e) {
      var btn = e.target.closest('[data-delta]');
      if (btn) { changeQty(btn.getAttribute('data-id'), parseInt(btn.getAttribute('data-delta'), 10)); return; }
      var rem = e.target.closest('[data-remove]');
      if (rem) { removeFromCart(rem.getAttribute('data-remove')); return; }
    };

    document.getElementById('checkout-btn').disabled = false;
    updateChange();
  }

  function updateChange() {
    var total = cartTotal();
    var cash = parseFloat(document.getElementById('cash-input').value) || 0;
    var el = document.getElementById('change-display');
    if (cash <= 0) {
      el.textContent = '— IQD';
      el.className = '';
      return;
    }
    var change = cash - total;
    el.textContent = fmt(Math.abs(change));
    if (change < 0) {
      el.className = 'insufficient';
      el.textContent = '-' + fmt(Math.abs(change));
    } else {
      el.className = '';
    }
  }

  // ── Checkout ──────────────────────────────────────────────
  function checkout() {
    if (state.cart.length === 0) return;
    var total = cartTotal();
    var cash = parseFloat(document.getElementById('cash-input').value) || 0;

    var now = Date.now();
    var receipt = {
      id: 'sale_' + now,
      timestamp: now,
      items: state.cart.map(function(c){ return Object.assign({}, c); }),
      total: total,
      cash: cash,
      change: cash - total
    };

    // Save sale
    state.sales.push(receipt);
    saveSales();

    state.lastReceipt = receipt;
    showReceipt(receipt);
  }

  function showReceipt(r) {
    var d = new Date(r.timestamp);
    var dateStr = d.toLocaleDateString('en-US', { weekday:'long', year:'numeric', month:'long', day:'numeric' });
    var timeStr = d.toLocaleTimeString('en-US', { hour:'2-digit', minute:'2-digit' });

    var itemsHtml = r.items.map(function(item) {
      return '<div class="receipt-row"><span>' + esc(item.name) + ' x' + item.qty + '</span><span>' + fmt(item.price * item.qty) + '</span></div>';
    }).join('');

    var changeHtml = r.cash > 0 ? '<hr class="receipt-divider">'
      + '<div class="receipt-row"><span>Cash</span><span>' + fmt(r.cash) + '</span></div>'
      + '<div class="receipt-change-row"><span>Change</span><span>' + fmt(r.change >= 0 ? r.change : 0) + '</span></div>' : '';

    document.getElementById('receipt-content').innerHTML = '<div class="receipt-header">'
      + '<div class="receipt-title">Nan u Döner</div>'
      + '<div class="receipt-sub">' + dateStr + '<br>' + timeStr + '</div>'
      + '</div>'
      + '<hr class="receipt-divider">'
      + itemsHtml
      + '<hr class="receipt-divider">'
      + '<div class="receipt-total-row"><span>TOTAL</span><span>' + fmt(r.total) + '</span></div>'
      + changeHtml
      + '<div class="receipt-footer">Thank you for dining with us!<br>Nan u Döner</div>';

    openModal('receipt-modal');
  }

  function printReceipt() {
    var content = document.getElementById('receipt-content').innerHTML;
    var win = window.open('', '_blank', 'width=400,height=600');
    if (!win) { showToast('Allow popups to print'); return; }
    win.document.write('<html><head><title>Receipt</title><style>'
      + 'body{font-family:monospace;font-size:12px;padding:16px;max-width:320px;margin:auto;}'
      + '.receipt-row{display:flex;justify-content:space-between;padding:2px 0;}'
      + '.receipt-total-row{display:flex;justify-content:space-between;font-weight:bold;font-size:14px;padding:4px 0;}'
      + '.receipt-change-row{display:flex;justify-content:space-between;color:#2E7D32;font-weight:600;padding:2px 0;}'
      + '.receipt-header{text-align:center;margin-bottom:12px;}'
      + '.receipt-title{font-size:16px;font-weight:700;}'
      + '.receipt-sub{font-size:11px;color:#555;}'
      + '.receipt-footer{text-align:center;margin-top:10px;font-size:11px;color:#777;}'
      + 'hr{border:none;border-top:1px dashed #aaa;margin:8px 0;}'
      + '</style></head><body>' + content + '</body></html>');
    win.document.close();
    win.focus();
    setTimeout(function(){ win.print(); win.close(); }, 300);
  }

  function newOrder() {
    closeModal('receipt-modal');
    clearCart();
    document.getElementById('cash-input').value = '';
  }

  // ── Sales ─────────────────────────────────────────────────
  function openSales() {
    var today = new Date(); today.setHours(0,0,0,0);
    var todaySales = state.sales.filter(function(s){ return s.timestamp >= today.getTime(); });
    var totalRevenue = todaySales.reduce(function(sum, s){ return sum + s.total; }, 0);
    var totalOrders = todaySales.length;

    document.getElementById('sales-summary').innerHTML = '<div class="sales-stat"><span>Today\'s Orders</span><span class="val">' + totalOrders + '</span></div>'
      + '<div class="sales-stat"><span>Today\'s Revenue</span><span class="val">' + fmt(totalRevenue) + '</span></div>'
      + '<div class="sales-stat"><span>All-time Sales</span><span class="val">' + state.sales.length + '</span></div>';

    var list = document.getElementById('sales-list');
    var sorted = state.sales.slice().reverse();
    if (sorted.length === 0) {
      list.innerHTML = '<div style="text-align:center;padding:20px;color:var(--text-dim);">No sales yet</div>';
    } else {
      list.innerHTML = sorted.slice(0, 50).map(function(s) {
        var itemSummary = s.items.map(function(i){ return i.name + ' x' + i.qty; }).join(', ');
        return '<div class="sale-entry"><div class="sale-entry-top"><span class="sale-time">' + fmtDate(s.timestamp) + '</span><span class="sale-amount">' + fmt(s.total) + '</span></div><div class="sale-items">' + esc(itemSummary) + '</div></div>';
      }).join('');
    }
    openModal('sales-modal');
  }

  function clearSales() {
    if (!confirm('Clear all sales data? This cannot be undone.')) return;
    state.sales = [];
    saveSales();
    openSales();
    showToast('Sales cleared');
  }

  function exportCSV() {
    if (state.sales.length === 0) { showToast('No sales to export'); return; }
    var rows = [['Date', 'Time', 'Items', 'Qty', 'Unit Price', 'Line Total', 'Order Total', 'Cash', 'Change']];
    state.sales.forEach(function(s) {
      s.items.forEach(function(item, idx) {
        rows.push([
          new Date(s.timestamp).toLocaleDateString(),
          new Date(s.timestamp).toLocaleTimeString(),
          '"' + item.name.replace(/"/g, '""') + '"',
          item.qty,
          item.price,
          item.price * item.qty,
          idx === 0 ? s.total : '',
          idx === 0 ? (s.cash || '') : '',
          idx === 0 ? (s.change != null ? s.change : '') : ''
        ]);
      });
    });
    var csv = rows.map(function(r){ return r.join(','); }).join('\n');
    var blob = new Blob([csv], { type: 'text/csv' });
    var url = URL.createObjectURL(blob);
    var a = document.createElement('a');
    a.href = url;
    a.download = 'nan-u-doner-sales-' + new Date().toISOString().slice(0,10) + '.csv';
    document.body.appendChild(a);
    a.click();
    document.body.removeChild(a);
    URL.revokeObjectURL(url);
    showToast('CSV exported');
  }

  // ── Admin ─────────────────────────────────────────────────
  function openAdmin() {
    adminTab('add', document.querySelector('.admin-tab.active') || document.querySelector('.admin-tab'));
    renderAdminItems();
    renderCatChips();
    populateCategorySelect();
    openModal('admin-modal');
  }

  function adminTab(name, btn) {
    document.querySelectorAll('.admin-tab').forEach(function(t){ t.classList.remove('active'); });
    document.querySelectorAll('.admin-panel').forEach(function(p){ p.classList.remove('active'); });
    if (btn) btn.classList.add('active');
    var panel = document.getElementById('panel-' + name);
    if (panel) panel.classList.add('active');
    if (name === 'items') renderAdminItems();
    if (name === 'cats') renderCatChips();
    if (name === 'add') populateCategorySelect();
  }

  function populateCategorySelect() {
    var sel = document.getElementById('item-category');
    var cats = getCategoriesFromMenu();
    sel.innerHTML = cats.map(function(c){ return '<option value="' + escAttr(c) + '">' + esc(c) + '</option>'; }).join('');
  }

  function handleImageUpload(input) {
    var file = input.files[0];
    if (!file) return;
    var reader = new FileReader();
    reader.onload = function(e) {
      var data = e.target.result;
      document.getElementById('item-img-data').value = data;
      var preview = document.getElementById('img-preview');
      preview.src = data;
      preview.style.display = 'block';
      document.getElementById('img-hint').textContent = 'Tap to change photo';
    };
    reader.readAsDataURL(file);
  }

  function saveItem() {
    var name = document.getElementById('item-name').value.trim();
    var price = parseInt(document.getElementById('item-price').value, 10);
    var category = document.getElementById('item-category').value;
    var imgData = document.getElementById('item-img-data').value;
    var editId = document.getElementById('edit-id').value;

    if (!name) { showToast('Please enter item name'); return; }
    if (!price || price <= 0) { showToast('Please enter a valid price'); return; }
    if (!category) { showToast('Please select a category'); return; }

    if (editId) {
      // Edit existing
      for (var i = 0; i < state.menu.length; i++) {
        if (state.menu[i].id === editId) {
          state.menu[i].name = name;
          state.menu[i].price = price;
          state.menu[i].category = category;
          if (imgData) state.menu[i].img = imgData;
          break;
        }
      }
      showToast(name + ' updated');
    } else {
      // New item
      var emoji = getCategoryEmoji(category);
      state.menu.push({ id: uid(), name: name, price: price, category: category, img: imgData, emoji: emoji });
      showToast(name + ' added');
    }

    saveMenu();
    renderMenu();
    renderCategoryBar();
    renderAdminItems();
    resetItemForm();
  }

  function getCategoryEmoji(cat) {
    var map = { 'Döner': '🥙', 'Drinks': '🥤', 'Extras': '🍟' };
    return map[cat] || '🍽️';
  }

  function resetItemForm() {
    document.getElementById('item-name').value = '';
    document.getElementById('item-price').value = '';
    document.getElementById('item-img-data').value = '';
    document.getElementById('edit-id').value = '';
    var preview = document.getElementById('img-preview');
    preview.src = '';
    preview.style.display = 'none';
    document.getElementById('img-hint').textContent = 'Tap to upload photo';
    document.getElementById('save-item-btn').textContent = 'Add Item';
    document.getElementById('cancel-edit-btn').style.display = 'none';
    state.editingId = null;
    document.getElementById('item-img-file').value = '';
  }

  function cancelEdit() {
    resetItemForm();
  }

  function editItem(id) {
    var item = state.menu.find(function(m){ return m.id === id; });
    if (!item) return;
    populateCategorySelect();
    document.getElementById('edit-id').value = item.id;
    document.getElementById('item-name').value = item.name;
    document.getElementById('item-price').value = item.price;
    document.getElementById('item-category').value = item.category;
    if (item.img) {
      document.getElementById('item-img-data').value = item.img;
      var preview = document.getElementById('img-preview');
      preview.src = item.img;
      preview.style.display = 'block';
      document.getElementById('img-hint').textContent = 'Tap to change photo';
    }
    document.getElementById('save-item-btn').textContent = 'Update Item';
    document.getElementById('cancel-edit-btn').style.display = 'block';
    adminTab('add', document.querySelectorAll('.admin-tab')[0]);
  }

  function deleteItem(id) {
    var item = state.menu.find(function(m){ return m.id === id; });
    if (!item) return;
    if (!confirm('Delete "' + item.name + '"?')) return;
    state.menu = state.menu.filter(function(m){ return m.id !== id; });
    state.cart = state.cart.filter(function(c){ return c.id !== id; });
    saveMenu();
    renderMenu();
    renderCategoryBar();
    renderCart();
    renderAdminItems();
    showToast(item.name + ' deleted');
  }

  function renderAdminItems() {
    var list = document.getElementById('admin-items-list');
    if (!list) return;
    if (state.menu.length === 0) {
      list.innerHTML = '<div style="text-align:center;padding:20px;color:var(--text-dim);">No items yet</div>';
      return;
    }
    list.innerHTML = '';
    state.menu.forEach(function(item) {
      var row = document.createElement('div');
      row.className = 'item-row';
      var imgHtml = item.img
        ? '<img class="item-row-img" src="' + escAttr(item.img) + '" alt="" onerror="this.style.display=\'none\';this.nextElementSibling.style.display=\'flex\';">'
          + '<div class="item-row-img-placeholder" style="display:none;">' + (item.emoji || '🍽️') + '</div>'
        : '<div class="item-row-img-placeholder">' + (item.emoji || '🍽️') + '</div>';

      row.innerHTML = imgHtml
        + '<div class="item-row-info">'
        + '<div class="item-row-name">' + esc(item.name) + '</div>'
        + '<div class="item-row-meta">' + esc(item.category) + ' · ' + fmt(item.price) + '</div>'
        + '</div>'
        + '<div class="item-row-actions">'
        + '<button class="btn-edit" data-edit="' + item.id + '">Edit</button>'
        + '<button class="btn-delete" data-del="' + item.id + '">Delete</button>'
        + '</div>';
      list.appendChild(row);
    });

    list.onclick = function(e) {
      var editBtn = e.target.closest('[data-edit]');
      if (editBtn) { editItem(editBtn.getAttribute('data-edit')); return; }
      var delBtn = e.target.closest('[data-del]');
      if (delBtn) { deleteItem(delBtn.getAttribute('data-del')); return; }
    };
  }

  // ── Categories ────────────────────────────────────────────
  function addCategory() {
    var input = document.getElementById('new-cat-input');
    var name = input.value.trim();
    if (!name) { showToast('Enter a category name'); return; }
    if (state.categories.indexOf(name) !== -1) { showToast('Category already exists'); return; }
    state.categories.push(name);
    saveCats();
    input.value = '';
    renderCatChips();
    populateCategorySelect();
    renderCategoryBar();
    showToast(name + ' category added');
  }

  function deleteCategory(name) {
    var inUse = state.menu.some(function(m){ return m.category === name; });
    if (inUse) { showToast('Cannot delete — category has items'); return; }
    state.categories = state.categories.filter(function(c){ return c !== name; });
    saveCats();
    renderCatChips();
    populateCategorySelect();
    renderCategoryBar();
    showToast(name + ' removed');
  }

  function renderCatChips() {
    var container = document.getElementById('cat-chips-list');
    if (!container) return;
    var cats = getCategoriesFromMenu();
    container.innerHTML = cats.map(function(cat) {
      return '<div class="cat-chip">' + esc(cat) + '<span class="del" data-delcat="' + escAttr(cat) + '">×</span></div>';
    }).join('');
    container.onclick = function(e) {
      var del = e.target.closest('[data-delcat]');
      if (del) deleteCategory(del.getAttribute('data-delcat'));
    };
  }

  // ── Filter/Search ─────────────────────────────────────────
  function filterCategory(cat, btn) {
    state.activeCategory = cat;
    document.querySelectorAll('.cat-btn').forEach(function(b){ b.classList.remove('active'); });
    if (btn) btn.classList.add('active');
    renderMenu();
  }

  function searchMenu(q) {
    state.searchQuery = q;
    renderMenu();
  }

  // ── Modals ────────────────────────────────────────────────
  function openModal(id) {
    var el = document.getElementById(id);
    if (el) el.classList.add('open');
  }

  function closeModal(id) {
    var el = document.getElementById(id);
    if (el) el.classList.remove('open');
  }

  // Close modal on overlay click
  document.addEventListener('click', function(e) {
    if (e.target.classList.contains('modal-overlay')) {
      e.target.classList.remove('open');
    }
  });

  // Close on Escape
  document.addEventListener('keydown', function(e) {
    if (e.key === 'Escape') {
      document.querySelectorAll('.modal-overlay.open').forEach(function(m){ m.classList.remove('open'); });
    }
  });

  // ── Toast ─────────────────────────────────────────────────
  var toastTimer = null;
  function showToast(msg) {
    var el = document.getElementById('toast');
    el.textContent = msg;
    el.classList.add('show');
    if (toastTimer) clearTimeout(toastTimer);
    toastTimer = setTimeout(function(){ el.classList.remove('show'); }, 2000);
  }

  // ── Escape helpers ────────────────────────────────────────
  function esc(str) {
    return String(str || '').replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;').replace(/"/g,'&quot;').replace(/'/g,'&#39;');
  }
  function escAttr(str) { return esc(str); }

  // ── Init ──────────────────────────────────────────────────
  function init() {
    loadData();
    renderCategoryBar();
    renderMenu();
    renderCart();
    // Prevent zoom on double-tap for iOS
    var lastTap = 0;
    document.addEventListener('touchend', function(e) {
      var now = Date.now();
      if (now - lastTap < 300) e.preventDefault();
      lastTap = now;
    }, { passive: false });
  }

  // Run on DOM ready
  if (document.readyState === 'loading') {
    document.addEventListener('DOMContentLoaded', init);
  } else {
    init();
  }

  // ── Public API ────────────────────────────────────────────
  return {
    filterCategory: filterCategory,
    searchMenu: searchMenu,
    addToCart: addToCart,
    changeQty: changeQty,
    removeFromCart: removeFromCart,
    clearCart: clearCart,
    updateChange: updateChange,
    checkout: checkout,
    printReceipt: printReceipt,
    newOrder: newOrder,
    openSales: openSales,
    clearSales: clearSales,
    exportCSV: exportCSV,
    openAdmin: openAdmin,
    adminTab: adminTab,
    handleImageUpload: handleImageUpload,
    saveItem: saveItem,
    cancelEdit: cancelEdit,
    addCategory: addCategory,
    openModal: openModal,
    closeModal: closeModal
  };
})();
</script>
</body>
</html>

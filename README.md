<h1 align="center">🍽️ Restoran 2000 Tiga — POS & QR Self-Ordering Ecosystem</h1>

<p align="center">
  <b>An End-to-End F&B Operational Web Application Case Study: Connecting Guest QR Portal to Cashier Engine</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Web_Desktop_%7C_Mobile-blue" alt="Platform" />
  <img src="https://img.shields.io/badge/Type-F%26B_Management_Ecosystem-orange" alt="Type" />
  <img src="https://img.shields.io/badge/Status-Case_Study_%2F_Concept-success" alt="Status" />
</p>

---

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [System Walkthrough](#-system-walkthrough)
  - [Part 1: Cashier Engine (Desktop)](#part-1-cashier-engine-desktop)
  - [Part 2: Guest Self-Ordering (Mobile)](#part-2-guest-self-ordering-mobile)
  - [Part 3: The Real-Time Handshake](#part-3-the-real-time-handshake)
- [Architectural Impact](#-architectural-impact)

---

## 💡 Project Overview

A full-cycle F&B operational utility designed to eliminate dine-in ordering friction for a 30-table restaurant. It bridges the gap between **Customer Self-Ordering via Smartphone** and **Staff Checkout Efficiency** in real-time.

### The Operational Handshake
* **For Guests:** Scan QR $\rightarrow$ Order & Customize $\rightarrow$ Choose Payment (Zero app download required).
* **For Staff:** Get Push Alert $\rightarrow$ Click Accept $\rightarrow$ Auto-fill POS running bill (Zero manual re-typing required).

---

## 🖥️ System Walkthrough

### PART 1: CASHIER ENGINE & BACK-OFFICE (Desktop View)
*Directory: `/kasir-pos` | Designed for speed: zero typing required for standard orders.*

#### 1. Gate Control & Floor Overview
| Shift Login | 30-Table Overview (Vacant) | POS Main Catalog View |
| :---: | :---: | :---: |
| ![Login](kasir-pos/login.png) | ![Denah](kasir-pos/denah%20meja.png) | ![Menu Catalog](kasir-pos/menu.png) |

#### 2. Core POS & Menu Management
| Active Table Cart | Add New Menu Modal | Order Settlement Modal |
| :---: | :---: | :---: |
| ![Pesanan](kasir-pos/pesanan%20meja.png) | ![Tambah Menu](kasir-pos/tambah%20menu.png) | ![Bayar](kasir-pos/bayar%20pop%20up.png) |

#### 3. Payment, Petty Cash & Auditing
| Payment Success Prompt | Petty Cash Logger | Transaction Logs |
| :---: | :---: | :---: |
| ![Berhasil](kasir-pos/pembayaran%20berhasil.png) | ![Pengeluaran](kasir-pos/pengeluaran.png) | ![Riwayat](kasir-pos/riwayat%20transaksi.png) |

#### 4. Authorization & Security (Void System)
| Master Password Request | Void Success Confirmation | Notification Center |
| :---: | :---: | :---: |
| ![Void Auth](kasir-pos/void%20bill.png) | ![Void Acc](kasir-pos/void%20berhasil.png) | ![Notif](kasir-pos/notifikasi%20pesanan%20di%20terima.png) |

#### 5. Executive Analytics & Hardware Settings
| Daily Cash Settlement | Sales Dashboard & Chart | USB Printer Detection |
| :---: | :---: | :---: |
| ![Laporan](kasir-pos/laporan%20harian.png) | ![Dashboard](kasir-pos/dashboard.png) | ![Fitur](kasir-pos/dashboard%20fitur.png) |

---

### PART 2: GUEST SELF-ORDERING PORTAL (Mobile View)
*Directory: `/mobile-qr` | Optimized for thumb-reach navigation and zero-friction adoption.*

| Mobile Catalog | Modifier & Notes | Table & Identity Form | Order Hand-off | Dispatched Validation |
| :---: | :---: | :---: | :---: | :---: |
| ![Catalog](mobile-qr/menu.png) | ![Cart](mobile-qr/order.png) | ![Form](mobile-qr/form%20order.png) | ![Confirm](mobile-qr/acc%20order.png) | ![Sent](mobile-qr/order%20terkirim.png) |

---

### PART 3: THE REAL-TIME HANDSHAKE (Loop Closure)
*Demonstrating the live data synchronization from Guest's phone directly to Cashier's desktop.*

1. **The Instant Capture:** The guest hits 'Place Order' on their phone. Instantly, a live floating card triggers on the cashier's dashboard. Staff clicks **`Terima & Masukkan Meja`**.  
   <img src="kasir-pos/qr pesanan di terima.png" width="700" alt="Capture Order" />

2. **The Server Handshake:** The system returns a success validation to the cashier.  
   <img src="kasir-pos/qr sudah di terima.png" width="700" alt="Server Handshake" />

3. **The Live Floor Update:** The designated table automatically shifts to **Red** on the floor map, instantly generating an accurate active running bill.  
   <img src="kasir-pos/detail%20qr%20diterima.png" width="700" alt="Floor Update" />

4. **The Zero-Typing Checkout:** When the guest walks up to the counter to settle the bill, their order summary is already fully populated. Staff proceeds directly to payment.  
   <img src="kasir-pos/detail%20qr%20diterima%202.png" width="700" alt="Auto Fill POS" />

---

## 🎯 Architectural Impact

* **100% Bill Integrity:** Mitigated revenue leakage caused by untracked extra orders requested by guests mid-meal.
* **Sub-15 Minute Staff Onboarding:** Linear UI layout allows newly hired cashiers to fully master the checkout workflow with virtually zero training.
* **2-Step Flow:** Reduced standard dine-in ordering bureaucracy from a 5-step analog process to a seamless 2-step digital handshake.

# 🚖 Taxi & Ride-Booking Operational & Revenue Analysis

An end-to-end data analytics and Business Intelligence project exploring **150,000+ ride booking transactions (2024)**. This project investigates key operational metrics, booking status distributions, cancellation root causes, revenue generation across vehicle types, and customer satisfaction ratings using Power BI and a clean, interactive modern Web Dashboard UI.

---

## 🌟 Interactive Web Dashboard (`index.html`)

An interactive, responsive operational dashboard is built directly into the repository for live browser exploration:
- **Real-Time KPIs**: Total Bookings (150K), Success Completion Rate (62%), Gross Revenue (₹51.85M), Turnaround Times (VTAT 8.46m / CTAT 29.15m), and Dual 5-Star Ratings.
- **Dynamic Charting**: Monthly demand trends, booking status pie charts, revenue by vehicle type, payment mode breakdowns, and driver/customer cancellation root-cause charts.
- **Interactive Vehicle Fleet Matrix**: Full breakdown of 7 service tiers (Auto, Go Mini, Go Sedan, Bike, Premier Sedan, eBike, Uber XL).
- **Zero Server Setup**: Open `index.html` directly in any web browser or host on GitHub Pages.

---

## 📌 Project Overview

Urban ride-hailing services experience fluctuating demands, cancellation challenges, and varying driver/customer satisfaction levels. The purpose of this project is to model, visualize, and analyze operational ride-booking performance to uncover actionable insights for fleet utilization, revenue optimization, and cancellation mitigation.

### Key Objectives:
- **Booking Volume & Trend Analysis**: Understand temporal patterns in booking volumes and vehicle type demand.
- **Cancellation & Failure Analysis**: Evaluate driver and customer cancellation factors alongside "No Driver Found" occurrences.
- **Revenue & Payment Breakdown**: Identify top revenue-generating vehicle categories and customer payment channel preferences (UPI, Cash, Wallets, Cards).
- **Service Quality & Turnaround Time**: Measure Average Vehicle Turnaround Time (VTAT), Customer Turnaround Time (CTAT), and ratings across services.

---

## 📊 Dataset Summary

- **Total Records**: 150,000 ride bookings
- **Date Range**: January 1, 2024 – December 30, 2024
- **Total Booking Value Analyzed**: ₹51.8M+
- **Average Trip Distance**: ~24.64 km
- **Source File**: `Riding Analysis/rideBookings.csv` (~25.5 MB)

### Data Dictionary

| Column Name | Description |
|:---|:---|
| `Date` & `Time` | Timestamp when the ride was booked |
| `Booking ID` | Unique identifier for each booking |
| `Booking Status` | `Completed`, `Cancelled by Driver`, `No Driver Found`, `Cancelled by Customer`, `Incomplete` |
| `Customer ID` | Unique identifier for the customer |
| `Vehicle Type` | Service category (`Auto`, `Go Mini`, `Go Sedan`, `Bike`, `Premier Sedan`, `eBike`, `Uber XL`) |
| `Pickup Location` & `Drop Location` | Locations for pickup and drop-off |
| `Avg VTAT` | Average Vehicle Turnaround Time (minutes) |
| `Avg CTAT` | Average Customer Turnaround Time (minutes) |
| `Cancelled Rides by Customer` | Indicator / details on customer-initiated cancellations |
| `Reason for cancelling by Customer` | Reasons including change of plans, high wait times, wrong address, etc. |
| `Cancelled Rides by Driver` | Indicator / details on driver-initiated cancellations |
| `Driver Cancellation Reason` | Reasons including customer far away, customer sickness, personal issues, etc. |
| `Incomplete Rides` & `Reason` | Trips interrupted prematurely (e.g., vehicle breakdown) |
| `Booking Value` | Total monetary value of the ride (INR) |
| `Ride Distance` | Distance traveled (km) |
| `Driver Ratings` & `Customer Rating` | Dual-sided rating feedback (1 to 5 stars) |
| `Payment Method` | Transaction mode (`UPI`, `Cash`, `Uber Wallet`, `Credit Card`, `Debit Card`) |

---

## 📈 Power BI Dashboard (`yt.pbix`)

The included **Power BI Report (`Riding Analysis/yt.pbix`)** features multi-page analytical views:

1. **Homepage**: Clean entry screen (background image display scaled to `Fit` to prevent cropping errors).
2. **Overall View**: Executive KPIs, monthly trip trajectories, and completion distribution.
3. **Vehicle Type**: Deep-dive comparisons across all 7 vehicle tiers for volume, revenue, and trip distances.
4. **Revenue & Payments**: Payment mode distribution (UPI, Cash, Wallets, Cards) and daily revenue trajectories.
5. **Cancellation Analysis**: Driver reasons, customer triggers, and incomplete ride breakdowns.
6. **Ratings & Turnaround (VTAT / CTAT)**: Cross-functional satisfaction correlations with operational latency.
7. **Executive Summary**: High-level scorecards for quick decision making.

---

## 📁 Repository Structure

```plaintext
Taxi-analysis/
├── .gitignore                      # Ignored files and patterns
├── README.md                       # Comprehensive project documentation
├── index.html                      # Interactive web dashboard UI (Tailwind + Chart.js)
├── dashboard_data.json             # Pre-aggregated operational metrics for the web UI
└── Riding Analysis/
    ├── rideBookings.csv            # 150K records transactional dataset (~25.5 MB)
    └── yt.pbix                     # Power BI interactive reporting file (~11.1 MB)
```

---

## 🚀 Getting Started

### 1. View Interactive Web Dashboard
Simply open `index.html` in your favorite web browser (Chrome, Edge, Firefox, Safari):
```bash
# Windows
start index.html

# Mac / Linux
open index.html
```

### 2. View Power BI Dashboard
- Open `Riding Analysis/yt.pbix` in [Power BI Desktop](https://powerbi.microsoft.com/desktop/).
- Click Refresh to load data from `Riding Analysis/rideBookings.csv` if modifying queries.

---

## 💡 Key Insights & Business Recommendations

1. **Digital Payments Dominance**:
   - UPI accounts for the highest transaction share, followed by Cash. Promotional discounts or cashback incentives tied to digital payments can further minimize cash handling.
2. **Addressing Cancellation Bottlenecks**:
   - Significant ride failure occurs under "Cancelled by Driver" (18%) and "No Driver Found" (7%). Improving driver dispatch algorithms and driver acceptance incentives in peak zones can drastically reduce unfulfilled demand.
3. **Turnaround Optimization**:
   - Lower VTAT and CTAT correlate strongly with higher customer ratings (4.5+). Improving ETA prediction accuracy and pickup hotspot mapping can improve retention.

---

## 👤 Author

- **Sanket Yeul** - [GitHub Profile](https://github.com/yeulsanket)

---

## 📄 License

This repository is distributed under the [MIT License](https://opensource.org/licenses/MIT).


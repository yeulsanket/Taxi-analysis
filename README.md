# 🚖 Taxi & Ride-Booking Operational & Revenue Analysis

An end-to-end data analysis and Business Intelligence project exploring **150,000+ ride booking transactions (2024)**. This project investigates key operational metrics, booking status distributions, cancellation root causes, revenue generation across vehicle types, and customer satisfaction ratings using Power BI and data analytics techniques.

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

The included **Power BI Report (`Riding Analysis/yt.pbix`)** features interactive dashboards designed for operational and executive review:

1. **Executive Overview**:
   - Total Bookings, Completed Rides, Completion Rate (%), Total Revenue, and Average Distance.
   - Slicers for Time Range, Vehicle Type, and Locations.
2. **Booking & Cancellation Diagnostics**:
   - Status split: Completed vs. Driver Cancelled vs. Customer Cancelled vs. No Driver Found vs. Incomplete.
   - Root-cause breakdown charts for customer and driver cancellation reasons.
3. **Revenue & Payment Dynamics**:
   - Revenue contributions by vehicle tier (`Auto`, `Go Mini`, `Go Sedan`, `Premier Sedan`, `Bike`, etc.).
   - Share of payment channels (dominance of UPI and Cash).
4. **Ratings & Operational Latency**:
   - Correlation between VTAT/CTAT and overall customer ratings.
   - Vehicle-level and zone-level satisfaction benchmark.

---

## 📁 Repository Structure

```plaintext
Taxi-analysis/
├── .gitignore                      # Ignored files and patterns
├── README.md                       # Comprehensive project documentation
└── Riding Analysis/
    ├── rideBookings.csv            # 150K records transactional dataset (~25.5 MB)
    └── yt.pbix                     # Power BI interactive reporting file (~11.1 MB)
```

---

## 🚀 Getting Started

### Prerequisites
- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (to view and interact with the `.pbix` dashboard)
- Optional: Python 3.8+ (with `pandas`, `numpy`, `matplotlib`, `seaborn`) or SQL for exploratory querying

### Running Locally
1. **Clone the repository**:
   ```bash
   git clone https://github.com/yeulsanket/Taxi-analysis.git
   cd Taxi-analysis
   ```

2. **Open the Power BI Dashboard**:
   - Double-click `Riding Analysis/yt.pbix` to launch the dashboard in Power BI Desktop.
   - If prompted, refresh the data source to point to `Riding Analysis/rideBookings.csv`.

3. **Data Exploration (Python snippet)**:
   ```python
   import pandas as pd

   # Load dataset
   df = pd.read_csv("Riding Analysis/rideBookings.csv")
   print(df.info())
   print(df['Booking Status'].value_counts())
   ```

---

## 💡 Key Insights & Business Recommendations

1. **Digital Payments Dominance**:
   - UPI accounts for the highest transaction share, followed by Cash. Promotional discounts or cashback incentives tied to digital payments can further minimize cash handling.
2. **Addressing Cancellation Bottlenecks**:
   - Significant ride failure occurs under "Cancelled by Driver" and "No Driver Found". Improving driver dispatch algorithms and driver acceptance incentives in peak zones can drastically reduce unfulfilled demand.
3. **Turnaround Optimization**:
   - Lower VTAT and CTAT correlate strongly with higher customer ratings (4.5+). Improving ETA prediction accuracy and pickup hotspot mapping can improve retention.

---

## 👤 Author

- **Sanket Yeul** - [GitHub Profile](https://github.com/yeulsanket)

---

## 📄 License

This repository is distributed under the [MIT License](https://opensource.org/licenses/MIT).

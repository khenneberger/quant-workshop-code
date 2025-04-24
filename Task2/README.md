 # 💼 Task 2: Natural Gas Storage Contract Valuation

This task implements a valuation model for a simplified natural gas storage contract. The objective is to calculate the **net value of a contract** involving the **injection, storage, and withdrawal** of natural gas over time, incorporating **market prices**, **injection/withdrawal costs**, and **storage fees**.

---

## 🧠 Problem Overview

Natural gas storage contracts allow a trader to inject (buy) gas into storage when prices are low and withdraw (sell) it when prices are high. This function simulates such a scenario:

- It tracks injection and withdrawal dates and volumes.
- It accounts for costs associated with purchasing, storing, and handling the gas.
- It returns the total **profit or loss** from executing the contract.

---

## 🧮 How It Works

The contract pricing logic simulates the financial flows of a natural gas storage agreement. It computes the overall contract value based on buying (injecting), storing, and selling (withdrawing) gas across specified dates.

### 1. Combine and Sort Dates
All injection and withdrawal dates are merged into a single, chronological sequence. This ensures events are processed in the correct order.

### 2. Iterate Through the Timeline
Each date is evaluated in order. Depending on the event type:

- **Injection (Buy) Date:**
  - Ensure that storage capacity is available before injecting.
  - Increase the stored volume by a fixed daily rate.
  - Add to the cost:
    - The cost to purchase gas at the market price on that date.
    - An operational fee for injection, charged per unit volume.

- **Withdrawal (Sell) Date:**
  - Ensure sufficient volume is stored before withdrawing.
  - Reduce the stored volume by the same daily rate.
  - Add to the revenue:
    - The income from selling gas at the market price on that date.
    - Subtract a withdrawal cost, also charged per unit volume.

### 3. Calculate Storage Cost
A flat monthly storage fee is applied, based on the number of months between the earliest injection and the latest withdrawal. The total storage cost depends on the contract duration and a fixed monthly rate.

### 4. Compute Net Contract Value
The final contract value is calculated as:

**Net Value = Total Revenue - Storage Cost - Purchase and Operational Costs**

This result represents the profit or loss from executing the contract as planned.

# DaVinCheese Café - Café Management System

This repository contains the **DaVinCheese Café Management System**. Built using C# for frontend and backend logic, integrated with SQL Server for database management, it handles café operations such as user sign-ups, menu management, discounts, feedback, cart operations, table reservations, and payments. This README provides a comprehensive guide to using the system and summarizes the software quality engineering analysis conducted using JIRA for manual testing.

---

## 🔧 Technologies Used

🔹 **Programming Language**: C#\
🔹 **Database**: SQL Server\
🔹 **Testing Tool**: JIRA (for test case management, execution, and bug tracking)

---

## 📖 System Usage Guide

### 🧑‍💼 Customer Functions

**Menu and Add to Cart**

- Browse the café's menu via the "Menu" option.
- View item details: name, price, calories, description.
- Add items to cart, adjust quantity, proceed to checkout.
- Submit feedback post-checkout using "Leave Feedback."

**Table Reservation**

- Select "Table Reservation."
- Choose up to two tables, pick date/time, click "Reserve."
- View reservation details afterward.

**Cart and Checkout**

- View cart via "Cart" option: update quantities or remove items.
- Click "Checkout," select payment method (credit card, EasyPaisa, JazzCash).
- Enter payment details and click "Confirm" to complete the purchase.

**View Profile**

- Select "Profile" to view personal info: name, contact, email, total orders.
- Update information if needed.

**View Past Orders**

- Select "Past Orders" to see previous orders.
- Useful for reordering favorites or tracking purchase history.

### 👩‍🍳 Staff Functions

**Add Menu Items**

- Select "Add Menu Items."
- Ensure availability in inventory, enter details (name, price, description, calories), click "Add."

**Edit Menu Items**

- Select "Edit Menu Items," choose item, update details, click "Update."

**View Table Reservations**

- Select "Table Reservations," enter customer and reservation ID to view reserved tables.

**View Product Feedbacks**

- Select "Product Feedbacks" to see customer feedback with associated items.

**View Orders**

- Select "View Orders" to see current and past orders.
- Enter number of orders to filter customers.

**View Customer Sales**

- Select "View Customer Sales."
- Enter a threshold amount to see customers with order totals exceeding that value.

### 🧑‍💼 Manager Functions

**Add Employee**

- Select "Add Employee," enter details (first/last name, email, password, contact), click "Add."

**View Employee Details**

- View employee info: contact details, roles, authority, completed sales.

**View Sales**

- Track financial performance, showing checked-out customers with invoice time and total.
- Panel shows Star (most popular) and Dog (least popular) items.

**View Product Details**

- View inventory, feedback, price, calories, description for all products.

**Add Event Discounts**

- Create event discounts: provide name, description, percentage.
- Only one event active at a time; remove current before adding new.
- Removing an event resets product prices to default.

**Add Inventory**

- View products with stock below 50.
- Enter product ID and quantity to restock.

---

## 🔍 Testing Overview

Manual testing was performed on 47 test cases covering core functionalities: user interactions, data operations, input validation, and edge cases. Focus was on identifying bugs, analyzing pass/fail ratios, and providing recommendations.

### 📊 JIRA Dashboards

**Test Execution Dashboard**

- Recent Test Cases: Lists most recently executed and completed cases.
- High-Priority Failed Test Cases: Highlights 4 critical failed test cases.
- Pass/Fail Pie Chart: 40 passed (85% pass rate), 7 failed out of 47 total.

**Bug Tracking Dashboard**

- Bug Status Pie Chart: All 7 bugs are "In Progress."
- Critical High-Priority Bugs: 3 bugs with high priority and critical severity.
- Priority Distribution Pie Chart: 4 high, 2 medium, 1 low.

---

## 📈 Analysis of Test Execution Results

### **🔹**Out of 47 test cases, 40 passed, 7 failed (\~85% pass rate).

### \
**Failed cases involved**

- Data validation issues (duplicate emails, empty feedback, zero quantity)
- Incorrect business logic (e.g., prices not reverting after discount removal)
- Edge case handling (e.g., payments with empty cart)
- Successful cases confirmed features like adding items, editing menu items, submitting feedback.

### 🧩 Complexity of Test Scenarios

Test scenarios simulated real-world usage:

🔹 **User Interactions**: Sign-up, feedback, cart operations.\
🔹 **Data Operations**: Menu edits, discount applications, data retrieval.\
🔹 **Input Validation**: Ensuring valid inputs across forms.\
🔹 **Edge Cases**: Empty cart payments, discount reversals.

### 🐞 Summary of Critical Bugs

**Online Payment with No Items in Cart**

- Impact: Allows invalid transactions, billing issues, customer dissatisfaction.
- Solution: Pre-payment check to ensure cart has items; display error if empty.

**Credit Card Payment with No Items in Cart**

- Impact: Permits empty cart transactions, causing confusion.
- Solution: Validation in credit card process to require items; prompt user.

**Original Price Not Reverted After Removing Discount**

- Impact: Price not reset, affecting revenue and accuracy.
- Solution: Store original prices before applying discounts and restore upon removal.

---

## 💡 Reflection and Lessons Learned

🔹 **Input Validation**: Strengthen form, payment, and data checks.\
🔹 **Edge Case Handling**: Focus on unlikely scenarios that disrupt features.\
🔹 **State Management**: Improve tracking of states (e.g., original prices).\
🔹 **Automation**: Automate tests for efficiency and accuracy.\
🔹 **Prioritization**: Emphasize payment and pricing testing to build trust.

Overall, the system is robust but requires enhancements in validation and state management. Future improvements should prioritize these areas and consider automated testing.

---

## 👨‍💻 Contributors
- **Abdullah Daoud (22I-2626)**  
- **Dawood Hussain (22I-2410)**  

---

## ⚖️ License
This project is for **academic and personal skill development purposes only**.  
Reuse is allowed for **learning and research** with proper credit.

---

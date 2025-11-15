# 🏬 Amazon Extended ER Modeling  

📚 **Course:** MIS-631A  
👨‍🏫 **Professor:** Dr. Morabito  
👥 **Team 3:** Snehal Dhatrak • Swarangi Patil • Cheyenne Manning • Pedro Monroy-Polanco • Rohini Mallikarjunaiah  

---

## 🔍 Project Overview  
This project models the **core business processes of Amazon’s e-commerce ecosystem** using extended entity-relationship (ER) design.  
The goal is to represent how Amazon manages **procurement, vendor compliance, orders, payments, and returns** across its global retail operations while ensuring data integrity and regulatory compliance.

---

## 🎯 Objectives  
- Capture Amazon’s business logic for suppliers, products, and customers (B2B + B2C).  
- Model purchase orders, invoices, and payments as inter-linked contracts.  
- Ensure compliance through business-rule constraints and triggers.  
- Provide scalable schemas for merchandising, technology, and fulfillment systems.

---

## 🧱 Key Business Rules  
- Only **approved suppliers** can sell products.  
- Each **product** has a unique `ProductID`.  
- **Purchase Orders** reference valid suppliers and products; no duplicate active PO per supplier/product.  
- **Invoices** must match verified purchase orders and passed QC inspections before payment.  
- **Returns** must link to an existing order, customer, and fall within 30 days.  
- **Dangerous goods** require special labeling and handling.

---

## 🧩 Functional Modules  
| Module | Description |
|---------|-------------|
| **Marketplace & Merchandising** | Product listing, search, recommendation, reviews, category management |
| **Platform & Technology** | User sessions, API requests, machine-learning recommendations, fraud detection |
| **Fulfillment & Operations** | Inventory, warehouses, shipment, returns, refund processing |
| **Contracts & Compliance** | Purchase orders, invoices, payments, vendor audits |

---

## 🧮 Contracts (Mini Scenarios)
**1. Placing a Purchase Order**  
- *Pre-condition:* Supplier approved and inventory below threshold.  
- *Post-condition:* New PO created → inventory status = “restock in progress.”  

**2. Payment of an Invoice**  
- *Invariant:* Invoice paid only after matching verified PO + QC-passed goods.  
- *Post-condition:* Payment transaction logged → invoice status = “paid.”  

**3. Return Policy**  
- *Pre-condition:* Product received by customer; within 30-day window.  
- *Post-condition:* Return order created → refund initiated → inventory updated.  

---

## 📐 ER Design Highlights  
- **High-Level ER Model** capturing Customers, Sellers, Products, Orders, Inventory, Payments, Shipments, and Reviews.  
- **Extended ER Model** adds hierarchy, specialization, and relationships among contracts and logistics.  
- Separate diagrams for:  
  - *Marketplace & Merchandising*  
  - *Platform & Technology*  
  - *Fulfillment & Operations*  

---

## 📈 Normalization & Integrity  
- Applied 1NF → 3NF to reduce redundancy.  
- Used bridging entities (e.g., OrderItem, RecommendationLog).  
- Enforced referential integrity through FK constraints and business rules.  

---

## 🧰 Tools & Techniques  
ERD Software: Lucidchart / Draw.io / Visio  
SQL Schema Design: Primary/Foreign Keys, Constraints, Relationships  
Excel: Entity Dictionary & Attribute Mapping  

---

## 📸 Diagrams

![Amazon ERD 1](amazon_erd_1.png)
![Amazon ERD 2](amazon_erd_2.png)
![Amazon ERD 3](amazon_erd_3.png)
![Amazon ERD 4](amazon_erd_4.png)
![Amazon ERD 5](amazon_erd_5.png)
![Amazon ERD 6](amazon_erd_6.png)
![Amazon ERD 7](amazon_erd_7.png)
![Amazon ERD 8](amazon_erd_8.png)

> The diagrams above represent different components of Amazon’s extended ER design — 
> from conceptual overviews to logical and physical models. 
> Each image captures relationships, cardinalities, and normalization across Marketplace, Technology, Fulfillment, and Compliance modules.


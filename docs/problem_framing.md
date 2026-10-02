# Problem Framing

**Project:** Retail Performance Review
**Stakeholder:** COO
**Author:** Dolfine Ngare
**Date:** October 2026
**Status:** Final v1

**Summary:** The COO feels the business is busier but not making more money. This analysis checks orders, revenue, big customers and cancellations to help decide what to fix first before the board meeting.

## 1. Questions in the brief
The COO's message has 4 questions:
1. Are we really getting more orders?
2. Is revenue going up too?
3. Have our big trade customers stopped buying?
4. Are cancellations a big problem?

## 2. The decision behind the request
The COO has a board meeting in 2 weeks and needs to decide what to fix first:
- Win back big customers that stopped buying. The sales team and sales manager can call or visit them to find out why they stopped.
- Fix the cancellation problem.
- Focus on the products that sell best.

To help the sales team act fast, I will give them a list of big customers who went quiet, showing how much they used to spend and when they last ordered.

## 3. Metrics
| COO's word | What I will measure | How |
|---|---|---|
| "Busier" | Orders per month | Count of unique invoice numbers |
| "Making money" | Revenue per month | Quantity × Unit Price |
| "Orders getting smaller" | Average Order Value (AOV) | Revenue ÷ Number of orders |
| "Gone quiet" | Days since last order | Last date in data − customer's last order date |
| "Out of control" | Cancellations as % of sales | Cancelled value ÷ Total sales × 100 |

## 4. What I can't answer with this data
- Profit: there is no cost data. I will use revenue and AOV instead and flag profit as a gap.
- Why customers cancel: there is no reason column. Cancelled orders can be seen (InvoiceNo starts with "C"), so I can show who cancels, which products, which countries and which months.
- Why big customers stopped buying: the data can show who stopped and when, but not why. The sales team will need to follow up.

## 5. Definitions
- Order = one unique InvoiceNo
- Cancelled order = InvoiceNo starting with "C"
- Big trade customer = top 10% of customers by total revenue. In wholesale, a small group of customers usually brings in most of the money.
- Gone quiet = no order in the last 90 days. Trade customers usually reorder within 3 months.
- Limitation: the business is seasonal (Christmas is the busiest time), so a 90-day gap is not always a problem. A better check would compare each customer to their own usual buying pattern.
- - Data note: December 2011 only has data up to 9 Dec, so it is not a full month and will not be compared with other months.

## 6. Hypotheses
1. Old customers are still buying but in smaller quantities, so orders go up but revenue does not (falling AOV).
2. There are more orders because new small customers are buying from us, but they spend less, so revenue is not growing as fast as orders.
3. Some of the order growth is just Christmas season, not real growth.
4. A few big customers bring in most of the revenue, so losing even 2-3 of them hurts a lot.
5. Most cancellations come from a few customers or products.

## 7. Scope and deliverables
In scope:
- Transactions from Dec 2010 to Dec 2011
- Orders, revenue, AOV, big customers and cancellations

Out of scope:
- Profit (no cost data)
- Marketing, website traffic and stock levels (no data)

Deliverables:
1. A 1-page Excel dashboard
2. A 1-page summary with 3 findings and 3 recommendations
3. A cleaning log showing every change made to the data

Plan: a short pre-meeting with the COO before the board meeting, to go through the findings and add anything missing.

## 8. Questions for the COO and answers
1. Do you have specific big trade customers in mind that you would like us to check?
   - COO: No formal list. Thinks some are from the Netherlands and Ireland. I will check the data to confirm.
2. Profit needs cost data. Can finance share it, or should we focus on revenue for now?
   - COO: Focus on revenue. Profit is flagged as a gap.
3. What cancellation level would worry you?
   - COO: Above 5% of sales.

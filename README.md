# Smart India Hackathon Workshop
# Date:22/11/2026
## Reference Number: 26009013
## Name: HARIHARAN T

## Problem Title
SIH 26033: Multiple intermediaries reduce farmers earnings and increase consumer prices.

## Problem Creater's Organization
Ministry of Consumer Affairs, Food & Public Distribution

## Theme
Agriculture, FoodTech & Rural Development

## Problem Description
Expected Solution: Create a digital marketplace that:

• Connects farmers/FPOs directly with consumers and bulk buyers.
• Provides logistics support.
• Uses AI for demand forecasting and route optimization.

Benefits:

• Better prices for farmers.
• Lower prices for consumers.
• Reduced supply chain inefficiencies.

## Proposed Solution

## 2.1 Solution Name

**AgriConnect -- AI-Powered Direct Farm-to-Market Platform**

AgriConnect is a digital agricultural marketplace that enables farmers
and FPOs to list produce and connect with buyers directly. It combines
product discovery, order management, transparent pricing, digital
payment support, logistics coordination and demand forecasting in one
platform.

The proposed system consists of: - A mobile application for farmers and
buyers. - A web dashboard for administrators and FPOs. - A backend API
to manage users, products, orders and transactions. - A database to
store marketplace information. - An AI/analytics module for demand
forecasting. - A logistics module to coordinate deliveries.

## 2.2 Major Modules

### A. Farmer and FPO Registration

1. Farmers register using a mobile number and complete the platform's
    verification process.
2. FPOs can create organization profiles and manage participating
    farmers.
3. User roles control which features and information each account can
    access.
4. Regional-language support is provided to improve accessibility.

### B. Product Listing and Inventory

1. Farmers add crop name, quantity, expected price, harvest date,
    location and product images.
2. Farmers can update available stock and listing status.
3. Buyers can view product details, seller information and available
    quantities.
4. The system prevents orders from exceeding the available listed
    quantity.

### C. Direct Digital Marketplace

1. Consumers, retailers and bulk buyers search for products by crop,
    location, quantity and price.
2. Buyers compare listings from different farmers and FPOs.
3. Buyers place orders through the platform.
4. Farmers accept or reject orders based on availability.
5. Bulk purchase requests can be sent to FPOs or groups of farmers.

### D. AI-Based Demand Forecasting

1. The system analyzes historical orders, crop type, seasonality and
    available market data.
2. A machine-learning model estimates demand for selected products over
    a defined future period.
3. Forecasts are displayed as decision-support information, not
    guaranteed predictions.
4. Farmers and FPOs can use the forecast to plan listings and
    inventory.
5. Model performance is evaluated using metrics such as Mean Absolute
    Error (MAE) and Root Mean Squared Error (RMSE).

### E. Logistics and Delivery Coordination

1. The platform connects orders with participating transport providers.
2. Orders from nearby locations may be grouped when product type,
    delivery schedule and handling requirements are compatible.
3. Delivery planning considers distance, vehicle capacity, delivery
    windows and product perishability.
4. Buyers receive order-status updates and delivery tracking where
    supported.
5. Transportation charges are shown separately from the produce price.

### F. Transparent Pricing

1. Product price, quantity, transport charge and platform service fee
    are displayed separately.
2. Farmers can view the estimated net amount they will receive before
    confirming an order.
3. The platform can show indicative market-price information from
    authorized or reliable sources, with the source and date clearly
    identified.
4. The system does not claim that a displayed indicative price is a
    guaranteed selling price.

### G. Digital Payments and Order Records

1. The platform integrates with an authorized payment gateway or
    supported UPI payment flow.
2. Payment status is recorded against the relevant order.
3. Digital receipts and transaction histories are available to buyers
    and sellers.
4. Refunds, cancellations and disputes follow clearly defined platform
    rules.
5. The prototype may use a payment sandbox rather than processing real
    money.

### H. Quality Information and Traceability

1. Farmers provide product and harvest details.
2. Quality grading can be recorded by trained personnel or authorized
    partners.
3. Each order receives a unique order identifier.
4. Buyers can view available seller, product, grading and delivery
    information.
5. The platform distinguishes farmer-provided information from
    independently verified information.

## 2.3 How the Solution Addresses the Problem

  -----------------------------------------------------------------------
  Existing challenge                  AgriConnect approach
  ----------------------------------- -----------------------------------
  Several trading layers              Direct digital connection between
                                      farmers/FPOs and buyers

  Limited price information           Indicative market prices and
                                      transparent transaction breakdown

  Difficulty reaching bulk buyers     FPO aggregation and bulk-order
                                      requests

  High or fragmented transport costs  Coordinated delivery and compatible
                                      order grouping

  Uncertain demand                    Historical-data-based demand
                                      forecasting

  Payment uncertainty                 Recorded digital payment status and
                                      receipts

  Limited product information         Product details, grading records
                                      and order traceability
  -----------------------------------------------------------------------

## 2.4 Innovation and Uniqueness

1.  **FPO-supported aggregation:** Small quantities from participating
    farmers can be coordinated to meet suitable bulk orders.
2.  **Demand forecasting:** Historical transaction data can be used to
    estimate demand and support inventory decisions.
3.  **Order and delivery coordination:** Compatible orders can be
    grouped to improve vehicle utilization.
4.  **Transparent farmer settlement view:** Farmers can see product
    value, deductions and estimated net earnings.
5.  **Regional-language and low-connectivity support:** The application
    is designed for practical use in rural settings.
6.  **Interoperability approach:** The platform can explore integration
    with existing agricultural market services instead of duplicating
    their functions.

------------------------------------------------------------------------


## Technical Approach

## 3.1 Proposed Technology Stack

  -----------------------------------------------------------------------
  Component               Proposed technology     Purpose
  ----------------------- ----------------------- -----------------------
  Farmer and buyer mobile Flutter                 Android/iOS application
  app                                             

  Web dashboard           React.js                Admin and FPO
                                                  management

  Backend                 Python FastAPI          APIs and business logic

  Database                PostgreSQL              Users, products, orders
                                                  and payments

  Geospatial support      PostGIS                 Location and distance
                                                  queries

  Machine learning        Python, Scikit-learn /  Demand forecasting
                          XGBoost                 

  Route optimization      Google Maps Platform    Mapping and vehicle
                          and OR-Tools            routing

  Authentication          OTP and JWT-based       User authentication
                          sessions                

  Payment                 Authorized payment      Payment processing
                          gateway / UPI           
                          integration             

  Notifications           Firebase Cloud          Order updates
                          Messaging / SMS         
                          provider                

  Hosting                 AWS / Azure /           Deployment and scaling
                          equivalent cloud        

  Version control         Git and GitHub          Source-code management
  -----------------------------------------------------------------------

The technologies listed are proposed choices. The final implementation
may use equivalent services depending on cost, availability, licensing
and institutional requirements.

## 3.2 System Architecture

The system follows a layered architecture:

**Presentation layer** - Farmer mobile application - Buyer mobile
application - FPO portal - Administrator dashboard

**Application layer** - Authentication and user management - Product and
inventory management - Search and marketplace services - Order
management - Payment integration - Logistics coordination - Notification
service - Reporting and analytics

**Data and intelligence layer** - PostgreSQL database with PostGIS -
Demand forecasting service - Route optimization service - Transaction
and audit records

**External services** - Payment gateway - Maps and geocoding service -
SMS/notification provider - Cloud object storage for product images

## 3.3 End-to-End Workflow

1.  A farmer or FPO registers and completes verification.
2.  The farmer lists produce with quantity, price, location and harvest
    information.
3.  A buyer searches and compares available listings.
4.  The buyer places an order or submits a bulk requirement.
5.  The farmer confirms availability and accepts the order.
6.  The platform records payment status through the payment provider.
7.  The logistics module coordinates pickup and delivery.
8.  The buyer receives the order and confirms delivery.
9.  The platform updates the order record and makes the settlement
    information available to the farmer.
10. The system stores transaction data for reports and future demand
    analysis.

## 3.4 AI and Optimization Components

### A. Demand Forecasting

**Inputs:** Historical order quantities, product category, date/season,
location and available market data.

**Candidate algorithms:** Random Forest Regression or XGBoost. A simple
baseline model should be evaluated before selecting a more complex
model.

**Output:** Estimated demand for a product and location over a selected
time period.

**Evaluation:** MAE and RMSE on a held-out test dataset. The model
should be compared with a simple historical-average baseline.

**Important limitation:** Forecast quality depends on the amount and
reliability of historical data. The system should display uncertainty or
confidence information where feasible and should not present forecasts
as guaranteed demand.

### B. Delivery Route Optimization

**Inputs:** Pickup locations, delivery locations, order quantities,
vehicle capacities and delivery time windows.

**Method:** Model the task as a Vehicle Routing Problem (VRP). Google
OR-Tools can be used to find practical routes subject to capacity and
scheduling constraints.

**Output:** Suggested vehicle assignments and delivery sequence.

**Evaluation:** Compare total distance, estimated travel time and
vehicle utilization against a simple nearest-first or manually planned
baseline.

### C. Market Price Information

1. Obtain price information from authorized sources where access is
    permitted.
2. Store the source, market, product, unit and observation date.
3. Normalize units before comparing prices.
4. Clearly label historical, indicative and live prices.
5. Do not treat an indicative market price as a guaranteed transaction
    price.

## 3.5 Proposed Database Design

  -----------------------------------------------------------------------
  Table                               Example fields
  ----------------------------------- -----------------------------------
  Users                               user_id, name, mobile, role,
                                      verification_status

  Farmers                             farmer_id, user_id, farm_location,
                                      profile_details

  FPOs                                fpo_id, name, registration_details,
                                      location

  FPO_Members                         fpo_id, farmer_id,
                                      membership_status

  Products                            product_id, farmer_id, crop_name,
                                      quantity, unit, price

  Orders                              order_id, buyer_id, status,
                                      total_amount, created_at

  Order_Items                         order_item_id, order_id,
                                      product_id, quantity, unit_price

  Payments                            payment_id, order_id, amount,
                                      provider_reference, status

  Deliveries                          delivery_id, order_id, provider_id,
                                      status, tracking_reference

  Price_Observations                  observation_id, product, market,
                                      price, unit, source, date

  Reviews                             review_id, user_id, order_id,
                                      rating, comments
  -----------------------------------------------------------------------

The database should use primary keys, foreign keys, constraints and
indexes. Payment and order status changes should be recorded
consistently to support reconciliation and auditing.

## 3.6 Security and Data Protection

1. Use secure authentication and role-based access control.
2. Store passwords using a strong password-hashing algorithm.
3. Use HTTPS for communication.
4. Validate and sanitize user inputs.
5. Do not store sensitive payment credentials in the application
    database.
6. Use the payment provider's secure integration and verify payment
    callbacks.
7. Restrict access to personal and location information.
8. Maintain audit logs for important actions.
9. Back up the database and test recovery procedures.
10. Follow applicable data-protection and cybersecurity requirements.

------------------------------------------------------------------------
## Feasibility and Viability
## 4.1 Technical Feasibility

The solution can be built using established mobile, web, database and
cloud technologies. A prototype can be developed in stages, beginning
with registration, product listings, search and orders. AI forecasting
and logistics optimization can be added after sufficient sample or
historical data is available.

## 4.2 Economic Feasibility

Potential operating and revenue models include: - A clearly disclosed
service fee on successfully completed transactions. - Optional logistics
coordination fees. - Institutional or FPO subscription plans for
additional management features. - Partnerships with agricultural
organizations and service providers.

The platform should keep charges transparent and evaluate whether the
model creates a net benefit for farmers and buyers. Revenue assumptions
must be validated through a pilot rather than treated as guaranteed.

## 4.3 Operational Feasibility

1. FPOs can help onboard farmers and aggregate produce.
2. Local collection points may support sorting, grading and
    consolidation.
3. Existing transport providers can provide delivery services.
4. A support process can help users with registration, order and
    payment issues.
5. Regional-language interfaces and training can improve adoption.

## 4.4 Challenges and Mitigation

  -----------------------------------------------------------------------
  Challenge                           Mitigation
  ----------------------------------- -----------------------------------
  Limited digital literacy            Simple interface, local-language
                                      support and FPO training

  Poor connectivity                   Save drafts locally and synchronize
                                      when online

  Low initial adoption                Pilot with selected FPOs and buyer
                                      groups

  Inconsistent product quality        Clear grading standards and
                                      verification records

  Perishable products                 Delivery time windows and suitable
                                      handling

  Transport cost                      Compatible order grouping and route
                                      optimization

  Payment disputes                    Provider reconciliation, receipts
                                      and grievance process

  Inaccurate forecasts                Data validation, baseline
                                      comparison and regular evaluation

  Regulatory differences              Review applicable state and
                                      national rules before launch
  -----------------------------------------------------------------------

## 4.5 Implementation Plan

  -----------------------------------------------------------------------
  Phase                   Work items              Deliverable
  ----------------------- ----------------------- -----------------------
  Phase 1                 Requirements, UI        Basic application
                          design, database and    
                          authentication          

  Phase 2                 Product listings,       Working marketplace
                          search and order        
                          management              

  Phase 3                 Payment sandbox,        Transaction workflow
                          notifications and       
                          delivery status         

  Phase 4                 Demand forecasting and  Intelligent features
                          route optimization      
                          prototype               

  Phase 5                 Testing, pilot feedback Validated pilot system
                          and deployment          
  -----------------------------------------------------------------------

**Minimum viable prototype (MVP):** - Farmer and buyer registration -
Product listing and search - Order placement and acceptance -
Transparent price breakdown - Simulated or sandbox payment workflow -
Basic delivery status - A small demand-forecasting demonstration using a
documented dataset

------------------------------------------------------------------------


## Impact and Benefits

## 5.1 Target Beneficiaries

**Farmers** - Improved access to buyers. - More transparent price
information. - Better visibility of available market opportunities. -
Easier access to bulk orders through FPOs.

**Consumers** - More information about product source and price. -
Ability to compare available farmer and FPO listings. - Potential access
to fresher products and more competitive prices.

**FPOs** - Digital coordination of member produce. - Easier handling of
bulk buyer requests. - Better records of listings and orders.

**Retailers and institutional buyers** - Easier product discovery. -
Consolidated procurement requests. - Better visibility of quantities and
delivery status.

## 5.2 Economic, Social and Environmental Benefits

**Economic** - Potential improvement in farmers' net realization through
reduced avoidable trading costs. - Better price transparency for buyers
and sellers. - More efficient procurement and delivery coordination.

**Social** - Improved digital access for rural communities. - Support
for small and marginal farmers. - Stronger coordination through FPOs.

**Environmental** - Potential reduction in unnecessary travel through
route planning. - Better inventory planning that may help reduce unsold
produce. - Improved coordination for handling perishable products.

These benefits are expected outcomes to be tested during the pilot; they
should not be presented as already achieved results.

## 5.3 Success Metrics

  -----------------------------------------------------------------------
  Indicator                           How it will be measured
  ----------------------------------- -----------------------------------
  Farmer net realization              Net amount received per unit,
                                      compared with a suitable baseline

  Consumer price difference           Comparable product, grade, quantity
                                      and location price comparison

  Order fulfilment                    Completed orders divided by
                                      confirmed orders

  Delivery performance                On-time delivery rate and average
                                      delivery duration

  Logistics efficiency                Distance and vehicle utilization
                                      per delivered unit

  Forecast performance                MAE and RMSE on test data

  Farmer adoption                     Number of active farmers and FPOs

  Buyer adoption                      Number of active buyers and repeat
                                      purchases

  Product loss                        Quantity damaged or unsold, where
                                      reliable data is available
  -----------------------------------------------------------------------

A pilot should collect baseline measurements before deployment and
compare them with results after implementation.

------------------------------------------------------------------------

## Research and References

The following official documentation and technical resources can support
the design and implementation of AgriConnect.

1.  **Smart India Hackathon -- Reference Repository**\
    https://github.com/selvasachein/SIH-26033

2.  **National Agriculture Market (e-NAM)**\
    https://enam.gov.in/

3.  **Ministry of Agriculture and Farmers Welfare, Government of
    India**\
    https://agriculture.gov.in/

4.  **Google Maps Platform Documentation**\
    https://developers.google.com/maps

5.  **Google OR-Tools Documentation**\
    https://developers.google.com/optimization

6.  **FastAPI Documentation**\
    https://fastapi.tiangolo.com/

7.  **PostgreSQL Documentation**\
    https://www.postgresql.org/docs/

8.  **Scikit-learn Documentation**\
    https://scikit-learn.org/stable/

9.  **Flutter Documentation**\
    https://docs.flutter.dev/

10. **React Documentation**\
    https://react.dev/

------------------------------------------------------------------------


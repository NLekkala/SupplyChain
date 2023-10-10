# 🛠️ SupplyChain 🛠️ 
The DAML application models a supply chain scenario where customers can place orders, suppliers can approve orders, orders can be delivered, payments can be made, and orders can be canceled.

### I. Overview
The DAML application models a supply chain scenario where customers can place orders, suppliers can approve orders, orders can be delivered, payments can be made, and orders can be canceled.

Key Data Structures:
OrderEnquiry: Represents an order inquiry created by a customer. It includes details such as customer, supplier, product, quantity, and price.
Order: Represents an order contract, including order details, status (e.g., ordered, delivered, canceled), and delivery address.
Payment: Represents a payment record between a customer and a supplier.
Address: A data record representing an address with fields for street, city, postal code, and country.
Cust and Suppl: Data records representing customer and supplier details.

### II. Workflow
1. Customer can start the order enquiry
2. Customer can Places Orders
3. Supplier can Approves Orders (Order contract will be created)
4. Customer can Updates Delivery Address
5. Supplier can Delivers Orders
6. Customer can Cancels an Order
7. Customer can Receives and Pays an Order (Payment contract will be created)
8. Supplier can Confirms Payment

### III. Challenge(s)
* The project was created by using `empty-skeleton` and the following was removed from `daml.yaml`:
```
sandbox-options:
   - --wall-clock-time
```
and the following was added:

```
init-script: SCMTest Setup

```

### IV. Compiling & Testing
To compile and test, run the pre-written script in the `Test.daml` under /daml OR run:
```
$ daml start
```
Test coverage report
```
$ daml test --show-coverage

**Test Summary
**

daml/SCMTest.daml:setup: ok, 0 active contracts, 0 transactions.
daml/SCMTest.daml:testFull: ok, 0 active contracts, 17 transactions.
Modules internal to this package:
- Internal templates
  3 defined
  3 (100.0%) created
  internal templates never created: 0
- Internal template choices
  13 defined
  10 ( 76.9%) exercised
  internal template choices never exercised: 3
    SCM:Order:Archive
    SCM:OrderEnquiry:Archive
    SCM:Payment:Archive
- Internal interface implementations
  0 defined
    0 internal interfaces
    0 external interfaces
- Internal interface choices
  0 defined
  0 (100.0%) exercised
  internal interface choices never exercised: 0
Modules external to this package:
- External templates
  0 defined
  0 (100.0%) created in any tests
  0 (100.0%) created in internal tests
  0 (100.0%) created in external tests
  external templates never created: 0
- External template choices
  0 defined
  0 (100.0%) exercised in any tests
  0 (100.0%) exercised in internal tests
  0 (100.0%) exercised in external tests
  external template choices never exercised: 0
- External interface implementations
  0 defined
- External interface choices
  0 defined
  0 (100.0%) exercised in any tests
  0 (100.0%) exercised in internal tests
  0 (100.0%) exercised in external tests
  external interface choices never exercised: 0
# Daml


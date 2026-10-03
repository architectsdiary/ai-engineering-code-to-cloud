# Mini E-Commerce Platform — Business Requirements

## Product vision
Build a Mini E-Commerce platform in which platform users can participate as customers, sellers, or administrators.

The system is developed incrementally using Spec-Driven Development.

## Core roles
### User
The platform identity.

### Customer
A User acting in the `CUSTOMER` role.

### Seller
A User acting in the `SELLER` role.

### Admin
A User acting in the `ADMIN` role.

A User may have more than one role.

## Target capabilities
- User Management
- Seller Management
- Product Catalog
- Inventory
- Cart
- Orders
- Payments
- Notifications
- Authentication and Authorization
- Observability
- Deployment and Operations

## Business requirements
- Maintain one unique platform User identity.
- A User has one or more roles: `CUSTOMER`, `SELLER`, `ADMIN`.
- A User may have multiple roles.
- A User lifecycle status is `ACTIVE` or `INACTIVE`.
- Customer and Seller are roles/capabilities of a User, not duplicate identities.
- Customer- or Seller-specific profile data is introduced only when a business requirement needs it.
- Sellers will eventually manage products and inventory.
- Customers will eventually discover products, use carts, place orders, and make payments.
- Capabilities must have clear boundaries.
- Each increment implements only its approved scope.
- Regression testing must protect behavior delivered by earlier increments.
- REST APIs are contract driven.

## Tutorial 02 outcome
Create the initial backend foundation and the User Management capability only.

## Out of scope for Tutorial 02
Product Catalog, Inventory, Cart, Orders, Payments, Notifications, authentication/authorization, messaging, and cloud deployment.

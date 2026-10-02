# Mini E-Commerce Platform — Business Requirements

The existing Customer Management application will evolve into a Mini E-Commerce Platform.

## Core concepts
- **User**: platform identity.
- **Customer**: customer-specific commerce capability/profile associated with a User.
- **Seller**: seller-specific capability/profile associated with a User.
- **Admin**: administrative role.
- Product, Cart, Order and Payment are future capabilities.

## Requirements
- BR-01: Support a unique platform User identity.
- BR-02: A User may hold one or more roles: CUSTOMER, SELLER, ADMIN.
- BR-03: User lifecycle is ACTIVE or INACTIVE.
- BR-04: Preserve the Tutorial 01 Customer capability while the identity model evolves.
- BR-05: Architecture must allow a User to act as Seller; seller-specific data is future scope.
- BR-06: Sellers will later manage products.
- BR-07: Customers will later browse, cart and order.
- BR-08: Payments are future scope.
- BR-09: Keep clear capability boundaries.
- BR-10: Implement only the current tutorial scope.

## Tutorial 02 outcome
Customer behavior remains operational; User identity, roles, lifecycle and User APIs are added and tested.

# Core Domain Model

## User
User represents the platform identity.

Initial attributes:
- `id` — UUID
- `username`
- `firstName`
- `lastName`
- `email`
- `status`
- `roles`
- `createdAt`
- `updatedAt`

## Roles
Supported roles:
- `CUSTOMER`
- `SELLER`
- `ADMIN`

A User must have at least one role and may have multiple roles.

## Customer and Seller
Customer and Seller are not separate identities in Tutorial 02.

A Customer is a User with the `CUSTOMER` role.
A Seller is a User with the `SELLER` role.

No separate Customer or Seller profile is created in this increment because no role-specific profile data is required yet.

If a later business requirement introduces customer-specific or seller-specific data, dedicated profile models may be introduced without replacing the fundamental User identity.

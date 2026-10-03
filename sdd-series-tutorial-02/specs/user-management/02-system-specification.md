# User Management — System Specification

## Create User
1. Validate required fields, email format, and roles.
2. Enforce case-insensitive uniqueness of username and email.
3. Generate a UUID.
4. Set status to `ACTIVE`.
5. Generate `createdAt` and `updatedAt`.
6. Persist the User.
7. Return the created User representation.

## Get User by ID
- Return the existing User for a valid UUID.
- If no User exists, return not found.

## List Users
- Return all Users.
- If no Users exist, return an empty collection.

## Update User
Editable values:
- username
- firstName
- lastName
- email
- roles

Rules:
- Preserve `id`, `createdAt`, and current `status`.
- Validate required fields and roles.
- Enforce case-insensitive uniqueness against other Users.
- Allow the User to retain their own username/email.
- Update `updatedAt`.

## Update Status
- Accept only `ACTIVE` or `INACTIVE`.
- Update status and `updatedAt`.
- Preserve other User state.

## Replace Roles
- Replace the complete role set.
- Require at least one supported role.
- Update `updatedAt`.
- Preserve other User state.

## Delete User
- Delete an existing User.
- If the User does not exist, return not found.

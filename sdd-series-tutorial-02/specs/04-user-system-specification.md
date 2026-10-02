# User System Specification
Create validates required fields, valid email, case-insensitive username/email uniqueness and non-empty supported roles. Generate UUID/timestamps and default ACTIVE.

Get returns User or not found. List returns all Users or an empty collection.

Update may change username, firstName, lastName, email and roles while preserving ID/createdAt and refreshing updatedAt. Uniqueness rules allow retaining one's own values.

Status patch accepts ACTIVE or INACTIVE. Roles patch replaces the complete non-empty role set.

Delete removes an existing User; missing User is not found. No Customer/Seller cascade is introduced.

Existing Tutorial 01 Customer behavior remains unless an approved impact-analysis decision explicitly changes it.

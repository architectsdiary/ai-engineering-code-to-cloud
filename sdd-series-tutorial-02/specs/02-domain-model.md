# Domain Model
## User
UUID id; unique case-insensitive username; firstName; lastName; unique case-insensitive email; ACTIVE/INACTIVE status; one or more CUSTOMER/SELLER/ADMIN roles; createdAt; updatedAt.

## Customer
Customer already exists from Tutorial 01. In the target model it represents customer-specific business capability/profile associated with a User.

Do not invent a destructive migration. Impact analysis must report overlapping fields, compatibility impact, relationship options and an incremental recommendation. Existing Customer APIs remain unless an approved specification change says otherwise.

## Seller
Future seller-specific profile associated with a User holding SELLER. Not implemented now.

Product, Inventory, Cart, Order, Payment and Notification are future domains.

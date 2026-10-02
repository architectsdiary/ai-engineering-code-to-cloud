# System Context
`mini-ecom-backend` is the single evolving backend. Tutorial 01 introduced Customer Management. Tutorial 02 introduces platform identity.

Future logical capabilities: User/Identity, Customer, Seller, Product Catalog, Inventory, Cart, Order, Payment, Notification.

Tutorial 02 implements only User identity, roles, lifecycle, User API, and compatibility with existing Customer behavior. These are logical boundaries; separate microservices are not required.

The agent must inspect existing Customer code before proposing changes. Any Customer model/API change must appear in impact analysis first.

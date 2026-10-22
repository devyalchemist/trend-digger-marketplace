# Trend Digger Marketplace Rebuild

A full-stack marketplace foundation using common shopping-platform UX patterns. It does not copy proprietary source code, branding or assets from Temu, Jumia or AliExpress.

## Customer
- Marketplace-style discovery, search and category browsing
- Dedicated product detail experience
- Colors, sizes, variant price/stock/SKU
- Reviews and ratings
- Cart and checkout
- Account required for checkout
- Email/Gmail address + password account flow
- Google OAuth connection point for production credentials
- Nigerian State/LGA/address/phone delivery fields
- Bank-transfer checkout controlled from Admin
- Unique order reference and receipt upload
- My Orders, payment/order status and genuine tracking details
- Customer PWA/installable website
- Exact owner-supplied Trend Digger logo

## Admin
Open `/admin/`.
- Dashboard
- Add Product
- Edit/Delete Product
- Description, category, price, compare price, stock
- Product image URLs and video URL
- Per-product shipping fee
- Colors and sizes as variants
- Variant price, stock and SKU
- Orders and customer details
- Payment status verification
- New / Paid / Processing / Shipped / Delivered / Cancelled
- Carrier + tracking number
- Customers
- Analytics
- Bank Transfer settings
- Separate Admin PWA

## No demo products
The catalogue starts empty. Add your own products from Admin.

## Run
Node.js 20+ recommended:
1. `npm install`
2. Set `SESSION_SECRET` in production.
3. `npm start`
4. Store: `http://localhost:3000/`
5. Admin: `http://localhost:3000/admin/`

To authorize an admin after registering a user, the developer can run:
`UPDATE users SET role='admin' WHERE email='YOUR_ADMIN_EMAIL';`

## Production before launch
Add HTTPS, strong secrets, rate limiting, CSRF protection, password reset/email verification, secure Google OAuth, cloud image/receipt storage, database backups, email/WhatsApp notifications, carrier integrations, policy pages and an audit log.

Never store Google passwords, card CVV, OTPs, PINs or other sensitive credentials.

## Research basis
Current official marketplace pages show common patterns including app-download promotion, account/sign-in, search/catalogue discovery, product reviews, checkout, order management, delivery/returns support and separate seller/vendor management. Trend Digger uses those patterns with its own UX and exact supplied logo.

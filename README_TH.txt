SmartExpiry Account + QR v2

Flow:
- First time visitor: Continue with Google creates a Firebase Auth user automatically. My Products starts empty.
- Returning visitor: Firebase Auth restores the signed-in session; scan QR -> Product Details directly.
- Signed out visitor scans QR: Google login first, then product details; never automatically adds a product.
- Product saved ONLY after pressing Add to My Products.
- Data stored in Firestore users/{uid}/products/{productId}.
- Existing data from previous version in same Firestore path is retained.
- QR codes use ?product=milk, coffee, burger, bread.
- Expiry dates are DEMO values and must be replaced with actual product/batch dates before real use.
- One record per product type in this prototype.
- M5 hardware integration not yet implemented.

Deployment:
1. Upload index.html, style.css, app.js, firebase-config.js to ROOT of GitHub repository Smart_Expiry (not nested folder).
2. Do NOT upload QR folder as website files unless desired.
3. In Firebase Console > Authentication > Sign-in method, enable Google.
4. Authorized domains must include mazjinoomnim.github.io.
5. Firestore rules must allow users/{uid}/products/{productId}; see firestore.rules.
6. Test each URL directly and test using two Google accounts.
7. If login fails, re-copy apiKey directly from Firebase console (case-sensitive) and check browser console.

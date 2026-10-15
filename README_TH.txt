SMARTEXPIRY GOOGLE LOGIN + FIRESTORE

1) Open https://console.firebase.google.com and create a Firebase project.
2) Project settings > Your apps > Web > Register app. Copy firebaseConfig values into firebase-config.js.
3) Authentication > Sign-in method > Google > Enable and save (set support email).
4) Authentication > Settings > Authorized domains > Add mazjinoomnim.github.io if not listed.
5) Firestore Database > Create database. In Rules, replace with firestore.rules and Publish. Never use public allow read/write rules.
6) Upload ONLY index.html, style.css, app.js, firebase-config.js to the ROOT of your GitHub repository Smart_Expiry. Do not upload firestore.rules to the site; paste it into Firebase console.
7) Visit https://mazjinoomnim.github.io/Smart_Expiry/ and click Continue with Google.
8) Scan https://mazjinoomnim.github.io/Smart_Expiry/?product=milk and click Add to My Products.
9) Sign in with the same Google account on another device to see saved products. Test with another Google account to verify isolation.

Important: product dates are DEMO values in app.js; not actual food safety guidance. Products are currently keyed by product type, so only one milk per user. A later version should support multiple batches/individual packages. M5 is not yet connected. Sign-in uses a Google popup and requires HTTPS/localhost; opening index.html directly via file:// will not work.

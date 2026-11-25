# ShopSmart-AI
Shopping Assistant Prototype
What this app does


Opens the ShopSmart AI prototype as an Android app.

Uses the tablet's screen size and responsive layout.

Enables JavaScript and browser local storage for the prototype.

Keeps the sample inventory and recorded sales in the app's local WebView storage.


Current limitations


This is a local demo; it has no cloud sync, user login or live AI API connection.

The “AI Advisor” uses predefined JavaScript business rules, not a live AI model.

Data is stored on that tablet inside the app. Clearing app storage or uninstalling the app can erase it.

The app currently does not need internet permission because all screens and logic are bundled locally.

Before using this for real business records, add backup, authentication, cloud database, security and proper accounting/tax handling.


Project layout


app/src/main/assets/ — index.html, style.css, script.js

app/src/main/java/com/shopsmart/ai/MainActivity.kt — Android WebView host

app/src/main/AndroidManifest.xml — app configuration

app/build.gradle — Android build configuration

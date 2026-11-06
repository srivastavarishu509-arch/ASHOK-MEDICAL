ASHOK MEDICAL — Android starter app
This is a native Android Studio starter project using Kotlin, Jetpack Compose and Room.
Included in this starter
Local/offline medicine inventory database
Add medicines, quantities, selling prices and expiry text
Low-stock indicator (10 units or fewer)
Customer order entry
Order delivery status updates
Pending balance tracking and mark-fully-paid action
Daily sales total based on orders created today
Persistent local storage using Room
Open and run
Install Android Studio (current stable).
Open this folder as an existing project.
Allow Gradle sync to complete.
Run the app configuration on an Android device or emulator (Android 8.0+).
Online sync: next integration step
The app currently works offline and stores data locally. Cloud sync is not yet connected. To enable the online half:
Create a Firebase project owned by the pharmacy.
Register Android app ID com.ashokmedical.app.
Add the generated google-services.json under app/.
Configure Firebase Authentication and Cloud Firestore with strict per-store security rules.
Implement conflict resolution and an outbox-based WorkManager sync worker before enabling multi-device writes.
Do not put service-account keys or admin credentials in the Android app.
Important production work still required
Owner/staff authentication and role-based permissions
Cloud sync, encrypted transport, backups and restore testing
Barcode scanning and receipt/thermal printer integration
Batch-wise stock deduction and expiry alerts
GST invoice configuration and audit logs
Prescription workflow and compliance review
Tested stock reconciliation and payment reversal flows
This is a starter implementation, not a production-ready pharmacy billing system. Verify local pharmacy, tax, prescription and data-protection requirements before using it with real customers. Do not use sample data for actual dispensing decisions.

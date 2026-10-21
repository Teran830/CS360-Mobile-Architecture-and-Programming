# CS360-Mobile-Architecture-and-Programming
Portfolio for my CS360 Android inventory application.

## App Requirements and Goals

My Inventory Tracker app helps users maintain inventory records and identify when supplies need restocking. The requirements included account creation, login, database storage, and the ability to display, add, edit, and delete inventory items. The app also includes optional SMS alerts when an item’s quantity reaches zero. These features address the need to manage supplies, such as masks, without relying on manual records.

## User-Centered Screens and Features

The app includes a login and registration screen and an inventory screen with item names, quantities, and editing controls. Notification settings allow users to enter a phone number and request SMS permission. I used descriptive labels, readable text, and consistent colors to make the interface understandable. Keeping inventory actions beside each item reduced unnecessary navigation, while confirmation prompts helped prevent accidental deletion. The design supported successful completion of the inventory tasks I tested.

## Coding Approach

I developed the app in Android Studio using Java and XML. I worked on individual features and tested them before connecting the complete workflow. I separated database operations into DatabaseHelper and notification handling into SmsAlertManager, which made the activity code easier to manage. I also included input validation and performed database work outside the main UI thread. In future projects, I can apply this approach to organize responsibilities, investigate errors, and add features without placing all the logic in one class.

## Testing and Results

I manually tested the app in the Android Emulator by creating an account, logging in, and adding, editing, and deleting inventory items. I also checked SMS permission choices and the phone-number setup process. Testing revealed startup problems and a lack of clear feedback during notification setup. This process was important because a feature could appear complete in the code while still confusing the user. Repeating the inventory actions after changes helped me confirm that those functions continued to work.

## Challenges and Problem Solving

Notification setup required me to consider more than whether the user granted permission. Entering a phone number alone did not clearly communicate whether alerts were enabled. I addressed this by separating notification handling into its own class and providing status messages for disabled alerts, enabled alerts, and SMS submission outcomes. The app also keeps inventory management available when SMS permission is denied. This challenge helped me design around different user choices and distinguish saving inventory from successfully sending a notification.

## Strongest Component

The inventory management component best demonstrates my knowledge and progress. I connected the interface to SQLite operations so users could add, view, update, and delete records. I also included quantity validation, deletion confirmation, and refreshed inventory information after changes. Successfully testing these actions with mask inventory showed my ability to combine interface design, Java programming, and database management into a practical mobile application.

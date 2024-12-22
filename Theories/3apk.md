
**APK **
=> It is a package file format used by android operating system for distribution and installation if android apps.
=> It means Android Application Package.
=> Similar to execuatble file .exe in windows os.

The extension of APK is .apk
It consists of :-
    application code (.dex files),manifest files,assests,resources files,



ACTIVITY :-

In Android development, an Activity is a core component of an application that represents a single, focused screen with a user interface (UI). It acts as the entry point for interacting with the user and facilitates tasks such as displaying content, capturing input, and navigating between different parts of the app.

Key Characteristics of an Activity
UI Representation:

Each activity is associated with a layout file (XML) that defines its UI.
For example, a login activity might use a layout with EditText fields for username and password.
Lifecycle Management:

Activities have a well-defined lifecycle managed by Android. Developers override lifecycle methods like onCreate(), onStart(), onPause(), and onDestroy() to implement functionality at different stages.
Interactivity:

Activities respond to user actions, such as button clicks, swipes, or other input events.
Navigation:

Apps often consist of multiple activities, and users navigate between them using intents or navigation components.
Activity Lifecycle
The lifecycle of an activity is managed by Android to optimize resource usage and ensure smooth app behavior. Here's a simplified overview:

Created (onCreate()):

Called when the activity is first created.
Used to initialize the activity, set up the UI, and bind data to views.
Started (onStart()):

Called when the activity becomes visible to the user.
Resumed (onResume()):

Called when the activity is in the foreground and ready for user interaction.
Paused (onPause()):

Called when the activity is partially obscured (e.g., when a dialog appears).
Used to pause animations or save UI state.
Stopped (onStop()):

Called when the activity is no longer visible.
Resources can be released here to save memory.
Destroyed (onDestroy()):

Called when the activity is completely removed from memory.
Common Use Cases for Activities
Single-Screen Apps:

If an app has only one screen (e.g., a calculator), it might consist of just one activity.
Multi-Screen Navigation:

Apps with multiple screens (e.g., login, dashboard, settings) have one activity per screen.
Specialized UIs:

Activities can be used for specific tasks like displaying media, capturing photos, or showing maps.
Activity vs Other Components
Activity vs Fragment:

Activities are independent screens, while Fragments are modular sections of UI that run within an activity.
Fragments allow for reusable and flexible UI designs, especially for apps that need dynamic layouts or navigation.
Activity vs Service:

While an activity handles user interaction, a Service is used for background tasks (e.g., downloading files or playing music).
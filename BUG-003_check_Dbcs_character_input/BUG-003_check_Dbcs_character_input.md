**[Check Dbcs Character Inputs]:** Full Name text field is entirely missing from the Edit Profile screen]

**[Summary]**
While attempting to validate double-byte character set (DBCS) inputs on the profile customization screen, the "Full Name" input text box is completely missing from the user interface. The screen only provides modification options for the profile avatar picture and the delivery address. Because the Full Name field does not exist on the form, the test case preconditions cannot be satisfied, and DBCS validation for the user's name cannot be executed.

**[Precondition]**
Software version: v1.0
Software configuration: Android 13 / One UI 5
Hardware specifications: Samsung Galaxy S20 FE 5G (Android OS)
Network configuration: Wi-Fi / LAN
User is signed in and has navigated to the profile settings menu.

**[Steps to reproduce]**

    Launch the application and open the profile navigation settings.

    Tap the edit button to access the profile fields modification screen.

    Scan the interface for the "Full Name" text entry field.

    Observe that only options for editing the "Profile Avatar" and "Delivery Address" are displayed.

    Input double-byte characters ('テストユーザー' / '張三') into the available "Delivery Address" text field to isolate system encoding behavior.

**[Actual results]**
The "Full Name" text field is completely absent from the Edit Profile interface layout. The user is only presented with controls to swap their profile avatar image and update their delivery address text, leaving no text box available to input the required Japanese or Chinese test characters for the name attribute.

**[Expected results]**
The Edit Profile form must include a dedicated "Full Name" input text field alongside the avatar and address options, allowing users to input, edit, and successfully save standard and double-byte character data to the profile cards.

**[Additional information]**
Isolating the issue shows that entering double-byte characters into the available "Delivery Address" text field works flawlessly without any system errors or layout distortions. The system safely accepts and processes the encoding; therefore, this defect is entirely a structural UI omission of the name field rather than a character processing error.

**[Is this Breakage?]**
Yes, broken in current pass

**[Severity: How does this problem impact the customer/user?]**
3. Major issue / Core function disabled (Users are completely unable to set or change their display name on the platform)

**[Likelihood: How often will a customer/user use this feature/function?]**
4. Low to Moderate (Typically used during initial account setup or onboarding profile adjustments)

**[Repeatability: Is this problem easily reproducible?]**
10. 100% Reproducible

**[Impacted Test Cases]**
UI-002: Check Dbcs Character Inputs

**[Impact Sizing (in days)]**
Less than a day (Requires adding the missing text input component back into the profile view layout file)

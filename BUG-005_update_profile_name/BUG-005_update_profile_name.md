**[Update Profile Name And Delivery Address]:** Update Name input field does not exist on the Edit Profile layout screen]

**[Summary]**
During validation of the profile update process, the option to update or change the user's name is missing from the interface. While the "Delivery Address" input field and "Profile Avatar" edits display normally, the text box for editing the profile name does not exist. Because the name modification field is entirely absent from the layout, the step to update the profile name to 'Clyde Egmilan' cannot be performed or validated.

**[Precondition]**
Software version: v1.0
Software configuration: Android 13 / One UI 5
Hardware specifications: Samsung Galaxy S20 FE 5G (Android OS)
Network configuration: Wi-Fi / LAN
User is securely logged into the application.

**[Steps to reproduce]**

    Launch the application on the Samsung Galaxy S20 FE 5G.

    Navigate to the Profile screen and tap the 'Edit Profile' action button.

    Inspect the loaded text input fields on the screen for the name attribute.

    Observe that fields for "Delivery Address" and "Profile Avatar" display, but an input for the name is absent.

**[Actual results]**
The profile modification details load partially, but the "Update Name" text field does not exist in the layout configuration. Only the "Delivery Address" and "Profile Avatar" entries are interactive and present on the screen, rendering it impossible to modify the profile name value from the user interface.

**[Expected results]**
The 'Edit Profile' view layout must expose both the "Update Name" and "Delivery Address" text entry fields so users can seamlessly change their display name to 'Clyde Egmilan', save the payload, and trigger the Riverpod state refresh to sync with the Supabase database.

**[Additional information]**
This confirms a recurring layout structural omission where the user display name field is dropped from the profile editor view component.

**[Is this Breakage?]**
Yes, broken in current pass

**[Severity: How does this problem impact the customer/user?]**
3. Major issue / Core function disabled (Users can modify their shipping address but are blocked from correcting or changing their account display name)

**[Likelihood: How often will a customer/user use this feature/function?]**
4. Low to Moderate

**[Repeatability: Is this problem easily reproducible?]**
10. 100% Reproducible on this specific hardware profile

**[Impacted Test Cases]**
PROF-001: Update Profile Name And Delivery Address

**[Impact Sizing (in days)]**
Less than a day (Requires adding the name text input field binder back to the widget tree / view file)

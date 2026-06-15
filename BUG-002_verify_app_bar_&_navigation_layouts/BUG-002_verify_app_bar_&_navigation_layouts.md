[Verify App Bar And Navigation Layouts]: App entirely ignores dark mode toggle and remains in light mode layout on Samsung Galaxy S20 FE 5G

[Summary]
When executing theme validation on a Samsung Galaxy S20 FE 5G, toggling the system or app-level dark mode setting produces absolutely no change in the user interface. The application fails to meet the test case preconditions of running in both display modes, as the entire theme, layout, components, and text show no visible changes or anomalies upon switching. The app simply stays locked in its default light mode configuration. Because everything remains in light mode, text readability itself is not broken, but the dark mode feature is completely non-functional.

[Precondition]
Software version: v1.0
Software configuration: Android 13 / One UI 5
Hardware specifications: Samsung Galaxy S20 FE 5G (Android OS)
Network configuration: Wi-Fi / LAN
App is running on the home dashboard screen in its default light mode state.

[Steps to reproduce]

    Launch the app on the Samsung Galaxy S20 FE 5G and navigate to the home dashboard.

    Observe the default light mode layout, buttons, margins, and text contrast ratios (all render correctly according to style guidelines).

    Toggle the dark mode setting (either via system quick settings or in-app theme toggle).

    Return to the dashboard to observe if any theme adaptation occurs.

[Actual results]
The app experiences no visible changes, layout shifts, or theme anomalies after toggling dark mode. It completely ignores the system change and continues running normally in its default light mode layout. While text readability remains perfectly fine due to the light mode styles staying intact, the application fails to transition into a dark theme entirely.

[Expected results]
All dashboard components, backgrounds, buttons, and app bars must seamlessly and instantly transition from light mode colors to their corresponding dark mode layout palettes upon toggling the setting, satisfying the visual display guidelines for both UI themes.

[Additional information]
Unlike typical theme bugs where text becomes unreadable due to partial color changes, this issue represents a total failure of the app to listen to or register the theme change event on this device profile.

[Is this Breakage?]
Yes, broken in current pass

[Severity: How does this problem impact the customer/user?]
2. Cosmetic issue / User is inconvenienced (The dark mode feature does not work at all, forcing users to use light mode exclusively)

[Likelihood: How often will a customer/user use this feature/function?]
6. Moderate

[Repeatability: Is this problem easily reproducible?]
10. 100% Reproducible on this specific hardware profile

[Impacted Test Cases]
UI-001: Verify App Bar And Navigation Layouts

[Impact Sizing (in days)]
Less than a day

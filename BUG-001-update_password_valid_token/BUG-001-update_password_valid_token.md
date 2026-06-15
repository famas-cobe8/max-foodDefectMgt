[Update Password]: Valid recovery link bypasses form and forces auto-login

[Summary]
When a user clicks the forgot password email recovery deep link, the application immediately resolves the session token, logs the user in, and redirects them directly to the dashboard. The system completely bypasses the mandatory password reset input form, preventing the user from updating their password while exposing a critical authentication vulnerability.

[Precondition]
Software version: v1.0
Software configuration: Default
Hardware specifications: Web App
Network configuration: N/A
User is logged out and has requested a password reset email link.

[Steps to reproduce]

    Open the forgot password recovery email.

    Click the recovery deep link to initiate the password update process.

    Observe the target application behavior upon link activation.

[Actual results]
The application skips the input form completely. Clicking the link automatically resolves the token, establishes an active authenticated session, and forces an immediate landing on the dashboard without requiring or accepting any new password input.

[Expected results]
Clicking the recovery link must safely route the user to the secure password reset input form, accept a new compliant password, update the database server upon clicking 'Save Password', and only then establish the authenticated session and redirect to the dashboard.

[Additional information]
This represents a severe security risk as the token acts as an immediate auto-login link rather than a form validator.

[Is this Breakage?]
Yes, broken in current pass

[Severity: How does this problem impact the customer/user?]
10. Critical issue / High security risk (Bypasses authentication form and allows direct dashboard access via link)

[Likelihood: How often will a customer/user use this feature/function?]
4. Low to Moderate (Triggered during account recovery flows)

[Repeatability: Is this problem easily reproducible?]
10. 100% Reproducible

[Impacted Test Cases]
AUTH-008: Update Password Valid Token

[Impact Sizing (in days)]
1-2 days (Requires security refactoring of the token validation and routing logic)

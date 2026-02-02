# Overview
I assessed the access controls enforced during user registration, with a focus on email domain restrictions. During testing, I identified a business logic flaw caused by discrepancies between the application’s email validation logic and the underlying email parsing behavior. By abusing UTF-7–encoded email formats, I bypassed domain-based restrictions, successfully registered an unauthorized account, and gained access to administrative functionality. This project demonstrates how inconsistent input parsing can directly lead to access control bypass and full privilege escalation.

# Methodology

Step 1: Intercepted and analyzed registration requests to understand email validation logic.

Step 2: Tested multiple encoded email formats to identify parsing inconsistencies.

Step 3: Bypassed domain restrictions using a UTF-7–encoded email payload.

Step 4: Activated the spoofed account and verified access to restricted administrative functionality.

# Conclusion

This assessment revealed a high-severity business logic vulnerability where inconsistent email parsing enabled unauthorized registration and administrative access. The findings highlight the risks of relying on string-based validation for access control decisions and the need for consistent input normalization across validation and processing layers.

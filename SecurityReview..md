1.Weak Password Policy
What is wrong?
The password policy is only checking for a minimum of 8 characters.This is considered weak as attackers can easily brute-force short passwords.
How did you find it?
In the registration validation schema, the password is only required to be a minimum of 8 characters.
How should it work/What should be fixed?
Strengthen the password policy by requiring a combination of uppercase letters, numbers, and special characters for example (z.string().min(8).regex(/^(?=.*[A-Z])(?=.*\d)(?=.*[!@#$%^&*]).+$/)).
2.No Session Expiration
What is wrong?
Sessions seem to persist indefinitely, with no expiration set for the session cookie.
How did you find it?
The session cookie is set without any expiration or timeout.
How should it work/What should be fixed?
Implement session expiration. You can set a max-age attribute in the session cookie and/or use a session expiration strategy for example (1 hour timeout)
3.Lack of User Role Validation for Admin Actions
What is wrong?
There is no explicit check to ensure that only administrators can perform actions like adding or deleting resources.
How did you find it?
There is no code that checks the user’s role before allowing certain actions in the system.
How should it work/What should be fixed?
Implement role-based access control (RBAC) to ensure that only users with the administrator role can perform admin actions. For example, use middleware to check the user’s role before accessing sensitive routes.
4.Missing CSRF Protection
What is wrong?
There is no mention of CSRF (Cross-Site Request Forgery) protection in the code.
How did you find it?
The application does not appear to include any mechanism to protect against CSRF attacks on state-modifying requests (like registration and login).
How should it work/What should be fixed?
Implement CSRF protection on all state-modifying requests for example login,registration,and reservation creation. You can use tokens stored in cookies.
5.No Protection Against Brute Force Attacks (Login)
What is wrong?
There is no mechanism to prevent brute-force login attempts, such as limiting the number of login attempts or introducing CAPTCHA.
How did you find it?
The login flow simply compares the user-provided password with the hashed password without any rate-limiting.
How should it work/What should be fixed?
Implement rate-limiting or CAPTCHA after a set number of failed login attempts to prevent brute force attacks. Use tools like express-rate-limit or implement custom rate-limiting logic.
6.Lack of HTTPS/Encryption for Data Transmission
What is wrong?
There is no indication that data is being transmitted over HTTPS, which means sensitive information (like passwords) could be intercepted during transmission.
How did you find it?
The code doesn’t mention enforcing HTTPS, and sensitive actions like login and registration could be vulnerable to man-in-the-middle (MITM) attacks.
How should it work/What should be fixed?
Ensure that the application only accepts HTTPS requests. Implement SSL/TLS certificates for encrypted communication.
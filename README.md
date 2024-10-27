# OTP_Verification_System
The OTP Verification System provides a secure solution for generating, sending, and validating one-time passwords for user authentication. It features customizable OTP length, secure transmission via email , and expiration-based validation. Designed with flexibility and security in mind, it can easily integrate into different applications to enhance user verification and protect against unauthorized access.

## OTP System User Interface
![OTP_System](https://github.com/user-attachments/assets/afb8c285-54f7-4591-842e-b5c371f8ea51)

## Need for Authentication
In the digital age, security and user authentication are paramount to protecting sensitive information and ensuring the integrity of online transactions. One of the most effective methods to enhance security is through the implementation of One-Time Passwords (OTPs). OTPs provide an additional layer of security by generating unique codes that are valid for only a short period or a single transaction.

## Project Objective
This Python project focuses on implementing an OTP verification system. The primary goal is to provide a robust and user-friendly solution for authenticating users through temporary, unique codes.
### **Key features**:
  - Dynamic OTP Generation
  - Time-Based Expiration
  - Email and OTP Verification
  - Error Handling and Feedback

## Technical Stacks
- **Frameworks** : SMTPLib, Mime, Random, Time
- **GUI** : Tkinter
- **Email Protocol** : SMTP

## OTP Verification Workflow
![image](https://github.com/user-attachments/assets/1913ed18-8a4c-4f77-954f-45de5adadcee)

## Key Methods
- Verify_sender_credentials()
- validate_email()
- generate_otp()
- send_otp_via_email()
- is_otp_expired()
- verify_otp()

## Dependencies
  - Python 3.x
  - Tkinter (usually included with Python)
  - smtplib, email.mime.text, email.mime.multipart, re, random (all are standard libraries)
  
## Setup
  - Replace your_email_password with the actual password for the email address used to send OTPs.
  - Ensure that less secure app access is enabled in the Gmail account settings if using Gmail for sending OTPs.

## Execution
  - Save the code to a file.
  - Run the file using a Python interpreter

## Testing
### Test Case 1: Valid Email and OTP
#### Objective: Verify that the system correctly handles valid email and OTP entries, granting access.
  - Launch the application.
  - Enter a valid email address in the email input field.
  - Click the "Send OTP" button.
  - Ensure the OTP is sent to the provided email address (check the inbox for the correct OTP).
  - Enter the correct OTP in the OTP input field.
  - Click the "Submit OTP" button.
#### Expected Result:
  - The application should display a message indicating that access is granted.
  - The application window should close after successful authentication.

### Test Case 2: Invalid Email Address
#### Objective: Verify that the system correctly handles invalid email addresses and prompts the user to re-enter.
  - Launch the application.
  - Enter an invalid email address.
  - Click the "Send OTP" button.
  - The application should display an error message about the invalid email.
  - Re-enter another invalid email address.
  - Click the "Send OTP" button.
  - The application should display another error message.
  - Repeat until the maximum number of attempts (3) is reached.
#### Expected Result:
  - The application should display an error message for each invalid email.
  - After 3 attempts, the application should exit with an appropriate error message.

### Test Case 3: Invalid OTP Format
#### Objective: Verify that the system correctly handles OTPs that are not 6-digit numbers.
  - Launch the application.
  - Enter a valid email address and click the "Send OTP" button.
  - When the OTP is received, enter an OTP that is not a 6-digit number.
  - Click the "Submit OTP" button.
#### Expected Result:
  - The application should display an error message indicating that the OTP format is invalid.
  - The user should be given up to 3 attempts to enter a valid OTP.
  - After 3 incorrect attempts, the application should exit with an appropriate error message.

### Test Case 4: Incorrect OTP
#### Objective: Verify that the system correctly handles incorrect OTPs and prompts the user to re-enter.
  - Launch the application.
  - Enter a valid email address and click the "Send OTP" button.
  - Enter a valid OTP but enter an incorrect OTP (not matching the sent OTP).
  - Click the "Submit OTP" button.
  - The application should display an error message about the incorrect OTP.
  - Re-enter an incorrect OTP (e.g., a different wrong OTP).
  - Click the "Submit OTP" button.
  - Repeat until the maximum number of attempts (3) is reached.
#### Expected Result:
  - The application should display an error message for each incorrect OTP.
  - After 3 incorrect attempts, the application should exit with an appropriate error message.

### Test Case 5: OTP Expiration
#### Objective: Verify that the system correctly handles OTP expiration after a specified time and prompts the user to request a new OTP.
  - Launch the application.
  - Enter a valid email address and click the "Send OTP" button.
  - Wait for the OTP expiration period to pass (e.g., 5 minutes).
  - Enter the OTP that was previously sent (after the expiration time).
  - Click the "Submit OTP" button.
#### Expected Result:
  - The application should display an error message indicating that the OTP has expired.
  - After 3 incorrect attempts, the application should exit with an appropriate error message.

### Test Case 6: Sending OTP Failure
#### Objective: Verify that the system handles failure to send the OTP correctly.
  - Launch the application
  - Enter a valid email address and click the "Send OTP" button.
  - Simulate a failure in sending the OTP (e.g., by modifying the SMTP settings or causing a network error).
  - Observe the behavior of the application.
#### Expected Result:
  - The application should display an error message indicating that the OTP failed to send.
  - The application should exit or handle the failure gracefully, depending on the error handling logic.

## Future Scope
- **Multi-Factor Authentication (MFA)**: Expand the OTP system into a multi-factor authentication process by combining OTP with biometric authentication or security questions.
- **Customizable Authentication Flow**: Allow system administrators to define their OTP delivery method (email, SMS, or in-app notifications) and adjust the validation parameters (e.g., OTP length, expiration).
- **Integration with OAuth**: Implement the OTP system into OAuth protocols to add another layer of security to third-party logins.
- **Mobile App Integration**: Extend the functionality to mobile applications, utilizing push notifications for OTP delivery.


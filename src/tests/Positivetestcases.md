TC ID	Test Scenario	Preconditions & Test Data	Steps	Expected Result
REG-P01	Register with all mandatory fields	User is on the registration page; unique email and valid credentials.	1. Fill all required fields with valid data.
2. Accept Terms & Conditions.
3. Click Register/Sign Up.	Account created successfully; confirmation message or verification email/OTP sent.
REG-P02	Register with mandatory + optional fields	Valid mandatory data + optional fields (e.g., phone, profile avatar, middle name).	1. Fill all required and optional fields.
2. Click Register.	Account created; optional profile details saved correctly in the database.
REG-P03	Password meets exact minimum complexity requirements	Password matches minimum length, 1 uppercase, 1 lowercase, 1 number, 1 special char (e.g., P@ssw0rd1).	1. Enter valid details and minimum valid password.
2. Click Register.	Password accepted; registration proceeds without complexity error.
REG-P04	Email and username trimming	Valid email/username with leading/trailing spaces (e.g., user@example.com).	1. Enter email/username with leading/trailing spaces.
2. Complete form and submit.	Whitespace is automatically trimmed; user is registered with clean input.
REG-P05	Successful account verification (Email / OTP)	Registration completed; verification token/OTP generated.	1. Open verification link or enter received OTP.
2. Submit verification.	Account status changes from Pending/Unverified to Active; user can now log in.
REG-P06	Maximum allowed boundary values	Fields filled with maximum allowed characters (e.g., 50-char name, 254-char email).	1. Enter max valid length for all inputs.
2. Submit form.	System accepts data without truncation or database buffer overflow.

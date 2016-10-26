Simple Windows Hello demo
-------------------------

# This simply shows the desired behaviour of using biometrics to logon to a Windows PC, with an IR camera for facial recognition.
Technologies: **Windows Hello**
Technical Depth: **None, basic windows admin**
Time: **2-3 minutes**
Software: **Windows 10**
Hardware: **Intel RealSense Camera**
Video: 
Supporting files: **N/A**
Accounts: **Preset Account needs to be enabled for the user in advance as per below.**

Setup
-----
1. Ensure you have an account with a PIN enabled Settings > Accounts > Sign-In Options > Pin - ADD -- Use an MSA (Live) Account 
2. Ensure Windows Hello is enabled 

-- Settings > Accounts > Sign-In Options > Windows Hello - Face (Click Set up) 
-- Click Get Started 
-- Enter your account PIN 
-- Click Improve Recognition a couple of times (Once for example with the screen rotated so the lighting conditions are different) 

3. Ensure that both yourself and someone else nearby has registered their face to this device. 
4. Set Require Sign in to 'Every Time' and ensure that Automatically unlock the screen if we recognise your face is checked :) 

Explain the demo
----------------

Show how the device can be unlocked with PIN and/or Face usng a Microsoft Account and an Azure AD Account.
Hello lets users authenticate to:
a Microsoft account.
an Active Directory account.
a Microsoft Azure Active Directory (Azure AD) account.
Identity Provider Services or Relying Party Services that support Fast ID Online (FIDO) v2.0 authentication

Hello addresses the following problems with passwords:
 - Passwords can be difficult to remember
 - users often reuse passwords on multiple sites.
 - Server breaches can expose symmetric network credentials.
 - Passwords can be subject to replay attacks.
 - Users can inadvertently expose their passwords due to phishing attacks 

Try and spoof it with a photo, IR will not display

** Make the following points clear:- **
 - A password is globally configured and can be used from any device.
 - A PIN is held locally on the machine it was registered from, it is tied to the device.
 - As a result the physical DEVICE becomes a second factor of authentication, along with your face / PIN, if you go to another domain / device your PIN / face registration will not work.

 - The Hello PIN is backed by a Trusted Platform Module (TPM) chip
 - Because Hello uses asymmetrical key pairs, users credentials can’t be stolen in cases where the identity provider or websites the user accesses have been compromised.

**PIN can be complex**

The Windows Hello for Business PIN is subject to the same set of IT management policies as a password, such as complexity, length, expiration, and history. 

**What if someone steals the laptop or phone?**
To compromise a Windows Hello credential that TPM protects, an attacker must have access to the physical device, and then must find a way to spoof the user’s biometrics or guess his or her PIN  — and all of this must be done before TPM anti-hammer capabilities lock the device.

i.e. The attacker would need to be able to generate a 3d infra-red reflective version of your image, or steal your head too (let's hope no-one seriously attempts that) :) 

This PIN enables you to sign in using the PIN when you can’t use your preferred biometric because of an injury or because the sensor is unavailable or not working properly.

This discussion should also include FIDO2 as that’s a key part of what we’re doing here. 

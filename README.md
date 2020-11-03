# basis-assignment

Frontend Developer Assignment for getbasis.co

Deploy link - https://basis.netlify.app/

flow -->

1. User enters phone number (validation is done)
2. Phone number is sent to backend to get the token (on success token is saved on local storage)
3. if success notification for otp sent appears
4. OTP component appears to enter the OTP, validation is done to check the OTP format before sending to backend
5. Entered OTP with token is sent to backend
6. If OTP is wrong , No. of attmpts remaining is shown on screen
7. after 3 unsuccessful attempts the user is promted to enter the number again
   Please Note: I tried hitting the resend OTP endpoint, but even after successfully sending the top all over again, the verify top route was showing "You ran out of OTP attempts! Please start over." So I started the process all over again by generating a new token
8. If OTP is successfully verified Signup screen appears if isLogin is false else user data and id is stored in local storage and user is promted with the profile page (token is also changed with the new one)
   Please Note: Home page is public na dProfile is private, authentication is in place for both in route management
9. validation for all feilds firstName, LastName, email, reference code is done, Phone number is taken from the local storage
10. reference code is checked from the API route onBlur and on submit events
11. next notification comes for succesfull token sent to email id
12. verify code screen appears, (validation is done for code format)
13. code is sent to backened with token and email id, if error, error notification comes, after three unsuccessful attempts user is forced to start again, hitting the resent link was giving the same problem as for the OTP part
14. on success user data obeject is saved in local storage and also token is changed and the user is promted with profile page
15. in profile page user can update his / her first anme or last Name, for which backend update profile route is hit ith authorization bearer token as given in the problem statement
16. on signout logout orute is hit in backend ith the same authorization in header as abobve, if success user successfully logs out of the system and notification is shown, else error notification comes with the proper error message.

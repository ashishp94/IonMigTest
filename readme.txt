Page Inventory

+ CREATE ACCOUNT
      - Login
      - Terms and Condition
      - Username and Password
      - Profile

+ HOME
      - Initial Screen
      - Prescriptions: Home (Reminders & Meds List)
      - Reminder

+ HEALTH
      - Prescriptions: Add
      - Prescriptions: Details
      - Prescriptions: List
      - Prescriptions: Frequency (modal)

+ IOP
      - IOP: Home
      - IOP: New Reading

+ ACTIVITIES
      - Activities: Home
      - Activities: Detail
      

//========================================================================================


SVN URL
https://DH62YV52:8443/svn/glaucoma

Username: alaan
Password: Sheep 12
Server name: dh62yv52


//========================================================================================


STARTING A PROJECT

$ ionic start glaucoma sidemenu
$ cd EP.Mobile.Emp

$ ionic platform add android
$ ionic build android
$ ionic emulate android

$ ionic platform add ios
$ ionic build ios
$ ionic emulate ios


$ ionic serve



//========================================================================================



TESTING IN BROWSER

When you run/test in browser, you may have "same origin policy" error.
workaround is to open the brower like below.

Chrome in mac
$ open -a Google\ Chrome --args --disable-web-security

Chrome in window
chrome.exe --disable-web-security



//========================================================================================


// EMULATION

Syntax to select the device to emulate:
$ ionic emulate ios --target="iPhone-4s"

To find out available emulations I run this:
$ ios-sim showdevicetypes

This command will return a list something like this:

iPhone-4s, 8.4
iPhone-5, 8.4
iPhone-5s, 8.4
iPhone-6-Plus, 8.4
iPhone-6, 8.4
iPad-2, 8.4
iPad-Retina, 8.4
iPad-Air, 8.4
Resizable-iPhone, 8.4
Resizable-iPad, 8.4



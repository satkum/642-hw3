Attack A: Cookie Theft
=======================
When displaying the error, the profile page displays whatever html we send as the username parameter. So, in this attack, the javascript to read the cookies and send to the steal_cookie api along with the css to hide the red error bar in the error page is sent at the username GET parameter.

Attack B: Cross-Site Request Forgery
=====================================
Since the post transfer api doesn;t have any CSRF protection, in the attack the attack page uses a pre-populated transfer form to transfer 10 bitbars to the attacker and submits it before redirecting to the class web page.

Attack C: Clickjacking
======================
In this attack, the framebusting code of the protected_transfer page is busted by registering a handler for the onbeforeunload event. Once the user cancels the navigation and stays at the attack page, and clicks the 'Request Invite' button which is below the invisible 'Transfer' button, 10 bitbars are transferred to the attacker and the handler watching for the iframe reload, redirects to the class web page.

Attack D: Profile Worm
======================
The profile page has vulnerable JS code where it evals the class name value of the DOM with the id 'bitbars'. Hence in this attack, the javascript to transfer 1 bitbar from the logged in user to the attacker and to set the worm as the victim's profile, is inserted as the value for the h3 element with the id 'bitbars' and the witty message.

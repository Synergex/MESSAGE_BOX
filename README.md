# Message_Box<br />
**Created Date:** 2/24/2020<br />
**Last Updated:** 2/24/2020<br />
**Description:** To process messages in synergy code and put the MSG_BOX in center of active synergy Window regardless of the size of the synergy window and MSG_BOX<br />
**Platforms:** Windows; Unix; OpenVMS<br />
**Products:** Synergy DBL<br />
**Minimum Version:** 9.1<br />
**Author:** Geoff Maccue
<hr>

**Additional Information:** Std code or UI-Toolkit compatible. See MESSAGE_BOX.TXT for complete information.
Subroutine: MESSAGE_BOX

To process messages in synergy code and put the MSG_BOX in center of active synergy Window
regardless of the size of the synergy window and MSG_BOX. Std code or UI-Toolkit compatible.

Supports: Up to 5 lines of message text
Up to 5 Buttons (Programmable and Configurable)
Buttons can have Tool Tips and can set default Button
Active Character for firing a Button by pressing First character of Button Text
Default Button can be configured for when user presses Enter
Works in DBL and UI-Toolkit programs
Can accommodate use of Function Keys
Can configure which Function Keys are permitted
User can reposition MSG_BOX to view data behind by dragging the MSG_BOX window
If user repositions MSG_BOX then next similar MSG instance will be at new position.
Dissimilar messages will revert to center of window
Works equally well in BATCH mode (BATCH environment variable set to B)
In Batch does not pause for input but returns a predefined value.
Can capture all function keys
F1 - F12 Normal Function Keys
SF1 - SF12 Shift Function Keys
CF1 - CF12 Ctrl Function Keys
Programmer can nominate which Function keys are permitted
Has timeout variable (in seconds) Or can wait forever for user input.


Min Version: 9 Synergy

Limitation: u_start will clear active channels (currently set to clear 250 - 253)
If old style code using OPEN (TTCHN,O,'TT:') u_start can potentially
close terminal channel.

Can be used in old style DBL code

OPEN (TT,O,'TT:')
XCALL MESSAGE_BOX

and in UT-Toolkit code

U_Start
XCALL MESSAGE_BOX

Provided in code exchange
1. This readme
2. Subroutine MESSAGE_BOX.DBL
3. Demo Program DEMO_MESSAGE_BOX.DBL

#Launching Applications and Session Management using the Self Service Plug-in (SSP)

All the following commands are called on SelfService.exe, which is
located in `%CitrixReceiverInstalllocation%\SelfServicePlugin`

Note that command-line parameters are case-sensitive.

##-qlaunch &lt;application friendly name&gt;

This command launches a named application by its friendly name. If the
application is already running it will automatically reconnect it.

This replaces pnagent.exe /CitrixShortcut: (2) /QLaunch "ACME:Wordpad"

##–qlogon

This command gets the user’s credentials from SSO and reconnects any
active user sessions.

Use `–fastterminate` or `–terminate` first if a different user is logged on.

##-terminate

This command disconnects all current users’ applications and exits.

This replaces `pnagent /terminate`

##-fastterminate

This command logs off the current user and leaves their applications
connected. This is for use in shared endpoint scenarios.

##-terminateuser &lt;user&gt;

This command disconnects a specific user’s applications and exits.



# XignCode3 bypass
A host-based emulator bypass for Wellbia's XignCode3.

Emulates the integrity-check for XignCode3 through a host-application.

* A host application launches and initializes XignCode3, causing XignCode3 to run its anti-hack analysis routines in the scope of that particular parent process. As a result, any attempt at attacking the original application will remain undetected by XignCode3.
* A client application hooks into the XignCode3 files (and exports), forwarding all integry-check requests to the host-application through a local socket in order to generate correct integrity-check responses.

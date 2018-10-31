# zer0cks
Xerox WorkCentre printer cloning.dlm password decryption

![alt text](https://github.com/billchaison/zer0cks/blob/master/xrx.png)

The information presented in this article can be used as a recovery method for passwords stored in Xerox WorkCentre backup files (cloning.dlm).  The ability to retrieve passwords from the cloning.dlm file may be useful for organizations that have forgotten or are using undocumented service credentials where resetting the password centrally would create an operational hardship.  Password recovery from the cloning.dlm file (whether downloaded directly from the printer or discovered in a backup folder) would also be useful for pentesters, allowing them to gain access to other systems where those credentials are used.

Xerox WorkCentre printer configs can be exported as a file called cloning.dlm from the device's web interface by an administrative user.  You must be able to access the printer as admin, the default password is "1111", but may have been changed.  Xerox WorkCentre printers support scan to folder and email functions, which means that LDAP, SMB and SMTP credentials, among others, should be recoverable.

The Xerox DLM file format was disclosed by Deral Heiland (PercX) in an August 2011 article entitled "From Printer to Pwned" and again in a February 2013 article entitled "From Patched to Pwned" found here:

http://foofus.net/goons/percx/defcon/P2PWND.pdf

http://foofus.net/goons/percx/Xerox_hack.pdf

The cloning.dlm password decryption procedure resides under a protected repository in my BitBucket

https://bitbucket.org/billchaison/zer0cks

The procedure has been tested successfully on the following WorkCentre models: 7225, 7530, 7535, 7545, 7556, 7830, 7855, 5945, 5955, 5745, 5755, 6655, 5632 and 5638.

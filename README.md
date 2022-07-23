# pntify
### PaiNT notIFY or Paint NoTIFY
This is a script, written in POSIX compliant shell script, that fetches notifications and alerts from [3DSPaint](https://3dspaint.com)/[DSiPaint](https://dsipaint.com) (\*Paint) and outputs them to STDOUT.  It is meant to be used in other scripts, for things like statusbar modules, etc., but it could also just be used as a lightweight way to access \*Paint notifications if you're too lazy to open a browser.

As it *is* POSIX compliant shell script, it can be used on any system with a POSIX compliant shell installed.  That being said, there are some external dependencies:

## Dependencies
 - *Coreutils* - You probably already have these on a \*nix system.  They don't have to necessarily be the GNU Coreutils.
 - *Curl* - You probably also have this already installed.

## Optional Dependencies
 - *[GNU Privacy Guard (GPG)](https://gnupg.org/)* - Encryption software.
 - *[pass](https://www.passwordstore.org/)* - A CLI password manager that uses GPG to encrypt passwords.  Used for storing credentials if installed.

Installing the optional dependencies is highly recommended, though not required.  If they are not installed, credentials will be stored in plaintext, and viewable by anybody with access to your system.  If you still wish to continue running this script like this, use the -i option.

# THIS IS INCOMPLETE.  I'VE GOTTEN THIS TO A FUNCTIONAL, ALTHOUGH UNFEATUREFUL STATE.  THIS REALLY CAN'T DO MUCH ATM OTHER THAN LOG IN, AND DISPLAY YOUR MESSAGE COUNT.

pinentry-auto
=============

Automatically sends pin to programs getting a pin via pin-entry. This is sometimes necessary.

Mainly, this is used as a pinentry replacement for GnuPG when used in combination with an OpenPGP smartcard (such as the crypto-stick).

For automatic signing, the PIN can be cached by gpg-agent, but will be cleared on reboot. For purposes where this is fully automated, it makes sense to use an OpenPGP smartcard so that the secret key can never be extracted.

However, storing the PIN in the gpg-agent memory "forever" is neither convenient (have to insert it again on reboot), neither is it safer.

USAGE
=====

Simply drop this script in /usr/local/bin and change your gpg configuration file to point to it. Don't forget to add a real PIN, too. 123456 is the default user PIN on most OpenPGP smartcards.

# FreeBSD + Asterisk VoIP Lab Screenshots

This folder contains a curated set of safe screenshots for GitHub documentation. The files demonstrate encrypted voice calling, IVR interaction, custom prompt testing, and voicemail access without showing personal identities or credentials.

| Screenshot filename | Description | Evidence shown |
|---|---|---|
| `01-zrtp-voice-call-test.png` | Linphone mobile call to extension 6003 with a 30-second call duration. | Shows an active voice call and the explicit “End-to-end encrypted by ZRTP” status. |
| `02-encrypted-desktop-call-test.png` | Linphone desktop/tablet call between extensions 6002 and 6003. | Shows an established 21-second end-to-end encrypted extension call. |
| `03-ivr-menu-call-test.png` | Linphone call to IVR extension 700. | Shows a 30-second IVR call with ZRTP end-to-end encryption. |
| `04-custom-ivr-prompt-call.png` | Linphone call to custom prompt test extension 701. | Shows an active seven-second call used to test custom IVR prompt playback. |
| `05-ivr-dtmf-input-test.png` | Linphone keypad displayed during the extension 701 test call. | Shows in-call DTMF interaction with `#` entered for IVR control testing. |
| `06-voicemail-access-test.png` | Linphone call to voicemail access code `*97`. | Shows an active 38-second voicemail-system access call without exposing a mailbox PIN. |

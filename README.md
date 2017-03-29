irssi-pushsafer
==============

Plugin for irssi (a console based IRC client) to send push-notifications using pushsafer.com.

This allows you to be notified when someone messages/mentions you on IRC, 
when you're not online.


# Installation

  0. Add a new application to your pushsafer control panel, note the API key.
  1. cp pushsafer.pl to ~/.irssi/scripts/ and symlink into scripts/autorun if you desire.
  2. touch ~/.irssi/pushsafer_ignores
  2. Within irssi: 
    1. /load autorun/pushsafer.pl
    2. /set pushsafer_key <<your pushsafer private or alias key>>
	3. optional set the following params > https://www.pushsafer.com/en/pushapi
	4. /set pushsafer_device <<device or device group id>>
    5. /set pushsafer_sound <<sound number>>
	6. /set pushsafer_icon <<icon number>>
	7. /set pushsafer_vibration <<vibration 0-3>>
	8. /set pushsafer_url <<optional url>>
	9. /set pushsafer_urltitle <<optional url title>>
	10. /set pushsafer_time2live <<number 0-43200 time in minutes, after which message automatically gets purged>>
    11. /save
    12. /pushtest hello world. (sends test message to your device(s)).


# Dependencies

  0. A pushsafer.com Account
  1. Crypt::SSLeay / libcrypt-ssleay-perl is installed 

# Other things 

  0. /set pushsafer_debug 1 - should make it verbose.
  1. /set pushsafer_ignore 1 - turn on ignore configurability
  2. /set pushsafer_ignorefile - ignore messages from ....
  3. /set pushsafer_ignorechannels - space separated list of channels to ignore.
  4. /pushignore help - should get you started in populating the ignore list.
  5. /set pushsafer_only_if_away [on|off] - if set to on, then you'll 
        need to be set to away before we send notifications.

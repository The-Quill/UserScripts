# User Scripts


This repository contains various [Tampermonkey](http://tampermonkey.net/) user scripts that add features to the review queue or to the chat room.

## SO Close Vote Request Generator
This script sends a `[tag:cv-pls]` message to the site's chatroom for the post you are currently viewing. It works on `*.stackexchange.com` and `*.stackoverflow.com` at the moment.

###Installation
To install this script [click here](https://rawgit.com/SO-Close-Vote-Reviewers/UserScripts/master/SECloseVoteRequestGenerator.user.js) or otherwise visit the following URL, and GreaseMonkey/TamperMonkey should ask you to install it.

     https://rawgit.com/SO-Close-Vote-Reviewers/UserScripts/master/SECloseVoteRequestGenerator.user.js
     
###Updating
This script has an auto-update feature. It will check for a new version every time the script is run, don't worry it is a very lightweight request.

To update manually you can visit the above URL again, or select <kbd>Check for updates</kbd> from the <kbd>cv-pls</kbd> menu.

###Target Chat Room
The default chat room is [SO Close Vote Reviewers](http://chat.stackoverflow.com/rooms/41570/so-close-vote-reviewers). When you change the target chat room, it will save the change for that site. Per-site metas and Stack Exchange sub domains will all be able to have their own setting.

The room URL that you enter into the prompt *must* be a valid chatroom URL. The script *will* yell at you if it is not. 

1. Select <kbd>Set Room</kbd> from the <kbd>cv-pls</kbd> menu (located in the post menu)
2. Paste the URL of the target room into the dialog.
  * The default room is SO Close Vote Reviewers.

###Sending Requests
Requests generated by this script will be in the following format:

    [tag:cv-pls] reason [title](url) - [user](url) time
    
They can also be sent whether you are in the target room or not, as long as you have write access. 

1. To open the reason prompt you can either:
  *  Press <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>a</kbd>
  *  Or select <kbd>Send request</kbd> from the <kbd>cv-pls</kbd> menu.
2. Enter your reason into the prompt
  *  Any markdown that is acceptable in chat is acceptable in the reason dialog.
3. Click <kbd>OK</kbd> on the prompt or press <kbd>enter</kbd> on your keyboard to submit the request. 
  * Clicking on the <kbd>X</kbd> or <kbd>Cancel</kbd> in the dialog will cancel the request.

###Short Reasons
This script has a short reason replacement feature. Basically what this means is that if you submit a one-letter reason and it matches a predefined short reason, the script will replace that letter with its corresponding reason.
* `t: too broad` 
* `u: unclear`
* `p: pob`
* `d: duplicate`
* `m: no mcve`
* `r: no repro`
* `s: superuser`
* `f: serverfault`

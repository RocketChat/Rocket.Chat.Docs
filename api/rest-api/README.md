# REST API

The REST API allows you to control and extend Rocket.Chat with ease.

> **This API is a work in progress, so feel free to test, ask us questions, and submit Pull Requests!**

If you are an end-user and not a dev or a tester, [create a New Feature Request](https://forums.rocket.chat/c/feature-requests) to request new APIs -- and consider [making a donation](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=ZL94ZE6LGVUSN) to the project.

> All API calls in the documentation are made using `curl`. However, you are free to use Java / Python / PHP / Golang / Ruby / Swift / Objective-C / Rust / Scala / C\# or any other programming languages.

## Production Security Concerns

When calling a production Rocket.Chat server, ensure it is running via HTTPS and has a valid SSL Certificate. The login method requires you to post your username and password in plaintext, which is why we highly suggest only calling the REST login API over HTTPS. Also, few things to note:

* Only call via HTTPS
* Implement a timed authorization token expiration strategy
* Ensure the calling user only has permissions for what they are calling and no more

### Miscellaneous Information

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/info` | Information about the Rocket.Chat server. | [Link](methods/miscellaneous/info.md) |
| `/api/v1/directory` | Search by all users and channels available on server. | [Link](methods/miscellaneous/directory.md) |
| `/api/v1/shield.svg` | Gets the shield svg\(badge\) to add in your website. | [Link](methods/miscellaneous/shield-svg.md) |
| `/api/v1/spotlight` | Searches for users or rooms that are visible to the user. | [Link](methods/miscellaneous/spotlight.md) |
| `/api/v1/statistics` | Statistics about the Rocket.Chat server. | [Link](methods/miscellaneous/statistics.md) |
| `/api/v1/statistics.list` | Selectable statistics about the Rocket.Chat server. | [Link](methods/miscellaneous/statistics-list.md) |
| `/api/v1/instances.get` | Gets all running instances. | [Link](https://github.com/RocketChat/docs/tree/06af028aecca9430169baa3f517704a68deb6278/api/rest-api/methods/miscellaneous/instances-get.md) |

### Assets

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/assets.setAsset` | Set an asset image by name. | [Link](methods/assets/setasset.md) |
| `/api/v1/assets.unsetAsset` | Unset an asset by name | [Link](methods/assets/unsetasset.md) |

### AutoTranslate

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/autotranslate.getSupportedLanguages` | Get the supported languages by the autotranslate. | [Link](methods/autotranslate/getsupportedlanguages.md) |
| `/api/v1/autotranslate.saveSetttings` | Save some settings about autotranslate. | [Link](methods/autotranslate/savesettings.md) |
| `/api/v1/autotranslate.translateMessage` | Translate the message. | [Link](methods/autotranslate/translatemessage.md) |

### Authentication

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/login` | Authenticate with the REST API. | [Link](methods/authentication/login.md) |
| `/api/v1/login` | Authenticate with google. | [Link](methods/authentication/google.md) |
| `/api/v1/login` | Authenticate with facebook. | [Link](methods/authentication/facebook.md) |
| `/api/v1/login` | Authenticate with twitter. | [Link](methods/authentication/twitter.md) |
| `/api/v1/logout` | Invalidate your REST API authentication token. | [Link](methods/authentication/logout.md) |
| `/api/v1/me` | Displays information about the authenticated user. | [Link](methods/authentication/me.md) |

### Users

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/users.presence` | Gets all connected users presence. | [Link](methods/users/presence.md) |
| `/api/v1/users.create` | Create a new user. | [Link](methods/users/create.md) |
| `/api/v1/users.createToken` | Create a user authentication token. | [Link](methods/users/createtoken.md) |
| `/api/v1/users.deactivateIdle` | Deactivate idle users. | [Link](methods/users/deactivateidle.md) |
| `/api/v1/users.delete` | Deletes an existing user. | [Link](methods/users/delete.md) |
| `/api/v1/users.deleteOwnAccount` | Deletes your own user. | [Link](methods/users/deleteownaccount.md) |
| `/api/v1/users.forgotPassword` | Send email to reset your password. | [Link](methods/users/forgotpassword.md) |
| `/api/v1/users.generatePersonalAccessToken` | Generate Personal Access Token. | [Link](methods/users/generatepersonalaccesstoken.md) |
| `/api/v1/users.getAvatar` | Gets the URL for a user's avatar. | [Link](methods/users/getavatar.md) |
| `/api/v1/users.getPersonalAccessTokens` | Gets the user's personal access tokens. | [Link](methods/users/getpersonalaccesstokens.md) |
| `/api/v1/users.getPreferences` | Gets all preferences of user. | [Link](methods/users/get-preferences.md) |
| `/api/v1/users.getPresence` | Gets the online presence of a user. | [Link](methods/users/getpresence.md) |
| `/api/v1/users.getStatus` | Gets the user's status. | [Link](methods/users/getstatus.md) |
| `/api/v1/users.getUsernameSuggestion` | Gets a suggestion a new username to user. | [Link](methods/users/getusernamesuggestion.md) |
| `/api/v1/users.info` | Gets a user's information, limited to the caller's permissions. | [Link](methods/users/info.md) |
| `/api/v1/users.list` | All of the users and their information, limited to permissions. | [Link](methods/users/list.md) |
| `/api/v1/users.regeneratePersonalAccessToken` | Regenerate a user personal access token. | [Link](methods/users/regeneratepersonalaccesstoken.md) |
| `/api/v1/users.register` | Register a new user. | [Link](methods/users/register.md) |
| `/api/v1/users.removeOtherTokens` | Remove all other user tokens | [Link](methods/users/removeothertokens.md) |
| `/api/v1/users.removePersonalAccessToken` | Remove a personal access token. | [Link](methods/users/removepersonalaccesstoken.md) |
| `/api/v1/users.requestDataDownload` | Request users download data. | [Link](methods/users/requestdatadownload.md) |
| `/api/v1/users.resetAvatar` | Reset a user's avatar | [Link](methods/users/resetavatar.md) |
| `/api/v1/users.setAvatar` | Set a user's avatar | [Link](methods/users/setavatar.md) |
| `/api/v1/users.setPreferences` | Set user's preferences | [Link](methods/users/set-preferences.md) |
| `/api/v1/users.setStatus` | Set the user's status | [Link](methods/users/setstatus.md) |
| `/api/v1/users.setActiveStatus` | Set a user's active status. | [Link](methods/users/setactivestatus.md) |
| `/api/v1/users.update` | Update an existing user. | [Link](methods/users/update.md) |
| `/api/v1/users.updateOwnBasicInfo` | Update basic information of own user. | [Link](methods/users/updateownbasicinfo.md) |

### Channels

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/channels.addAll` | Adds all of the users on the server to a channel. | [Link](methods/channels/addall.md) |
| `/api/v1/channels.addLeader` | Gives the role of Leader for a user in the current channel. | [Link](methods/channels/addleader.md) |
| `/api/v1/channels.addOwner` | Gives the role of owner for a user in the current channel. | [Link](methods/channels/addowner.md) |
| `/api/v1/channels.anonymousread` | Gets the messages in public channels to an anonymous user | [Link](methods/channels/anonymousread.md) |
| `/api/v1/channels.archive` | Archives a channel. | [Link](methods/channels/archive.md) |
| `/api/v1/channels.close` | Removes a channel from a user's list of channels. | [Link](methods/channels/close.md) |
| `/api/v1/channels.counters` | Gets channel counters. | [Link](methods/channels/counters.md) |
| `/api/v1/channels.create` | Creates a new channel. | [Link](methods/channels/create.md) |
| `/api/v1/channels.delete` | Removes a channel. | [Link](methods/channels/delete.md) |
| `/api/v1/channels.files` | Gets a list of files from a channel. | [Link](methods/channels/files.md) |
| `/api/v1/channels.getAllUserMentionsByChannel` | Gets all the mentions of a channel. | [Link](methods/channels/getallusermentionsbychannel.md) |
| `/api/v1/channels.getIntegrations` | Gets the channel's integration. | [Link](methods/channels/getintegrations.md) |
| `/api/v1/channels.history` | Retrieves the messages from a channel. | [Link](methods/channels/history.md) |
| `/api/v1/channels.info` | Gets a channel's information. | [Link](methods/channels/info.md) |
| `/api/v1/channels.invite` | Adds a user to a channel. | [Link](methods/channels/invite.md) |
| `/api/v1/channels.join` | Joins yourself to a channel. | [Link](methods/channels/join.md) |
| `/api/v1/channels.kick` | Removes a user from a channel. | [Link](methods/channels/kick.md) |
| `/api/v1/channels.leave` | Removes the calling user from a channel. | [Link](methods/channels/leave.md) |
| `/api/v1/channels.list` | Retrieves all of the channels from the server. | [Link](methods/channels/list.md) |
| `/api/v1/channels.list.joined` | Gets only the channels the calling user has joined. | [Link](methods/channels/list-joined.md) |
| `/api/v1/channels.members` | Retrieves all channel users. | [Link](methods/channels/members.md) |
| `/api/v1/channels.messages` | Retrieves all channel messages. | [Link](methods/channels/messages.md) |
| `/api/v1/channels.moderators` | List all moderators of a channel. | [Link](methods/channels/moderators.md) |
| `/api/v1/channels.online` | List all online users of a channel. | [Link](methods/channels/online.md) |
| `/api/v1/channels.open` | Adds the channel back to the user's list of channels. | [Link](methods/channels/open.md) |
| `/api/v1/channels.removeleader` | Removes the role of Leader for a user in the current channel. | [Link](methods/channels/removeleader.md) |
| `/api/v1/channels.rename` | Changes a channel's name. | [Link](methods/channels/rename.md) |
| `/api/v1/channels.roles` | Gets the user's roles in the channel. | [Link](methods/channels/roles.md) |
| `/api/v1/channels.setCustomFields` | Sets a channel's custom fields. | [Link](methods/channels/setcustomfields.md) |
| `/api/v1/channels.setAnnouncement` | Sets a channel's announcement. | [Link](methods/channels/setannouncement.md) |
| `/api/v1/channels.setDefault` | Sets whether a channel is a default channel or not. | [Link](methods/channels/setdefault.md) |
| `/api/v1/channels.setDescription` | Sets a channel's description. | [Link](methods/channels/setdescription.md) |
| `/api/v1/channels.setJoinCode` | Sets the channel's code required to join it. | [Link](methods/channels/setjoincode.md) |
| `/api/v1/channels.setPurpose` | Sets a channel's description. | [Link](methods/channels/setpurpose.md) |
| `/api/v1/channels.setReadOnly` | Sets whether a channel is read only or not. | [Link](methods/channels/setreadonly.md) |
| `/api/v1/channels.setTopic` | Sets a channel's topic. | [Link](methods/channels/settopic.md) |
| `/api/v1/channels.setType` | Sets the type of room the channel should be. | [Link](methods/channels/settype.md) |
| `/api/v1/channels.unarchive` | Unarchives a channel. | [Link](methods/channels/unarchive.md) |
| `/api/v1/channels.addOwner` | Gives the role of owner for a user in the current channel. | [Link](methods/channels/addowner.md) |
| `/api/v1/channels.removeOwner` | Removes the role of owner from a user in the current channel. | [Link](methods/channels/removeowner.md) |

### Groups

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/groups.archive` | Archives a private group. | [Link](methods/groups/archive.md) |
| `/api/v1/groups.addLeader` | Gives the role of Leader for a user in the current group. | [Link](methods/groups/addleader.md) |
| `/api/v1/groups.close` | Removes a private group from the list of groups. | [Link](methods/groups/close.md) |
| `/api/v1/groups.counters` | Gets group counters. | [Link](methods/groups/counters.md) |
| `/api/v1/groups.create` | Creates a new private group. | [Link](methods/groups/create.md) |
| `/api/v1/groups.delete` | Removes a private group. | [Link](methods/groups/delete.md) |
| `/api/v1/groups.files` | Gets a list of files from a private group. | [Link](methods/groups/files.md) |
| `/api/v1/groups.history` | Retrieves the messages from a private group. | [Link](methods/groups/history.md) |
| `/api/v1/groups.info` | Gets the information about a private group. | [Link](methods/groups/info.md) |
| `/api/v1/groups.invite` | Adds a user to the private group. | [Link](methods/groups/invite.md) |
| `/api/v1/groups.kick` | Removes a user from a private group. | [Link](methods/groups/kick.md) |
| `/api/v1/groups.leave` | Removes the calling user from the private group. | [Link](methods/groups/leave.md) |
| `/api/v1/groups.list` | List the private groups the caller is part of. | [Link](methods/groups/list.md) |
| `/api/v1/groups.listAll` | List all the private groups. | [Link](methods/groups/listall.md) |
| `/api/v1/groups.members` | Gets the users of participants of a private group. | [Link](methods/groups/members.md) |
| `/api/v1/groups.messages` | Retrieves all group messages. | [Link](methods/groups/messages.md) |
| `/api/v1/groups.moderators` | List all moderators of a group. | [Link](methods/groups/moderators.md) |
| `/api/v1/groups.online` | List all online users of a group. | [Link](https://github.com/RocketChat/docs/tree/aeb4dd8de5017b7cd9c9d9367a0e2155f911ba5a/api/rest-api/methods/groups/online.md) |
| `/api/v1/groups.open` | Adds the private group back to the list of groups. | [Link](methods/groups/open.md) |
| `/api/v1/groups.removeLeader` | Removes the role of Leader for a user in the current group. | [Link](methods/groups/removeleader.md) |
| `/api/v1/groups.rename` | Changes the name of the private group. | [Link](methods/groups/rename.md) |
| `/api/v1/groups.roles` | Gets the user's roles in the private group. | [Link](methods/groups/roles.md) |
| `/api/v1/groups.setAnnouncement` | Sets a group's announcement. | [Link](methods/groups/setannouncement.md) |
| `/api/v1/groups.setCustomFields` | Sets private group's custom fields. | [Link](methods/groups/setcustomfields.md) |
| `/api/v1/groups.setDescription` | Sets a private group's description. | [Link](methods/groups/setdescription.md) |
| `/api/v1/groups.setPurpose` | Sets a private group's description. | [Link](methods/groups/setpurpose.md) |
| `/api/v1/groups.setReadOnly` | Sets whether the room is read only or not. | [Link](methods/groups/setreadonly.md) |
| `/api/v1/groups.setTopic` | Sets a private group's topic. | [Link](methods/groups/settopic.md) |
| `/api/v1/groups.setType` | Sets the type of room this group will be. | [Link](methods/groups/settype.md) |
| `/api/v1/groups.unarchive` | Unarchives a private group. | [Link](methods/groups/unarchive.md) |
| `/api/v1/groups.addOwner` | Gives the role of owner for a user in the current group. | [Link](methods/groups/addowner.md) |
| `/api/v1/groups.removeOwner` | Removes the role of owner from a user in the current Group. | [Link](methods/groups/removeowner.md) |

### Chat

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/chat.delete` | Deletes an existing chat message. | [Link](methods/chat/delete.md) |
| `/api/v1/chat.followMessage` | Follows an existing chat message. | [Link](methods/chat/followmessage.md) |
| `/api/v1/chat.getDeletedMessages` | Retrieves the deleted messages since specific date. | [Link](methods/chat/getdeletedmessages.md) |
| `/api/v1/chat.getDiscussions` | Retrieves the discussions messages of a room. | [Link](methods/chat/getdiscussions.md) |
| `/api/v1/chat.getMentionedMessages` | Retrieves mentioned messages. | [Link](methods/chat/getmentionedmessages.md) |
| `/api/v1/chat.getMessage` | Retrieves a single chat message. | [Link](methods/chat/getmessage.md) |
| `/api/v1/chat.getMessageReadReceipts` | Retrieves message read receipts. | [Link](methods/chat/getmessagereadreceipts.md) |
| `/api/v1/chat.getPinnedMessages` | Retrieve pinned messages from a room. | [Link](methods/chat/getpinnedmessages.md) |
| `/api/v1/chat.getSnippetedMessages` | Retrieves snippeted messages. | [Link](methods/chat/getsnippetedmessages.md) |
| `/api/v1/chat.getSnippetedMessageById` | Retrieves snippeted message by id. | [Link](methods/chat/getsnippetedmessagebyid.md) |
| `/api/v1/chat.getStarredMessages` | Retrieves starred messages. | [Link](methods/chat/getstarredmessages.md) |
| `/api/v1/chat.getThreadMessages` | Retrieves thread's messages. | [Link](methods/chat/getthreadmessages.md) |
| `/api/v1/chat.getThreadsList` | Retrieves channel's threads. | [Link](methods/chat/getthreadslist.md) |
| `/api/v1/chat.ignoreUser` | Ignores an user from a chat. | [Link](methods/chat/ignoreuser.md) |
| `/api/v1/chat.pinMessage` | Pins a chat message to the message's channel. | [Link](methods/chat/pinmessage.md) |
| `/api/v1/chat.postMessage` | Posts a new chat message. | [Link](methods/chat/postmessage.md) |
| `/api/v1/chat.react` | Sets/unsets the user's reaction to an existing chat message. | [Link](methods/chat/react.md) |
| `/api/v1/chat.reportMessage` | Reports a message. | [Link](methods/chat/reportmessage.md) |
| `/api/v1/chat.search` | Search for messages in a channel. | [Link](methods/chat/search.md) |
| `/api/v1/chat.starMessage` | Stars a chat message for the authenticated user. | [Link](methods/chat/starmessage.md) |
| `/api/v1/chat.sendMessage` | Send new chat message. | [Link](methods/chat/sendmessage.md) |
| `/api/v1/chat.syncThreadMessages` | Retrieves synced thread's messages. | [Link](methods/chat/syncthreadmessages.md) |
| `/api/v1/chat.syncThreadsList` | Retrieves thread's synced channel threads. | [Link](methods/chat/syncthreadslist.md) |
| `/api/v1/chat.unfollowMessage` | Unfollows an existing chat message. | [Link](methods/chat/unfollowmessage.md) |
| `/api/v1/chat.unPinMessage` | Removes the pinned status of the provided chat message. | [Link](methods/chat/unpinmessage.md) |
| `/api/v1/chat.unStarMessage` | Removes the star on the chat message for the authenticated user. | [Link](methods/chat/unstarmessage.md) |
| `/api/v1/chat.update` | Updates the text of the chat message. | [Link](methods/chat/update.md) |

### Custom Sounds

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/custom-sounds.list` | Retrieves a list of custom sounds. | [Link](methods/custom-sounds/list.md) |

### IM

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/im.close` | Removes a direct message from the list of direct messages. | [Link](methods/im/close.md) |
| `/api/v1/im.counters` | Gets counters of direct messages. | [Link](methods/im/counters.md) |
| `/api/v1/im.create` | Create a direct message session with another user. | [Link](methods/im/create.md) |
| `/api/v1/im.history` | Retrieves the messages from a direct message. | [Link](methods/im/history.md) |
| `/api/v1/im.files` | Retrieves a list of files from a direct message. | [Link](methods/im/files.md) |
| `/api/v1/im.members` | Retrieves the users of participants of a direct message. | [Link](methods/im/members.md) |
| `/api/v1/im.messages` | Retrieves the messages from specific direct message. | [Link](methods/im/messages.md) |
| `/api/v1/im.messages.others` | Retrieves the messages from any direct message in the server. | [Link](methods/im/messages-others.md) |
| `/api/v1/im.list` | List the direct messages the caller is part of. | [Link](methods/im/list.md) |
| `/api/v1/im.list.everyone` | List all direct message the caller in the server. | [Link](methods/im/list-everyone.md) |
| `/api/v1/im.open` | Adds the direct message back to the list of direct messages. | [Link](methods/im/open.md) |
| `/api/v1/im.setTopic` | Sets a direct message topic. | [Link](methods/im/settopic.md) |

### Integrations

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/integrations.create` | Creates an integration. | [Link](methods/integration/create.md) |
| `/api/v1/integrations.get` | Gets an integration. | [Link](methods/integration/get.md) |
| `/api/v1/integrations.history` | Lists all history of the specified integration. | [Link](methods/integration/history.md) |
| `/api/v1/integrations.list` | Lists all of the integrations. | [Link](methods/integration/list.md) |
| `/api/v1/integrations.remove` | Removes an integration. | [Link](methods/integration/remove.md) |

### Invites

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/findOrCreateInvite` | Created a new Invite or returns an existing one with the same parameters. | [Link](methods/invites/findorcreateinvite.md) |
| `/api/v1/listInvites` | Lists all of the invite tokens. | [Link](methods/invites/listinvites.md) |
| `/api/v1/removeInvite` | Removes an invite. | [Link](methods/invites/removeinvite.md) |
| `/api/v1/useInviteToken` | Report to the server that an invite token was used. | [Link](methods/invites/useinvitetoken.md) |
| `/api/v1/validateInviteToken` | Checks if an invite token is valid. | [Link](methods/invites/validateinvitetoken.md) |

### Livechat

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/livechat/inquiries.list` | Retrieves a list of open inquiries. | [Link](methods/livechat/inquiries.md#inquiries-list) |
| `/api/v1/livechat/inquiries.take` | Take an open inquiry. | [Link](methods/livechat/inquiries.md#livechat-take-inquiry) |
| `/api/v1/livechat/rooms` | Retrieves a list of livechat rooms. | [Link](methods/livechat/rooms.md) |

### OAuthApps

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/oauth-apps.get` | Retrieves an OAuth App by id or client id. | [Link](methods/oauthapps/get.md) |
| `/api/v1/oauth-apps.list` | Retrieves a list of OAuth Apps. | [Link](methods/oauthapps/list.md) |

### Permissions

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/permissions.listAll` | Lists permissions on the server. | [Link](methods/permissions/listall.md) |
| `/api/v1/permissions.update` | Edits permissions on the server. | [Link](methods/permissions/update.md) |

### Roles

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/roles.create` | Create a new role in the system. | [Link](methods/roles/create.md) |
| `/api/v1/roles.list` | Gets all the roles in the system. | [Link](methods/roles/list.md) |
| `/api/v1/roles.sync` | Gets all the roles in the system which are updated after a given date. | [Link](methods/roles/sync.md) |
| `/api/v1/roles.addUserToRole` | Assign a role to an user. | [Link](methods/roles/addusertorole.md) |
| `/api/v1/roles.removeUserFromRole` | Unassign a role from an user. | [Link](methods/roles/removeuserfromrole.md) |
| `/api/v1/roles.getUsersInRole` | Gets the users that belongs to a role. | [Link](methods/roles/getusersinrole.md) |

### Push Token

| Url | Method | Short Description | Details Page |
| :--- | :--- | :--- | :--- |
| `/api/v1/push.token` | `POST` | Saves push token. | [Link](methods/push/push-token.md) |
| `/api/v1/push.token` | `DELETE` | Removes push token. | [Link](methods/push/deletepushtoken.md) |

### Rooms

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/rooms.adminRooms` | Retrieve all rooms \(requires special permission\). | [Link](methods/rooms/adminrooms.md) |
| `/api/v1/rooms.cleanHistory` | Cleans up a room's history, requires special permission. | [Link](methods/rooms/cleanhistory.md) |
| `/api/v1/rooms.createDiscussion` | Creates a new discussion. | [Link](methods/rooms/creatediscussion.md) |
| `/api/v1/rooms.favorite` | Favorite/Unfavorite room. | [Link](methods/rooms/favorite.md) |
| `/api/v1/rooms.get` | Gets rooms. | [Link](methods/rooms/get.md) |
| `/api/v1/rooms.getDiscussions` | Gets room's discussions. | [Link](methods/rooms/getdiscussions.md) |
| `/api/v1/rooms.info` | Gets info from a room. | [Link](methods/rooms/info.md) |
| `/api/v1/rooms.leave` | Leaves a room. | [Link](methods/rooms/leave.md) |
| `/api/v1/rooms.saveNotification` | Sets the notifications settings of specific channel. | [Link](methods/rooms/savenotification.md) |
| `/api/v1/rooms.upload/:rid` | Upload a message with attached file. | [Link](methods/rooms/upload.md) |

### Command Methods

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/commands.get` | Get specification of the slash command. | [Link](methods/commands/get.md) |
| `/api/v1/commands.list` | Lists all available slash commands. | [Link](methods/commands/list.md) |
| `/api/v1/commands.run` | Execute a slash command in the specified room. | [Link](methods/commands/run.md) |

### Custom User Status

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/custom-user-status.list` | Lists all available custom user's status. | [Link](methods/custom-user-status/list.md) |

### Emoji Custom

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/emoji-custom.list` | List the custom emojis available. | [Link](methods/emoji-custom/list.md) |
| `/api/v1/emoji-custom.create` | Create new custom emoji. | [Link](methods/emoji-custom/create.md) |
| `/api/v1/emoji-custom.delete` | Delete an existent custom emoji. | [Link](methods/emoji-custom/delete.md) |
| `/api/v1/emoji-custom.update` | Update an existent custom emoji. | [Link](methods/emoji-custom/update.md) |

### Settings

| Url | Method | Short Description | Details Page |
| :--- | :--- | :--- | :--- |
| `/api/v1/settings` | `GET` | Lists all private settings. | [Link](methods/settings/get.md) |
| `/api/v1/settings.public` | `GET` | Lists all public settings. | [Link](methods/settings/public.md) |
| `/api/v1/settings.oauth` | `GET` | Return list of all available oauth services. | [Link](methods/settings/oauth.md) |
| `/api/v1/service.configurations` | `GET` | Lists all service configurations. | [Link](methods/settings/service-configuration.md) |
| `/api/v1/settings/:_id` | `GET` | Gets a setting. | [Link](methods/settings/get-by-id.md) |
| `/api/v1/settings/:_id` | `POST` | Updates a setting. | [Link](methods/settings/update.md) |

### Subscriptions

| Url | Method | Short Description | Details Page |
| :--- | :--- | :--- | :--- |
| `/api/v1/subscriptions.get` | `GET` | Get all subscriptions. | [Link](methods/subscriptions/get.md) |
| `/api/v1/subscriptions.getOne` | `GET` | Get the subscription by room Id. | [Link](methods/subscriptions/getone.md) |
| `/api/v1/subscriptions.read` | `POST` | Mark a room as read. | [Link](methods/subscriptions/read.md) |
| `/api/v1/subscriptions.unread` | `POST` | Mark messages as unread. | [Link](methods/subscriptions/unread.md) |

### Video Conference

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/video-conference/jitsi.update-timeout` | Updates the timeout of Jitsi video conference in a channel. | [Link](methods/video-conference/jitsi-update-timeout.md) |

### Webdav

| Url | Short Description | Details Page |
| :--- | :--- | :--- |
| `/api/v1/webdav.getMyAccounts` | Retrieves the user's webdav accounts. | [Link](methods/webdav/getmyaccounts.md) |

### Licenses

| Url | Method | Short Description | Details Page |
| :--- | :--- | :--- | :--- |
| `/api/v1/licenses.get` | `GET` | Gets all active licenses. | [Link](https://github.com/RocketChat/docs/tree/06af028aecca9430169baa3f517704a68deb6278/api/rest-api/methods/licenses/get.md) |
| `/api/v1/licenses.add` | `POST` | Adds a new license. | [Link](https://github.com/RocketChat/docs/tree/06af028aecca9430169baa3f517704a68deb6278/api/rest-api/methods/licenses/add.md) |

## Language specific wrappers

### Java

* [rocket-chat-rest-client](https://github.com/baloise/rocket-chat-rest-client)

### PHP

* [rocketchat-php](https://github.com/alekseykuleshov/rocket-chat)

### Python

* [rocketchat\_API](https://github.com/jadolg/rocketchat_API)

### Ruby

* [rocketchat-ruby](https://github.com/abrom/rocketchat-ruby)

### Clojure

* [rocketchat-clojure](https://github.com/MalloZup/missile)

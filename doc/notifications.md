# Notifications
Parsing notifications from \*Paint

## Retrieving Notifications
Before you can parse notifications, you must first have them (obviously).  \*Paint keeps your notifications in /includes/ajax.section.my_alerts.php, stored in the JSON format.

## Breaking it down
When you retrieve your notifications from the previously mentioned location, they will look a little something like this:

	[{"id":690420,"type":"group_shout","member":118963,"name":"SoulDJ673","title":"Very cool group name","mess":42069,"min":69}]

#### "id"
I'm not entirely sure what this is for.  Notification id?  It doesn't seem to be used elsewhere.

#### "type"
This describes what the notification pertains to.  Its values can include:

- alert - PM received.  Duplicate of message.
- badge - You earned a badge.
- bb_post - You received a reply on a bulletin board post.
- blog_bumped - A blog post you made was bumped.
- blog_featured - A blog post you made was featured.
- blog_declined - Your request to feature a blog was denied.
- blog_unbumped - A blog post you made was unbumped.
- friend_request - You received a friend request.
- group_shout - There was a shout in the shoutbox of a group you're in.
- message - PM received.
- savii_auction_lost - Your bid in a Savii auction lost.
- savii_auction_sold - Your Savii auction item sold.
- savii_auction_unsold - Your Savii auction item didn't sell.
- savii_auction_won - Your Savii auction bid won.

The following are indeed functional types, but seem to be handled differently than the rest, so the descriptions here may be inaccurate:

- blog_comment - You received a comment on a blog post you made.
- blog_reply - Possible duplicate of blog_comment.  I'm not sure.
- group_invitation - You've received an invitation to a group. This doesn't seem to function.
- helpdesk_duplicate - Your Help Desk post was marked as a duplicate.
- helpdesk_reply - Your Help Desk post received a reply.
- helpdesk_resolved - Your Help Desk post was marked as resolved.
- profile_comment - You received a comment on your profile.
- new - I'm not sure what this was intended to be used for.  It was used when a comment was left on my profile, perhaps it's a catchall?

#### "member"
This is the id of the member the notification pertains to, if any at all.  Appending it to the end of 

	https://3dspaint.com/member/?id=

or

	https://dsipaint.com/member/?id=

will bring you to said member's profile page, like this: [https://3dspaint.com/member/?id=118963](https://3dspaint.com/member/?id=118963).

The member id has other uses too, listed in [friends.md](./friends.md).

#### "name"
This is the username of the member the notification pertains to, if any.

#### "title"
This is not used very consistently at all, it very much varies on the type of notification:

- group_shout - Name of the group
- message - Subject of the incoming message
- new - The entirety of what is displayed in the notifcations area on the main page (html tags included)

#### "mess"
As portrayed by the name, this originally created for message ids.  In that application, appending it to the message viewer url would open that specific PM conversation.

	https://3dspaint.com/mymessageviewer.php?message=[mess]

Now, like "title", this has very inconsistent uses, varying depending on the notification type:

- message - Message ID
- group_shout - Group ID

#### "min"
This is how long, in minutes, it's been since the notification occurred.

Please, help complete the information I have here.  Visit [https://git.souldj673.xyz:6733/#contribute](https://git.souldj673.xyz:6733/#contribute) for information on how to contribute.

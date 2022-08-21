# Friends
Retrieving online friends and understanding how they're kept on \*Paint.

## Retrieving Online Friends
\*Paint keeps your currently online friends stored in JSON format at /includes/ajax.section.my_friends.php

## Parsing
Retrieving the file previously mentioned will return output that will resemble this:

	[{"id":150961,"name":"DCTheGamr","min":15,"act":"Shouting in a Group"}]

It's fairly easy to understand.

#### "id"
This is the id of the friend in question.  It is used to uniquely identify them and pages relating to them.   I'll list only a few pages, most pages work similarly to these.

##### Profile Page
Append their id to the member page (/member/?id=[id]), and their profile page will appear.

##### Blogs
You can find public blogs written by them by appending their id to the blog page:

	https://3dspaint.com/blog/?author=[id]

You can also see unfeatured blogs by then appending "&featured=false" to that:

	https://3dspaint.com/blog/?author=[id]&featured=false

##### Polls
Similarly to blogs, you can find public polls held by them by appending their id to the polls page.  The scheme is almost identical to the one used for blogs:
	
	https://3dspaint.com/poll/?author=[id]

including showing unfeatured polls:

	https://3dspaint.com/poll/?author=[id]&featured=false

##### 3DSPaint Gallery
You are able to view the 3DSPaint Gallery of a user as well.  **This does not work for the DSiPaint Gallery, as that never had a way to search by user.**  To view a user's 3DSPaint Gallery, append their id to the gallery page:

	https://3dspaint.com/paint/gallery.php?member=[id]

#### "name"
This is the username of your friend.  Pretty self-explanatory.

#### "min"
This is the amount of time they've been performing a particular activity.

#### "act"
This is what they're currently doing.  There's a lot of things that can show here, and I'm not sure of how long that list could go.  I'll list a few though:

- [Private] - The user has set \*Paint to not display their activity.
- Chilling on the Homepage - Pretty self-explanatory.
- Talking in Chatroom [chatroom] - Again, self explanatory
- Configuring Account - The user is on their settings page
- Viewing the profile for [user] - The user is on the profile page of the specified user
- Chilling on the Blogs Menu - The user is on the Blogs page, or just viewing the list of their own blogs.
- Reading a Blog by [user] - The user is reading a blog written by the specified user.
- Viewing own Friendlist - Self-explanatory.

There's hundreds more, but I don't have time right now to get a list of all of those.

Please, help me add to this!  See [https://git.souldj673.xyz:6733/#contribute](https://git.souldj673.xyz:6733/#contribute) for details on contributing to this.

That's all, folks!

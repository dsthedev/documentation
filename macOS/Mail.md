# Mail

I’ve used many email clients over the years, always setting Apple Mail aside because of a negative experience many years ago. Turns out it’s pretty great, and with the new Dark Mode introduced in Mojave, it’s even better! Here is how I customize Mail for an optimal experience.

**Note**: This content is occasionally pulled directly from my [documentation](https://github.com/dsthedev/documentation) repository on GitHub.

Before you can even use Mail, you have to sign in with at least one account. It’s quite an annoying “feature” if you don’t use the app, but since I do now, here we go:

1. Sign in with Google account (Authenticate in Safari)
2. Use with Mail, Contacts, Calendars, Notes

Now that an email account has been set up, the first thing to do is go through all the app’s preferences, one by one.

## Mail Preferences

### General

| Option                                                            | Value                               |
| ----------------------------------------------------------------- | ----------------------------------- |
| Default email reader                                              | `Mail.app`                          |
| Check for new messages                                            | `Every 15 minutes`                  |
| New messages sound                                                | `New Messages Sound`                |
| Play sounds for other mail actions                                | `true`                              |
| Dock unread count                                                 | `All Mailboxes`                     |
| New message notifications                                         | `All Mailboxes`                     |
| Downloads folders                                                 | `~/Downloads/Mail` (Need to Create) |
| Remove unedited downloads                                         | `After Message is Deleted`          |
| Archive or delete muted messages                                  | `false`                             |
| Add invitations to Calendar automatically                         | `false`                             |
| Automatically try sending later if outgoing server is unavailable | `false`                             |
| Prefer opening messages in split view when in full screen         | `true`                              |
| When searching all mailboxes, include messages from               | `Trash`, not Junk or Encrypted      |

@todo Look into custom sounds for email alerts, like the Metal Gear Solid chirp.

### Accounts

- Add additional emails here as necessary
- The defaults for all settings should be fine (with Gmail at least)

### Junk Mail

No need to activate junk mail filtering in Mail because it’s handled by Gmail and Live. If you add a custom email domain or want further junk mail filtering, feel free to enable and explore.

### Fonts & Colors

Leave these at the default settings.

### Viewing

| Option                                                | Value        |
| ----------------------------------------------------- | ------------ |
| List Preview                                          | `1 Line`     |
| Move discarded messages into                          | `Trash`      |
| Show message headers                                  | `Default`    |
| Display unread messages with bold font                | `true`       |
| Load remote content in messages                       | `false`      |
| Use Smart Addresses                                   | `false`      |
| Use dark backgrounds for messages                     | `true`       |
| Highlight messages with color when not grouped        | `Ocean Blue` |
| Include related messages                              | `true`       |
| Mark all messages as read when opening a conversation | `false`      |
| Show most recent messages at the top                  | `true`       |
| ~~Use classic layout~~                                | `false`      |
| ~~Show To/Cc label in the message list~~              | `true`       |
| ~~Show contact photos in the message list~~           | `true`       |

### Composing

| Option                                              | Value                                                       |
| --------------------------------------------------- | ----------------------------------------------------------- |
| Message format                                      | `Plain Text`                                                |
| Check spelling                                      | `as I type`                                                 |
| Automatically `cc/bcc` myself                       | `false`                                                     |
| Addressing                                          | ...                                                         |
| When sending to a group, show all member addresses  | `true`                                                      |
| Mark addresses not ending with                      | `false`                                                     |
| Send new messages from                              | `Automatically select the best account`                     |
| Responding                                          | ...                                                         |
| Use the same message format as the original message | `false`                                                     |
| Quote the text of the original message              | `true`                                                      |
| Increase quote level                                | `true`                                                      |
| When quoting text in replies or forwards            | `Include selected text, if any; otherwise include all text` |

### Signatures

Every email account should have a custom signature, and applied here. Also make sure to select each account individually to apply the right signature.

| Option                               | Value  |
| ------------------------------------ | ------ |
| Always match my default message font | `true` |
| Place signature above quoted text    | `true` |

### Rules

@todo Take some time to go over the possibilities of Apple Mail rules and set some sensible rules
@todo Find a way to extract these out for export import when wiping or setting up a new mac.

## Tips

### Search

At first, searching seems like it sucks. But that’s only because Apple hides advanced search options from its users. You can find advanced search options here. For example:

- `date: 01/01/13-12/31/13`

### View

| Option                | Value         |
| --------------------- | ------------- |
| Show Date and Time    | `true`        |
| Show Mailbox List     | `shift+cmd+M` |
| Enable Message Filter | `cmd+L`       |


## Conclusion

Not much, other than the default Mail app that comes with macOS is extremely nice, and I highly recommend using it!
# Apple Mail

## First Steps

- Choose a Mail account provider...
  - Other Mail Account...
    - Name: `{Full Name}`
    - Email Address: `{emailaddress}@{domain.com}`
    - Password: `{password}`
    - If it doesn't work automagically:
      - Enter the Account Type (IMAP) and Incoming / Outgoing Server URL's

---

## Preferences

### General

- Default email reader: `Mail.app`
- Check for new messages: `Every 15 minutes`
- New messages sound: `New Messages Sound`
  - TODO: Look into custom sounds
- Play sounds for other mail actions: `true`
- Dock unread count: `All Mailboxes`
- New message notifications: `All Mailboxes`
- Downloads folders: `Downloads/Mail`
  - Create a folder called `Mail` in the default `Downloads` folder.
- Remove unedited downloads: `After Message is Deleted`
- Add invitations to Calendar automatically: `false`
- Automatically try sending later if outgoing server is unavailable: `false`
- Prefer opening messages in split view when in full screen: `true`
- When searching all mailboxes, include messages from: `Trash`, not Junk or Encrypted

### Accounts

- Add additional emails here as necessary
- The defaults for all settings should be fine (with Gmail at least)

### Junk Mail

No need to activate junk mail filtering in Mail because it’s handled by Gmail and Live. If you add a custom email domain or want further junk mail filtering, feel free to enable and explore.

### Fonts & Colors

Leave these at the default settings.

### Viewing

- Use classic layout: `false`
- Show To/Cc label in the mesage list: `true`
- Show contact photos in the message list: `true`
- List Preview: `1 Line`
- Move discarded messags into: `Trash`
- Show message headers: `Default`
- Display unread messages with bld font: `true`
- Load remote content in messages: `false`
- Use Smart Addresses: `false`
- Use dark backgrounds for mesages: `true`
- Highlight messages with color when not grouped: `Default Blue`
- Include related messages: `true`
- Mark all messages as read when oening a conversation: `false`
- Show most recent messages at the top: `true`

### Composing

- Composing:
  - Message format: `Plain Text`
    - No need for goofy pasted text from other sources, let the recipient receive normal plain old text
  - Check spelling: `As I type`
  - Automatically `cc/bcc` myself: `false`
- Addressing:
  - When sending to a group, show all member addresses: `true`
  - Mark addresses not ending with: `false`
  - Send new messages from: `Automatically select the best account`
- Responding
  - Use the same message format as the original message: `false`
  - Quote the text of the original message: `true`
  - Increase quote level: `true`
  - When quoting text in replies or forwards: `Include selected text, if any; otherwise include all text`

### Signatures

- Add any custom signatures here for each account and:
  - Make sure to select each account and apply the right signature for each
  - Always match my default message font: `true`
- Place signature above quoted text: `true

### Rules

- TODO: Take some time to go over the possibilities of Apple Mail rules and set some sensible rules

---

## Tips

- Search uses keywords and has a unique "Apple" format, here's some useful examples:
  - `date: 01/01/19-12/31/19`
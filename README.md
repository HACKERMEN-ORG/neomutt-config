# Why this exists

So my friends can send me encrypted mail, bottom post, and send/apply
patches.

> "I installed neomutt but I haven't figured it out"

Neomutt defaults have legacy lock-in issues.

# Barebones neomutt config

## Features
- optional PGP encryption/signing/both
- Automatic PGP decryption
- hjkl movement: navigate
- n/p movement: read+page mails like in the GNUs client
- open HTML mail in the $BROWSER with a bind
- edit mail in the $EDITOR
- Can setup multiple mailboxes (just source more files like me-TEMPLATE)
- arcane-config-TEMPLATE to keep user-specific config separate
- Lots of colors
- A million default setting changes that don't do much
- signature

## Non-features

## Install
- clone to ~/.config/neomutt
- install neomutt
- install isync and sendmail for IMAP and SMTP
- install notmuch to search your mails
- install gpg (optional)
- Edit and rename the TEMPLATE files
- Edit the sources at the top of the neomuttrc to fit your needs

## Good alias to do background mail stuff when opening the client

```sh
alias dog="sh -c 'mbsync me 1>&/dev/null && notmuch new 1>&/dev/null'  & neomutt"
```

## TODO
- Automatic WKD for automatic PGP encryption without manually adding keys

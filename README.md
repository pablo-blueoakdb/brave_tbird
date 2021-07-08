## brave_tbird

A smart-ish email client handler script for `brave`.

This script runs `Thunderbird` when a `mailto` link is clicked in
`brave`.

Under certain conditions, webmail may be used instead of
`Thunderbird`.

## Installation

TODO:

## Customization

### XDG_EMAIL_HOOK_WEBMAIL_URL

A user defined variable influences this script as follows:

| XDG_EMAIL_HOOK_WEBMAIL_URL | If Thunderbird is not running |
|----------------------------|-------------------------------|
| Not defined                | Start `Thunderbird`           |
| Defined or set to ""       | Use gmail in `brave`          |
| Set to a Webmail URL       | Use the URL in `brave`        |

## Set up

### Tweak brave handler

On `brave`, ensure that there are not hanlders for email defined or
that `mail.google.com` is blocked:

```
brave://settings/handlers
```
### xdg-mime

Confirm that `Thunderbird` is the default email client.

The expected output from the command below is `thunderbird.desktop`:

```shell
xdg-mime query default 'x-scheme-handler/mailto'
```

#### KDE

On `KDE`, if the above output is not returned:

1. `System Settings > Applications > Default Applications`
2. Ensure that the `Email client` is set to `Thunderbird`.

## brave_tbird

A smart-ish email client hanlder script for `brave`.

This script runs `Thunderbird` when a `mailto` link is clicked in
`brave`.

Under certain conditions, webmail may be used instead of
`Thunderbird`.

## Installation

TODO:

## XDG_EMAIL_HOOK_WEBMAIL_URL

A user defined variable influences this script as follows:

| XDG_EMAIL_HOOK_WEBMAIL_URL | If Thunderbird is not running |
|----------------------------|-------------------------------|
| Not defined                | Start `Thunderbird`           |
| Defined or set to ""       | Use gmail in `brave`          |
| Set to a Webmail URL       | Use the URL in `brave`        |

## xdg voodoo

Confirm that thunderbird is the default email client:

```shell
xdg-mime query default 'x-scheme-handler/mailto'
```

Expected output `thunderbird.desktop`

### KDE

`System Settings > Applications > Default Applications`  Ensure that
the `Email client` is set to `Thunderbird`.

## Tweak brave handler

On `brave`, ensure that there are not hanlders for email defined or
that `mail.google.com` is blocked:

```
brave://settings/handlers
```

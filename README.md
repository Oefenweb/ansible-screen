## screen [![Build Status](https://travis-ci.org/Oefenweb/ansible-screen.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-screen)

Set up screen in Debian-like systems.

#### Requirements

None

#### Variables

* `screen_screenrc_destinations`: [default: `[/etc/skel, {{ ansible_env.HOME }}]`]: Destinations to copy the screenrc file to
* `screen_startup_message`: [default: `false`]: Whether or not to show the copyright notice during startup
* `screen_autodetach`: [default: `true`]: Whether or not to automatically detach the session on SIGHUP
* `screen_vbell`: [default: `false`]: Whether or not to use visual bell
* `screen_defscrollback`: [default: `1000`]: Default lines of scrollback

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
  - screen
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-screen/issues)!

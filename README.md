## screen

[![CI](https://github.com/Oefenweb/ansible-screen/workflows/CI/badge.svg)](https://github.com/Oefenweb/ansible-screen/actions?query=workflow%3ACI)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-screen-blue.svg)](https://galaxy.ansible.com/Oefenweb/screen)

Set up screen in Debian-like systems.

#### Requirements

None

#### Variables

* `screen_screenrc_destinations`: [default: `{skell: dest: /etc/skel, current: dest: "{{ ansible_env.HOME }}"}`]: Destinations to copy the screenrc file to
* `screen_screenrc_destinations.key`: The identifier of the file (e.g. `skel`)
* `screen_screenrc_destinations.key.dest`: The remote path of the file to copy (e.g. `/etc/skel`)
* `screen_screenrc_destinations.key.owner`: The name of the user that should own the file (optional, default `root`)
* `screen_screenrc_destinations.key.group`: The name of the group that should own the file (optional, default `owner`, then `root`)
* `screen_screenrc_destinations.key.mode`: The mode of the file, such as 0644 (optional, default `0644`)

* `screen_startup_message`: [default: `false`]: Whether or not to show the copyright notice during startup
* `screen_autodetach`: [default: `true`]: Whether or not to automatically detach the session on SIGHUP
* `screen_vbell`: [default: `false`]: Whether or not to use visual bell
* `screen_defscrollback`: [default: `1000`]: Default lines of scrollback
* `screen_termcapinfo`: [optional]: Use this to modify your terminal's termcap entry without going through all the hassles involved in creating a custom termcap entry (e.g. `xterm* ti@:te@`)

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - oefenweb.screen
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-screen/issues)!

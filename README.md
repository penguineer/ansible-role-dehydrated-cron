# Ansible Role: Deyhdrated Cron

> Install cron calls to dehydrated and only send e-mails in case of changes.


## Usage


### Configuration

Please note that all variables have default values and usually do not need to be changed.

* `dehydrated_cron_script_dir`: Path to the cron helper scripts
* `dehydrated_config_dir`: Path to the Dehydrated configuration
* `dehydrated_certs_dir`: Path to the Dehydrated certificates
* `dehydrated_binary`: Path to the Dehydrated binary
* `dehydrated_check_span`: Time (in seconds) before expiration for a certificate to be reported as stale.
* `dehydrated_cron_renew`: Crontab pattern for the renew call
* `dehydrated_cron_check`: Crontab pattern for the check call

The configuration variables are compatible with [24367dfa/ansible-role-dehydrated](https://github.com/24367dfa/ansible-role-dehydrated).


### Include

as role:

```yaml
vars:
  - dehydrated_…: …

roles:
  - role: dehydrated
```

as task:

```yaml
tasks:
  - name: Setup cron for dehydrated
    include_role:
      name: ansible-role-dehydrated-cron
    vars:
      dehydrated_…: …
```


## Maintainers

* Stefan Haun ([@penguineer](https://github.com/penguineer))


## Contributing

PRs are welcome!

If possible, please stick to the following guidelines:

* Keep PRs reasonably small and their scope limited to a feature or module within the code.
* If a large change is planned, it is best to open a feature request issue first, then link subsequent PRs to this issue, so that the PRs move the code towards the intended feature.


## License

[MIT](LICENSE.txt) © 2022 Stefan Haun and contributors

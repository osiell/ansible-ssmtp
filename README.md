# sSMTP

Ansible role to deploy sSMTP on a Debian or Ubuntu host.

## Supported Platforms

* Debian
    - Wheezy    (7)
    - Jessie    (8)
    - Stretch   (9)
* Ubuntu
    - Trusty    (14.04)
    - Xenial    (16.04)

## Example (Playbook)

```yaml
- name: Any host
  hosts: my_host
  become: yes
  roles:
    - ssmtp
  vars:
	- ssmtp_conf:
		Root: root@your.domain
		Mailhub: mail.provider.net:465
		UseTLS: 'YES'
		AuthUser: Login
		AuthPass: PaSsWORd
		RewriteDomain: your.domain
		FromLineOverride: 'NO'
```

## Variables

See the [defaults/main.yml](defaults/main.yml) file.

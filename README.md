# Ansible Role: php with fpm package



## Requirements

None.

## Role Variables

Available variables are listed below, along with default values:

    # The defaults provided by this role are specific to each distribution.
    php_version:
       - 5.6 or 7.1

Set the php_version accordingly.


## Dependencies

None.

## Example Playbook (installs default mysql-server available)

    - hosts: php
      roles:
        - osm_php-fpm

## Example Playbook (install mysql-server client)

For Debian:

    - hosts: php
      roles:
        - role: osm_php-fpm
          when: "ansible_os_family == 'Debian'"
          php_version:
            - 5.6 or 7.1

## License

MIT / BSD

## Author Information

www.opstree.com

blog.opstree.com

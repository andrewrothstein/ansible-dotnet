andrewrothstein.dotnet
=========
![Build Status](https://github.com/andrewrothstein/ansible-dotnet/actions/workflows/build.yml/badge.svg)

Generic installation role for either .NET Core SDK or runtime.

Requirements
------------

See [meta/main.yml](meta/main.yml)

Role Variables
--------------

See [defaults/main.yml](defaults/main.yml)

Definition Structure:
```yml
dotnet_install_type: {{ sdk | runtime }}
dotnet_ver: {{ target_semver }}
dotnet_subdirs:
 '{{ dotnet_platform }}': '{{ dotnet_subdir }}'
dotnet_checksums:
 '{{ dotnet_platform }}': '{{ dotnet_checksum }}'
```

Dependencies
------------

See [meta/main.yml](meta/main.yml)

Example Playbook
----------------

```yml
- hosts: servers
  roles:
    - andrewrothstein.dotnet
```

License
-------

MIT

Author Information
------------------

Andrew Rothstein <andrew.rothstein@gmail.com>

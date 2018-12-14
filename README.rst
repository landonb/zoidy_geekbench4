zoidy_geekbench4
================

An Ansible role to run `Geekbench 4 <https://www.geekbench.com/>`__ benchmarks.

Role Variables
--------------

Default values are stored in ``defaults/main.yml``.
There are 2 interesting values.

- Keep the Geekbench 4 version current::

    zoidy_geekbench4_app_version: '4.x.x'

- Find working files and results in user home on the host::

    zoidy_geekbench4_working_dir: "/{{ ansible_env.HOME }}/Documents/{{ now_date }}-geekbench4"

  For instance, you might find the results at::

    /home/user/Documents/2018_12_13-geekbench4/

Example Playbook
----------------

It's simple to run the role from a playbook::

  - hosts: servers
    roles:
       - role: zoidy_geekbench4

License
-------

`GPLv3 <LICENSE>`__


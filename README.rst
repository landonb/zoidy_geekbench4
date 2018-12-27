zoidy_geekbench4
================

An Ansible role to run `Geekbench 4 <https://www.geekbench.com/>`__ benchmarks.

Role Variables
--------------

Default values are stored in ``defaults/main.yml``.
There are 2 interesting values.

- Keep the Geekbench 4 version current::

    zoidy_geekbench4_app_version: '4.x.x'

- You'll find benchmark result URLs stored on the host in a single file::

    ~/.local/share/zoidy_geekbench4/$(hostname)-geekbench-results.lnk

  as indicated by the two variables::

    zoidy_geekbench4_working_dir: "{{ ansible_env.HOME }}/.local/share/zoidy_geekbench4"

    zoidy_geekbench4_results_lns: "{{ zoidy_geekbench4_working_dir }}/{{ ansible_hostname }}-geekbench4-results.txt"

Example Playbook
----------------

It's simple to run the role from a playbook::

  - hosts: servers
    roles:
       - role: zoidy_geekbench4

License
-------

`GPLv3 <LICENSE>`__


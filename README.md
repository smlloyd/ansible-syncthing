Ansible syncthing
=========

Install and manages syncthing (http://syncthing.net/) on Linux (Centos).

* checks versions
* download syncthing (specific version or latest)
* installs it in `{{ syncthing_home }}/bin/`
* configurates addresses, username (a few basic options)


Requirements
------------
 * https://github.com/cmprescott/ansible-xml (https://galaxy.ansible.com/cmprescott/xml/)

Role Variables
--------------

| Option                       | Description                                   | Default           |
| ---------------------------- | --------------------------------------------- | ----------------- |
| **syncthing_user**           | The user who runs the syncthing daemon.       | `syncthing`
| **syncthing_home**           | Home directory of syncthing                   | `/home/{{ syncthing_user }}`
| **syncthing_address**        | address for webinterface                      | `127.0.0.1:8080`
| **syncthing_localannounce**  | enable/disable localAnnounce option           | `false`
| **syncthing_globalannounce** | enable/disable globaleAnnounce option         | `false`
| **syncthing_listen**         | address for remote connections option         | `tcp://0.0.0.0:22000`
| **syncthing_upnp**           | enable/disable `upnp`.                        | `false`
| **syncthing_gui_user**       | Username for the gui login.                   | 
| **syncthing_gui_password**   | Password for the gui login.                   | 


Dependencies
------------

 * cmprescott.xml: https://galaxy.ansible.com/cmprescott/xml/

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
    - role: syncthing
      syncthing_user: syncthing
      syncthing_localannounce: false
      syncthing_globalannounce: false
      syncthing_upnp: false

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
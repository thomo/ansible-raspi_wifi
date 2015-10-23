Ansible Role: thomo.raspi_wifi
=========

An Ansible role to configure the WiFi connection parameter on a Raspberry PI.


Role Variables
--------------

    # Protocol type can be: RSN (for WPA2) and WPA (for WPA1)
    raspi_wifi_proto: RSN

    # Key management type can be: WPA-PSK or WPA-EAP (Pre-Shared or Enterprise)
    raspi_wifi_key_mgmt: WPA-PSK

    # Pairwise can be CCMP or TKIP (for WPA2 or WPA1)
    raspi_wifi_pairwise: CCMP

    #Authorization option should be OPEN for both WPA1/WPA2 (in less commonly used are SHARED and LEAP)
    raspi_wifi_auth_alg: OPEN

    # define/set it in playbook or in group_vars/host_vars
    # You should encrypt the file with ansible-vault
    raspi_wifi_ssid: 'your wifi name'
    raspi_wifi_psk: 'your wifi secret'


Dependencies
------------


Example Playbook
----------------

    - hosts: new
      roles:
         - role: thomo.raspi_wifi

License
-------

**MIT** - see LICENSE file for details.

Author Information
------------------

Thomas Mohaupt https://github.com/thomo/ansible-raspi_wifi

:source: fortios_wireless_controller_hotspot20_h2qp_conn_capability.py

:orphan:

.. _fortios_wireless_controller_hotspot20_h2qp_conn_capability:

fortios_wireless_controller_hotspot20_h2qp_conn_capability -- Configure connection capability in Fortinet's FortiOS and FortiGate.
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 2.9

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiGate or FortiOS (FOS) device by allowing the user to set and modify wireless_controller_hotspot20 feature and h2qp_conn_capability category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v6.0.5


Requirements
------------
The below requirements are needed on the host that executes this module.

- fortiosapi>=0.9.8


Parameters
----------

.. raw:: html

    <ul>

    <li><span class="li-head">host</span> - FortiOS or FortiGate IP address. <span class="li-normal">type: str</span> <span class="li-required">required: false</span></li>
    <li><span class="li-head">username</span> - FortiOS or FortiGate username. <span class="li-normal">type: str</span> <span class="li-required">required: false</span></li>
    <li><span class="li-head">password</span> - FortiOS or FortiGate password. <span class="li-normal">type: str</span> <span class="li-normal">default: ""</span></li>
    <li><span class="li-head">vdom</span> - Virtual domain, among those defined previously. A vdom is a virtual instance of the FortiGate that can be configured and used as a different unit. <span class="li-normal">type: str</span> <span class="li-normal">default: root</span></li>
    <li><span class="li-head">https</span> - Indicates if the requests towards FortiGate must use HTTPS protocol. <span class="li-normal">type: bool</span> <span class="li-normal">default: true</span></li>
    <li><span class="li-head">ssl_verify</span> - Ensures FortiGate certificate must be verified by a proper CA. <span class="li-normal">type: bool</span> <span class="li-normal">default: true</span></li>
    <li><span class="li-head">state</span> - Indicates whether to create or remove the object. <span class="li-normal">type: str</span> <span class="li-required">required</span> <span class="li-normal">choices: present,  absent</span></li>
    <li><span class="li-head">wireless_controller_hotspot20_h2qp_conn_capability</span> - Configure connection capability. <span class="li-normal">default: null</span> <span class="li-normal">type: dict</span></li>
            <ul class="ul-self">

            <li><span class="li-head">esp_port</span> - Set ESP port service (used by IPsec VPNs) status. <span class="li-normal">type: str</span> <span class="li-normal">choices: closed,  open,  unknown</span></li>
            <li><span class="li-head">ftp_port</span> - Set FTP port service status. <span class="li-normal">type: str</span> <span class="li-normal">choices: closed,  open,  unknown</span></li>
            <li><span class="li-head">http_port</span> - Set HTTP port service status. <span class="li-normal">type: str</span> <span class="li-normal">choices: closed,  open,  unknown</span></li>
            <li><span class="li-head">icmp_port</span> - Set ICMP port service status. <span class="li-normal">type: str</span> <span class="li-normal">choices: closed,  open,  unknown</span></li>
            <li><span class="li-head">ikev2_port</span> - Set IKEv2 port service for IPsec VPN status. <span class="li-normal">type: str</span> <span class="li-normal">choices: closed,  open,  unknown</span></li>
            <li><span class="li-head">ikev2_xx_port</span> - Set UDP port 4500 (which may be used by IKEv2 for IPsec VPN) service status. <span class="li-normal">type: str</span> <span class="li-normal">choices: closed,  open,  unknown</span></li>
            <li><span class="li-head">name</span> - Connection capability name. <span class="li-required">required</span> <span class="li-normal">type: str</span></li>
            <li><span class="li-head">pptp_vpn_port</span> - Set Point to Point Tunneling Protocol (PPTP) VPN port service status. <span class="li-normal">type: str</span> <span class="li-normal">choices: closed,  open,  unknown</span></li>
            <li><span class="li-head">ssh_port</span> - Set SSH port service status. <span class="li-normal">type: str</span> <span class="li-normal">choices: closed,  open,  unknown</span></li>
            <li><span class="li-head">tls_port</span> - Set TLS VPN (HTTPS) port service status. <span class="li-normal">type: str</span> <span class="li-normal">choices: closed,  open,  unknown</span></li>
            <li><span class="li-head">voip_tcp_port</span> - Set VoIP TCP port service status. <span class="li-normal">type: str</span> <span class="li-normal">choices: closed,  open,  unknown</span></li>
            <li><span class="li-head">voip_udp_port</span> - Set VoIP UDP port service status. <span class="li-normal">type: str</span> <span class="li-normal">choices: closed,  open,  unknown</span>
            </ul>

    </ul>




Notes
-----

.. note::


   - Requires fortiosapi library developed by Fortinet

   - Run as a local_action in your playbook



Examples
--------

.. code-block:: yaml+jinja

    - hosts: localhost
      vars:
       host: "192.168.122.40"
       username: "admin"
       password: ""
       vdom: "root"
       ssl_verify: "False"
      tasks:
      - name: Configure connection capability.
        fortios_wireless_controller_hotspot20_h2qp_conn_capability:
          host:  "{{ host }}"
          username: "{{ username }}"
          password: "{{ password }}"
          vdom:  "{{ vdom }}"
          https: "False"
          state: "present"
          wireless_controller_hotspot20_h2qp_conn_capability:
            esp_port: "closed"
            ftp_port: "closed"
            http_port: "closed"
            icmp_port: "closed"
            ikev2_port: "closed"
            ikev2_xx_port: "closed"
            name: "default_name_9"
            pptp_vpn_port: "closed"
            ssh_port: "closed"
            tls_port: "closed"
            voip_tcp_port: "closed"
            voip_udp_port: "closed"



Return Values
-------------
Common return values are documented: https://docs.ansible.com/ansible/latest/reference_appendices/common_return_values.html#common-return-values, the following are the fields unique to this module:

.. raw:: html

    <ul>

    <li><span class="li-return">build</span> - Build number of the fortigate image <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: '1547'</span></li>
    <li><span class="li-return">http_method</span> - Last method used to provision the content into FortiGate <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: 'PUT'</span></li>
    <li><span class="li-return">http_status</span> - Last result given by FortiGate on last operation applied <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: 200</span></li>
    <li><span class="li-return">mkey</span> - Master key (id) used in the last call to FortiGate <span class="li-normal">returned: success</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: id</span></li>
    <li><span class="li-return">name</span> - Name of the table used to fulfill the request <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: urlfilter</span></li>
    <li><span class="li-return">path</span> - Path of the table used to fulfill the request <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: webfilter</span></li>
    <li><span class="li-return">revision</span> - Internal revision number <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: 17.0.2.10658</span></li>
    <li><span class="li-return">serial</span> - Serial number of the unit <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: FGVMEVYYQT3AB5352</span></li>
    <li><span class="li-return">status</span> - Indication of the operation's result <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: success</span></li>
    <li><span class="li-return">vdom</span> - Virtual domain used <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: root</span></li>
    <li><span class="li-return">version</span> - Version of the FortiGate <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: v5.6.3</span></li>
    </ul>



Status
------

- This module is not guaranteed to have a backwards compatible interface.



Authors
-------

- Miguel Angel Munoz (@mamunozgonzalez)
- Nicolas Thomas (@thomnico)



.. hint::
    If you notice any issues in this documentation, you can create a pull request to improve it.
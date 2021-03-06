:source: fortios_firewall_ssl_server.py

:orphan:

.. _fortios_firewall_ssl_server:

fortios_firewall_ssl_server -- Configure SSL servers in Fortinet's FortiOS and FortiGate.
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 2.8

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiGate or FortiOS (FOS) device by allowing the user to set and modify firewall feature and ssl_server category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v6.0.5


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
    <li><span class="li-head">state</span> - Indicates whether to create or remove the object. This attribute was present already in previous version in a deeper level. It has been moved out to this outer level. <span class="li-normal">type: str</span> <span class="li-required">required: false</span> <span class="li-normal">choices: present,  absent</span></li>
    <li><span class="li-head">firewall_ssl_server</span> - Configure SSL servers. <span class="li-normal">default: null</span> <span class="li-normal">type: dict</span></li>
            <ul class="ul-self">

            <li><span class="li-head">state</span> - B(Deprecated) Starting with Ansible 2.9 we recommend using the top-level 'state' parameter. HORIZONTALLINE Indicates whether to create or remove the object. <span class="li-normal">type: str</span> <span class="li-required">required: false</span> <span class="li-normal">choices: present,  absent</span></li>
            <li><span class="li-head">add_header_x_forwarded_proto</span> - Enable/disable adding an X-Forwarded-Proto header to forwarded requests. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable,  disable</span></li>
            <li><span class="li-head">ip</span> - IPv4 address of the SSL server. <span class="li-normal">type: str</span></li>
            <li><span class="li-head">mapped_port</span> - Mapped server service port (1 - 65535). <span class="li-normal">type: int</span></li>
            <li><span class="li-head">name</span> - Server name. <span class="li-required">required</span> <span class="li-normal">type: str</span></li>
            <li><span class="li-head">port</span> - Server service port (1 - 65535). <span class="li-normal">type: int</span></li>
            <li><span class="li-head">ssl_algorithm</span> - Relative strength of encryption algorithms accepted in negotiation. <span class="li-normal">type: str</span> <span class="li-normal">choices: high,  medium,  low</span></li>
            <li><span class="li-head">ssl_cert</span> - Name of certificate for SSL connections to this server. Source vpn.certificate.local.name. <span class="li-normal">type: str</span></li>
            <li><span class="li-head">ssl_client_renegotiation</span> - Allow or block client renegotiation by server. <span class="li-normal">type: str</span> <span class="li-normal">choices: allow,  deny,  secure</span></li>
            <li><span class="li-head">ssl_dh_bits</span> - Bit-size of Diffie-Hellman (DH) prime used in DHE-RSA negotiation. <span class="li-normal">type: str</span> <span class="li-normal">choices: 768,  1024,  1536,  2048</span></li>
            <li><span class="li-head">ssl_max_version</span> - Highest SSL/TLS version to negotiate. <span class="li-normal">type: str</span> <span class="li-normal">choices: tls-1.0,  tls-1.1,  tls-1.2</span></li>
            <li><span class="li-head">ssl_min_version</span> - Lowest SSL/TLS version to negotiate. <span class="li-normal">type: str</span> <span class="li-normal">choices: tls-1.0,  tls-1.1,  tls-1.2</span></li>
            <li><span class="li-head">ssl_mode</span> - SSL/TLS mode for encryption and decryption of traffic. <span class="li-normal">type: str</span> <span class="li-normal">choices: half,  full</span></li>
            <li><span class="li-head">ssl_send_empty_frags</span> - Enable/disable sending empty fragments to avoid attack on CBC IV. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable,  disable</span></li>
            <li><span class="li-head">url_rewrite</span> - Enable/disable rewriting the URL. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable,  disable</span>
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
      - name: Configure SSL servers.
        fortios_firewall_ssl_server:
          host:  "{{ host }}"
          username: "{{ username }}"
          password: "{{ password }}"
          vdom:  "{{ vdom }}"
          https: "False"
          state: "present"
          firewall_ssl_server:
            add_header_x_forwarded_proto: "enable"
            ip: "<your_own_value>"
            mapped_port: "5"
            name: "default_name_6"
            port: "7"
            ssl_algorithm: "high"
            ssl_cert: "<your_own_value> (source vpn.certificate.local.name)"
            ssl_client_renegotiation: "allow"
            ssl_dh_bits: "768"
            ssl_max_version: "tls-1.0"
            ssl_min_version: "tls-1.0"
            ssl_mode: "half"
            ssl_send_empty_frags: "enable"
            url_rewrite: "enable"



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
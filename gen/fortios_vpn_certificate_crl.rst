:source: fortios_vpn_certificate_crl.py

:orphan:

.. _fortios_vpn_certificate_crl:

fortios_vpn_certificate_crl -- Certificate Revocation List as a PEM file in Fortinet's FortiOS and FortiGate.
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 2.9

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiGate or FortiOS (FOS) device by allowing the user to set and modify vpn_certificate feature and crl category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v6.0.5


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
    <li><span class="li-head">vpn_certificate_crl</span> - Certificate Revocation List as a PEM file. <span class="li-normal">default: null</span> <span class="li-normal">type: dict</span></li>
            <ul class="ul-self">

            <li><span class="li-head">crl</span> - Certificate Revocation List as a PEM file. <span class="li-normal">type: str</span></li>
            <li><span class="li-head">http_url</span> - HTTP server URL for CRL auto-update. <span class="li-normal">type: str</span></li>
            <li><span class="li-head">last_updated</span> - Time at which CRL was last updated. <span class="li-normal">type: int</span></li>
            <li><span class="li-head">ldap_password</span> - LDAP server user password. <span class="li-normal">type: str</span></li>
            <li><span class="li-head">ldap_server</span> - LDAP server name for CRL auto-update. <span class="li-normal">type: str</span></li>
            <li><span class="li-head">ldap_username</span> - LDAP server user name. <span class="li-normal">type: str</span></li>
            <li><span class="li-head">name</span> - Name. <span class="li-required">required</span> <span class="li-normal">type: str</span></li>
            <li><span class="li-head">range</span> - Either global or VDOM IP address range for the certificate. <span class="li-normal">type: str</span> <span class="li-normal">choices: global,  vdom</span></li>
            <li><span class="li-head">scep_cert</span> - Local certificate for SCEP communication for CRL auto-update. Source vpn.certificate.local.name. <span class="li-normal">type: str</span></li>
            <li><span class="li-head">scep_url</span> - SCEP server URL for CRL auto-update. <span class="li-normal">type: str</span></li>
            <li><span class="li-head">source</span> - Certificate source type. <span class="li-normal">type: str</span> <span class="li-normal">choices: factory,  user,  bundle</span></li>
            <li><span class="li-head">source_ip</span> - Source IP address for communications to a HTTP or SCEP CA server. <span class="li-normal">type: str</span></li>
            <li><span class="li-head">update_interval</span> - Time in seconds before the FortiGate checks for an updated CRL. Set to 0 to update only when it expires. <span class="li-normal">type: int</span></li>
            <li><span class="li-head">update_vdom</span> - VDOM for CRL update. Source system.vdom.name. <span class="li-normal">type: str</span>
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
      - name: Certificate Revocation List as a PEM file.
        fortios_vpn_certificate_crl:
          host:  "{{ host }}"
          username: "{{ username }}"
          password: "{{ password }}"
          vdom:  "{{ vdom }}"
          https: "False"
          state: "present"
          vpn_certificate_crl:
            crl: "<your_own_value>"
            http_url: "<your_own_value>"
            last_updated: "5"
            ldap_password: "<your_own_value>"
            ldap_server: "<your_own_value>"
            ldap_username: "<your_own_value>"
            name: "default_name_9"
            range: "global"
            scep_cert: "<your_own_value> (source vpn.certificate.local.name)"
            scep_url: "<your_own_value>"
            source: "factory"
            source_ip: "84.230.14.43"
            update_interval: "15"
            update_vdom: "<your_own_value> (source system.vdom.name)"



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
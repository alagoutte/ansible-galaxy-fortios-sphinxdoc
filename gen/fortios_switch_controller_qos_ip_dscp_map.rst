:source: fortios_switch_controller_qos_ip_dscp_map.py

:orphan:

.. _fortios_switch_controller_qos_ip_dscp_map:

fortios_switch_controller_qos_ip_dscp_map -- Configure FortiSwitch QoS IP precedence/DSCP in Fortinet's FortiOS and FortiGate.
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 2.9

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiGate or FortiOS (FOS) device by allowing the user to set and modify switch_controller_qos feature and ip_dscp_map category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v6.0.5


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
    <li><span class="li-head">switch_controller_qos_ip_dscp_map</span> - Configure FortiSwitch QoS IP precedence/DSCP. <span class="li-normal">default: null</span> <span class="li-normal">type: dict</span></li>
            <ul class="ul-self">
     description: Description of the ip-dscp map name. <span class="li-normal">type: str</span></li>
            <li><span class="li-head">map</span> - Maps between IP-DSCP value to COS queue. <span class="li-normal">type: list</span></li>
                    <ul class="ul-self">

                    <li><span class="li-head">cos_queue</span> - COS queue number. <span class="li-normal">type: int</span></li>
                    <li><span class="li-head">diffserv</span> - Differentiated service. <span class="li-normal">type: str</span> <span class="li-normal">choices: CS0,  CS1,  AF11,  AF12,  AF13,  CS2,  AF21,  AF22,  AF23,  CS3,  AF31,  AF32,  AF33,  CS4,  AF41,  AF42,  AF43,  CS5,  EF,  CS6,  CS7</span></li>
                    <li><span class="li-head">ip_precedence</span> - IP Precedence. <span class="li-normal">type: str</span> <span class="li-normal">choices: network-control,  internetwork-control,  critic-ecp,  flashoverride,  flash,  immediate,  priority,  routine</span></li>
                    <li><span class="li-head">name</span> - Dscp mapping entry name. <span class="li-required">required</span> <span class="li-normal">type: str</span></li>
                    <li><span class="li-head">value</span> - Raw values of DSCP (0 - 63). <span class="li-normal">type: str</span>
                    </ul>

            <li><span class="li-head">name</span> - Dscp map name. <span class="li-required">required</span> <span class="li-normal">type: str</span>
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
      - name: Configure FortiSwitch QoS IP precedence/DSCP.
        fortios_switch_controller_qos_ip_dscp_map:
          host:  "{{ host }}"
          username: "{{ username }}"
          password: "{{ password }}"
          vdom:  "{{ vdom }}"
          https: "False"
          state: "present"
          switch_controller_qos_ip_dscp_map:
            description: "<your_own_value>"
            map:
             -
                cos_queue: "5"
                diffserv: "CS0"
                ip_precedence: "network-control"
                name: "default_name_8"
                value: "<your_own_value>"
            name: "default_name_10"



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
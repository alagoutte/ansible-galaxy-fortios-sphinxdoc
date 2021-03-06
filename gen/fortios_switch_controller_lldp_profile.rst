:source: fortios_switch_controller_lldp_profile.py

:orphan:

.. _fortios_switch_controller_lldp_profile:

fortios_switch_controller_lldp_profile -- Configure FortiSwitch LLDP profiles in Fortinet's FortiOS and FortiGate.
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 2.8

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiGate or FortiOS (FOS) device by allowing the user to set and modify switch_controller feature and lldp_profile category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v6.0.5


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
    <li><span class="li-head">switch_controller_lldp_profile</span> - Configure FortiSwitch LLDP profiles. <span class="li-normal">default: null</span> <span class="li-normal">type: dict</span></li>
            <ul class="ul-self">

            <li><span class="li-head">state</span> - B(Deprecated) Starting with Ansible 2.9 we recommend using the top-level 'state' parameter. HORIZONTALLINE Indicates whether to create or remove the object. <span class="li-normal">type: str</span> <span class="li-required">required: false</span> <span class="li-normal">choices: present,  absent</span></li>
            <li><span class="li-head">802.1_tlvs</span> - Transmitted IEEE 802.1 TLVs. <span class="li-normal">type: str</span> <span class="li-normal">choices: port-vlan-id</span></li>
            <li><span class="li-head">802.3_tlvs</span> - Transmitted IEEE 802.3 TLVs. <span class="li-normal">type: str</span> <span class="li-normal">choices: max-frame-size</span></li>
            <li><span class="li-head">auto_isl</span> - Enable/disable auto inter-switch LAG. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable,  enable</span></li>
            <li><span class="li-head">auto_isl_hello_timer</span> - Auto inter-switch LAG hello timer duration (1 - 30 sec). <span class="li-normal">type: int</span></li>
            <li><span class="li-head">auto_isl_port_group</span> - Auto inter-switch LAG port group ID (0 - 9). <span class="li-normal">type: int</span></li>
            <li><span class="li-head">auto_isl_receive_timeout</span> - Auto inter-switch LAG timeout if no response is received (3 - 90 sec). <span class="li-normal">type: int</span></li>
            <li><span class="li-head">custom_tlvs</span> - Configuration method to edit custom TLV entries. <span class="li-normal">type: list</span></li>
                    <ul class="ul-self">

                    <li><span class="li-head">information_string</span> - Organizationally defined information string (0 - 507 hexadecimal bytes). <span class="li-normal">type: str</span></li>
                    <li><span class="li-head">name</span> - TLV name (not sent). <span class="li-required">required</span> <span class="li-normal">type: str</span></li>
                    <li><span class="li-head">oui</span> - Organizationally unique identifier (OUI), a 3-byte hexadecimal number, for this TLV. <span class="li-normal">type: str</span></li>
                    <li><span class="li-head">subtype</span> - Organizationally defined subtype (0 - 255). <span class="li-normal">type: int</span>
                    </ul>

            <li><span class="li-head">med_network_policy</span> - Configuration method to edit Media Endpoint Discovery (MED) network policy type-length-value (TLV) categories. <span class="li-normal">type: list</span></li>
                    <ul class="ul-self">

                    <li><span class="li-head">dscp</span> - Advertised Differentiated Services Code Point (DSCP) value, a packet header value indicating the level of service requested for traffic, such as high priority or best effort delivery. <span class="li-normal">type: int</span></li>
                    <li><span class="li-head">name</span> - Policy type name. <span class="li-required">required</span> <span class="li-normal">type: str</span></li>
                    <li><span class="li-head">priority</span> - Advertised Layer 2 priority (0 - 7; from lowest to highest priority). <span class="li-normal">type: int</span></li>
                    <li><span class="li-head">status</span> - Enable or disable this TLV. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable,  enable</span></li>
                    <li><span class="li-head">vlan</span> - ID of VLAN to advertise, if configured on port (0 - 4094, 0 = priority tag). <span class="li-normal">type: int</span>
                    </ul>

            <li><span class="li-head">med_tlvs</span> - "Transmitted LLDP-MED TLVs (type-length-value descriptions): inventory management TLV and/or network policy TLV." <span class="li-normal">type: str</span> <span class="li-normal">choices: inventory-management,  network-policy</span></li>
            <li><span class="li-head">name</span> - Profile name. <span class="li-required">required</span> <span class="li-normal">type: str</span>
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
      - name: Configure FortiSwitch LLDP profiles.
        fortios_switch_controller_lldp_profile:
          host:  "{{ host }}"
          username: "{{ username }}"
          password: "{{ password }}"
          vdom:  "{{ vdom }}"
          https: "False"
          state: "present"
          switch_controller_lldp_profile:
            802.1_tlvs: "port-vlan-id"
            802.3_tlvs: "max-frame-size"
            auto_isl: "disable"
            auto_isl_hello_timer: "6"
            auto_isl_port_group: "7"
            auto_isl_receive_timeout: "8"
            custom_tlvs:
             -
                information_string: "<your_own_value>"
                name: "default_name_11"
                oui: "<your_own_value>"
                subtype: "13"
            med_network_policy:
             -
                dscp: "15"
                name: "default_name_16"
                priority: "17"
                status: "disable"
                vlan: "19"
            med_tlvs: "inventory-management"
            name: "default_name_21"



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
:source: fortios_wireless_controller_qos_profile.py

:orphan:

.. _fortios_wireless_controller_qos_profile:

fortios_wireless_controller_qos_profile -- Configure WiFi quality of service (QoS) profiles in Fortinet's FortiOS and FortiGate.
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 2.9

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiGate or FortiOS (FOS) device by allowing the user to set and modify wireless_controller feature and qos_profile category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v6.0.5


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
    <li><span class="li-head">wireless_controller_qos_profile</span> - Configure WiFi quality of service (QoS) profiles. <span class="li-normal">default: null</span> <span class="li-normal">type: dict</span></li>
            <ul class="ul-self">

            <li><span class="li-head">bandwidth_admission_control</span> - Enable/disable WMM bandwidth admission control. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable,  disable</span></li>
            <li><span class="li-head">bandwidth_capacity</span> - Maximum bandwidth capacity allowed (1 - 600000 Kbps). <span class="li-normal">type: int</span></li>
            <li><span class="li-head">burst</span> - Enable/disable client rate burst. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable,  disable</span></li>
            <li><span class="li-head">call_admission_control</span> - Enable/disable WMM call admission control. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable,  disable</span></li>
            <li><span class="li-head">call_capacity</span> - Maximum number of Voice over WLAN (VoWLAN) phones allowed (0 - 60). <span class="li-normal">type: int</span></li>
            <li><span class="li-head">comment</span> - Comment. <span class="li-normal">type: str</span></li>
            <li><span class="li-head">downlink</span> - Maximum downlink bandwidth for Virtual Access Points (VAPs) (0 - 2097152 Kbps). <span class="li-normal">type: int</span></li>
            <li><span class="li-head">downlink_sta</span> - Maximum downlink bandwidth for clients (0 - 2097152 Kbps). <span class="li-normal">type: int</span></li>
            <li><span class="li-head">dscp_wmm_be</span> - DSCP mapping for best effort access . <span class="li-normal">type: list</span></li>
                    <ul class="ul-self">

                    <li><span class="li-head">id</span> - DSCP WMM mapping numbers (0 - 63). <span class="li-required">required</span> <span class="li-normal">type: int</span>
                    </ul>

            <li><span class="li-head">dscp_wmm_bk</span> - DSCP mapping for background access . <span class="li-normal">type: list</span></li>
                    <ul class="ul-self">

                    <li><span class="li-head">id</span> - DSCP WMM mapping numbers (0 - 63). <span class="li-required">required</span> <span class="li-normal">type: int</span>
                    </ul>

            <li><span class="li-head">dscp_wmm_mapping</span> - Enable/disable Differentiated Services Code Point (DSCP) mapping. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable,  disable</span></li>
            <li><span class="li-head">dscp_wmm_vi</span> - DSCP mapping for video access . <span class="li-normal">type: list</span></li>
                    <ul class="ul-self">

                    <li><span class="li-head">id</span> - DSCP WMM mapping numbers (0 - 63). <span class="li-required">required</span> <span class="li-normal">type: int</span>
                    </ul>

            <li><span class="li-head">dscp_wmm_vo</span> - DSCP mapping for voice access . <span class="li-normal">type: list</span></li>
                    <ul class="ul-self">

                    <li><span class="li-head">id</span> - DSCP WMM mapping numbers (0 - 63). <span class="li-required">required</span> <span class="li-normal">type: int</span>
                    </ul>

            <li><span class="li-head">name</span> - WiFi QoS profile name. <span class="li-required">required</span> <span class="li-normal">type: str</span></li>
            <li><span class="li-head">uplink</span> - Maximum uplink bandwidth for Virtual Access Points (VAPs) (0 - 2097152 Kbps). <span class="li-normal">type: int</span></li>
            <li><span class="li-head">uplink_sta</span> - Maximum uplink bandwidth for clients (0 - 2097152 Kbps). <span class="li-normal">type: int</span></li>
            <li><span class="li-head">wmm</span> - Enable/disable WiFi multi-media (WMM) control. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable,  disable</span></li>
            <li><span class="li-head">wmm_uapsd</span> - Enable/disable WMM Unscheduled Automatic Power Save Delivery (U-APSD) power save mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable,  disable</span>
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
      - name: Configure WiFi quality of service (QoS) profiles.
        fortios_wireless_controller_qos_profile:
          host:  "{{ host }}"
          username: "{{ username }}"
          password: "{{ password }}"
          vdom:  "{{ vdom }}"
          https: "False"
          state: "present"
          wireless_controller_qos_profile:
            bandwidth_admission_control: "enable"
            bandwidth_capacity: "4"
            burst: "enable"
            call_admission_control: "enable"
            call_capacity: "7"
            comment: "Comment."
            downlink: "9"
            downlink_sta: "10"
            dscp_wmm_be:
             -
                id:  "12"
            dscp_wmm_bk:
             -
                id:  "14"
            dscp_wmm_mapping: "enable"
            dscp_wmm_vi:
             -
                id:  "17"
            dscp_wmm_vo:
             -
                id:  "19"
            name: "default_name_20"
            uplink: "21"
            uplink_sta: "22"
            wmm: "enable"
            wmm_uapsd: "enable"



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
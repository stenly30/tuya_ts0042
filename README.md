# tuya_ts0042

Zigbee2MQTT - Tuya 2-Button Switch (MQTT Subscribe and Filter) Blueprint
Overview

This Home Assistant blueprint is designed for the Tuya TS0042 2-button Zigbee device. The blueprint supports six distinct actions:

    Button 1 Single Press (1_single)
    Button 1 Double Press (1_double)
    Button 1 Long Press (1_hold)
    Button 2 Single Press (2_single)
    Button 2 Double Press (2_double)
    Button 2 Long Press (2_hold)

It also supports multiple devices and a variety of automation modes.
Features

    MQTT Integration: Listens to MQTT messages from Zigbee2MQTT.
    Device Filtering: Ensures only messages from the selected Tuya TS0042 device(s) trigger the automation.
    Flexible Action Mapping: Customize actions for each button press type.
    Multiple Device Support: Use a single blueprint for one or more devices.
    Automation Modes: Choose from single, restart, queued, or parallel to control how automation instances behave.

Installation

    Save the Blueprint File:
        Copy the blueprint YAML code and save it in your Home Assistant configuration directory under blueprints/automation/tuya_ts0042.yaml.

    Import the Blueprint:
        In Home Assistant, go to Settings > Automations & Scenes > Blueprints.
        Click Import Blueprint and provide the path or paste the YAML code.

Usage

    Create an Automation:
        After importing the blueprint, create a new automation using it.
        Select your Tuya TS0042 device(s) from the device selector.

    Configure Actions:
        Assign the desired actions for each button press type (e.g., call light.turn_on for a short press or cover.open_cover for a long press).
        Each action is linked to a specific payload command (1_single, 1_double, 1_hold, etc.).

    Select an Automation Mode:
        Choose the automation mode that fits your needs (e.g., parallel for simultaneous execution of multiple actions).

    Save and Test:
        Save your automation and test it by pressing the buttons on your Tuya TS0042 device to verify that the corresponding actions are executed.

License

This blueprint is provided "as-is" without any warranty. You are free to use and modify it as needed.

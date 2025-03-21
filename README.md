# Zigbee2MQTT - Tuya 2-Button Switch (MQTT Subscribe and Filter)

This repository contains a Home Assistant blueprint designed for the Tuya TS0042 2‑button Zigbee device. When a button action (e.g. `1_single`, `1_double`, `1_hold`, `2_single`, `2_double`, `2_hold`) is received from a Tuya TS0042 device, the corresponding automation action is triggered.

## Features

- **MQTT Integration:** Listens to MQTT messages from Zigbee2MQTT.
- **Device Filtering:** Only triggers automations for the selected Tuya TS0042 device(s).
- **Flexible Action Mapping:** Customize actions for each button press type.
- **Multiple Device Support:** Use one blueprint for one or more devices.
- **Automation Modes:** Choose from `single`, `restart`, `queued`, or `parallel` to control how automation instances behave.

## Installation

1. **Save the Blueprint File:**
   - Copy the blueprint YAML code from this repository and save it into your Home Assistant configuration directory under `blueprints/automation/tuya_ts0042.yaml`.

2. **Import the Blueprint:**
   - In Home Assistant, navigate to **Settings > Automations & Scenes > Blueprints**.
   - Click **Import Blueprint** and provide the path or paste the YAML code.

## Usage

1. **Create an Automation:**
   - After importing the blueprint, create a new automation using it.
   - Select your Tuya TS0042 device(s) from the device selector.

2. **Configure Actions:**
   - Define the actions for each button press type (short press, double press, long press) as needed.
   - The blueprint maps payload commands (`1_single`, `1_double`, `1_hold`, `2_single`, `2_double`, `2_hold`) to the corresponding action.

3. **Select an Automation Mode:**
   - Choose the automation mode that best fits your use case (e.g., `parallel` for simultaneous execution of multiple actions).

4. **Save and Test:**
   - Save your automation and test it by pressing the buttons on your Tuya TS0042 device to ensure the expected actions are executed.
          - "{{ command == '2_hold' }}"
        sequence: !input button_two_long_press

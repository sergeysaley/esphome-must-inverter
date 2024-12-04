# Must Solar Inverter ESPHome Monitor

This repository contains an **ESPHome YAML configuration** for monitoring and controlling the Must Solar Inverter. The configuration leverages ESP32 with Modbus communication to interact with the inverter, providing detailed insights into its operational parameters and status.

## Features

- **Real-time Monitoring**:
  - Battery voltage, current, and power.
  - PV charger states, voltage, current, and power.
  - Inverter operational states including grid, load, and bus metrics.
  - Temperature readings for various components (radiator, transformer, etc.).
  
- **Energy Metrics**:
  - Accumulated power for charging, discharging, buying, selling, and load consumption.
  - AC and DC operational power and energy states.

- **Customizable Controls**:
  - Energy use modes (e.g., Solar-first, Utility-only).
  - Charger source priorities and voltage configurations.

## Prerequisites

- **Hardware**:
  - ESP32 board recommended (I used WT32-ETH, [AliExpress](https://www.aliexpress.com/item/1005006074972994.html)).
    It also works with ESP8266.
  - RS485 to UART board. I used this one: [AliExpress](https://www.aliexpress.com/item/1005001621746811.html)
- **Software**:
  - [ESPHome](https://esphome.io/) installed.
  - Home Assistant (optional but recommended).

## Usage

1. Clone this repository.
2. Replace placeholders (`wifi_ssid`, `wifi_password`, `api_key`, `ota_password`) with your specific configurations in the `yaml` file.
3. Flash the ESP32 board with this YAML file using ESPHome.
4. Connect the ESP32 to the inverter's communication port.
5. Access real-time data through Home Assistant or ESPHome dashboard.

## Notes

- Adjust logging levels (`INFO`, `DEBUG`) based on performance needs.

## License

This project is licensed under the MIT License. Feel free to use and modify the code as needed.

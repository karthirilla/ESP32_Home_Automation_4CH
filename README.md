# ESP32-S3 Based Home Automation

## Overview

The **ESP32-S3 Based Home Automation** system is designed to provide an intelligent, fully automated home experience by controlling multiple home appliances like AC units, lighting, and audio systems. The system uses the **ESP32-S3** microcontroller to monitor and control these devices based on real-time inputs, such as temperature, humidity, and manual switches. The system supports a wide range of power inputs and communication protocols, including **RS232**, **RS485**, **BLE**, and **MQTT** for remote control and automation.

This project integrates various technologies and is designed for both local and remote management, providing flexibility for home automation. It features temperature and humidity-based automation, relay control with individual status LEDs, real-time communication, and compatibility with external hardware.

![Front View](https://github.com/karthirilla/ESP32_Home_Automation_4CH/blob/main/ESP32_HOME_AUTOMATION_4CH_FRONT.png)
![Back View](https://github.com/karthirilla/ESP32_Home_Automation_4CH/blob/main/ESP32_HOME_AUTOMATION_4CH_BACK.png)

### Key Features

- **Relay Control**: 4-channel isolated relay outputs to control AC appliances and other home devices.
- **Temperature & Humidity Automation**: Inbuilt **DHT22** or similar sensor for real-time temperature and humidity monitoring.
- **Status LEDs**:
  - **Individual Relay Status LEDs**: Indicate the status of each relay (on/off).
  - **WS2812 LED**: RGB LED status to show Wi-Fi connection, MQTT connection status, and hardware errors.
- **Power Supply**: Wide input range (5V to 46V), making the system adaptable to various power sources.
- **Communication Protocols**:
  - **RS232/RS485**: Direct support for these communication modules to integrate with other home automation systems.
  - **BLE (Bluetooth Low Energy)**: Control devices via a mobile app or Bluetooth mesh.
  - **MQTT**: Enables cloud-based control and automation, compatible with home automation systems like **Google Home**.
- **Timer-Based Control**: Automates relay switching based on preset timers.
- **Expansion Connector**: Additional connectors to add more devices for automation (e.g., lighting, audio systems).
- **Mobile App Integration**: Control and monitor the system using mobile apps via BLE or MQTT.
- **Google Home Integration**: Automate and control appliances via Google Home through MQTT.

## System Components

1. **ESP32-S3 Microcontroller**: The heart of the system, enabling Wi-Fi, BLE, and MQTT communication.
2. **4-Channel Isolated Relay Outputs**: Control various appliances, including AC units and lighting.
3. **AHT20 (Temperature & Humidity Sensor)**: Monitors room temperature and humidity for automation.
4. **Status LEDs**:
   - **Individual Relay LEDs**: Show the status of each controlled relay.
   - **WS2812 RGB LED**: Displays Wi-Fi, MQTT, and system status.
5. **Wide Input Power Supply**: Supports 5V to 46V power input for flexibility.
6. **RS232/RS485 Modules**: Direct integration for communication with external devices.
7. **Expansion Connector**: Allows you to add more devices, such as additional relays or home automation components.
8. **External Modules (Optional)**: For lighting control, audio systems, and other appliances.

## Features in Detail

### 1. **Relay Control with Isolated Inputs**
The system includes 4 channels of isolated switch inputs and relay outputs:
- Each relay is controlled based on user input or automation scripts.
- **Status LEDs** are provided for each relay to indicate whether the relay is ON or OFF.

### 2. **Temperature and Humidity Automation**
- The system uses the **DHT22 sensor** to monitor room temperature and humidity.
- **Automation Logic**: If the temperature exceeds or falls below a specified threshold, the system automatically controls the relays to manage the connected AC unit or heater.
- You can adjust thresholds and timers via mobile control or MQTT.

### 3. **Wi-Fi and MQTT Communication**
- The **ESP32-S3** connects to Wi-Fi and uses **MQTT** for cloud-based communication.
- The **MQTT Protocol** ensures real-time updates and control over the system from any device connected to the network, including smartphones, tablets, and PCs.

### 4. **BLE Control**
- The system supports **Bluetooth Low Energy (BLE)** for local control via a mobile app.
- BLE allows communication with mobile devices directly for controlling the system without requiring Wi-Fi or Internet access.

### 5. **WS2812 LED Indicators**
- **Wi-Fi Connection**: The WS2812 LED provides real-time feedback on Wi-Fi connection status (solid color for connected, blinking for disconnected).
- **MQTT Connection**: Indicates the status of the MQTT connection (green for connected, red for disconnected).
- **Hardware Error**: A blinking red LED will signal any system errors.

### 6. **RS232 and RS485 Modules**
- Supports **RS232** and **RS485** communication modules for integration with other industrial or home automation systems.
- These modules allow the system to communicate with existing devices that use these protocols.

### 7. **Wide Power Supply Range (5V to 46V)**
- The system supports a wide input voltage range, making it adaptable to various power sources and ideal for diverse home automation setups.

### 8. **Expansion Connector**
- The system includes an expansion connector, which enables you to easily add additional devices, such as relays, sensors, and other home automation components.
  
### 9. **Google Home Integration**
- Integrates with **Google Home** for voice-based control via MQTT.
- Use voice commands to control devices connected to the system.

### 10. **Mobile Control and BLE Mesh**
- The system can be controlled directly from a mobile app through **BLE**.
- **BLE Mesh** technology allows multiple devices to communicate with each other in a network, enabling extended control over multiple ESP32-S3 devices in the home.

---

## Design and Development Process

### 1. **PCB Design**
The **PCB design** for the system was done using **EasyEDA**. The PCB design includes the ESP32-S3 microcontroller, relay control circuitry, temperature sensor, and all necessary connectors for power input, RS232/RS485 modules, and expansion.

### 2. **PCB Assembly and Testing**
The assembly of the **PCBs** was done using a **reflow oven**, ensuring proper soldering of components. Post-assembly, each board was thoroughly tested to ensure:
- Proper operation of relays.
- Accurate temperature and humidity readings.
- Stable communication via **Wi-Fi**, **MQTT**, and **BLE**.
- Integration with **Google Home**.

### 3. **Software Development**
The software was written in **Arduino C++** for the ESP32-S3 platform, handling:
- Relay control based on temperature, humidity, or manual inputs.
- Wi-Fi and MQTT communication for cloud-based control.
- BLE support for mobile app control and BLE mesh functionality.
- Real-time status updates via WS2812 LEDs.

---

## Hardware Overview

- **Microcontroller**: ESP32-S3
- **Relays**: 4-channel isolated relay module for AC control
- **Sensor**: DHT22 (temperature and humidity)
- **LEDs**: WS2812 (for Wi-Fi, MQTT, and error status)
- **Power Supply**: 5V to 46V input range
- **Communication Modules**: RS232, RS485
- **Expansion Connector**: For additional home automation devices

---

## Contributing

This project is an internal company initiative, so contributions are not open to external sources. However, you are welcome to adapt this system for personal or academic use and make improvements as needed.

---

## License

This project is proprietary and is not open-source.

---

## Acknowledgments

- **ESP32-S3**: Thanks to Espressif for providing the powerful ESP32 platform, perfect for home automation applications.
- **DHT22**: Thanks to the creators of the DHT22 sensor for providing an affordable, reliable solution for monitoring temperature and humidity.
- **EasyEDA**: For offering a robust PCB design tool that made the hardware development process smoother.

---

## Additional Notes

- This system is fully scalable, allowing for additional modules and expansion for more complex home automation tasks (e.g., lighting, audio).
- The wide input voltage range makes it flexible for use in various geographical regions with different power supply standards.

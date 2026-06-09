# 🌿 SmartGardenIoT-ESP32 - Automated plant care for home gardens

[![Download SmartGarden](https://img.shields.io/badge/Download-Software-blue.svg)](https://github.com/vanesselo9574/SmartGardenIoT-ESP32)

This software helps you manage your indoor or outdoor garden. It connects your ESP32 hardware to a simple dashboard on your computer. You can track soil moisture, trigger water pumps, and set watering schedules.

## 🛠 Prerequisites

Before you start, ensure your computer meets these requirements:

1. Windows 10 or Windows 11.
2. At least 4GB of RAM.
3. An active internet connection for the initial setup.
4. A USB cable compatible with your ESP32 device.

## 📥 Getting the software

You need to access the official project page to download the necessary files.

[Click here to visit the download page](https://github.com/vanesselo9574/SmartGardenIoT-ESP32)

Locate the section labeled "Releases" on the right side of the page. Select the latest version listed. Download the file ending in `.zip` to your computer.

## ⚙️ Installation steps

Follow these steps to prepare your system once the download finishes:

1. Open your Downloads folder.
2. Right-click the downloaded file and select "Extract All".
3. Choose a permanent location for the folder, such as your Documents or Desktop.
4. Open the extracted folder to view the project files.

## 🔌 Connecting your hardware

The software talks to your garden hardware through a USB cable. 

1. Plug your ESP32 board into an available USB port on your computer.
2. Wait for Windows to identify the device.
3. If you see a notification about new hardware, wait for the installation to finish automatically.
4. Keep the device plugged in during the entire setup process.

## 🚀 Running the application

The system consists of two parts: the backend server and the visual dashboard.

1. Locate the file named `start_system.bat` inside the project folder.
2. Double-click this file.
3. A black box called a Command Prompt will appear. This window starts the background services needed to talk to your plants.
4. Keep this window open. If you close it, the garden monitoring stops.
5. Open your web browser (Chrome, Firefox, or Edge).
6. Type `http://localhost:8000` into the address bar and press Enter.

## 📊 Using the dashboard

The dashboard provides a simple interface to manage your garden. 

### Monitor moisture levels
The main screen shows a chart for each plant sensor. These charts update every few seconds to show the current soil status. Green levels indicate healthy soil, while yellow or red levels suggest the plant needs water.

### Manual watering
Find the "Control" tab. Every connected pump has a toggle switch next to it. Click the switch to turn the pump on. Click it again to turn it off. Use this feature to test if your equipment works properly.

### Watering schedules
Set automatic rules in the "Schedule" tab:
1. Click "Add New Schedule".
2. Select the specific pump you want to control.
3. Pick a time of day for the watering event.
4. Set the duration in seconds.
5. Save the rule. The system will handle the watering even if you are not looking at the dashboard.

## 🧠 AI Assistant features

The AI assistant provides suggestions based on the data collected from your soil sensors. If the system detects that your soil stays dry despite frequent watering, it will show a notification. Click on the "Insights" tab to read these suggestions. This helps you figure out if your plants need more water or if a sensor needs cleaning.

## 🔧 Troubleshooting

Common issues often have simple solutions:

- **Dashboard does not load**: Ensure the black Command Prompt window is still open. Check that the ESP32 board is plugged into the USB port.
- **Data does not update**: Refresh your browser page. If the charts remain empty, unplug the ESP32 and plug it back in.
- **Pumps do not start**: Check the physical wiring between the ESP32 and the relay module. Ensure the external power supply for the pump is plugged into a wall outlet.
- **Slow performance**: Close other heavy applications on your computer. The system performs best when it has sufficient memory.

## 🛡 System maintenance

Keep your software updated to get new features and fixes. When a new version releases on the project page, download the new folder and replace the old one. Always back up your custom watering schedules before you replace the folder.

## 🌐 Connecting multiple rooms

The system supports multiple ESP32 boards. You can rename each board in the "Settings" tab. This helps you track different garden zones like "Living Room" or "Backyard". Each board must have its own unique ID assigned in the configuration file if you plan to use more than five devices simultaneously.

## 📝 Configuration notes

Advanced users can edit the settings file located in the `config` folder. You can change the port numbers or the refresh rate of the dashboard. Do not change these settings unless the system fails to connect, as the default values work for most home setups.

## 🛑 Stopping the system

When you finish managing your garden, you can safely stop the application:

1. Close the browser tab.
2. Return to the black Command Prompt window.
3. Press `Ctrl + C` on your keyboard.
4. Confirm you want to stop the service.
5. Close the window. 
6. You may now unplug the ESP32 hardware.
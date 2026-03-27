# 🧺 Miele Appliance Custom Card & Generator for Home Assistant

[Русский](README.md) | 🌐 **English**

[![Home Assistant](https://img.shields.io/badge/Home_Assistant-Dashboard-blue.svg)](https://www.home-assistant.io/)

An interactive custom card for Miele washing and drying machines (W1/T1 models) and a **built-in HTML generator** for quick setup without manually writing complex code.

## 📸 Gallery

<p align="center">
  <img src="https://github.com/user-attachments/assets/de27cd22-c60b-4963-af59-02b6c4b16654" alt="Overview" width="800">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/692fc4a2-0797-4759-b871-1422a7d74700" alt="Screenshot 1" width="220">
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/e58f489b-fff7-48b1-8b67-80f270303b09" alt="Screenshot 2" width="220">
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/adb5381b-1403-4a35-922a-0caf50d287c0" alt="Screenshot 3" width="220">
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/d49a0c81-8f27-4cc4-88b3-5069e90e383f" alt="Dryer screenshot" width="220">
</p>

## ✨ Features

No more huge YAML sheets! A lightweight and smooth custom card that works out of the box.

* ⭕ **Progress Ring:** Dynamic SVG indication around the door that smoothly fills with orange color as the program progresses.
* 💧 **TwinDos (Washing Machines):** Phase 1 and Phase 2 containers visually display the remaining detergent in real-time.
* 🌪️ **Smart Filter (Tumble Dryers):** The card adapts the interface for a tumble dryer and displays a flashing notification when the filter needs cleaning.
* 🎛️ **Smart Controls:** Context-aware Start/Stop buttons (appear only when needed) and a Power button that changes color depending on the state.
* 🔒 **Interactivity:** Clicking on metrics (drum, remaining time, water, energy, door) opens standard Home Assistant history graphs (More Info).
* ⚡ **Zero Dependencies:** No more third-party integrations like `card-mod` or `button-card` are needed. All the magic is built into one isolated JS file!
* 🌍 **Multi-language:** On-the-fly translation of washing and drying programs and phases (built-in support for En, Ru, De).

## ⚙️ Custom Sensors (Advanced Settings)

If your sensor names differ from those created by the official Miele integration (e.g., you renamed them or use an MQTT bridge), **the card will easily adapt to your setup**.

In the HTML generator, click the **"⚙️ Advanced Settings"** button. A list of all expected sensors will appear. Simply type your custom `entity_id`s into the appropriate fields, and the generator will automatically add the override configurations to your final YAML code!

## 🚀 Installation and Usage

1. **Download the files.** Download the plugin code `miele-appliance-card.js`, the HTML generator `miele_card_generator.html`, and the background-free images (`washer.webp` and/or `dryer.webp`) from this repository.

2. **Add the plugin to Home Assistant.**
   * Create a `miele` folder at the path `config/www/` (if it doesn't exist).
   * Place the downloaded image files and the `miele-appliance-card.js` file into the `config/www/miele/` folder.
   * In the Home Assistant interface, go to *Settings -> Dashboards -> Resources*.
   * Click "Add Resource", enter the URL: `/local/miele/miele-appliance-card.js`, and select the **JavaScript Module** type.

3. **Generate the code.**
   * Open the `miele_card_generator.html` file in any browser on your computer.
   * Select your machine type (Washer or Dryer) and enter its entity prefix (for example, if the time sensor is named `sensor.washer_remaining_time`, your prefix is `washer`).
   * *(Optional) Map any custom sensor names in the Advanced Settings.*
   * Copy the generated short YAML code.

4. **Add to dashboard.**
   * Clear your browser cache (`Cmd+Shift+R` or `Ctrl+F5`) so Home Assistant "sees" the new JS file.
   * In your Home Assistant dashboard edit mode, click "Add Card" -> scroll down and select **Manual**.
   * Paste the copied YAML code and save!

## 👨‍💻 Author

Developed by [Eugen417](https://github.com/Eugen417) for beautiful integration of Miele appliances (PowerWash, TwinDos, Heat Pump Dryers) into Home Assistant.

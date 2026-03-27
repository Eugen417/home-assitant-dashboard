# 🧺 Miele Appliance Custom Card & Generator for Home Assistant

[Русский](README.md) | 🌐 **English**

[![Home Assistant](https://img.shields.io/badge/Home_Assistant-Dashboard-blue.svg)](https://www.home-assistant.io/)

An interactive custom card for Miele washing and drying machines (W1/T1 models) and a **built-in HTML generator** for quick setup without manually writing complex code.

## 📸 Gallery

<p align="center">
  <img src="https://github.com/user-attachments/assets/b85d3631-dce2-4e17-916b-4466e61a9223" alt="Overview" width="800">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/692fc4a2-0797-4759-b871-1422a7d74700" alt="Screenshot 1" width="250">
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/e58f489b-fff7-48b1-8b67-80f270303b09" alt="Screenshot 2" width="250">
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/adb5381b-1403-4a35-922a-0caf50d287c0" alt="Screenshot 3" width="250">
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
   * Copy the generated short YAML code (only 4 lines!).

4. **Add to dashboard.**
   * Clear your browser cache (`Cmd+Shift+R` or `Ctrl+F5`) so Home Assistant "sees" the new JS file.
   * In your Home Assistant dashboard edit mode, click "Add Card" -> scroll down and select **Manual**.
   * Paste the copied YAML code and save!

## 👨‍💻 Author

Developed by [Eugen417](https://github.com/Eugen417) for beautiful integration of Miele appliances (PowerWash, TwinDos, Heat Pump Dryers) into Home Assistant.

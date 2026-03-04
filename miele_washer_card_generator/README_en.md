# 🧺 Miele W1 Interactive Card Generator for Home Assistant

[Русский](README.md) | 🌐 **English**

[![Home Assistant](https://img.shields.io/badge/Home_Assistant-Dashboard-blue.svg)](https://www.home-assistant.io/)
[![HACS](https://img.shields.io/badge/HACS-Custom_Card-orange.svg)](https://hacs.xyz/)

An interactive Picture Elements card for Miele washing machines (specifically designed for W1 models with TwinDos) and a **built-in HTML code generator** for quick setup without manually editing YAML.

<p align="center">
  <img src="washer.webp" alt="Miele Washer" width="300">
</p>

## 📸 Gallery

<p align="center">
  <img src="https://github.com/user-attachments/assets/8e72f698-32e8-4009-a9a2-58659ae3cd75" alt="Overview" width="800">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/692fc4a2-0797-4759-b871-1422a7d74700" alt="Screenshot 1" width="250">
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/e58f489b-fff7-48b1-8b67-80f270303b09" alt="Screenshot 2" width="250">
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/adb5381b-1403-4a35-922a-0caf50d287c0" alt="Screenshot 3" width="250">
</p>

## ✨ Features

No need to dig into dozens of lines of code. Just enter your machine's prefix in the generator, and it will output ready-to-use YAML!

* ⭕ **Progress Ring:** Dynamic LED-style indicator around the door that fills with orange color as the washing cycle progresses.
* 💧 **Dynamic TwinDos:** Phase 1 and Phase 2 containers visually fill and empty in real-time based on the remaining detergent percentage.
* 🎛️ **Smart Controls:** Context-aware Start/Stop buttons (appear only when needed) and a Power button that changes color based on the machine's state.
* 🔒 **Lock Indicator:** Visual door status (open/closed).
* ⚡ **Statistics:** Minimalist indicators for current water and energy consumption.
* 🌍 **Multi-language:** The generator and the generated card support English, German, and Russian with a single click.

## ⚙️ Requirements

The **card-mod** plugin is required for CSS gradients (progress ring and dynamic TwinDos filling) to work.
* Install [lovelace-card-mod](https://github.com/thomasloven/lovelace-card-mod) via **HACS** (Frontend section).

## 🚀 Installation and Usage

1. **Download the files**
   Download the generator file [miele_washer_card_generator.html](miele_washer_card_generator.html) and the background-free image [washer.webp](washer.webp) from this repository.

2. **Upload the image to Home Assistant**
   * Go to your Home Assistant configuration folder (where `configuration.yaml` is located).
   * Create a `www` folder (if it doesn't exist), and a `miele` folder inside it.
   * Place the downloaded `washer.webp` file at this path: `config/www/miele/washer.webp`.
   * **Restart Home Assistant.** After that, the image will be available to the system at the local path `/local/miele/washer.webp`.

3. **Generate the code**
   * Open the downloaded `miele_washer_card_generator.html` file in any browser on your computer. *(If you place the `washer.webp` image in the same folder, the generator will show a beautiful preview).*
   * Select your preferred interface language.
   * Enter the entity prefix of your washing machine. For example, if the time sensor is named `sensor.washer_remaining_time`, your prefix is **washer**.
   * Click **"Generate Code"** and copy the result.

4. **Add to dashboard**
   * Enter edit mode on your Home Assistant dashboard.
   * Click "Add Card" -> scroll down and select **Manual**.
   * Paste the copied code and save!

## 👨‍💻 Author
Developed by [Eugen417](https://github.com/Eugen417) for integrating Miele (PowerWash & TwinDos & Steam Passion) washing machines into Home Assistant.

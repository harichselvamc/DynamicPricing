# Dynamic Pricing Based on Device and Battery Level

## Overview
This project dynamically calculates the price of a product or service based on the user's device type (iPhone, Android, Windows, macOS) and battery level. The price varies depending on the battery percentage and the detected device, with higher prices for lower battery levels and different prices based on the platform.

## Logic Explanation

1. **Device Detection**:
   The script uses the `navigator.userAgent` property to detect the type of device accessing the page. It checks for:
   - iPhone, iPad, iPod (iOS devices)
   - Android devices
   - Windows operating system
   - macOS operating system

2. **Battery Status**:
   The `navigator.getBattery()` API is used to retrieve the device's battery level. This gives us a percentage value that represents the current battery charge.

# 3. Price Calculation

## Price Calculation Based on Device Type and Battery Percentage (INR)

This system calculates the price of a service based on the **device type** (iPhone, Android, Windows, macOS, or unknown) and the **battery percentage** of the device. The price changes depending on the battery level, where lower prices are applied to devices with higher battery percentages, and higher prices are applied when the battery is lower.

---

## Price Calculation Rules:

### iPhone:
- If the battery percentage is above 80%: ₹40
- If the battery percentage is between 61% and 80%: ₹110
- If the battery percentage is between 41% and 60%: ₹180
- If the battery percentage is between 21% and 40%: ₹270
- If the battery percentage is below 20%: ₹360

### Android:
- If the battery percentage is above 80%: ₹90
- If the battery percentage is between 61% and 80%: ₹140
- If the battery percentage is between 41% and 60%: ₹170
- If the battery percentage is between 21% and 40%: ₹260
- If the battery percentage is below 20%: ₹350

### Windows:
- If the battery percentage is above 80%: ₹90
- If the battery percentage is between 61% and 80%: ₹120
- If the battery percentage is between 41% and 60%: ₹150
- If the battery percentage is between 21% and 40%: ₹230
- If the battery percentage is below 20%: ₹330

### macOS:
- If the battery percentage is above 80%: ₹40
- If the battery percentage is between 61% and 80%: ₹70
- If the battery percentage is between 41% and 60%: ₹138
- If the battery percentage is between 21% and 40%: ₹220
- If the battery percentage is below 20%: ₹290

### Unknown Device:
- If the device is unrecognized, the default price is set to ₹60.

---

This calculation system automatically adjusts the price based on your device's battery level to provide a dynamic and fair pricing model. The lower your battery, the higher the price you will pay!


4. **UI and Styling**:
   - The page is styled with a gradient background and a container in the center showing the price, device type, and battery level.
   - The price color changes based on the battery level: green for high battery and red for low battery.
   - The page provides a smooth hover effect on the container for better user experience.

## How to Use
1. Open the HTML file in a web browser.
2. The script will automatically detect your device and battery level and display the dynamic price.

## Technologies Used
- HTML
- CSS
- JavaScript (for device detection and battery status)

## Demo Link
You can view the live version of the project here: [Dynamic Pricing Demo](https://harichselvamc.github.io/DynamicPricing/)


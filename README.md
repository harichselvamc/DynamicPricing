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

3. **Price Calculation**:
   - The price changes depending on the device type and battery percentage.
   - If the battery percentage is above 50%, a lower price is applied.
   - If the battery percentage is 50% or below, a higher price is set.
   - Price ranges are set for each device type (in INR):
     - iPhone: ₹180 (high battery) / ₹250 (low battery)
     - Android: ₹120 (high battery) / ₹200 (low battery)
     - Windows: ₹70 (high battery) / ₹130 (low battery)
     - macOS: ₹250 (high battery) / ₹350 (low battery)
   - For unknown devices, a default price of ₹150 is used.

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


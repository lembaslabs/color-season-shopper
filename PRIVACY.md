# Privacy Policy for Color Season Shopper

**Last Updated:** December 29, 2025

## Overview

Color Season Shopper is a Chrome extension that helps you identify and collect colors from webpages that match your personal seasonal color palette. This privacy policy explains what data the extension stores and how it's used.

## Data Collection and Storage

Color Season Shopper stores the following data **locally on your device** using Chrome's storage API:

- **Color Season Preference:** Your selected season (Spring, Summer, Autumn, or Winter)
- **Picked Colors:** Hex color codes you select using the eyedropper tool
- **Website Information:** URLs and page titles of websites where you picked colors
- **Timestamps:** Date and time when colors were picked

## Data Privacy

### What We DON'T Do

- ❌ **No data transmission:** No data is sent to external servers or third parties
- ❌ **No personal information:** We don't collect names, emails, addresses, or any personally identifiable information
- ❌ **No tracking:** No analytics, tracking pixels, or behavior monitoring
- ❌ **No third-party services:** No external services, APIs, or data processors are used
- ❌ **No selling of data:** Your data is never sold, rented, or shared with anyone

### What We DO

- ✅ **Local storage only:** All data stays on your device in Chrome's secure storage
- ✅ **Optional sync:** If you enable Chrome Sync, your color collections sync across your devices via Google's infrastructure (controlled by your Chrome settings, not us)
- ✅ **User control:** You have complete control over your data at all times

## How We Use Data

The stored data is used solely for the extension's core functionality:

1. **Season Preference:** Remembers your chosen season to show which colors match your palette
2. **Color Collections:** Saves picked colors so you can reference them later
3. **Website Organization:** Groups colors by website for easy navigation
4. **Timestamps:** Displays when colors were picked for your reference

## Permissions Explained

The extension requests the following Chrome permissions:

### activeTab
**Why:** To access webpage content when you use the eyedropper tool
**How it's used:** Only activates when you click "Start selecting" to read pixel colors from the page
**Scope:** Only affects the currently active tab

### scripting
**Why:** To inject the eyedropper functionality into webpages
**How it's used:** Programmatically adds the color picker interface when you request it
**Scope:** Only runs when you explicitly activate the eyedropper

### storage
**Why:** To save your color season and collected colors
**How it's used:** Stores your preferences and color collections locally in Chrome storage
**Scope:** Limited to extension data only

### host_permissions (<all_urls>)
**Why:** To enable color picking from any website you visit
**How it's used:** Allows you to use the eyedropper on any webpage without restriction
**Scope:** Only accesses pages when you activate the eyedropper; reads only color values, not page content

## Your Data Rights

You have complete control over your data:

- **View:** All collected colors are visible in the extension popup
- **Delete Individual Colors:** Click the delete button on any color card
- **Clear Website Collections:** Use the "Reset" button to remove all colors from a specific website
- **Delete All Data:** Uninstall the extension to completely remove all stored data
- **Export:** Copy individual hex codes using the copy button

## Data Retention

- **Automatic cleanup:** Colors are automatically deleted when you close all tabs for a website domain
- **Session-based storage:** Data persists only while you have tabs open for that domain
- **Example:** If you pick colors from amazon.com/item1 and amazon.com/item2, those colors are kept until you close all amazon.com tabs
- **Manual deletion:** You can also delete individual colors or entire website collections at any time
- **Uninstalling:** Removes all local data immediately

## Children's Privacy

Color Season Shopper does not knowingly collect any information from children. The extension is designed for general audiences and does not target children specifically.

## Changes to This Policy

We may update this privacy policy from time to time. Any changes will be reflected by updating the "Last Updated" date at the top of this policy. Continued use of the extension after changes constitutes acceptance of the updated policy.

## Open Source

Color Season Shopper is built with transparency in mind. You can review the source code to verify these privacy practices.

## Contact

If you have questions or concerns about this privacy policy or the extension's data practices, please contact:

- **Email:** [Your email address]
- **GitHub Issues:** [Your GitHub repository URL]/issues

## Technical Details

### Data Format
Colors are stored in the following format:
```json
{
  "chosenSeason": "Spring",
  "colorGroups": {
    "https://example.com": {
      "url": "https://example.com",
      "pageTitle": "Example Page",
      "baseDomain": "example.com",
      "firstPickedDate": "2025-12-22",
      "colors": [
        {
          "hex": "#FF5733",
          "season": "Autumn",
          "timestamp": 1703250000000,
          "date": "2025-12-22"
        }
      ]
    }
  }
}
```

### Storage Location
- **Chrome Storage API:** `chrome.storage.sync`
- **Maximum Size:** 100KB (Chrome's sync storage limit)
- **Encryption:** Handled by Chrome's built-in storage encryption

## Compliance

This extension complies with:
- Chrome Web Store Developer Program Policies
- Chrome Extension Manifest V3 requirements
- General Data Protection Regulation (GDPR) principles of data minimization and user control

---

**Summary:** Color Season Shopper is a privacy-first extension. All data stays local on your device, nothing is transmitted externally, and you maintain complete control over your information.

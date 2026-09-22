<img width="1710" height="1107" alt="image" src="https://github.com/user-attachments/assets/80fdba6f-7503-4b33-b58c-e4324f968ab4" />
<img width="1710" height="1107" alt="image" src="https://github.com/user-attachments/assets/001c11bb-c9ad-4cb2-b67f-7a6923b5bc23" />

# Amazon Web Scraper to Apple Notes (UiPath RPA)

A cross-platform Robotic Process Automation (RPA) workflow developed with **UiPath Studio Web** and executed on macOS via **UiPath Assistant**.

---

## 📌 Project Overview
* **Web Application:** Google Chrome (`Amazon.in`)
* **Desktop Application:** Native macOS Apple Notes (`Notes.app`)
* **Target Runtime:** UiPath Cross-Platform Runtime (.NET Core)
* **Execution Client:** UiPath Assistant for Mac

---

## ⚙️ Workflow Architecture
1. **Target Attachment (`Use Application/Browser`):** Connects to the active Google Chrome window on Amazon.in.
2. **UI Scraping (`Get Text`):** Dynamically extracts live navigation items (`Today's Deals`, `Coupons`, `Flights`) into runtime variables.
3. **Application Control:** Launches or switches focus to macOS `Notes.app`.
4. **Shortcut Trigger:** Sends `Cmd + N` to create a new note document.
5. **Data Population (`Type Into`):** Types extracted variable data using newline expressions (`Environment.NewLine`).

---

## 📁 Repository Structure
```text
├── Main.xaml          # Main automation workflow
├── project.json       # Project dependencies and configuration
├── project.uiproj     # UiPath project metadata
└── .gitignore         # Ignores runtime cache, logs, and screenshots# UiPath macOS Automation Solution

A cross-platform Robotic Process Automation (RPA) solution developed in **UiPath Studio Web** and executed via **UiPath Assistant** on macOS. This repository contains modular automations combining native macOS desktop applications and web browsers.

---

## 📂 Included Projects

### 1. Amazon Web Scraper to Apple Notes (`Amazon_scraper`)
* **Target Platforms:** Google Chrome (Amazon.in) & Native macOS Apple Notes (`Notes.app`)
* **Key Features:**
  * Connects to Amazon web elements via UI automation.
  * Extracts dynamic navigation elements (`Today's Deals`, `Coupons`, `Flights`) into runtime variables.
  * Launches or switches to the macOS Notes application.
  * Triggers native macOS shortcuts (`Cmd + N`) to create a fresh note.
  * Injects scraped values cleanly into the note editor using dynamic expressions.

---

## 🛠️ Tech Stack & Prerequisites
* **Platform:** UiPath Studio Web, UiPath Assistant for Mac
* **Scripting / Expressions:** VB.NET runtime expressions (`Environment.NewLine`, variable interpolation)
* **Environment:** macOS

---

## 🚀 How to Run Locally

1. **Permissions:**
   Ensure UiPath Robot has accessibility permissions enabled under macOS **System Settings > Privacy & Security > Accessibility**.
2. **Execution:**
   Open **UiPath Assistant** on macOS, select the deployed process, and click **Play (▶)**.

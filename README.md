
![Unreal Engine](https://img.shields.io/badge/Engine-Unreal%20Engine%205-9cf)
![C++](https://img.shields.io/badge/Language-C%2B%2B17-blue)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Mac%20%7C%20Linux-informational)
![Blueprints](https://img.shields.io/badge/Supports-Blueprints-blueviolet)
![Plugin](https://img.shields.io/badge/Type-UE%20Plugin-orange)
![License: MIT](https://img.shields.io/badge/License-MIT-brightgreen)
# ValidatorX – Unreal Engine Blueprint Validation Plugin

**ValidatorX** is a modular plugin for Unreal Engine that automatically detects issues in Blueprints and helps maintain clean, performant, and error-free graphs.

---
![Validator Preview](Documentation/preview_image.jpg)
## 🔍 Features

- Detects **unused nodes** (e.g., disconnected variables, empty events/functions)
- Finds **unused or dead functions and macros**
- Identifies **empty branches**, **empty functions**, and **default values that are never used**
- Warns about **local/global variable name conflicts**
- Tracks **unused event dispatchers**
- Flags **long or overly complex functions**
- Highlights **cyclical dependencies** between Blueprints

---

## ✅ Validators Included

| Validator                         | Description |
|----------------------------------|-------------|
| **UnusedNodeValidator**          | Flags blueprint nodes with no usage or connections |
| **EmptyFunctionValidator**       | Detects functions that are completely empty |
| **UnusedFunctionValidator**      | Finds functions that are never called |
| **EmptyMacroValidator**          | Detects macros that contain no nodes |
| **UnusedMacroValidator**         | Identifies unused macros |
| **LocalVariableNeverUsedValidator** | Finds local variables never read or written |
| **GlobalVariableNeverUsedValidator** | Detects unused Blueprint variables |
| **DefaultAssignmentValidator**   | Flags variables with default values that are never read |
| **EmptyBranchValidator**         | Warns on branches with unconnected outputs |
| **CircularDependencyValidator**  | Detects circular Blueprint dependencies |
| **LocalGlobalNameConflictValidator** | Finds naming conflicts between local/global variables |
| **UnboundEventDispatcherValidator** | Detects dispatchers that are never bound or called |
| **LongFunctionValidator**        | Flags functions that are too large or complex |
| **DeadBranchValidator**         | Detects **dead** branch nodes                  |

---

## 🛠 Installation 
- Create 'Plugins' folder in your project root directory
- Download appropriate version of .zip in releases
- Extract to Plugins folder
- Open your project, and you're done!

## 💻 Usage

In Tools Menu open the Plugin
  ![Validator Preview](Documentation/open_window_plugin.jpg)

Enable the validator you need

  ![Validator Preview](Documentation/check_validator.jpg)

Simply click **Save** or **Validate Asset**.

Open the Message Log window to view any reported issues.
     
  ![Validator Preview](Documentation/warning.jpg)

Double-click the messages to jump directly to the problem nodes.

  ![Validator Preview](Documentation/jump.jpg)

Problematic nodes will display tooltips or optional bubble comments like `⚠ Unused Node`.

  ![Validator Preview](Documentation/unused_node.jpg)
 
---

## 🧩 Integration

- All validators are modular C++ classes
- Can be toggled individually
- Easy to extend with custom validators
- Integrated into `FDataValidationContext` system

---

## 🛠 Development

To create your own validator:
1. Inherit from `UBlueprintValidatorBase`
2. Override `ValidateLoadedAsset_Implementation`
3. Register using the plugin module

---

## ⚠️ Project Status

This project is **not final** and is under active development.  
More validators and improvements will be added over time. Stay tuned for updates!

---

## 📜 License

MIT License (you can change this if needed)

---

## ✨ Contributing

Pull requests are welcome. If you want to add your own validator — feel free to fork and contribute!

---

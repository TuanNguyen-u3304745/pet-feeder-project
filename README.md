# 🐾 Smart Pet Feeder System

A responsive, sensor-driven pet feeder designed to automate scheduled feeding, monitor consumption, and notify users of issues in real time.

## 📌 Overview

This system ensures pets are fed reliably and owners are kept informed. It integrates time-based scheduling, weight sensors, and alert mechanisms to manage feeding routines with minimal human intervention.

## 🎯 Objectives

- Dispense food at scheduled times.
- Monitor food consumption using scale sensors.
- Alert users if food is uneaten or supply is insufficient.
- Provide real-time data on food levels and consumption.

## 🔧 System Inputs

| Input               | Description                                      |
|--------------------|--------------------------------------------------|
| Feeding Time        | Scheduled time for dispensing food              |
| Current Time        | Real-time clock input                           |
| Food Needed         | Amount of food to dispense                      |
| Bowl Weight Sensor  | Measures food remaining in the bowl             |
| Container Sensor    | Measures food available in the feeder container |

## 📤 System Outputs

| Output              | Description                                      |
|---------------------|--------------------------------------------------|
| Motor Control        | Opens/closes dispenser gate                     |
| Alerts               | Notifies user of issues (e.g., uneaten food)    |
| Data Reports         | Remaining food and consumption metrics          |

## 🔄 Workflow Logic

1. **User Input**: Feeding time and required food amount.
2. **Time Check**: Wait until current time matches feeding time.
3. **Calculate Dispense Amount**:  
   `FoodDispensed = FoodNeed - FoodOnBowl`
4. **Check Container Supply**:
   - If insufficient: Send alert.
   - If sufficient: Dispense food.
5. **Monitor Bowl**:
   - Wait 5 minutes.
   - If food remains uneaten: Send alert and report.
6. **Repeat Process**:
   - If container is low: Alert to refill.
   - Otherwise: Wait for next feeding time.

## 🧪 Example Scenario

- **Feeding Time**: `17/08/2025 09:00AM`
- **Food Needed**: `250g`
- **Outcome**:
  - If pet doesn't eat: Alert user and report remaining food.
  - If container is low: Alert user to refill.

## ⚠️ Assumptions & Limitations

- System requires Wi-Fi for alerts.
- Hardware failures (e.g., motor malfunction) may disrupt operation.
- Multiple food types require separate containers.

## 🚀 Suggested Enhancements

- Allow partial dispensing if full amount isn't available.
- Integrate mobile notifications or app-based alerts.
- Support multiple feeding profiles for different pets.

---

**Developed for reliability, automation, and pet well-being.**  
For questions or contributions, please contact the project maintainer.

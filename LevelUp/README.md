[← Back to Main Portfolio](../README.md) | [Studio Portal](https://mundane-76d8e.web.app)

![Compatibility](https://img.shields.io/badge/Compatibility-Unity%202021.3%2B-555555?style=for-the-badge)
![C#](https://img.shields.io/badge/C%23-Clean_Code-239120?style=for-the-badge&logo=c-sharp)
![Architecture](https://img.shields.io/badge/Architecture-Strategy_Pattern-blue?style=for-the-badge)

# 🚀 LevelUp Engine
**The Event-Driven Progression System Compatible with Unity® & Modern C# Engines.**

Stop putting leveling logic inside your `Update()` loop. The LevelUp Engine provides a clean, decoupled architecture to manage experience, levels, and stat curves.

![LevelUp Engine Card](level_card.png)

## Key Features
* ✅ **Strategy Pattern:** Swap leveling math (Linear, Exponential, MMO) instantly via Inspector.
* ✅ **Event-Driven:** UI updates automatically without polling.
* ✅ **Scalable:** Built for projects that plan to grow.

## Code Preview
```csharp
// Clean, readable API designed for Senior Engineers
public void AddExperience(int amount)
{
    _currentXp += amount;
    
    // UI updates automatically via Events
    OnExperienceChanged?.Invoke(_currentXp);
    
    CheckLevelUp();
}

```

---

## 📧 Contact & Support

For bug reports, feature requests, or documentation questions:

**Email:** [alkiren44@gmail.com](mailto:alkiren44@gmail.com)

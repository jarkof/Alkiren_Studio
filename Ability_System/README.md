[← Back to Main Portfolio](../README.md)

![Unity](https://img.shields.io/badge/Unity-2021.3%2B-000000?style=for-the-badge&logo=unity)
![C#](https://img.shields.io/badge/C%23-Clean_Code-239120?style=for-the-badge&logo=c-sharp)
![Architecture](https://img.shields.io/badge/Architecture-Strategy_Pattern-blue?style=for-the-badge)

# Data-Driven Ability System
**The Command & Strategy Framework for Unity.**

Stop hardcoding spells and combat logic. This system decouples **Logic** (C#) from **Data** (ScriptableObjects), allowing designers to assemble complex abilities—like Fireballs, AoE Explosions, and Status Effects—entirely in the Inspector.

![Ability System Card](ability_card.png)

## Key Features
* ✅ **Strategy Pattern:** Swap logic like Lego blocks (e.g., change `RaycastTarget` to `AoETarget` instantly).
* ✅ **Command Pattern:** Encapsulates combat data into a context packet for clean pipeline execution.
* ✅ **Production Ready:** Built-in support for Projectile Physics, Damage-over-Time (DoT), and Object Pooling.

## Code Preview
```csharp
// 1. The Strategy (The Logic)
public class SpawnProjectileEffect : IAbilityEffect
{
    public void Apply(AbilityContext context)
    {
        // Decoupled logic: Spawns prefab and passes data context
        var projectile = Object.Instantiate(_prefab, context.Caster.Transform.position, rotation);
        projectile.Initialize(context.TargetLocation, _damagePayload);
    }
}

// 2. The Configuration (The Data)
[CreateAssetMenu(menuName = "Alkiren/Abilities/New Fireball")]
public class AbilityConfig : ScriptableObject
{
    public CooldownStrategy Cooldown; // e.g., 2 Seconds
    public TargetingStrategy Targeting; // e.g., Raycast 50m
    public List<EffectConfig> Effects;  // e.g., SpawnProjectile -> Explosion -> Damage
}
```

---


## 📧 Contact & Support

For bug reports, feature requests, or documentation questions:

**Email:** [alkiren44@gmail.com](mailto:alkiren44@gmail.com)
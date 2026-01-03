![Banner](Banner.png)

![Unity](https://img.shields.io/badge/Unity-2022.3%2B-000000?style=for-the-badge&logo=unity)
![C#](https://img.shields.io/badge/C%23-Clean_Code-239120?style=for-the-badge&logo=c-sharp)
![Architecture](https://img.shields.io/badge/Architecture-SOLID-blue?style=for-the-badge)

# Professional Architecture Tools
We build robust, event-driven systems to eliminate spaghetti code. Our assets follow strict industry standards (**SOLID**, **Strategy Pattern**, **Observer Pattern**) for serious engineers.

---

## 🛠️ Products

### 🧠 Code-First FSM
**The Hierarchical State Machine for Clean Architecture.**

Stop writing boolean flags in your `Update()` loop. This strictly typed framework lets you build complex AI and character logic using nested states, event triggers, and declarative transitions.

![Code-First FSM Card](FSM_Card.png)

#### Key Features
* ✅ **Hierarchical (HFSM):** Nest states inside states (e.g., `Grounded` > `Walk`).
* ✅ **Visual Debugger:** View active states and history in real-time.
* ✅ **Zero Boilerplate:** Use lambda-based `ActionState` for rapid prototyping.

#### Code Preview
```csharp
// Define logic in pure C# classes (No MonoBehaviours)
var jumpState = new HeroJumpState(_blackboard);

// Declarative Transitions: "Jump when Space is pressed"
groundMachine.AddTransition(jumpState, () => Input.GetKeyDown(KeyCode.Space));

// Event Triggers: "Fire jump logic from anywhere"
_fsm.Trigger("Jump");

```

---



### 🚀 LevelUp Engine
**The Event-Driven Progression System for Unity.**

Stop putting leveling logic inside your `Update()` loop. The LevelUp Engine provides a clean, decoupled architecture to manage experience, levels, and stat curves.

![LevelUp Engine Card](card.png)

#### Key Features
* ✅ **Strategy Pattern:** Swap leveling math (Linear, Exponential, MMO) instantly via Inspector.
* ✅ **Event-Driven:** UI updates automatically without polling.
* ✅ **Scalable:** Built for projects that plan to grow.

#### Code Preview
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

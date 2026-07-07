# 🎮 Java Backend Game Engine (School Project)

A robust, multi-threaded backend game architecture developed in Java. This project focuses on deep server-side mechanics, object-oriented design patterns, and efficient state synchronization, serving as a core foundation for a game engine.

---

## 🧠 Core Backend Mechanics

This project bypasses heavy frontend rendering pipelines to focus strictly on performance, predictability, and low-latency state mutations on the backend.

* **Deterministic Game Loop:** Implements a fixed-timestep game loop (`delta time`) to decouple the internal game updates from frame rendering, ensuring consistent game speed across different hardware configurations.
* **Component-Based Entity Architecture:** Utilizes a lightweight Entity Component System (ECS) approach to manage game objects dynamically without deep, fragile inheritance structures.
* **State Management & Serialization:** Handles game saves, level data, and state synchronization using structured **JSON** and **XML** configurations.
* **Thread-Safe Collisions:** Emplements space-partitioning algorithms to optimize backend boundary detection and spatial queries efficiently.

---

## 🧰 Technical Architecture

* **Language:** Java 17+ (utilizing modern OOP paradigms, Streams API, and Concurrency utils)
* **Data Serialization:** Jackson / Gson (JSON), JAXB (XML)
* **Build System:** Maven / Gradle

---

## 🚀 Architectural Design Patterns Applied

1. **Singleton Pattern:** Manages global infrastructure states safely, such as the `GameEngine` lifecycle coordinator and resource managers.
2. **State Pattern:** Handles seamless transitions between main menus, gameplay loops, paused mechanics, and game-over states.
3. **Observer Pattern:** Decouples backend triggers (e.g., collisions, health changes, score metrics) from game systems, broadcasting updates via an asynchronous event bus.

---

## 💾 Network-Ready Data Formats

The backend uses a dual-format data handling layer designed to mirror enterprise network configurations:

* **JSON Payloads:** Used for dynamic, fast-parsed transactional data like real-time player positioning, player actions, and live stat counters.
* **XML Frameworks:** Leveraged for rigid structural schemas, static game configurations, level design grids, and item attribute tables.

---

## ⚙️ Setup & Execution

Ensure you have Java Development Kit (JDK) 17 or higher installed on your system.

1. **Clone the repository:**
   ```bash
   git clone https://github.com
   ```
2. **Compile the source files:**
   ```bash
   javac Src/*.java -d bin/
   ```
3. **Run the application backend:**
   ```bash
   java -cp bin Main
   ```


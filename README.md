# 🌿 DigitalHome.Cloud Simulation LAB

**DigitalHome.Cloud Simulation LAB** is an open-source experimental platform for simulating sustainable, intelligent environments using Webots and ROS. It forms the simulation layer of the [DigitalHome.Cloud](https://github.com/YOUR_USER/DigitalHome.Cloud) ecosystem, which combines Building Operating System (BOS) principles with a modular digital twin architecture.

This LAB project focuses on rapid prototyping, automation logic, and smart scenarios for human-centric, nature-connected living — starting with an MVP: **the Smart Garden**.

---

## 🎯 MVP: Smart Garden Simulation

Simulate an intelligent garden featuring:
- A **SunMower** robot navigating zones
- A **solar cooker** reacting to sunlight
- **Environmental sensors** (solar, soil, temperature)
- **Scenario logic** driven by a lightweight digital twin

> Example: "If solar irradiance is high and the mower is idle, activate the solar cooker."

---

## 🧱 Project Structure

```plaintext
digitalhome-simulation-lab/
├── README.md                   # Project overview
├── requirements.txt            # Python dependencies
│
├── worldgen/                   # World generation engine
│   ├── generate_world.py      # Generates Webots world from JSON model
│   ├── data_model.json        # Sample twin config (zones, equipment)
│   ├── template/
│   │   └── world_template.wbt # Jinja2 template for garden layout
│   └── output/
│       └── garden_world.wbt   # Generated Webots world
│
├── webots_project/             # Webots-compatible simulation
│   ├── worlds/
│   │   └── garden_world.wbt   # Symlink or copied from worldgen
│   ├── protos/
│   │   ├── SunMower.proto
│   │   ├── SolarCooker.proto
│   │   └── Sensor.proto
│   ├── controllers/
│   │   └── supervisor/        # Dynamic behavior via Supervisor
│   │       └── supervisor.py
│
└── ros_integration/            # (Optional) ROS/ROS2 support
    ├── launch/
    ├── msg/
    └── scripts/


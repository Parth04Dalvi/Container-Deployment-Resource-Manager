# Container Deployment Resource Manager

# 🚀 Container Deployment & Resource Manager Simulator

A single-file web application designed to simulate a modern container orchestration and resource management system. This project showcases expertise in front-end **State Synchronization**, **Real-time Data Visualization**, and implementing **Complex Alerting** logic using vanilla JavaScript and Chart.js.

## ✨ Features

This project is a completely self-contained, single-page application (`index.html`) demonstrating several critical concepts:

* **State Synchronization:** Manages the health (`Up`/`Restarting`) and resource state (`CPU`/`Memory`) for multiple independent container deployments.
* **Deployment Actions:** Implements interactive controls to simulate **Scale Up**, **Scale Down**, and **Restart** commands, directly affecting the system's resource consumption.
* **Real-time Metrics:** Uses **Chart.js** to visualize the aggregate time-series usage of CPU and Memory across all running replicas.
* **Complex Alerting:** Continuously monitors aggregate resource metrics and triggers persistent, on-screen alerts when CPU (75%) or Memory (80%) thresholds are breached.
* **Dynamic UI Updates:** Resource usage for each container fluctuates in real-time, simulating a dynamic production environment.

## 🛠️ Technology Stack

This project is intentionally built with minimal dependencies to showcase core front-end skills:

* **HTML5:** Structure
* **CSS3:** Styling
* **Vanilla JavaScript (ES6+):** All core logic, state management, simulation, and event handling.
* **Chart.js:** Used for generating the responsive, real-time line graphs.

## 📦 Getting Started

Since this is a single-file application, running it couldn't be simpler!

### Prerequisites

You need nothing more than a modern web browser (Chrome, Firefox, Edge, Safari).

### Installation & Execution

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git)
    cd YOUR_REPO_NAME
    ```
2.  **Open the File:**
    Locate the `index.html` file in the project directory.
3.  **Launch:**
    **Double-click** on `index.html` to open it directly in your web browser.

The simulation will start automatically, generating metrics and updating the UI every second.

## 🧑‍💻 How to Interact

### Containers Panel

This panel displays individual container deployments.

| Action | Description | Effect on System |
| :--- | :--- | :--- |
| **Scale Up (+1)** | Adds one replica to the deployment. | Increases the total aggregated CPU/Memory usage. |
| **Scale Down (-1)** | Removes one replica from the deployment. | Decreases the total aggregated CPU/Memory usage. |
| **Restart** | Changes status to 'Restarting' for 3 seconds. | Resets the individual container's resource usage to a lower baseline after the restart is complete. |

### Alerts Panel

* The **red alerts panel** appears only when a defined threshold (CPU > 75% or Memory > 80%) is breached.
* **To trigger an alert:** Use the **Scale Up** button repeatedly on one or more containers until the aggregate usage pushes the total percentage over the limit.
* **To clear an alert:** Use the **Scale Down** button to bring the aggregate usage back below the threshold.

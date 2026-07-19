# 🐳 Task 6: Docker Swarm Deployment (Cluster & Scaling Scenario)

## 🎯 Objective

Deploy and manage a clustered containerized application using **Docker Swarm** with:

- 📈 Scaling
- ⚖️ Load Balancing
- ❤️ High Availability
- 🔄 Auto Healing
- 🚀 Rolling Updates

---

# 📁 Project Structure

```text
task6-docker-swarm/
│
├── 📁 app/
│   ├── 📄 app.py                 # Flask Web Application
│   ├── 📄 requirements.txt       # Python Dependencies
│   └── 📄 Dockerfile             # Docker Image Configuration
│
├── 📁 screenshots/
│   ├── swarm-init.png
│   ├── service-create.png
│   ├── service-ls.png
│   ├── service-ps.png
│   ├── scaling.png
│   ├── rolling-update.png
│   └── auto-healing.png
│
├── 📄 README.md
│
└── 📄 .gitignore
```

---

# 🏗️ Architecture

```
                    🌐 Browser
                 http://localhost
                        │
                        ▼
          ┌─────────────────────────┐
          │ Docker Swarm Routing Mesh│
          └─────────────┬───────────┘
                        │
        ┌───────────────┼───────────────┐
        ▼               ▼               ▼
  🐳 Replica 1     🐳 Replica 2     🐳 Replica 3
     Flask App        Flask App        Flask App
        │               │               │
        └───────────────┼───────────────┘
                        │
                🌐 Overlay Network
```---------------------------------------------------------------------------------------------------------
             Overlay Network
      -----------------------------
      |                           |
+-------------+            +-------------+
| Manager     |            | Worker      |
| Web Service | <------->  | API Service |
+-------------+            +-------------+
---

# 🧰 Technology Stack

| Technology | Purpose |
|------------|---------|
| 🐳 Docker | Containerization |
| 🐝 Docker Swarm | Container Orchestration |
| 🐍 Python | Programming Language |
| 🌶 Flask | Web Framework |
| 🌐 Overlay Network | Service Communication |
| ⚖️ Routing Mesh | Built-in Load Balancing |

---

# 📂 Folder Description

## 📁 app/

Contains the Flask application and Docker configuration.

### 📄 app.py

- Flask Application
- Returns hostname of the running container
- Used to demonstrate Load Balancing

### 📄 requirements.txt

Contains Python dependencies.

```
Flask
```

### 📄 Dockerfile

Builds the Docker Image for the Flask application.

---

# 📁 screenshots/

Contains screenshots of every execution step.

Suggested screenshots:

- ✅ Swarm Initialization
- ✅ Overlay Network
- ✅ Service Deployment
- ✅ Scaling
- ✅ Load Balancing
- ✅ Auto Healing
- ✅ Rolling Update

---

# 🔄 Workflow

```
Write Flask App
        │
        ▼
Build Docker Image
        │
        ▼
Initialize Swarm
        │
        ▼
Create Overlay Network
        │
        ▼
Deploy Service
        │
        ▼
Create 3 Replicas
        │
        ▼
Load Balancer Distributes Requests
        │
        ▼
Scale to 5 Replicas
        │
        ▼
Perform Rolling Update
        │
        ▼
Auto Healing if Container Fails
```

---

# 🚀 Features Implemented

- ✅ Docker Swarm Cluster
- ✅ Overlay Network
- ✅ Docker Service Deployment
- ✅ Multiple Replicas
- ✅ Built-in Load Balancing
- ✅ Auto Healing
- ✅ Rolling Updates
- ✅ Service Scaling

---

# 📌 Expected Output

Browser:

```
http://localhost
```

or

```
http://localhost:8080
```

Output:

```
Hello from Docker Swarm!

Container:
8dc53c8e7b19
```

Refreshing the page several times shows different container IDs, proving that requests are distributed across replicas.

---

# 🎯 Learning Outcomes

After completing this project, you will understand:

- 🐳 Docker Swarm Architecture
- 🧩 Service Creation
- 📈 Horizontal Scaling
- ⚖️ Docker Routing Mesh
- 🌐 Overlay Networking
- ❤️ High Availability
- 🔄 Auto Healing
- 🚀 Rolling Updates
- 📊 Service Management
- 🏗️ Container Orchestration

---

# 💼 Interview Highlights

You can explain this project as:

> Developed a highly available containerized Flask application using Docker Swarm. Created a Swarm cluster, deployed the application as a replicated service, configured an overlay network for communication, demonstrated horizontal scaling from three to five replicas, verified built-in load balancing using the routing mesh, tested auto-healing by stopping a container, and performed rolling updates with zero downtime.

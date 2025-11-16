# DeployHub – Advanced Web Deployment Platform (Frontend Demo)

DeployHub is a **frontend-only demo of a modern web deployment platform**.  
It simulates features of platforms like Netlify, Vercel, and Render through an interactive dashboard built with pure **HTML, CSS, and JavaScript**.

> ⚠️ Note: This is a **simulation**. No real deployments or GitHub API calls are made.

---

## 🚀 Features

### 🌐 GitHub Connection (Simulated)
- “Connect GitHub” button opens a modal for:
  - GitHub Personal Access Token (fake in this demo)
  - GitHub Username  
- After “connecting”, a list of **sample repositories** is loaded:
  - Name, description, language
  - Stars, forks, last updated time
  - Branch list with branch selector buttons
- Each repo has a **Deploy** button.

---

### ⚡ One-Click Deployments

- Deploy any sample repository with **one click**.
- A **Deploy Modal** lets you choose:
  - Branch (`main`, `develop`, etc.)
  - Environment (`Production` or `Staging/Preview`)
- Simulated deployment steps shown in logs:
  - Cloning repo  
  - Installing dependencies  
  - Building application  
  - Running tests  
  - Creating container image  
  - Deploying to cluster  
  - Running health checks  
- On success, a fake URL like  
  `https://myapp-abc123.deployhub.app` is displayed.

---

### 👀 Preview Deployments

- Preview deploys simulate **Pull Request environments**.
- Shows a **Preview URL** like:  
  `https://pr-124-myapp-xyz789.deployhub.app`
- Great for explaining how teams can test changes before merging.

---

### 📊 Metrics & Auto-Scaling Simulation

In the **Metrics** tab:

- CPU, Memory, Latency, and Error Rate are displayed as:
  - Metric cards with values
  - Progress bars that change width & color (normal / warning / danger)
- A **CPU Usage Monitor**:
  - Animated bar chart simulating CPU usage over time
  - Warning and danger thresholds
  - Status labels: `Normal`, `Moderate`, `High`
- **Auto-Scaling Logic** (simulated):
  - When CPU usage exceeds a configurable threshold (slider),  
    instance count increases (up to 10).
  - Shows:
    - Current instances  
    - Max instances  
    - Scaling progress bar  
  - Adds auto-scaling events to the deployment logs.

---

### ❤️ Service Health Dashboard

Displays health of multiple services:

- Web Server  
- API Gateway  
- Database  
- Cache Service  

Each service shows:

- Health indicator (colored dot)
- Status pill (e.g., `Healthy`, `High Load`)
- Resource usage: CPU, memory, containers / connections / hit rate

---

### 🔄 Intelligent Rollback UI

- After some deployments, a **rollback alert** may appear (simulated).
- Shows:
  - Increase in error rates and latency
  - CPU and memory spikes
  - Root cause (e.g., DB connection pool misconfiguration)
- Comparison between:
  - **Previous Version** metrics
  - **Current Version** metrics
- Buttons:
  - **Confirm Rollback** → Resets CPU usage and logs rollback
  - **Dismiss** → Hides the alert

---

### ⚙️ Project Settings

In the **Settings** tab:

- Git Repository URL
- Default Branch
- Build Command
- Start Command
- Toggles:
  - Auto-deploy on push
  - Preview deployments for PRs
  - Automatic rollback on issues
- **CPU Threshold slider** for auto-scaling (50–90%)

---

## 🧱 Tech Stack

- **HTML5**
- **CSS3** (custom styling, no framework)
- **Vanilla JavaScript** (no frontend framework)
- Icons via **Font Awesome CDN**

No backend, no database — everything runs in the browser.

---

## 📂 Project Structure

```text
project-root/
├── index.html   # Main page with HTML, CSS (in <style>), and JS (in <script>)

# Virtual Agent for Social Project Analysis

This repository presents the **Virtual Agent**, an artificial intelligence solution I developed to analyze data from social projects stored in an **Azure Blob Storage** container.

The core idea is to leverage the **Gemini model** to interpret **natural language requests**, perform data analysis functions, and provide **insights into the financial viability and social return** of early childhood education initiatives.

<img width="1919" height="823" alt="image" src="https://github.com/user-attachments/assets/eb032cf8-948b-4966-bb95-ecd5c36a5056" />  

---

## How I built this project

The project is structured into **two main components**: a backend (hosted on **Google Cloud Run**) and a frontend (published on **GitHub Pages**).

### 🔹 Backend (`/virtual-agent`)

For the virtual agent’s API, I developed with:

* **Python 3.9** as the main programming language.
* **Flask** to build the API that receives and processes frontend requests.
* **Google Gemini API** for conversational capabilities and tool execution.
* **Azure Storage Blob SDK** for integration with data stored in Azure.
* **Pandas** for data manipulation and analysis.
* **python-dotenv** for loading environment variables (such as the API key).
* **flask-cors** for handling CORS policies.
* **Docker** to package and run the backend in a container.

📂 Main structure of the `virtual-agent` folder:

* `app.py` → API logic, integration with the Gemini model, and tool definitions.
* `requirements.txt` → required dependencies.
* `dockerfile.dockerfile` → Docker image build instructions.
* `GOOGLE_APY_KEY.env` → environment variables (not versioned).

The backend was deployed to **Google Cloud Run**, enabling automatic scaling and frontend communication.

---

### 🔹 Frontend (`/virtual_agent_frontend`)

The web interface was designed to be simple, interactive, and easily accessible:

* **React + Vite** for building and bundling the application.
* **Tailwind CSS** for responsive design and styling.
* **GitHub Pages** for free and convenient frontend hosting.

📂 Main structure of the `virtual_agent_frontend` folder:

* `app.jsx` → React application code.
* `index.html` → entry page that connects to the backend deployed on Cloud Run.

---

## Workflow

1. The user accesses the frontend hosted on **GitHub Pages**.
2. Requests are sent to the **backend on Google Cloud Run**.
3. The backend uses the **Gemini model** to interpret natural language queries.
4. Data is retrieved from **Azure Blob Storage** and processed with **Pandas**.
5. The agent returns results in a clear and user-friendly format.

---

## Key Learnings

Throughout development, I worked with:

* Integration between different cloud services (**Google Cloud Run + Azure Blob Storage**).
* Building scalable Python APIs and packaging them with Docker.
* Connecting a React frontend to a cloud-based backend.
* Applying AI to analyze social projects in a real-world scenario.

---

👉 GitHub Repository:
[https://github.com/cristinaresendedealmeida/virtual-agent](https://github.com/cristinaresendedealmeida/virtual-agent)

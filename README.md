### **Presenting the "Virtual Agent"**

The "Virtual Agent for Social Project Analysis" is a project I developed to explore the potential of artificial intelligence in analyzing complex data. It uses the **Gemini** AI model to interpret natural language requests and provide insights into the financial viability and social return of early childhood education initiatives.

The main challenge was to integrate different technologies to create a complete solution: a robust **back-end** to process the data and an intuitive **front-end** for user interaction.

---

### **Project Structure**

The project was divided into two main parts, each with its own function and technology.

#### **Back-end: The Agent's Brain**

The back-end is responsible for all the logic and data processing. It was built using:

* **Python 3.9:** The main language, chosen for its simplicity and power.
* **Flask:** A Python micro-framework that allowed me to create a lightweight API to receive requests from the front-end.
* **Google Gemini API:** The AI that lets the agent understand what the user is asking and respond intelligently.
* **Pandas:** An essential library for manipulating and analyzing social project data.
* **Docker:** To ensure the back-end environment was consistent and easy to deploy, the application was packaged into a Docker container.

The source code is organized in the `virtual-agent` folder, with the following files:
* `app.py`: Where all the API logic and Gemini integration are defined.
* `requirements.txt`: A list of Python dependencies.
* `Dockerfile`: Instructions for Docker to build the application image.
* `GOOGLE_API_KEY.env`: A file to securely manage environment variables, such as API keys, without exposing them in the source code.

#### **Front-end: The User Interface**

The front-end is the interface the user sees and interacts with. It was developed with:

* **React:** A JavaScript library for building a modular and efficient interface.
* **Vite:** A build tool that speeds up front-end development and packaging.
* **Tailwind CSS:** A framework for styling the interface quickly and consistently.
* **GitHub Pages:** A hosting service I used to make the front-end publicly accessible.

The front-end structure is in the `virtual_agent_frontend` folder and includes the files:
* `app.jsx`: The main user interface component.
* `index.html`: The base HTML file.

---

### **Development and Deployment Process**

The project followed a clear workflow, from conception to final deployment in the cloud.

1.  **Initial Setup:** I created a GitHub repository (`virtual-agent`) to manage versioning and track project progress.
2.  **Environment Configuration:** I set up a virtual environment for the back-end and installed all necessary dependencies, ensuring the project could run locally.
3.  **Back-end Development:** I wrote the API code in `app.py`, defining the functionalities and tools the AI could use to interact with the data.
4.  **Containerization:** To simplify deployment, I created a `Dockerfile` to package the back-end, including all dependencies, into a Docker image.
5.  **Cloud Deployment:** The Docker container was deployed on **Google Cloud Run**, a serverless compute service. This allowed me to host the back-end in a scalable way without worrying about server management.
6.  **Front-end Connection:** The front-end was configured to communicate with the public URL provided by Google Cloud Run, linking the two parts of the project.

The result is a functional application where the user can interact with an AI to get detailed analyses and help with decision-making for social projects.

# Virtual Agent for Social Project Analysis

This project is a virtual agent with artificial intelligence technology, designed to analyze data from social projects stored in an Azure Blob Storage container. It uses the Gemini model to interpret natural language requests and execute data analysis functions, providing insights into the financial viability and social return of early childhood education initiatives.

## Technologies Used

The project consists of two main components: the backend (hosted on Google Cloud Run) and the frontend (a static web application).

### Backend

Python 3.9: Main programming language.
Flask: Web microframework to create the API that receives requests from the frontend.
Google Gemini API: Used for conversational capabilities and tool execution.
Azure Storage Blob SDK: Library for interacting with Azure Blob Storage, allowing data files to be read.
Pandas: Library for data manipulation and analysis.
python-dotenv: To load environment variables from a .env file.
flask-cors: To manage the CORS (Cross-Origin Resource Sharing) security policy.
Docker: To package the application and its dependencies into a container, facilitating deployment.

### Frontend

React: JavaScript library for building the user interface.
Vite: Build tool for frontend development and packaging.
GitHub Pages: Static page hosting service for the frontend.
Tailwind CSS: CSS framework to style the interface.

### Project Structure

app.py: The backend source code, which contains the API logic, tool definitions, and integration with the Gemini model.
requirements.txt: Lists the necessary Python dependencies for the backend.
Dockerfile: Instructions for creating the Docker image of the backend application.
.env: File to securely store the Google API key (should not be uploaded to GitHub).


## How to Run


### How to Run (Locally)


#### Clone the repository:
git clone https://github.com/your-username/your-repository.git
cd your-repository


#### Create the virtual environment and install dependencies:
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
pip install -r requirements.txt


#### Create a .env file:
Create a .env file in the project root and add your Google API key.
GOOGLE_API_KEY=YOUR_KEY_HERE


#### Run the backend:
python app.py


The server will be running at http://localhost:8080.


### How to Deploy on Google Cloud Run


#### Install the Google Cloud SDK: 
Follow the official Google instructions.

#### Authenticate:
gcloud auth login
gcloud config set project YOUR_PROJECT_ID


#### Deploy the service:
gcloud run deploy virtualagent --source . --region=europe-west10


The command will build the Docker image and deploy the service to Cloud Run. At the end, it will provide the public URL of your service.
Frontend Configuration:
On your frontend, update the backend URL with the address provided by Google Cloud Run so that communication works correctly.

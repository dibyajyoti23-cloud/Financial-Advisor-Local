# 🎙️ Voice-Powered Financial Advisor

A full-stack web application that allows you to track your daily expenses simply by speaking. This project uses Google's Gemini API to understand natural language, categorize your spending, and help you visualize your finances against your set budgets.

 ✨ Features

- **Voice-Powered Entry**: Add new expenses by describing them in natural language.
- **AI Categorization**: Uses Google's Gemini API to automatically extract the amount and category from your speech.
- **Secure Authentication**: Full user signup and login functionality using JWT for secure sessions.
- **Interactive Dashboard**: View a summary of your spending for the current month and see recent transactions.
- **Budget Tracking**: Set monthly budgets for different categories and visually track your progress with progress bars.
- **Containerized Environment**: Fully containerized with Docker and Docker Compose for a simple, one-command setup.

---
## 🛠️ Tech Stack

- **Frontend**: HTML5, CSS3, JavaScript (Web Speech API)
- **Backend**: Python 3.11, Flask
- **Database**: MariaDB
- **AI**: Google Gemini API
- **DevOps**: Docker, Docker Compose, Nginx (as a reverse proxy)

---
## 🚀 Getting Started

Follow these instructions to get the project up and running on your local machine for development and testing purposes.

### Prerequisites

You must have the following software installed on your machine:
- [Git](https://git-scm.com/downloads)
- [Docker](https://www.docker.com/products/docker-desktop/)
- [Docker Compose](https://docs.docker.com/compose/install/) (usually included with Docker Desktop)

### Local Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```

2.  **Create the Environment File:**
    Create a file named `.env` in the root of the project. Copy the contents of `.env.example` below and fill in your details.

    ```env
    # .env.example
    
    # For Python backend
    GOOGLE_API_KEY="your_gemini_api_key"
    SECRET_KEY="your_super_secret_string_for_jwt"
    FLASK_APP=app.py
    
    # For MariaDB service in Docker Compose
    DB_ROOT_PASSWORD="root_password_for_db"
    DB_NAME="fin_advisor_db"
    DB_USER="fin_user"
    DB_PASSWORD="fin_password"
    ```
    - **`GOOGLE_API_KEY`**: Your API key from Google AI Studio.
    - **`SECRET_KEY`**: A long, random string used for signing authentication tokens.
    - **`DB_...`**: Credentials for the local MariaDB database container. You can make these up.

3.  **Build and Run the Containers:**
    From the project's root directory, run the following command:
    ```bash
    docker-compose up --build
    ```
    This command will build the Docker images for the first time and start all the services (database, backend, frontend).

4.  **Access the Application:**
    Once the containers are running, open your web browser and navigate to:
    **`http://localhost:8080`**

---
## 💻 Usage

1.  Navigate to `http://localhost:8080`.
2.  Create an account using the "Sign Up" form.
3.  Log in with your new credentials.
4.  You will be redirected to your personal dashboard.
5.  (Optional) Click on "Manage Budgets" to set your monthly spending limits for each category.
6.  On the dashboard, click the microphone button to record a new expense (e.g., "I spent 500 on groceries"). The dashboard will update automatically.


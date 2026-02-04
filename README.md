# JioPay RAG Chatbot

This RAG chatbot for JioPay customer support automation was completed as a project for the LLM Production and Deployment course by Vizuara

## 🚀 Local Setup

To run this project locally, follow these steps:

1.  **Clone the repository**

2.  **Install Git LFS:**
    This project uses Git LFS to handle large files. You'll need to install it on your local machine.
    ```bash
    # On macOS with Homebrew
    brew install git-lfs

    # On other systems, see the official installation guide:
    # https://git-lfs.github.com/
    ```

3.  **Pull the LFS files:**
    ```bash
    git lfs pull
    ```

4.  **Create a virtual environment:**
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

5.  **Install the dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

6.  **Set up your environment variables:**
    Create a file named `.env` in the root of the project and add your API keys. You can use the `env.example` file as a template.

## ⚙️ Environment Variables

Create a `.env` file in the project's root directory and add the following variables:

*   `GOOGLE_API_KEY`: Your API key for the Google Gemini model.
*   `OPENAI_API_KEY`: Your OpenAI API key (optional, but recommended if you want to experiment with OpenAI models).

## 🏃‍♀️ Running the Application Locally

To run the Streamlit application locally, use the following command:

```bash
streamlit run src/web/streamlit_app.py
```

## ☁️ Deployment to Hugging Face Spaces

This application is designed to be deployed on Hugging Face Spaces.

1.  **Create a Hugging Face Space:**
    *   Go to [huggingface.co/new-space](https://huggingface.co/new-space).
    *   Give your Space a name.
    *   For the SDK, choose **"Docker"** and then **"Blank"**.
    *   Create the Space.

2.  **Push your code to the Space:**
    Use `git` to push your code to the Hugging Face Space. You'll need to add the Space as a remote and then push to it.
    ```bash
    # Add the Hugging Face remote
    git remote add huggingface https://huggingface.co/spaces/YourUsername/YourSpaceName.git

    # Push your code
    git push huggingface main
    ```

3.  **Set your secrets:**
    In your Hugging Face Space settings, go to the "Secrets" section and add your `GOOGLE_API_KEY`.

# GDG ADK LAB 01

## Authentication

- Option A - Google Gemini API Key
  1. set environment variables in .env file

     ```zsh
     GOOGLE_GENAI_USE_VERTEXAI=FALSE
     GOOGLE_API_KEY=google_api_key
     ```

     or

     ```zsh
     GOOGLE_GENAI_USE_VERTEXAI=0
     GOOGLE_API_KEY=google_api_key
     ```

- Option B - Google Vertex AI
  1. set environment variables in .env file

     ```zsh
     GOOGLE_GENAI_USE_VERTEXAI=TRUE
     GOOGLE_CLOUD_PROJECT=YOUR_GCP_PROJECT_ID
     GOOGLE_CLOUD_LOCATION=global
     MODEL=gemini_flash_model_id
     ```

  2. authenticate via Google Cloud

     ```zsh
     gcloud auth login
     ```

  3. set the Google Cloud project

     ```zsh
     gcloud config set project PROJECT_ID
     ```

  4. set Google Cloud project quota

     ```zsh
     gcloud auth application-default set-quota-project QUOTA_PROJECT_ID
     ```

  4. enable Google Cloud Logging API for PROJECT_ID

     ```zsh
     gcloud services enable logging.googleapis.com --project=PROJECT_ID
     ```

  5. enable Google Vertex API for PROJECT_ID

     ```zsh
     gcloud services enable aiplatform.googleapis.com --project=PROJECT_ID
     ```

## Sources

- GENAI104
  - https://www.skills.google/focuses/147009?catalog_rank=%7B%22rank%22%3A1%2C%22num_filters%22%3A0%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=77026694

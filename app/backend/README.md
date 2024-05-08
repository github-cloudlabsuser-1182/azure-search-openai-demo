Backend Application Documentation
The backend application for the Azure Search OpenAI demo is built using Quart, a Python framework for asynchronous web applications. The backend code is primarily located in the app/backend directory.

Main Components
Authentication
The authentication process is handled by the script in auth_update.py. This script uses the Azure Developer CLI Credential and the Microsoft Graph Service Client to authenticate the application.

Document Processing
The document processing setup is handled by the setup_file_processors function in prepdocs.py. This function sets up different file processors for different file types, such as .heic, .md, and .txt.

Customization
You can customize the backend application to suit your needs. The primary backend code you'll want to customize is located in the app/backend/approaches folder, which contains the classes powering the Chat and Ask tabs. Each class uses a different Retrieval Augmented Generation (RAG) approach.

Chat Approach
The chat tab uses the approach programmed in chatreadretrieveread.py. This approach involves calling the OpenAI ChatCompletion API to turn the user question into a good search query, querying Azure AI Search for search results for that query, and then combining the search results and original user question to answer the question based on the sources.

Infrastructure
The infrastructure for the backend application is defined in the infra directory, with the main configuration in main.bicep. This file sets up the application frontend, App Service Plan, and Application Insights Dashboard.

For more detailed customization options, refer to the customization guide.


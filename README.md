# myBacklog

myBacklog is a web application designed to help you keep track of the games you've played and the games you want to play. It also includes a chat feature to discuss games with others.

## Installation

Follow these steps to install the project.

### Prerequisites

- Node.js and npm

### Steps

1. Clone the repository and navigate to the project directory:

    ```sh
    git clone https://github.com/UniCT-WebDevelopment/myBacklog.git
    cd myBacklog
    ```

2. Create a Google Cloud service account key:
   - Go to the [Google Cloud Console](https://console.cloud.google.com/).
   - Navigate to **IAM & Admin** > **Service Accounts**.
   - Click **Create Service Account**.
   - Follow the prompts to create a new service account.
   - Download the JSON key file and place it in a `config` folder within the project directory.
   - Create a **Bucket**.

3. Create a MongoDB Atlas cluster:
   - Go to the [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) website.
   - Sign in or create a new account.
   - Click **Build a Cluster**.
   - Go to the **Network Access** tab and add your IP address or allow access from anywhere.
   - Obtain your connection string from the **Clusters** view. It should look something like this:
     ```text
     mongodb+srv://username:password@cluster0.mongodb.net/
     ```

4. Create a `.env` file with the necessary parameters (replace with your credentials) and place it in the project directory. The required parameters are:

    ```env
    GOOGLE_APPLICATION_CREDENTIALS= ./config/your-JSON-key-file
    GCS_BUCKET_NAME= your-bucket-name
    DB_CONNECTION_STRING= your-mongodb-connection-string
    JWT_SECRET= "8fbb5e8d43c9a7b17b99c2c6d4e4c8d7f9e394b3d3e8b1f2a87e5d0b6f3f9a77"
    PORT = 8888
    ```

5. Install the dependencies:

    ```sh
    npm install
    ```

## Usage

Start the application with the following command:

```sh
npm start
```

The application will be accessible at http://localhost:8888 by default. Replace PORT with your preferred port number in your .env file.

## Technologies Used

### Frontend
- **HTML**, **CSS**, **JavaScript**: Basic web technologies used for building the user interface.

### Backend
- **Node.js**: Server-side JavaScript runtime for building the backend.
- **Socket.IO**: Used for enabling real-time, bidirectional communication for the chat feature.
- **Multer**: Middleware used for handling image uploads in the application.
- **MongoDB**: NoSQL database used for storing and retrieving application data.
- **Google Cloud**: Used for cloud storage of images.

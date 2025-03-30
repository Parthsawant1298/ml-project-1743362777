# Ml ML Project

This repository contains a machine learning model for ml tasks.

## Model Information

- Model Type: Ml
- Model File: `best_model.pkl`

## Running Locally

### Option 1: Run with Streamlit (Recommended)

1. Clone this repository:
   ```bash
   git clone [repository-url]
   cd [repository-name]
   ```

2. Install the requirements:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Streamlit app:
   ```bash
   streamlit run load_model.py
   ```

4. Open your browser and go to `http://localhost:8501`

### Option 2: Run as a Python Script

1. Clone this repository:
   ```bash
   git clone [repository-url]
   cd [repository-name]
   ```

2. Install the requirements:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the main script:
   ```bash
   python run.py
   ```

## Deployment Options

### Deploy to GitHub Pages (Static Exports Only)

If your Streamlit app generates static content, you can export it and host on GitHub Pages:

1. Create a `gh-pages` branch
2. Add your static exports to the branch
3. Enable GitHub Pages in repository settings

### Deploy with ngrok (Temporary Public URL)

1. Install ngrok: [https://ngrok.com/download](https://ngrok.com/download)
2. Run your Streamlit app locally:
   ```bash
   streamlit run load_model.py
   ```
3. In another terminal, run:
   ```bash
   ngrok http 8501
   ```
4. Use the provided ngrok URL to access your app from anywhere

### Deploy on your own Server/VPS

1. Set up a VPS (Digital Ocean, Linode, AWS EC2, etc.)
2. Clone this repository to your server
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Use a process manager to keep your app running:
   ```bash
   # Install PM2 with Node.js
   npm install -g pm2
   # Start your Streamlit app with PM2
   pm2 start "streamlit run load_model.py --server.port=8501 --server.address=0.0.0.0" --name ml-app
   ```
5. Set up Nginx as a reverse proxy (optional for custom domain)

## API Endpoints (if applicable)

If your application exposes API endpoints, they are:

- `/predict` - POST request for model predictions
- `/upload` - POST request for file uploads
- `/download` - GET request for downloading results

## Contributing

Feel free to submit issues or pull requests to improve this project.

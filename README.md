# Deal Finder App

This is a Flask-based web application for analyzing real estate investment opportunities.

## Features
- Upload property and comps CSVs
- Auto-calculate ARV and Offer Price
- Flag High Potential deals
- Generate downloadable LOIs
- Track LOI sent and follow-up sent status

## Getting Started

### Local Setup
1. Install dependencies:
    ```
    pip install -r requirements.txt
    ```

2. Run the app:
    ```
    python app.py
    ```

3. Go to `http://localhost:5000`

### Deploy to Render
- Make sure you include:
  - `app.py`
  - `templates/index.html`
  - `Procfile`
  - `requirements.txt`

- Set the Render start command to:
  ```
  gunicorn app:app
  ```

## File Upload Format

Your property CSV must include at least:
- `Id`
- `Listing Price`

Optional columns:
- `Condition Override`
- `LOI Sent`
- `Follow-Up Sent`
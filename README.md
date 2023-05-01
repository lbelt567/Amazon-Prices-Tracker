# Amazon-Prices-Tracker

## Overview
This Python script automates the process of tracking price drops of your favorite Amazon items. When the script detects a price drop, it notifies you via the inputed email.

## Requirements
- Python >= 3.6
- `requests-html` module (install using `pip install requests-html`)
- A `config.py` file with the following variables:
    - `PRODUCTS_TO_TRACK`: A list of Amazon product IDs to track.
    - `FROM_EMAIL_ID`: The email address from which notifications will be sent.
    - `FROM_EMAIL_ID_PASSWORD`: The password for the email address from which notifications will be sent.
    - `TO_EMAIL_ID`: The email address to which notifications will be sent.
    - `SMTP_HOST`: The SMTP server host.
    - `SMTP_PORT`: The SMTP server port.

## Usage
1. Clone the repository and navigate to the project directory.
2. Create a `config.py` file with the above variables.
3. Run the `amazon_price_tracker.py` script using the command `python amazon_price_tracker.py`.
4. The script will periodically check the prices of the products in `PRODUCTS_TO_TRACK`. If a price drop is detected, you will receive an email notification.

## Example config.py file
```python
PRODUCTS_TO_TRACK = ["B07ZRXF7M8", "B09G9HRYFZ"]
FROM_EMAIL_ID = "your_email_address@gmail.com"
FROM_EMAIL_ID_PASSWORD = "your_email_password"
TO_EMAIL_ID = "recipient_email_address@gmail.com"
SMTP_HOST = "smtp.gmail.com"
SMTP_PORT = 587

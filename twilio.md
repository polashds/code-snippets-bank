# === .env ===
TWILIO_ACCOUNT_SID=xxxxxxxxxxx
TWILIO_AUTH_TOKEN=xxxxxxxxxxxx

```python
import os
from twilio.rest import Client
from dotenv import load_dotenv

load_dotenv()  # load .env file

def send_text_message(destination: str, message: str):
    # Debug: Check if environment variables are loaded
    account_sid = os.environ.get("TWILIO_ACCOUNT_SID")
    auth_token = os.environ.get("TWILIO_AUTH_TOKEN")
    
    print(f"Account SID: {account_sid}")
    print(f"Auth Token: {auth_token[:5]}...")  # Show first 5 chars for security
    
    if not account_sid or not auth_token:
        raise ValueError("Twilio credentials not found in environment variables")
    
    client = Client(account_sid, auth_token)

    message = client.messages.create(
        body=message,
        from_="+12513179667",  # Your Twilio phone number
        to=destination,
    )

    print(f"Message SID: {message.sid}")
    print(f"Message status: {message.status}")

def main():
    try:
        send_text_message("+8801721926800", "Hello from Python!")
    except Exception as e:
        print(f"Error: {e}")

if __name__ == "__main__":
    main()

```

** Next time you face a similar task, you're not starting from zero; you're starting from 80%.**
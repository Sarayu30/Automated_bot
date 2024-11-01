 
# Automated Meeting Scheduling and Reminder Bot

This Python script automates the scheduling of meetings by sending email invites to participants, along with a reminder email shortly before the meeting begins. It's ideal for streamlining the process of notifying team members or clients about scheduled meetings, ensuring timely attendance.

## Features

- **Meeting Scheduling**: Sends an initial email invite with meeting details to all participants.
- **Reminder Notification**: Sends a reminder email a specified number of minutes before the meeting starts.
- **Customizable Meeting Details**: Easily configure meeting date, time, and participant list.

## Prerequisites

- **Python** 3.x
- **Email Account**: Gmail account or any SMTP-enabled email account.
- **App-Specific Password**: If using Gmail, generate an app-specific password (recommended for security).

## Installation

1. Clone this repository or copy the script.
2. Install any required Python libraries. This script uses only standard libraries (`smtplib`, `datetime`, `time`, and `threading`).

## Configuration

1. **SMTP and Email Credentials**: Update `sender_email` and `sender_password` with your email and app-specific password.
2. **SMTP Server Information**: Adjust `smtp_server` and `smtp_port` if not using Gmail.
3. **Meeting Details**: Set `meeting_subject` and `meeting_datetime` to your desired meeting subject and date/time.
4. **Reminder Timing**: Modify `reminder_minutes` to set how many minutes before the meeting the reminder should be sent.
5. **Participants List**: Add the email addresses of the participants to the `participants` list.

## Usage

Run the script:

```bash
python meeting_scheduler_bot.py
```

The script will:
1. Schedule a meeting by sending an email with the details to all participants.
2. Wait until the specified reminder time before the meeting.
3. Send a reminder email to all participants.

### Example Configuration

For a meeting scheduled on **November 5, 2024, at 10:00 AM** with a **15-minute reminder**:

```python
meeting_datetime = datetime(2024, 11, 5, 10, 0)  # YYYY, MM, DD, HH, MM
reminder_minutes = 15
```

## Script Overview

### Functions

1. **`send_email`**: Handles sending emails with SMTP.
2. **`schedule_meeting`**: Sends the initial meeting invite to participants.
3. **`send_reminder`**: Sends a reminder email `reminder_minutes` before the meeting.
4. **`main`**: Runs both `schedule_meeting` and `send_reminder` in parallel.

 

### Troubleshooting

- **SMTP Authentication Error**: Ensure your email and password are correct. If using Gmail, enable 2-Step Verification and generate an app-specific password.
- **Firewall or Security Settings**: Some email providers may block SMTP access for security. Ensure your email settings allow SMTP usage.

## Contributing

Feel free to open issues or submit pull requests if you find any bugs or have suggestions for new features!

--- 

### Author

This bot was developed to streamline meeting management and improve workflow automation.

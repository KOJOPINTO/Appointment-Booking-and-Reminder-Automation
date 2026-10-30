# Workflow Overview – Appointment Booking & Reminder Automation

## Introduction

This project contains two independent Make.com scenarios that work together to automate appointment management.

## Scenario 1: Appointment Booking Confirmation

**Trigger:** A new appointment response is submitted through Google Forms.

### Workflow Steps

1. **Google Sheets – Watch New Rows:** Detects new appointment submissions.
2. **Google Sheets – Update a Row:** Sets booking and reminder statuses and generates a Booking ID.
3. **Gmail – Customer Confirmation:** Sends booking confirmation details to the customer.
4. **Gmail – Business Owner Notification:** Notifies the business owner of the new appointment.

### Expected Outcome

The customer receives confirmation, the business owner receives a notification, and the booking is recorded in Google Sheets.

## Scenario 2: Automated Appointment Reminders

**Trigger:** Scheduled execution every hour.

### Workflow Steps

1. **Google Sheets – Search Rows:** Retrieves confirmed appointments with pending reminders.
2. **Filter – Appointment Date and Time:** Checks whether the appointment is between 22 and 24 hours away.
3. **Gmail – Send Reminder:** Sends an appointment reminder to the customer.
4. **Google Sheets – Update a Row:** Changes Reminder Status from `Pending` to `Sent`.

### Expected Outcome

Customers receive reminders before their scheduled appointments, and the system tracks completed reminder processing.

## Data Flow

Google Forms captures the appointment request.

Google Sheets stores and tracks appointment information.

Make.com processes the booking and reminder workflows.

Gmail handles customer and business notifications.

## Workflow Relationship

Scenario 1 prepares the booking record. Scenario 2 uses the confirmed booking information to determine when a reminder should be sent.

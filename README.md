# Appointment Booking & Automated Reminder System

## Project Overview

An automated appointment management solution built with Make.com, Google Forms, Google Sheets, and Gmail.

The system captures appointment requests, confirms bookings, notifies business owners, and sends automated reminders before scheduled appointments.

## Business Problem

Managing appointments manually can lead to missed bookings, delayed confirmations, forgotten appointments, and repetitive administrative work.

This project demonstrates how workflow automation can simplify appointment management and improve customer communication.

## Key Features

- Automated appointment request collection through Google Forms.
- Automatic booking confirmation emails.
- Unique appointment ID generation.
- Business owner email notifications.
- Centralized appointment tracking using Google Sheets.
- Automated reminders 22–24 hours before appointments.
- Reminder status tracking to help prevent duplicate emails.

## Technology Stack

| Technology | Purpose |
|---|---|
| Make.com | Workflow automation |
| Google Forms | Appointment request collection |
| Google Sheets | Booking database and tracking |
| Gmail | Email notifications and reminders |

## Workflow Architecture

### Scenario 1: Appointment Booking Confirmation

Google Forms → Google Sheets (Watch New Rows) → Update Booking Status → Customer Confirmation Email → Business Owner Notification

### Scenario 2: Automated Appointment Reminders

Google Sheets (Search Rows) → Appointment Date/Time Filter → Gmail Reminder → Update Reminder Status

## Booking Data Structure

The Google Sheets database tracks:

- Customer name and contact details
- Service required
- Preferred appointment date and time
- Booking status
- Reminder status
- Unique booking ID
- Combined appointment date and time

## Business Benefits

- Reduces repetitive administrative tasks.
- Improves customer communication.
- Helps reduce forgotten appointments.
- Provides organized booking records.
- Supports more efficient appointment management.

## Project Status

Completed and activated. Both automation scenarios are configured for automatic execution.

## Future Enhancements

- Google Calendar integration.
- Appointment availability and conflict checking.
- Appointment cancellation and rescheduling.
- AI-powered customer inquiry handling.
- Automated business performance reports.

## Author

Solomon Pinto

**Focus Areas:** Data Analytics | IT Support | Business Process Automation | AI Automation

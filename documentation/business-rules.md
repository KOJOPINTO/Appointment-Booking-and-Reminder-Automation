# Business Rules – Appointment Booking Automation

## 1. Booking Confirmation

When a customer submits the appointment form:

- The booking is recorded in Google Sheets.
- Booking Status is updated to `Confirmed`.
- Reminder Status is initialized to `Pending`.
- A unique Booking ID is generated using the `APT-` prefix and row number.
- A confirmation email is sent to the customer.
- A notification email is sent to the business owner.

## 2. Appointment Reminder Rules

The reminder scenario searches for records where:

- Booking Status = `Confirmed`
- Reminder Status = `Pending`

The scenario checks the combined appointment date and time.

A reminder is eligible when the appointment is between 22 and 24 hours away.

## 3. Reminder Processing

When an appointment meets the reminder conditions:

1. A reminder email is sent to the customer.
2. The corresponding Google Sheets record is updated.
3. Reminder Status changes from `Pending` to `Sent`.

This status update helps prevent repeated reminders.

## 4. Data Management

Google Sheets stores appointment details, customer contact information, booking identifiers, and reminder statuses.

The `AppointmentDateTime` field combines the preferred appointment date and time to support date-based filtering.

## 5. Important Limitations

- The current workflow confirms bookings automatically; it does not check calendar availability.
- Appointment conflicts are not automatically detected.
- Customers cannot currently cancel or reschedule through the workflow.
- Email delivery depends on the connected Gmail account and successful scenario execution.

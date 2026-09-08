# Bug 03 - Missing technician ID validation

## Description

The Add Donation form does not properly validate the technician ID before attempting to save the donation.

The application should verify the technician before performing the database operation.

## Evidence

[▶ View missing technician ID validation](./missing%20validation%20-%20id.mp4)

## Expected Behavior

Before adding a donation, the application should verify that:

- Technician ID is provided.
- Technician ID is numeric.
- The technician exists in the database.

If validation fails, the donation must not be saved.

The error should also be included in the combined validation message described in Bug 02.

## Proposed Fix

Add technician ID validation before the database INSERT operation and query the appropriate database table to verify that the technician exists.

## Status

🔴 Open

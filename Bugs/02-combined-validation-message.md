# Bug 02 - Validation errors should be displayed in one message

## Description

Validation errors on the Add Donation form are currently handled separately.

When multiple fields contain invalid or missing values, the application should not display separate error messages one after another.

## Evidence

[▶ View error message demonstration](./error%20message%20pop%20up.mp4)

## Expected Behavior

The application should validate all fields first and collect all detected errors.

For example:

- Donor ID is required.
- Amount must be valid.
- Technician ID is required.

All detected errors should then be displayed in **one message box**.

## Proposed Fix

1. Create a collection of validation errors.
2. Validate every required field.
3. Add each detected problem to the collection.
4. Display one MessageBox containing all errors.
5. Stop the database operation until all errors are corrected.

## Status

🔴 Open

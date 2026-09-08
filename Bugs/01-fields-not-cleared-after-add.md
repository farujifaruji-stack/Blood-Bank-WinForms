# Bug 01 - Fields are not cleared after adding a donation

## Description

After a donation is added successfully, the input fields remain populated.

This can cause the user to accidentally submit the same donation data again.

## Evidence

![Add Donation form after submission](./Add%20donation%20form.png)

## Expected Behavior

After a successful donation:

- Ask the user whether they want to add another donation.
- If **Yes**, clear all input fields and reset the form.
- If **No**, close the Add Donation window.

## Proposed Fix

After successfully saving the donation:

1. Display a success message.
2. Ask whether the user wants to add another donation.
3. Clear and reset the form if the answer is **Yes**.
4. Close the form if the answer is **No**.

## Status

🔴 Open

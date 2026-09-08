# Bug 04 - Multiple instances of the same window can be opened

## Description

Each time a menu option such as **Add Donation** is clicked, the application creates a new instance of the form.

This allows multiple copies of the same window to remain open at the same time.

For example, repeatedly clicking **Add Donation** opens several Add Donation windows on top of each other.

## Evidence

![Multiple Add Donation windows](./Add%20donation%20-%20new%20window.png)

## Expected Behavior

Only one instance of the Add Donation window should be open at a time.

If the Add Donation window is already open and the user selects **Add Donation** again, the application should bring the existing window to the front instead of creating another instance.

Closing or selecting **Back** from the Add Donation window should return the user to the existing Doctor Menu rather than creating another Doctor Menu.

## Cause

The menu creates a new form instance every time the button is clicked:

```csharp
new AddDonation(id, connection).Show();

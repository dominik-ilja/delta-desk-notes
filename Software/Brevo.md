---
aliases:
cssclasses:
tags:
Related: []
Sources: []
Type: Documentation
---
# Brevo

- In Brevo, contacts are global, uniquely keyed by email (or other identifier), not scoped per “event.” If the same email signs up again (for a new event or list), it will typically update the existing contact (or merge) rather than create a wholly separate contact with the same email.
- You cannot have the same email exist as two completely independent contacts (with different name, SMS, etc.) unless you use workarounds (e.g. aliasing the email) because email is considered a unique identifier.
- If a new signup uses an email that already exists as a contact in Brevo, it will never create a second contact.
- Regarding confirmation emails: depending on your settings (single opt-in / double opt-in / no confirmation), a contact may receive a confirmation email, or might be added silently without confirmation.
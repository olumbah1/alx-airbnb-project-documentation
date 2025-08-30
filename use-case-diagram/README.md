# Use-Case-Diagram
Created a Use Case Diagram flow showing how features and functionalities will interact from one flow to the other between User Registration, Property, Payment, Booking.

1. User Registration & Login
 • Register (with details: username, email, password, etc.)
 • Login
 • Update Profile (optional after login)

Flow: A User must register → then login → then proceed to property-related actions.

2. Property Interaction
 • Search Property
 • View Property Details
 • Select Property

Flow: After login, the User searches → views → selects a property.
For Admin/Host, use cases are: Add Property, Edit Property, Delete Property.

3. Booking
 • Book Property
 • <<include>> Payment (since booking requires payment)
 • <<extend>> Cancel Booking (optional)
 • Booking History (view past/current bookings)

Flow: After selecting property → user can make a booking → booking leads to payment.

4. Payment
 • Make Payment
 • <<include>> Transaction History (automatically recorded)
 • <<extend>> Refund (if booking is cancelled)
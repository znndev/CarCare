
Academic project
# CarCare - Car Maintenance Management App
Academic project for CS 388T Agile Software Development, Section 7C1, Group 1.

## To Run the app

- Open `index.html` in any browser. Nothing needs to be installed.
- Data is saved in the browser (localStorage). To start again, tap **Reset demo data** on the home screen.
- Demo card for payment: `4242 4242 4242 4242`, any future expiry date, any 3 digits.

## Screens and owners

| Story | Screen | Owner |
|---|---|---|
| US01 | My cars, Add a vehicle | Norah Alrougi |
| US02 | Service centers (map and list) | Joud Aldhaban |
| US03 | Filters | Renad Alqahtani |
| US04 | Book a service | Shahad Alhusayni |
| US05 | Available slots (service center) | Sara Alzannan |
| US06 | Booking requests (service center) | Norah Alrougi |
| US07 | Pay for booking, Invoice | Renad Alqahtani |
| T0.1 | Shared data layer | Shahad Alhusayni |
| T0.2 | Home screen and navigation | Sara Alzannan |
| T0.3 | End-to-end test and final build | Joud Aldhaban |

Each section of the code in `index.html` starts with a comment naming its story and owner.

## Demo path

1. Home, then **I'm a driver**. Pick a center and tap **Book**.
2. Add a vehicle when asked, choose the problem and a free time, and send the request.
3. Tap **Open as** the center and **Accept** the request.
4. Tap **Switch side**, open **Bookings**, tap **Pay now**, and pay to get the invoice.

## Shared data (localStorage keys)

- `cars`: id, make, model, year, plate, odometer
- `centers`: id, name, district, rating, priceLevel, services, lat, lng
- `slots`: id, centerId, date, time, available, bookingId
- `bookings`: id, ref, mine, carId, car, centerId, slotId, date, time, issue, note, status, createdAt
- `invoices`: id, no, bookingId, sub, vat, total, method, last4, issuedAt

Booking status moves from `pending` to `accepted` or `rejected`, then to `paid`.

## Sprint 1 limits

- Card and Apple Pay payment is simulated; no real money moves.
- The map is drawn inside the app; no map service is called.
- Data stays on one device. Accounts and a shared backend are planned for Sprint 2 (US16).

## Testing

An end-to-end test run on 18/10/2026 passed 56 checks covering every acceptance criterion of US01 to US07.

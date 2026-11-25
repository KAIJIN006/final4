StaySwift room photo update

This update adds room photos for Standard, Deluxe, and Suite room types to the existing Flask project.

Files:
- app.py: updated homepage and Find a Room results to display the matching room photo.
- static/rooms/standard.jpg
- static/rooms/deluxe.jpg
- static/rooms/suite.jpg
- requirements.txt: unchanged (Flask and gunicorn)

To update an existing GitHub repository:
1. Replace the existing app.py with this app.py.
2. Upload the entire static folder (including static/rooms and all three JPG files) to the same repository level as app.py.
3. Keep your existing requirements.txt and Render environment variables unchanged.
4. Commit the changes. Render should deploy the new commit automatically; otherwise use Manual Deploy -> Deploy latest commit.

The room photos are illustrative concept images for the school project, not photographs of an actual hotel property. Prices shown on the cards come from the room records already stored in the app database.

Waiting-list confirmation update:
- When a guest or admin cancels a confirmed reservation, StaySwift checks for matching waiting-list requests for that room type and date range.
- Matching guests receive an email containing a Review & Confirm Booking link (email delivery still requires valid Resend configuration and a verified sender domain for recipients other than the Resend account owner).
- Opening the link displays the room, dates, and nightly price. It does NOT reserve the room.
- The guest must press Confirm Reservation. The first successful confirmation reserves the room; competing offers for overlapping dates become unavailable.

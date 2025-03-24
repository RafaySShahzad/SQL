SELECT u.Username, b.BookingID, c.CruiseName, c.Destination, b.BookingDate, b.RoomType, b.TotalPrice
FROM Users u
JOIN Bookings b ON u.UserID = b.UserID
JOIN Cruises c ON b.CruiseID = c.CruiseID
ORDER BY b.BookingDate DESC;

SELECT c.CruiseID, c.CruiseName, c.Destination, AVG(r.Rating) AS AvgRating, COUNT(r.ReviewID) AS TotalReviews
FROM Cruises c
JOIN Reviews r ON c.CruiseID = r.CruiseID
GROUP BY c.CruiseID, c.CruiseName, c.Destination
ORDER BY AvgRating DESC, TotalReviews DESC;


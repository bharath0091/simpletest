
SELECT      *
FROM        plays
INNER JOIN  reservations on plays.id = reservations.play_id
GROUP BY plays.id, plays.title, sum(reservations.number_of_tickets) AS reserved_tickets
ORDER BY    reserved_tickets DESC;



SELECT      plays.id, plays.title, count(reservations.number_of_tickets) AS reserved_tickets
FROM        plays
INNER JOIN  reservations on plays.id = reservations.play_id
ORDER BY    reserved_tickets DESC;

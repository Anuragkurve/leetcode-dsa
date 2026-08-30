Intuition
We need to report every person's first name and last name along with their city and state. The Person table contains the information about each person, while the Address table contains their address information. Since some people may not have an address, we need to make sure those people are still included in the result.

Approach
We use a LEFT JOIN between the Person and Address tables using personId as the matching column. A LEFT JOIN keeps every row from the Person table, even when there is no corresponding row in the Address table. For people without an address, city and state will therefore appear as NULL.

Finally, we select the person's first name and last name from Person, along with the city and state from Address.

Code
SELECT p.firstName, p.lastName, a.city, a.state
FROM Person p
LEFT JOIN Address a
    ON p.personId = a.personId;
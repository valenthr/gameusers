# Game users analysis

All analysis:
* [there](https://docs.google.com/spreadsheets/d/1nDF6XyUX4lqK0IlGMc0MSp06uWr8jsFb9h3P3jtiQMI/edit?usp=sharing) - of games, paid users and purchases;
* [there](https://docs.google.com/spreadsheets/d/1CHVbDpb-Syuoy5tXE9nvRSnrsW2KwkiVi8j379J8V6o/edit?usp=sharing) - of active users and activity.
  
## About data

The dataset contain 5 tables with information about game users:
1. [games_payments (2.0)](https://docs.google.com/spreadsheets/d/1jXQeUYch2KtZEOw-m7BqVpDaSUV0YqKZiK9stmPkl7o/edit?usp=sharing) - data about game purchases:
   user_id - unique id of each user;
   game_name - name of the game (there are only game 1, game 2 and game 3);
   payment_date - date of purchase;
   revenue_amount_usd - revenue per purchase in USD.
2. [games_paid_users](https://docs.google.com/spreadsheets/d/1UiiFHE2pJ17Rllac7przdDOyXBXW4OGVubBD5eaoC7o/edit?usp=sharing) - data about users, who has made a purchase:
   user_id - unique id of each user;
   game_name - name of the game;
   language - user's language;
   has_older_device_model - boolean value (if user plays in old device then "TRUE", if user plays in new device then "FALSE");
   age - age of each user.
3. [activity](https://docs.google.com/spreadsheets/d/1yrGRYWPMh-Oa1LMGRvI8M1o9QO9_YysmOZ4WPPORAnY/edit?usp=sharing) - data about attendance at games:
   user_id - unique id of each user;
   activity_date - date of visit;
   game_activity_name - combined column of name of the game and activity, in which user play (later was divided into 2 columns - game and activity_name);
   total_seconds - length of session.
4. [active_users](https://docs.google.com/spreadsheets/d/1yrGRYWPMh-Oa1LMGRvI8M1o9QO9_YysmOZ4WPPORAnY/edit?usp=sharing) - data about players, who visit games regularly:
   user_id - unique id of each user;
   game_name - name of the game;
   language - user's language;
   has_older_device_model - boolean value (if user plays in old device then "TRUE", if user plays in new device then "FALSE");
   age - age of each user.
5. [games(2.0)](https://docs.google.com/spreadsheets/d/1bVIW2UmfZl5KIbePGAqryYcR2BQvxx5Vm0yLxGx7rGQ/edit?usp=sharing) - comparison of games:
   game_name - name of the game;
   Ad spend - advertising spends;
   Total users count - number of users.
   
## Tools

Google Sheets

## Purpose

The main goal is to to gain insights from game user data, analyzing the various factors that affect purchases.

## Games comparison

For each game were calculated (in "games(2.0)" table):
1. Total revenue.
2. Paid users count.
3. CR to Paid.
4. ARPPU.
5. Average Age (of paid users).
6. Minimum age (of paid users).
7. Maximum age (of paid users).

## Age analysis. For the age of users were calculated:

1. Average age.
2. Standart deviation.
3. Median.
4. Interquartile range.
5. 10 percentile.
6. 90 percentile.
7. Interquartile range (of paid users in "games(2.0)" table).
8. 10 percentile (of paid users in "games(2.0)" table).
9. 90 percentile (of paid users in "games(2.0)" table).
10. Median age (of paid users in "games(2.0)" table).
11. Minimum and maximum age.

## DAU, WAU, Stickiness and prediction of this metrics:

For each day was calculated DAU, for each week - WAU and stickiness DAU/WAU. The values of the above metrics for 20 weeks were also predicted. WAU and DAU/WAU were visualized 

## Visualisations:

1. Division of users by language (for both paid and active users)
2. Division of users by device (for both paid and active users)
   
## New columns in "activity"
1. Language - data from "active users".
2. activity_type (unification activity_name in 5 types), activity_month (month of activity, first activity month (month, in which user made first visit), activity_month_number (difference between activity_month and first activity month - calculated columns (was calculated also for payments).

## Cohort analysis

Also were made the cohort analysis of user's retention activity month for active and paid users.

## Insights
1. The most used and sold game is game 3 - almost all paid and non-paid users are players of game 3. It also has a 5 times higher CR to paid and ARPPU.
2. Against this background, the only game stands out negatively, which did not recoup even 10% of its advertising costs - game 2. It means that for Game 2, the priority at this stage is not advertising spend, but spending on product quality.
3. From the age analysis, we learned that younger people are more willing to buy: average age of paid users is 23 years, median age - 22, but average age of active users is 28, median age - 25. Interquartile range of paid users are 1,5 times smaller - 9 against 15 of active users. Minimum age are the same - 14 years
4. About the oldest users. It was found that 10 percent of the oldest paid users are between 33 and 44 years old, and 10 percent of the oldest active users are between 42 and 83 years old. Conclusion - older users are also active, but have less desire to pay.
5. The most common ages of active users are 17, 18 and 23. The most common ages of paid users are 18, 19 and 25. Therefore, we can conclude that active users become paid after a year or 2 years of using the product.
6. DAU gradually increased throughout the year, but dropped significantly at the end of the year. It can be associated with Christmas. DAU/WAU remained roughly flat throughout the year, but dropped sharply in early March and then returned to normal values. There is a hypothesis that stickiness decreased due to the celebration of International Women's Day
7. Cohort analysis (for active users) revealed that user retention is roughly equal each month, with 1 exception - in July, retention after 1 month dropped sharply to half, but then almost no one dropped out from this cohort. It means that exactly for July users there were not enough interesting events during the first month of the game.
8. With the help of a cohort analysis of retention of paid users, 2 zones of the largest dropout of paying users were established - after the first month (which was expected) and after seventh months after making the first purchase. It means that at the time of 7 months after the first purchase, the games are not able to give the user such a paid product that he would like to pay for.

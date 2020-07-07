# Gold Medal Metrics

## Project Overview

Gold Medal Metrics allows users to:

 - View countries in a list with their population, GDP, and number of Olympic gold medals.
 - Sort the list of countries by any of these attributes, as well as alphabetically by name.
 - View a detailed description of a country, with statistics on their Olympic wins.
 - View a list of every Olympic win a country has with the year, season, winner name, city, and event.
 - Sort the list of Olympic wins by any of these attributes.

### Gold Medal Metric Functions

#### createCountryTable

Returns the SQL command that will create a table, named `Country` with the following columns:

 - `name` a required text field.
 - `code` a required text field.
 - `gdp` an integer.
 - `population` an integer.

#### createGoldMedalTable

Returns the SQL command that will create a table, named `GoldMedal` with the following columns:

 - `id` an integer that will function as the primary key.
 - `year` a required integer.
 - `city` a required text field.
 - `season` a required text field.
 - `name` a required text field.
 - `country` a required text field.
 - `gender` a required text field.
 - `sport` a required text field.
 - `discipline` a required text field.
 - `event` a required text field.

#### goldMedalNumber

Takes an argument, the name of a country. Returns the SQL command that will retrieve the number of gold medals that country has won in all Olympic games, aliased to the name `count`.

#### mostSummerWins

Takes an argument, the name of a country. Returns the SQL command that will retrieve the year where the given country won the most summer medals, along with the number of medals aliased to 'count'

#### mostWinterWins

Takes an argument, the name of a country. Returns the SQL command that will retrieve the year where the given country won the most winter medals, along with the number of medals aliased to 'count'

#### bestYear

Takes an argument, the name of a country. Returns the SQL command that will retrieve the `year` that country won the most Olympic medals, and how many medals were won, aliased to the name `count`.

#### bestDiscipline

Takes an argument, the name of a country. Returns the SQL command that will retrieve the `discipline` in which that country won the most Olympic medals, and how many medals were won, aliased to the name `count`.

#### bestSport

Takes an argument, the name of a country. Returns the SQL command that will retrieve the `sport` in which that country won the most Olympic medals, and how many medals were won, aliased to the name `count`.

#### bestEvent

Takes an argument, the name of a country. Returns the SQL command that will retrieve the `event` in which that country won the most Olympic medals, and how many medals were won, aliased to the name `count`.

#### numberMenMedalists

Takes an argument, the name of a country. Returns the SQL command that will retrieve the number of men who have won Olympic medals for that country, aliased to the name `count`.

#### numberWomenMedalists

Takes an argument, the name of a country. Returns the SQL command that will retrieve the number of women who have won Olympic medals for that country, aliased to the name `count`.

#### mostMedaledAthlete

Takes an argument, the name of a country. returns the sql command that will retrieve the `name` of the athlete who won olympic medals for that country, aliased to the name `count`.

#### orderedMedals

Takes three arguments, the name of the country and, optionally, a `field` to sort the results by and a boolean, `sortAscending` representing whether the list should be ascending in value (`true`) or descending (`false`). This function should return a SQL query that returns all fields for every Olympic medal won by the given country in the specified order, ascending or descending.


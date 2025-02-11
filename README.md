# AdvancedCodingProject
## Working with KSA entertainment

# 🧠 Let`s learn how to load a csv file in MySQL
Step 1: Create or Select a Database Open MySQL Workbench. Create a new database

<img width="364" alt="image" src="https://github.com/user-attachments/assets/3d97f68f-67fd-4098-a8ca-6cbf92fca7ff" />

or select an existing one. 

Step 2: Use the Table Data Import Wizard Right-click on the database in the Navigator panel. Select Table Data Import Wizard from the context menu.

<img width="789" alt="image" src="https://github.com/user-attachments/assets/26f02b7a-0d14-4bb4-9127-5d49f417d641" />

Step 3: Select the CSV File In the wizard, browse to and select the CSV file you want to import. Click Next.

## 1. Select All Theaters
Description: Retrieves all records from the cleaned_file table, displaying details about each theater.

```SELECT * FROM cleaned_file;```
<img width="994" alt="image" src="https://github.com/user-attachments/assets/cad01907-e603-4cba-b0f2-ebf242289af4" />

## 2. Get Theaters with a Rating of 5
Description: Fetches the names, locations, and best comments of theaters with a perfect rating of 5.

```
SELECT name, location, best_comment 
FROM cleaned_file 
WHERE rating = 5;
```
<img width="996" alt="image" src="https://github.com/user-attachments/assets/05246121-6733-4d93-92d8-e680b9d9b60d" />

## 3. Count Theaters by Genre
Description: Counts the number of theaters in each genre.

```
SELECT genre, COUNT(*) AS theater_count 
FROM cleaned_file 
GROUP BY genre;
```
<img width="867" alt="image" src="https://github.com/user-attachments/assets/b1ee0f7f-c585-4c95-b4e8-8a4e936f377b" />

## 4. Find Theaters with More than 10,000 Reviews
Description: Lists theaters that have received more than 10,000 reviews.
```
SELECT name, review_count 
FROM cleaned_file 
WHERE review_count > 10000;
```
<img width="872" alt="image" src="https://github.com/user-attachments/assets/1fc62d8d-6b93-47e5-8876-e98992c0764d" />

## 5. Average Rating of Theaters by Location
Description: Calculates the average rating of theaters for each location, ordered by average rating in descending order.

```
SELECT location, AVG(rating) AS average_rating 
FROM cleaned_file 
GROUP BY location;
```
<img width="867" alt="image" src="https://github.com/user-attachments/assets/5d803b39-f6c1-4dcd-a25d-f799ac72a6f3" />

## 6. Find Theaters with a Rating of 0
Description: Retrieves the names and locations of theaters that have a rating of 0.
```
SELECT name, location, rating
FROM cleaned_file 
WHERE rating = 0;
```
<img width="872" alt="image" src="https://github.com/user-attachments/assets/289707dc-7c2b-4d77-af70-5a092f6d2625" />

## 7. Find Theaters Showing Action Movies
Description: Retrieves the names and locations of theaters that are showing Action movies.
```
SELECT name, location 
FROM cleaned_file 
WHERE genre LIKE '%Action%';
```
<img width="871" alt="image" src="https://github.com/user-attachments/assets/803b6874-89bc-4b3b-9150-0446c27a3f2c" />

## 8. Find Comments for Theaters Rated Below 3
Description: Fetches the names and comments of theaters that have a rating below 3.
```
SELECT name, best_comment 
FROM cleaned_file 
WHERE rating < 3;
```
<img width="870" alt="image" src="https://github.com/user-attachments/assets/278b0fa4-289b-47a4-ab45-371ef97a185e" />

## 9. Count of Theaters by Rating
Description: Counts the number of theaters for each rating category.

```
SELECT rating, COUNT(*) AS count 
FROM cleaned_file 
GROUP BY rating;
```
<img width="870" alt="image" src="https://github.com/user-attachments/assets/4c2beefc-eaa5-42f9-a72c-f48738a1dee9" />


## 10. Get Theaters in Riyadh with a Rating of 4 or Higher
Description: Retrieves the names and locations of theaters in Riyadh that have a rating of 4 or higher.
```
SELECT name, location 
FROM cleaned_file 
WHERE location LIKE '%Riyadh%' AND rating >= 4;
```
<img width="870" alt="image" src="https://github.com/user-attachments/assets/5a958f8e-2965-453f-a107-601906036dd5" />


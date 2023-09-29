## Guidance
Answer the following questions considering the [learning outcomes for this week](https://learn.foundersandcoders.com/course/syllabus/developer/database/learning-outcomes/).
Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of a learning outcome you have achieved this week.
> **Link multiple records in one table to multiple records in another**
>
> This was difficult but we were all super pleased when we got this to work! It links two of our tables (venue, cuisine) through creating a new table (venue_cuisine) with a prepared statement and then returns them in the listVenueCuisines function.

```javascript
const select_venue_cuisines = db.prepare(/*sql*/ ```sql 
    `
    SELECT
        venue.name AS venue_name,
        GROUP_CONCAT(cuisine.name, ', ') AS cuisine_names
    FROM venue
    JOIN venue_cuisine ON venue.id = venue_cuisine.venue_id
    JOIN cuisine ON venue_cuisine.cuisine_id = cuisine.id
    GROUP BY venue.name
`);

function listVenueCuisines() {
    return select_venue_cuisines.all();
}
```

> **Set up separate environments for production and testing** 
> <img width="690" alt="Screenshot 2023-09-29 at 10 54 52" src="https://github.com/fac28/progress-log/assets/117110978/cf269aff-b3de-4cbc-9918-d9587c446d9d">

> We decided to create a dev-branch this week which was great, it made the workflow nice and smooth. 

> ### 2. Show an example of a learning outcome you have struggled with and/or would like to re-visit.
**Create, read update and delete from our database using SQL queries**

>We successfully used SQL queries to delete from the database but I'd like to revisit deleting from the database:

``` javascript
const insert_cuisine = db.prepare(/*sql*/ ```sql `
  INSERT INTO cuisine (name)
  VALUES ($cuisine)
  RETURNING id AS cuisine_id
`);

function createCuisine(cuisine) {
  return insert_cuisine.get({ cuisine });
}

```

## Feedback
> [**Course Facilitator name**]  
> [*What went well*]  
> [*Even better if*]

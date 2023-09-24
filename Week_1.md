## Guidance
Answer the following questions considering the [learning outcomes for this week](https://learn.foundersandcoders.com/course/syllabus/developer/server/learning-outcomes/).
Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of a learning outcome you have achieved this week.
#### Read information sent in a URL query string
Using information sent in a query string is a convenient way to collect user input and utilise it in your code. Take the following example:
```
server.get("/colour", (req, res) => {
  const colour = req.query.hex || "ffffff";
  res.send(/*html*/ `<!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <link rel="stylesheet" href="/style.css">
      <title>Server Workshop</title>
      <style>
      body{
        background-color: #${colour};
      }
    </style>
    </head>
    <body>
      <form action="/colour" method="GET">
        <label for="hex">Type a colour</label>
        <input type="text" name="hex">
        <button type="submit">Submit</button>
      </form>
    </body>
    </html>`);
});
```
Here we have a form that makes a get request and has one text input for a user to enter a hex colour code. By utilising the name attribute of the input element we can attach the value of the user input to the request using a query string, which looks in this instance like this:
```
colour?hex=whatever-user-inputs
```
Then by using the query method of the request object we can retrieve that data using the key name we specified, in this case ```hex```. Here we assign that value to a constant called colour
```
const colour = req.query.hex
```
We then use this data to do some inline styling in our html and presto! We have a form input that can change the background of the page.
```
 <style>
      body{
        background-color: #${colour};
      }
    </style>
```

 ### 2. Show an example of a learning outcome you have struggled with and/or would like to re-visit.
### Write tests with the built-in Node Test Runner
As is probably often the case I feel like I gave the least amount of time in attempting to the really understand the implementation tests for servers. The workshops we helpful but also threw a lot of information at us without explanation, like all the helper functions. Although I was able to write some tests and make things pass I don't have real understanding yet and the async nature of these test means I really need to go back and revise. 


## Feedback
### Beth and Alphonso!  
I think things in general went well and I don't have a lot of feedback yet as I feel like we are all just settling in. But I had a lot of fun with the project this week and thought the roles and working methods introduced were really helpful.

> [*Even better if*]
I should have take more advantage of having Mark in the room! So maybe more opportunities to make use of our weekly mentors.

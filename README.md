# What to Cook
App to help users find a new recipe to try in the kitchen by generating random recipes after sign-up.

### Page Design
##### Inserting background image:
``` 
body {
  background-image: url("https://i.dietdoctor.com/wp-content/uploads/2016/08/14-day-meal-plan-presentation-16-9.jpg?auto=compress%2Cformat&w=1600&h=900&fit=crop");
  background-size: cover;
}
```

### File Installation (Linux Terminal)
*sudo npm install -g sequelize*<br>
*sudo npm install -g sequelize-cli*<br>
*sudo npm install -g pg*<br>

### API information
##### Database: 
https://www.themealdb.com/
##### API: 
https://www.themealdb.com/api.php

### Get and Send API data to app
``` js
app.get('/',isLoggedIn, function(req, res) {
  if (req.user) {
  axios.get('https://www.themealdb.com/api/json/v1/1/random.php')
    .then(function (response) {
      console.log(JSON.stringify(response.data.meals[0]));
      res.render("recipes", {
        recipe: response.data.meals[0]
      })
      console.log(typeof response.data);
    })
  }  
  else res.render('index', { alerts: res.locals.alerts });
});
```

### Pass Random Recipe to App
``` ejs
<pre><%= JSON.stringify(recipe) %></pre>
```
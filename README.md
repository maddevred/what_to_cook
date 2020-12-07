# What to Cook
App to help users find a new recipe to try in the kitchen by generating random recipes after sign-up.

### Page Design
##### Inserting background image:
``` 
body {
  background-image: url("https://www.aafoodservice.com/wp-content/themes/custom-theme/img/slider-v1704.jpg");
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
```
app.get('/', function(req, res) {
  
  axios.get('https://www.themealdb.com/api/json/v1/1/random.php')
    .then(function (response) {
      // handle success
      console.log(response.data);
    })

  console.log(res.locals.alerts);
  res.render('index', { alerts: res.locals.alerts });
});
```

*** ADD TO THIS!!! NEEDS SEND INFO!!! ***


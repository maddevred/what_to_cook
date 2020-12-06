# What to Cook
App to help users decide on a new recipe to try by generating random recipes after sign-up.

### Page Design
##### Inserting background image:
``` 
body {
  background-image: url("https://www.aafoodservice.com/wp-content/themes/custom-theme/img/slider-v1704.jpg");
  background-size: cover;
} 
```

##### Centering header tag:
```
h1 {
  color: white;
  text-align: center;
  position: absolute;
  top: 50%;
  left: 50%;
  margin-right: -50%;
  transform: translate(-50%, -50%);
```

##### Adding subheader BELOW header tag:
```
text-align: center;
  position: absolute;
  top: 60%;
  left: 50%;
  margin-right: -50%;
  transform: translate(-50%, -50%);
```

### Get and Send API data to host server
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

### Where I got my API information from 
##### Database: https://www.themealdb.com/

##### API: https://www.themealdb.com/api.php

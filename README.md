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
<<<<<<< HEAD
##### Centering header tag:
=======
##### Centering header tag in background:
>>>>>>> 563b8fc38676bfe18fc5489661652228a6687080
```
h1 {
  color: white;
  text-align: center;
  position: absolute;
<<<<<<< HEAD
  top: 50%;
=======
  top: 40%;
>>>>>>> 563b8fc38676bfe18fc5489661652228a6687080
  left: 50%;
  margin-right: -50%;
  transform: translate(-50%, -50%);
```
##### Adding subheader BELOW header tag:
```
text-align: center;
  position: absolute;
<<<<<<< HEAD
  top: 60%;
=======
  top: 50%;
>>>>>>> 563b8fc38676bfe18fc5489661652228a6687080
  left: 50%;
  margin-right: -50%;
  transform: translate(-50%, -50%);
```

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
<<<<<<< HEAD
=======

>>>>>>> 563b8fc38676bfe18fc5489661652228a6687080

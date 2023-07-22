# Businesscard.
This project was made using HTML5.0 and CSS3.0. This project consists of a two-sided business card. The developer is shown on the front and the developer's name and a small interaction with each of the social networks is shown on the back.

HTML:

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Tarjeta de Presentación</title>
    <link rel="stylesheet" href="mitarjetapresentacion.css">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/latest/css/font-awesome.min.css">
</head>

<body>
    <div class="card">
        <div class="card-front"></div>
        <div class="card-back">
            <h2>Oswaldo Jesús Marín Pagés<br><span>Web Dev</span></h2>
            <div class="social-icons">
                <a href="#" class="fa fa-facebook" aria-hidden="true"></a>
                <a href="#" class="fa fa-twitter" aria-hidden="true"></a>
                <a href="#" class="fa fa-google-plus" aria-hidden="true"></a>
                <a href="#" class="fa fa-linkedin" aria-hidden="true"></a>
                <a href="#" class="fa fa-instagram" aria-hidden="true"></a>
            </div>
        </div>
    </div>  
</body>

</html>

CSS:

@import "https://fonts.googleapis.com/css?family=Josefin+Sans:400,700";
body {
  margin: 0;
  padding: 0;
  font-family: "Josefin Sans", sans-serif;
  background-color: #000;
  color: #fff;
}

body a {
  color: orange;
  text-decoration: none;
}

.card {
  position: absolute;
  top: 50%;
  left: 50%;
  height: 400px;
  width: 300px;
  transform: translate(-50%, -50%);
  transform-style: preserve-3d;
  perspective: 600px;
  transition: 0.5s;
}

.card:hover .card-front {
  transform: rotateX(-180deg);
}
.card:hover .card-back {
  transform: rotateX(0deg);
}

.card-front {
  height: 100%;
  width: 100%;
  background-image: url(img/A7Rm2gSV_400x400.jpg);
  background-position: 50% 50%;
  background-size: cover;
  position: absolute;
  top: 0;
  left: 0;
  background-color: blue;
  backface-visibility: hidden;
  transform: rotateX(0deg);
  transition: 0.5s;
}

.card-back {
  height: 100%;
  width: 100%;
  position: absolute;
  top: 0;
  left: 0;
  background-color: darkblue;
  backface-visibility: hidden;
  transform: rotateX(180deg);
  transition: 0.5s;
  color: #ffffff;
  text-align: center;
}

.card-back h2 {
  margin: 60% auto 35% auto;
  font-size: 26px;
}
.card-back h2 span {
  font-size: 20px;
}
.card-back a {
  height: 20px;
  width: 20px;
  padding: 5px 5px;
  border-radius: 4px;
  line-height: 20px;
}
.card-back a:hover {
  color: blue;
  background-color: #000;
}

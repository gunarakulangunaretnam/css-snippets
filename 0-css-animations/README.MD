# CSS Animation Snippets

## Example 0

####  HTML Code

```html

<!DOCTYPE html>
<html >
  <head>
    <meta charset="UTF-8">
    <title>Playing a CSS animation on hover</title>
    <link href="styles.css" type="text/css" media="all" rel="Stylesheet"/>

  </head>

  <body>

    <link href='http://fonts.googleapis.com/css?family=Bree+Serif' rel='stylesheet' type='text/css'>

<div class="wrap">
  <div class="sticker"></div>
  <div class="msg">new!</div>
</div>

  </body>
</html>

```

####  CSS Code

```css
body {padding:6em; background:#fcfcfc;}

.wrap {width:200px; margin:auto;  z-index:1;}

.msg {
  color: whitesmoke;
  text-align:center;
  font-family: 'Bree Serif', Courier, monospaced;
  font-size:3.5em;
  width:200px;
  position:absolute;
  margin:55px 0 0 2px;
  pointer-events: none;
}

.sticker {
  width:200px;
  height:200px;
  position:absolute;
  background: url(sticker.png) top center no-repeat;
  animation:spin 10s linear infinite;
  animation-play-state:paused;/*It is pasused*/
}

    .sticker:hover {/*Running*/


        animation-play-state:running;
    }


@keyframes spin {

    0%{transform:rotate(0turn);}
    100%{transform:rotate(1turn);}
    /*1turn means it will completly rotate once.*/

}

```

#### Output

![Banner Image](github-readme-contents/example-0-output.gif)

## Example 1

####  HTML Code

```html

<html>
	<head>
		<title>Animation Basics</title>		
		<link rel="stylesheet" href="styles.css" media="all" />
	</head>
	<body>

	<div class="wrapper">
		<img src="tall_robot.svg" width="150" alt="tall robot" class="robot" />
	</div>

	</body>
</html>

```

####  CSS Code

```css
body {
	background-image: url('background.png');
	background-size: cover;
	background-position: 0px -250px;
}

.wrapper {
	margin: 20em auto 2em auto;
	width:80%;
	position:relative;
}

.robot {

  animation-name:slide;
  animation-duration:3s;
  animation-timing-function:ease-in;
  animation-iteration-count:1;/*infinite will not stop*/
  animation-delay:1s;
  animation-fill-mode:forwards;/*The aniamtion-fill-mode is useful to decide how to finish the animation*/
                               /*backwords and both*/
}

@keyframes slide{

	from{transform:translate(0px);}
	to{transform:translate(900px);}


}

```

#### Output

![Banner Image](github-readme-contents/example-1-output.gif)

## Example 2

####  HTML Code

```html
<html>
	<head>
		<title>animation-fill-mode</title>
		<link rel="stylesheet" href="styles.css" media="all" />
	</head>

	<body>		
		<img class="ball" src="ball.png" alt="ball"width="111" height="111" />
	</body>

</html>
```

####  CSS Code

```css

body {margin: 4em 10%; background:#493F5B;}

 .ball {
	animation-name: move-left-right;
	animation-duration: 2s;
	animation-timing-function: ease-in;
	animation-iteration-count: 1;
 	animation-delay:1s;
    animation-fill-mode:both;
}

@keyframes move-left-right {
	0% {transform: translateX(100px) rotate(0turn);}
	20% {transform: translateX(-10px) rotate(-0.5turn);}
	100% {transform:translateX(450px) rotate(2turn);}			
}
```

#### Output

![Banner Image](github-readme-contents/example-2-output.gif)


## Example 3

####  HTML Code

```html
<html>
	<head>
		<title>Animation Basics</title>		
		<link rel="stylesheet" href="styles.css" media="all" />
	</head>
	<body>

	<div class="wrapper">
		<img src="tall_robot.svg" width="150" alt="tall robot" class="robot" />
	</div>

	</body>
</html>

```

####  CSS Code

```css
body {
	background-image: url('background.png');
	background-size: cover;
	background-position: 0px -250px;
}

.wrapper {
	margin: 20em auto 2em auto;
	width:80%;
	position:relative;
}

.robot {
	animation-name: slide;
	animation-duration: 2s;
	animation-timing-function: ease-in;
	animation-iteration-count: 1;
	animation-fill-mode:forwards;
    animation-direction:reverse;/*This will run the animation reversly*/
}

@keyframes slide {
	from {transform: translateX(0);}
	to {transform: translateX(900px);}
}
```

#### Output

![Banner Image](github-readme-contents/example-3-output.gif)

## Example 4

####  HTML Code

```html
<html>
	<head>
		<title>Animation Basics</title>		
		<link rel="stylesheet" href="styles.css" media="all" />
	</head>
	<body>

	<div class="wrapper">
		<img src="tall_robot.svg" width="150" alt="tall robot" class="robot" />
	</div>

	</body>
</html>
```

####  CSS Code

```css

body {
	background-image: url('background.png');
	background-size: cover;
	background-position: 0px -250px;
}

.wrapper {
	margin: 20em auto 2em auto;
	width:80%;
	position:relative;
}

.robot {
	animation-name: slide;
	animation-duration: 2s;
	animation-timing-function: ease-in;
	animation-iteration-count: 2;/*We should make to 2*/
	animation-fill-mode:forwards;
    animation-direction:alternate;/*This will move the element in both*/
}

@keyframes slide {
	from {transform: translateX(0);}
	to {transform: translateX(900px);}
}
```

#### Output

![Banner Image](github-readme-contents/example-4-output.gif)

## Example 5

####  HTML Code

```html
<html>
	<head>
		<title>Animation Basics</title>		
		<link rel="stylesheet" href="styles.css" media="all" />
	</head>
	<body>

	<div class="wrapper">
		<img src="tall_robot.svg" width="150" alt="tall robot" class="robot" />
	</div>

	</body>
</html>
```

####  CSS Code

```css
body {
	background-image: url('background.png');
	background-size: cover;
	background-position: 0px -250px;
}

.wrapper {
	margin: 20em auto 2em auto;
	width:80%;
	position:relative;
}

.robot {
	animation-name: slide;
	animation-duration: 2s;
	animation-timing-function: ease-in;
	animation-iteration-count: 2;/*We should make to 2*/
	animation-fill-mode:forwards;
    animation-direction:alternate-reverse;/*This will move the element from reverse to start*/
}

@keyframes slide {
	from {transform: translateX(0);}
	to {transform: translateX(900px);}
}
```

#### Output

![Banner Image](github-readme-contents/example-5-output.gif)

## Example 6

####  HTML Code

```html
<html>
	<head>
		<title>Animation Basics</title>		
		<link rel="stylesheet" href="styles.css" media="all" />
	</head>
	<body>

	<div class="wrapper">
		<img src="tall_robot.svg" width="150" alt="tall robot" class="robot" />
	</div>

	</body>
</html>
```

####  CSS Code

```css
body {
	background-image: url('background.png');
	background-size: cover;
	background-position: 0px -250px;
}

.wrapper {
	margin: 20em auto 2em auto;
	width:80%;
	position:relative;
}

.robot {
	animation-name: slide;
	animation-duration: 3s;
	animation-timing-function: cubic-bezier(.41,.07,.62,.91) ;
	animation-fill-mode:forwards;
	animation-direction: alternate;
	animation-iteration-count: 4;
}

@keyframes slide {
	0%{transform: translateX(0);}
	20% {transform:translateX(200px);}
	35% {transform:translateX(0);}
	90% {transform: translateX(980px);}
	100% {transform: translateX(900px);}
}
```

#### Output

![Banner Image](github-readme-contents/example-6-output.gif)

## Example 7

####  HTML Code

```html
<!DOCTYPE html>
<html>
<head>
	<title>Clouds</title>
	<link rel="stylesheet" href="styles.css" media="all" />

</head>
<body>

<div class="sky">
	<div class="cloud fcloud01"></div>
	<div class="cloud fcloud02"></div>
</div>

</body>
</html>
```

####  CSS Code

```css
body {
  background:#678bb3;
  padding:0;
  margin:0;
}

.sky {
  width:100%;
  height:1000px;
  background: transparent url(img/sky.jpg) top left no-repeat;
  background-size: 100% 100%;
  margin:auto;
  position:relative;
}

.cloud {
  width: 250px;
  height:200px;
  position:absolute;
  background:transparent url(img/front_cloud.png) 0 0 no-repeat;
}

.fcloud01 {
  top:100px;
  z-index:100;

      animation:drift 25s linear infinite;
      /*Animation name,duration,type of timing function , iteration-count*/
  }

.fcloud02 {
  top:240px;
  z-index: 200;

      animation:drift 45s  linear infinite;
        /*Animation name,duration,delay,type of timing function , iteration-count*/
}

@keyframes drift {

  from{transform:translateX(-255px);}
  to{transform:translateX(1350px);}

}
```

#### Output

![Banner Image](github-readme-contents/example-7-output.gif)

## Example 8

####  HTML Code

```html
<!DOCTYPE html>
<html >
  <head>
    <meta charset="UTF-8">
    <title>Animated entrance</title>
    <link rel="stylesheet" href="styles.css">

  </head>

  <body>

    <section>
    <div class="card">
        <div class="icon-space">
        <img src="pink_robot.svg"/>
      </div>
        <div class="inner">
           <div class="info">
        <h2>Your Reservation is complete!</h2>
          <p>Come meet the robots on Saturday at 2pm. <br/>
           We can't wait to see you there!</p>
          <button>Make another reservation</button>
        </div>

      </div>
    </div>
</section>


  </body>
</html>
```

####  CSS Code

```css

@import url(http://fonts.googleapis.com/css?family=Roboto+Condensed:400,300|Lato:300,400);

body {
  background: rgb(249, 228, 202);
  font-family: 'Lato', sans-serif;
  line-height: 1.4;
  font-weight: 300;
  margin: 6em 0;
  overflow:hidden;
}

section {
  width: 500px;
  margin: auto;
}

.card {
  background: rgba(255, 255, 255, 0.9);
  font-family: 'Roboto Condensed', sans-serif;
  padding: .5em 2em;
  border-radius: 4px;
  box-shadow: 0px 0px 0px 1px rgba(0, 0, 0, 0.03), 0px 1px 2px 0px rgba(0, 0, 0, 0.05);
  margin: auto;
  width: 430px;
  text-align: center;
}

.inner {
  margin: 1em 0 2em 0;
}

h2 {
  color: #FB5362;
  font-family: 'Roboto Condensed', sans-serif;
  font-size: 40px;
  font-size: 2rem;
  font-weight: 300;
  margin: 0 0 .15em 0;
}

h3 {
  margin: 0 0 .5em 0;
}

p {
  margin: 0;
  color: #666666;
}

.icon-space {
  margin-top: -40px;

}
.icon-space img {
  border-radius: 50%;
  display: block;
  margin: auto;
  border: 4px solid white;
  background: white;
  width: 100px;
  height: 100px;
  box-shadow: 0px 0px 0px 1px rgba(0, 0, 0, 0.03), 0px 1px 2px 0px rgba(0, 0, 0, 0.2);
}

button {
  width: auto;
  height: 40px;
  display: block;
  margin: 2em auto;
  padding: 0 5%;
  border: none;
  border-radius: 4px;
  background-color: #1A9DB4;
  color: whitesmoke;
  font-size: 1em;
  font-family: 'Lato', sans-serif;
  font-weight: 400;
  box-shadow: 0px 0px 0px 1px rgba(0, 0, 0, 0.03), 0px 1px 2px 0px rgba(0, 0, 0, 0.3);
  transition: background-color .3s ease-out;
}
button:hover {
  background-color: #FB5362;
}

section {

    animation:slide_in .8s linear,fade_in .5s ease-in;
    /*If we want to add multiple animations we should use , seperator*/

}

@keyframes slide_in {

    0%{
        transform:translateY(400px);
        animation-timing-function:ease-in
    }
    60%{
        transform:translateY(-50px);
        animation-timing-function:ease-out;
    }
    80%{
        transform:translateY(10px);
        animation-timing-function:ease-in;
    }
    100%{

        transform:translateY(0);
        animation-timing-function:ease-out;
    }

}

@keyframes fade_in {


    from {
    opacity:0;
    }
    to {

    opacity:1;
    }

}
```

#### Output

![Banner Image](github-readme-contents/example-8-output.gif)

## Example 9

####  HTML Code

```html
<!DOCTYPE html>
<html >
  <head>
    <meta charset="UTF-8">
    <title>Animating 3D Transforms</title>
     <link href="styles.css" type="text/css" media="all" rel="Stylesheet"/>

  </head>

  <body>

    <link href='http://fonts.googleapis.com/css?family=Alfa+Slab+One' rel='stylesheet' type='text/css'>

 <div>
  <span>U</span>
  <span>P</span>
  <span>&</span>
  <span>O</span>
  <span>V</span>
  <span>E</span>
  <span>R</span>
  </div>

  </body>
</html>
```

####  CSS Code

```css
body {
  font-family: 'Alfa Slab One', cursive;
  font-size:6rem;
  background:#2c333a;
}

div {
  width:80%;
  margin:4rem auto;
  text-align:center;
  perspective: 800px;
 }

span {
   display:inline-block;
   margin-left: -20px;
   color:#77c6bc;
   transform-origin:50% 70%;
}


span:nth-child(2n) {
  color:#95b8cb;
}

span:nth-child(1) {

    animation:filp-Up 1s cubic-bezier(0.68, -0.55, 0.26, 1.55) both;
}

span:nth-child(2) {
  margin-right:30px;
   animation:filp-Up 1s cubic-bezier(0.68, -0.55, 0.26, 1.55) 0.2s both;
}

span:nth-child(3) {
 margin-right:30px;
  animation:filp-Up 1s cubic-bezier(0.68, -0.55, 0.26, 1.55) 0.4s both;
}

span:nth-child(4) {
     animation:filp-Up 1s cubic-bezier(0.68, -0.55, 0.26, 1.55) 0.6s both;
}

span:nth-child(5) {
  margin-left:-28px;
   animation:filp-Up 1s cubic-bezier(0.68, -0.55, 0.26, 1.55) 0.8s both;
 }

span:nth-child(6) {
     animation:filp-Up 1s cubic-bezier(0.68, -0.55, 0.26, 1.55) 1s both;
}

span:nth-child(7) {
     animation:filp-Up 1s cubic-bezier(0.68, -0.55, 0.26, 1.55) 1.2s both;
}

@keyframes filp-Up {

    0%{transform:rotateX(90deg);}
    100%{transform:rotateX(0deg);}
}
```

#### Output

![Banner Image](github-readme-contents/example-9-output.gif)

## Example 10

####  HTML Code

```html
<!DOCTYPE html>
<html >
  <head>
    <meta charset="UTF-8">
    <title>Animating 3D Transforms</title>
     <link href="styles.css" type="text/css" media="all" rel="Stylesheet"/>

  </head>

  <body>

    <link href='http://fonts.googleapis.com/css?family=Alfa+Slab+One' rel='stylesheet' type='text/css'>

 <div>
  <span>U</span>
  <span>P</span>
  <span>&</span>
  <span>O</span>
  <span>V</span>
  <span>E</span>
  <span>R</span>
  </div>

  </body>
</html>
```

####  CSS Code

```css
body {
  font-family: 'Alfa Slab One', cursive;
  font-size:6rem;
  background:#2c333a;
}

div {
  width:80%;
  margin:4rem auto;
  text-align:center;
  perspective: 800px;
 }

span {
   display:inline-block;
   margin-left: -20px;
   color:#77c6bc;
   transform-origin: 50% 70%;
}


span:nth-child(2n) {
  color:#95b8cb;
}

span:nth-child(1) {
  animation: flipUp 1s cubic-bezier(0.68, -0.55, 0.26, 1.55) both,
             flipDown .5s cubic-bezier(0.45, 0.03, 0.51, 0.95) 2s forwards,
             swing 4s cubic-bezier(0.45, 0.03, 0.51, 0.95) forwards 4.1s;
}

span:nth-child(2) {
  margin-right:30px;
  animation: flipUp 1s cubic-bezier(0.68, -0.55, 0.26, 1.55) .2s both,
             flipDown .5s cubic-bezier(0.45, 0.03, 0.51, 0.95) 2.2s forwards,
             swing 4s cubic-bezier(0.45, 0.03, 0.51, 0.95) forwards 3.8s;
}

span:nth-child(3) {
 margin-right:30px;
 animation: flipUp 1s cubic-bezier(0.68, -0.55, 0.26, 1.55) .4s both,
            flipDown .5s cubic-bezier(0.45, 0.03, 0.51, 0.95) 2.4s forwards,
            swing 4s cubic-bezier(0.45, 0.03, 0.51, 0.95) forwards 4.4s;
}

span:nth-child(4) {
 animation: flipUp 1s cubic-bezier(0.68, -0.55, 0.26, 1.55) .6s both,
            flipDown .5s cubic-bezier(0.45, 0.03, 0.51, 0.95) 2.6s forwards,
            swing 4s cubic-bezier(0.45, 0.03, 0.51, 0.95) forwards 4.8s;
}

span:nth-child(5) {
  margin-left:-28px;
  animation: flipUp 1s cubic-bezier(0.68, -0.55, 0.26, 1.55) .8s both,
            flipDown .5s cubic-bezier(0.45, 0.03, 0.51, 0.95) 2.8s forwards,
            swing 4s cubic-bezier(0.45, 0.03, 0.51, 0.95) forwards 4.6s;
 }

span:nth-child(6) {
  animation: flipUp 1s cubic-bezier(0.68, -0.55, 0.26, 1.55) 1s both,
            flipDown .5s cubic-bezier(0.45, 0.03, 0.51, 0.95) 3s forwards,
            swing 4s cubic-bezier(0.45, 0.03, 0.51, 0.95) forwards 5s;
}

span:nth-child(7) {
  animation: flipUp 1s cubic-bezier(0.68, -0.55, 0.26, 1.55) 1.2s both,
             flipDown .5s cubic-bezier(0.45, 0.03, 0.51, 0.95) 3.2s forwards,
             swing 4s cubic-bezier(0.45, 0.03, 0.51, 0.95) forwards 4s;

}

@keyframes flipUp {
  from {transform: rotateX(90deg);}
  to {tranform: rotateX(0deg);}
}


@keyframes flipDown {
  to {transform: rotateX(-180deg);}
}


@keyframes swing {
  0% {
     transform: rotateX(-180deg);
  }

  20% {
    transform: rotateX(-180deg) rotateY(-45deg);
  }

  40% {
    transform: rotateX(-180deg) rotateY(45deg);
  }

  60% {
    transform: rotateX(-180deg) rotateY(-45deg);
  }

  80% {
    transform: rotateX(-180deg) rotateY(45deg);
  }

  100% {
    transform: rotateX(-180deg);
  }
}
```

#### Output

![Banner Image](github-readme-contents/example-10-output.gif)

## Example 11

####  HTML Code

```html
<html>
	<head>
		<title>Transform Basics</title>		
		<link rel="stylesheet" href="styles.css" media="all" />
	</head>
	<body>

	<div class="wrapper">
		<img src="blue_robot.svg" width="350" alt="tall robot" class="blue_robot" />
	</div>

	</body>
</html
```

####  CSS Code

```css
/* Animation Basics */
body {
	background-color: #D8E8FA;
}

.wrapper {
	margin: 2em auto 2em auto;
	width:350px;
	position:relative;
}

.blue_robot {
	transform: translate(100px,50px) skew(20deg) scale(2) rotate(45deg);

	/*
	    transale() is use to move the element.
        skew() is used to bend the element
        scale() is used to increase the size of the element.
        rotate() is used to rotate the element.
	*/
}
```

#### Output

![Banner Image](github-readme-contents/example-11-output.gif)

## Example 12

####  HTML Code

```html
<html>
	<head>
		<title>Transforms</title>		
		<link rel="stylesheet" href="styles.css" media="all" />
	</head>
	<body>

	<div class="wrapper">
		<img src="london.jpg" width="500px" alt="London">
		</div>
	</div>

	</body>
</html>
```

####  CSS Code

```css

body {
	background-color: #D8E8FA;
}

.wrapper {
	margin: 2em auto 2em auto;
    perspective:300px;/* We must add perspective to make 3d effects to the content of the img.*/
                       /*We can give 100px or less than it to make it much more better*/                         
}

img {
	display:block;
	margin: 0 auto;
    transform:rotateY(45deg);/*This is the value for the rotate*/

}
```

#### Output

![Banner Image](github-readme-contents/example-12-output.png)

## Example 13

####  HTML Code

```html
<html>
	<head>
		<title>Transition Basics</title>		
		<link rel="stylesheet" href="styles.css" media="all" />
	</head>
	<body>

	<div class="wrapper">
		<h2></h2>
		<p>Roll into the future right now and buy your very own robot!</p>
		<button>BUY NOW</button>
	</div>

	</body>
</html>
```

####  CSS Code

```css
@import url(https://fonts.googleapis.com/css?family=Lato:400,900,300,300italic,400italic,900italic);

body {
	background-color: #f7e4fe;
	background-image: url('purple_diag_background.svg');
	background-size: cover;
	background-position: 0 -50px;
	font-family: 'Lato', arial, helvetica, sans-serif;
	font-size: 1.6rem;
	font-weight: 300;
}

.wrapper {
	margin: 12em auto 2em auto;
	width:80%;
	position:relative;
}

p {
	color: white;
	text-align: center;
}

button {
	cursor: hand;
	background-color: #ff8d35;
	color: white;
	font:weight: 900;
	font-size: 1.2rem;
	border: none;
	padding:1em 3em;
	margin: 2em auto;
	display:block;
    transition:background .5s ease-in, transform .5s .25s ease-in-out;

    /*5s is the duration .25s is the delay for the transistion*/
}

button:hover {
	background: #c61140;
	transform: scale(1.2);
}
```

#### Output

![Banner Image](github-readme-contents/example-13-output.gif)

## Example 14

####  HTML Code

```html
<html>
	<head>
		<title>Transition Basics</title>		
		<link rel="stylesheet" href="styles.css" media="all" />
	</head>
	<body>

	<div class="wrapper">
		<h2></h2>
		<p>Roll into the future right now and buy your very own robot!</p>
		<button>BUY NOW</button>
	</div>

	</body>
</html>
```

####  CSS Code

```css
@import url(https://fonts.googleapis.com/css?family=Lato:400,900,300,300italic,400italic,900italic);

body {
	background-color: #f7e4fe;
	background-image: url('purple_diag_background.svg');
	background-size: cover;
	background-position: 0 -50px;
	font-family: 'Lato', arial, helvetica, sans-serif;
	font-size: 1.6rem;
	font-weight: 300;
}

.wrapper {
	margin: 12em auto 2em auto;
	width:80%;
	position:relative;
	perspective: 1000px;/*This is the important for the rotate*/
}

p {
	color: white;
	text-align: center;
}

button {
	cursor: hand;
	background-color: #ff8d35;
	color: white;
	font:weight: 900;
	font-size: 1.2rem;
	border: none;
	padding:1em 3em;
	margin: 2em auto;
	display:block;

	transition: background .6s ease-in, transform .2s ease-out;
}

button:hover {
	background: #c61140;
	transform: scale(1.2) rotateX(30deg);
}
```
#### Output

![Banner Image](github-readme-contents/example-14-output.gif)

## Example 15

####  HTML Code

```html
<!doctype html>
<html>
    <head>

        <title>Module 1 | CSS Transition Fundamentals</title>
        <meta name="description" content="CSS Transition Fundamentals | Demos">
        <link rel="stylesheet" href="style.css">
    </head>
    <body>

        <h1>CSS Transition Fundamentals | Demos</h1>

        <!-- Blue to green -->
        <section id='color'>

             <h3>Blue to green</h3>

            <div class='square'>
            </div>

        </section><hr>

        <!-- Square to circle-->
        <section id='circle'>

            <h3>Square to circle</h3>

            <div class='square'>
            </div>

        </section>
    </body>
</html>
```

####  CSS Code

```css
.square {
	width: 250px;
	height: 250px;
	margin: 1rem 0 2rem 1rem;
	background-color: blue;
}

/* Blue to green */
#color .square {
-webkit-transition-property: background-color;
-moz-transition-property: background-color;
-o-transition-property: background-color;
-ms-transition-property: background-color;
transition-property: background-color;
-webkit-transition-duration: 5s;
-moz-transition-duration: 5s;
-o-transition-duration: 5s;
-ms-transition-duration: 5s;
transition-duration: 5s;
}

#color .square:hover {
  background-color: green;
}

/* Square to circle */
#circle .square {
-webkit-transition: border-radius 2s 5s, background-color 3s 2s;
-moz-transition: border-radius 2s 5s, background-color 3s 2s;
-o-transition: border-radius 2s 5s, background-color 3s 2s;
-ms-transition: border-radius 2s 5s, background-color 3s 2s;
transition: border-radius 2s 5s, background-color 3s 2s;
}

#circle .square:hover {
  border-radius: 50%;
  background-color: purple;
}
```

#### Output

![Banner Image](github-readme-contents/example-15-output.gif)

## Example 16

####  HTML Code

```html
<!doctype html>
<html class="no-js" lang="">
    <head>
        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <title>2DTransition &amp; Transform | Demos</title>
        <meta name="description" content="This is a demonstration about CSS 2D transition">
        <link rel="stylesheet" href="style.css">
    </head>
    <body>

        <h1>2DTransition &amp; Transform | Demos</h1><br>

        <!-- The skew() method  -->
        <section id='skew'>

            <h3>The skew() method</h3>

            <p>skews an element along the X and Y-axis by the given angle.</p>


            <div class='square'>
            </div>

        <hr>
        </section>

        <!-- The scale() method -->
        <section id='scale'>

            <h3>The scale() method</h3>

            <p>increases or decreases the size of an element.</p>

            <div class='square'>

                <div></div>
            </div>

        <hr>
        </section>

        <!-- The rotate() method -->
        <section id='rotate'>

            <h3>The rotate() method</h3>

            <p>rotates an element clockwise or counter-clockwise according to a given degree.</p>

            <div class='square'>
            </div>

        <hr>
        </section>

         <!-- The translate() method  -->
        <section id='translate'>

            <h3>The translate() method</h3>

            <p>moves an element from its current position. This div element is moved 900 pixels to the right.</p>

            <div class='square'>
            </div>

        <hr>
        </section>           
    </body>
</html>
```

####  CSS Code

```css
section, h1 {
 margin: 2rem 4rem;
}
.square {
	width: 150px;
	height: 150px;
	background: blue;
  position: relative;
}


/* The skew() method */
#skew .square {
  background-color: purple;
  -webkit-transition: transform 5s;
  -moz-transition: transform 5s;
  -o-transition: transform 5s;
  -ms-transition: transform 5s;
  transition: transform 5s;
}


#skew .square:hover {
 -webkit-transform: skewX(-20deg);
 -moz-transform: skewX(-20deg);
 -o-transform: skewX(-20deg);  
 -ms-transform: skewX(-20deg);
 transform: skewX(-20deg);
}


/* The scale() method */
#scale .square div {
   background: #000;  
   position: absolute;
   left: 25%;
   top: 25%;
   width: 75px;
   height: 75px;
   -webkit-transition: transform 5s, background-color 2s 1s;
   -moz-transition: transform 5s, background-color 2s 1s;
   -o-transition: transform 5s, background-color 2s 1s;
   -ms-transition: transform 5s, background-color 2s 1s;
   transition: transform 5s, background-color 2s 1s;
}

#scale .square div:hover {
  background-color: blue;
  -webkit-transform: scale(2,2);
  -moz-transform: scale(2,2);
  -o-transform: scale(2,2);
  -ms-transform: scale(2,2);
  transform: scale(2,2);
}

/* The rotate() method */
#rotate .square {
  background-color: tomato;
  -webkit-transition: transform 5s;
  -moz-transition: transform 5s;
  -o-transition: transform 5s;
  -ms-transition: transform 5s;
  transition: transform 5s;
}

#rotate .square:hover {
 -webkit-transform: rotate(360deg);
 -moz-transform: rotate(360deg);
 -o-transform: rotate(360deg);
 -ms-transform: rotate(360deg);  
 transform: rotate(360deg);
}


/* The translate() method */
#translate .square {
  background-color: orange;
  -webkit-transition: transform 5s ease-in, background 3s 2s;
  -moz-transition: transform 5s ease-in, background 3s 2s;
  -o-transition: transform 5s ease-in, background 3s 2s;
  -ms-transition: transform 5s ease-in, background 3s 2s;
  transition: transform 5s ease-in, background 3s 2s;

}

#translate .square:hover {
 background-color: green;
 -webkit-transform: translateX(900px) rotate(360deg);
 -moz-transform: translateX(900px) rotate(360deg);
 -o-transform: translateX(900px) rotate(360deg);
 -ms-transform: translateX(900px) rotate(360deg);
 transform: translateX(900px) rotate(360deg);
}    
```

#### Output

![Banner Image](github-readme-contents/example-16-output.gif)


## Other Notes

### Alternate
![Banner Image](notes/alternative.png)

### Alternate Reverse
![Banner Image](notes/alternative-reverse.png)

### Animation Direction
![Banner Image](notes/animation-direction.png)

### Animation Fill Mode
![Banner Image](notes/animation-fill-mode.png)

### Timing Function 1
![Banner Image](notes/timing-function-1.png)

### Timing Function 2
![Banner Image](notes/timing-function-2.png)

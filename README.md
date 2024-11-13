## Ex.07 Interactive photo Gallery
## Date: 13/11/2024
## AIM:
To design an interactive photo gallery using HTML, CSS and Javascript.

## DESIGN STEPS:
## Step 1:
Create a Django Admin project.

## Step 2:
Create an app in the Django interface.

## Step 3:
Create a folder named 'static' in the app folder.

## Step 4:
Create a new HTML file in the static folder.

## Step 5:
Write the HTML code with relevant CSS properties.

## Step 6:
Choose the appropriate style and color scheme.

## Step 7:
Insert the images in their appropriate places.

## Step 8:
Publish the website in the LocalHost.

## PROGRAM:
html:
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Photo Gallery</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.css"
    integrity="sha512-oHDEc8Xed4hiW6CxD7qjbnI+B07vDdX7hEPTvn9pSZO1bcRqHp8mj9pyr+8RVC2GmtEfI2Bi9Ke9Ass0as+zpg=="
    crossorigin="anonymous" referrerpolicy="no-referrer">
  <link href="https://fonts.googleapis.com/css2?family=Anton&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="assets/css/styles.css">
  <link rel="stylesheet" href="assets/css/baguetteBox.min.css">
</head>
<body>
  <main>
    <div class="heading">
      <h1 class="title">Interactive Photo Gallery</h1>
      <div class="search-box">
        <input type="search" id="search" placeholder="Search...">
      </div>
    </div>
    <div class="gallery-container gallery" id="photos">
      <ul id="container">
        <li> <a href="photos/01.jpg"
            data-caption="I love hay bales. Took this snap on a drive through the countryside past some straw fields."
            data-alt="Hay Bales">
            <img src="photos/thumbnails/01.jpg" alt="Hay Bales." class="gallery__item">
          </a>
        </li>
        <li><a href="photos/02.jpg"
            data-caption="The lake was so calm today. We had a great view of the snow on the mountains from here."
            data-alt="Lake">
            <img src="photos/thumbnails/02.jpg" alt="Lake" class="gallery__item">
          </a>
        </li>
        <li> <a href="photos/03.jpg"
            data-caption="I hiked to the top of the mountain and got this picture of the canyon and trees below."
            data-alt="Canyon">
            <img src="photos/thumbnails/03.jpg" alt="Canyon" class="gallery__item">
          </a>
        </li>
        <li><a href="photos/04.jpg"
            data-caption="It was amazing to see an iceberg up close, it was so cold but didn’t snow today."
            data-alt="Iceberg">
            <img src="photos/thumbnails/04.jpg" alt="Iceberg" class="gallery__item">
          </a>
        </li>
        <li> <a href="photos/05.jpg"
            data-caption="The red cliffs were beautiful. It was really hot in the desert but we did a lot of walking through the canyons."
            data-alt="Desert">
            <img src="photos/thumbnails/05.jpg" alt="Desert" class="gallery__item">
          </a>
        </li>
        <li> <a href="photos/06.jpg"
            data-caption="Fall is coming, I love when the leaves on the trees start to change color." data-alt="Fall">
            <img src="photos/thumbnails/06.jpg" alt="Fall" class="gallery__item">
          </a>
        </li>
        <li><a href="photos/07.jpg" data-caption="I drove past this plantation yesterday, everything is so green!"
            data-alt="Plantation">
            <img src="photos/thumbnails/07.jpg" alt="Plantation" class="gallery__item">
          </a>
        </li>
        <li> <a href="photos/08.jpg" data-caption="My summer vacation to the Oregon Coast. I love the sandy dunes!"
            data-alt="Dunes">
            <img src="photos/thumbnails/08.jpg" alt="Dunes" class="gallery__item">
          </a>
        </li>
        <li><a href="photos/09.jpg" data-caption="We enjoyed a quiet stroll down this countryside lane."
            data-alt="Countryside Lane">
            <img src="photos/thumbnails/09.jpg" alt="Countryside Lane" class="gallery__item">
          </a>
        </li>
        <li> <a href="photos/10.jpg" data-caption="Sunset at the coast! The sky turned a lovely shade of orange."
            data-alt="Sunset">
            <img src="photos/thumbnails/10.jpg" alt="Sunset" class="gallery__item">
          </a>
        </li>
        <li> <a href="photos/11.jpg"
            data-caption="I did a tour of a cave today and the view of the landscape below was breathtaking."
            data-alt="Cave">
            <img src="photos/thumbnails/11.jpg" alt="Cave" class="gallery__item">
          </a>
        </li>
        <li> <a href="photos/12.jpg"
            data-caption="I walked through this meadow of bluebells and got a good view of the snow on the mountain before the fog came in."
            data-alt="Bluebells">
            <img src="photos/thumbnails/12.jpg" alt="Bluebells" class="gallery__item">
          </a>
        </li>
      </ul>
    </div>
    </div>
  </main>
  <script>
    window.addEventListener('load', function () {
      baguetteBox.run(".gallery", {
        captions: true,
        buttons: 'auto',
        fullScreen: false,
        noScrollbars: false,
        titleTag: true,
        async: false,
        preload: 2,
        animation: 'fadeIn',
        onChange: null
      });
    });
  </script>
  <script src="assets/js/baguetteBox.min.js" async></script>
  <!-- <script src="assets/js/searchFilter.js"></script> -->
  <script src="assets/js/app.js"></script>
</body>
</html>
```
CSS:
```
/* ==========================================================================
// Global Styling
// ========================================================================*/

* {
	box-sizing: border-box;
}

body {
	background-color: #ecf0f1;
	max-width: 100%;
	margin: auto;
}

main {
	margin: 0 auto;
	padding: 2em 0;
	max-width: 1024px;
	height: 100vh;
	text-align: center;
	align-items: center;
}

input {
	margin: 0 auto;
}

input[type="search"] {
	display: block;
	width: 40%;
	margin: 0 auto 2em;
	padding: 0.3125em;
	border: 2px solid #999;
	border-radius: 5px;
	outline: none;
}

h1 {
	font-family: "Anton", sans-serif;
	text-align: center;
	align-items: center;
	position: relative;
}

input::placeholder {
	color: #999;
}

ul {
	list-style: none;
	padding: 0;
}

#container {
	max-width: 1050px;
	display: grid;
	grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
	gap: 15px;
	padding: 10px;
}

.gallery-container {
	background-color: #fff;
	margin-right: 5px;
	padding: auto;
}

.gallery {
	display: grid;
	justify-content: center;
	grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
	grid-gap: 6px;
	padding-top: 10px;
}

.gallery__item {
	width: 100%;
	height: 100%;
	object-fit: cover;
}

.title {
	background-color: red;
	/* Create the gradient. */
	background-image: linear-gradient(45deg, #f70845, #fafa6e);
	/* Set the background size and repeat properties. */
	background-size: 100%;
	background-repeat: repeat;
	/* Use the text as a mask for the background. */
	/* This will show the gradient as a text color rather than element bg. */
	-webkit-background-clip: text;
	-webkit-text-fill-color: transparent;
	-moz-background-clip: text;
	-moz-text-fill-color: transparent;
}

#search {
	font-size: 17px;
	border: 2px solid rgb(168, 168, 168);
	border-radius: 6px;
	min-width: 30%;
	margin: auto;
	margin-bottom: 2%;
	padding: 12px 20% 12px 12px;
	color: rgb(91, 91, 91);
}

input:focus {
	outline: 2px solid orange;
}

img {
	flex-basis: 29.7%;
	grid-gap: 5px;
	opacity: 0.9;
	cursor: pointer;
	padding-bottom: 1.9rem;
}

a:hover {
	opacity: 1;
}

.gallery img {
	max-width: 100%;
	height: auto;
}

.lb-nav a.lb-prev {
	color: tomato;
}

figcaption {
	color: orangered;
	background-color: aliceblue;
}

@media (max-width: 767px) {
	.gallery {
		width: 90%;
	}

	.gallery img {
		height: 500px;
		width: 500px;
	}

	.lb-data .lb-close {
		position: fixed;
		left: 10px;
		top: 20px;
	}

	.lb-nav a.lb-next {
		position: fixed;
		right: 35px;
		top: 0;
	}

	.lb-nav a.lb-prev {
		position: fixed;
		left: 35px;
		top: 0;
	}
}
@media (max-width: 480px) {
	img {
		flex-basis: 100%;
		margin-bottom: 21px;
	}

	.lightbox-content {
		width: 90%;
		margin: 20% auto;
	}
}
```
Javascript
```
// lightbox.option({
//   'showImageNumberLabel': false,
//   'wrapAround': true,
//   'positionFromTop': 125,
//   'alwaysShowNavOnTouchDevices': true
// })

// const gallery = baguetteBox.run(".gallery");

document.querySelector("#search").addEventListener("keyup", userSearch);

function userSearch() {
   const caption = document.querySelectorAll("a[data-caption]");
   let captionsList = [];

   for (let i = 0; i < caption.length; i++) {
      let captions = caption[i].getAttribute("data-caption");
      captionsList.push(captions.toLowerCase());
      // create variable set it to user search input toLowerCase()
      let searchVar = document.querySelector("#search");
      searchVar = searchVar.value.toLowerCase();
      // create conditional statement (if) to search indexOf
      if (captionsList[i].indexOf(searchVar) > -1) {
         // set style of lstCnt to display block
         caption[i].style.display = "block";
      } else {
         // set style of lstCnt to display none
         caption[i].style.display = "none";
      }
   }
}

console.log(userSearch());
// document.getElementById('search').addEventListener('keyup', searchFilter);
// let thumbnails = document.getElementsByTagName('img');

// function searchFilter() {
//     // grabs user input as its being typed into search field and converts it to all upper case for case sensitivity
//     let userInput = document.getElementById('search').value.toUpperCase();
//     // targets all a tags with the data-caption attribute
//     let links = document.querySelectorAll('a[data-caption]');
//     // iterating through all the a tags
//     for (let i = 0; i < links.length; i++) {
//         let captions = links[i].getAttribute('data-caption');
//         //turning captions into upper case for case sensitivity
//         captions = captions.toUpperCase();
//         // check if the current value of the search input is included within any captions, if it is display the associated thumbnail, if not, hide it
//         if (captions.includes(userInput)) {
//             thumbnails[i].parentNode.style.display = '';
//         } else {
//             thumbnails[i].parentNode.style.display = 'none';
//         }
//     }
// }
```

## OUTPUT:
![Screenshot 2024-11-13 092615](https://github.com/user-attachments/assets/fb078cd3-d4ea-45cb-b18c-477d37204b40)
![Screenshot 2024-11-13 092620](https://github.com/user-attachments/assets/8fa39a3e-3c27-48dd-a228-416f3fded589)


## RESULT:
The program for designing an interactive photo gallery using HTML, CSS and Javascript is completed successfully.

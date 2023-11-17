<script>
//import

   export default {
    data() {
      return{
        //dati
		musicOn : false,
		description : false,

      }
    },
    methods: {
        //function
		getImagePath: function(image){
            return new URL (image, import.meta.url).href;
        },

		getMusicOn(){
			this.musicOn = true;
		},

		getDescription(){
			this.description = true;
			console.log(this.description )
		}

    },
    components: {
        //dichiarazione
    },
	computed: {
		stars(){
			if(this.softSkills.vote === 5){
				return this.softSkills.icon
			}
		}
	},
    props:{
        //utilizzo per file padre
    }
    
    
  }
</script>


<template>

    <main>
		
		<!-- sezione progetti/dev skills -->
		<section  id="skills" class="skills-section">

			<div class="dev-skill">

				<h3 class="text-center">
					Developer Skills
				</h3>

				<h4 class="text-center mt-4">
					FrontEnd
				</h4>
				
				<!-- ------------- -->

				<div class="container">
					
					<!-- boolando -->
					<div class="row align-items-center justify-content-center mt-5">
						<div class="col-4 col-text order-1 order-sm-1">
							<div class="d-flex">
								<div class="dev-skill-box html">
									<img src="../assets/img/HTML5_logo_svg.png" alt="">
								</div>
								<div class="dev-skill-box css">
									<img src="../assets/img/css_logo.png" alt="">
								</div>
							</div>
							<div class="project-text">
								<h3 class="text-center text-md-start">
									Boolando
								</h3>
								<!-- <span @click="getDescription()" class="d-md-none">
									clicca
								</span> -->
								<div>
									<p>
										Boolando is the reproduction of the original website Zalando. The technologies used are <span class="main-color">HTML</span> and <span class="main-color">CSS</span> with added animation in some elements of the page. A simple and accurate e-commerce, ready to sell new products!
									</p>
								</div>
								
								<div class="button-container">
									<a href="https://michela30.github.io/Boolando/" class="btn-show" target="_blank">
										Show
									</a>
								</div>
							</div>
						</div>
						
						<div class="col-8 col-video order-2 order-sm-2">
							<div class="video-box">
								<video muted autoplay loop>
									<source class="video-filter" src="../assets/video/boolando-video.mp4" type="">
								</video>
							</div>
						</div>
					</div>

					<!-- spotify -->
					<div class="row align-items-center justify-content-center mt-5">
						
						<div class="col-8 col-video order-2 order-sm-2 order-md-1">
							<div class="video-box">
								<video muted autoplay loop>
									<source class="video-filter" src="../assets/video/spotify-video.mp4" type="">
								</video>
							</div>
						</div>
						<div class="col-4 col-text order-1 order-sm-1 order-md-2 ps-md-5">
							<div class="d-flex">
								<div class="dev-skill-box html">
									<img src="../assets/img/HTML5_logo_svg.png" alt="">
								</div>
								<div class="dev-skill-box css">
									<img src="../assets/img/css_logo.png" alt="">
								</div>
							</div>
							<div class="project-text">
								<h3 class="text-center text-md-start">
									Spotify
								</h3>
								<p>
									Spotify is the reproduction of the Spotify web application for <span class="text-decoration-underline">
										Desktop</span>. The Frontend technologies used are <span class="main-color">HTML</span> and <span class="main-color">CSS</span>. Ready to make everyone dance!
								</p>
								<div class="button-container">
									<a href="https://michela30.github.io/Spotifyweb/" class="btn-show" target="_blank">
										Show
									</a>
								</div>
							</div>
						</div>
					</div>

					<!-- form treno-->
					<div class="row align-items-center justify-content-center mt-5">
						<div class="col-4 col-text">
							<div class="d-flex">
								<div class="dev-skill-box">
									<img src="../assets/img/HTML5_logo_svg.png" alt="">
								</div>
								<div class="dev-skill-box">
									<img src="../assets/img/css_logo.png" alt="">
								</div>
								<div class="dev-skill-box html">
									<img src="../assets/img/JavaScript-Logo.png" alt="">
								</div>
								<div class="dev-skill-box css">
									<img src="../assets/img/bootstrap_logo.png" alt="">
								</div>
							</div>
							<div class="project-text">
								<h3 class="text-center text-md-start">
									Ticket Train
								</h3>
								<p>
									Do you want to leave? Here is a small web application made with HTML and CSS, and especially <span class="main-color">JAVASCRIPT</span> for logic and the <span class="main-color"> BOOTSTRAP </span>framework for some graphic elements, which allows you to enter your data, the km to be made, your age (with possibility of discount) and calculate the ticket price!
								</p>
								<div class="button-container">
									<a href="https://michela30.github.io/Biglietto-del-treno-generator/" class="btn-show" target="_blank">
										Show
									</a>
								</div>
							</div>
						</div>
						<div class="col-8 col-video">
							<div class="video-box">
								<video muted autoplay loop>
									<source class="video-filter" src="../assets/video/FormJsTreno.mp4" type="">
								</video>
							</div>
						</div>

					</div>
					
					<!-- boolzapp -->
					<div class="row align-items-center justify-content-center mt-5">
						<div class="col-8 col-video order-2 order-sm-2 order-md-1">
							<div class="video-box">
								<video muted autoplay loop>
									<source class="video-filter" src="../assets/video/boolzapp-video.mp4" type="">
								</video>
							</div>
						</div>
						<div class="col-4 col-text order-1 order-sm-1 order-md-2 ps-md-5">
							<div class="d-flex">
								<div class="dev-skill-box">
									<img src="../assets/img/HTML5_logo_svg.png" alt="">
								</div>
								<div class="dev-skill-box">
									<img src="../assets/img/css_logo.png" alt="">
								</div>
								<div class="dev-skill-box">
									<img src="../assets/img/bootstrap_logo.png" alt="">
								</div>
								<div class="dev-skill-box html">
									<img src="../assets/img/Vue.js_Logo.svg.png" alt="">
								</div>
							</div>
							<div class="project-text">
								<h3 class="text-center text-md-start">
									Boolzapp
								</h3>
								<p>
									Inspired by the web application Whatsapp for <span class="text-decoration-underline">
										Desktop</span>, here is Boolzapp! Created with HTML, for the frontend CSS and BOOTSTRAP, and to make the app dynamic the framework javascript: <span class="main-color">VUEJS </span>. Now you can chat with your friends!

								</p>
								<div class="button-container">
									<a href="https://michela30.github.io/Boolzapp/" class="btn-show" target="_blank">
										Show
									</a>
								</div>
							</div>
						</div>
					</div>

					<!-- dc comics -->
					<div class="row align-items-center justify-content-center mt-5">
						<div class="col-4 col-text">
							<div class="d-flex">
								<div class="dev-skill-box">
									<img src="../assets/img/HTML5_logo_svg.png" alt="">
								</div>
								<div class="dev-skill-box css">
									<img src="../assets/img/sass_logo.png" alt="">
								</div>
								<div class="dev-skill-box html">
									<img src="../assets/img/Vue.js_Logo.svg.png" alt="">
								</div>
								<div class="dev-skill-box css">
									<img src="../assets/img/vite_logo.png" alt="">
								</div>
								<div class="dev-skill-box html">
									<img src="../assets/img/nodejs-logo.png" alt="">
								</div>
							</div>
							<div class="project-text">
								<h3 class="text-center text-md-start">
									Dc Comics
								</h3>
								<p>
									A site entirely dedicated to Dc Comics! You can find your comic book library, made with HTML, <span class="main-color">SCSS</span>, and frameworks <span class="main-color">VUEJS</span>, <span class="main-color">VITE</span> and <span class="main-color">NODE.JS</span>. <br>
									Do you want to buy one?
								</p>
								<div class="button-container">
									<a href="https://michela30.github.io/Dc-comics/" class="btn-show" target="_blank">
										Show
									</a>
								</div>
							</div>
						</div>
						<div class="col-8 col-video">
							<div class="video-box">
								<video muted autoplay loop>
									<source class="video-filter" src="../assets/video/dc-comic-video.mp4" type="">
								</video>
							</div>
						</div>
					</div>

					<!-- boolflix -->
					<div class="row align-items-center justify-content-center mt-5">
						<div class="col-8 col-video order-2 order-sm-2 order-md-1">
							<div class="video-box">
								<video muted autoplay loop>
									<source class="video-filter" src="../assets/video/Boolflix.mp4" type="">
								</video>
							</div>
						</div>
						<div class="col-4 col-text order-1 order-sm-1 order-md-2 ps-md-5">
							<div class="d-flex">
								<div class="dev-skill-box">
									<img src="../assets/img/HTML5_logo_svg.png" alt="">
								</div>
								<div class="dev-skill-box">
									<img src="../assets/img/sass_logo.png" alt="">
								</div>
								<div class="dev-skill-box html">
									<img src="../assets/img/Vue.js_Logo.svg.png" alt="">
								</div>
								<div class="dev-skill-box css">
									<img src="../assets/img/vite_logo.png" alt="">
								</div>
								<div class="dev-skill-box html">
									<img src="../assets/img/nodejs-logo.png" alt="">
								</div>
								<div class="dev-skill-box css">
									<img src="../assets/img/axios-logo.png" alt="">
								</div>
							</div>
							<div class="project-text">
								<h3 class="text-center text-md-start">
									Boolflix
								</h3>
								<p>
									Reproduction of the famous Netflix site, made with HTML and SCSS technologies, through the frameworks <span class="main-color">VUEJS</span>, <span class="main-color">VITE</span> and <span class="main-color">NODE.JS</span>, and finally a call API through the <span class="main-color">AXIOS</span> library allowed the printing of all the movies. Now you just have to choose which one to watch!
								</p>
								<div class="button-container">
									<a href="https://michela30.github.io/Boolflix/" class="btn-show" target="_blank">
										Show
									</a>
								</div>
							</div>
						</div>
					</div>

					<!-- Frontend Project -->
					<div class="row align-items-center justify-content-center mt-5">
						<div class="col-4 col-text">
							<div class="d-flex">
								<div class="dev-skill-box">
									<img src="../assets/img/HTML5_logo_svg.png" alt="">
								</div>
								<div class="dev-skill-box">
									<img src="../assets/img/sass_logo.png" alt="">
								</div>
								<div class="dev-skill-box">
									<img src="../assets/img/Vue.js_Logo.svg.png" alt="">
								</div>
								<div class="dev-skill-box html">
									<img src="../assets/img/vite_logo.png" alt="">
								</div>
								<div class="dev-skill-box css">
									<img src="../assets/img/nodejs-logo.png" alt="">
								</div>
							</div>
							<div class="project-text">
								<h3 class="text-center text-md-start">
									Frontend Project
								</h3>
								<p>
									Here is a mockup of a website that deals with courses of study. Made entirely with frontend technologies: HTML, SCSS, VUEJS, <span class="main-color">VITE</span> and <span class="main-color">NODE.JS</span>. 
								</p>
								<div class="button-container">
									<a href="https://michela30.github.io/Progetto-frontend/" class="btn-show" target="_blank">
										Show
									</a>
								</div>
							</div>
						</div>
						<div class="col-8 col-video">
							<div class="video-box">
								<video muted autoplay loop>
									<source class="video-filter" src="../assets/video/Progetto-Frontend.mp4" type="">
								</video>
							</div>
						</div>
					</div>
					
					<!-- Hires Company -->
					<div class="row align-items-center justify-content-center mt-5">
						<div class="col-8 col-video order-2 order-sm-2 order-md-1">
							<div class="video-box">
								<video muted autoplay loop>
									<source class="video-filter" src="../assets/video/hires-video.mp4" type="">
								</video>
							</div>
						</div>
						<div class="col-4 col-text order-1 order-sm-1 order-md-2 ps-md-5">
							<div class="d-flex">
								<div class="dev-skill-box html">
									<img src="../assets/img/HTML5_logo_svg.png" alt="">
								</div>
								<div class="dev-skill-box css">
									<img src="../assets/img/css_logo.png" alt="">
								</div>
							</div>
							<div class="project-text">
								<h3 class="text-center text-md-start">
									Hires Company
								</h3>
								<p>
									My first online website after the Boolean course, made with <span class="main-color">HTML</span> and <span class="main-color">CSS</span> technologies.
								</p>
								<div class="button-container">
									<a href="https://hires-company.com/" class="btn-show" target="_blank">
										Show
									</a>
								</div>
							</div>
						</div>
					</div>

				</div>

				<!-- ------------- -->

				<h4 class="text-center backend-skill">
					Backend
				</h4>

				<div class="container">
					<!-- besport -->
					<div class="row align-items-center justify-content-center mt-5">
						<div class="col-4 col-text order-1 order-sm-1">
							<div class="d-flex">
								<div class="dev-skill-box me-3 html">
								<img src="../assets/img/php_logo.png" alt="">
								</div>
								<div class="dev-skill-box me-3 html">
									<img src="../assets/img/phpmyadmin-icon-.png" alt="">
								</div>
								<div class="dev-skill-box me-3 html">
									<img src="../assets/img/laravel.png" alt="">
								</div>
								<div class="dev-skill-box me-3 html">
									<img src="../assets/img/sql_logo.png" alt="">
								</div>
								<div class="dev-skill-box me-3 html">
									<img src="../assets/img/mysql-logo.png" alt="">
								</div>
							</div>

							<div class="project-text">
								<h3 class="text-center text-md-start">
									BeSport
								</h3>
								<div>
									<p>
										During the final project of Boolean course in team was born BeSport. I created the Dashboard in blade,  with the help of  SCSS, and I edited the Database with the Migration, Crud and API of <span class="main-color">LARAVEL</span>.
										Braintree and chart.js libraries were used for the payment method and graphs.
									</p>
								</div>
								
								<!-- <div class="button-container">
									<a href="https://michela30.github.io/Boolando/" class="btn-show" target="_blank">
										Show
									</a>
								</div> -->
							</div>
						</div>
						
						<div class="col-8 col-video order-2 order-sm-2">
							<div class="video-box">
								<video muted autoplay loop>
									<source class="video-filter" src="../assets/video/BeSport-video.mp4" type="">
								</video>
							</div>
						</div>
					</div>
				</div>

				<h4 class="text-center backend-skill">
					Tools
				</h4>

				<div class="row justify-content-between">
					<div class="back-skill-box">

						<div class="dev-skill-box me-3 html">
							<img src="../assets/img/git.png" alt="">
						</div>
						<div class="dev-skill-box me-3 html">
							<img src="../assets/img/GitHub.png" alt="">
						</div>
						<div class="dev-skill-box me-3 html">
							<img src="../assets/img/mamp-icon.png" alt="">
						</div>

					</div>
				</div>
			</div>
 
		</section>

		

    </main>

</template>




<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;


.frontend{
	width: 200px;
	height: 300px;
	border: 1px solid white;
	background-color: #FCC9FC;
}
.backend{
	width: 200px;
	height: 300px;
	border: 1px solid white;
	background-color: yellow;
}
.dev-skill{
	padding: 30px 0;
	h3{
		margin-bottom: 20px;
	}


	.row{
		margin: 10px;
		.dev-skill-box{
			margin-top: 15px;
			width: calc((100% / 4) - 20px);
			height: 80px;
			padding: 20px;
			border-radius: 50%;
			display: flex;
			justify-content: center;

			img{
				height: 100%;
			}
		}
	}

	.backend-skill{
		margin-top: 80px;
	}
	.back-skill-box{
		margin-top: 15px;
		width: calc((100% / 5) - 20px);
		height: 120px;
		padding: 20px;
		border-radius: 50%;
		display: flex;
		justify-content: center;
	}
}

@keyframes zoominoutsinglefeatured {
    0% {
        transform: scale(1,1);
    }
    50% {
        transform: scale(1.2,1.2);
    }
    100% {
        transform: scale(1,1);
    }
}

.html img {
    animation: zoominoutsinglefeatured 1s ease-in-out 5s 9;
}
.css img {
    animation: zoominoutsinglefeatured 1s ease-in-out 6.5s 8;
}


.video-box{
	width: 600px;
	height: 275px;

	video{
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
}

#frontend-video{
	width: 600px;
	height: 260px;

	video{
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
}

.image-box{
	width: 600px;
	height: 275px;

	img{
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
}
@media screen and (min-width: 280px){
	.col-video{
		width: 100%;
		.video-box{
			width: 100%;

			video{
				width: 100%;
				height: 100%;
				object-fit: cover;
			}
		}
	}
	.col-text{
		width: 100%;
	}
	.button-container{
	display: flex;
	justify-content: center;
	margin-bottom: 20px;
		.btn-show{
			background-color: #F10081;
			padding: 5px 10px;
			color: white;
			text-decoration: none;
			border-radius: 15px;
			border: 1px solid transparent;
		}
}
}

@media screen and (min-width: 375px){
	.col-video{
		width: 100%;
		.video-box{
			width: 100%;

			video{
				width: 100%;
				height: 100%;
				object-fit: cover;
			}
		}
	}
	.col-text{
		width: 100%;
	}
	.button-container{
	display: flex;
	justify-content: center;
	margin-bottom: 20px;
		.btn-show{
			background-color: #F10081;
			padding: 5px 10px;
			color: white;
			text-decoration: none;
			border-radius: 15px;
			border: 1px solid transparent;
		}
}
}

@media screen and (min-width: 425px){
	.col-video{
		width: 100%;
		.video-box{
			width: 100%;

			video{
				width: 100%;
				height: 100%;
				object-fit: cover;
			}
		}
	}
	.col-text{
		width: 100%;
	}
	.button-container{
	display: flex;
	justify-content: center;
	margin-bottom: 20px;
		.btn-show{
			background-color: #F10081;
			padding: 5px 10px;
			color: white;
			text-decoration: none;
			border-radius: 15px;
			border: 1px solid transparent;
		}
}
}


@media screen and (min-width: 576px){

}

/* Tablet */

@media screen and (min-width: 768px){

	
	.col-video{
		width: 60%;
		.video-box{
			width: 450px;
			height: 275px;

			video{
				width: 100%;
				height: 100%;
				object-fit: cover;
			}
		}
	}
	.col-text{
		width: calc(40% - 80px);
	}

	.button-container{
		display: block;
		.btn-show{
			background-color: #F10081;
			padding: 0px 10px;
			color: white;
			text-decoration: none;
			border-radius: 15px;
			border: 1px solid transparent;
		}
	}
	
.dev-skill{
	.row{
		
		.dev-skill-box{
			width: calc((100% / 5) - 20px);
		}
	}
}

.best-projects{
	padding: 20px 0;
	.project-box{
		width: calc((100% / 2) - 20px);
	}
}
}


/* Desktop */
@media screen and (min-width: 992px){
.dev-skill{
	.row{
		.dev-skill-box{
			width: calc((100% / 7) - 20px);
		}
	}
}

.col-video{
		width: 60%;
		.video-box{
			width: 600px;
			height: 275px;

			video{
				width: 100%;
				height: 100%;
				object-fit: cover;
			}
		}
	}
	.col-text{
		width: calc(40% - 50px);
	}

}


@media screen and (min-width: 1200px){
	.col-text{
		width: calc(40%);
	}
}
</style>
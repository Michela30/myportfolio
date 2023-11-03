<script>
//import

   export default {
    data() {
      return{
        //dati
		linkMenu: [
			{
				title: 'SKILLS',
				link: '#skills'
			},
			{
				title: 'ABOUT ME',
				link: '#about'
			},
			{
				title: 'RESUME',
				link: '#cv'
			},
			{
				title: 'CONTACTS',
				link: '#contact'
			},
		],
		isVisible : false,
      }
    },
    methods: {
        //function
		presentation(){
			this.isVisible = true;
		}


    },
    components: {
        //dichiarazione
    },
    props:{
        //utilizzo per file padre
    }
    
    
  }
</script>


<template>
    
    <header>

		<video muted autoplay loop class="videowheel">
			<source class="video-filter" src="../assets/img/intro.mp4" type="">
		</video>
	 
      	<nav class="header-top">
			<ul>
				<li v-for="(singleLink, i) in linkMenu" :key="i">
					<a :href="singleLink.link">
						{{singleLink.title}}
					</a>
				</li>
			</ul>
      	</nav>

	  	<div>
				<div class="presentation">
					<h5>
						Hi there! My name is
					</h5>
					<h1>
						Michela De Stefano
					</h1>
					<h4>
						A Jr Full Stack Web Developer from Rome.
					</h4>
					<h6>
						Take a look at the portfolio to find out more
					</h6>
				</div>
		</div>
    </header>

</template>



<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

header{
	height: 480px;
	position: relative;
}

.videowheel{
	height: 500px;
	width: 100%;
	z-index: -100;
	position: absolute;
	object-fit: cover;
	filter: grayscale(100%);

}

.header-top{
	height: 100px;
	padding-top: 50px;
	background-color: transparent;
	z-index: 2;
	display: flex;
	flex-wrap: wrap;
	justify-content: center;
	align-items: center;

		ul{
			display: flex;
			flex-wrap: wrap;

		li{
			list-style-type: none;
			padding-right: 20px;
			padding-bottom: 30px;
			
			a{
				background-color: #F10081;
				padding: 10px 15px;
				color: white;
				text-decoration: none;
				border-radius: 15px;
				border: 1px solid transparent;
			}

			a:hover{
				background-color: #8DAAA6;
				border: 1px solid #DBDDDF;
			}
		}
	
	}
}

.circle{
	height: 150px;
	width: 150px;
	border-radius: 50%;
	background-color: #F10081;
	animation-name: circle;
	animation-duration: 2s;
	animation-timing-function: ease-in-out;
	display: block;
	position: absolute;
	left: 200px;
}

.circle2{
	height: 150px;
	width: 150px;
	border-radius: 50%;
	background-color: #8DAAA6;
	animation-name: circle2;
	animation-duration: 2s;
	animation-timing-function: ease-in-out;
	display: block;
	position: absolute;
	top: 250px;
	left: 350px;
}
@keyframes circle {
	0% {
		transform: translateX(-700px);
	}
	
	100% {
		transform: translateX(150px);
	}
}
@keyframes circle2 {
	0% {
		transform: translateX(-700px);
	}
	
	100% {
		transform: translateX(300px);
	}
}

.presentation{
	position: absolute;
	left: 40px;
	bottom: 30px;
	width: 50%;
	color: white;
	text-shadow: #8DAAA6 1px 0 10px;
}


/* Tablet */

@media screen and (min-width: 768px){
	
}


/* Desktop */
@media screen and (min-width: 992px){
    
}
</style>
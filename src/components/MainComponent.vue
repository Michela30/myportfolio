<script>
//import
import SkillsSection from './SkillsSection.vue';

   export default {
    data() {
      return{
        //dati
		musicOn : false,

		softSkills: [
			{
				titolo: 'Communication',
				icon: 'fa-solid fa-star',
				vote: 'height: 10px; margin-left: 0; border-radius: 5px; background-color: #FCC9FC; width: 93%;'
			},
			{
				titolo: 'Time Management',
				icon: 'fa-solid fa-star',
				vote: 'height: 10px; margin-left: 0; border-radius: 15px; background-color: #FCC9FC; width: 120%;'
			},
			{
				titolo: 'Adaptability',
				icon: 'fa-solid fa-star',
				vote: 'height: 10px; margin-left: 0; border-radius: 15px; background-color: #FCC9FC; width: 100%;'
			},
			{
				titolo: 'Problem Solving',
				icon: 'fa-solid fa-star',
				vote: 'height: 10px; margin-left: 0; border-radius: 15px; background-color: #FCC9FC; width: 100%;'
			},
			{
				titolo: 'Teamwork',
				icon: 'fa-solid fa-star',
				vote: 'height: 10px; margin-left: 0; border-radius: 15px; background-color: #FCC9FC; width: 100%;'
			},
			{
				titolo: 'Creativity',
				icon: 'fa-solid fa-star',
				vote: 'height: 10px; margin-left: 0; border-radius: 15px; background-color: #FCC9FC; width: 140%;'
			},
			{
				titolo: 'Work Ethic',
				icon: 'fa-solid fa-star',
				vote: 'height: 10px; margin-left: 0; border-radius: 15px; background-color: #FCC9FC; width: 100%;'
			},
			{
				titolo: 'Open-minded',
				icon: 'fa-solid fa-star',
				vote: 'height: 10px; margin-left: 0; border-radius: 15px; background-color: #FCC9FC; width: 95%;'
			}

		]
      }
    },
    methods: {
        //function
		getImagePath: function(image){
            return new URL (image, import.meta.url).href;
        },

		getMusicOn(){
			this.musicOn = true;
		}

    },
    components: {
        //dichiarazione
		SkillsSection
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
        <section class="quote-box">
			<div class="quote">
				<i class="fa-solid fa-quote-left"></i>
				Exploring a curiosity or a real passion and being motivated by a desire to solve something, that's really the best way.
				<i class="fa-solid fa-quote-right"></i>
			</div>
			<small>
				Reshma Saujani
			</small>
		</section>

		<SkillsSection></SkillsSection>

		<section class="quote-box">
			<div class="quote">
				<i class="fa-solid fa-quote-left"></i>
				Coding is the language of the future. Coding is fun, collaborative and creative.
				<i class="fa-solid fa-quote-right"></i>
			</div>
			<small>
				Reshma Saujani
			</small>
		</section>

		<section id="about" class="resume-section">
			<h3 class="mb-3">
				About Me
			</h3>
			<div class="row">
				<!-- descrizione -->
				<div class="section-skills">
					<h6 class="px-4 description">
						My name is Michela De Stefano,
						I am 25 years old and I was born in Rome.
						After my artistic degree, I started my path in dance.
						This experience has been important for Discipline, Sacrifice and
						Determination.
						That’s why I commissioned a dance website, that introduced me to the world of Web Programming. 
						I'm the perfect Web Dev Jr. candidate because I aspire to improve and learn new things every day.
						I am ready to the creativity of the frontend and the logic of the backend!
						<br>
						I am a dreamer,
						<span class="text-decoration-underline main-color music" @click="getMusicOn()">Music</span> is the soundtrack of my life
						<i class="fa-solid fa-music"></i>  
					</h6>
					<div v-if="musicOn === true">
						<iframe style="border-radius:12px" src="https://open.spotify.com/embed/playlist/4YFcYGIRDchpBu2bM5FRWs?utm_source=generator" width="60%" height="152" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy" class="mb-3 mb-md-0"></iframe>
					</div>
				</div>
				<!-- foto -->
				<div class="section-skills">
					<div class="photo-box">
						<img src="../assets/img/Michela-jumbotron-piccolo.png" alt="">
					</div>

					<div id="cv" class="scarica_cv">
						<a href="https://michela30.github.io/public/Michela-De-Stefano-CV.pdf" download="">
							<button class="mb-5">
								Download CV
							</button>
						</a>
					</div>
				</div>
				<!-- soft skill -->
				<div class="section-skills">
					<h6>
						Soft skills
					</h6>
					<div class="soft-skills">
						<ul>
							<li v-for="softSkill in softSkills">
								{{ softSkill.titolo }}
								<span class="skill-container">
									<div :style="softSkill.vote" class="bar-line">
										<i :class="softSkill.icon" class="star"></i>
									</div>
								</span>
							</li>
						</ul>
					</div>
				</div>
			</div>
		</section>


    </main>

</template>




<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

.quote-box{
	background-color: #FCC9FC;
	padding: 30px 10px;
	text-align: center;
	
	.quote{
		width: 60%;
		font-size: 1.5em;
		font-style: italic;
		i{
			color: #E2205C;
			vertical-align: top;
		}
	}

	small{
		font-size: 0.8em;
	}

}

.soft-skill{
	padding: 20px 0;
	.soft-skill-row{
		display: flex;
		flex-direction: column;
		align-items: center;

		.soft-skill-box{
			width: 50%;
			margin-bottom: 10px;
			height: 30px;
			border-radius: 20px;
			background-color: #8DAAA6;
			color: black;
			text-align: center;
		}
	}

}

.resume-section{
	padding: 40px 0;
	height: 350px;
	background-color: white;
	text-align: center;

	.section-skills{
		.music{
			cursor: pointer;
		}
	}
	.section-skills{
		.soft-skills{
			margin-top: 20px;
			width: 100%;

			ul{
				list-style-type: none;
				padding-left: 0;
				
				li{
					width: 300px;
					font-family: 'Handwriting', sans-serif;
					text-align: left;
					display: flex;
					align-items: center;
					
					.skill-container{
						width: 150px;
						height: 15px;
						background-color: #8DAAA6;
						border-radius: 15px;
						border: 1px solid black;
						.bar-line{
							position: relative;
							animation: progress 1500ms ease-in 1;

							.star{
								font-size: 1.5em;
								position: absolute;
								right: -7px;
								bottom: -4px;
								color:#E2205C;
								z-index: 5;
							}
						}
					}
				}
			}                                       
		}
	}

	.section-skills{
		.photo-box{
			height: 250px;
			width: 250px;
			margin-bottom: 50px;

			img{
				border-radius: 50%;
				margin-top: 10px;
				width: 100%;
				height: 100%;
				object-fit: contain;
			}
		}
	}

}
.scarica_cv{
	text-align: center;
	padding-top: 20px;
	a{
		button{
			background-color: #F10081;
			padding: 10px 15px;
			color: white;
			text-decoration: none;
			border-radius: 15px;
			border: 1px solid transparent;
		}
	}
}

/* Animation */
@keyframes progress {
	from {
		width: 0;
	}
}

@media screen and (min-width: 280px){

.resume-section{
	padding: 40px 10px;
.section-skills{
		width: 100%;

		.description{
			padding: 5px 80px;
		}
	}
}
}


@media screen and (min-width: 375px){

.resume-section{
.section-skills{
		width: 100%;

		.description{
			padding: 5px 80px;
		}
	}
}
}

@media screen and (min-width: 425px){

	.resume-section{
	.section-skills{
			width: 100%;

			.description{
				padding: 5px 80px;
			}
		}
	}
}


@media screen and (min-width: 576px){
	.resume-section{
	.section-skills{
			width: 100%;
		}
	}
}


/* Tablet */

@media screen and (min-width: 768px){

	.quote-box{
		.quote{
			width: 70%;
		}
	}
	.resume-section{
	.section-skills{
			width: 100%;
		}
}

}




/* Desktop */
@media screen and (min-width: 992px){

	.resume-section{
		.section-skills{
				width: calc(100% / 3);
			}
	}
}
</style>
<script>
//import

   export default {
    data() {
      return{
        //dati
      }
    },
    methods: {
        //function
        getImagePath: function(image){
            return new URL (image, import.meta.url).href;
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
    <footer>

		<div class="contacts" id="contact">
			<h2 class="text-center py-3">
				Contacts
			</h2>
			<div class="d-flex justify-content-center text-center">
				<p>
					Michela De Stefano
					<br>
					Phone Number: <strong> 3484266535 </strong>
					<br>
					Email: <a class="text-decoration-none text-dark" href="mailto:micheladestefano30@gmail.com"><strong>
						micheladestefano30@gmail.com
						</strong></a>
					<br>
					<br>
					<i class="fa-brands fa-linkedin"></i>
					<a class="main-color" href="https://www.linkedin.com/in/michela-de-stefano/"  target="_blank">
						Linkedin Link
					</a>
					<br>
					<i class="fa-brands fa-github"></i>
					<a class="main-color" href="https://github.com/Michela30"  target="_blank">
						GitHub Link
					</a>
				</p>
			</div>
		</div>
		
    </footer>

</template>



<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

@media (min-with: 375px){

	footer{
	margin-top: 800px;
	height: 200px;
	.contacts{
		background-color: #f0cdf0;
		padding-top: 40px;
		padding-bottom: 60px;
	}
}
}

@media screen and (min-width: 425px){

	footer{
	margin-top: 800px;
	height: 200px;
	.contacts{
		background-color: #f0cdf0;
		padding-top: 40px;
		padding-bottom: 60px;
	}
}
}


@media screen and (min-width: 576px){

}


/* Tablet */

@media screen and (min-width: 768px){

}




/* Desktop */
@media screen and (min-width: 992px){

	footer{
	margin-top: 250px;
	height: 200px;
	.contacts{
		background-color: #f0cdf0;
		padding-top: 40px;
		padding-bottom: 60px;
	}
	}

}
</style>
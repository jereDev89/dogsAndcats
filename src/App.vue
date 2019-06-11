<template>
<div id="app">
	<div id="container">
		<!-- navigacija -->
		<div class="navigation">
			<div>
				<img src="./assets/images/aquarium.png" alt="Aquarium with fish" class="navi_icon"/>
			</div>
			<div>
			<ol>
				<a href="index.html#pets"><li>Daily pet facts</li></a>
				<a href="index.html#gallery"><li>Gallery</li></a>
				<a href="index.html#contact"><li>Contacts</li></a>
			</ol>
			</div>
		</div>
		<!-- velika slika ispod navigacije -->
		<div class="header">
			<img src="./assets/images/headline_image.png" alt="Nice and lazy cat">
		</div>

		<div class="content">
			<div class="big_margin_tb">
				<h1 id="pets">Daily pet facts - Love!</h1>
			</div>

			<div class="content_section">
				<div class="section_image" 
						data-aos="fade-right" 
						data-aos-delay="300"
						data-aos-duration="1000"
						data-aos-easing="ease-in-out"
						data-aos-once="true"
						data-aos-anchor-placement="bottom-bottom">
					<img src="./assets/images/meow.png" alt="Cat">
				</div>
				<div class="section_text section_margin_left"
						data-aos="fade-left" 
						data-aos-delay="300"
						data-aos-duration="1000"
						data-aos-easing="ease-in-out"
						data-aos-once="true"
						data-aos-anchor-placement="bottom-bottom">
					<h2 class="medium_margin_b">The Cat</h2>
					<p class="medium_margin_b">
						Cats have been domesticated for around 4,000 years. While they were once valued for their hunting abilities, they are now valued for their companionship and loving behaviour.
					</p>
					<p class="medium_margin_b">
						While not well known, the collective nouns used for cats and kittens are a clowder of cats and a kindle of kittens.
					</p>
					<p class="medium_margin_b">
						Our domestic cats are known as little cats. They differ from large cats such as lions and tigers because they are naturally active at night and can purr.
					</p>
					<p>
						Cats are now the most popular pet in the UK and in the US.
					</p>
				</div>
			</div>

			<div class="content_section section_reverse">
				<div class="section_image" 
						data-aos="fade-left" 
						data-aos-delay="300"
						data-aos-duration="1000"
						data-aos-easing="ease-in-out"
						data-aos-once="true"
						data-aos-anchor-placement="bottom-bottom">
					<img src="./assets/images/woof.png" alt="Dog">
				</div>
				<div class="section_text section_margin_right"
						data-aos="fade-right" 
						data-aos-delay="300"
						data-aos-duration="1000"
						data-aos-easing="ease-in-out"
						data-aos-once="true"
						data-aos-anchor-placement="bottom-bottom">
					<h2 class="medium_margin_b">The Dog</h2>
					<p class="medium_margin_b">
						Domestic dogs have been companions to people for more than 15,000 years. There are more than 400 different breeds of dogs. PAWS or your local animal shelter has a wide variety of breeds available for adoption. The most popular types are the non-pedigree. They are extra special because they are one-of-a-kind!
					</p>
					<p>
						In general, small dogs live longer than large dogs. Small dogs such as terriers may live 20 years. Giant dogs like Great Danes may live eight years. The average lifespan for a mixed breed dog is 13 to 14 years. By making sure dogs have good food, regular veterinary care, shelter and a loving family, they will live longer, healthier lives.
					</p>
				</div>
			</div>
      	</div>

		<div class="gallery">
			<div class="medium_margin_tb"> 
				<h1 id="gallery">Gallery</h1>
			</div>
			<div class="big_gallery">
				<div>
					<img src="./assets/images/animal_3.png" alt="Hotdog">
				</div>
				<div class="div_show_text"
						@mouseover="hover = true"
						@mouseleave="hover = false">
					<img src="./assets/images/animal_2.png" alt="Dog">
					<div class="show_text" v-if="hover">
						<h2>Border Collie</h2>
						<p>The Border Collie is a working and herding dog breed developed in the Scottish borders for herding livestock, especially sheep. It was specifically bred for intelligence and obedience.</p>
					</div>
				</div>
				<div>
					<img src="./assets/images/animal_1.jpg" alt="Dog">
				</div>
			</div>
			<div class="gallery_navigation">
				<img src="./assets/images/arrow_left.png" alt="Strelica lijevo">
				<img src="./assets/images/arrow_right.png" alt="Strelica desno">
			</div>
			<div class="mini_gallery">            	
				<img src="./assets/images/gallery/img_1.png" alt="Cat" class="img_mini_gallery hvr-grow">
				<img src="./assets/images/gallery/img_2.png" alt="Cat" class="img_mini_gallery hvr-grow">
				<img src="./assets/images/gallery/img_3.png" alt="Cat" class="img_mini_gallery hvr-grow">
				<img src="./assets/images/gallery/img_4.png" alt="Cat" class="img_mini_gallery hvr-grow">
				<img src="./assets/images/gallery/img_5.png" alt="Cat" class="img_mini_gallery hvr-grow">
				<img src="./assets/images/gallery/img_6.png" alt="Cat" class="img_mini_gallery hvr-grow">
				<img src="./assets/images/gallery/img_7.png" alt="Cat" class="img_mini_gallery hvr-grow">
				<img src="./assets/images/gallery/img_8.png" alt="Cat" class="img_mini_gallery hvr-grow">
			</div>
		</div>

		<div class="contact">
			<div>
				<h1 class="big_margin_b" id="contact">Say Hello!</h1>
			</div>
			
			<form class="contact_form" method="POST" action="" @submit="checkForm" novalidate="true">
				<div>
					<label for="email">EMAIL:</label><br>
					<input id="email" type="email" name="email" v-model="email" class="input_text">
				</div>
				<div>
					<label for="name">NAME AND SURNAME:</label><br>
					<input id="name" type="text" v-model="name" name="name" class="input_text">
				</div>
				<div>
					<label for="message">MESSAGE:</label><br>
					<textarea name="message" id="" cols="30" rows="10" class="input_text textarea"></textarea>
				</div>
				<div class="input_radio">
					<label for="sex" class="sex_input">SEX:</label>
					<input type="radio" name="gender" class="input_type">Male
					<input type="radio" name="gender" class="input_type">Female
					<input type="radio" name="gender" class="input_type">Will not say
				</div>
				<div>
					<p v-if="errors.length" class="error_message">
    					Please correct the following error(s):
    					<ul>
      						<li v-for="error in errors"> {{ error }} </li>
    					</ul>
  					</p>
				</div>
				<div class="input_radio">
					<input type="submit" value="SEND" class="btn_send">
				</div>
			</form>
		</div>

		<div class="footer">
			<div class="footer_info_section">
				<div class="footer_section">
					<h3>PET-FACTS.COM</h3>
					<ul>
						<li>About us</li>
						<li>Careers</li>
						<li>FAQ</li>
					</ul>
				</div>
				<div class="footer_section">
					<h3>OUR BRANDS</h3>
					<ul>
						<li>Supercoat</li>
						<li>Fancy Feast</li>
						<li>Pro Plan</li>
						<li>Beyond</li>
					</ul>
				</div>
				<div class="footer_section">
					<h3>CONTACT US</h3>
					<ul>
						<li>Contact us</li>
						<li>Terms & Conditions</li>
						<li>Privacy Policy</li>
					</ul>
				</div>
			</div>
          
			<div class="copyright">
				<p>
					Copyright is a legal right, existing in many countries, that grants the creator of an original work exclusive rights to determine whether, and under what conditions, this original work may be used by others.
				</p>
			</div>
      	</div>       
  	</div>
</div>
</template>

<script>
import AOS from 'aos'; // Animacije  -- https://github.com/michalsnik/aos
import 'aos/dist/aos.css'; // Animacije

export default {
	data() {
		return {
			hover: false, // Velika galerija
			name: null,
			email: null,
			errors: [],
		}
	},
	methods: {
		checkForm(e) {
		this.errors = [];

		if (!this.name) {
			this.errors.push('Enter Your name...');
		}
		if (!this.email) {
			this.errors.push('Enter Your email...');
		} else if (!this.validEmail(this.email)) {
			this.errors.push('Enter valid email...');
		}

		if (!this.errors.length) {
			return true;
		}

		e.preventDefault();
		},

		validEmail(email) {
		var re = /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
		return re.test(email);
		}
	}
}

AOS.init(); // Animacije
</script>

<style>
/*
CSS reset
*/
html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed,
figure, figcaption, footer, header, hgroup,
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
 margin: 0;
 padding: 0;
 border: 0;
 font-size: 100%;
 font: inherit;
 vertical-align: baseline;
}
#container {
    display: flex;
    flex-direction: column;
}
body{
    font-family: Open Sans;
    font-size: 20px;
    font-weight: normal;
    overflow-x: hidden;
    color: #2B2B2B;
    line-height: 30px;
    letter-spacing: 0.0888889px;
}
html {
    scroll-behavior: smooth;
}
#container {
    width: 1440px;
    margin: auto;
}
h1 {
    font-size: 46px;
    line-height: 53px;
    text-align: center;
    letter-spacing: 0.204444px;
}
h2 {
    font-size: 36px;
    line-height: 49px;
    letter-spacing: 0.16px;
}
/* mali naslovi u footer-u */
h3 {
    font-weight: bold;
    padding-bottom: 40px;
}
/* lista u footer-u*/
ul li {
    list-style: none;
}
/* lista u navigaciji */
ol li {
    list-style: none;
    display: inline;
    text-transform: uppercase;
    padding-right: 50px;
}
/* linkovi u navigaciji */
a , a:link , a:visited {
    color: #545355;
    text-decoration: none;
}
input:focus,
select:focus,
textarea:focus,
button:focus {
    outline: none;
}
/* H1 - Daily pet facts - Love!*/
.big_margin_tb {
    margin: 110px 0px 100px 0px;
}
/* H1 - Gallery*/
.medium_margin_tb {
    margin: 74px 0px;
}
/* H2 */
.medium_margin_b {
    margin-bottom: 25px;
}
.big_margin_b {
    margin-bottom: 50px;
}
/* dvije klase za odvojiti slike od teksta u glavnom section-u */
.section_margin_left {
    margin-left: 30px;
}
.section_margin_right {
    margin-right: 30px;
}
/* klasa za slike u glavnom section-u*/
.section_image {
    width: 445px;
    height: 445px;
}
.navigation {
	padding: 10px 150px;
	display: flex;
	flex-direction: row;
	background-color: #F7F7F7;
	align-items: center;
}
/* ikona u navigaciji */
.navi_icon {
	width: 40px;
	height: 40px;
	padding-right: 100px;
	margin-top: 5px;
}
.content , .header{
    background-color: #F7F7F7;
    display: flex;
    flex-direction: column;
}
.gallery , .contact {
    display: flex;
    flex-direction: column;
}
/* Prvi section sa mačkama */
.content_section {
    display: flex;
    justify-content: space-between;
    margin: 0px 165px;
    padding-bottom: 75px;
    letter-spacing: 0.0888889px;
    line-height: 30px;
}
/* klasa za drugi section sa psima */
.section_reverse {
    display: flex;
    flex-direction: row-reverse;
}
/* section sa tri velike slike*/
.big_gallery {
    margin-bottom: 74px;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}
/* navigacija za veliku galeriju - strelice */
.gallery_navigation {
    margin: 0px 165px 107px 165px;
    text-align: center;
    display: flex;
    justify-content: space-around;
}
/* section sa 8 malih slika */
.mini_gallery {
    margin: 0px 165px 100px 165px;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}
/* Grow - animacija za mini gallery*/
.hvr-grow {
  display: inline-block;
  vertical-align: middle;
  -webkit-transform: perspective(1px) translateZ(0);
  transform: perspective(1px) translateZ(0);
  box-shadow: 0 0 1px rgba(0, 0, 0, 0);
  -webkit-transition-duration: 0.3s;
  transition-duration: 0.3s;
  -webkit-transition-property: transform;
  transition-property: transform;
}
.hvr-grow:hover, .hvr-grow:focus, .hvr-grow:active {
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
}
.img_mini_gallery {
    margin-bottom: 30px;
}
/* div koji se prikazuje na hover slike - opis životinje */
.div_show_text {
	position: relative;
}
.div_show_text .show_text {
	position: absolute; 
  	bottom: 7px; 
  	color: #FFF;
	background-image: linear-gradient(rgba(180,180,180,0.3) ,rgba(0,0,0,0.8));
  	font-size: 18px;
	border-radius: 10px;
	line-height: 120%;
  	padding: 20px 30px;
}
/* CONTACT*/
.contact_form {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 50px;
}
.input_text {
    width: 600px;
    height: 40px;
    border: 1px solid #545355;
    border-radius: 5px;
    font-size: 18px;
    margin-bottom: 20px;
    padding-left: 10px;
}
.textarea {
    height: 300px;
}
.input_radio {
    width: 600px;
    height: 40px;
    margin-bottom: 20px;
}
.input_type {
    display: inline-flex;
    flex-direction: row;
    align-self: flex-end;
}
.btn_send {
    background-color: #FFF;
    font-weight: bold;
    border: 1px solid #545355;
    border-radius: 5px;
    padding: 15px 50px;
}
label {
    font-weight: bold;
    font-size: 18px;
    padding-left: 10px;
}
.sex_input {
    margin-right: 260px;
}
.error_message{
	background-color: #E02525;
	color: #FFF;
	margin-bottom: 20px;
	border-radius: 10px;
	padding: 10px;
}
/* END CONTACT*/
.footer {
    font-size: 16px;
    line-height: 28px;
    text-align: center;
    letter-spacing: 0.0711111px;
    color: #FFFFFF;
    background-color: #1D1D1D;
    padding: 80px 60px;
}
.footer_info_section {
    display: flex;
    justify-content: space-around;
}
.copyright {
    padding: 40px 200px 0px 200px;
}
</style>

<template>
	<div id="home">
		
		<header class="flex flex-col h-screen relative items-center justify-center w-full">	
			<div class="background"></div>
			<div style=" background:transparent;" class="lg:w-5/6 pt-16 w-full relative w-full flex flex-col ">
				ini adalah content
			</div>
		</header>

		<section style="background-color:#f8f9fa" class="w-full  py-4 md:pb-16 flex flex-col items-center">

			<div class="lg:w-5/6 w-full lg:mt-10 mt-6 px-4 lg:px-0 ">
				<div class="section-header mb-5 md:mb-8 lg:mb-10 flex justify-between items-center">
					<h1 class="font-bold text-lg md:text-xl lg:text-2xl">
						Berita Terbaru
					</h1>
					<a href="#" class="text-xs md:text-lg capitalize underline">
						lihat selengkapnya
						<span class="material-icons">
							keyboard_arrow_right
						</span>
					</a>
				</div>
				<div class="section-body md:p-12 p-8" style="background-color: white;">
					<card-horizontal :image="image1">
						
					</card-horizontal>
					<card-horizontal :image="image1">
						
					</card-horizontal>
				</div>
			</div>
			
		</section>

		<section style="background-color:#f8f9fa" class="justify-center flex py-4 lg:py-4">
			
			<div class="lg:w-5/6 w-full px-4 md:px-8 lg:px-0 ">
				<div class="section-header md:mb-10 mb-4 flex justify-between items-center">
					<h1 class="font-bold text-xl md:text-xl lg:text-2xl">
						Pengumuman
					</h1>
					<a href="#" class="text-xs md:text-base capitalize underline">
						lihat selengkapnya
						<span class="material-icons">
							keyboard_arrow_right
						</span>
					</a>
				</div>
				<div class="section-body md:p-12 p-8 " style="background-color: white; min-height: 300px;">
					<div class="grid gap-4 md:gap-10 md:grid-cols-2 grid-cols-1">
						<div class="flex flex-col justify-between">
							<a href="" class="md:text-base text-sm">
							Lorem ipsum dolor, sit amet consectetur adipisicing elit. Fugiat mollitia veritatis autem expedita fuga exercitationem, alias unde ratione temporibus dolorem, quibusdam doloremque perferendis consequuntur placeat delectus adipisci numquam ex! Tempore!
							</a>
							<span>
								
							</span>
						</div>
						<a href="" class="hidden md:block">
							Lorem, ipsum dolor sit amet consectetur adipisicing, elit. Nisi expedita laborum consequuntur, ad quia dicta enim magni alias sequi temporibus quaerat voluptate officia unde sint nulla. Non dolore, eaque error.
						</a>
					</div>
				</div>
			</div>
		</section >

		<section class="justify-center flex py-4 lg:py-4">
			<div class="lg:w-5/6 w-full lg:mt-10 mt-6 px-4 lg:px-0 ">
				<div class="section-header mb-5 md:mb-8 lg:mb-10 flex justify-between items-center">
					<h1 class="font-bold text-lg md:text-xl lg:text-2xl">
						Widget
					</h1>
				</div>
				<div class="grid grid-cols-1 md:gap-6 lg:gap-8 gap-2 md:grid-cols-2">
					<div class="section-body md:p-12 p-8 " style="background-color: white;">
						<div class="menu b-2 md:mb-4 lg:mb-6 flex justify-between">
							<h1 style="" class="font-bold text-lg md:text-xl lg:text-xl">
								Events
							</h1>

							<a href="#">
								<span class="material-icons">
									more_horiz
								</span>
							</a>
						
						</div>
						<img :src="image2" class="mb-2 md:mb-4 lg:mb-6" alt="">
						<div class="event-today mb-2 md:mb-4 lg:mb-6 flex flex-col items-center">
							<h1 class="capitalize  text-sm md:text-base lg:text-lg">
								No event today
							</h1>
						</div>
						<div class="paginate flex flex-row justify-around">
							<a href="">1</a>
							<a href="">2</a>
							<a href="">3</a>
							<a href="">4</a>
							<a href="">31</a>
						</div>
					</div>
					<div class="section-body md:p-12 p-8 " style="background-color: white;">
						<div class="menu mb-2 md:mb-4 lg:mb-6 flex justify-between">
							<h1 style="" class="font-bold text-lg md:text-xl lg:text-xl">
								Agenda
							</h1>

							<a href="#" class="md:text-base text-sm">
								<span class="material-icons">
									more_horiz
								</span>
							</a>
						
						</div>
						
					</div>
				</div>
			</div>
		</section>
		<section style="background-color:#f8f9fa" class="justify-center flex  lg:-8">
			
			<div class="lg:w-5/6 w-full px-4 md:px-8 lg:px-0 ">
				<div class="section-header md:mb-6 lg:mb-8 mb-4 flex justify-between items-center">
					<h1 class="font-bold capitalize text-xl md:text-xl lg:text-2xl">
						Destinasi wisata
					</h1>
				</div>
				<carousel :settings="settings" :breakpoints="breakpoints">
					<Slide v-for="slide in 10" :key="slide">
						<Card class="mx-2" :image="image1"></Card>
					</Slide>

				    <template #addons>
				       <navigation />
     				 	<pagination />
				    </template>
				  </carousel>
			</div>
		</section >
	</div>
</template>
<script>
	import Card from '@/components/Card'
	import 'vue3-carousel/dist/carousel.css';
	import { Carousel, Navigation, Slide } from 'vue3-carousel';
	import CardHorizontal from '@/components/CardHorizontal.vue'
	import image1 from '@/assets/img/kopi_sewu.jpg'
	import image2 from '@/assets/img/gandrung_sewu.jpg'
	export default {
		components: {
			CardHorizontal,
			  Carousel,
		    Slide,
		    Navigation,
		    Card
		},
		data(){
			return {
				image1: image1,
				image2: image2,
				settings:{
					itemsToShow: 1,
					snapAlign: 'center'
				},
				breakpoints: {
					576: {
						itemsToShow: 2.5,
						 snapAlign: "center"
					},
					1024: {
			          itemsToShow: 3,
			           snapAlign: "center"
			        }
				}
			}
		}
	}
</script>
<style lang="stylus">

	$primary = #4E47DE
	
	#home
		header
			.background
					background: $white;
					position:absolute
					height 100vh
					width 100%
					background: linear-gradient(90deg, rgba(78,71,222,1) 58%, rgba(0,110,251,1) 97%, rgba(0,134,250,1) 99%);
		
		section
			
			background-color:#f8f9fa
			.section-header 
				h1
					color: #22223b
			
				a
					color: #4a4e69
					letter-spacing:1.4px;
				a:hover 
					color:#FFC14F
					transition-property color
					transition-duration .6s	
					
			.section-body
				
				
				border-radius 20px
				box-shadow 0 0 20px 1px #E9E9E9
				min-height 200px
				// border 1px solid gray
				width 100%	
					
				> div
					> h1
						color:gray;
						font-weight bold
				.menu
					font-family 'Nunito', sans-serif
					h1 
						color:gray
					
					a
						color: #84a59d
					a:hover, a:focus 
						color: #22223b
						transition-property all
						transition-duration .6s
	
				img 
					border-radius 20px;
					
				.paginate
					a
						padding:6px 18px;
						font-weight 600
						color:gray
						position relative
						border 1px solid lightgray
						border-radius 50%
						background-color #f0efeb
						font-size:.875rem
					a:hover
						background-color $primary
						color:white
						
						transition-duration .6s
						transition-property all
	.carousel__viewport 
		padding: 16px 0px	

			
</style>
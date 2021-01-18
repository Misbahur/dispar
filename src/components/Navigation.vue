<template>
    <div id="nav-top" :class="[scrolled ? 'scrolled' : '']">
    	<div class="nav-wrapper w-full h-full">
    		<div class="background-box"></div>
	    	<nav class="nav-body lg:w-5/6 w-full p-8 lg:px-0 flex justify-between items-center">
	    		<div class="logo flex items-center">
	    			<img :src="logo" alt="">
	    		</div>
	    		<ul class="nav-item hidden lg:flex list-none m-0 p-0">
    				<li><a href="">profil</a></li>
    				<li><a href="">program</a></li>
    				<li><a href="">informasi public</a></li>
    				<li><a href="">berita</a></li>
    				<li><a href="">galeri</a></li>
    				<li><a href="">pengumuman</a></li>
    				<li><a href="">regulasi</a></li>
    				<li><a href="">ppid</a></li>
    				<li><a href="">kontak</a></li>
    			</ul>
    			<a class="block lg:hidden">
    				<span class="material-icons">
    					menu
    				</span>
    			</a>
	    	</nav>
    	</div>
    </div>   
</template>

<script>
	import logo_new from '@/assets/logo.png'
export default {
	name:"Navigation",
	data(){
		return {
			logo: logo_new,
			scrolled: false,
		}
	},

	methods: {
		verticalScroll(){
			let vScroll = window.scrollY > 10
			this.scrolled = vScroll
			console.log(this.scrolled)
		}
	},

	created() {
		window.addEventListener('scroll', this.verticalScroll)
	}


}
</script>

<style lang="stylus" scoped>

	.scrolled 
		.nav-wrapper
			background: rgb(78,71,222);
			box-shadow 0 2px 20px 1px rgba(78,71,222, 1)
			position:absolute
			height 100vh
			width 100%
			

	.nav-wrapper 
		color: white

	#nav-top
		position: fixed
		z-index 11
		height 100px
		top:0
		width 100%
		
		.nav-wrapper 
			position: relative
			height 100%
			width 100%
			display: flex
			
			justify-content center
			
			.background-box
				position: absolute
				
				z-index -1
				height 100% 
				width 100%
				
			
					
			.nav-body
				.logo
					img
						padding: 20px
						width 70%;
						height auto;
						vertical-align middle

			
				.nav-item 
					li
						padding: 0px 8px
						a
							font-size: 14px;
							text-transform uppercase
							font-weight 600			
				
		


		
</style>
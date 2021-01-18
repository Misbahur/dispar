<template>
	<div id="card-horizontal">
		<div class="card lg:py-8 py-4">
			<div class="md:grid-cols-3 grid gap-4">
				<div class="card-body md:col-span-2">
					<a href="" id="item-link" class="text-base lg:text-lg">
						Anim duis cillum reprehenderit fugiat adipisicing excepteur ex consequat excepteur officia aute.
					</a>
					<div id="description">
						<div id="posted" class="flex flex-row text-xs md:text-base" >
							<span id="date-time mb-1"><span class="text-gray-400">
								Time
							</span>: 2020-12-09</span>
							<span class="by pl-5"><span class="capitalize" style="color:gray">post by</span>: Admin</span>
							
						</div>
						<p id="text-desc" class="text-sm md:text-base">
							Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
							tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
							quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
							consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
							cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
							proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
						</p>
					</div>
				</div>
			    <div class="hidden md:block card-image md:col-span-1">
			    	<img :src="image" alt="">
			    </div>
			</div>
		</div>
	</div>
</template>
<script>
	export default {
		props:['image'],
		data() {
			return {

			}
		}
	}
</script>
<style lang="stylus">
	#card-horizontal
		.card
			.card-body 
				display flex
				flex-direction column
				#item-link
					font-weight bold
					margin-bottom .5em
				#item-link:hover 
					color: #4E47DE
					transition-property all
					transition-duration .6s
				#posted
					margin-bottom 1em
					
					#text-desc
						text-align justify
			.card-image
				img
					border-radius 20px
					

				
</style>
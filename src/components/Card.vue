<template>
	<div id="card" class="w-full">
		<div class="card-body p-2 md:p-4">
			<img :src="image" class="mb-2 md:mb-4 lg:mb-8">
						
		</div>
	</div>
</template>

<script>
export default {
	props: [
		"image"
	],
  name: 'Card',

  data () {
    return {

    }
  }
}
</script>

<style lang="stylus" scoped>
	#card
		background-color:white
		border-radius  10px
		min-height 150px;
		box-shadow 0 0 20px 2px #E9E9E9		
		
		.card-body
			
			img 
				border-radius:10px
				width 100%
				height auto
			
</style>
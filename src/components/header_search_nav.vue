<template>
	<header class="mui-bar mui-bar-nav custom-nav-header custom-nav-header-search">
		<a v-on:click="leftIconClick">
			<img v-bind:src="headerNavData.leftIcon">			
		</a>
		<div v-if="headerNavData.search" class="mui-input-row mui-search custom-search">
			<input type="search" class="mui-input-clear" placeholder="搜索商品"/>
		</div>
		<div else-if class="title">
				<h4>{{ headerNavData.title }}</h4>
		</div>
		<a v-on:click="rightIconClick">
			<img v-bind:src="headerNavData.rightIcon">			
		</a>
	</header>
</template>

<script>
	export default{
		props: ['headerNavData'],
		methods: {
			leftIconClick: function(){
				this.$emit('click', 'leftIcon')
			},
			rightIconClick: function(){
	//			this.$emit('click', event.target)
				this.$emit('click', 'rightIcon')
			}
		}
	}
</script>

<style>
</style>
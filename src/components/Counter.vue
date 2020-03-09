<template>
	<div>
		<button v-on:click="increase">increase</button>
		<button v-on:click="decrease">decrease</button><br>
		{{count}}
	</div>
</template>

<script>
	export default {
		data() {
			return {
				count:0
			}
		},
		methods: {
			increase() {
				if (this.count < 10) {
					return this.counter++;
				} else {
					alert("You cannot buy more than 10 items");
				}
			},
			decrease() {
				if (this.counter > 0) {
					return this.count--;
				} else {
					return this.count;
				}
			}
		}
	} 
</script>

<style scoped>
	header{
		background:rgb(122, 63, 100);
		padding:10px;
		border-style: solid;
		border-color:black;
		border-width: 2px;
	}
	button{
		background-color:rgb(139, 158, 190);
		font-size:25px;
		border-radius: 10px;
		text-align: center;
		text-decoration: none;
		display:inline-block;
		padding:10px 30px;
	}
	img{
		width:100px;
		height:100px;
	}
	label{
		width:100px;
		font-size: 30px;
	}
</style>
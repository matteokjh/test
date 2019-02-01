<template>
	<div class="hello">
		<div class="title">
			<h1>{{ msg }}</h1>
		</div>
		<hr>
		<task1></task1>
		<hr>
		<task2></task2>
		<hr>
		<task3></task3>
		<hr>
	</div>
</template>

<script>
import Task1 from '@/components/task1.vue'
import Task2 from '@/components/task2.vue'
import Task3 from '@/components/task3.vue'
export default {
	name: 'HelloWorld',
	data () {
		return {
			msg: '测试'
		}
	},
	components: {
		'task1': Task1,
		'task2': Task2,
		'task3': Task3,

	}
	
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
	width: 700px;
	margin: auto;
	background-color: #fff;
	padding: 5vh 0;
	min-height: 90vh;
}
.title {
	padding: 0 5vw;
}
ul {
	list-style-type: none;
	padding: 0;
}
li {
	display: inline-block;
	margin: 0 10px;
}
a {
	color: #42b983;
}
hr {
	margin: 40px 0;
    border: none;
    height: 3px;
    background-color: #ddd;
    background-image: repeating-linear-gradient(-45deg,#fff,#fff 4px,transparent 0,transparent 8px);
}
</style>

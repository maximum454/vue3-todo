<template>
	<div class="home">
		<TaskAdd></TaskAdd>
		<TaskList v-bind:list="ArrList"></TaskList>
	</div>
</template>

<script>

import TaskList from "@/components/TaskList";
import TaskAdd from "@/components/TaskAdd";

export default {
	name: 'HomeView',
	components: {TaskAdd, TaskList},
	data: function () {
		return {
			ArrList: [
				{id: 1, name: 'Задача 1'},
				{id: 2, name: 'Задача 2'},
				{id: 3, name: 'Задача 3'},
				{id: 4, name: 'Задача 4'},
			]
		}
	},
	setup() {


		return {}
	}
}
</script>

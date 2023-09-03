<template>
	<div class="home">
		<task-add v-bind:list="listTask"></task-add>
		<task-list v-bind:list="listTask"></task-list>
	</div>
</template>

<script>
import TaskAdd from "@/components/TaskAdd";
import TaskList from "@/components/TaskList";

export default {
	name: 'HomeView',
	components: {
		TaskList,
		TaskAdd,
	},
	data(){
		return{
			listTask: [
				{id:1, name: 'Название'}
			]
		}
	}
}
</script>

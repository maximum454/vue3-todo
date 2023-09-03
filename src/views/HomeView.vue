<template>
	<div class="home">
		<task-add></task-add>
		<task-list></task-list>
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
	}
}
</script>

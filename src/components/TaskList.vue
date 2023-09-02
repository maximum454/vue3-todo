<template>
	<ol class="task">
		<li class="task__item" v-for="item in list" v-bind:key="item.id">
			<div class="task__name">{{ item.name }}</div>
			<div class="task__del">x</div>
		</li>
	</ol>
</template>

<script>
import {onMounted} from 'vue'
import {initFlowbite} from 'flowbite'

export default {
	name: "TaskList",
	props: {
		list: {
			default: () => [],
			type: Array,
		}
	},
	setup() {
		onMounted(() => {
			initFlowbite();
		})
	}
}
</script>

<style scoped lang="scss">
.task {
	margin: 0 auto;
	padding: 0;
	max-width: 400px;

	&__item {
		display: flex;
		gap: 20px;
	}

	&__name {

	}

	&__del {

	}
}
</style>
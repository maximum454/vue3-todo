<template>
	<ol class="task w-1/2 mx-auto mt-5">
		<li class="task__item" v-for="item in list" v-bind:key="item.id">
			<div class="task__name">{{ item.name }}</div>
			<div class="task__btns">
				<button type="button" class="task__success">Выполнено</button>
				<button type="button" class="task__del">Удалить</button>
			</div>
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
	&__item {
		@apply mb-2 flex justify-between items-center
	}

	&__name {

	}

	&__btns{
		@apply space-x-2
	}
	&__success{
		@apply focus:outline-none text-white bg-green-600 hover:bg-green-800 focus:ring-4 focus:ring-green-300 font-medium rounded-lg text-sm px-5 py-2.5 dark:bg-green-600 dark:hover:bg-green-700 dark:focus:ring-green-800
	}
	&__del{
		@apply focus:outline-none text-white bg-red-600 hover:bg-red-800 focus:ring-4 focus:ring-red-300 font-medium rounded-lg text-sm px-5 py-2.5 dark:bg-red-600 dark:hover:bg-red-700 dark:focus:ring-red-900
	}
}
</style>
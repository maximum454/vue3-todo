<template>
	<form class="form-add w-1/2 mx-auto mb-2">
		<label for="default-todo" class="mb-2 text-sm font-medium text-gray-900 sr-only dark:text-white">Задачи</label>
		<div class="relative">
			<div class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none">
				<svg aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5 text-gray-500 dark:text-gray-400">
					<path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.5v15m7.5-7.5h-15" />
				</svg>

			</div>
			<input type="text" id="default-todo" class="form-add__input" v-bind:value="nameTask" placeholder="Введите название задачи" required>
			<button type="submit" class="form-add__btn" @click="createTask">Добавить</button>
		</div>
	</form>
</template>

<script>
export default {
	name: "TaskAdd",
	props: {
		list: {
			default: () => [],
			type: Array,
		}
	},
	data(){
		return{
			nameTask: '',
		}
	},
	methods: {
		createTask() {
			list.push(this.nameTask)
		}
	}
}
</script>

<style scoped lang="scss">
.form-add{
	&__input{
		@apply block w-full p-4 pl-10 text-sm text-gray-900 border border-gray-300 rounded-lg bg-gray-50 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500
	}
	&__btn{
		@apply text-white absolute right-2.5 bottom-2.5 bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-4 py-2 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800
	}
}
</style>
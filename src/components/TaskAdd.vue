<template>
	<form action="" class="form-add">
		<input type="text" placeholder="Задача" class="form-add__input">
		<button type="button" class="form-add__btn">Add</button>
	</form>
</template>

<script>
export default {
	name: "TaskAdd"
}
</script>

<style scoped lang="scss">
.form-add {
	margin-bottom: 40px;
}

.form-group {
	margin-bottom: 20px;
}
</style>
<template>
    <header>
        <h1>{{ title }}</h1>
        <AppButton @btn-click="$emit('toggle-add-task')"
         :text="showAddTask ? 'Close' : 'Add Task'"
         :color="showAddTask ? 'red' : 'green'" />
    </header>
</template>

<script>
import AppButton from './AppButton.vue';

export default {
    name: 'AppHeader',
    props: {
        title: String,
        showAddTask: Boolean,
    },
    components: {
        AppButton
    }
}
</script>

<style scoped>
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 30px;
}
</style> 
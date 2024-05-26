<template>
    <div :key="task.id" v-for="task in tasks">
        <IndividualTask @toggle-reminder="$emit('toggle-reminder', task.id)" @delete-task="$emit('delete-task', task.id)" :task="task" />
    </div>
</template>

<script>
import IndividualTask from './IndividualTask.vue';

export default {
    name: 'TasksToDo',
    props: {
        tasks: Array
    },
    components: {
        IndividualTask
    },
    emits: ['delete-task', 'toggle-reminder'],
}
</script>
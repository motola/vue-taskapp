<template>
<header>
    <h1>{{  title }}</h1>
    <Button @toggle-task="toggleTask" :text="showAddTask ? 'Close' : 'Add Task'" color="green" />
</header>
    
</template>


<script>
import Button from './Button.vue'


export default {
    name: 'Header',
    components: {
        Button
    },  
    props: {
        title: String,
        showAddTask: Boolean  
    },
    emits: ['toggle-task'],
    methods: {
        toggleTask() {
            this.$emit('toggle-task');
        }
    }

    
}
</script>


<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}

</style>
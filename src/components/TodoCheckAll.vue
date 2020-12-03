<template>
    <div><label><input type="checkbox" :checked="!anyRemaining" @change="AllChecked"> Check All</label></div>
</template>

<script>
export default {
    name: 'todo-check-all',
    props: {
        anyRemaining: {
            type: Boolean,
            required: true
        }
    },
    methods: {
        AllChecked() {
            eventBus.$emit('checkAllChanged', this.anyRemaining)
        }
    }
}
</script>
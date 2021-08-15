<template>
    <div id="app">
        <div v-for="n in notifications" :key="n.title">
            <PushAlert v-if="n.type == 'push'" :notification="n" />
        </div>
    </div>
</template>

<script>
import PushAlert from './components/PushAlert.vue';

export default {
    data() {
        return {
            notifications: [
                {
                    title: 'title1',
                    description: 'Description 1',
                    type: 'push',
                },
                {
                    title: 'title2',
                    description: 'Description 3',
                    type: 'push',
                },
                {
                    title: 'title3',
                    description: 'Description 3',
                    type: 'modal',
                },
            ],
        };
    },
    components: {
        PushAlert,
    },
};
</script>
<style lang="scss">
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
}
</style>

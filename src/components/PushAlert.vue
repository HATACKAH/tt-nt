<template>
    <div class="push">
        <h3>{{ notification.title }}</h3>
        <p>{{ notification.description }}</p>
    </div>
</template>

<script>
export default {
    name: 'PushAlert',

    props: {
        notification: {
            type: Object,
            required: true,
        },
    },
};
</script>

<style scoped lang="scss">
@keyframes opacityon {
    from {
        opacity: 0;
    }
    to {
        opacity: 1;
    }
}
.push {
    width: 20%;
    margin: auto;
    border: 1px solid #b48af2;
    border-radius: 10px;
    margin-bottom: 10px;
    animation-duration: 1.5s;
    animation-name: opacityon;
}

@media screen and (max-width: 700px) {
    .push {
        width: 100%;
    }
}
</style>

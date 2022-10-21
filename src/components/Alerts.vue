<template>
    <Alert :message="message" :type="type" />
</template>

<script>
import Alert from './Alert.vue';

export default {
    props: ['message', 'type'],
    components: {
        Alert
    }
}
</script>
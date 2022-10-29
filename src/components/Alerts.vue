<template>
    <Alert :message="message" :type="type" v-for="type in types" :key="item" :show="true" />
</template>

<script>
import Alert from './Alert.vue';

export default {
    props: ['message', 'type', 'types'],
    components: {
        Alert
    }
}
</script>
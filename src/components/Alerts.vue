<template>
    <Alert :message="message" :type="type" v-for="type in types" :key="item" :show="true" />
</template>

<script>
import Alert from './Alert.vue';

export default {
    // props: ['message', 'types'],
    props: {
        message: String,
        types: Array
    },
    components: {
        Alert
    }
}
</script>
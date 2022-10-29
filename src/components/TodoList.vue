<template>
    <ul class="list-group">
        <li class="list-group-item" v-for="item in items" :key="item.id">
            <p class="mb-0 pb-2">{{ item.name }}</p>
            <button class="btn btn-sm btn-success">Done</button>
        </li>
        <li class="list-group-item">All: {{ all }} | Todo: {{ todo }} | Done: {{ done }}</li>
    </ul>
</template>

<script>
export default {
    props: ['endpoint'],
    data: () => ({
        items: [],
        all: 3,
        todo: 1,
        done: 1
    }),
    methods: {
        mockApi () {
            this.items = [
                { id: 1, name: "Video recording", done: true },
                { id: 2, name: "Editing recording", done: true },
                { id: 3, name: "Publishing recording", done: false },
            ]
        }
    },
    mounted () {
        setTimeout(() => this.mockApi(), 1000);
    }
}
</script>
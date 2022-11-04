<template>
    <ul class="list-group">
        <li class="list-group-item" v-for="item in items" :key="item.id">
            <slot v-bind="item"></slot>
        </li>
        <li class="list-group-item">
            <slot name="footer" :all="all" :todo="todo" :done="done">
                All: {{ all }} | Todo: {{ todo }} | Done: {{ done }}
            </slot>
        </li>
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
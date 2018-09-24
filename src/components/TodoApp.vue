<template lang="pug">
    ol.list
        li(v-for="(item,index) in items" @click="check(index)") 
            | {{ index + ". " + item }}
        input(type="text" v-model="newItem" @keyup.enter="itemAdd")
        button(@click="itemAdd") Add
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    data: ()=>({
        items: new Array,
        newItem: "",
    }),
    methods: {
        itemAdd: function () {
            this.items.push(this.newItem);
            this.newItem = "";
        },
        check: function (index:number) {
            this.items = this.items.filter((item, i) => {
                return i != index;
            });
        }
    },
    name: 'TodoApp'
});
</script>

<style scoped lang="scss">
    ol {
        list-style-type: none;
    }
    ol:hover {
        cursor: pointer;
    }
</style>
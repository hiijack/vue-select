<template>
    <div>
        <div class="searchBox">
            <input class="searchInput" type="text" placeholder="点一下" v-on:click="showList" v-bind:value="text"/>
        </div>
        <SelectList v-show="listShow" v-bind:list="listValue" v-on:changeValue="changeValue"></SelectList>
    </div>
</template>

<script>
import SelectList from './SelectList'
export default {
    name: 'customList',
    components: {
        SelectList
    },
    data() {
        return {
            listShow: false,
            text: '',
            listValue: ['vue', 'react', 'angular']
        }
    },
    methods: {
        showList() {
            this.listShow = true;
        },
        hideList() {
            this.listShow = false;
        },
        changeValue(val) {
            this.text = val;
            this.listShow = false;
        }
    }
}
</script>

<style scoped>
    .searchBox {
        border-width: 1px;
        border-style: solid;
        border-color: #ccc;
        width: 85%;
        display: inline-block;
    }
    
    .searchInput {
        float: left;
        width: 95%;
        height: 35px;
        margin: 3px 1px 0 15px;
        padding: 0 10px 0 0;
        font-size: 16px;
        outline: none;
        border: 0;
        box-sizing: content-box;
    }
    
</style>

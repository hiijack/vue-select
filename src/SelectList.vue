    <template>
        <ul class="list-group">
            <li class="list-group-item" v-for="item of list" @click="selectItem(item)">
                <!--<a href='#' v-on:click="selectItem(item)">{{item}}</a>-->
                {{item}}
            </li>
        </ul>
    </template>
    <script>
    export default {
        name: 'SelectList',
        props: ['list'],
        methods: {
            selectItem(item) {
                this.$emit('changeValue', item);
            }
        }
    }
    </script>
    <style scoped>
        .list-group {
            margin: auto;
            width: 85%;
            padding-left: 0px;
        }
        
        .list-group-item {
            position: relative;
            display: block;
            padding: 10px 15px;
            margin-bottom: -1px;
            background-color: #fff;
            border: 1px solid #ddd;
        }
        
        ul {
            list-style-type: none;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        li {
            cursor: pointer;
            text-align: left;
            border: 0;
            border-collapse: collapse;
            border-spacing: 0;
            list-style: none;
            margin: 0;
            padding: 0;
        }
        
        li:hover {
            background-color: #ccc;
        }
    </style>

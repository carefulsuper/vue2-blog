<template>
    <div id="WelCome">
        <div class="block" style="padding-top: 140px"><el-avatar :size="100" :src="circleUrl"></el-avatar></div>
        <div style="display: inline-block" v-for="(item,index) in columns" :key="index">
            <el-card style="background: #FF9671;color: #fff;height: 100px;width: 165px" >
                <div @click="ToList">
                    {{item.title}}
                </div>
                <div>
                    {{item.numbers}}
                </div>
                <div>
                    {{item.content}}
                </div>
            </el-card>
        </div>
        <div>
            <el-table
                    :data="tableData"
                    style="width: 60%;margin-left: 20%">
                <el-table-column
                        prop="date"
                        label="日期"
                        width="180">
                </el-table-column>
                <el-table-column
                        prop="title"
                        label="标题"
                        width="180">
                    <template slot-scope="scope">
                        <el-link type="primary" @click="ToDetail">{{scope.row.title}}</el-link>
                    </template>
                </el-table-column>
                <el-table-column
                        prop="tags"
                        label="标签">
                </el-table-column>
            </el-table>
        </div>
    </div>
</template>

<script>
    export default {
        name: "WelCome",
        components:{},
        props:'',
        data(){
            return {
                circleUrl: "https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png",
                columns:[
                    {
                        title:'',
                        numbers:'12'
                    },
                    {
                        title:'',
                        numbers:'12'
                    },
                    {
                        title:'我是小猪佩奇',
                        content:'',
                        numbers:'12'
                    },
                    {
                        title:'学习笔记',
                        content:'我是小猪佩奇'
                    }
                ],
                tableData: [{
                    date: '2016-05-02',
                    title: '王小虎',
                    tags: '上海市普陀区金沙江路 1518 弄'
                }, {
                    date: '2016-05-04',
                    title: '王小虎',
                    tags: '上海市普陀区金沙江路 1517 弄'
                }, {
                    date: '2016-05-01',
                    title: '王小虎',
                    tags: '上海市普陀区金沙江路 1519 弄'
                }, {
                    date: '2016-05-03',
                    title: '王小虎',
                    tags: '上海市普陀区金沙江路 1516 弄'
                }, {
                    date: '2016-05-03',
                    title: '王小虎',
                    tags: '上海市普陀区金沙江路 1516 弄'
                }, {
                    date: '2016-05-03',
                    title: '王小虎',
                    tags: '上海市普陀区金沙江路 1516 弄'
                }, {
                    date: '2016-05-03',
                    title: '王小虎',
                    tags: '上海市普陀区金沙江路 1516 弄'
                }, {
                    date: '2016-05-03',
                    title: '王小虎',
                    tags: '上海市普陀区金沙江路 1516 弄'
                }]
            }
        },
        methods:{
            ToDetail(){
                this.$router.push({path:'/detail'})
            },
            ToList(){
                this.$router.push({path:'/note'})
            }
        }
    }
</script>

<style scoped>
    .el-card{

        padding: 10px;
        margin: 20px;
    }
</style>

<template>
    <div>
        <div style="width: 100%;background:#FF6F91;min-height: 20px;display: flex;position:fixed">
            <div class="bigtitle">我也不知道这是什么东东</div>
            <div style="margin-top: 20px;margin-left: 60%">
                <el-button @click="dialogVisible = true" type="danger">登录</el-button>
                <el-dialog title="登录你的账号" icon="el-icon-user-solid
" :visible.sync="dialogVisible" width="30%" :before-close="handleClose">
                    <div>
                        <div style="display: flex">
                            <div class="mes">账号：</div>
                            <el-input placeholder="输入账号名称" style="width: 240px"></el-input>
                        </div>
                        <div style="display: flex;padding-top: 10px;">
                            <div class="mes">密码：</div>
                            <el-input placeholder="输入密码" style="width: 240px"></el-input>
                        </div>
                    </div>
                    <span slot="footer" class="dialog-footer">
        <el-button @click="dialogVisible = false">取 消</el-button>
        <el-button type="primary" @click="dialogVisible = false">确 定</el-button>
      </span>
                </el-dialog>
                <el-button type="danger" style="margin-left: 20px">注册</el-button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "TopView",
        components:{},
        data(){
            return{
                dialogVisible: false,
            }
        },
        methods:{
            handleClose(done) {
                this.$confirm('确认关闭？')
                    .then(() => {
                        done();
                    })
                    .catch(() => { });
            }
        }
    }
</script>

<style scoped>
.mes{
    padding-top: 8px;
    font-weight: 700;
}
  .bigtitle{
    color: #fff;
    font-size: 36px;
    font-weight: 700;
    padding: 20px;
  }
  @media (min-width: 750px) {
    .bigtitle{
      color: #fff;
      font-size: 36px;
      font-weight: 700;
      padding: 20px;
    }
  }
</style>

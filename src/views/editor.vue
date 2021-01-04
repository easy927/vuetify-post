<template>
        <v-card flex style="background-color: #FFFBE6">
            <v-divider></v-divider>
            <v-row>
                <v-col :cols="2"></v-col>
                <v-col :cols="8">
                    <template class="mx-md-15">
                        <v-card-title>
                            <span class="headline">#分享你的故事</span>
                        </v-card-title>

                        <v-card-text>
                            <v-text-field label=""
                                          v-model="post_name"
                                          style="max-width: 1200px"
                                          placeholder="书信标题"
                            ></v-text-field>
                            <mavon-editor
                                    v-model="content"
                                    ref="md"
                                    @change="change"
                                    style="height: 700px;max-width: 1200px;"
                            />
                            <v-container fluid>
                                <p>访问权限：</p>
                                <v-radio-group v-model="limits"  row>
                                    <v-radio label="公开" value="public"></v-radio>
                                    <v-radio label="仅登陆用户" value="half_public"></v-radio>
                                    <v-radio label="私密" value="private"></v-radio>
                                </v-radio-group>
                            </v-container>
                            <v-text-field label="tag标签"
                                          v-model="tags"
                                          style="max-width: 1200px"
                            ></v-text-field>
                            <v-text-field label=""
                                          v-model="post_pwd"
                                          style="max-width: 1200px"
                                          placeholder="密码保护（只有私密信件才需要密码访问）"
                            ></v-text-field>

                        </v-card-text>
                        <v-card-actions>
                            <v-btn class="ma-2" rounded color="blue" dark @click="submit">发布</v-btn>
                            <router-link to="/">
                                <v-btn class="ma-5" rounded outlined color="success" @click="">取消</v-btn>
                            </router-link>
                            <v-spacer></v-spacer>
                        </v-card-actions>
                    </template>
                </v-col>
            </v-row>
        </v-card>

</template>

<script>
    // 导入组件 及 组件样式
    import { mavonEditor } from 'mavon-editor'
    import 'mavon-editor/dist/css/index.css'
    export default {
        name: "editor",
        // 注册
        components: {
            mavonEditor,
        },
        data() {
            return {
                post_name:'',
                content:'', // 输入的markdown
                html:'',    // 及时转的html
                limits:'public',
                tags:[],
                post_pwd:'',

            }
        },
        methods: {
            // 所有操作都会被解析重新渲染
            change(value, render){
                // render 为 markdown 解析后的结果[html]
                this.html = render;
            },
            // 提交
            submit(){
                console.log(this.html);
            }
        },
        mounted() {

        }
    }
</script>

<style scoped>
    .basil {
        background-color: #FFFBE6 !important;
        justify-content: center !important;
    }

    .basil--text {
        color: #356859 !important;
    }

</style>
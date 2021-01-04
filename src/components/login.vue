<template>
    <v-dialog v-model="dialog" max-width="500px" persistent style="background-color: #FFFBE6">
        <v-card>
            <v-card-title>
                <span class="headline">登陆信息</span>
                <v-spacer></v-spacer>
                <v-btn icon color="blue light-2" @click="dialog=false">
                    <v-icon>mdi-cancel</v-icon>
                </v-btn>
            </v-card-title>
            <v-card-text>
                <v-container>
                    <v-row>
                        <v-col cols="12">
                            <v-text-field label="用户名/邮箱/手机号"
                                          v-model="username"
                                          :rules="[rules.required()]"
                            ></v-text-field>
                        </v-col>
                        <v-col cols="12">
                            <v-text-field
                                    v-model="password"
                                    :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                                    :rules="[rules.required, rules.min]"
                                    :type="show1 ? 'text' : 'password'"
                                    name="input-10-1"
                                    hint="At least 8 characters"
                                    counter
                                    @click:append="show1 = !show1"
                            ></v-text-field>
                        </v-col>
                    </v-row>
                </v-container>
            </v-card-text>
            <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn class="ma-2" rounded color="blue" dark @click="submit">登陆</v-btn>
                <v-btn class="ma-5" rounded outlined color="success" @click="reg">注册</v-btn>
            </v-card-actions>
            <register v-if="showRegister"></register>
        </v-card>
    </v-dialog>

</template>

<script>
    import Register from "./register";
    export default {
        components: {Register},
        data: () => ({
            dialog: true,
            show1: false,
            password: 'password',
            username: 'username',
            showRegister:false,
            rules: {
                required: value => !!value || 'Required.',
                min: v => v.length >= 8 || 'Min 8 characters',
                emailMatch: () => ('The email and password you entered don\'t match'),
            },
        }),
        methods:{
            submit(){
                console.log('提交登陆信息');
                this.dialog = false
            },
            reg() {
                this.showRegister = true
                this.dialog = false
            }
        }
    }
</script>

<template>
    <v-dialog v-model="dialog"  max-width="500px">
        <v-card>
            <v-card-title>
                <span class="headline">注册信息</span>
            </v-card-title>
            <v-card-text>
                <v-container>
                    <v-row>
                        <v-col cols="12">
                            <v-text-field label="昵称"
                                          v-model="username"
                                          :rules="[rules.required()]"
                            ></v-text-field>
                        </v-col>
                        <v-col cols="12">
                            <v-text-field label="邮箱/手机号"
                                          v-model="usernum"
                                          :rules="[rules.required()]"
                            ></v-text-field>
                        </v-col>
                        <v-col cols="12">
                            <v-text-field label="密码"
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
                        <v-col cols="12" sm="6">
                            <v-select
                                    :items="['男', '女']"
                                    label="性别*"
                                    required
                            ></v-select>
                        </v-col>

                    </v-row>
                </v-container>

            </v-card-text>
            <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn class="ma-3" rounded color="blue" dark @click="dialog = false">注册</v-btn>
                <!--<v-btn class="ma-5" rounded outlined color="success" @click="dialog = false">Save</v-btn>-->
            </v-card-actions>
        </v-card>
    </v-dialog>
</template>

<script>
    export default {
        data: () => ({
            dialog: true,
            show1: false,
            password: '',
            username: '',
            usernum:'',
            rules: {
                required: value => !!value || 'Required.',
                min: v => v.length >= 8 || 'Min 8 characters',
                emailMatch: () => ('The email and password you entered don\'t match'),
            },
        }),
    }
</script>
<template>

    <v-dialog v-model="dialog" max-width="500px">
        <v-card>
            <v-card-title>
                <span class="headline">登陆信息</span>
            </v-card-title>
            <v-card-text>
                <v-container>
                    <v-row>
                        <v-col cols="12">
                            <v-text-field label="邮箱/手机号"
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
                <v-btn class="ma-2" rounded color="blue" dark @click="dialog = false">登陆</v-btn>
                <router-link to="/register">
                    <v-btn class="ma-5" rounded outlined color="success" @click="dialog = false">注册</v-btn>
                </router-link>
                <router-view></router-view>
            </v-card-actions>
        </v-card>
    </v-dialog>

</template>

<script>
    export default {
        data: () => ({
            dialog: true,
            show1: false,
            password: 'password',
            username: 'username',
            rules: {
                required: value => !!value || 'Required.',
                min: v => v.length >= 8 || 'Min 8 characters',
                emailMatch: () => ('The email and password you entered don\'t match'),
            },
        }),
    }
</script>

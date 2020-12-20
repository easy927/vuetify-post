<template>
    <v-card color="basil">
        <v-card-title class="text-center justify-center py-6" :aria-level="0">

            <router-link to="/">
                <h6 class="font-weight-light display-2 basil--text">锦书</h6>
            </router-link>

            <v-spacer></v-spacer>
            <v-text-field
                    v-model="search"
                    append-icon="mdi-magnify"
                    label="搜索"
                    single-line
                    hide-details
            ></v-text-field>
            <v-spacer></v-spacer>


            <router-link to="/login">
                <v-avatar>
                    <img src="https://cdn.vuetifyjs.com/images/john.jpg"
                         alt="John"
                    ></v-avatar>
            </router-link>
            <router-view></router-view>


        </v-card-title>
        <v-divider></v-divider>

        <!--        <v-tabs
                        v-model="tab"
                        background-color="transparent"
                        color="basil"
                        vertical
                        v-for="item in items"
                >

                    <v-tab

                            :key="item"
                    >
                        <v-icon left>mdi-account</v-icon>
                        <span class="font-weight-bold subtitle-1">{{ item }}</span>
                    </v-tab>
                    <v-tab-item

                            :key="item"
                    >
                        <v-card
                                color="basil"

                        >
                            <v-card-text>{{ item }}</v-card-text>
                        </v-card>
                    </v-tab-item>
                </v-tabs>-->

        <v-tabs vertical
                background-color="transparent"
                centered
                height="900"
                overflow
        >

            <v-tab>
                <v-icon left>mdi-account</v-icon>
                Option 1
            </v-tab>
            <v-tab>
                <v-icon left>mdi-lock</v-icon>
                Option 2
            </v-tab>
            <v-tab>
                <v-icon left>mdi-access-point</v-icon>
                Option 3
            </v-tab>
            <v-tab>
                <v-icon left>mdi-access-point</v-icon>
                Option 4
            </v-tab>


            <v-tab-item>
                <v-card flat>
                    <v-card-text>
                        <p>
                            Sed aliquam ultrices mauris. Donec posuere vulputate arcu. Morbi ac felis. Etiam feugiat
                            lorem non metus. Sed a libero.
                        </p>

                        <p>
                            Nam ipsum risus, rutrum vitae, vestibulum eu, molestie vel, lacus. Aenean tellus metus,
                            bibendum sed, posuere ac, mattis non, nunc. Aliquam lobortis. Aliquam lobortis. Suspendisse
                            non nisl sit amet velit hendrerit rutrum.
                        </p>

                        <p class="mb-0">
                            Phasellus dolor. Fusce neque. Fusce fermentum odio nec arcu. Pellentesque libero tortor,
                            tincidunt et, tincidunt eget, semper nec, quam. Phasellus blandit leo ut odio.
                        </p>
                    </v-card-text>
                </v-card>
            </v-tab-item>
            <v-tab-item>
                <v-card flat>
                    <v-card-text>
                        <p>
                            Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis
                            tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris
                            ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt
                            non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
                        </p>

                        <p>
                            Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante
                            convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet
                            ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac
                            habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.
                        </p>

                        <p>
                            Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a
                            libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae
                            tortor. Aliquam eu nunc.
                        </p>

                        <p>
                            Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra
                            rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.
                        </p>

                        <p class="mb-0">
                            Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget,
                            vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis,
                            dictum sed, iaculis a, condimentum nec, nisi.
                        </p>

                        <p>
                            Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis
                            tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris
                            ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt
                            non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
                        </p>

                        <p>
                            Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante
                            convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet
                            ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac
                            habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.
                        </p>

                        <p>
                            Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a
                            libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae
                            tortor. Aliquam eu nunc.
                        </p>

                        <p>
                            Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra
                            rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.
                        </p>

                        <p class="mb-0">
                            Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget,
                            vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis,
                            dictum sed, iaculis a, condimentum nec, nisi.
                        </p>
                        <p>
                            Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis
                            tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris
                            ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt
                            non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
                        </p>

                        <p>
                            Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante
                            convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet
                            ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac
                            habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.
                        </p>

                        <p>
                            Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a
                            libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae
                            tortor. Aliquam eu nunc.
                        </p>

                        <p>
                            Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra
                            rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.
                        </p>

                        <p class="mb-0">
                            Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget,
                            vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis,
                            dictum sed, iaculis a, condimentum nec, nisi.
                        </p>
                        <p>
                            Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis
                            tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris
                            ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt
                            non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
                        </p>

                        <p>
                            Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante
                            convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet
                            ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac
                            habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.
                        </p>

                        <p>
                            Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a
                            libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae
                            tortor. Aliquam eu nunc.
                        </p>

                        <p>
                            Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra
                            rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.
                        </p>

                        <p class="mb-0">
                            Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget,
                            vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis,
                            dictum sed, iaculis a, condimentum nec, nisi.
                        </p>
                        <p>
                            Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis
                            tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris
                            ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt
                            non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
                        </p>

                        <p>
                            Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante
                            convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet
                            ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac
                            habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.
                        </p>

                        <p>
                            Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a
                            libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae
                            tortor. Aliquam eu nunc.
                        </p>

                        <p>
                            Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra
                            rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.
                        </p>

                        <p class="mb-0">
                            Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget,
                            vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis,
                            dictum sed, iaculis a, condimentum nec, nisi.
                        </p>
                        <p>
                            Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis
                            tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris
                            ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt
                            non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
                        </p>

                        <p>
                            Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante
                            convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet
                            ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac
                            habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.
                        </p>

                        <p>
                            Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a
                            libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae
                            tortor. Aliquam eu nunc.
                        </p>

                        <p>
                            Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra
                            rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.
                        </p>

                        <p class="mb-0">
                            Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget,
                            vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis,
                            dictum sed, iaculis a, condimentum nec, nisi.
                        </p>
                        <p>
                            Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis
                            tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris
                            ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt
                            non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
                        </p>

                        <p>
                            Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante
                            convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet
                            ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac
                            habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.
                        </p>

                        <p>
                            Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a
                            libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae
                            tortor. Aliquam eu nunc.
                        </p>

                        <p>
                            Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra
                            rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.
                        </p>

                        <p class="mb-0">
                            Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget,
                            vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis,
                            dictum sed, iaculis a, condimentum nec, nisi.
                        </p>
                        <p>
                            Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis
                            tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris
                            ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt
                            non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
                        </p>

                        <p>
                            Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante
                            convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet
                            ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac
                            habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.
                        </p>

                        <p>
                            Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a
                            libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae
                            tortor. Aliquam eu nunc.
                        </p>

                        <p>
                            Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra
                            rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.
                        </p>

                        <p class="mb-0">
                            Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget,
                            vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis,
                            dictum sed, iaculis a, condimentum nec, nisi.
                        </p>
                        <p>
                            Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis
                            tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris
                            ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt
                            non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
                        </p>

                        <p>
                            Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante
                            convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet
                            ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac
                            habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.
                        </p>

                        <p>
                            Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a
                            libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae
                            tortor. Aliquam eu nunc.
                        </p>

                        <p>
                            Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra
                            rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.
                        </p>

                        <p class="mb-0">
                            Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget,
                            vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis,
                            dictum sed, iaculis a, condimentum nec, nisi.
                        </p>
                        <p>
                            Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis
                            tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris
                            ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt
                            non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
                        </p>

                        <p>
                            Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante
                            convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet
                            ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac
                            habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.
                        </p>

                        <p>
                            Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a
                            libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae
                            tortor. Aliquam eu nunc.
                        </p>

                        <p>
                            Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra
                            rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.
                        </p>

                        <p class="mb-0">
                            Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget,
                            vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis,
                            dictum sed, iaculis a, condimentum nec, nisi.
                        </p>
                        <p>
                            Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis
                            tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris
                            ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt
                            non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
                        </p>

                        <p>
                            Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante
                            convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet
                            ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac
                            habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.
                        </p>

                        <p>
                            Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a
                            libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae
                            tortor. Aliquam eu nunc.
                        </p>

                        <p>
                            Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra
                            rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.
                        </p>

                        <p class="mb-0">
                            Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget,
                            vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis,
                            dictum sed, iaculis a, condimentum nec, nisi.
                        </p>
                        <p>
                            Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis
                            tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris
                            ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt
                            non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
                        </p>

                        <p>
                            Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante
                            convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet
                            ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac
                            habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.
                        </p>

                        <p>
                            Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a
                            libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae
                            tortor. Aliquam eu nunc.
                        </p>

                        <p>
                            Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra
                            rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.
                        </p>

                        <p class="mb-0">
                            Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget,
                            vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis,
                            dictum sed, iaculis a, condimentum nec, nisi.
                        </p>
                        <p>
                            Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis
                            tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris
                            ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt
                            non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
                        </p>

                        <p>
                            Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante
                            convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet
                            ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac
                            habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.
                        </p>

                        <p>
                            Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a
                            libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae
                            tortor. Aliquam eu nunc.
                        </p>

                        <p>
                            Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra
                            rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.
                        </p>

                        <p class="mb-0">
                            Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget,
                            vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis,
                            dictum sed, iaculis a, condimentum nec, nisi.
                        </p>
                        <p>
                            Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis
                            tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris
                            ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt
                            non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
                        </p>

                        <p>
                            Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante
                            convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet
                            ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac
                            habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.
                        </p>

                        <p>
                            Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a
                            libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae
                            tortor. Aliquam eu nunc.
                        </p>

                        <p>
                            Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra
                            rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.
                        </p>

                        <p class="mb-0">
                            Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget,
                            vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis,
                            dictum sed, iaculis a, condimentum nec, nisi.
                        </p>
                        <p>
                            Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis
                            tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris
                            ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt
                            non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
                        </p>

                        <p>
                            Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante
                            convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet
                            ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac
                            habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.
                        </p>

                        <p>
                            Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a
                            libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae
                            tortor. Aliquam eu nunc.
                        </p>

                        <p>
                            Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra
                            rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.
                        </p>

                        <p class="mb-0">
                            Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget,
                            vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis,
                            dictum sed, iaculis a, condimentum nec, nisi.
                        </p>


                    </v-card-text>
                </v-card>
            </v-tab-item>
            <v-tab-item>
                <v-card flat>
                    <v-card-text>
                        <p>
                            Fusce a quam. Phasellus nec sem in justo pellentesque facilisis. Nam eget dui. Proin
                            viverra, ligula sit amet ultrices semper, ligula arcu tristique sapien, a accumsan nisi
                            mauris ac eros. In dui magna, posuere eget, vestibulum et, tempor auctor, justo.
                        </p>

                        <p class="mb-0">
                            Cras sagittis. Phasellus nec sem in justo pellentesque facilisis. Proin sapien ipsum, porta
                            a, auctor quis, euismod ut, mi. Donec quam felis, ultricies nec, pellentesque eu, pretium
                            quis, sem. Nam at tortor in tellus interdum sagittis.
                        </p>
                    </v-card-text>
                </v-card>
            </v-tab-item>
            <v-tab-item>
                <Personal></Personal>
            </v-tab-item>
        </v-tabs>

        <div class="d-flex flex-column mb-6" :elevation="24"
        >
            <v-card
                    v-for="n in 3"
                    :key="n"
                    class="pa-2"
                    outlined
                    tile
            >
                Flex item {{ n }}
            </v-card>
        </div>
    </v-card>
</template>

<script>
    import Login from "./login";
    import Personal from "./personal"

    export default {
        components: {Login, Personal},
        data() {
            return {
                tab: null,
                items: [
                    '热门信件', '最新发布', '我要写信', '个人中心',
                ],
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
                isLogin: false,
                search: '',
            }
        },
    }
</script>

<style>
    /* Helper classes */
    .basil {
        background-color: #FFFBE6 !important;

    }

    .basil--text {
        color: #356859 !important;
    }

    a {
        text-decoration: none;
    }

    .router-link-active {
        text-decoration: none;
    }
</style>

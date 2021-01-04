<template>
    <v-card height="150">
        <v-footer
                absolute
                class="font-weight-medium"
        >
            <v-col
                    class="text-center"
                    cols="12"
            >
                {{ new Date().getFullYear() }} —— @easy&pluto product.
            </v-col>

        </v-footer>
    </v-card>
</template>

<script>
    export default {
        name:'cus_footer',
        data: () => ({
            icons: [
                'mdi-facebook',
                'mdi-twitter',
                'mdi-linkedin',
                'mdi-instagram',
            ],
        }),
    }
</script>
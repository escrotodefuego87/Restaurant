<template>
    <v-row justify="center">
        <v-dialog v-model="dialog" persistent max-width="300">
            <v-card>
                <v-card-title>
                    <span class="headline">Log in</span>
                </v-card-title>
                <v-card-text>
                   
                </v-card-text>
            </v-card>
        </v-dialog>
    </v-row>
</template>
<script>
export default {
    name: 'Login',
    data: () => ({
        dialog: true
    })
    
}
</script>

<template>
    <div>
        <v-toolbar 
            color="transparent" 
            class="ml-4">
            <v-col>
                <v-toolbar-title class="font-weight-bold">Profile Growth</v-toolbar-title>
                <span>Teste</span>
            </v-col>
            <v-btn-toggle 
                rounded="xl"
                color="indigo darken-2"
                elevation="1"
                class="mr-4"
            >
                <v-btn>Months</v-btn>
                <v-btn>Years</v-btn>
            </v-btn-toggle>
        </v-toolbar>
    </div>
</template>

<script>


    export default {
        name:"GraphicInicial"
    }

</script>

<style>

</style>
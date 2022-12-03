<template>
    <v-app-bar app elevation="0">
        <v-card
            width="400"
            class="ml-8"

            elevation="0"
        >
            <v-text-field
                id="text-field"
                density="compact"
                label="Search templates"
                append-inner-icon="mdi-magnify"
                single-line
                hide-details
            ></v-text-field>
        </v-card>
    </v-app-bar>
 </template>
 

<script>
    export default {
        name:"HeaderBar"
    }
</script>

<style>

.v-field{
    border-radius: 25px !important;
}

.v-field__outline{
    display: none !important;
}

</style>
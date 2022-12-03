<template>
    <v-navigation-drawer v-model="drawer" app color="indigo darken-2" mini-variant mini-variant-width="90">
        <v-avatar class="d-block text-center mx-auto mt-4 mb-4" size="80">
            <v-img 
                src="https://pt.freelogodesign.org/assets/img/logo-colors-meanings/logos-blancs/logo-apple.svg" 
                alt="logo"
            >
            </v-img>
        </v-avatar>
        <v-list >
            <v-list-item
                v-for="(item, i) in items"
                :key="i"
                :value="item"
                rounded="xl"
                class="mt-2 ml-4 mr-4"
            >
                <template v-slot:prepend>
                    <v-icon :icon="item.icon"></v-icon>
                </template>

                <v-list-item-title v-text="item.text"></v-list-item-title>
            </v-list-item>
        </v-list>
        <div style="position: absolute; bottom: 20px; margin-left: auto; margin-right: auto; left:0; right:0; text-align: center">
            <v-icon>mdi-exit-to-app</v-icon><br><span class="caption">Logout</span>
        </div>
    </v-navigation-drawer>
</template>

<script>
    export default {
        name:"SideBar",
        data(){
            return{
                selectedItem: 0,
                drawer: null,
                items: [
                    {icon:'mdi-home', text: 'Dashboard'},
                    {icon:'mdi-account', text: 'Profile'},
                    {icon:'mdi-message-reply-text', text: 'Messages'},
                    {icon:'mdi-google-analytics', text: 'Analytics'},
                    {icon:'mdi-cog-outline', text: 'Settings'},
                ],
            }
        }
    }
</script>

<style>


</style>
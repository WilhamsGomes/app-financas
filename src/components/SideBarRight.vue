<template>
    <v-navigation-drawer app location="right">
        <v-row>
            <v-col cols="12" sm="12">
                <v-list-item three-line  class="text-center ">
                    <v-avatar>
                        <v-img 
                            src="https://pt.freelogodesign.org/assets/img/logo-colors-meanings/logos-blancs/logo-apple.svg" 
                            alt="logo"
                        >
                        </v-img>
                    </v-avatar>
                    <v-list-item-content 
                        v-for="(item, i) in items" :key="i"
                        class="mt-8 d-flex align-center justify-space-around"
                    >
                        <div class="d-flex align-start flex-column">
                            <v-list-item-subtitle>
                            {{item.subtitle}}
                            </v-list-item-subtitle>
                            <v-list-item-title class="font-weight-bold">
                            R${{item.title}}
                            </v-list-item-title>
                        </div>
                        <v-avatar>
                            <v-icon color="indigo darken-2" size="35">mdi-arrow-right-bold-box</v-icon>
                        </v-avatar>
                    </v-list-item-content>
                    <v-divider class="mt-8"></v-divider>
                </v-list-item>
            </v-col>
        </v-row>
        <div class="mt-4 ml-8">Seu histórico</div>
        <v-timeline side="start" align="start">
            <v-timeline-item
                dot-color="indigo darken-2"
                size="small"
            >
                <div class="d-flex">
                    <strong class="mr-4">5pm</strong>
                    <div>
                    <strong>New Icon</strong>
                    <div class="text-caption">
                        Mobile App
                    </div>
                    </div>
                </div>
            </v-timeline-item>
            <v-timeline-item
                dot-color="indigo darken-2"
                size="small"
            >
                <div class="d-flex">
                    <strong class="mr-4">5pm</strong>
                    <div>
                    <strong>New Icon</strong>
                    <div class="text-caption">
                        Mobile App
                    </div>
                    </div>
                </div>
            </v-timeline-item>
        </v-timeline>
    </v-navigation-drawer>
</template>

<script>
    export default {
        name:"SideBarRight",
        data(){
            return{
                items:[
                    {subtitle: "Opção informada", title: 803.50 },
                    {subtitle: "Opção informada", title: 506.50 },
                    {subtitle: "Opção informada", title: 199.50 },
                ],
            }
        }
    }
</script>

<style>

.v-timeline--vertical.v-timeline{
    height: 0% !important;
}

</style>
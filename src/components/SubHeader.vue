<template>
    <v-container>
       <v-row>
            <v-col cols="12" sm="12" class="mx-auto d-flex flex-wrap">
                <v-card 
                    v-for="(item, index) in items"
                    :key="index"
                    class="mx-auto d-flex flex-wrap" 
                    width="200" 
                    elevation="0"
                >

                    <v-icon
                        icon="mdi-alarm"
                        size="30"
                        color="indigo darken-2"
                        class="mr-2"
                    ></v-icon>

                    <div>
                        <v-card-text class="px-0 pt-0 pb-0"> 
                            {{item.title}} 
                        </v-card-text>
                        <v-card-title class="px-0 pt-1 pb-0 text-h5 font-weight-bold"> 
                            {{item.values}} 
                        </v-card-title>  
                        <v-card-text class="px-0 pt-0 font-weight-bold text-caption"> 
                            {{item.percentage}}% 
                        </v-card-text>  
                    </div>
                </v-card> 
            </v-col>
       </v-row>
    </v-container>
</template>

<script>
    export default {
        name:"SubHeader",
        data: () => ({
            items:[
                {title: "Sessions", values: "24k", percentage:"+33.45"},
                {title: "Avg. Sessions", values: "00:18", percentage:"-112.45"},
                {title: "Bounce Rate", values: "$2400", percentage:"+62.10"},
                {title: "Avg. Watch time", values: "45.42", percentage:"+4.46"},
            ]
        }),
    }
</script>

<style>

</style>
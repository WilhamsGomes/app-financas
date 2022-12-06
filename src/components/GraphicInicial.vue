<template>
    <div>
        <v-toolbar 
            color="transparent" 
            class="ml-4">
            <v-col>
                <v-toolbar-title class="font-weight-bold">Profile Growth</v-toolbar-title>
                <span>Overall Information</span>
            </v-col>
            <v-btn-toggle 
                rounded="xl"
                color="indigo darken-2"
                elevation="1"
                class="mr-4"
            >
                <v-btn 
                    @click="selectedOption(1)"
                >
                Months
                </v-btn>
                <v-btn 
                    @click="selectedOption(2)"
                >
                Years
                </v-btn>
            </v-btn-toggle>
        </v-toolbar>
        <div id="chart">
            <apexchart type="bar" height="350" :options="chartOptions" :series="series">
            </apexchart>
        </div>
    </div>
</template>

<script>

    import VueApexCharts from 'vue3-apexcharts'

    export default {
        name:"GraphicInicial",
        components: {
          apexchart: VueApexCharts,
        },
        data() {
            return{
                series: [
                    {
                        name: 'Prohibited',
                        data: [44, 55, 57, 56, 61, 58, 63, 60, 66]
                    }, 
                    {
                        name: 'Exit',
                        data: [76, 85, 101, 98, 87, 105, 91, 114, 94]
                    }, 
                    {
                        name: 'Balance',
                        data: [35, 41, 36, 26, 45, 48, 52, 53, 41]
                    }
                ],
                chartOptions: {
                    chart: {
                        type: 'bar',
                        height: 350
                    },
                    plotOptions: {
                        bar: {
                            horizontal: false,
                            columnWidth: '55%',
                            endingShape: 'rounded'
                        },  
                    },
                    dataLabels: {
                        enabled: false
                    },
                    stroke: {
                        show: true,
                        width: 2,
                        colors: ['transparent']
                    },
                    xaxis: {
                        categories: ['Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct'],
                    },  
                    yaxis: {
                        title: {
                            text: 'Balance'
                        }
                    },
                    fill: {
                        opacity: 1
                    },
                    tooltip: {
                        y: {
                            formatter: function (val) {
                            return "$ " + val 
                            }
                        }
                    },
                    colors: ['#3F51B5', '#5C6BC0', '#7986CB']
                },
            }
        },

        methods: {

            selectedOption(option){      

                if (option == 1){

                    this.chartOptions = {...this.chartOptions, ...{
                        xaxis: {
                            categories: ['Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct']
                        }
                    }}

                    this.series = [
                        {
                            name: 'Prohibited',
                            data: [44, 55, 57, 56, 61, 58, 63, 60, 66]
                        }, 
                        {
                            name: 'Exit',
                            data: [76, 85, 101, 98, 87, 105, 91, 114, 94]
                        }, 
                        {
                            name: 'Balance',
                            data: [35, 41, 36, 26, 45, 48, 52, 53, 41]
                        }
                    ]

                } else if (option == 2){

                    this.chartOptions = {...this.chartOptions, ...{
                        xaxis: {
                            categories: [2013, 2012, 2014, 2015, 2016, 2017, 2018, 2019, 2020]
                        }
                    }}

                    this.series = [
                        {
                            name: 'Prohibited',
                            data: [10, 42, 52, 37, 53, 40, 12, 20, 48]
                        }, 
                        {
                            name: 'Exit',
                            data: [45, 58, 46, 82, 72, 82, 50, 13, 94]
                        }, 
                        {
                            name: 'Balance',
                            data: [41, 41, 48, 55, 35, 69, 53, 68, 82]
                        }
                    ]
                    
                }
                

            }
            
        }
    }

</script>

<style>

</style>
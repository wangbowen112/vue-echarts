<template>
    <div>
        <div id="main1" style="width: 600px;height:400px;"></div>
    </div>
</template>

<script>
    import echarts from "echarts"
    export default {
        data(){
            return {
                myChart:null,
                option:{}
            }
        },
        mounted(){
            this.myChart = echarts.init(document.getElementById('main1'))
            this.option = {
                legend: {},
                tooltip: {},
                dataset: {
                    source: [
                        ['product', '2015', '2016', '2017'],
                        ['Matcha Latte', 43.3, 85.8, 93.7],
                        ['Milk Tea', 83.1, 73.4, 55.1],
                        ['Cheese Cocoa', 86.4, 65.2, 82.5],
                        ['Walnut Brownie', 72.4, 53.9, 39.1]
                    ]
                },
                xAxis: {type: 'category'},
                yAxis: {},
                // Declare several bar series, each will be mapped
                // to a column of dataset.source by default.
                series: [
                    {type: 'bar'},
                    {type: 'bar'},
                    {type: 'bar'}
                ]
            };
            this.myChart.setOption(this.option)
        }
    }
</script>

<style scoped>

</style>
<template>
    <div>
        <div id="main2" style="width: 600px;height:400px;"></div>
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
            this.myChart = echarts.init(document.getElementById('main2'))
            this.option = {
                xAxis: {
                    type: 'category',
                    data: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']
                },
                yAxis: {
                    type: 'value'
                },
                series: [{
                    data: [820, 932, 901, 934, 1290, 1330, 1320],
                    type: 'line'
                }]
            }
            this.myChart.setOption(this.option)
        }
    }
</script>

<style scoped>

</style>
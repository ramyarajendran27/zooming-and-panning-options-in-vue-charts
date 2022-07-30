<template>
  <div id="app">
    <ejs-chart :primaryXAxis="chartPrimaryXAxis" :title="chartTitle"
    :primaryYAxis="chartPrimaryYAxis"
    :zoomSettings="chartZoomingOptions">
      <e-series-collection>
        <e-series type="Area" :dataSource="chartData" xName="period" yName="profit"
        width="2" opacity="0.25"></e-series>
      </e-series-collection>   
    </ejs-chart>
  </div>
</template>

<script>
import Vue from "vue";
import { ChartPlugin, AreaSeries, DateTime, Zoom, ScrollBar } from '@syncfusion/ej2-vue-charts';
Vue.use(ChartPlugin);

export default {
  provide : {chart : [AreaSeries, DateTime, Zoom, ScrollBar ]},
  data() {
    return {
      chartZoomingOptions : {
        enableSelectionZooming : true,
        toolbarItems : ['ZoomIn', 'ZoomOut', 'Reset'],
        enablePan : true,
        mode : 'XY',
        enableScrollbar: true, 
      },
      chartPrimaryYAxis : { title : 'Profit ($)' },
      chartTitle : 'Sales History of the Product',
      chartPrimaryXAxis : {
        valueType : 'DateTime',
        title : 'Years',
        enableAutoIntervalOnZooming : true,
        format : "yMMM"
      },
      chartData : [
        {period : new Date("2000, 02, 11"), profit : 14 },
        {period : new Date("2000, 09, 04"), profit : 20 },
        {period : new Date("2001, 02, 11"), profit : 25 },
        {period : new Date("2001, 09, 16"), profit : 21 },
        {period : new Date("2002, 02, 07"), profit : 13 },
        {period : new Date("2002, 09, 07"), profit : 18 },
        {period : new Date("2003, 02, 11"), profit : 24 },
        {period : new Date("2003, 09, 14"), profit : 23 },
        {period : new Date("2004, 02, 06"), profit : 19 },
        {period : new Date("2004, 09, 06"), profit : 31 },
        {period : new Date("2005, 02, 11"), profit : 39 },
        {period : new Date("2005, 09, 11"), profit : 50 },
        {period : new Date("2006, 02, 11"), profit : 24 },
        {period : new Date("2006, 09, 04"), profit : 16 },
        {period : new Date("2007, 02, 12"), profit : 22 },
        {period : new Date("2007, 09, 17"), profit : 18 },
        {period : new Date("2008, 02, 04"), profit : 10 },
        {period : new Date("2008, 09, 15"), profit : 15 },
        {period : new Date("2009, 02, 16"), profit : 19 },
        {period : new Date("2009, 09, 14"), profit : 21 },
        {period : new Date("2010, 02, 08"), profit : 33 },
        {period : new Date("2010, 09, 06"), profit : 28 },
        {period : new Date("2011, 02, 07"), profit : 40 },
        {period : new Date("2011, 09, 19"), profit : 35 },
        {period : new Date("2012, 02, 13"), profit : 20 },
        {period : new Date("2012, 09, 10"), profit : 30 },
        {period : new Date("2013, 02, 11"), profit : 36 },
        {period : new Date("2013, 09, 16"), profit : 45 },
        {period : new Date("2014, 02, 10"), profit : 27 },
        {period : new Date("2014, 09, 05"), profit : 12 },
        {period : new Date("2015, 02, 09"), profit : 38 },
        {period : new Date("2015, 09, 07"), profit : 14 },
        {period : new Date("2016, 02, 15"), profit : 23 },
        {period : new Date("2016, 09, 12"), profit : 19 },
        {period : new Date("2017, 02, 13"), profit : 11 },
        {period : new Date("2017, 09, 11"), profit : 16 },
        {period : new Date("2018, 02, 12"), profit : 26 },
        {period : new Date("2018, 09, 10"), profit : 29 },
        {period : new Date("2019, 02, 11"), profit : 43 },
        {period : new Date("2019, 09, 16"), profit : 30 },
        {period : new Date("2020, 02, 10"), profit : 32 },
        {period : new Date("2020, 09, 14"), profit : 48 },
        {period : new Date("2021, 02, 15"), profit : 31 },
        {period : new Date("2021, 09, 13"), profit : 50 }
      ]
    };
  }
}
</script>






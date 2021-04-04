<template>
    <div>
        <svg id="stream-graph">
            
        </svg>
    </div>
</template>

<script>
    import {select, extent, scaleLinear, scaleOrdinal, csv, stack, stackOffsetSilhouette } from 'd3';
    
    export default{
        name: "StreamGraph",
        created() {
            csv('https://raw.githubusercontent.com/isabelstoddart/NoisyPartiesNYC/main/data.csv')
            .then(data => {
                this.keys = data.columns.slice(1)
                this.domain = extent(data, function(d) {return d.month;})
            })},
      
       computed: {
        xScale() {
          return scaleLinear()
            .domain(this.domain)
            .range([0,this.width-350]);
        },
        yScale() {
          return scaleLinear()
            .domain([-3000,3000])
            .range([this.height, 0])
        },
        colors() {
        return scaleOrdinal()
          .domain(this.keys)
          .range(['#ff3155','#ffaf42','#ffed5e','#49f770','#2daefd'])
        },
        stack(){
        return stack()
          .offset(stackOffsetSilhouette)
          .keys(this.keys)
        }
       },
       
    mounted(){
     select("#stream-graph")
        .append("svg")
        .attr("width", this.width + this.margin.left + this.margin.right)
        .attr("height", this.height + this.margin.top + this.margin.bottom)
        .append("g")
            .attr("transform",
                "translate(" + this.margin.left + "," + this.margin.top + ")")
    }
    }
      
</script>
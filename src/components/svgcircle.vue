<template>
  <div>
    <svg :height="height" :width="width"> 
      <circle :cx="cx" :cy="cy" :r="radius" stroke="black" stroke-width="1" fill="#dbe7f5" />
      <text :x="x" :y="y" text-anchor="middle" fill="black">{{ text }}</text>
    </svg>
  </div>
</template>

<script>
export default {
  name: 'svgcircle',
  props: {
    text: String,
    radius: Number
  },
  created: function(){
    // Auto convert the radius into other required
    // SVG attributes

    // Use diameter to set svg height and width
    this.height = (this.radius * 2) + 7  // +7 margin to avoid distorted borders
    this.width = (this.radius * 2) + 7
    
    // Set the center of circle
    this.cx = this.radius + 3.5  // +3.5 adjustment due to margin
    this.cy = this.radius + 3.5
    
    // Set the center of the text
    this.x = this.radius
    this.y = this.radius
  }

  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

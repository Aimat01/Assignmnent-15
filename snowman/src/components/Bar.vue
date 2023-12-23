<template>
    <div>
      <canvas ref="chartRef"></canvas>
    </div>
  </template>
  
  <script>
  export default {
    mounted() {
      this.renderChart();
    },
    methods: {
      renderChart() {
        const ctx = this.$refs.chartRef.getContext('2d');
        new window.Chart(ctx, {
          type: 'bar',
          data: {
            labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
            datasets: [{
              label: 'Sample Bar Data',
              backgroundColor: '#3498db',
              data: [12, 19, 3, 5, 2, 3],
            }]
          },
          options: {}
        });
      }
    }
  }
  </script>
  
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
          type: 'pie',
          data: {
            labels: ['Red', 'Blue', 'Yellow'],
            datasets: [{
              data: [10, 20, 30],
              backgroundColor: ['#ff6384', '#36a2eb', '#ffce56'],
            }]
          },
          options: {}
        });
      }
    }
  }
  </script>
  
<script>
import { Line } from "vue-chartjs";

export default {
  name: 'AreaChart',
  extends: Line,
  data() {
    return {    
      gradient: null,
      gradient2: null,
      primaryColor: '#336CFB', //blue
    };
  },
  mounted() {
    this.gradient = this.$refs.canvas
      .getContext("2d")
      .createLinearGradient(100, 50, 80, 450);

    this.gradient.addColorStop(0, " rgba(51, 108, 251, 0.2)");
    this.gradient.addColorStop(0.5, "rgba(51, 108, 251, 0.02)");
    // this.gradient.addColorStop(1, "rgba(255, 0, 0, 0)");

    this.renderChart(
      {
        labels: [
          "1 July",
          "8 July",
          "16 July",
          "24 July",
          "31 July",

        ],
        datasets: [
          {
            label: "Income in current month",
            borderColor: this.primaryColor,
            pointBackgroundColor: "#A9C1FD",
            borderWidth: 2,
            pointBorderColor: "#fff",
            backgroundColor: this.gradient,
            data: [45500, 80000, 35000, 60000, 40000]
          }
        ]
      },
      { responsive: true, maintainAspectRatio: false }
    );
  }
};
</script>
<script>
import { Line } from "vue-chartjs";

export default {
  name: 'AreaChart',
  extends: Line,
  data() {
    return {    
      gradient2: null,
      secondaryColor: '#FAC032', //yellow
    };
  },
  mounted() {
    this.gradient2 = this.$refs.canvas
      .getContext("2d")
      .createLinearGradient(120, 40, 90, 350);
    this.gradient2.addColorStop(0, "rgba(250,192,50, 0.2)");
    this.gradient2.addColorStop(0.5, "rgba(241,241,241, 0.02)");
    // this.gradient2.addColorStop(0, "rgba(0, 231, 255, 0.9)");
    // this.gradient2.addColorStop(0.5, "rgba(0, 231, 255, 0.25)");
    // this.gradient2.addColorStop(1, "rgba(0, 231, 255, 0)");

    this.renderChart(
      {
        labels: [
          "25 July",
          "26 July",
          "27 July",
          "28 July",
          "29 July",
          "30 July",
          "31 July",
        ],
        datasets: [
          {
            label: "Income in current week",
            borderColor: this.secondaryColor,
            pointBackgroundColor: "#FCDF98",
            pointBorderColor: "white",
            borderWidth: 2,
            backgroundColor: this.gradient2,
            data: [61000, 35000, 49000, 40000, 68000, 19000, 50000 ]
          }
        ]
      },
      { responsive: true, maintainAspectRatio: false }
    );
  }
};
</script>
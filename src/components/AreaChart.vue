<script>
import { Line } from "vue-chartjs";

export default {
  name: 'AreaChart',
  extends: Line,
  data() {
    return {    
      gradient: null,
      gradient2: null,
      primaryColor: '#336CFB', //bue
      secondaryColor: '#FAC032', //yellow
    };
  },
  mounted() {
    this.gradient = this.$refs.canvas
      .getContext("2d")
      .createLinearGradient(100, 50, 80, 450);
    this.gradient2 = this.$refs.canvas
      .getContext("2d")
      .createLinearGradient(120, 40, 90, 350);

    this.gradient.addColorStop(0, " rgba(51, 108, 251, 0.2)");
    this.gradient.addColorStop(0.5, "rgba(51, 108, 251, 0.02)");
    // this.gradient.addColorStop(1, "rgba(255, 0, 0, 0)");

    this.gradient2.addColorStop(0, "rgba(250,192,50, 0.2)");
    this.gradient2.addColorStop(0.5, "rgba(241,241,241, 0.02)");
    // this.gradient2.addColorStop(0, "rgba(0, 231, 255, 0.9)");
    // this.gradient2.addColorStop(0.5, "rgba(0, 231, 255, 0.25)");
    // this.gradient2.addColorStop(1, "rgba(0, 231, 255, 0)");

    this.renderChart(
      {
        labels: [
          "2020-1",
          "2020-2",
          "2020-3",
          "2020-4",
          "2020-5",
          "2020-6",
          "2020-7",
          "2020-8",
          "2020-9",
          "2020-10",
          "2020-11",
          "2020-12",
        ],
        datasets: [
          {
            label: "Patients 2019",
            borderColor: this.primaryColor,
            pointBackgroundColor: "white",
            borderWidth: 2,
            pointBorderColor: "white",
            backgroundColor: this.gradient,
            data: [145, 110, 200, 150, 150, 140, 180, 170, 140, 210, 175, 300]
          },
          {
            label: "Patients 2020",
            borderColor: this.secondaryColor,
            pointBackgroundColor: "white",
            pointBorderColor: "white",
            borderWidth: 2,
            backgroundColor: this.gradient2,
            data: [50, 120, 90, 160, 105, 155, 130, 180, 95, 90, 185, 187]
          }
        ]
      },
      { responsive: true, maintainAspectRatio: false }
    );
  }
};
</script>
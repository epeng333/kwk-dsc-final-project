<script>
//   import * as Highcharts from "highcharts";
//   import "highcharts/modules/exporting";
//   import { Chart } from "@highcharts/svelte";
  import Scroller from "../lib/Scroller.svelte";
  import ArticleText from "../lib/ArticleText.svelte";

//   const series = [
//     {
//       name: "Group 1",
//       data: [
//         [1990, 3],
//         [2000, 4],
//         [2010, 1],
//         [2020, 1],
//       ],
//       color: "#8427c9",
//     },
//     {
//       name: "Group 2",
//       data: [
//         [1990, 2],
//         [2000, 5],
//         [2010, -2],
//         [2020, 2],
//       ],
//       color: "#ff99fc",
//     },
//     {
//       name: "Group 3",
//       data: [
//         [1990, 4],
//         [2000, 3],
//         [2010, 0],
//         [2020, 3],
//       ],
//       color: "#4096fa",
//     },
//   ];

//   let chart;
//   let thirdSeriesVisible = false;

//   let options = {
//     chart: {
//       type: "spline",
//       backgroundColor: "#e3ff00",
//       borderColor: "#007052",
//       borderWidth: 5,
//       borderRadius: 20,
//     },
//     title: {
//       text: "Another Example Chart",
//     },
//     subtitle: {
//       text: "With a subtitle! And styling!",
//     },
//     series: [series[0], series[1]],
//   };

//   function toggleThirdSeries() {
//     const existingSeries = chart.series.find((s) => s.name === "Group 3");

//     if (existingSeries) {
//       existingSeries.remove();
//       thirdSeriesVisible = false;
//     } else {
//       chart.addSeries(series[2]);
//       thirdSeriesVisible = true;
//     }
//   }
</script>

<div>
  <Scroller layout="left">
    {#snippet sticky()}
      <h2>Building Black Wealth</h2>

      <!-- Data graphic 15  -->
      <img
        class="ladder-wealth-building-img"
        src="ladder-wealth-building.png"
        alt="Ladder Wealth Building"
      />

      <p>
        Laddered Path to Wealth Building from the <a
          href="https://chiul.org/wp-content/uploads/2025/06/Final-SOBC-2025-Full-Report-1.pdf"
          >2025 State of Black Chicago report</a
        >.
      </p>

      <p>
        The wealth of available information, data, research insights, and
        actionable strategies in this report as well as other sources can serve
        as a helpful foundation and springboard for Black individuals looking to
        increase their wealth and improve their financial well-being.
      </p>
    {/snippet}

    <!-- {#snippet sticky()}
    <div class="chart">
        <Chart bind:chart {options} highcharts={Highcharts} />
      </div>
      <button on:click={toggleThirdSeries} class="toggle-button">
        {thirdSeriesVisible ? "Remove Group 3" : "Add Group 3"}
      </button>
      <div>
        <p>
          You can use Svelte to add and remove data from a Highcharts chart.
        </p>
        <p>
          When you click the button above, a third group is toggled in the
          chart. Check out the source code to see how it's done.
        </p>
        <p>
          <strong
            >🤔 How might you use other HTML elements, like checkboxes or radio
            buttons, in a similar way to filter data?</strong
          >
        </p>
      </div>
    {/snippet} -->

    {#snippet scrolly()}
      <ArticleText>
        Organizations such as the <a href="https://blackwealthdata.org/about-us"
          >Black Wealth Data Center</a
        >
        and the <a href="https://www.urban.org/">Urban Institute</a> have created
        databases, conducted research, and published their findings to help provide
        accessible information and solutions to help Black people increase their
        wealth and improve their financial well-being.
      </ArticleText>

      <ArticleText>
        The <a href="https://thechicagourbanleague.org/">Chicago Urban League</a
        >
        has released the
        <a
          href="https://thechicagourbanleague.org/2025/05/08/chicago-urban-league-releases-2025-state-of-black-chicago-report/"
          >2025 State of Black Chicago report</a
        >
        titled <i>A Laddered Path to Wealth Building</i> that identifies wealth contributors
        and provides a five-step ladder, collaborative solutions, and policy recommendations
        to aid Black individuals increase their wealth.
      </ArticleText>

      <ArticleText>
        According to the report, factors such as education, entrepreneurship,
        homeownership, workforce development, civic engagement, justice, and
        health contribute to wealth.
      </ArticleText>

      <ArticleText>
        The <a
          href="https://chiul.org/wp-content/uploads/2025/06/Final-SOBC-2025-Full-Report-1.pdf"
          >full report</a
        >
        contains a ladder with five steps to build wealth (from bottom of the ladder
        to top of the ladder):<br />
        <br />
        1. <strong>Money Mindfulness</strong>: Cultivating a growth-focused
        relationship to money<br />
        2. <strong>Stable Security</strong>: Fulfilling basic financial needs<br
        />
        3. <strong>Compounding Interest</strong>: Exploring investment pathways<br
        />
        4. <strong>Community Prosperity</strong>: Building wealth with others<br
        />
        5. <strong>Long-Term Growth</strong>: Achieving generational wealth<br
        />
      </ArticleText>

      <ArticleText>
        The report also presents <a
          href="https://chiul.org/wp-content/uploads/2025/05/FINAL-2025-SOBC-Executive-Summary-1.pdf"
          >policy recommendations</a
        >, including:<br />
        <br />
        1. Support Small Business Owners<br />
        2. Support Workforce and Wage Growth<br />
        3. Support Homeownership<br />
        4. Strengthen Education<br />
        5. Invest in Health Equity<br />
        6. Support Civil Engagement<br />
        7. Support Community Safety<br />
      </ArticleText>

      <!-- <ArticleText>
        You might notice that this basic template doesn't have certain features
        that are common in scrollytelling.
      </ArticleText>

      <ArticleText>
        For example, you might want a component that doesn't feature a sticky
        component at all. Or a component that is solely a sticky component.
      </ArticleText>

      <ArticleText>
        You might also want to add more interactivity or gamify parts of your
        scrollytelling piece.
      </ArticleText>

      <ArticleText>
        <strong>
          It's up to you to research how to create the effects and functionality
          that you envision!
        </strong>
      </ArticleText> -->
    {/snippet}
  </Scroller>
</div>

<style>
  .ladder-wealth-building-img {
    width: 100%;
    margin: 0px auto;
  }

  /* .chart {
    width: 90%;
    margin: 0px auto;
  }

  .toggle-button {
    margin: 20px;
    padding: 20px;
    color: #007052;
    background-color: #0bd956;
    border: solid 2px #007052;
    border-radius: 16px;
    font-size: large;
    cursor: pointer;
    transition: all 0.2s ease;
    box-shadow: 0 4px 0 #007052;
  }

  .toggle-button:active {
    transform: translateY(2px);
    box-shadow: 0 2px 0 #007052;
  } */
</style>

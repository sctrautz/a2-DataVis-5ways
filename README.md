# Assignment 2 - Data Visualization, 5 Ways  


## JavaScript + D3

I built the scatterplot in the browser with SVG. It was easy to map color and size after the scales were set, but the harder part was loading the CSV asynchronously and keeping ticks consistent while adding hover. I could see d3 being useful when you need custom interactions on the web. The main workaround was manually setting domains and tick values to match the reference.

<img src="img/d3-new.png" alt="d3" width="600">

## R + ggplot2

ggplot2 made the basic chart quick to build using aesthetics for x, y, color, and size. The harder part was tuning axis limits and tick breaks to match the non‑zero scales. I could see ggplot2 being useful for quick, clean plots in reports or papers. I limited bill length to a fixed range for consistent sizing and set explicit scale breaks to match the reference.

<img src="img/r-ggplot2.png" alt="d3" width="600">

## Python + Altair

Altair’s declarative style made the encodings easy to set. The hardest part was matching axis domains and tick values. I could see Altair being useful for quick interactive prototypes. The hover highlight and tooltip were easy to add. The main tweak was setting explicit domains and tick values.

<img src="img/altair.png" alt="d3" width="600">

## JSON + Vega-Lite

Vega‑Lite is compact and maps directly to the encodings. Gridlines and legends were easy, but matching axis domains and tick values took more effort. I could see Vega‑Lite being useful when you want a small, portable spec that can render in different places. The main tweak was setting explicit tick values for 1000‑unit steps, plus a simple hover selection for interaction.

<img src="img/vega.png" alt="d3" width="600">

## Python + Plotly

Plotly made a polished chart quickly. Setting ranges, gridlines, and colors was easy; matching tick spacing and the legend layout took more work. I could see Plotly being useful for dashboards. The main adjustment was nudging margins and the legend position to avoid clipping.

<img src="img/plotly.png" alt="d3" width="600">


## Technical Achievements
- **Hover interactions**: Built tooltips + hover highlights in d3, Altair, and Vega‑Lite so you can inspect values without changing the chart.
- **Explicit scales**: Set non‑zero domains and tick values in each tool to mirror the reference chart.
- **Data cleaning**: Filtered out rows with missing values so only valid points were plotted.

### Design Achievements
- **Shared visual language**: Kept the same species colors and size range across all tools so the charts read the same.
- **Custom fonts**: Applied a custom font in the web‑based charts to keep labels and legends consistent.
- **Legend + grid consistency**: Kept legends and gridlines consistent across all visualizations.

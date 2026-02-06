# Assignment 2 - Data Visualization, 5 Ways  


## JavaScript + D3

I used d3 to build the scatterplot directly in the browser with an SVG. It was easy to map color and size once the scales were set up, but the harder part was handling async CSV loading and keeping ticks consistent while adding hover behavior. I could see d3 being best for highly customized, interactive visualizations on the web. The main “hack” was manually tuning domains/ticks to align with the reference.

<img src="img/d3-new.png" alt="d3" width="600">

## R + ggplot2

ggplot2 made the visual mapping straightforward using aesthetics for x, y, color, and size. It was easy to get a clean baseline chart, while the more difficult part was tuning axis limits and tick breaks to match the non‑zero scales. ggplot2 feels ideal for quick, publication‑style plots. I did clamp bill length for consistent sizing and used explicit scale breaks to match the reference.

<img src="img/r-ggplot2.png" alt="d3" width="600">

## Python + Altair

Altair’s declarative syntax made it easy to replicate the scatterplot with the right encodings. The toughest part was matching axis domains and tick values, but once that was set the rest was simple. I’d use Altair for rapid, interactive prototypes; the hover highlight + tooltip were easy to add. The only real tweak was explicit domain/tick control.

<img src="img/altair.png" alt="d3" width="600">

## JSON + Vega-Lite

Vega‑Lite was approachable because the spec is compact and mirrors the visual encodings directly. It was easy to add gridlines and legends, but I had to be precise about axis domains and tick values to match the rubric. I can see Vega‑Lite being useful for portable, declarative specs that render anywhere. The only “hack” was setting explicit tick values to enforce 1000‑unit steps, plus a simple hover selection for interaction.

<img src="img/vega.png" alt="d3" width="600">

## Python + Plotly

Plotly was straightforward for quick charts with polished defaults. It was easy to set ranges, gridlines, and consistent colors; the tricky part was getting tick spacing and legend layout to match the other tools. I’d use Plotly for dashboards or rapid sharing. The main adjustment was nudging margins and the legend position to avoid label clipping.

<img src="img/plotly.png" alt="d3" width="600">


## Technical Achievements
- **Hover interactions**: Built tooltips + hover highlights in d3, Altair, and Vega‑Lite so you can inspect values without changing the chart.
- **Explicit scales**: Set non‑zero domains and tick values in each tool to mirror the reference chart.
- **Data cleaning**: Filtered out rows with missing values so only valid points were plotted.

### Design Achievements
- **Shared visual language**: Kept the same species colors and size range across all tools so the charts read the same.
- **Custom fonts**: Applied a custom font in the web‑based charts to keep labels and legends consistent.
- **Legend + grid consistency**: Kept legends and gridlines consistent across all visualizations.

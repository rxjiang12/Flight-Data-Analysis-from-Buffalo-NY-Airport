# Analysis of Flight Data from Buffalo Niagara International Airport (BUF)

An analysis of one month of flight activity at BUF, combining 30 days of raw JSON records into a single dataset to find where delays and cancellations actually concentrate — by airline, destination, gate, and date.

**[Read the full case study →](https://ranxinjiang.github.io/project-buffalo-flights.html)**

A collaborative academic project by **Anna Bold, Kossi Gamli, Ran Xin Jiang, and Christina Pratas**.

---

## The Problem

Airports and airlines manage scheduling constraints, gate availability, weather, and flight volume simultaneously. When something slips, it isn't obvious which factor is responsible or where the delay concentrates. Without structured analysis there's no way to say whether delays are spread evenly across operations or driven by a small number of gates, routes, or days.

## The Data

Thirty JSON files covering daily flight activity at BUF throughout **January 2025**. Each record contains:

- Scheduled and actual departure times
- Scheduled and actual arrival times
- Airline carrier
- Destination airport
- Aircraft information
- Gate assignment
- Delay and cancellation indicators

Combined into a single dataset of **5,509 flights**, of which **4,145** carried usable departure delay data.

## Method

**Data preparation** — loaded and combined the 30 daily JSON files, handled missing values and inconsistent formatting, standardized scheduled and actual time fields, derived departure and arrival delay metrics, and created a cancellation flag.

**Analysis** — grouped aggregations across airline, destination airport, departure gate, and date of operation, evaluating average and median delay, 90th-percentile delay, and cancellation frequency.

**Visualization** — four charts covering daily cancellation rate, gate-level departure delay, and destination-level arrival delay and cancellation rate.

## Findings

**Flights leave late and arrive early.** The average departure ran **27.3 minutes behind schedule** (median 20 minutes), with the slowest tenth leaving more than an hour late. Yet the average arrival came in **10.9 minutes early** (median 14 minutes early).

That gap is schedule padding — carriers build slack into block times, so a late pushback frequently still produces an on-time landing. It also means departure delay overstates the passenger-facing problem, since most lost time is recovered in the air.

**Delays are common but modest.** By the DOT's 15-minute standard, **45% of flights were delayed** — 2,479 of 5,509.

**Cancellations are rare and clustered.** Only **53 flights** cancelled across the month, under 1% of activity. They concentrate on a handful of dates rather than spreading evenly, which is the signature of weather events rather than chronic operational failure.

**Some gates and destinations carry more delay than others.** Grouping by departure gate surfaced a wide spread, pointing at ground operations and turnaround rather than anything in the air. A small number of destinations accounted for a disproportionate share of arrival delay, and a separate small set drove most cancellations.

## Repository Contents

| File | Description |
|---|---|
| `buffalo_flight_analysis.ipynb` | The full analysis — data preparation, aggregations, and visualizations |
| `BUF_1.json` – `BUF_30.json` | Raw daily flight records, January 2025 |
| `Ran Xin Jiang's Individual Contributions.md` | Breakdown of individual work on the project |

## Running It

1. Clone or download this repository.
2. Ensure Python is installed along with Pandas, NumPy, and Matplotlib.
3. Open `buffalo_flight_analysis.ipynb` in Jupyter or another notebook environment.
4. Run the cells in order to reproduce the data preparation, analysis, and charts.

The notebook reads the JSON files from the repository root, so no additional setup is required.

## Limitations

- The analysis covers a single month, so seasonal patterns can't be separated from January-specific weather.
- External factors — weather data in particular — were not incorporated, which limits how far the cancellation clustering can be explained.
- The dataset contains no information on airline staffing or aircraft maintenance, both plausible drivers of the delays observed.

## Built With

Python · Pandas · NumPy · Matplotlib · Jupyter

# Analyzing Fuel Sources of US Electric Utilities and Independent Power Producers - Data Science Portfolio Project

## Project Overview:

This project focuses on using Python to explore and analyze the coal, hydroelectric, natural gas, and nuclear fuel sources of each state’s electric utilities and independent power producers (IPPs), with the goal of answering the following questions:

- Which states’ utilities and IPPs have the highest summer capacity from coal, hydroelectric, natural gas, and nuclear sources?
- Which states’ utilities and IPPs rely most heavily on each of these four fuel sources, measured as a percentage of all sources?
- What other notable patterns appear in the fuel mix?

The project code and results are contained in the Jupyter Notebook `fuel_sources-Copy1.ipynb`, with a summary of the conclusions below.

## Data:

The data used in this project is stored in a single CSV file:

- `capacity_csv.csv` contains 57,778 rows and 8 columns of annual electric generator capacity by year (1990–2025), state, producer type, and fuel source, including generators, facilities, nameplate capacity, and summer capacity (in megawatts). This analysis uses 2025 data for the electric utilities and independent power producers.

## Credit:

The data was obtained from the U.S. Energy Information Administration (file: `existcapacity_annual.xls`) using the following link:

- <https://www.eia.gov/electricity/data/state/>

## Conclusion:

In summary, this project provides insight into how the fuel mix of electric utilities and IPPs differs across the United States. Here are some key findings from the analysis (2025 summer capacity; each entry is a state and producer type, and “%” is the share of that group’s all-sources summer capacity):

**Top 5 by summer capacity**

- **Coal:** Indiana utilities (12,127 MW), West Virginia utilities (10,425 MW), Texas IPPs (10,260 MW), Kentucky utilities (8,631 MW), Missouri utilities (8,553 MW)
- **Hydroelectric:** Washington utilities (21,415 MW), California utilities (9,670 MW), Oregon utilities (8,215 MW), New York utilities (3,531 MW), Alabama utilities (3,291 MW)
- **Natural gas:** Florida utilities (46,602 MW), Texas IPPs (35,656 MW), Pennsylvania IPPs (25,984 MW), Texas utilities (23,761 MW), California IPPs (19,744 MW)
- **Nuclear:** Illinois IPPs (11,596 MW), Pennsylvania IPPs (9,896 MW), South Carolina utilities (6,646 MW), Georgia utilities (6,289 MW), Alabama utilities (5,453 MW)

**Top 5 by percentage of all sources**

- **Coal:** West Virginia utilities (94.4%), Indiana utilities (59.1%), Wyoming utilities (53.6%), North Dakota utilities (52.2%), West Virginia IPPs (51.8%)
- **Hydroelectric:** Maine utilities (100.0%), New Hampshire utilities (100.0%), Washington utilities (79.7%), Oregon utilities (73.1%), Montana utilities (71.8%)
- **Natural gas:** Delaware utilities (96.2%), Maryland utilities (92.7%), Delaware IPPs (90.7%), Alabama IPPs (89.2%), Mississippi utilities (81.8%)
- **Nuclear:** Wisconsin IPPs (65.9%), South Carolina utilities (30.8%), New Hampshire IPPs (29.0%), Illinois IPPs (26.9%), Tennessee utilities (23.4%)

**Other facts of interest**

- Only two states use 100% hydroelectric as a fuel source: New Hampshire and Maine (both utilities, though with very small capacities of 5.1 MW and 1.2 MW)
- West Virginia utilities are the most coal-dependent group at 94.4% of summer capacity, while Indiana utilities have the highest coal capacity
- Washington utilities have by far the most hydroelectric capacity (21,415 MW), roughly 80% of their total
- Florida utilities have the largest natural gas capacity (46,602 MW), while Delaware utilities have the highest gas share (96.2%)
- Wisconsin IPPs rely on nuclear power the most (65.9% of capacity), while Illinois IPPs have the largest nuclear capacity (11,596 MW)

There are a couple of caveats to these conclusions that we can address in future analyses which include:

- summer capacity measures the ability to generate power, not actual electricity generated
- percentage rankings can be dominated by groups with very small total capacity (e.g., Delaware utilities, New Hampshire and Maine hydroelectric)
- a state can appear more than once because utilities and IPPs are ranked separately, and other producer types (e.g., commercial, industrial) are excluded
- changes over time, since only 2025 is analyzed although the data runs from 1990

## Python Version and Library Dependencies

- Python (3.14)
- numpy
- pandas

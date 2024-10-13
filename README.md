# Airbnb Data Analysis - Pricing and Guest Satisfaction

## Project Overview
This project aims to analyze Airbnb data from various cities in Europe to better understand how factors such as price, guest satisfaction, room type, and host characteristics impact rental prices. Additionally, this project explores pricing strategies using economic models like Cournot competition and employs machine learning models to predict optimal prices and guest satisfaction levels.

## Key Features

1. **Data Loading & Preprocessing**
   - The project loads data from multiple CSV files containing Airbnb listings from different cities.
   - Data from both weekdays and weekends are combined for each city, with additional columns created to distinguish between cities and weekend/weekday records.

2. **Exploratory Data Analysis (EDA)**
   - Visualizations are used to explore relationships between price, guest satisfaction, room types, and cities.
   - A heatmap is used to show correlations between numerical variables such as price, distance to city center, and guest satisfaction.

3. **Pricing Models**
   - The project uses Cournot competition theory to estimate optimal prices by analyzing neighborhood-level price competition.
   - Real vs. optimal prices are compared for each listing.

4. **Statistical Tests**
   - A Mann-Whitney U test is applied to compare guest satisfaction between superhosts and non-superhosts, identifying any statistically significant differences.

5. **Machine Learning Models**
   - Linear regression and Random Forest models are employed to predict rental prices based on features like guest satisfaction, distance to city center, and room capacity.
   - Feature importance is analyzed to identify which factors influence rental prices the most.

6. **Weekend Premium Analysis**
   - The average price premium for weekends vs. weekdays is calculated and visualized for each city.

7. **Game Theory Simulation**
   - A simplified game theory model simulates host competition where hosts choose price and quality to maximize profit. Demand and customer satisfaction are modeled as functions of price and quality.

## Theory Used

### Cournot Competition
The Cournot competition model is an economic theory that describes the behavior of firms in an oligopoly setting, where firms compete on the quantity of output produced. In this project, we adapt this model to represent the pricing competition between Airbnb hosts in the same neighborhood. Each host chooses a rental price, considering the prices of neighboring listings, and attempts to maximize profit. The Cournot model helps us estimate the "optimal" price where each host balances their own interests with the competitive pressure from others.

### Game Theory & Nash Equilibrium
In our game theory simulation, each Airbnb host is modeled as a player in a game where they choose both the price and quality of their listing. The objective is to maximize profit by balancing price, quality, and the level of competition in their market. The Nash Equilibrium is used to determine the point where no host can improve their profit by unilaterally changing their pricing or quality level, given the strategies of others.

### Statistical Tests
The Mann-Whitney U test, a non-parametric test, is used to compare guest satisfaction scores between two groups: superhosts and non-superhosts. This test helps determine whether the observed differences in guest satisfaction are statistically significant or if they could have occurred by chance.

## Project Structure

- **Data Files**: Multiple CSV files containing Airbnb listings data for different cities and for weekdays and weekends.
- **Main Script**: The core script that loads, preprocesses, analyzes, and models the data.
- **Visualizations**: Graphs and charts that visualize price distributions, correlations, and other key insights.
- **Machine Learning Models**: Predictive models used to estimate optimal pricing and analyze the importance of various features.
- **Statistical Tests**: Tests conducted to check if host characteristics (e.g., superhost status) significantly impact guest satisfaction.

## Getting Started

### Prerequisites
- Python 3.x
- Libraries:
  - `pandas`
  - `numpy`
  - `seaborn`
  - `matplotlib`
  - `scikit-learn`
  - `xgboost`
  - `scipy`

You can install the necessary libraries using:
```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost scipy
```

### Running the Project
1. Clone this repository.
2. Place the provided CSV files in the appropriate folder.
3. Run the main Python script to execute the analysis, generate visualizations, and see model outputs.

## Key Insights

- Room type and location significantly influence Airbnb prices.
- Superhosts generally offer a higher level of guest satisfaction compared to non-superhosts.
- Prices tend to increase on weekends across cities, with some cities showing a larger price premium than others.
- The Cournot competition model can effectively estimate optimal pricing based on neighborhood competition.

## Future Work

- Extend the pricing model to consider seasonal factors and events in cities.
- Explore additional machine learning models to improve price predictions.
- Incorporate more data sources to further enhance the analysis of guest satisfaction and pricing dynamics.

## License
This project is licensed under the MIT License.

## Contact
If you have any questions or suggestions, feel free to contact the project maintainer:
- **Name**: Moussaab
- **Email**: moussaaboualijane@gmail.com

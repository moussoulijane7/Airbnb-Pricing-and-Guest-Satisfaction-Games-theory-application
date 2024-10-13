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


This project models the competition between hosts on a short-term rental platform like Airbnb, using game theory. The goal is to simulate various scenarios where hosts choose their prices and service quality to reach a Nash equilibrium.

### Description of the Game Flow to Understand Game Theory

Imagine you are the owner of a house or apartment that you want to rent out on a platform like Airbnb. You are not the only one: several other hosts in the same city are also trying to attract customers. Each of you must make several strategic decisions:

1. **Set a Price**: Each host must choose the price at which they want to rent their property. You do not know in advance what price other hosts will set.

2. **Offer Service Quality**: In addition to the price, each host offers a certain level of service quality. For example, if you are a *superhost*, it means you have positive reviews, and clients are willing to pay a little more to stay with you. The quality can be either high or standard.

#### Steps of the Game

1. **Hosts Choose Strategies**: Each host chooses a price and decides whether to offer high service quality (*superhost*) or standard quality.

2. **Client Demand**: Clients look at the different prices and qualities offered by hosts. They will choose where to stay based on two main factors:
   - Price: A lower price attracts more clients.
   - Quality: Clients prefer to stay with *superhosts* or in higher-quality properties, even if it costs a little more.

3. **Client Distribution**: Clients are distributed among the different hosts. If a host offers a better value for money, they will attract more clients.

4. **Hosts’ Revenue Calculation**: Once each host has attracted a certain number of clients, their revenue is calculated. Revenue depends on the number of clients they have attracted, multiplied by the rental price, minus the cost of service quality.

5. **Client Satisfaction**: Clients who paid a low price for good service quality will be more satisfied than those who paid a higher price for lower quality.

#### Objective of the Game

The goal for each host is to attract as many clients as possible while maximizing their revenue. To do this, each host must find a balance between:
   - Setting a competitive price (not too high to avoid losing clients, but not too low to avoid losing money).
   - Offering a sufficient level of service quality to attract clients (e.g., by becoming a *superhost*).

#### The Concept of Equilibrium (Nash Equilibrium)

At the end of the game, all hosts have adjusted their strategies (price and quality) in response to the choices of other hosts. An **equilibrium** is reached when no host has any incentive to change their strategy (price or quality), because they would earn less by making changes. This is called a **Nash Equilibrium**.

#### Concrete Example in This Game

- If a host sets a very low price, they will attract more clients but risk earning less money.
- If another host offers high quality (like *superhost*), they can charge a higher price and attract clients looking for good quality, but it will also cost them more.
- If two hosts offer similar services, they will need to adjust their prices to avoid losing clients. This is how competition drives prices to stabilize around a certain point.

#### Conclusion

This game shows how, in a competitive market like short-term rentals, hosts must make decisions based on what others are doing. They adjust their prices and service quality to maximize their revenue while trying to attract clients amid the competition.



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



## Contact
If you have any questions or suggestions, feel free to contact the project maintainer:
- **Name**: Moussaab
- **Email**: moussaaboualijane@gmail.com

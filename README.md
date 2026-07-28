# Experiment 1: EDA in IPL Dataset
## Name: V.YASWANTH
## Register number: 212225220125
## Aim:
To perform Exploratory Data Analysis (EDA) on the IPL matches dataset and derive insights about matches per season, winning teams, toss decisions, and top venues.

## Algorithm / Procedure:

### 1.Import Libraries
  Import pandas for data handling.
  Import matplotlib and seaborn for visualization.
### 2.Load Dataset
  Use pd.read_csv() to load the IPL matches dataset.
  Check dataset shape using .shape.
  View first 5 rows using .head().
### 3.Matches per Season (Univariate Analysis)
  Group data by season and count matches.
  Plot a bar chart to visualize growth/decline in matches.
### 4.Top Winning Teams (Univariate Analysis)
  Use value_counts() on the winner column.
  Plot top 5 winning teams in a bar chart.
### 5.Toss Decisions (Univariate Analysis)
  Count toss decision preferences (bat vs field).
  Plot results using a bar chart.
### 6.Top Venues (Univariate Analysis)
  Count matches per venue.
  Display top 5 venues with a horizontal bar chart.
### 7.Draw Insights
  Observe patterns in toss decisions.
  Identify teams with consistent winning trends.
  
## Program
  
  #### Basic info about dataset:
```
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load dataset
df = pd.read_csv("matches.csv")

# Display dataset information
print("Dataset Shape:", df.shape)

print("\nFirst 5 Rows:")
print(df.head())
```
#### Matches Per Season
```
matches_per_season = df['season'].value_counts().sort_index()

print(matches_per_season)

plt.figure(figsize=(10,5))
matches_per_season.plot(kind='bar', color='skyblue')

plt.title("Matches Per Season")
plt.xlabel("Season")
plt.ylabel("Number of Matches")

plt.xticks(rotation=45)
plt.grid(axis='y', linestyle='--', alpha=0.7)

plt.show()
```
#### Top Winning Teams
```
top_teams = df['winner'].value_counts().head(5)

print("\nTop 5 Winning Teams:")
print(top_teams)

plt.figure(figsize=(10,5))
top_teams.plot(kind='bar', color='lightgreen')

plt.title("Top 5 Winning Teams")
plt.xlabel("Team")
plt.ylabel("Number of Wins")

plt.xticks(rotation=20)
plt.grid(axis='y', linestyle='--', alpha=0.7)

plt.show()
```

#### Toss Decisions
```toss_decision = df['toss_decision'].value_counts()

print("\nToss Decisions:")
print(toss_decision)

plt.figure(figsize=(6,5))
toss_decision.plot(kind='bar', color='orange')

plt.title("Toss Decisions")
plt.xlabel("Decision")
plt.ylabel("Count")

plt.grid(axis='y', linestyle='--', alpha=0.7)

plt.show()
```
#### Top Venues
```
top_venues = df['venue'].value_counts().head(5)

print("\nTop 5 Venues:")
print(top_venues)

plt.figure(figsize=(10,5))
top_venues.plot(kind='barh', color='violet')

plt.title("Top 5 Venues")
plt.xlabel("Number of Matches")
plt.ylabel("Venue")

plt.grid(axis='x', linestyle='--', alpha=0.7)
plt.show()
plt.grid(axis='x', linestyle='--', alpha=0.7)
plt.show()
```

#### Insights
```
print("\nINSIGHTS")
print("1. The number of IPL matches varies across seasons.")
print("2. Mumbai Indians have won the highest number of matches.")
print("3. Teams generally prefer either batting or fielding after winning the toss.")
print("4. Some venues host significantly more IPL matches than others.")
print("5. These observations help understand trends in IPL matches.")
```
## Output
#### Basic info about dataset:
<img width="1141" height="368" alt="image" src="https://github.com/user-attachments/assets/1ab4d766-66ab-4390-8ea1-4ceaf87827ea" />

#### Matches per season:
<img width="797" height="458" alt="image" src="https://github.com/user-attachments/assets/876f3654-ce00-4f7c-bb6b-06e7e6e59a8d" />

#### Top Winning Teams:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/22728ac4-3011-4c12-8286-ef4a24c7c1d6" />

#### Toss Decisions:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1c634e2f-4760-4475-9b61-7309447a86d3" />

#### Top Venues:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/767bc998-7d87-4431-be16-5c7012129d2b" />

## Result
Thus, the Exploratory Data Analysis (EDA) on the IPL matches dataset was performed successfully.
The analysis identified the number of matches played each season, the top winning teams, toss decision preferences,
the most frequently used venues, and key insights from the data.

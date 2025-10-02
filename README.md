# Movie Recommender System Implementation

A comprehensive movie recommendation system implementation using **collaborative filtering** techniques on the MovieLens 100K dataset. This project demonstrates both item-based and user-based collaborative filtering approaches with extensive exploratory data analysis (EDA).

## Dataset

This project uses the **MovieLens 100K dataset** which contains:
- 100,000 ratings from 943 users on 1,682 movies
- Each user has rated at least 20 movies
- Ratings are on a scale of 1-5 stars
- Includes movie metadata with genre information

### Dataset Files
- `u.data`: User ratings data (user_id | item_id | rating | timestamp)
- `u.item`: Movie information including titles, release dates, and genre classifications

## Features

### 1. Exploratory Data Analysis (EDA)
- Distribution analysis of ratings and user behavior
- Statistical insights into movie popularity
- Data visualization using matplotlib and seaborn

### 2. Item-Based Collaborative Filtering
- Uses **Pearson Correlation** to find similar movies
- Recommends movies based on user's previous ratings
- Filters recommendations by minimum rating threshold

### 3. User-Based Collaborative Filtering
- Uses **Cosine Similarity** to find similar users
- Standardizes user ratings to account for rating bias
- Generates personalized recommendations based on similar users' preferences

## Technologies Used

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Scikit-learn** - Machine learning algorithms
- **Matplotlib & Seaborn** - Data visualization
- **SciPy** - Statistical functions

## Project Structure

```
├── RecSys_implementation.ipynb    # Main Jupyter notebook
├── u.data                         # User ratings dataset
├── u.item                         # Movie information dataset
└── README.md                      # This file
```

## Installation & Setup

1. Clone the repository:
```bash
git clone https://github.com/ParsaNaderiX/movie-recommender-system.git
cd movie-recommender-system-implementation
```

2. Install required dependencies:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn scipy jupyter
```

3. Launch Jupyter Notebook:
```bash
jupyter notebook
```

4. Open `RecSys_implementation.ipynb` and run all cells

## Key Insights

### Data Statistics
- **943 users** rated **1,682 movies** with **100,000 total ratings**
- Average rating distribution follows a **normal distribution**
- Most movies have fewer than 100 ratings (**long tail distribution**)

### Recommendation Examples
- **Item-based**: "Dead Poets Society" → Similar movies like "Good Will Hunting", "Scent of a Woman"
- **User-based**: Personalized recommendations for User 100 based on similar users' preferences

## Methodology

### Item-Based Collaborative Filtering
1. Create user-movie rating matrix
2. Calculate **Pearson correlation** between movies
3. Filter movies with sufficient ratings (threshold: 50+ ratings)
4. Return top similar movies

### User-Based Collaborative Filtering
1. Create user-movie rating matrix
2. Standardize ratings to normalize user behavior
3. Calculate **cosine similarity** between users
4. Find most similar users
5. Generate weighted recommendations based on similar users' ratings

## Results & Performance

The system successfully generates meaningful recommendations by:
- Identifying movies with strong positive correlations
- Filtering out movies with insufficient data
- Providing personalized suggestions based on user similarity
- Maintaining recommendation quality through statistical validation

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is open source and available under the [MIT License](LICENSE).

## Author

Created by Parsa Naderi

---

*This project is for educational purposes and demonstrates fundamental concepts in recommendation systems and collaborative filtering.*

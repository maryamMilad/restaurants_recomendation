# Restaurant Recommendation System

## Overview
This project implements a content-based restaurant recommendation system that suggests dining options based on user preferences for cuisine types, price range, and minimum ratings. The system uses cosine similarity to find restaurants that best match a user's profile.

## Key Features

### Data Preprocessing
- Standardizes numerical features (cost, price range, ratings, votes)
- Encodes binary features (table booking, online delivery)
- One-hot encodes cuisine types for similarity matching

### Recommendation Engine
- Accepts user preferences for:
  - Cuisine types (multi-select)
  - Price range 
  - Minimum rating threshold
- Uses cosine similarity to find closest matches
- Returns top 5 recommendations with key details

## Sample Usage
```python
user_preferences = {
    'cuisines': ['Japanese', 'Sushi'],
    'price_range': 3,  # Mid-range
    'min_rating': 4.0
}

recommendations = get_recommendations(user_preferences, features_df, df, cuisines_list)
```

## Output Includes
- Restaurant name
- Cuisine types
- Price range
- Aggregate rating
- Average cost for two
- City location

## Technical Implementation
- Built with Python and scikit-learn
- Uses StandardScaler for feature normalization
- Employs cosine similarity for recommendation scoring
- Handles both categorical (cuisines) and numerical features

## Requirements
- Python 3.x
- pandas
- numpy
- scikit-learn

## Future Enhancements
- Incorporate location-based filtering
- Add user review sentiment analysis
- Implement collaborative filtering approach
- Build web/mobile interface for end users

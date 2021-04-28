## Understanding CitySpire A DS Repository


- listed below are the are the endpoints created
- correstponding folders for creating these endpoints are listed below

### External.py
@router.post('/api/temperature')
- no corresponding folder

@router.post('/api/job_opportunities')
- notebooks/datasets/data/indeed
    shows how endpoint should work

@router.post('/api/rental_listing')
- no corresponding folder

@router.post('/api/schools_listing')
- notebooks/datasets/data/schools
    shows how school data was scraped and cleaned
- notebooks/datasets/model/schools
    create categorized pickle dictionary for faster lookup

### ML.py
@router.post("/api/get_data", response_model=CityData)

@router.post("/api/coordinates")

@router.post("/api/crime")
- notebooks/datasets/data/crime_data
- download adn clean information from FBI website

@router.post("/api/rental_price")
- notebooks/datasets/data/new_rents_data
- return average rental price for 2 bedroom apartments retrieved from HUD.

@router.post("/api/pollution")
- notebooks/datasets/data/pollution
- clean information from https://www.airnow.gov/aqi/aqi-basics/

@router.post("/api/walkability")
@router.post("/api/transitscore")
@router.post("/api/bikescore")
- notebooks/datasets/data/walk_score
- all three scores are scraped from walkability website -> walkscore.com

@router.post("/api/livability")
- notebooks/datasets/model/livability
- create a pickle that scales numbers that are not from a 0-100 scale, rental data, number of good days from pollution data, crime rate per 1000 residents.

@router.post("/api/population")
- notebooks/datasets/model/livability
- population data is gleaned from 2020 crime data

@router.post("/api/school_summary")
- notebooks/datasets/data/datasets_to_merge/labs2/add_school.ipynb
- create summary from web scraped school data

@router.post("/api/nearest", response_model=CityRecommendations)
- notebooks/datasets/data/model/nearest_neighbor
- during labs1 and 2, utilize numeric columns to find the 5 closest cities.

### Viz.py
@router.post("/api/demographics_graph")
@router.post("/api/employment_graph")
@router.post("/api/crime_graph")
@router.post("/api/aqi_graph")
- notebooks/datasets/visuals
@router.post('/api/population_forecast_graph')
@router.post('/api/rental_forecast_graph')
# keplergl-example

This guide will help you set up and run the project from scratch.

## Prerequisites Installation

### 1. Install Node.js
First, you need to install Node.js on your system:

- Visit [Node.js official website](https://nodejs.org/)
- Download and install the LTS (Long Term Support) version
- Verify installation by opening a terminal/command prompt and running:
  ```bash
  node --version
  npm --version
  ```

### 2. Install Yarn
After installing Node.js, install Yarn package manager:

```bash
npm install -g yarn
```

Verify Yarn installation:
```bash
yarn --version
```

## Project Setup

### 1. Clone the Repository
```bash
git clone https://github.com/[username]/keplergl-example.git
cd keplergl-example
```

### 2. Install Dependencies
Run the following command in the project root directory:
```bash
yarn install
```

### 3. Development Server
To start the development server:
```bash
yarn dev
```

The application will be running at `http://localhost:8000` by default.

## Project Structure

```
keplergl-example/
├── src/
│   ├── app.tsx         # Main application component
│   └── index.html      # HTML template
├── esbuild.config.mjs  # Build configuration
├── tsconfig.json       # TypeScript configuration
├── .yarnrc.yml        # Yarn configuration
└── package.json       # Project dependencies and scripts
```

## Available Scripts

- `yarn dev` - Starts the development server
- `yarn build` - Creates a production build
- `yarn start` - Runs the production build

## Troubleshooting

If you encounter any issues:

1. Make sure all prerequisites are installed correctly
2. Try removing these directories/files and reinstalling:
   ```bash
   rm -rf node_modules
   rm yarn.lock
   yarn install
   ```
3. Ensure you're using a compatible Node.js version
4. Clear your browser cache if you see stale content

## System Requirements

- Node.js 16.x or higher
- Yarn 1.22.x or higher
- Modern web browser (Chrome, Firefox, Safari, Edge)

## Additional Notes

- This project uses TypeScript for type safety
- Built with esbuild for fast development experience
- Uses Kepler.gl for geospatial data visualization

## Sample Data

### Local Sample Data
This repository includes pre-downloaded sample data in the `./data` directory that you can use immediately:

```
keplergl-example/
├── data/
│   ├── nyctrips/
│   │   ├── data.csv          # NYC Taxi trip records (pickup/dropoff locations)
│   │   └── config.json       # Pre-configured Kepler.gl visualization settings
│   ├── county_unemployment/
│   │   ├── config.json       # Pre-configured unemployment visualization settings
│   │   └── data.geojson     # County unemployment GeoJSON data
│   └── world_flights/
│       ├── config_soe14h.json     # Pre-configured flight visualization settings
│       └── world_flights_soe14h.json  # World flights data
```

The included datasets demonstrate different visualization capabilities:
- NYC Taxi Trips: Shows point and arc layers for taxi pickup and dropoff locations
- County Unemployment: Demonstrates choropleth mapping of unemployment rates
- World Flights: Visualizes global flight paths and patterns

You can load these local files directly into the application using the "Add Data" button.

### Additional Sample Data
For more sample datasets, you can visit the [kepler.gl-data repository](https://github.com/keplergl/kepler.gl-data). Available datasets include:

- World Flights (CSV) - 18,000 flights with country of origin data
- California Earthquakes (CSV) - 2.5+ magnitude earthquakes data from USGS
- NYC Taxi Trips (CSV) - Yellow and green taxi trip records
- San Francisco Street Trees (JSON) - Street tree locations and details
- NYC Census Data (JSON) - 2010 Census tract map with population data
- And many more...

To use additional sample data:
1. Visit [kepler.gl-data](https://github.com/keplergl/kepler.gl-data)
2. Navigate to your desired dataset folder
3. Download the CSV or JSON files
4. Load the files into the application using the "Add Data" button

Some popular datasets to start with:
```bash
# Direct links to sample datasets
https://raw.githubusercontent.com/keplergl/kepler.gl-data/master/earthquakes/earthquakes.csv
https://raw.githubusercontent.com/keplergl/kepler.gl-data/master/nyctrips/nyc_trips.csv
https://raw.githubusercontent.com/keplergl/kepler.gl-data/master/sftrees/sf_trees.json
```

## License

MIT License
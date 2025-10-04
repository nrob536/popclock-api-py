# popclock-api-py
A population clock for regions of Aoetaroa New Zealand

# Project structure
popclock-api-py/
├── .github/
│   └── workflows/              # GitHub Actions for CI/CD and deployment
│       └── deploy.yml          # Workflow for GitHub Pages deployment
├── api/
│   ├── Dockerfile              # Docker configuration for the API
│   ├── requirements.txt        # Python dependencies
│   ├── main.py                 # FastAPI application entry point
│   ├── config.py               # Configuration settings
│   └── modules/
│       ├── __init__.py
│       ├── ade_client.py       # ADE API client using pandasdmx
│       ├── population.py       # Population calculation logic
│       └── models.py           # Data models and schemas
├── visualization/              # Hugo static site
│   ├── archetypes/
│   ├── content/
│   │   └── _index.md           # Main content page
│   ├── data/                   # Data for Hugo templates
│   ├── layouts/
│   │   ├── _default/
│   │   └── partials/
│   │       ├── population_table.html
│   │       └── population_map.html
│   ├── static/
│   │   ├── css/
│   │   │   └── style.css
│   │   ├── js/
│   │   │   ├── population-clock.js  # Clock functionality
│   │   │   ├── data-fetcher.js      # API interaction
│   │   │   └── visualizations.js    # D3.js/Chart.js code
│   │   └── images/
│   ├── themes/
│   └── config.toml             # Hugo configuration
├── docs/                       # Documentation
│   └── architecture.md         # Architecture documentation
├── scripts/
│   └── generate_diagram.py     # Script for architecture diagram
├── docker-compose.yml          # For local development
└── README.md                   # Project documentation
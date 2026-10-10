# RepoPulse: GitHub Repository Health Analyzer

A polished tool for analyzing the health of public GitHub repositories. Provides insights into repository activity, maintenance, and community engagement through metrics like issue responsiveness, PR turnaround, release cadence, and more.

## Features

- **Repository Analysis**: Enter any public GitHub repository URL to get a comprehensive health report
- **Key Metrics**: Track stale issues, PR turnaround times, release frequency, contributor activity, and CI status
- **Health Score**: Evidence-based scoring system with clear explanations for each factor
- **Trend Analysis**: View metrics over time with customizable date filters
- **Export Options**: Export reports as JSON or Markdown for sharing and documentation
- **Rate Limit Aware**: Graceful handling of GitHub API limits with optional token authentication

## Getting Started

### Prerequisites

- Node.js 16+ (for frontend)
- Python 3.8+ (for backend)
- GitHub account (optional, for higher rate limits)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Jayvyanelfad/repopulse-github-health-monitor.git
   cd repopulse-github-health-monitor
   ```

2. Install backend dependencies:
   ```bash
   cd server
   pip install -r requirements.txt
   ```

3. Install frontend dependencies:
   ```bash
   cd ../client
   npm install
   ```

4. Configure environment variables:
   ```bash
   cp .env.example .env
   # Edit .env to add your GitHub token (optional) and other settings
   ```

5. Start the development servers:
   ```bash
   # In one terminal (backend)
   cd server
   python server.py
   
   # In another terminal (frontend)
   cd client
   npm start
   ```

   The backend API will be available at http://localhost:8000 and the frontend at http://localhost:3000.
   **Note**: As of this milestone, only the backend health endpoint (`GET /health`) is implemented. Additional API endpoints for repository data are planned for Milestone 2.

## Usage

1. Open your browser to `http://localhost:3000`
2. Enter a public GitHub repository URL (e.g., `https://github.com/facebook/react`)
3. View the health dashboard with metrics and insights
4. Use filters to customize date ranges and comparison views
5. Export reports as needed

## API Endpoints

- `GET /health` - Health check endpoint (currently implemented)
- `GET /api/repo/:owner/:repo` - Get repository metadata (planned)
- `GET /api/repo/:owner/:repo/issues` - Get issues (paginated) (planned)
- `GET /api/repo/:owner/:repo/pulls` - Get pull requests (paginated) (planned)
- `GET /api/repo/:owner/:repo/releases` - Get releases (paginated) (planned)
- `GET /api/repo/:owner/:repo/contributors` - Get contributors (planned)
- `GET /api/repo/:owner/:repo/workflow-runs` - Get GitHub Actions workflow runs (planned)

## Development Roadmap

See [ROADMAP.md](ROADMAP.md) for detailed development milestones.

## Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

This project is licensed under the MIT License - see [LICENSE](LICENSE) for details.

## Acknowledgments

- Built with React, TypeScript, and FastAPI
- Uses GitHub REST API for repository data
- Inspired by the need for better open source project health visibility
# Nandini's GitHub Engineering Dashboard

A responsive, dark GitHub analytics dashboard inspired by the supplied reference image.

## Features
- Live GitHub public profile data, repository counts, stars, followers, and years on GitHub
- Public project cards linking to real repositories
- Repository primary-language breakdown
- Recent public activity heatmap (limited to the GitHub public Events API history; **not** a full contribution graph)
- Responsive sidebar and mobile layout
- No dependencies, no GitHub access token required

## Run locally
Open `index.html` in a browser. If the browser blocks API requests from local files, serve the folder using `python -m http.server 8000` and open `http://localhost:8000`.

## Deploy to Vercel
1. Create a new GitHub repository (e.g. `github-dashboard`) and upload `index.html` and `README.md`.
2. In Vercel, choose **Add New → Project**, import that repository, and deploy using **Other** framework preset (no build command).
3. Use a separate domain/subdomain such as `github.nandiniportfolio.site` if desired. Do not replace your existing portfolio deployment.

## Notes
GitHub's unauthenticated REST API is rate-limited, so the site handles failed requests gracefully. The public Events API does not expose a full year of contributions; the heatmap only visualizes the limited history returned by the API. Language shares count repositories by their primary language, not bytes of code. The tech-stack badges are manually curated.

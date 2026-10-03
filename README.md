# DWEALTH SPORTS PREDICTOR V2

This build upgrades V1 with a GitHub Actions data pipeline.

## Security
The API-Football key is read from the GitHub Actions repository secret `API_FOOTBALL_KEY`.
It is never placed in `index.html`.

## How it works
API-Football -> GitHub Actions -> data/football.json -> GitHub Pages -> browser.

## First run
1. Upload/replace `index.html`.
2. Upload `.github/workflows/update-football-data.yml`.
3. Upload the `data` folder (the workflow will create/update `data/football.json`).
4. In GitHub, open Actions.
5. Select `DWEALTH SPORTS PREDICTOR V2 - Fetch Football Data`.
6. Click Run workflow.
7. Wait for it to finish successfully.
8. Refresh GitHub Pages.

## Important
The first V2 data pipeline uses real upcoming fixtures. The prediction engine still uses a transparent baseline strength model while the historical statistics layer is being added. Do not treat the probabilities as guaranteed outcomes.

## Next model layer
Historical results, home/away form, goals for/against, xG where available, rest days, injuries/lineups, Elo/Dixon-Coles calibration, chronological backtesting, Brier score, log loss and model-vs-market benchmarking.

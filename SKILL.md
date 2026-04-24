---
name: portfolio-manager
description: >
  Manage a portfolio monitored by portfolio monitor (separate app).  This is a CLI interface to the portfolio monitor that allows access to portfolio data, watchlists, pricing information, and other portfolio-related data.
metadata:
  {
    "openclaw":
      {
        "emoji": "📈",
        "requires": {
          "bins": ["portfolio-manager"],
          "env": [
            "PORTFOLIO_MANAGER_TOKEN",
            "PORTFOLIO_MANAGER_URL",
          ]
        },
        "install": [
          {
            "id": "uv",
            "kind": "uv",
            "package": "portfolio_monitor @ git+https://github.com/madsmith/portfolio_monitor",
            "bins": ["portfolio-manager"],
            "label": "Install portfolio-manager (uv)"
          }
        ],
        "primaryEnv": "PORTFOLIO_MANAGER_TOKEN",
      },
  }
---

# portfolio-manager

Use `portfolio-manager` to view status of a portfolio monitored by portfolio monitor (separate app).  This is a CLI
interface to the portfolio monitor that allows access to portfolio data, watchlists, pricing information, and other
portfolio-related data.

## Quick Start

List portfolios: `portfolio-manager portfolio list`
List portfolio details: `portfolio-manager portfolio show <portfolio-id>`
List watchlists: `portfolio-manager watchlist list`
Show watchlist: `portfolio-manager watchlist show <watchlist-id>`
Get current OHLCV: `portfolio-manager price <ticker>`
Get current OHLCV for crypto: `portfolio-manager price -t crypto <ticker>`
Get previous session OHLCV: `portfolio-manager price --previous-close <ticker>`
Get session OHLCV with pre/after-hours: `portfolio-manager price --open-close <ticker>`
Get OHLCV range: `portfolio-manager price --last 1mo --span 1d <ticker>`

## Additional References

For more detailed information, see the [CLI Examples](references/cli-examples.md) document.
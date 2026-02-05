options-straddle-analysis/
│
├── db/
│   ├── schema.sql
│   ├── indexes.sql
│   └── queries.sql
│
├── src/
│   ├── db_loader.py
│   ├── straddle_builder.py
│   ├── analytics.py
│
├── notebooks/
│   └── research.ipynb
│
├── outputs/
├── README.md
└── requirements.txt

Key observations from the data:

The "Fear Premium" is quantifiable: On expiry day (0 DTE), an ATM Straddle costs ~84 points when VIX is <10. That same straddle jumps to ~126 points when VIX is >15. That’s a 50% premium increase purely due to implied volatility.

Theta Decay isn't linear: Look at the drop in premiums from 3 DTE to 0 DTE in high volatility regimes (VIX >15). The crush is massive, dropping from ~309 to ~126.

Call vs. Put Skew: Interestingly, in low volatility regimes (<10 VIX), longer-dated ATM Calls (4 DTE) seem to command a significantly higher premium (94) compared to Puts (71).

The "black boxes" in the heatmaps? Those represent market conditions that are statistically rare (e.g., sustaining very high VIX over long DTEs without expiry resetting).

Data visualization built with [Tool Name, e.g., Python/Seaborn/Excel].



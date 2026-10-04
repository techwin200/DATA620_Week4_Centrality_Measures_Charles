# DATA 620 – Week 4: Centrality Measures (data source and plan)

Kerwin Charles

This assignment identifies a web-available network dataset with a categorical variable for every node,
lays out a plan for loading it, and describes a hypothetical outcome that could be predicted by comparing
degree centrality across the categories. It builds on my Week 3 assignment (same SNAP ego-Twitter network).

## Summary

| Item | Choice |
|---|---|
| Data source | SNAP *Social circles: Twitter* (<https://snap.stanford.edu/data/ego-Twitter.html>), HTTP download |
| Network | Ego network of user `374007416`: 139 users, 638 directed "follows" edges (ego excluded) |
| Categorical variable | **List status**: Listed (in 1+ of the ego's circles) = 109, Unlisted = 30 |
| Secondary variable | Photography tagger (uses #photography, #photos, #photoshop or #photographers): 24 yes, 115 no |
| Main measure | In-degree centrality (out-degree as a secondary measure) |
| Hypothetical outcome | Whether a user is added to one of the ego's lists, predicted from in-degree centrality |
| Wider dataset | 938 of the 973 ego networks use lists; this ego lists 78 % of its followees vs. a median of 19 % |

## Files

| Path | Contents |
|---|---|
| `centrality_measures_plan.ipynb` | The write-up: data source, variables, loading plan with checks, degree centrality, hypothetical outcome, limitations |
| `centrality_measures_plan.pdf` | PDF export of the executed notebook |
| `figures/` | Group sizes, share of alters listed across ego networks, network coloured by list status |
| `video_script.md` | Script for the video presentation |
| `build_notebook.py` | Script that generates the notebook |

The notebook downloads `twitter.tar.gz` (about 22 MB) from SNAP into `data/` the first time it runs and
extracts it there. The data is not committed to the repository.

## Run it

```bash
pip install networkx matplotlib pandas jupyter
jupyter notebook centrality_measures_plan.ipynb
```

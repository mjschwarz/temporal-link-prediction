# Temporal Link Prediction

## Instructions

1. Clone this repository.
2. Install [DGL](https://www.dgl.ai).
3. Manually download the training files from the challenge website.
- [edges_train_A.csv](https://data.dgl.ai/dataset/WSDMCup2022/edges_train_A.csv.gz)
- [node_features.csv](https://data.dgl.ai/dataset/WSDMCup2022/node_features.csv.gz)
- [edge_type_features.csv](https://data.dgl.ai/dataset/WSDMCup2022/edge_type_features.csv.gz)
- [edges_train_B.csv](https://data.dgl.ai/dataset/WSDMCup2022/edges_train_B.csv.gz)
4. Place the training files in the train_csvs directory.
5. Extract the training .csv files from .gz format.
```
gunzip -d train_csvs/*.gz
```
6. Manually download the testing CSV files from the challenge website.
- [input_A_initial.csv](https://data.dgl.ai/dataset/WSDMCup2022/input_A_initial.csv.gz)
- [input_B_initial.csv](https://data.dgl.ai/dataset/WSDMCup2022/input_B_initial.csv.gz)
7. Place the testing files in the test_csvs directory.
8. Extract the testing .csv files from .gz format.
```
gunzip -d test_csvs/*.gz
```
9. Convert the provided CSV files to DGL graph objects (for each dataset).
```
python csv2DGLgraph.py --dataset [A or B]
```
10. Train the baseline model (for each dataset).
```
python base_pipeline.py --dataset [A or B]
```
11. Check performance on testing sets.
- For reference, the baseline model got AUC of 0.511 on Dataset A and 0.510 on Dataset B.

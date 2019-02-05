# _retail_ Sample App

Sample python recipe using the retail data.

# Steps:

git clone this repository

Navigate the directory to the one containing `build.sh` file and run

```
sh ./login.sh
sh ./build.sh
```

Please note the `login.sh` script should only need to be run once.

# Sample Configuration File
Sample configuration json to be used with the recipe.
```
[
  {
    "name": "train",
    "parameters": [
      {
        "key": "learning_rate",
        "value": "0.1"
      },
      {
        "key": "n_estimators",
        "value": "100"
      },
      {
        "key": "max_depth",
        "value": "3"
      },
      {
        "key": "ACP_DSW_INPUT_FEATURES",
        "value": "date,store,storeType,storeSize,temperature,regionalFuelPrice,markdown,cpi,unemployment,isHoliday"
      },
      {
        "key": "ACP_DSW_TARGET_FEATURES",
        "value": "weeklySales"
      },
      {
        "key": "ACP_DSW_FEATURE_UPDATE_SUPPORT",
        "value": false
      },
      {
        "key": "ACP_DSW_TRAINING_XDM_SCHEMA",
        "value": "/_customer/default/DSWRetailSales"
      }
    ]
  },
  {
        "name": "score",
        "parameters": [
            {
                "key": "output_dataset_id",
                "value": "<output_dataset_id>"
            }
        ]
  }
]
```



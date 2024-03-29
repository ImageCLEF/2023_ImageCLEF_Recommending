Folder for which users will create pull requests for submissions (Recommending editorials subtask)

**Input and Output format**

For the recommending editorials subtask, you will have to answer 3 queries. Each query will point to a list of 3 items from an editorial. The format of this list is the same as the one used to parsing the training datasets. Each query will will be given to you as a json file in the following format:

 ```json
{
    "task": "editorials",
    "query": [
        "https://cuhe.in-two.com/recommendation-task/6866c21e-e97e-49f1-bc7f-563c42fe499b?format=json"
    ]
}
```

As a result of your recommendation system, we expect from you that you extend this json with a ranked array of editorial recommendations. This ranked array with recommendations should have a size <= 10. The array should start with the best editorial recommended. The output format we expect for each query is shown in the following `json`.

 ```json
{
    "task": "editorials",
    "query": [
        "https://cuhe.in-two.com/recommendation-task/6866c21e-e97e-49f1-bc7f-563c42fe499b?format=json"
    ],
    "recommendations": [ 
        "1765",
        "8896",
        "9067"
    ]
}
```

Please note that the recommended editorials should be represented by their ids, which are the 4-digit numbers with which the training dataset `json` file names are starting. Also note that the size of the recommendations array in the `json` should be <= 10. You can provide less than 10 recommendations as you see fit.

**Naming conventions**

* The query `json` files will be named according to the following scheme: `query[n].json` with `n = 1, 2, 3`. Example file name: `query1.json` 
* The output from your recommendation system should be named according to the following scheme: `recommendations[n].json`, where `n = 1, 2, 3` Example file name: `recommendations1.json`. 

Please note that you need to answer all queries and provide exactly 3 output files. 

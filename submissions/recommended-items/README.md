Folder for which users will create pull requests for submissions (Recommending items subtask)

**Input and Output format**

For the recommending items subtask, you will have to answer 10 queries. Each query will consists of 1 item which will be represented with its `linkURL` (see element `linkURL` in the json files of the training dataset). Each query will will be given to you as a json file in the following format:

 ```json
{
    "task": "items",
    "query": [
        "https://cuhe.in-two.com/recommendation-task/post/1234"
    ]
}
```

As a result of your recommendation system, we expect from you that you extend this json with a ranked array of item recommendations. This ranked array with recommendations should have a size <= 10. The array should start with the best item recommended. The output format we expect for each query is shown in the following `json`.

 ```json
{
    "task": "items",
    "query": [
        "https://cuhe.in-two.com/recommendation-task/post/1234"
    ],
    "recommendations": [ 
        "https://cuhe.in-two.com/recommendation-task/post/2345",
        "https://cuhe.in-two.com/recommendation-task/post/3456",
        "https://cuhe.in-two.com/recommendation-task/post/4567",
        "https://cuhe.in-two.com/recommendation-task/post/5678",
        "https://cuhe.in-two.com/recommendation-task/post/6789"
    ]
}
```

Please note that the recommended items should be represented by their `linkURL` elements, Also note that the size of the recommendations array in the `json` should be <= 10. You can provide less than 10 recommendations as you see fit.

**Naming conventions**

* The query `json` files will be named according to the following scheme: `query[n].json` with `n = 1..10`. Example file name: ``query1.json` 
* The output from your recommendation system should be named according to the following scheme: `recommendations[n].json`, where `n = 1..10` Example file name: `recommendations1.json`.

Please note that you need to answer all queries and provide exactly 10 output files. 

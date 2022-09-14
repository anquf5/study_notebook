# README.md

### Overview

This script is used for the technical challenge: JSON Boards CLI. Users could use the command line to combine JSON files together by inputting the folder route which includes all of the JSON files.



### Environment Requirement

This project uses Python, it doesn't use any third parties libraries, but Python 3.9 will be the best option.&#x20;

* Python 3.9

I recommend using Anaconda Command Prompt

```
conda create -n json_boards_cli python=3.9
conda activate json_boards_cli
```

### How to Run

Run cmd in ARM\__CLI\__Tool folder, execute the following command:

```
python main.py -r xxx
// "xxx" is the folder route which includes all the JSON files
```

The output file will be generated in ARM\__CLI\__Tool named _**boards.py**_

_****_

### To Do

| Item                                                                                                                                                                               | Completed |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- |
| Combine all board lists inside the JSON files into a single JSON output                                                                                                            | √         |
| Order the board list alphabetically first by `vendor`, and then by `name`                                                                                                          | √         |
| <p>Include metadata in the JSON output under a <code>_metadata</code> object including:</p><ul><li>The total number of unique vendors</li><li>The total number of boards</li></ul> | √         |
| Output the resultant JSON                                                                                                                                                          | √         |
| Test case                                                                                                                                                                          | ×         |

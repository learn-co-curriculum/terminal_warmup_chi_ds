
# Terminal Warmup Exercise

Yesterday, we learned to create folders, files, and print their content to the terminal.  Today, we will start with some basic data exploration in the command line. Let's explore the data found at the following url.  Open up a terminal window (or use the ! operator in a jupyter code cell) to navigate to a directory where you want to store the data, and run the following command:


```
curl http://rcs.bu.edu/examples/python/data_analysis/flights.csv -o flights.csv
```

### Now, perform some initial data exploration with the following commands:

    cat flights.csv

    head flights.csv

    tail flights.csv

    less flights.csv

### Try out the following commands.  The "|" is called a pipe.  It operates on the output of the previous command.  Explore what each part of the expression is doing.

    cat flights.csv |  cut -d, -f12 | tail -n +2 | sort | uniq  | wc -l 

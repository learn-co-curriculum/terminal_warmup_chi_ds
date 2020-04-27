
# Terminal Warmup Exercise

Yesterday, we learned to create folders, files, and print their content to the terminal.  Today, we will start with some basic data exploration in the command line. Let's explore the data found at the following url.  Open up a terminal window (or use the ! operator in a jupyter code cell) to navigate to a directory where you want to store the data, and run the following command:


```
curl http://rcs.bu.edu/examples/python/data_analysis/flights.csv -o flights.csv
```

Hint: Anytime you want to learn more about the executable in the terminal, you can run, for example 
```
man cat 
```
or 
```
man head
```

### Now, perform some initial data exploration with the following commands:

    cat flights.csv

    head flights.csv

    tail flights.csv

    less flights.csv

### Try out the following commands.  The "|" is called a pipe.  It operates on the output of the previous command.  Explore what each part of the expression is doing.

    cat flights.csv |  cut -d, -f12 | tail -n +2 | sort | uniq  | wc -l 


```python
# Write what each part does in this cell
```

### Now test out this command, and explore the difference between the two.

    cat flights.csv| cut -d, -f12 | tail -n +2 | sort| uniq -c | sort -r -n | head -n10 


```python
# Write what the difference is here
```

### Next, use similar methods to gather these data sets and answer the associated questions.

    https://raw.githubusercontent.com/vega/vega/master/docs/data/sp500.csv
    
    What is the highest price reached of the sp500? What is the lowest price reached?     
    



```python
# your answer here
```

```
https://raw.githubusercontent.com/vega/datalib/master/test/data/stocks.csv

How many observations of each unique stock?
``` 



```python
# your answer here
```

```       
    http://www.gutenberg.org/cache/epub/5200/pg5200.txt
    
    What are the most common words and their counts?
    hint: use   tr " " "\n"  to break out words on their own line
```


```python
# Your answer here
```


```python

```

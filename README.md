
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

'''
1. cat flights.csv outputs the data of the csv file, and pipes it into the next command
2. Cut -d, tells to split up each line by a comma for a delimiter, then output the 12th column
3. tail -n +2 removes the header from the outpu
4. Sort sorts the values alphabetically
5. uniq reduces the output to uniqu values
6. wc -l counts the number of lines output in the terminal

'''

```

### Now test out this command, and explore the difference between the two.

    cat flights.csv| cut -d, -f12 | tail -n +2 | sort| uniq -c | sort -r -n | head -n10 


```python
"""
1. everything is the same as before up to uniq -c
2. uniq -c counts the number of each unique value
3. sort -r -n sorts the values in reverse numerically.  Without -n, the numerical sort would be wonky.
4. Head -n10 outputs the top 10 counts.
"""
```

### Next, use similar methods to gather these data sets and answer the associated questions.

    https://raw.githubusercontent.com/vega/vega/master/docs/data/sp500.csv
    
    What is the highest price reached of the sp500? What is the lowest price reached?     
    



```python
"""
high: 1549.38
cat sp500.csv | cut -d, -f2 | sort -r -n | head -n1

low: 735.09 
500.csv | cut -d, -f2 | sort -r -n | tail -n2

"""
```

```
https://raw.githubusercontent.com/vega/datalib/master/test/data/stocks.csv

How many observations of each unique stock?
``` 



```python
"""
68 GOOG
123 AAPL
123 AMZN
123 IBM
123 MSFT
 
cat stocks.csv | cut -d, -f1|uniq -c|sort -n

"""
```

```       
    http://www.gutenberg.org/cache/epub/5200/pg5200.txt
    
    What are the most common words and their counts?
    hint: use   tr " " "\n"  to break out words on their own line
```


```python
"""
cat pg5200.txt | tr " " "\n"| sort|uniq -c|sort -r -n|head
"""
```




    '\ncat pg5200.txt | tr " " "\n"| sort|uniq -c|sort -r -n|head\n'



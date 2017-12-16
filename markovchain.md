# Tweet Generator 

#### 

#### Histogram

Counts the number of occurrences in word.  

List of tuples \[\('Fish', 4\), \('red', 1\) ...\]

Dictionary maps Key --&gt; Value

**Hash table**: 

Sample words randomly based on frequency weighting count tokens in corpus in one big histogram. 



#### Markov Chain 

Count co-occurrences of words in context 

Dictionary maps keys --&gt; Values 



#### Linked List 

**N** is the number of nodes.

Length - of linked list.

Append -  append the value to the end of the list O\(1\).

Prepend - Make new node O\(1\), node.next = head O\(1\), adjust head to the next node O\(1\). 

 Find \(quality function\) - Iterate over all the nodes, new tail or not found. 

Worse case: While loop: \# N iterations, If check quality \(data\), return data and current = current. next O\(n\)

Best case: O\(1\) new head. 



#### Hash Table 

N is the number of entrees \(key, value\).

B is the number of buckets.

L is the average length of each bucket. 



L = N/B  -- **Load factor **









Suppose you have a corpus with 50,000 words total \(2, 000 unique words\)

1\) If you build a histogram, how many entries will it have?

Only 2000 \(number of types\) , because the histogram will count the number of the occurrences.

Dictionary takes only unique values.

2\) If you build a 1st order Markov Chain what structues do you need to create and how many?

Two Dictionaries

{'Dictogram': \({ Dictogram }\) }

3\) If you build a 2nd order Markov chain, how many would you structures change? Approximately how many of these structures will you have?

Two Dictionary and a String {'String': {... : ... }}

Two Dictionary and a tuple {\(... , ....\){... : ... }}

String is a data type and not a structure. Structures are build off of data types.


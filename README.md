# Julia vs Python

 This is to check the speed of execution of Julia vs Python. There are 3 Python versions
 - with Dataframes
 - with only numpy arrays
 - with numpy arrays+ Numba @JIT decorator

The task is very simple. There are 5 states (1,2,3,4,5) and 10000 rows that carry a random state. There is also a transition probability matrix, that show the migration probability from one state to another. 

We have to simulate the changes of those 10000 rows 100 periods ahead, and store them in an array/dataframe. This totals to 1000000 iterations.

The results show that with DataFrame/pandas version Python does this in ~300 secons. With Numpy array version the time shrinks to ~60 secons. With @jit decorator this result is broadly unchanged.

While Julia does this job in only 1.26 seconds.

Your result may vary depending on a speed of your computerm but the differences between the versions might be stable.

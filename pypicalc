import time
import psutil
import math

def calculate_pi(n):
    pi = 0
    for i in range(n):
        pi += (-1)**i / (2*i + 1)
    return 4 * pi

def measure_performance(n):
    # Record start time and initial memory usage
    start_time = time.time()
    process = psutil.Process(os.getpid())
    initial_memory = process.memory_info().rss

    # Calculate pi
    pi = calculate_pi(n)

    # Record end time and final memory usage
    end_time = time.time()
    final_memory = process.memory_info().rss

    # Calculate elapsed time and memory usage
    elapsed_time = end_time - start_time
    memory_usage = final_memory - initial_memory

    return elapsed_time, memory_usage

n = 100000
elapsed_time, memory_usage = measure_performance(n)
print(f'Calculating pi using the Leibniz formula with n = {n} took {elapsed_time:.2f} seconds and used {memory_usage/1024**2:.2f} MB of memory.')

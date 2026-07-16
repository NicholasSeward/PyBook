# Advanced Complexity

## Beyond the Basics

We've covered O(1), O(n), O(log n), and O(n²). Now let's look at some more complex algorithms and their performance characteristics.

## O(n!) - Factorial Time

### What is n!?
n! means n × (n-1) × (n-2) × ... × 2 × 1
- 3! = 3 × 2 × 1 = 6
- 5! = 5 × 4 × 3 × 2 × 1 = 120
- 10! = 3,628,800

### Why So Slow?
Factorial grows incredibly fast:
- 5 items: 120 operations
- 10 items: 3.6 million operations
- 20 items: 2.4 quintillion operations!

### Real Examples
- **Traveling Salesman**: Find shortest route visiting all cities
- **Permutations**: Generate all possible orderings of items
- **Scheduling**: Find optimal schedule for many tasks

**Warning**: These problems become impossible to solve exactly as n grows!

## O(2ⁿ) - Exponential Time

### What is 2ⁿ?
- 2¹ = 2
- 2² = 4
- 2³ = 8
- 2¹⁰ = 1,024
- 2²⁰ = 1,048,576

### Why Exponential is Bad
Each item doubles the work:
- 10 items: 1,024 operations
- 20 items: 1 million operations
- 30 items: 1 billion operations

### Real Examples
- **Subset Sum**: Find all possible combinations of numbers
- **Knapsack Problem**: Choose items to fit in limited space
- **Boolean Satisfiability**: Find true/false values for variables

**Rule**: If you see "try all combinations," it's probably exponential!

## O(n × log n) - Linearithmic Time

### What is n × log n?
This is actually quite good! It's between O(n) and O(n²):
- 100 items: 100 × log₂(100) ≈ 664 operations
- 1,000 items: 1,000 × log₂(1,000) ≈ 9,966 operations
- 1,000,000 items: 1,000,000 × log₂(1,000,000) ≈ 19.9 million operations

### Why This is Good
- Much better than O(n²)
- Close to linear time
- Often the best we can do for certain problems

### Real Examples
- **Sorting**: Merge sort, quick sort, heap sort
- **Searching**: Binary search on sorted data
- **Divide and Conquer**: Problems that can be split in half

## Comparing Growth Rates

From fastest to slowest:
1. **O(1)** - Constant (always the same)
2. **O(log n)** - Logarithmic (grows very slowly)
3. **O(n)** - Linear (grows with input size)
4. **O(n × log n)** - Linearithmic (good for sorting)
5. **O(n²)** - Quadratic (gets slow quickly)
6. **O(2ⁿ)** - Exponential (explodes!)
7. **O(n!)** - Factorial (impossible for large n)

## Business Impact

### O(n!) and O(2ⁿ)
- **Never use** for business applications
- **Customers will leave** waiting for results
- **Server costs explode**
- **Use approximations** instead

### O(n × log n)
- **Acceptable** for most business needs
- **Sorting is fine** at this complexity
- **Scales reasonably** with growth
- **Industry standard** for many problems

## Key Points

- **O(n!)**: Factorial - grows impossibly fast
- **O(2ⁿ)**: Exponential - doubles with each item
- **O(n × log n)**: Linearithmic - good for sorting
- **Avoid**: Factorial and exponential for business
- **Accept**: Linearithmic for complex but necessary operations
- **Growth rates**: Know which ones are business-friendly

# NumPy : Numerical Python

## Key Topics Discussed
- Creating null (zero) matrices and arrays  
- Specifying array shapes for 1‑D and 2‑D data  
- Changing element data types (`dtype`)  
- Generating equally spaced values with `linspace`  
- Producing random numbers (`rand`, `randint`)  
- Performing arithmetic, trigonometric, and logarithmic operations  
- Using statistical helpers: median, mean, variance, std, cumulative sums/products  

## Array Creation
- `np.zeros(shape)` → null matrix/array of zeros  
- `np.full(shape, fill_value)` for constant non‑zero entries  
- `np.identity(n)` or `np.eye(n)` → identity matrix (1 on diagonal)  
- Shape syntax: `(rows, cols)` for 2‑D, single integer for 1‑D  
- Example: `np.zeros((5, 6))` creates a 5 × 6 zero matrix  

## Data Types & Conversion
- Default dtype is `float64`; specify with `dtype=` argument  
- Convert after creation: `arr.astype(np.int32)` or other types  
- Changing dtype affects how values are stored and displayed  

## Generating Equally Spaced Values
- `np.linspace(start, stop, num)` → `num` evenly spaced numbers  
- To split interval into *k* parts, use `num = k + 1` (e.g., 5 parts → 6 numbers)  
- Contrast with `np.arange(start, stop, step)` which uses step size  

## Random Numbers
- Uniform floats: `np.random.rand(N)` → N values in [0, 1)  
- Integer range: `np.random.randint(low, high, size=…)` → inclusive low, exclusive high  
- Example: `np.random.randint(1, 11)` returns a random integer 1–10  

## Arithmetic Operations
- Element‑wise: `np.add(a, b)`, `np.subtract(a, b)`, `np.multiply(a, b)`, `np.divide(a, b)`  
- Modulus: `np.mod(a, b)` (remainder)  
- Matrix multiplication: `np.dot(A, B)` or the `@` operator  

## Mathematical Functions
- Logarithms: `np.log(x)` (base e), `np.log10(x)`, `np.log2(x)`; custom base → `np.log(x)/np.log(b)`  
- Square root: `np.sqrt(x)`  
- Trigonometry: `np.sin`, `np.cos`, `np.tan`; input in radians (use `np.deg2rad` for degrees)  

## Statistical Functions
- Mean: `np.mean(a)`  
- Median: `np.median(a)`  
- Variance: `np.var(a)` (spread around the mean)  
- Standard deviation: `np.std(a)` (sqrt of variance)  
- Cumulative sum: `np.cumsum(a)`  
- Cumulative product: **use** `np.cumprod(a)` (not `np.cumproduct`)  

## Sorting & Indexing
- Sort ascending: `np.sort(a)`; descending via slicing `np.sort(a)[::-1]`  
- Get sorted indices: `np.argsort(a)`  
- Find max/min values and their indices: `np.max(a)`, `np.min(a)`, `np.argmax(a)`, `np.argmin(a)`  
- Reverse array order: `a[::-1]`  

## Common Errors & Fixes
- `np.cumproduct` does not exist → replace with `np.cumprod`  
- dtype mismatches cause unexpected casting; specify `dtype` explicitly when needed  
- Remember radians vs degrees for trig functions; convert if necessary  

# Pandas vs FireDucks Comparison

## 1. Pandas
Pandas is a widely-used Python library for data manipulation and analysis. It provides data structures such as Series and DataFrame, making it easy to work with structured data.

### Features
- Provides Series and DataFrame for handling structured data
- Supports reading/writing data from multiple formats (CSV, Excel, SQL, JSON, etc.)
- Offers powerful groupby and aggregation functions
- Enables easy data cleaning and transformation
- Supports time series analysis
- Integrates well with NumPy and SciPy for scientific computing

### Installation
Pandas can be installed using pip:

```sh
pip install pandas
```

## 2. FireDucks
FireDucks is a high-performance, compiler-accelerated dataframe library for Python. It is designed with speed and Pandas compatibility in mind.

## 3. Installation
FireDucks is currently available for Linux (manylinux) on the x86_64 architecture. Support for other platforms will be added based on user requests. It can be installed using pip:

```sh
pip install fireducks
```

## 4. Import Hook
FireDucks provides an import hook utility that automatically replaces `import pandas` statements with FireDucks. This allows existing programs to run with FireDucks without manual modifications.

### Usage
Run your Python script using FireDucks with the `-m` option:

```sh
python3 -m fireducks.pandas your_script.py
```

For IPython/Jupyter Notebook, a magic command is available:

```python
%load_ext fireducks.pandas
import pandas as pd
```

### Benefits
- Useful when your program includes multiple scripts importing Pandas internally.
- Avoids manually replacing import statements.
- Ensures compatibility with external libraries (e.g., Matplotlib) that may use Pandas DataFrames.

📢 **Note:** The import hook feature has been renamed to `fireducks.pandas` from FireDucks 0.11.0. The old module name `fireducks.imhook` is still available as an alias.

## 5. Explicit Import
FireDucks provides a Pandas-like module `fireducks.pandas`, which can be imported directly instead of Pandas. To use FireDucks in an existing Pandas program, modify the import statement as follows:

```python
# import pandas as pd
import fireducks.pandas as pd
```

## 6. Running the Notebook in a Linux-Based Environment
To run the "fireducks vs pandas.ipynb" file in Google Colab with a CPU runtime (Colab is free to use), follow these steps:

### Steps to Run in Google Colab
1. Open [Google Colab](https://colab.research.google.com/)
2. Click on **File** > **Upload Notebook**
3. Upload the `fireducks vs pandas.ipynb` file
4. Ensure the runtime is set to **CPU** by clicking on **Runtime** > **Change runtime type** > **Select CPU**
5. Run the notebook cells sequentially

This setup allows you to compare the performance and functionality of Pandas and FireDucks in a cloud-based Linux environment without local installation hassles.

# Pandas vs FireDucks Comparison

## 1. FireDucks
FireDucks is a high-performance, compiler-accelerated dataframe library for Python. It is designed with speed and Pandas compatibility in mind.

## 2. Installation
FireDucks is currently available for Linux (manylinux) on the x86_64 architecture. Support for other platforms will be added based on user requests. It can be installed using pip:

```sh
pip install fireducks
```

## 3. Import Hook
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

## 4. Explicit Import
FireDucks provides a Pandas-like module `fireducks.pandas`, which can be imported directly instead of Pandas. To use FireDucks in an existing Pandas program, modify the import statement as follows:

```python
# import pandas as pd
import fireducks.pandas as pd

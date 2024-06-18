# LZW Compression Algorithm

This repository contains an implementation of the LZW (Lempel-Ziv-Welch) compression algorithm in Python. The algorithm compresses text data and calculates various metrics such as bits before compression, bits after compression, compression ratio, symbol probabilities, entropy, and compression efficiency. Additionally, it provides functionality to decompress the encoded data back to its original form.

## Features

- **LZW Compression**: Compresses input text data using the LZW algorithm.
- **Metrics Calculation**: Calculates bits before and after compression, compression ratio, symbol probabilities, entropy, and compression efficiency.
- **LZW Decompression**: Decompresses the encoded data back to the original text.

## Installation

Clone the repository to your local machine:

```bash
git clone https://github.com/yourusername/lzw-compression.git
cd lzw-compression
```

## Usage

The main class in this implementation is `LZW`. Here is an example of how to use it:

```python
from lzw import LZW

# Input text to be compressed
text = "wabbawabbadrewsr fyht g"

# Create an LZW object
lzw = LZW(text)

# Print the results
print(lzw.get_results())

# Decompress the encoded string
decompressed_text = LZW.lzw_decompress(lzw.encoded_string)
print("Decompressed text:", decompressed_text)
```

### Example Output

```json
{
    "encoded_string": [119, 97, 98, 98, 97, 256, 258, 100, 114, 101, 119, 115, 114, 32, 102, 121, 104, 116, 32, 103],
    "bits_before": 192,
    "bits_after": 100,
    "compression ratio (%)": 192.0,
    "probabilities": {
        "w": 0.083,
        "a": 0.083,
        "b": 0.083,
        "d": 0.042,
        "r": 0.125,
        "e": 0.042,
        "s": 0.042,
        "f": 0.042,
        "y": 0.042,
        "h": 0.042,
        "t": 0.042,
        " ": 0.083,
        "g": 0.042
    },
    "entropy": 3.494,
    "efficiency": 47.9
}
Decompressed text: wabbawabbadrewsr fyht g
```

## Methods

### `__init__(self, text)`
Initializes the LZW object with the given text and performs compression and metric calculations.

### `compress(self)`
Compresses the input text using the LZW algorithm.

### `compute_bits_before(self)`
Calculates the total number of bits required to represent the original text.

### `compute_bits_after(self)`
Calculates the total number of bits required to represent the compressed text.

### `compute_cr(self)`
Calculates the compression ratio.

### `compute_probabilities(self)`
Calculates the probabilities of each character in the input text.

### `compute_entropy(self)`
Calculates the entropy of the input text.

### `compute_efficiency(self)`
Calculates the compression efficiency.

### `get_results(self)`
Returns a dictionary of all computed metrics.

### `@staticmethod lzw_decompress(compressed)`
Decompresses the given compressed data back to the original text.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request or open an issue.

## License

This project is licensed under the MIT License.

## Acknowledgements

This project was inspired by the need to understand and implement the LZW compression algorithm in Python.

---

Feel free to reach out with any questions or suggestions!

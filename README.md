# Llama 3.2 Token Counter

![Python Version](https://img.shields.io/badge/python-3.11%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)

A simple and efficient token counter for Llama 3.2 models.

## Description

The Llama 3.2 Token Counter is a Python package that provides an easy way to count tokens generated by Llama 3.2 models. This tool is essential for developers and researchers working with large language models, helping them manage token limits and optimize their use of the Llama 3.2 architecture.

## Features

- Accurate token counting for Llama 3.2 models
- Easy-to-use Python API
- Supports both string and list of strings inputs
- Asynchronous token counting support
- Batch processing for large inputs
- Lightweight and efficient

## Installation

You can install the Llama 3.2 Token Counter using pip:

```bash
pip install llama3.2-token-counter
```

## Usage

Here's a quick example of how to use the Llama 3.2 Token Counter:

```python
from llama_token_counter import LlamaTokenCounter
import asyncio

# Initialize the token counter
counter = LlamaTokenCounter()

# Synchronous token counting
text = "Hello, world! This is a sample text for token counting."
token_count = counter.count_tokens(text)
print(f"The text contains {token_count} tokens.")

# Asynchronous token counting
async def count_async():
    text = "This is an async token counting example."
    token_count = await counter.count_tokens(text)
    print(f"The async text contains {token_count} tokens.")

asyncio.run(count_async())

# Count tokens in a list of strings
texts = ["Hello, world!", "This is another sample.", "Multiple strings can be processed."]
token_count = counter.count_tokens(texts)
print(f"The list of texts contains {token_count} tokens in total.")

# Get the maximum token limit
max_tokens = counter.get_max_tokens()
print(f"The maximum token limit is {max_tokens}.")

# Batch processing for large lists
large_list = ["Text " + str(i) for i in range(10000)]
token_count = counter.count_tokens(large_list, batch_size=500)
print(f"The large list contains {token_count} tokens in total.")
```

## Contributing

We welcome contributions to the Llama 3.2 Token Counter! If you'd like to contribute, please look at [CONTRIBUTING.md](CONTRIBUTING.md) for more information.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

Anthony - [@anthoeknee](https://github.com/anthoeknee)

Project Link: [https://github.com/anthoeknee/llama3.2-token-counter](https://github.com/anthoeknee/llama3.2-token-counter)

## Running Tests

To run the tests, follow these steps:

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/llama3.2-token-counter.git
   cd llama3.2-token-counter
   ```

2. Install the development dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Run the tests:
   ```
   pytest tests
   ```

Make sure you have the necessary tokenizer files in the `src/llama_token_counter/tokenizer` directory before running the tests.
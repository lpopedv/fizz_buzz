# FizzBuzz

This application is a simple implementation of the classic FizzBuzz problem written in Elixir. It reads a list of numbers from a file, processes them, and returns a list where numbers divisible by 3 are replaced with `:fizz`, numbers divisible by 5 are replaced with `:buzz`, and numbers divisible by both 3 and 5 are replaced with `:fizzbuzz`. Numbers that do not meet these criteria remain unchanged.

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed by adding `fizz_buzz` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:fizz_buzz, "~> 0.1.0"}
  ]
end
```

## Usage

To use the FizzBuzz module, create a file with comma-separated numbers (e.g., `numbers.txt`):

**Example file (`numbers.txt`):**
```
1, 2, 3, 4, 5, 15
```

Then, call the `build/1` function with the file name:

```elixir
FizzBuzz.build("numbers.txt")
# Output: {:ok, [1, 2, :fizz, 4, :buzz, :fizzbuzz]}
```

If there is an issue reading the file, the function will return an error tuple:

```elixir
FizzBuzz.build("nonexistent.txt")
# Output: {:error, "Error reading the file: enoent"}
```

## Running Tests

To verify the functionality of the application, run the tests using the following command:

```bash
mix test
```

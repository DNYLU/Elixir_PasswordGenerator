# Password Generator

A module that generates random passwords based on given options. The main function of the module is `generate(options)` which takes an options map as input.

## Usage

```elixir
options = %{
  "length" => "10",
  "numbers" => "true",
  "uppercase" => "true",
  "symbols" => "true"
}

{:ok, password} = PasswordGenerator.generate(options)
IO.puts("Generated password: #{password}")
```

<h2>Options</h2>
The available options for generating passwords are:

* "length": The desired length of the password.
* "numbers": Include numbers in the password.
* "uppercase": Include uppercase letters in the password.
* "symbols": Include symbols in the password.

Example of using options:
```elixir
options = %{
  "length" => "12",
  "numbers" => "true",
  "uppercase" => "false",
  "symbols" => "true"
}
```

<h2>Examples</h2>
<h3>Generating a Password</h3>

```elixir
options = %{
  "length" => "16",
  "numbers" => "true",
  "uppercase" => "true",
  "symbols" => "true"
}

{:ok, password} = PasswordGenerator.generate(options)
IO.puts("Generated password: #{password}")
```
<h3>Error Handling</h3>
If any validation fails during password generation, an error tuple is returned:

```elixir
options = %{
  "length" => "5",
  "numbers" => "invalid",
  "uppercase" => "false",
  "symbols" => "true"
}

{:error, reason} = PasswordGenerator.generate(options)
IO.puts("Error: #{reason}")
```
<h3>Running Tests</h3>
To run the tests for the 'PasswordGenerator' module, use the following command:

```elixir
mix test
``` 
<h3>Testing Notes</h3>
The 'PasswordGeneratorTest' module contains unit tests for various scenarios of password generation and error handling. These tests ensure that the password generation logic is working as expected.

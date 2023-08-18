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

Options
The available options for generating passwords are:

* "length": The desired length of the password.
* "numbers": Include numbers in the password.
* "uppercase": Include uppercase letters in the password.
* "symbols": Include symbols in the password.

Example of using options:
options = %{
  "length" => "12",
  "numbers" => "true",
  "uppercase" => "false",
  "symbols" => "true"
}

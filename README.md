# crypt3r

crypt(3) NIF for Elixir.

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed
by adding `crypt3` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:crypt3r, "~> 1.0.0"}
  ]
end
```

Documentation can be generated with [ExDoc](https://github.com/elixir-lang/ex_doc)
and published on [HexDocs](https://hexdocs.pm). Once published, the docs can
be found at [https://hexdocs.pm/crypt3r](https://hexdocs.pm/crypt3r).

## Usage

```elixir
iex> Crypt3.crypt("aaaaaaaa", "aa")
"aakcR08PK3l1o"
```

## Acknowledgement

This code is a fork of [https://github.com/ominousness/crypt3](https://github.com/ominousness/crypt3) which has sadly disappeared from the internet
and I needed to fix a bug in the C source to make it compile on a mac, hence the reanimation of it.

# DO NOT USE THIS UNLESS YOU KNOW WHAT YOU'RE DOING

Seriously - this stuff is ancient awfulness and should not be used for anything else except if you
for some reason have a bunch of crypt(3) hashed passwords, that for some reason you want to be able to
deal with from within elixir. Given how easily hackable the darn things are, you're probably better off
brute-forcing the plaintexts and re-hashing them using [Bcrypt](https://hexdocs.pm/bcrypt_elixir/api-reference.html)

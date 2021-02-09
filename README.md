## My First Steps with Elixir :diamonds:

### Install

**Arch Linux** (Community repository)

- Run: `pacman -S elixir`

<br>

*Checking the installed version of Elixir*
Once you have Elixir installed, you can check its version by running 

```elixir
elixir --version
```

### Links

- https://elixir-lang.org/install.html

<br>

### Learning

https://elixirschool.com/en/

Terminal Elixir, for Interactive Elixir

```elixir
Interactive Elixir (1.11.0) - press Ctrl+C to exit (type h() ENTER for help)
iex(1)> 1 + 2 
3
```

To leave the Interactive Elixir, you need to hit Ctrl+C twice.

```elixir
IO.puts "Hello World"
```

Elixir executable

```shell
elixir hello_world.exs
hello World
```

It's simple to compile our file from the Interactive Elixir:

```shell
iex
iex(1)> c "hello_world.exs"
Hello, World!
[]
```

#### Mix

> *Mix is a build tool that ships with Elixir that provides tasks for creating, compiling, testing your application, managing its dependencies and much more.*

https://hexdocs.pm/mix/Mix.html

https://elixir-lang.org/getting-started/mix-otp/introduction-to-mix.html

For those who are familiar with Ruby, mix is some kind of mixture of Bundler, rake and a little bit of Ruby on Rails generators. *[Click Here](https://whatdidilearn.info/2017/09/14/elixir-first-steps.html)*

```
Elixir
 └── mix
     ├── Create applications
     ├── Compile applications
     ├── Run tasks (such as tests)
     └── Manage dependencies
```

Let’s try to generate new application by typing `mix new hello_world` in the terminal window:

```shell
mix new hello_world
* creating README.md
* creating .formatter.exs
* creating .gitignore
* creating mix.exs
* creating lib
* creating lib/hello_world.ex
* creating test
* creating test/test_helper.exs
* creating test/hello_world_test.exs

Your Mix project was created successfully.
You can use "mix" to compile it, test it, and more:

    cd hello_world
    mix test

Run "mix help" for more commands.
```

More interesting files

`mix.exs` - contains application version and dependencies
`lib/hello_world.ex` - our actual implementation of the project
`text/hello_world_test.exs` - contains tests for the implementation file

<br>

Compile our project

```shell
iex -S mix
```

Now we can call or function using `ModuleName.function_name` format:

```
iex -S mix
Erlang/OTP 23 [erts-11.1.6] [source] [64-bit] [smp:4:4] [ds:4:4:10] [async-threads:1] [hipe]

Compiling 1 file (.ex)
Generated hello_world app
Interactive Elixir (1.11.0) - press Ctrl+C to exit (type h() ENTER for help)
iex(1)> HelloWorld.hello
:world
```

[Project hello_world](hello_world/)
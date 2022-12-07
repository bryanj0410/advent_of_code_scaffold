# 🎄 [Advent of Code](https://adventofcode.com/) solutions in [Elixir](https://elixir-lang.org/) ⚗️

A scaffold for Advent of Code solutions in Elixir

## Usage

Solutions, tests, and input are structured by years and day.
* Solutions: `lib/advent/y<YYYY>/d<DD>.ex`, e.g. `lib/advent/y2020/d01.ex`
* Tests: `test/advent/y<YYYY>/d<DD>_test.exs`, e.g. `test/advent/y2020/d01_test.exs`
* Input: `priv/puzzle_input/y<YYYY>/d<DD>.txt`, e.g. `priv/puzzle_input/y2020/d01.txt`

### Generate code scaffold for a given day

You can generate a scaffold for a given day by running:

```
mix aoc.gen.day <YYYY> <dd> [--session <TOKEN>]
```

For example, `mix aoc.gen.day 2021 7` will generate

* `lib/advent/y2021/d07.ex`. Has two empty functions `part_one/1` and
  `part_two/1`
* `test/advent/y2021/d07_test.exs`. Has 4 unit tests, 2 for each part. Each
  part has one for example input and another for file input
* `priv/puzzle_input/y2021/d07.txt`. An empty file to copy/paste your puzzle
  input into

The optional `--session` flag takes your web browser session token (you can
retrieve if you inspect the web page while logged in). If provided, the task
will attempt to download your input file.

You also can set the `AOC_SESSION` environment variable where you would store the session cookie.
If you do this, you only need to call:
```
mix aoc.gen.day <YYYY> <dd>
```
and it will get your input file content.

### Running tests

You can run all tests with `mix test`.

You also have the option of testing a narrowed scope.
For example: `mix test test/advent/y2022/` tests a specific year and
`mix test test/advent/y2022/d01_test.exs` tests a specific day.

Further, some tests are tagged as `long_running: true`. These tests typically
take longer than 10 seconds to complete on my laptop. Tests with this
tag are excluded by default. To include these tests add
`--include long_running:true` to your `mix test` command.

You can read more about `mix test` options
[here](https://hexdocs.pm/mix/Mix.Tasks.Test.html).

## License

This project is licensed under the
[MIT License](https://choosealicense.com/licenses/mit/). See the
[LICENSE](https://github.com/ed-flanagan/advent-of-code-solutions-elixir/blob/main/LICENSE)
file for more details.

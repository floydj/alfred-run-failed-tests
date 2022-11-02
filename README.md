# alfred-run-failed-tests
Automagically combine failed minitest tests into a single command in iTerm2

# Usage
When you have failed tests in a rails minitest suite using the defer option, e.g. `rails test test/models/whatever_test.rb -d`, you get something like the following out of the box in iTerm2:

```
Failed tests:

rails test test/system/whatever_test.rb:4
rails test test/system/filler_test.rb:135
```

This can be a pain when you have some flaky tests, and in my experience, you'll always have _some_ flakiness with system tests especially. Once you have the workflow installed, just type `combinerailstests` in Alfred, and the appropriate command to run those failed tests will be built, typed into iTerm2 and run for you, e.g. `bin/rails test test/system/whatever_test.rb:4 test/system/filler_test.rb:135 -vd`

# Installation
Download the `alfred-run-failed-tests.alfredworkflow` file from this repo, double-click it in macOS to install in Alfred, and you're good to go.

# Assumptions
* You're using binstubs in your Rails app


#### MIT License

Copyright (c) 2022 Jason Floyd

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

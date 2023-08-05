# Testing in System tests driven by rack_test

https://twitter.com/robzolkos/status/1687863191794249730

- [Setup] (https://github.com/robzolkos/testperformance/blob/main/test/application_system_test_case.rb)

Benefits of running system test using rack_test - can run non-javascript tests using same capybara actions as you're used to. Speed is the same as running controller tests.

### Running System test using `rack_test`

- [Example Test](https://github.com/robzolkos/testperformance/blob/main/test/system/posts_test.rb)

```
❯ rails test test/system/posts_test.rb
Running 2 tests in a single process (parallelization threshold is 50)
Run options: --seed 18584

# Running:

..

Finished in 0.088925s, 22.4909 runs/s, 22.4909 assertions/s.
```

### Running System test using Browser

- [Example Test](https://github.com/robzolkos/testperformance/blob/main/test/system/posts_browser_test.rb)

```
❯ rails test test/system/posts_browser_test.rb
Running 2 tests in a single process (parallelization threshold is 50)
Run options: --seed 19508

# Running:

Capybara starting Puma...
* Version 5.6.6 , codename: Birdie's Version
* Min threads: 0, max threads: 4
* Listening on http://127.0.0.1:64298
..

Finished in 1.818186s, 1.1000 runs/s, 1.1000 assertions/s.
```

### Running Controller Test

- [Example Test](https://github.com/robzolkos/testperformance/blob/main/test/controllers/posts_controller_test.rb)

```
rails test test/controllers
Running 3 tests in a single process (parallelization threshold is 50)
Run options: --seed 12327

# Running:

...

Finished in 0.081580s, 36.7737 runs/s, 49.0316 assertions/s.
```

# Using Eliot for better understanding about functions call

When you are working with Python, sometime to really want to check input/output of some functions in order to debug or understand the inside. Usually you will using standard Python `logging` or even `print` function to see the input/output. But It is not really a good way and time consumed

After reading some Python document I found a library to solve this proble, it is `Eliot`

## How?

Install Eliot is straitforward, `pip install eliot`

Let assume that you have some simple function below

```python
def add(a, b):
    return a + b


def multiply(a, b):
    return a * b


def multiplysum(a, b, c, d):
    return multiply(add(a, b), multiply(c, d))

result = multiplysum(1, 2, 4, 5) # (1 + 2) * (4 * 5) ⇒ 60

print(result)
assert result == 60

```

Basically when you try to test it, you can see result is printed out without any error.

But It is painful for you to understand the output and input despite above snippet is quite simple.

So let's apply Eliot and see how it can help us


```python
from eliot import log_call, to_file
to_file(open("out.log", "w"))


@log_call
def add(a, b):
    return a + b


@log_call
def multiply(a, b):
    return a * b


@log_call
def multiplysum(a, b, c, d):
    return multiply(add(a, b), multiply(c, d))


result = multiplysum(1, 2, 4, 5) # (1 + 2) * (4 * 5) ⇒ 60

print(result)
assert result == 61

```

I added `@log_call` and also changed `assert`. Trigger python file, then you can see `out.log` appears.

Example content

```
{"a": 1, "b": 2, "c": 4, "d": 5, "action_status": "started", "timestamp": 1579170124.754551, "task_uuid": "460b784f-1c58-499c-80ed-3fb7f74fd2bb", "action_type": "__main__.multiplysum", "task_level": [1]}
{"a": 1, "b": 2, "action_status": "started", "timestamp": 1579170124.754828, "task_uuid": "460b784f-1c58-499c-80ed-3fb7f74fd2bb", "action_type": "__main__.add", "task_level": [2, 1]}
{"result": 3, "action_status": "succeeded", "timestamp": 1579170124.7548878, "task_uuid": "460b784f-1c58-499c-80ed-3fb7f74fd2bb", "action_type": "__main__.add", "task_level": [2, 2]}
```

## What? Log file is a text file, how to understand Install?

Did I mention that It helps you to have better understanding? There are many lines it comes painful.

Our eliottree will help us to render log file as ASCII tree. Check https://github.com/jonathanj/eliottree for more detail

When you call `eliot-tree out.log` you possible see the output

```
460b784f-1c58-499c-80ed-3fb7f74fd2bb
└── __main__.multiplysum/1 ⇒ started 2020-01-16 10:22:04 ⧖ 0.001s
    ├── a: 1
    ├── b: 2
    ├── c: 4
    ├── d: 5
    ├── __main__.add/2/1 ⇒ started 2020-01-16 10:22:04 ⧖ 0.000s
    │   ├── a: 1
    │   ├── b: 2
    │   └── __main__.add/2/2 ⇒ succeeded 2020-01-16 10:22:04
    │       └── result: 3
    ├── __main__.multiply/3/1 ⇒ started 2020-01-16 10:22:04 ⧖ 0.000s
    │   ├── a: 4
    │   ├── b: 5
    │   └── __main__.multiply/3/2 ⇒ succeeded 2020-01-16 10:22:04
    │       └── result: 20
```

Very clear and understandable about your code and steps

If you want to know more about it, visit its website at https://eliot.readthedocs.io/en/stable/index.html


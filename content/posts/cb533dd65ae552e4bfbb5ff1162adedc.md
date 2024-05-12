---
title: 'GitHub - MartinThoma/flake8-simplify: ❄ A flake8 plugin that helps you to
  simplify code'
date: 2022-09-13
src_link: https://www.notion.so/GitHub-MartinThoma-flake8-simplify-A-flake8-plugin-that-helps-you-to-simplify-code-2560f304c0794b85ad9e51a1e2146404
src_date: '2022-09-13 22:01:00'
gold_link: https://github.com/MartinThoma/flake8-simplify
gold_link_hash: cb533dd65ae552e4bfbb5ff1162adedc
tags:
- '#host_github_com'
---

[![](https://camo.githubusercontent.com/964b9b70541e1c55600c0aededeef03f72d5da9e4e2c25d2a7d9af1be425d451/68747470733a2f2f62616467652e667572792e696f2f70792f666c616b65382d73696d706c6966792e737667)](https://badge.fury.io/py/flake8-simplify)
[![](https://camo.githubusercontent.com/0d6532519dcc1084dc8ad11e7dd1f87c5b34d12c6ff985fc5f8a5fc875196a95/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f436f64652d4769744875622d627269676874677265656e)](https://github.com/MartinThoma/flake8-simplify)
[![](https://github.com/MartinThoma/flake8-simplify/workflows/Unit%20Tests/badge.svg)](https://github.com/MartinThoma/flake8-simplify/actions)
[![](https://camo.githubusercontent.com/7d770c433d6198d89f8c1e2f187b904a9721d176259d0e97157337741cc8e837/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f636f64652532307374796c652d626c61636b2d3030303030302e737667)](https://github.com/psf/black)


flake8-simplify
===============


A [flake8](https://flake8.pycqa.org/en/latest/index.html) plugin that helps you simplify your code.


Installation
------------


Install with `pip`:



```
pip install flake8-simplify
```

Python 3.8 to 3.11 are supported.


Usage
-----


Just call `flake8 .` in your package or `flake your.py`:



```
$ flake8 .
./foo/__init__.py:690:12: SIM101 Multiple isinstance-calls which can be merged into a single call for variable 'other'

```

Rules
-----


Python-specific rules:


* `SIM101`: Multiple isinstance-calls which can be merged into a single call by
using a tuple as a second argument ([example](#SIM101))
* [`SIM104`](https://github.com/MartinThoma/flake8-simplify/issues/4) [![](https://camo.githubusercontent.com/4bc45a69d3ffcbd91fc11087ff7315f9bb72cffc4ba946a386b8c54ebb6d81a4/68747470733a2f2f736869656c64732e696f2f62616467652f2d6c65676163796669782d696e616374697665)](https://camo.githubusercontent.com/4bc45a69d3ffcbd91fc11087ff7315f9bb72cffc4ba946a386b8c54ebb6d81a4/68747470733a2f2f736869656c64732e696f2f62616467652f2d6c65676163796669782d696e616374697665): Use 'yield from iterable' (introduced in Python 3.3, see [PEP 380](https://docs.python.org/3/whatsnew/3.3.html#pep-380)) ([example](#SIM104))
* [`SIM105`](https://github.com/MartinThoma/flake8-simplify/issues/5): Use ['contextlib.suppress(...)'](https://docs.python.org/3/library/contextlib.html#contextlib.suppress) instead of try-except-pass ([example](#SIM105))
* [`SIM107`](https://github.com/MartinThoma/flake8-simplify/issues/9): Don't use `return` in try/except and finally ([example](#SIM107))
* [`SIM108`](https://github.com/MartinThoma/flake8-simplify/issues/12): Use the ternary operator if it's reasonable ([example](#SIM108))
* [`SIM109`](https://github.com/MartinThoma/flake8-simplify/issues/11): Use a tuple to compare a value against multiple values ([example](#SIM109))
* [`SIM110`](https://github.com/MartinThoma/flake8-simplify/issues/15): Use [any(...)](https://docs.python.org/3/library/functions.html#any) ([example](#SIM110))
* [`SIM111`](https://github.com/MartinThoma/flake8-simplify/issues/15): Use [all(...)](https://docs.python.org/3/library/functions.html#all) ([example](#SIM111))
* [`SIM113`](https://github.com/MartinThoma/flake8-simplify/issues/18): Use enumerate instead of manually incrementing a counter ([example](#SIM113))
* [`SIM114`](https://github.com/MartinThoma/flake8-simplify/issues/10): Combine conditions via a logical or to prevent duplicating code ([example](#SIM114))
* [`SIM115`](https://github.com/MartinThoma/flake8-simplify/issues/17): Use context handler for opening files ([example](#SIM115))
* [`SIM116`](https://github.com/MartinThoma/flake8-simplify/issues/31): Use a dictionary instead of many if/else equality checks ([example](#SIM116))
* [`SIM117`](https://github.com/MartinThoma/flake8-simplify/issues/35): Merge with-statements that use the same scope ([example](#SIM117))
* `SIM119`: [![](https://camo.githubusercontent.com/dbe5dfaa0b175e6fccb4e85cfe4ed26c395fe2ec9dc02d5c64c2668563ac2969/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d72656d6f7665642d6c6967687467726579)](https://camo.githubusercontent.com/dbe5dfaa0b175e6fccb4e85cfe4ed26c395fe2ec9dc02d5c64c2668563ac2969/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d72656d6f7665642d6c6967687467726579) Moved to [flake8-scream](https://github.com/MartinThoma/flake8-scream) due to [issue 63](https://github.com/MartinThoma/flake8-simplify/issues/63)
* `SIM120` [![](https://camo.githubusercontent.com/4bc45a69d3ffcbd91fc11087ff7315f9bb72cffc4ba946a386b8c54ebb6d81a4/68747470733a2f2f736869656c64732e696f2f62616467652f2d6c65676163796669782d696e616374697665)](https://camo.githubusercontent.com/4bc45a69d3ffcbd91fc11087ff7315f9bb72cffc4ba946a386b8c54ebb6d81a4/68747470733a2f2f736869656c64732e696f2f62616467652f2d6c65676163796669782d696e616374697665): Use 'class FooBar:' instead of 'class FooBar(object):' ([example](#SIM120))
* `SIM121`: Reserved for [SIM908](#sim908) once it's stable
* `SIM125`: Reserved for [SIM905](#sim905) once it's stable
* `SIM126`: Reserved for [SIM906](#sim906) once it's stable
* `SIM127`: Reserved for [SIM907](#sim907) once it's stable


Simplifying Comparisons:


* `SIM201`: Use 'a != b' instead of 'not a == b' ([example](#SIM201))
* `SIM202`: Use 'a == b' instead of 'not a != b' ([example](#SIM202))
* `SIM203`: Use 'a not in b' instead of 'not (a in b)' ([example](#SIM203))
* `SIM204`: [![](https://camo.githubusercontent.com/dbe5dfaa0b175e6fccb4e85cfe4ed26c395fe2ec9dc02d5c64c2668563ac2969/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d72656d6f7665642d6c6967687467726579)](https://camo.githubusercontent.com/dbe5dfaa0b175e6fccb4e85cfe4ed26c395fe2ec9dc02d5c64c2668563ac2969/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d72656d6f7665642d6c6967687467726579) Moved to [flake8-scream](https://github.com/MartinThoma/flake8-scream) due to [issue 116](https://github.com/MartinThoma/flake8-simplify/issues/116)
* `SIM205`: [![](https://camo.githubusercontent.com/dbe5dfaa0b175e6fccb4e85cfe4ed26c395fe2ec9dc02d5c64c2668563ac2969/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d72656d6f7665642d6c6967687467726579)](https://camo.githubusercontent.com/dbe5dfaa0b175e6fccb4e85cfe4ed26c395fe2ec9dc02d5c64c2668563ac2969/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d72656d6f7665642d6c6967687467726579) Moved to [flake8-scream](https://github.com/MartinThoma/flake8-scream) due to [issue 116](https://github.com/MartinThoma/flake8-simplify/issues/116)
* `SIM206`: [![](https://camo.githubusercontent.com/dbe5dfaa0b175e6fccb4e85cfe4ed26c395fe2ec9dc02d5c64c2668563ac2969/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d72656d6f7665642d6c6967687467726579)](https://camo.githubusercontent.com/dbe5dfaa0b175e6fccb4e85cfe4ed26c395fe2ec9dc02d5c64c2668563ac2969/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d72656d6f7665642d6c6967687467726579) Moved to [flake8-scream](https://github.com/MartinThoma/flake8-scream) due to [issue 116](https://github.com/MartinThoma/flake8-simplify/issues/116)
* `SIM207`: [![](https://camo.githubusercontent.com/dbe5dfaa0b175e6fccb4e85cfe4ed26c395fe2ec9dc02d5c64c2668563ac2969/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d72656d6f7665642d6c6967687467726579)](https://camo.githubusercontent.com/dbe5dfaa0b175e6fccb4e85cfe4ed26c395fe2ec9dc02d5c64c2668563ac2969/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d72656d6f7665642d6c6967687467726579) Moved to [flake8-scream](https://github.com/MartinThoma/flake8-scream) due to [issue 116](https://github.com/MartinThoma/flake8-simplify/issues/116)
* `SIM208`: Use 'a' instead of 'not (not a)' ([example](#SIM208))
* `SIM210`: Use 'bool(a)' instead of 'True if a else False' ([example](#SIM210))
* `SIM211`: Use 'not a' instead of 'False if a else True' ([example](#SIM211))
* [`SIM212`](https://github.com/MartinThoma/flake8-simplify/issues/6): Use 'a if a else b' instead of 'b if not a else a' ([example](#SIM212))
* [`SIM220`](https://github.com/MartinThoma/flake8-simplify/issues/6): Use 'False' instead of 'a and not a' ([example](#SIM220))
* [`SIM221`](https://github.com/MartinThoma/flake8-simplify/issues/6): Use 'True' instead of 'a or not a' ([example](#SIM221))
* [`SIM222`](https://github.com/MartinThoma/flake8-simplify/issues/6): Use 'True' instead of '... or True' ([example](#SIM222))
* [`SIM223`](https://github.com/MartinThoma/flake8-simplify/issues/6): Use 'False' instead of '... and False' ([example](#SIM223))
* [`SIM224`](https://github.com/MartinThoma/flake8-simplify/issues/88): Reserved for [SIM901](#sim901) once it's stable
* [`SIM300`](https://github.com/MartinThoma/flake8-simplify/issues/16): Use 'age == 42' instead of '42 == age' ([example](#SIM300))


Simplifying usage of dictionaries:


* [`SIM401`](https://github.com/MartinThoma/flake8-simplify/issues/72): Use 'a\_dict.get(key, "default\_value")' instead of an if-block ([example](#SIM401))
* [`SIM118`](https://github.com/MartinThoma/flake8-simplify/issues/40): Use 'key in dict' instead of 'key in dict.keys()' ([example](#SIM118))
* `SIM119` Reserved for [SIM911](#sim911) once it's stable


General Code Style:


* `SIM102`: Use a single if-statement instead of nested if-statements ([example](#SIM102))
* [`SIM103`](https://github.com/MartinThoma/flake8-simplify/issues/3): Return the boolean condition directly ([example](#SIM103))
* [`SIM106`](https://github.com/MartinThoma/flake8-simplify/issues/8): Handle error-cases first ([example](#SIM106)). This rule was removed due to too many false-positives.
* [`SIM112`](https://github.com/MartinThoma/flake8-simplify/issues/19): Use CAPITAL environment variables ([example](#SIM112))
* `SIM122` / SIM902: [![](https://camo.githubusercontent.com/dbe5dfaa0b175e6fccb4e85cfe4ed26c395fe2ec9dc02d5c64c2668563ac2969/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d72656d6f7665642d6c6967687467726579)](https://camo.githubusercontent.com/dbe5dfaa0b175e6fccb4e85cfe4ed26c395fe2ec9dc02d5c64c2668563ac2969/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d72656d6f7665642d6c6967687467726579) Moved to [flake8-scream](https://github.com/MartinThoma/flake8-scream) due to [issue 125](https://github.com/MartinThoma/flake8-simplify/issues/125)
* `SIM123` / SIM902: [![](https://camo.githubusercontent.com/dbe5dfaa0b175e6fccb4e85cfe4ed26c395fe2ec9dc02d5c64c2668563ac2969/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d72656d6f7665642d6c6967687467726579)](https://camo.githubusercontent.com/dbe5dfaa0b175e6fccb4e85cfe4ed26c395fe2ec9dc02d5c64c2668563ac2969/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d72656d6f7665642d6c6967687467726579) Moved to [flake8-scream](https://github.com/MartinThoma/flake8-scream) due to [issue 130](https://github.com/MartinThoma/flake8-simplify/issues/130)
* `SIM124`: Reserved for SIM909 once it's stable


**Experimental rules:**


Getting rules right for every possible case is hard. I don't want to disturb
peoples workflows. For this reason, flake8-simplify introduces new rules with
the `SIM9` prefix. Every new rule will start with SIM9 and stay there for at
least 6 months. In this time people can give feedback. Once the rule is stable,
the code will change to another number.


Current experimental rules:


* `SIM901`: Use comparisons directly instead of wrapping them in a `bool(...)` call ([example](#SIM901))
* `SIM904`: Assign values to dictionary directly at initialization ([example](#SIM904))
* [`SIM905`](https://github.com/MartinThoma/flake8-simplify/issues/86): Split string directly if only constants are used ([example](#SIM905))
* [`SIM906`](https://github.com/MartinThoma/flake8-simplify/issues/101): Merge nested os.path.join calls ([example](#SIM906))
* [`SIM907`](https://github.com/MartinThoma/flake8-simplify/issues/64): Use Optional[Type] instead of Union[Type, None] ([example](#SIM907))
* [`SIM908`](https://github.com/MartinThoma/flake8-simplify/issues/50): Use dict.get(key) ([example](#SIM908))
* [`SIM909`](https://github.com/MartinThoma/flake8-simplify/issues/114): Avoid reflexive assignments ([example](#SIM909))
* [`SIM910`](https://github.com/MartinThoma/flake8-simplify/issues/171): Avoid to use `dict.get(key, None)` ([example](#SIM910))
* [`SIM911`](https://github.com/MartinThoma/flake8-simplify/issues/161): Avoid using `zip(dict.keys(), dict.values())` ([example](#SIM911))


Disabling Rules
---------------


You might have good reasons to
[ignore some flake8 rules](https://flake8.pycqa.org/en/3.1.1/user/ignoring-errors.html).
To do that, use the standard Flake8 configuration. For example, within the `setup.cfg` file:



```
[flake8]
ignore = SIM106, SIM113, SIM119, SIM9
```

Examples
--------


### SIM101



```
# Bad
isinstance(a, int) or isinstance(a, float)

# Good
isinstance(a, (int, float))
```

### SIM102



```
# Bad
if a:
    if b:
        c

# Good
if a and b:
    c
```

### SIM105



```
# Bad
try:
    foo()
except ValueError:
    pass

# Good
from contextlib import suppress

with suppress(ValueError):
    foo()
```

Please note that `contextlib.suppress` is roughly 3x slower than `try/except`
([source](https://github.com/MartinThoma/flake8-simplify/issues/91)).


### SIM107



```
# Bad: This example returns 3!
def foo():
    try:
        1 / 0
        return "1"
    except:
        return "2"
    finally:
        return "3"


# Good
def foo():
    return_value = None
    try:
        1 / 0
        return_value = "1"
    except:
        return_value = "2"
    finally:
        return_value = "3"  # you might also want to check if "except" happened
    return return_value
```

### SIM108



```
# Bad
if a:
    b = c
else:
    b = d

# Good
b = c if a else d
```

### SIM109



```
# Bad
if a == b or a == c:
    d

# Good
if a in (b, c):
    d
```

### SIM110



```
# Bad
for x in iterable:
    if check(x):
        return True
return False

# Good
return any(check(x) for x in iterable)
```

### SIM111



```
# Bad
for x in iterable:
    if check(x):
        return False
return True

# Good
return all(not check(x) for x in iterable)
```

### SIM112



```
# Bad
os.environ["foo"]
os.environ.get("bar")

# Good
os.environ["FOO"]
os.environ.get("BAR")
```

### SIM113


Using [`enumerate`](https://docs.python.org/3/library/functions.html#enumerate) in simple cases like the loops below is a tiny bit easier to read as the reader does not have to figure out where / when the loop variable is incremented (or if it is incremented in multiple places).



```
# Bad
idx = 0
for el in iterable:
    ...
    idx += 1

# Good
for idx, el in enumerate(iterable):
    ...
```

### SIM114



```
# Bad
if a:
    b
elif c:
    b

# Good
if a or c:
    b
```

### SIM115



```
# Bad
f = open(...)
...  # (do something with f)
f.close()

# Good
with open(...) as f:
    ...  # (do something with f)
```

### SIM116



```
# Bad
if a == "foo":
    return "bar"
elif a == "bar":
    return "baz"
elif a == "boo":
    return "ooh"
else:
    return 42

# Good
mapping = {"foo": "bar", "bar": "baz", "boo": "ooh"}
return mapping.get(a, 42)
```

### SIM117



```
# Bad
with A() as a:
    with B() as b:
        print("hello")

# Good
with A() as a, B() as b:
    print("hello")
```

Thank you for pointing this one out, [Aaron Gokaslan](https://github.com/Skylion007)!


### SIM118



```
# Bad
key in a_dict.keys()

# Good
key in a_dict
```

Thank you for pointing this one out, [Aaron Gokaslan](https://github.com/Skylion007)!


### SIM120



```
# Bad
class FooBar(object):
    ...


# Good
class FooBar:
    ...
```

Both notations are equivalent in Python 3, but the second one is shorter.


### SIM201



```
# Bad
not a == b

# Good
a != b
```

### SIM202



```
# Bad
not a != b

# Good
a == b
```

### SIM203



```
# Bad
not a in b

# Good
a not in b
```

### SIM208



```
# Bad
not (not a)

# Good
a
```

### SIM210



```
# Bad
True if a else False

# Good
bool(a)
```

### SIM211



```
# Bad
False if a else True

# Good
not a
```

### SIM212



```
# Bad
b if not a else a

# Good
a if a else b
```

### SIM220



```
# Bad
a and not a

# Good
False
```

### SIM221



```
# Bad
a or not a

# Good
True
```

### SIM222



```
# Bad
... or True

# Good
True
```

### SIM223



```
# Bad
... and False

# Good
False
```

### SIM300



```
# Bad; This is called a "Yoda-Condition"
42 == age

# Good
age == 42
```

### SIM401



```
# Bad
if key in a_dict:
    value = a_dict[key]
else:
    value = "default_value"

# Good
thing = a_dict.get(key, "default_value")
```

### SIM901


This rule will be renamed to `SIM224` after its 6-month trial period is over.
Please report any issues you encounter with this rule!


The trial period starts on 23rd of January and will end on 23rd of August 2022.



```
# Bad
bool(a == b)

# Good
a == b
```

### SIM904


This rule will be renamed to `SIM224` after its 6-month trial period is over.
Please report any issues you encounter with this rule!


The trial period starts on 12th of February and will end on 12th of September 2022.



```
# Bad
a = {}
a["b"] = "c"

# Good
a = {"b": "c"}
```

### SIM905


This rule will be renamed to `SIM225` after its 6-month trial period is over.
Please report any issues you encounter with this rule!


The trial period starts on 13th of February and will end on 13th of September 2022.



```
# Bad
domains = "de com net org".split()

# Good
domains = ["de", "com", "net", "org"]
```

### SIM906


This rule will be renamed to `SIM126` after its 6-month trial period is over.
Please report any issues you encounter with this rule!


The trial period starts on 20th of February and will end on 20th of September 2022.



```
# Bad
os.path.join(a, os.path.join(b, c))

# Good
os.path.join(a, b, c)
```

### SIM907


This rule will be renamed to `SIM127` after its 6-month trial period is over.
Please report any issues you encounter with this rule!


The trial period starts on 28th of March and will end on 28th of September 2022.



```
# Bad
def foo(a: Union[int, None]) -> Union[int, None]:
    return a


# Good
def foo(a: Optional[int]) -> Optional[int]:
    return a
```

### SIM908


This rule will be renamed to `SIM121` after its 6-month trial period is over.
Please report any issues you encounter with this rule!


The trial period starts on 28th of March and will end on 28th of September 2022.



```
# Bad
name = "some_default"
if "some_key" in some_dict:
    name = some_dict["some_key"]

# Good
name = some_dict.get("some_key", "some_default")
```

### SIM909


Thank you Ryan Delaney for the idea!


This rule will be renamed to `SIM124` after its 6-month trial period is over.
Please report any issues you encounter with this rule!


The trial period starts on 28th of March and will end on 28th of September 2022.



```
# Bad
foo = foo

# Good: Nothing. Reflexive assignments have no purpose.
```

or



```
# Bad
foo = foo = 42

# Good
foo = 42
```

### SIM910



```
# Bad
dict.get(key, None)

# Good
dict.get(key)
```
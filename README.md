# promisepay-python
PromisePay/AssemblyPayments SDK for python

# Installation

```python
pip install promisepay
```

# Django framework configuration

```python
settings.py

PROMISE_PAY_KEY = 'YOUR PROMISEPAY username'
PROMISE_PAY_SECRET = 'YOUR PROMISEPAY SECRET KEY'
PROMISE_PAY_IS_PROD = 'IF YOUR are using production metion True . if not dont declare '
```


# Core python

```python
from promisepay import auth

auth('YOUR PROMISEPAY username','YOUR PROMISEPAY SECRET KEY',PROMISE_PAY_IS_PROD)

```

# Example usage


```python
from promisepay.modules import PromisePayUser

#get list of users

p = PromisePayUser()
users = p.get_list(limit=2)

for user in users:
  print user.id
  print user.full_name

#get one user

user = PromisePayUser('UNIQUE id of promisepay user')
if user.status=='success':
  print user.id 
  print user.full_name

```


# currently under development . will update soon

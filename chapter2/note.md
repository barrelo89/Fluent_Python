# Python Sequence Type by Data Type:
1. container sequences: list, tuple, collecitons.deque -> any type of data
2. flat sequences: str, bytes, bytearray, memoryview, array.array -> only primitive values like char, bytres, and numbers

# Python Sequence Type by Mutability:
1. Mutable Sequences: list, bytearray, arra.arra, collections.deque, memoryview
2. Immutable Sequences: tuple, str, bytes

# Note
List Comprehension: Listcomp Generator Expression: Genexp
1. Genexp saves memory because it yields items one by one using the iterator protocol instead of builiding a whle list just to feed another constructor. -> use genexp to initialize s equences other than lists, or to produce output that you don't need to keep in memory
2. Tuples are not ojust immutable lists but records
3. Another example of tuple unpacking is prefixing an argument with a star when calling a function:
```
t = (20, 8)
function(*t)
```
4. Using * to grab excess items: In Python 3, this idea was extended to apply to parallel assignment as well:
```
a, b, *rest = range(5)
a, b, rest
(0, 1, [2, 3, 4])
```
5. collections.namedtuple
```
from collections import namedtuple
City = namedtuple('City', 'name country population coordinates')
tokyo = City('Tokyo', 'JP', 36.933, (35.689722, 139.691667))
tokyo
City(name='Tokyo', country='JP', population=36.933, coordinates=(35.689722,139.691667))
tokyo.population
36.933
tokyo.coordinates
(35.689722, 139.691667)
tokyo[1]
'JP'

>>> City._fields
('name', 'country', 'population', 'coordinates')
LatLong = namedtuple('LatLong', 'lat long')
delhi_data = ('Delhi NCR', 'IN', 21.935, LatLong(28.613889, 77.208889))
delhi = City._make(delhi_data)
delhi._asdict()
OrderedDict([('name', 'Delhi NCR'), ('country', 'IN'), ('population',
21.935), ('coordinates', LatLong(lat=28.613889, long=77.208889))])
for key, value in delhi._asdict().items():
print(key + ':', value)
name: Delhi NCR
country: IN
population: 21.935
coordinates: LatLong(lat=28.613889, long=77.208889)
```
6. Beware of expressions like a * n when a is a sequence containing mutable items because the result may surprise you. For example, trying to initialize a list of lists as my_list = [[]] * 3 will result in a list with three references to the same inner list, which is probably not what you want.














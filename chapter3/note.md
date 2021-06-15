## Dictionary
1. dictionary.setdefault(key, object)
2. from collections import defaultdict: can define a default value whenver a key is missing
3. StrKeyDict0: when searching for a non-string key, StrKeyDict0 converts it to str when it is not found
4. from collections import OrderedDict: maintains keys in insertion order, allowing iteration over items in a predictable order. 'popitem' method of an OrderedDict pops the first item by default, but if called as 'popitem(last = True)', it pops the last item added
5. from collections import Counter: holds an integer count for each key, method: counter.update(), counter.most_common()
6.  

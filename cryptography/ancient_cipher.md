# 古典暗号
## 単一換字式暗号
* 頻度分析が有効
```python
from collections import Counter
from string import ascii_lowercase

with open("study-guide.txt", "r") as f:
    ciphertext = f.read()

charcount = Counter(c for c in ciphertext if c in ascii_lowercase)
total_chars = sum(charcount.values())

for char, count in charcount.items():
    print(f"{char}: {(count * 100)/total_chars}% ({count})")
```

このあと、https://quipqiup.com/  をつかって、候補を探り出す (めちゃ有能)

- [datetime](#datetime)
  - [時刻の足し算引き算をするコード](#時刻の足し算引き算をするコード)
    - [23時59分の一分後](#23時59分の一分後)
    - [23時59分の1秒前](#23時59分の1秒前)
  - [演算子を使って比較](#演算子を使って比較)

# datetime
## 時刻の足し算引き算をするコード
```python
import datetime
basetime = datetime.time(23, 59, 00)
```

### 23時59分の一分後
```python
dt1 = datetime.datetime.combine(datetime.date.today(), basetime) + datetime.timedelta(minutes=1)
```
### 23時59分の1秒前
```python
dt2 = datetime.datetime.combine(datetime.date.today(), basetime) - datetime.timedelta(seconds=1)
```
```python
print(dt1.strftime("%H:%M:%S"))
print(dt2.strftime("%H:%M:%S"))
```

## 演算子を使って比較
```python
from datetime import datetime, timedelta

previous_date = datetime.now() - timedelta(days=1)
current_date = datetime.now()
print(present > past)
```
> True
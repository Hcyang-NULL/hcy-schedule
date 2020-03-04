## Python进度条

#### 1. 安装
```python
pip install hcy-schedule -i https://pypi.python.org/pypi
```

#### 2. 使用
```python
from schedule import Schedule
lis = [i for i in range(100)]
shedule = Schedule(lis, name='Loop')
for i in lis:
    # some code
    schedule.watch()
```

#### 3. 参数
Schedule类在创建时支持传入两个参数
* var: 可以为数字（十进制）或者任何支持len()方法的变量，用于获取循环次数 [required]
* name: 当前进度的名称 [optional]

#### 4. 方法
* 使用os内置方法获取当前终端窗口的宽度使得进度条占据终端的完整宽度
* 时间计算是根据已经完成的比例和已流逝的时间进行简单推算，只有当一次循环结束时会更新一次

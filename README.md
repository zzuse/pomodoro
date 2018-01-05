# Pomodoro

Simple command line pomodoro app with visualization of statistics.
The Pomodoro technique is a time management technique for improving productivity.

Check (<https://en.wikipedia.org/wiki/Pomodoro_Technique>)
for more details.

The code is based on : <http://code.activestate.com/recipes/577358-pomodoro-timer/>
TODO: add did what column and statics

## How to install ?

```bash
    git clone https://github.com/zzuse/pomodoro
    cd pomodoro
    pip3 install -r requirements.txt
    python3 setup.py install
```

## How to use it?

```bash
  pomodoro 60 5
```

will run pomodoro cycles of 60mins of work and 5mins of rest. 
By default an alarm sound will be played at the end of pomodoros.
**Warning** : alarm needs mpg123 (https://www.mpg123.de/)

it can be disabled using:
  
```bash
  pomodoro 60 5 --alarm=False
```

Instead of an alarm, you might rather want to receive a message box each time you finish a pomodoro. 
To do that, you can do:

```bash
  pomodoro 60 5 --notif=True --alarm=False
```

**Warning** : notif needs pyqt5 (https://pypi.python.org/pypi/PyQt5/5.8.2)
```bash
  pip3 install PyQt5
```

## Statistics

each time a pomodoro is performed, its recorded on a small text database in your HOME/.pomodoro. To visualize the statistics of your pomodoros, you can use pomostat. Here are some examples:

```bash
  pomostat overall
  pomostat week
  pomostat thisweek
  pomostat lastweek
  pomostat stats
  pomostat weeks
  pomostat today
  pomostat yesterday
```

Check ```pomostat --help``` for more information. 

Here is an example of graph with ```pomostat thisweek```:

![pomo](https://raw.githubusercontent.com/mehdidc/pomodoro/master/pomo.png)




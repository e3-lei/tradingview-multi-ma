multi-ma
---

snippets used to draw multiple ma lines on trading view

```
study(title="Moving Averages", shorttitle="MAs", overlay=true)
exponential = input(true, title="Exponential MA")
level1=input(title="level1",defval=20)
level2=input(title="level2",defval=50)
level3=input(title="level3",defval=100)
level4=input(title="level4",defval=200)

src = close

ma20 = exponential ? ema(src, level1) : sma(src, level1)
ma50 = exponential ? ema(src, level2) : sma(src, level2)
ma100 = exponential ? ema(src, level3) : sma(src, level3)
ma200 = exponential ? ema(src, level4) : sma(src, level4)

plot(ma20, color=orange, style=line, title="MMA20", linewidth=1)
plot(ma50, color=fuchsia, style=line, title="MMA50", linewidth=1)
plot(ma100, color=purple, style=line, title="MMA100", linewidth=1)
plot(ma200, color=black, style=line, title="MMA200", linewidth=1)
```

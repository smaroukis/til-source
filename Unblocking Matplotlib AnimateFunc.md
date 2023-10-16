---
publish:true
---
#til #python 

For my [real time graphing script](https://github.com/smaroukis/realtime-plotter/), I was hunting down a bug that wasn't allowing the matplotlib animation function. 

It turns out we needed to delay in the `while 1` loop to allow the animation function to fully finish.

```python
# ... 
plot = plotter(queue, save_figas)
ani = plot.ani 
try:
    while True:
        plt.pause(0.1) # <-- KEY POINT need small pause to allow animation to update
        pass 
except KeyboardInterrupt:
    print("interrrupted by keyboard")
```

Code can be seen at https://github.com/smaroukis/realtime-plotter/. Here is an overview:

![[Pasted image 20231009093501.png]]
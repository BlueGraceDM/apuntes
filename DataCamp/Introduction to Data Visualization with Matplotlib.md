## How to create Graphs on Matplotlib

```python
import matplotlib.pyplot as plt # Import the library


fig, ax = plt.subplots() # Create the figure base and axes. Dont forget the arguments
plt.show() # Call the show function tho show the result 
```

## Adding data to an Axes object

```python
import matplotlib.pyplot as plt

fig, ax = plt.subplots()
# if you want to imput data from a pandas dataframe
ax.plot(austin_weather['MONTH'], austin_weather['MLY_PRCP_NORMAL'])
# call the function
plot.show()
```

## Adding markers

in ax.plot add

| marker                  | symbol                                                | description                                                                                                                                                                               |
| ----------------------- | ----------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `"."`                   | ![m00](https://matplotlib.org/stable/_images/m00.png) | point                                                                                                                                                                                     |
| `","`                   | ![m01](https://matplotlib.org/stable/_images/m01.png) | pixel                                                                                                                                                                                     |
| `"o"`                   | ![m02](https://matplotlib.org/stable/_images/m02.png) | circle                                                                                                                                                                                    |
| `"v"`                   | ![m03](https://matplotlib.org/stable/_images/m03.png) | triangle_down                                                                                                                                                                             |
| `"^"`                   | ![m04](https://matplotlib.org/stable/_images/m04.png) | triangle_up                                                                                                                                                                               |
| `"<"`                   | ![m05](https://matplotlib.org/stable/_images/m05.png) | triangle_left                                                                                                                                                                             |
| `">"`                   | ![m06](https://matplotlib.org/stable/_images/m06.png) | triangle_right                                                                                                                                                                            |
| `"1"`                   | ![m07](https://matplotlib.org/stable/_images/m07.png) | tri_down                                                                                                                                                                                  |
| `"2"`                   | ![m08](https://matplotlib.org/stable/_images/m08.png) | tri_up                                                                                                                                                                                    |
| `"3"`                   | ![m09](https://matplotlib.org/stable/_images/m09.png) | tri_left                                                                                                                                                                                  |
| `"4"`                   | ![m10](https://matplotlib.org/stable/_images/m10.png) | tri_right                                                                                                                                                                                 |
| `"8"`                   | ![m11](https://matplotlib.org/stable/_images/m11.png) | octagon                                                                                                                                                                                   |
| `"s"`                   | ![m12](https://matplotlib.org/stable/_images/m12.png) | square                                                                                                                                                                                    |
| `"p"`                   | ![m13](https://matplotlib.org/stable/_images/m13.png) | pentagon                                                                                                                                                                                  |
| `"P"`                   | ![m23](https://matplotlib.org/stable/_images/m23.png) | plus (filled)                                                                                                                                                                             |
| `"*"`                   | ![m14](https://matplotlib.org/stable/_images/m14.png) | star                                                                                                                                                                                      |
| `"h"`                   | ![m15](https://matplotlib.org/stable/_images/m15.png) | hexagon1                                                                                                                                                                                  |
| `"H"`                   | ![m16](https://matplotlib.org/stable/_images/m16.png) | hexagon2                                                                                                                                                                                  |
| `"+"`                   | ![m17](https://matplotlib.org/stable/_images/m17.png) | plus                                                                                                                                                                                      |
| `"x"`                   | ![m18](https://matplotlib.org/stable/_images/m18.png) | x                                                                                                                                                                                         |
| `"X"`                   | ![m24](https://matplotlib.org/stable/_images/m24.png) | x (filled)                                                                                                                                                                                |
| `"D"`                   | ![m19](https://matplotlib.org/stable/_images/m19.png) | diamond                                                                                                                                                                                   |
| `"d"`                   | ![m20](https://matplotlib.org/stable/_images/m20.png) | thin_diamond                                                                                                                                                                              |
| `"\|"`                  | ![m21](https://matplotlib.org/stable/_images/m21.png) | vline                                                                                                                                                                                     |
| `"_"`                   | ![m22](https://matplotlib.org/stable/_images/m22.png) | hline                                                                                                                                                                                     |
| `0` (`TICKLEFT`)        | ![m25](https://matplotlib.org/stable/_images/m25.png) | tickleft                                                                                                                                                                                  |
| `1` (`TICKRIGHT`)       | ![m26](https://matplotlib.org/stable/_images/m26.png) | tickright                                                                                                                                                                                 |
| `2` (`TICKUP`)          | ![m27](https://matplotlib.org/stable/_images/m27.png) | tickup                                                                                                                                                                                    |
| `3` (`TICKDOWN`)        | ![m28](https://matplotlib.org/stable/_images/m28.png) | tickdown                                                                                                                                                                                  |
| `4` (`CARETLEFT`)       | ![m29](https://matplotlib.org/stable/_images/m29.png) | caretleft                                                                                                                                                                                 |
| `5` (`CARETRIGHT`)      | ![m30](https://matplotlib.org/stable/_images/m30.png) | caretright                                                                                                                                                                                |
| `6` (`CARETUP`)         | ![m31](https://matplotlib.org/stable/_images/m31.png) | caretup                                                                                                                                                                                   |
| `7` (`CARETDOWN`)       | ![m32](https://matplotlib.org/stable/_images/m32.png) | caretdown                                                                                                                                                                                 |
| `8` (`CARETLEFTBASE`)   | ![m33](https://matplotlib.org/stable/_images/m33.png) | caretleft (centered at base)                                                                                                                                                              |
| `9` (`CARETRIGHTBASE`)  | ![m34](https://matplotlib.org/stable/_images/m34.png) | caretright (centered at base)                                                                                                                                                             |
| `10` (`CARETUPBASE`)    | ![m35](https://matplotlib.org/stable/_images/m35.png) | caretup (centered at base)                                                                                                                                                                |
| `11` (`CARETDOWNBASE`)  | ![m36](https://matplotlib.org/stable/_images/m36.png) | caretdown (centered at base)                                                                                                                                                              |
| `"None"`, `" "` or `""` |                                                       | nothing                                                                                                                                                                                   |
| `'$...$'`               | ![m37](https://matplotlib.org/stable/_images/m37.png) | Render the string using mathtext. E.g `"$f$"` for marker showing the letter `f`.                                                                                                          |
| `verts`                 |                                                       | A list of (x, y) pairs used for Path vertices. The center of the marker is located at (0, 0) and the size is normalized, such that the created path is encapsulated inside the unit cell. |
| path                    |                                                       | A [`Path`](https://matplotlib.org/stable/api/path_api.html#matplotlib.path.Path "matplotlib.path.Path") instance.                                                                         |
| `(numsides, 0, angle)`  |                                                       | A regular polygon with `numsides` sides, rotated by `angle`.                                                                                                                              |
| `(numsides, 1, angle)`  |                                                       | A star-like symbol with `numsides` sides, rotated by `angle`.                                                                                                                             |
| `(numsides, 2, angle)`  |                                                       | An asterisk with `numsides` sides, rotated by `angle`.                                                                                                                                    |

```python
styles = markers + [
    r'$\lambda$',
    r'$\bowtie$',
    r'$\circlearrowleft$',
    r'$\clubsuit$',
    r'$\checkmark$']

colors = ('b', 'g', 'r', 'c', 'm', 'y', 'k')
```



![../../_images/line_styles.png](https://matplotlib.org/1.3.1/_images/line_styles.png)



### Customizing the axes label

```python
# Adding labels to axes Y and X
ax.set_xlabel("Time(months)")
ax.set_ylabel("Average temperature(fahrenheit degrees)")
plt.show()

# Adding title to chart
ax.set_title("Weather in Seattle")
plt.show()
```

## Small multiples

### Introduction to data visualization with matplotlib

```python
ax.plot(seattle_weather["MONTH"],
        seattle_weather["MLY-PRCP-NORMAL"],
        color='b')
ax.set_xlabel('Time (months)')
ax.set_ylabel('Precipitation (inches)')
plt.show()
```

![](C:\Users\zhior\AppData\Roaming\marktext\images\2021-12-04-00-16-08-image.png)

```python
ax.plot(seattle_weather["MONTH"], seattle_weather["MLY-PRCP-25PCTL"],
        linestyle='--', color='b')
ax.plot(seattle_weather["MONTH"], seattle_weather["MLY-PRCP-75PCTL"],
        linestyle='--',color=color)
plt.show()
```

![](C:\Users\zhior\AppData\Roaming\marktext\images\2021-12-04-00-23-07-image.png)

```python
fig, ax = plt.subplots()
fig, ax = plt.subplots(3, 2)
plt.show()
```

![](C:\Users\zhior\AppData\Roaming\marktext\images\2021-12-04-00-26-19-image.png)

```python
ax.shape(3,2)
ax[0, 0].plot(seattle_weather["MONTH"],
              seattle_weather["MLY-PRCP-NORMAL"],
              color='b')
plt.show()
```

![](C:\Users\zhior\AppData\Roaming\marktext\images\2021-12-04-00-33-17-image.png)

# color_timestamps
Detect the color of balls and get the timestamps of balls entering or exiting the quadrent

# Design

```python
# Find entry or exit
import typing

import ballpy

quadrants: ballpy.Quadrants

status: ballpy.Status  = ballpy.get_ball_status(quadrants)
```

```python
# Find new ball
import typing

import ballpy

quadrants: typing.List[ballpy.Quadrant]

new_ball: ballpy.Ball = ballpy.get_new_ball(quadrants)
```

```python
# Find color of the ball
import ballpy

ball: ballpy.Ball

color: ballpy.Color = ballpy.get_color(ball)
```

```python
# Find time_stamp
import ballpy

status: ballpy.TimeStamp

time_stamp: ballpy.TimeStamp = ballpy.get_time_stamp(status)
```

```python
# Write information onto text file
import ballpy

file: ballpy.TextFile
status: ballpy.Status
color: ballpy.Color
time_stamp: ballpy.TimeStamp

ballpy.write_status(file, status,)
ballpy.write_color(file, color,)
ballpy.write_time_stamp(file, time_stamp)
```

```python
# Write information onto image
import ballpy

image: ballpy.Image
status: ballpy.Status
time_stamp: ballpy.TimeStamp
ball: ballpy.Ball

new_image: ballpy.Image = ballpy.write_ball_track_on_image(image, ball,)
new_image: ballpy.Image = ballpy.write_time_stamp_on_image(image, time_stamp,)
new_image: ballpy.Image = ballpy.write_status_on_image(image, status,)
```
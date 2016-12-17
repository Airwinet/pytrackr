# pytrackr
Python3 interface to the Trackr API

```python
import time
import trackr

trackr.authenticate('email adress here', 'password here')
devices = trackr.get_trackrs()

for device in devices:
    print(device.name())
    print(str(device.last_known_location()))
    time.sleep(60)
    device.update_state_from_api()
    print(str(device.last_known_location()))

```

## nostalgia-timeline

This repo contains the timeline app for [nostalgia](https://nostalgia-dev.github.io).

### Setup

    git clone https://github.com/nostalgia-dev/timeline
    pip install -r requirements.txt

Next, get some [sources connected](https://github.com/nostalgia-dev/nostalgia#available-data-bindings).

Then, make sure you are loading the sources in `~/nostalgia_data/nostalgia_entry.py`.

For example, to load [Fitbit](https://github.com/nostalgia-dev/nostalgia_fitbit) and [Chrome History](https://github.com/nostalgia-dev/nostalgia_chrome) after setting up those sources:

```python
# File contents of ~/nostalgia_data/nostalgia_entry.py below
from nostalgia.sources.fitbit.heartrate import FitbitHeartrate
from nostalgia.sources.chrome_history import WebHistory

heartrate = FitbitHeartrate.register()
web_history = WebHistory.register()
```

### Running

    python timeline.py

### Updating the code

    git pull

### Screenshots

<img src="https://raw.githubusercontent.com/nostalgia-dev/timeline/master/timeline1.jpg" />

Driving, music, heartrate (my heartrate got lower with less traffic):

<img src="https://raw.githubusercontent.com/nostalgia-dev/timeline/master/less_traffic_jam.png" />

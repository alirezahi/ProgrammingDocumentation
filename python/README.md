Python
========================
## Daylight Saving

For zones with daylight savings time, python standard libraries do not provide a standard class, so it is necessary to use a third party library. pytz and dateutil are popular libraries providing time zone classes.

~~~python
from datetime import datetime, timedelta 
import pytz
PT = pytz.timezone('US/Pacific')
dt_pst = PT.localize(datetime(2015, 1, 1, 12)) 
dt_pdt = PT.localize(datetime(2015, 11, 1, 0, 30)) 
print(dt_pst)
# 2015-01-01 12:00:00-08:00
print(dt_pdt)
# 2015-11-01 00:30:00-07:00
dt_new = dt_pdt + timedelta(hours=3) 
# This should be 2:30 AM PST print(dt_new)
# 2015-11-01 03:30:00-07:00
dt_corrected = PT.normalize(dt_new)
print(dt_corrected)
# 2015-11-01 02:30:00-08:00
~~~

## Run Server
To start a server just execute the following command from your command line:
~~~shell
python -m http.server
~~~

To consider a specific port we can set it like this:
~~~shell
python -m http.server 8080
~~~

Why do we have to run a server? 
Well, we can test our html file and its link so it will be alright
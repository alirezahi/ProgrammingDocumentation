Python
========================
# Daylight Saving

For zones with daylight savings time, python standard libraries do not provide a standard class, so it is necessary to use a third party library. pytz and dateutil are popular libraries providing time zone classes.

~~~python
from datetime import datetime, timedelta import pytz
PT = pytz.timezone('US/Pacific')
dt_pst = PT.localize(datetime(2015, 1, 1, 12)) dt_pdt = PT.localize(datetime(2015, 11, 1, 0, 30)) print(dt_pst)
# 2015-01-01 12:00:00-08:00
print(dt_pdt)
# 2015-11-01 00:30:00-07:00
dt_new = dt_pdt + timedelta(hours=3) # This should be 2:30 AM PST print(dt_new)
# 2015-11-01 03:30:00-07:00
dt_corrected = PT.normalize(dt_new)
print(dt_corrected)
# 2015-11-01 02:30:00-08:00
~~~
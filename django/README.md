### Find duplicate models by a field(in this example: `name`):

~~~python3
from django.db.models import Count
MyModel.objects.values('name')
               .annotate(Count('id'))
               .order_by()
               .filter(id__count__gt=1)
~~~

## Django management command with arbitrary optional params

Looking for a management command which accepts optional parameters, then you are in luck.

**import** logging  
  
**from** django.core.management.base **import** BaseCommand  
**from** locl.locations.models **import** Location  
**from** locl.locations.tasks **import** fetch\_metrics\_for\_location  
  
logger = logging.getLogger(\_\_name\_\_)  
  
  
**class** Command(BaseCommand):  
    help = **'Fetch Location Data'  
  
    def** add\_arguments(self, parser):  
        *\# Optional argument* parser.add\_argument(**'-ids'**, **'--location\_ids'**, type=str, nargs=**'+'**, help=**'Debug location data fetch from google'**)  
  
    **def** handle(self, \*args, \*\*kwargs):  
        location\_ids = kwargs\[**'location\_ids'**\]

This management command can be run using any of these terminal commands. I’m using location\_stats as my file has this name. use your own file name in which you would place the above code

**python manage.py location\_stats**

**python manage.py location\_stats -ids value1**

**python manage.py location\_stats -ids value1 value2**
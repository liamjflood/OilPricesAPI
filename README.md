# OilPricesAPI

import pandas as pd
import requests

data = requests.get('http://api.eia.gov/series/?api_key=801c30520735b2cec61c5e25c13f281e&series_id=PET.RBRTE.D').json()
df = pd.DataFrame(data['series'][0]['data'],columns=["Date", "$ (Europe Brent Spot Price FOB, Daily)"])

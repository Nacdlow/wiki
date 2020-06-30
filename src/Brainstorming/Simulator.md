## Simulator logic

### Time simulation

The simulated environment will start at the current time, running normal time.
In the simulator app, we will be able to speed up, change, or stop the time.
This will reflect Darksky's real data. The simulated home will also have a
location, which is used for getting the weather data.

### Weather simulation

Weather will get pulled from Darksky, which will also return an hourly
forecast of the weather. This can be used in both simulating the weather, and
also for the smart home app and its suggestions.  

Darksky provides weather/natural disaster alerts, this data can be used. In the
simulator page, you should be able to override the Darksky temperatures and
values, and simulate alerts.

### Temperatures

If a door or window is opened, the room's temperature will slowly start to
match the outside temperature.

Also, this applies to temperature control. When the temperature control is
running, it will slowly adjust the room temperature to the set temperature.

The temperature control is also able to "fight" with the outside weather if
both windows/main door and temp control is running.

If both temperature control (heating/cooling) and windows/doors are closed,
then the room temperatures will very slowly change towards the outside
temperature. Also opening the windows for a minute or two can significantly
drop the temperature of the rooms.

### Power generation

Depending on the cloud coverage (pulled from the weather data), the power
generation will vary (under the max solar power generation capacity, in the
simulated home).

### Power consumption

Depending on the devices running on the home, the power consumption will
change. There will also be a "baseline" power consumption, which will count in
fridges and other appliances. This baseline power consumption will vary
depending on the time of day, based on an average home power consumption graph.


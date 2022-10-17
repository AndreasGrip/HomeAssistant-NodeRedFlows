# HomeAssistant-NodeRedFlows
Flows that I have created for NodeRed

Tibber - Will use HA Tibber integration to fetch the prices for the current and when available, next day. Will make this available in global variables as well as the best prices for anything that will run 1,2,3,4,5,6 etc. hours. Only prices for the future will be available.

Dishwasher - Using Home Connect integration will control a Bosch smu4haw48s but any supported model should work, possibly with minor modifications to get the correct washing program names and powerconsumption (please measure yourself, bosh data is not correct). Home Connects limit of 1000api calls per 24h can be a problem while testing.
- Will start the dishwasher at the time it will be cheapest by using the prices fetched from Tibber
- Once an hour will start the dishwasher to get a update on the door status until the door has been opened after a finished wash.
- Will only start the dishwasher again if the door has been opened since last finished wash.
- Once the door has been opened calculate when to start the dishwasher next time and what program to use (some times power is cheap for just 1-2hours and then it's better to use a faster but more powerconsuming program.
- Once the time to start the next wash, start the washingmashine and run the given program.

# NEST style thermostat Dashboard widget for Node-red

This widget is based on the widget developed by automatikas in [GITHUB](https://github.com/automatikas/Node-red-Nest-thermostat) but has been encapsulated in a single installable node through the node-red palette.

If you have made heating or cooling controls on Node-red you will need nice thermostat widget to display and control your device via Node-red dashboard.

![thermostat](https://user-images.githubusercontent.com/15208705/128023309-bf8d81c4-17be-40a7-912e-ec3fe8ce34a9.png)

Fully responsive design. Touch enabled set-point makes it even more interactive. Press and hold finger or mouse and it will activate the set-point sliding function.

Also it has several display modes like heating, cooling and away. It makes it more interactable and user intuitive. For ECO friendly folks there is possible to turn on and off that little green leaf.

![heating](https://user-images.githubusercontent.com/15208705/128031236-9d219f97-c6fc-4cee-84bd-82f597b53c54.png)
![cooling](https://user-images.githubusercontent.com/15208705/128031234-ee0b535b-c40b-4278-8f57-6f6237847127.png)
![away](https://user-images.githubusercontent.com/15208705/128031229-7ad1a5c1-af22-4a1d-bf8d-db6913c1f004.png)

## What data can I push in and out:

You can push the folowing values in json format. When target temperature is changed from UI node will push new values in the same structure in the output.

- **`ambient_temperature`** your temperature readings numeric payloads.
- **`target_temperature`** your thermostat setpoint numeric payloads.
- **`hvac_state`** string (`off`, `heating`, `cooling`) payload.
- **`has_leaf`** boolean (`true`, `false`) payloads.
- **`away`** boolean (`true`, `false`) payloads.

```
msg.payload = {
    "ambient_temperature": 21.1,
    "target_temperature": 23,
    "hvac_state": "heating",
    "has_leaf": false,
    "away": false
};

msg.topic = "update";

```

# Dashboard-Home-AssistantConfig
Dashboard for my tiny smart home 🏠. Maybe in an OVER-COMPLICATED way 💥

Hass.io running on Proxmox VE. </br>
2GB of Ram, 1 Socket & 1 Cores on an old HP Thin Client t610 📠 <i>(same one as the <a href="https://github.com/niccolobusato/Main-Home-AssistantConfig">Main HA</a>)</i>. 
</br>
Currently running two Hass.io instances, the Dashboard is showed below but it's only a "one page" shwoing the most relevant information from the Main one that you can find <a href="https://github.com/niccolobusato/Main-Home-AssistantConfig">here</a>.
</br> </br>

## Main View
<img src="/www/images/DSCF0027.gif?raw=true">

## Important Note: No Options to Upgrade HA. 💥
### Ha Companion App on iPad's mini support HA until v.0.94.4
#### Dashboard are displaying on a set of iPad's mini, apple dropped the updates for those versions and HA is not releasing no more app update 'cause the low iOS firmware version installed on those. Fortunatelly LovelaceUi does work but very restricted because you can't add any "custom_card" or any fancy plugin like "Compact Custom Header", they will block the loading of the all UI.
</br>
Using a combinations of "input_select", template "sensor", template "binary_sensor" and some scripts i can (quite) easily get it to work as i wanted.
</br>
Everything is controlled via Node-RED hosted on the Main HA. Every time anything changes on the Main instance Node-RED will change on the Dashboard instance the "input_select" option via "input_select.select_option" service in Node-RED. Same thing will do when something is going to be tapped on the Dashboard it will change the "input_select" option via "input_select.select_option" service with a script, Node-Red will notice the change and send a command to the Main instance effecting the changes.

## How it works
<img src="/www/images/FLOW.gif?raw=true">


 




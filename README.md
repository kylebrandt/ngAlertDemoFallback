# Demo Backup for NG Alert

## Add An Alert and see Instances

(ngalert feature flag needs to be enabled)

1. Go to list of Alert rules

![image of selecting alert rules](alert_side_panel_alert_list.jpg)

2. From the list view, create New NG Alert

![image of add ng alert button in alert rules list view](alert_list_new_ng_alert.jpg)

3. Draw the owl, I mean, add queries and expressions, set the condition to a RefID/Query that returns labels numbers, name it, and hit save (test does not work from UI yet, but would show up in Alerting instances tab (Label, and True False)):

![an alert defintion with prometheus, test data source, and expressions](an_alert_def_with_expr.jpg)

4. On a branch of mine, you can list alert instances being returned from the definition running in the background by Grafana's server scheduler (There is also a REST API for this):

![image of filtered instance list](filtered_instance_list.jpg)

5. You can go back and edit the alert from the list view

![image of edit alert button](edit_alert_button.jpg)

## Misc

Things API can do but UI Can't yet:
 - Testing of instances not saved (although that may be merged soon)
 - Pause / unpause alert definitions
 - Create queries with different time ranges, compare them with expressions

Alert Definition, and a Dashboard using a manual copy of the same queries:

![image of above description](dashboard_and_alert.jpg)

Scheduler running alert definitions and creating instances (which are saved):

![image of above description](grafana_server_console_output.jpg)

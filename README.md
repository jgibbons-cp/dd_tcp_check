# dd_tcp_check
Sample Datadog [tcp_check](https://docs.datadoghq.com/integrations/tcp_check/?tab=host) config and 
[monitor](https://docs.datadoghq.com/monitors/monitor_types/) config  
  
This sample will show how to get network timing between hosts 
in Datadog.

Check Configuration
--

1) The base conf.yaml will go in tcp_check.d/conf.yaml of the agent
   [configuration directory](https://docs.datadoghq.com/agent/guide/agent-configuration-files/?tab=agentv6v7#agent-configuration-directory)
2) To configure it modify the following lines:  
  a) In line 20 - configure your name to something meaningful such as
   <host>_tcp_check  
   b) In line 26 add the host or IP  
   c) In line 31 add the port to use for the check  
3) Restart the agent
4) Confirm the metric is flowing to Datadog. In the 
   [metric explorer](https://app.datadoghq.com/metric/explorer?from_ts=1614292728125&to_ts=1614296328125&live=true&page=0&is_auto=false&tile_size=m&exp_agg=avg&exp_row_type=metric) 
   enter in network.tcp.response_time for the metric to graph over the 
   url:<tag>  
5) Export to a dashboard then click then click the cog on the widget and choose create monitor.  

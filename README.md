# Monitoring Plugin: Number of connections

### Description

Monitor the number of open sockets on your server.

For example:
    # ./check_connections  -p 443 -w 400 -c 500 -d    
    established tcp connections (5) is ok|'max'=500;;;;0 'total'=169;;;;0 'established'=5;;;;0 'time_wait'=164;;;;0 'close_wait'=0;;;;0 'fin_wait'=0;;;;

This will monitor the current https connections and throws a warning with 400 and more connectiond and critical with 500 and more.
You can also gather performance data if you specify -d.

### Usage
    -h      Show this message
    -p      Port
    -w      Max established connections (warning)
    -c      Max established connections (critical)
    -d      Performance Data

### Install 

Copy check_connections to your plugin folder and create a service/exec in your monitoring engine. 

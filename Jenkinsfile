pipeline
{
  agent any
  stages('checking'){
    steps{
#!/bin/bash

echo "====================================="
echo "     *** SERVER HEALTH CHECK ***"
echo "====================================="

echo
echo "Hostname:"
hostname

echo
echo "Uptime:"
uptime

echo
echo "Disk Usage:"
df -h /

echo
echo "Memory Usage:"
free -h

echo
echo "Top Processes:"
ps aux --sort=-%cpu | head -6
    }
  }
}

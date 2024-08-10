KIWI - Syslog Sender tool to Windows. Excellent to troubleshooting Sentinel LogForwarders.

For Linux, consider the command bellow:
logger -p local4.warn -P 514 -n 192.168.1.3 --rfc3164 -t CEF "0|DeviceVendorName-Test|DeviceProduct-Test|common=event-format-test|end|TRAFFIC|1|rt=$common=event-formatted-receive_time"
![image](https://github.com/user-attachments/assets/87133046-d289-4d19-9f5a-164425f6158c)

Listenting to run on logforwarder:
sudo tcpdump -i any port 514 -1 -A -vv &

More details: https://charbelnemnom.com/simulate-validate-cef-logs-microsoft-sentinel/

# logFilter
threat detection for logs in YAML format

Function group_timestamps_by_ip iterates through a copy of the YAML file and groups timestamps per IP address. Returns a dictionary; key == IP, value == array of timestamps. Has ability to filter timestamps by the action performed(not required)

Function detect_suspicious_ips with default threshold of 60 seconds and default number of attempts(3) necessary to flag the IP address uses a sliding window method to check whether an IP address has made more than 3(default) attempts in 60 seconds. Returns an array of suspicious IPs that broke the conditions.



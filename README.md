# HNG TASk 5

## devopsfetch Documentation

# Introduction

"devopsfetch" is a command line tool much like ls and grep designed for devops professionals to collect and display system info including active ports, user logins, Nginx configurations, Docker images, and container statuses. It also includes a systemd service for continuous monitoring and logging.

## Installation and Configuration


1. **Install**:
###  Clone the Repository

Clone the repository from GitHub and navigate into the directory.

```bash
git clone https://github.com/otie16/HNG-task-5.git
cd HNG-task-5.git
```

Run this command on the terminal
```bash
    ./installation_script.sh
```

2. **Save the `devopsfetch` Script**:
    Save the provided `devopsfetch` script content in `/usr/local/bin/devopsfetch`.

3. **Make the Script Executable**:
```bash
    sudo chmod +x /usr/local/bin/devopsfetch
```

4. **Enable the Systemd Service**:
```bash
    sudo systemctl enable devopsfetch
    sudo systemctl start devopsfetch
```

## Usage Examples
Display Active Ports and Services

```bash 
devopsfetch -p
```

Provide Detailed Information about a Specific Port
```bash
devopsfetch -p <port_number>
```

List All Docker Images and Containers
```bash
devopsfetch -d
```

Provide Detailed Information about a Specific Container
```bash
devopsfetch -d <container_name>
```

Display All Nginx Domains and Their Ports
```bash
devopsfetch -n
```

Provide Detailed Configuration Information for a Specific Domain
```bash
devopsfetch -n <domain>
```

List All Users and Their Last Login Times
```bash
devopsfetch -u
```

Provide Detailed Information about a Specific User
```bash
devopsfetch -u <username>
```

Display Activities within a Specified Time Range
```bash
devopsfetch -t 2024-07-18 2024-07-22
```

Display Activities for a Specific Date
```bash
devopsfetch -t 2024-07-21
```

Display Help Message
```bash
devopsfetch -h
```

## Logging Mechanism
# Log Retrieval
Logs are stored in `/var/log/devopsfetch.log`. To view the logs, use:

```bash
cat /var/log/devopsfetch.log
```
# Log Rotation
Logs are rotated daily and compressed to save space. The log rotation configuration is set up in `/etc/logrotate.d/devopsfetch`.
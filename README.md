# HNG TASk 5

## devopsfetch Documentation

# Introduction

"devopsfetch" is a command line tool much like ls and grep designed for devops professionals to collect and display system info including active ports, user logins, Nginx configurations, Docker images, and container statuses. It also includes a systemd service for continuous monitoring and logging.

## Installation and Configuration
## Prerequisites
Ensure you have the following dependencies installed on your system:

* net-tools
* jq
* docker.io
* nginx
* Installation
* Update package list and install dependencies:

1. **Install and Dependencies**:
```bash
    sudo apt-get update
    sudo apt-get install -y net-tools jq docker.io nginx
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
# Failed Logins

A Linux CLI tool to detect failed SSH login attempts and identify potential attacks.

## Features

- Show recent failed login attempts
- Detect top attacking IP addresses
- Filter IPs by number of failed attempts
- Supports both auth.log and journalctl
- Clean formatted output

## Requirements

Linux system with: grep, awk, sort, uniq, head

## Usage

### Show recent failed attempts

./failed-logins.sh

### Show top attacking IPs

./failed-logins.sh --top

### Filter by number of attempts

./failed-logins.sh --threshold 5

## Example Output


FAILED LOGIN ATTEMPTS

Mar 19 10:22:31 sshd[1234]: Failed password for invalid user admin from 192.168.1.50

Mar 19 10:22:35 sshd[1235]: Failed password for root from 192.168.1.50

TOP OFFENDING IPs

192.168.1.50   → 12 attempts

10.0.0.2       → 5 attempts

## Author

Jose Daniel Fernández - GitHub: https://github.com/Daniel-Fernandez11

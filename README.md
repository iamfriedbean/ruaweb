# ruaweb - aRe yoU A WEB
Fast Web/HTTP checker using its own custom list of web ports (e.g. 80,443,8080,8008 and lots,lots more) use by different technologies identified from various testing engagements.
It takes a list of domains and checks for running web service at different ports. Only domains with running web service (active) will be returned.

## Basic Usage
```
echo 'github.com' | ruaweb
cat domains.txt | ruaweb
```

## Parallelism
Number of threads can be set using the -threads flag. It uses 5 threads by default.
```
cat domains.txt | ruaweb -threads 30
```

## Timeout
Connectivity time out can be specified using the -timeout flag in seconds. It uses 1 second by default.

```
cat domains.txt | ruaweb -threads 30 -timeout 5

```

## Output
The results are displayed as standard output. It returns the URL including the identified protocol(http/https),port used, status code, http title and server if available.

```
echo 'github.com' | ruaweb

https://github.com:443, 200, "GitHub: Let’s build from here · GitHub", GitHub.com

```
## Installation

Part of Beanscan Web Attack Surface Scanner. See beanscan repository.

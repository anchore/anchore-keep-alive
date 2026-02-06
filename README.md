# anchore-keep-alive

A minimal Go program that stays running until it receives a termination signal
(SIGTERM or SIGINT).

## Usage

This is useful in container environments where you need a lightweight process to
keep a container alive, e.g. while executing STIG profiles against a running
container image.

## Building

```bash
go build -o anchore-keep-alive .
```

## Running

```bash
./anchore-keep-alive
```

The process will run indefinitely until it receives SIGTERM or SIGINT (Ctrl+C).

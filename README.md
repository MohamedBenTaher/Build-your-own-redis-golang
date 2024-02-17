# Redis-like Server in Go

This project is a simple, educational implementation of a Redis-like in-memory key-value store written in Go.

## Features

- In-memory storage of key-value pairs.
- Basic command support: `SET`, `GET`, `HSET`, `HGET`, `HGETALL`, `MULTI`, `EXEC`.
- Persistence to disk using an append-only file (AOF).

## Usage

To start the server, run:

```sh
go run *.go
```

The server listens on port 6379.

Commands are sent to the server in the Redis protocol. For example, to set a key-value pair, send:
    
```*3
$3
SET
$3
key
$5
value
```
And to get a value by key, send:
```
*2
$3
GET
$3
key
```
THE Server allows the follwoing commands:
- SET
- GET
- HSET
- HGET
- HGETALL

You can try them and see the results in the server terminal.

# Project Structure
- main.go: The entry point of the server. It sets up the server and handles incoming connections.
- handler.go: Contains the command handlers for the different commands that the server supports.
- aof.go: Handles reading from and writing to the AOF.
- resp.go: Contains functions for parsing and serializing data in the Redis protocol.
- mycommands.txt: An example of commands sent to the server in the Redis protocol.

# Dependencies
This project uses Go's standard library. No additional dependencies are required.

# Contributing
Contributions are welcome. Please submit a pull request or create an issue to discuss the changes you want to make.

# License
This project is licensed under the MIT License.


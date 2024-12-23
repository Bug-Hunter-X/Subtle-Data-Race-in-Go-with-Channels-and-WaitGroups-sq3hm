# Subtle Data Race in Go with Channels and WaitGroups

This repository demonstrates a subtle data race in a Go program that uses goroutines, channels, and WaitGroups. The race condition is not immediately obvious, highlighting the importance of careful concurrency programming.

## Description

The `bug.go` file contains the buggy code. The race condition happens because the `close(ch)` call might not always happen before the for...range loop in the second goroutine finishes. This can result in a deadlock or inconsistent results.

The `bugSolution.go` file contains a corrected version of the code that addresses the data race and ensures proper synchronization.

## How to Run

1. Clone the repository:
   `git clone <repository_url>`
2. Navigate to the repository directory.
3. Run the buggy code:
   `go run bug.go`
4. Run the corrected code:
   `go run bugSolution.go`

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.
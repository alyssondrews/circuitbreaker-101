# Circuit Breaker 101 - Ping? Pong

## Overview

This repository presents a straightforward Go project illustrating the foundational concept and application of the Circuit Breaker pattern. Integral to ensuring the resilience of services, this project breaks down its components into:
- A mock server (`server()`) which simulates the behavior of a service experiencing intermittent failures.
- A function (`DoReq()`) making requests to the above server.
- Circuit breaker logic (`main()`) to shield the application from repeated failures.

## What is a Circuit Breaker?

The Circuit Breaker is a design pattern frequently used in software development, especially in microservices architecture, to enhance system resilience. It acts as a proxy or intermediary for calls to external systems or services. If a service experiences frequent failures, the circuit breaker 'trips' or 'opens,' pausing all requests to the problematic service for a predefined time. This behavior prevents the system from making futile calls to a failing service, conserves system resources, and can potentially aid the failing service in recovering.

## How to Run the Project

1. **Prerequisites**: Ensure you have Go installed on your machine.

2. **Clone & Navigate**:
```bash
git clone https://github.com/alyssondrews/circuitbreaker-101.git
cd circuitbreaker-101
```

3. **Install Dependencies**:
   This project requires the `gin-gonic/gin` and `sony/gobreaker` Go packages. To install these dependencies, run:
```bash
go get -v ./...
```

4. **Run the Program**:
```bash
go run main.go
```

Upon execution, you'll observe the mock server's behavior and how the Circuit Breaker reacts to consecutive failures.

## Conclusion

Kudos! You've successfully delved into and executed a Go project showcasing the Circuit Breaker pattern. This fundamental introduction acts as a stepping stone to more intricate and large-scale systems that harness the Circuit Breaker pattern to fortify their resilience.

For a deeper dive and broader applications, peruse the extensive documentation and versatile features of the `gobreaker` library and other resilience patterns in Go.

Happy building! 🚀

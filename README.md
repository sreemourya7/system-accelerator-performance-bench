# system-accelerator-performance-bench
Benchmarking PCIe, NUMA, memory-transfer, and multi-GPU performance for accelerator systems.

# System-Level Accelerator Performance Benchmarking

A hands-on performance engineering project for studying accelerator behavior across the full system stack.

## Goals

This project measures and analyzes:

- PCIe host-to-device and device-to-host bandwidth
- Pageable vs pinned host memory
- Asynchronous CUDA transfers
- Compute/communication overlap
- NUMA topology
- GPU topology
- Multi-GPU peer-to-peer communication
- System-level performance bottlenecks

## Current Benchmarks

### 1. PCIe Bandwidth
Compares:

- Pageable H2D
- Pageable D2H
- Pinned H2D
- Pinned D2H

### 2. Async Transfer + Compute
Measures end-to-end latency for:

- H2D transfer
- GPU compute
- D2H transfer

using CUDA streams and asynchronous copies.

### 3. System Topology
Collects:

- PCIe device topology
- NVIDIA GPU topology
- NUMA configuration
- GPU PCI bus IDs

## Planned Extensions

- Multi-stream overlap
- GPU peer-to-peer bandwidth
- NUMA affinity benchmarking
- Multi-GPU scaling
- Nsight Systems profiling
- Automated benchmark result collection
- Latency/throughput plots

## Build

```bash
mkdir build
cd build
cmake ..
make -j

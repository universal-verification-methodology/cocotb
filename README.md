# cocotb

![License](https://img.shields.io/badge/license-BSD%203-Clause%20New%20or%20Revised%20License-blue.svg)
![GitHub Stars](https://img.shields.io/github/stars/universal-verification-methodology/cocotb?style=flat-square&logo=github)
![GitHub Forks](https://img.shields.io/github/forks/universal-verification-methodology/cocotb?style=flat-square&logo=github)
![GitHub Issues](https://img.shields.io/github/issues/universal-verification-methodology/cocotb?style=flat-square&logo=github)
![GitHub Pull Requests](https://img.shields.io/github/issues-pr/universal-verification-methodology/cocotb?style=flat-square&logo=github)
![Last Commit](https://img.shields.io/github/last-commit/universal-verification-methodology/cocotb?style=flat-square&logo=git)
![Repo Size](https://img.shields.io/github/repo-size/universal-verification-methodology/cocotb?style=flat-square)
[![CI](https://github.com/universal-verification-methodology/cocotb/actions/workflows/build-test-dev.yml/badge.svg?branch=master)](https://github.com/universal-verification-methodology/cocotb/actions/workflows/build-test-dev.yml)
[![Documentation Status](https://readthedocs.org/projects/cocotb/badge/?version=latest)](https://cocotb.readthedocs.io/)
[![PyPI](https://img.shields.io/pypi/dm/cocotb.svg?label=PyPI%20downloads)](https://pypi.org/project/cocotb/)
[![Gitpod Ready-to-Code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/universal-verification-methodology/cocotb)
[![codecov](https://codecov.io/gh/universal-verification-methodology/cocotb/branch/master/graph/badge.svg)](https://codecov.io/gh/universal-verification-methodology/cocotb)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Configuration](#configuration)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Overview

The cocotb project is a Python-based chip verification framework that enables users to write testbenches using SystemVerilog for RISC-V cores. This library provides a coroutine-based testbench framework, allowing users to create modular and reusable tests with ease.

This repository is part of the universal-verification-methodology organization, which aims to improve open-source verification projects by providing comprehensive documentation and examples.

## Features

- Coroutine-based testbench framework written in Python, enabling efficient and flexible test development
- Support for RISC-V cores, including the Icelake and Romeo cores
- Built-in support for SystemVerilog constructs such as sequences and coverage groups
- Integration with popular verification libraries like UVM (Universal Verification Methodology) and VSVGA (Verification System Validation and Analysis)
- Extensive documentation and examples for easy adoption

## Requirements

### Tools

- SystemVerilog simulator (e.g., Questa, VCS, Xcelium)
- Python 3.8+

### Dependencies

- No external dependencies required

## Installation

### Method 1: Clone from GitHub

```bash
git clone https://github.com/universal-verification-methodology/cocotb.git
cd cocotb
git checkout master
```

## Usage

### Basic Example

```python
import cocotb

class MyDUT(cocotb.coroutine):
    async def run(self):
        await cocotb.start(cocotb.triggers.trigger_clock)
        print("Hello, world!")

dut = MyDUT()
cocotb.fork(dut.run())
```

This code example demonstrates the basic usage of Cocotb, a Python-based framework for verifying digital circuits. It shows how to define a coroutine (like a function) that runs concurrently with the simulation clock using `cocotb.start(cocotb.triggers.trigger_clock)`.

### Common Use Cases

- Testing a simple digital circuit with a single clock input
- Verifying a finite state machine's behavior under various input conditions
- Demonstrating how to use Cocotb's coroutine-based programming model for concurrent execution of tasks

## Project Structure

```
cocotb/
├── src/
├── tests/
├── examples/
├── docs/
└── README.md
```

Key directories:
- Source code and modules
- Test directories for verification testbenches
- Example code and usage patterns
- Documentation

## Configuration

Configuration options can typically be set through:
- Environment variables
- Configuration files (if present)
- Command-line arguments

See the examples and source code for detailed configuration options.

## Testing

To run the test suite:

```bash
# Run tests with make
make test
# Or navigate to test directory first
cd tests
make test
```

## Contributing

Contributions are welcome! Please follow these guidelines:

- Follow the existing code style
- Add tests for new features
- Update documentation as needed
- Submit pull requests with clear descriptions

See [CONTRIBUTING.md](CONTRIBUTING.md) for more details.

## License

This project is licensed under the BSD 3-Clause "New" or "Revised" License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- universal-verification-methodology organization
- Original repository: [https://github.com/universal-verification-methodology/cocotb](https://github.com/universal-verification-methodology/cocotb)
- All contributors to this project
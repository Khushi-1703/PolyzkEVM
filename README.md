# ZK SNARK Designer

This README provides an overview of the CIRCOM code that defines a circuit template for checking if `c` is the correct multiplication of `a` and `b`.

## Table of Contents

- [Introduction](#introduction)
- [Circuit Description](#circuit-description)
- [Templates](#templates)
  - [Multiplier2](#multiplier2-template)
  - [NOT](#not-template)
  - [AND](#and-template)
  - [OR](#or-template)
- [Usage](#usage)
- [Credits](#credits)
- [License](#license)

## Introduction

This CIRCOM code defines a circuit template that verifies whether the value `c` is the result of multiplying values `a` and `b`. The circuit template utilizes custom gate templates for basic logical operations such as AND, NOT, and OR.

## Circuit Description

The circuit consists of the following main components:
- `Multiplier2` template: This is the main circuit template that checks if `c` is the multiplication of `a` and `b`.
- `NOT` template: Implements the NOT gate.
- `AND` template: Implements the AND gate.
- `OR` template: Implements the OR gate.

## Templates

### Multiplier2 Template

The `Multiplier2` template is the central component of the circuit. It verifies the multiplication relationship between `a`, `b`, and `c`. The template performs the following steps:

1. Utilizes the `AND` gate template to compute the logical AND of `a` and `b`.
2. Applies the `NOT` gate template to negate the value of `b`.
3. Uses the `OR` gate template to calculate the logical OR of the output of the `AND` gate and the negated `b`.
4. The result of the `OR` operation is considered as the output `q`.

### NOT Template

The `NOT` template implements a basic NOT gate, which takes an input `in` and produces the negation of that input.

### AND Template

The `AND` template represents a basic AND gate. It takes two inputs `a` and `b`, and the output is the result of the logical AND operation between the inputs.

### OR Template

The `OR` template is a basic OR gate. It accepts inputs `a` and `b` and produces the result of the logical OR operation between the inputs.

## Usage

To use this circuit template, you can instantiate the `main` component, which is an instance of the `Multiplier2` template. Assign the appropriate values to `a`, `b`, and `c`, and the circuit will evaluate whether `c` is indeed the multiplication of `a` and `b`.

Please ensure you have the required environment and tools to compile and execute the CIRCOM code.

## Credits
This project is created by ***[Khushi Gupta](https://github.com/Khushi-1703)***.

## License
This project is licensed under the ***[MIT License](https://github.com/Khushi-1703/SmartContractManagement/blob/main/LICENSE)***.

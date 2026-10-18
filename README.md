# Cash Register — OOP Part 2 Lab

A Python `CashRegister` class that simulates the core functions of an
e-commerce cash register: adding items, applying percentage discounts,
and voiding the most recent transaction.

Built as part of the **Moringa Module 4 — Object Oriented Programming (Part 2)**
lab.

---

## Table of Contents

- [Description](#description)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Screenshots](#screenshots)
- [Project Structure](#project-structure)
- [Testing](#testing)
- [Author](#author)
- [License](#license)

---

## Description

This lab builds a `CashRegister` object using Python classes. The register
tracks a running total, a list of purchased items, an optional percentage
discount, and a history of transactions so that the last sale can be
undone if needed.

The goal of the exercise was to practice **object-oriented design** —
encapsulating state (attributes) and behaviour (methods) inside a single
class — and to apply input validation at object construction time.

---

## Features

- **Configurable discount** — pass an integer `0–100` at construction.
  Invalid values print `"Not valid discount"` and default to `0`.
- **Add items** — `add_item(item, price, quantity)` updates the total,
  the items list, and the transaction history in one call.
- **Apply a discount** — `apply_discount()` applies the configured
  percentage to the current total. If no transactions exist yet it
  prints `"There is no discount to apply."`
- **Void the last transaction** — `void_last_transaction()` reverses the
  most recent `add_item` call, restoring both `total` and `items`. If
  there is nothing to undo it prints `"There is no transaction to void."`
- **Transaction history** — every sale is stored as a dictionary with
  `item`, `price`, and `quantity`, so undo is exact.

---

## Tech Stack

- **Python 3.10+**
- **pytest** (for the provided test suite)

> Note: the lab instructions mention `npm install`, but this is a
> Python-only lab — the repository does not contain a `package.json`.
> Use `pytest` instead (see [Testing](#testing)).

---

## Installation

Clone the repo and move into it:

```bash
git clone https://github.com/<your-username>/oop-p2-cash-register-lab.git
cd oop-p2-cash-register-lab
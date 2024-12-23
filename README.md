# React Native AsyncStorage Data Corruption Bug

This repository demonstrates a common bug in React Native applications involving AsyncStorage and provides a solution to prevent data corruption.

## Bug Description

When storing complex objects or arrays in AsyncStorage without proper serialization and deserialization, data corruption can occur, leading to inconsistencies and unexpected data loss. AsyncStorage only supports string storage. This bug shows how to reproduce this data corruption. The bug occurs because the data is not properly stringified before being stored and parsed after being retrieved from AsyncStorage. 

## Solution

The solution involves correctly stringifying data before storing and parsing it after retrieval using `JSON.stringify` and `JSON.parse`, respectively. This ensures data integrity and prevents corruption. Handle potential parsing errors with a `try...catch` block. 

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run the application on a simulator or device.
4. Observe the inconsistent data after several store and retrieve operations.
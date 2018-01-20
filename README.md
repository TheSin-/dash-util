# terracoin-util

[![npm version](https://img.shields.io/npm/v/terracoin-util.svg)](https://www.npmjs.com/package/terracoin-util)
[![Build Status](https://travis-ci.org/terracoin/terracoin-util.svg?branch=master)](https://travis-ci.org/terracoin/terracoin-util)
[![Dependency Status](https://david-dm.org/terracoin/terracoin-util.svg)](https://david-dm.org/terracoin/terracoin-util)

**Utility functions for Terracoin hashes and targets**

## Usage

`npm install terracoin-util`

### Methods

#### `toHash(hex)`

Takes a hex string that contains a Terracoin hash as input, and returns a Terracoin-protocol-friendly little-endian Buffer. Throws an error if the hex string is not of length 64 (representing a 256-bit hash).

#### `compressTarget(target)`

Converts the difficulty target `target` to its compact representation (used in the "bits" field in block headers). `target` should be a `Buffer` (little-endian, the zeroes should be at the end). Returns a `number`.

#### `expandTarget(bits)`

Converts the compressed target integer `bits` to its target hash representation. Returns a `Buffer`.

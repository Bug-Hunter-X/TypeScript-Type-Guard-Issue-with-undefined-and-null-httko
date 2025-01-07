# TypeScript Type Guard Issue with undefined and null

This repository demonstrates a subtle issue with TypeScript's type guards when dealing with both `null` and `undefined`.  A simple null check doesn't automatically account for `undefined` values, potentially leading to runtime errors.

## The Bug
The `greet` function is designed to handle both string inputs and `null` values.  However, if an `undefined` value is passed, the type guard `name === null` fails, and TypeScript doesn't provide sufficient protection against this scenario.  This results in a runtime error when trying to use the undefined value.

## The Solution
The solution expands the null check to also include `undefined` to ensure comprehensive handling of these scenarios.
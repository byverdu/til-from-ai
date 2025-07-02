# Code Snippets

## Typescript Function Overloads

**Date:** July 2, 2025

They allow you to define multiple signatures for a single function, enabling different parameter types and return types based on how the function is called.

### How Function Overloads Work

Function overloads consist of:

1. **Overload signatures** - Define the different ways the function can be called
2. **Implementation signature** - The actual function implementation that handles all cases

### Basic Example

```typescript
// Overload signatures
function getValue(key: string): string;
function getValue(key: number): number;

// Implementation signature
function getValue(key: string | number): string | number {
  if (typeof key === 'string') {
    return `Value for ${key}`;
  } else {
    return key * 2;
  }
}

// Usage - TypeScript knows the exact return type
const stringResult = getValue("name"); // Type: string
const numberResult = getValue(42);     // Type: number
```

### Benefits

1. **Type Safety** - Exact return types based on input
2. **No Type Casting** - You don't need to cast results
3. **Better IntelliSense** - IDE provides accurate suggestions
4. **Documentation** - Multiple signatures serve as documentation

> I've found it useful because it prevents you to have to cast the result when you use the method.

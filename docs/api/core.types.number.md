<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@theatre/core](./core.md) &gt; [types](./core.types.md) &gt; [number](./core.types.number.md)

## types.number variable

A number prop type.

<b>Signature:</b>

```typescript
number: (defaultValue: number, opts?: ({
    nudgeFn?: NumberNudgeFn | undefined;
    range?: PropTypeConfig_Number['range'];
    nudgeMultiplier?: number | undefined;
} & PropTypeConfigOpts) | undefined) => PropTypeConfig_Number
```

## Example

Usage

```ts
// shorthand:
const obj = sheet.object('key', {x: 0})

// With options (equal to above)
const obj = sheet.object('key', {
  x: t.number(0)
})

// With a range (note that opts.range is just a visual guide, not a validation rule)
const x = t.number(0, {range: [0, 10]}) // limited to 0 and 10

// With custom nudging
const x = t.number(0, {nudgeMultiplier: 0.1}) // nudging will happen in 0.1 increments

// With custom nudging function
const x = t.number({
  nudgeFn: (
    // the mouse movement (in pixels)
    deltaX: number,
    // the movement as a fraction of the width of the number editor's input
    deltaFraction: number,
    // A multiplier that's usually 1, but might be another number if user wants to nudge slower/faster
    magnitude: number,
    // the configuration of the number
    config: {nudgeMultiplier?: number; range?: [number, number]},
  ): number => {
    return deltaX * magnitude
  },
})
```

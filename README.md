## Nomial

Nomial is a TypeScript implementation of Cem Yuksel's extremely fast, robust, and simple root finding algorithm presented in the paper "High-Performance Polynomial Root Finding for Graphics" (2022). It can be used to find real roots of polynomials of degree 10 and higher. It has no dependencies.

## Usage

### Importing

```typescript
// as a ES module
import { Polynomial, polynomialRoots } from 'nomial';

// as a CommonJS module
const { Polynomial, polynomialRoots } = require('nomial');
```

### Usage

```typescript
// The coefficients are stored in order of exponent power so this polynomial corresponds to
// -7412 - 1505x - 20x^2 - 10x^3 + x^5
const f = new Polynomial([-7412, -1505, -20, -10, 0, 1]);

const roots = polynomialRoots(f);
```

There are optional arguments to specify the start and end of the search interval and epsilon used to terminate root finding.

```typescript
const startSearchInterval = -100;
const endSearchInterval = 100;
const epsilon = 1e-6;

const roots = polynomialRoots(f, startSearchInterval, endSearchInterval, epsilon);
```

### Installing

> npm install nomial

or using yarn

> yarn add nomial

### Paper

Cem Yuksel. 2022. High-Performance Polynomial Root Finding for Graphics. Proc. ACM Comput. Graph. Interact. Tech. 5, 3, Article 7 (July 2022), 15 pages.

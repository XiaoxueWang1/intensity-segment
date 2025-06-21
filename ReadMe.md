### Introduction
This is a lightweight JavaScript library that uses a difference group algorithm for efficient intensity segmentation management. 
It provides the ability to add and set intensity values as well as toString feature.

### Runtime Commands For Test Case
```bash
# Install dependencies
npm install

# Run with sample test data
npm start

# Run test suite
npm test
```

### Installation
```bash
npm install intensity-segments
```

### Basic Usage
const IntensitySegments = require('intensity-segments');
```javascript
const segments = new IntensitySegments();

// Add intensity to interval [10, 20)
segments.add(10, 20, 5);

// Set intensity in interval [15, 25)
segments.set(15, 25, 10);

// Get string representation
segments.toString() // [[10,5],[15,10],[20,5],[25,0]]
```

### Current API Complexity
| Method | Time Complexity | Space Complexity |
|-------|-------|-------|
| add() | O(n)  | O(1)   |
| set() | O(n)  | O(n)   |
| toString() | O(n)  | O(n)   |

### Complexity Optimization Strategies
| Method | Array Time Complexity | AVL Time Complexity |
|-------|-------|-------|
| add() | O(n)  | O(log n)   |
| set() | O(n)  | O(k log n)   |
| toString() | O(n)  | O(n)   |


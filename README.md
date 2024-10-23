# Overview
This repo contains two applications:

1. **Rule Engine with AST**: Evaluates user eligibility using dynamic rules.
2. **Real-Time Weather Monitoring System**: Monitors weather, performs rollups, and triggers alerts.

## Application 1: Rule Engine with AST

### Features
- **AST Structure**: Nodes (`type`, `left`, `right`, `value`) representing rules.
- **API**:
  - `create_rule(rule_string)`: Generate AST from rule.
  - `combine_rules(rules)`: Merge multiple rules into one AST.
  - `evaluate_rule(JSON data)`: Evaluate user data against rules.

### Sample Rule
- `((age > 30 AND department = 'Sales') OR (age < 25 AND department = 'Marketing')) AND (salary > 50000 OR experience > 5)`

### Tests
- Verify AST creation, rule combination, and evaluation.

## Application 2: Real-Time Weather Monitoring

### Features
- **API Integration**: Fetch weather data every 5 minutes.
- **Rollups**:
  - Daily avg, max, min temperature.
  - Dominant weather condition.
- **Alerts**: Triggered by user-defined thresholds.

### Tests
- Verify API, temperature conversion, rollups, and alerts.

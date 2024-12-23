# PHP Loose Comparison Pitfall

This repository demonstrates a common, yet subtle, error in PHP related to loose comparisons.  PHP's loose comparison operator (`==`) does not perform strict type checking. This means that values of different types can be considered equal under certain circumstances.  This example highlights the issue with comparing the string '0' to the integer 0.

## The Problem
The core issue is that PHP's loose comparison (`==`) will evaluate '0' and 0 as equal. While this might seem intuitive in some situations, it can lead to unexpected behavior in many cases, particularly when dealing with user input or data from external sources where type consistency cannot be guaranteed.

## The Solution
To avoid this pitfall, always use the strict comparison operator (`===`) when you need to ensure both the value and the type are identical. The strict comparison operator will correctly identify that '0' and 0 are of different types and therefore not equal.
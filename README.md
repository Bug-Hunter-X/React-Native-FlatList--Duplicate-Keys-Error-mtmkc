# React Native FlatList: Duplicate Keys Bug

This repository demonstrates a common error in React Native's `FlatList` component: using duplicate keys when rendering items.  Duplicate keys lead to incorrect rendering, unexpected behavior, or crashes.

## Bug Description
The bug occurs when the `keyExtractor` function in `FlatList` returns duplicate keys for different items in the data array.  This prevents React Native from efficiently updating the list, resulting in problems.

## How to Reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run the app on an iOS or Android emulator/device.
4. Observe the incorrect rendering of items in the FlatList.

## Solution
The solution is to ensure that the `keyExtractor` function returns a unique key for each item.  This key should ideally be a stable identifier for the item, such as a database ID or UUID.

## Key takeaway
Always use a unique key for each item in a FlatList. This is crucial for performance and to avoid unexpected errors.
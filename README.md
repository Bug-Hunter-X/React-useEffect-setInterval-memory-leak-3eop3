# React useEffect setInterval Memory Leak
This repository demonstrates a common error in React applications involving the `useEffect` hook and `setInterval`.  The issue arises when `setInterval` is used without proper cleanup, leading to memory leaks and unexpected behavior.

## Bug Description
The provided code uses `setInterval` within a `useEffect` hook without providing a cleanup function. This means that multiple intervals are created every time the component renders, resulting in a memory leak and potentially incorrect counter updates.

## Solution
The solution involves returning a cleanup function from the `useEffect` hook, which will clear the interval when the component unmounts or when the dependency array changes.
# Objective-C KVO: Observer Not Removed in dealloc

This repository demonstrates a common bug in Objective-C related to Key-Value Observing (KVO).  The bug occurs when an observer is added to an object but not properly removed in the observer's `dealloc` method.  This can lead to crashes or undefined behavior when the observed object is deallocated.

The `BuggyKVO.m` file shows the problematic code.  The `FixedKVO.m` file provides a corrected version that demonstrates the proper way to remove the observer in the `dealloc` method.

This issue is a subtle one and highlights the importance of meticulous memory management in Objective-C.
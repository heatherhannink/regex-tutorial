# Regex Tutorial: Understanding Look-Ahead and Look-Behind Assertions

## Introduction

Welcome to this tutorial on understanding look-ahead and look-behind assertions in regular expressions! In this tutorial, we'll explore these advanced regex concepts and learn how to use them effectively in pattern matching.

Summary
The regex pattern we'll be focusing on in this tutorial is:

This pattern matches the string "foo" only if it is followed by "bar".

## Table of Contents

1. [Look-Ahead Assertion](#look-ahead-assertion)
2. [Look-Behind Assertion](#look-behind-assertion)
3. [Negative Look-Ahead Assertion](#negative-look-ahead-assertion)
4. [Negative Look-Behind Assertion](#negative-look-behind-assertion)
5. [Practical Example](#practical-example)
6. [Author Information](#author-information)

## Look-Ahead Assertion

A look-ahead assertion allows you to check if a certain pattern exists ahead of the current position in the string, without consuming characters. It's denoted by `(?=pattern)`.

### Code Snippet

```regex
(?=bar)

Explanation
This look-ahead assertion ensures that the pattern "bar" exists immediately after the current position, but "bar" itself is not part of the match.

Example
Consider the regex foo(?=bar). It matches "foo" only if it is followed by "bar". For example, it matches "foobar" but not "foobaz".

Look-Behind Assertion
A look-behind assertion allows you to check if a certain pattern exists behind the current position in the string. It's denoted by (?<=pattern).

Explanation
This look-behind assertion ensures that the pattern "foo" exists immediately before the current position, but "foo" itself is not part of the match.

Example
Consider the regex (?<=foo)bar. It matches "bar" only if it is preceded by "foo". For example, it matches "foobar" but not "bazbar".

Negative Look-Ahead Assertion
Negative look-ahead assertions are denoted by (?!pattern). They assert that a pattern does not exist ahead of the current position.

Code Snippet
(?!bar)

Explanation
This negative look-ahead assertion ensures that the pattern "bar" does not exist immediately after the current position.

Example
Consider the regex foo(?!bar). It matches "foo" only if it is not followed by "bar". For example, it matches "foobaz" but not "foobar".

Negative Look-Behind Assertion
Negative look-behind assertions are denoted by (?<!pattern). They assert that a pattern does not exist behind the current position.

Explanation
This negative look-behind assertion ensures that the pattern "foo" does not exist immediately before the current position.

Example
Consider the regex (?<!foo)bar. It matches "bar" only if it is not preceded by "foo". For example, it matches "bazbar" but not "foobar".

Practical Example
Let's say you want to find all occurrences of the word "apple" that are not preceded by the word "green". You can use a negative look-behind assertion like this: (?<!green )apple.

Author Information
This tutorial was written by Heather Hannink. You can find more tutorials and projects on my GitHub profile.

# CustomDemoDeprecated

As of Xcode 6, Apple has created a first-party solution to writing asynchronous tests. See Testing with Xcode

Overview

Allows testing of asynchronous APIs using XCTest much like gh-unit.

Pleasee see issues for any problems.

Interested users should also check out XCTAsyncTestCase, another awesome async library for XCTest.

Install

Add XCTestCase+AsyncTesting.h and XCTestCase+AsyncTesting.m to your project.

...or via cocoapods pod 'XCAsyncTestCase'

Usage

Add #import "XCTestCase+AsyncTesting.h" to tests that need to be asynchronous.
Optional: add #define XCA_SHORTHAND to your .pch file and enjoy methods without the XCA_ prefix. (new as of v1.0.0)
Create your test cases as usual
Call -XCA_waitForStatus:timeout: or -XCA_waitForTimeout: after you start your asynchronous call
Call -XCA_notify: in your callbacks
See AsyncXCTestingKitTests.m for more information.

Contributors

A big thanks to these folks for their contributions to the project:

CarlJ
Duemonk
FelixLam
Rafiki270
LICENSE

This code is licensed under the MIT license: http://www.opensource.org/licenses/mit-license.php

Copyright (c) 2011 Masashi Ono.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

KEYWORDS

XCTest, XCTestCase, Asynchronous, XCode 5, Developer Preview, iOS 7, GHUnit, SenTest, Objective C
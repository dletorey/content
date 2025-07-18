---
title: declarativeNetRequest.isRegexSupported
slug: Mozilla/Add-ons/WebExtensions/API/declarativeNetRequest/isRegexSupported
page-type: webextension-api-function
browser-compat: webextensions.api.declarativeNetRequest.isRegexSupported
sidebar: addonsidebar
---

Checks if a regular expression is supported as a [`declarativeNetRequest.RuleCondition.regexFilter`](/en-US/docs/Mozilla/Add-ons/WebExtensions/API/declarativeNetRequest/RuleCondition#regexfilter) rule condition.

## Syntax

```js-nolint
let count = await browser.declarativeNetRequest.isRegexSupported(
    regexOptions                // object
);
```

### Parameters

- `regexOptions`
  - : An object containing the regular expression to check.
    - `isCaseSensitive` {{optional_inline}}
      - : `boolean` Whether the regex specified is case sensitive. Default is `true`.
    - `regex`
      - : `string` The regular expression to check.
    - `requireCapturing` {{optional_inline}}
      - : `boolean` Whether the regex specified requires capturing. Capturing is only required for redirect rules that specify a regexSubstitution action. The default is false.

### Return value

A [`Promise`](/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) that fulfills with an object with these properties:

- `isSupported`
  - : `boolean` Whether the regular expression is supported.
- `reason` {{optional_inline}}
  - : `string` Specifies the reason why the regular expression is not supported. Possible values are `"syntaxError"` and `"memoryLimitExceeded"`. Only provided if `isSupported` is false.

If the request fails, the promise is rejected with an error message.

## Examples

{{WebExtExamples}}

## Browser compatibility

{{Compat}}

<!--
// Copyright 2015 The Chromium Authors. All rights reserved.
//
// Redistribution and use in source and binary forms, with or without
// modification, are permitted provided that the following conditions are
// met:
//
//    * Redistributions of source code must retain the above copyright
// notice, this list of conditions and the following disclaimer.
//    * Redistributions in binary form must reproduce the above
// copyright notice, this list of conditions and the following disclaimer
// in the documentation and/or other materials provided with the
// distribution.
//    * Neither the name of Google Inc. nor the names of its
// contributors may be used to endorse or promote products derived from
// this software without specific prior written permission.
//
// THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
// "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
// LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
// A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
// OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
// SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
// LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
// DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
// THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
// (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
// OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
-->

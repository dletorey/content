---
title: "Permissions-Policy: gyroscope directive"
short-title: gyroscope
slug: Web/HTTP/Reference/Headers/Permissions-Policy/gyroscope
page-type: http-permissions-policy-directive
status:
  - experimental
browser-compat: http.headers.Permissions-Policy.gyroscope
sidebar: http
---

{{SeeCompatTable}}

The HTTP {{HTTPHeader("Permissions-Policy")}} header `gyroscope` directive controls whether the current document is allowed to gather information about the orientation of the device through the {{domxref("Gyroscope")}} interface.

Specifically, where a defined policy blocks use of this feature, {{domxref("Gyroscope.Gyroscope", "Gyroscope()")}} constructor calls will throw a {{domxref("DOMException")}} of type `SecurityError`.

## Syntax

```http
Permissions-Policy: gyroscope=<allowlist>;
```

- `<allowlist>`
  - : A list of origins for which permission is granted to use the feature. See [`Permissions-Policy` > Syntax](/en-US/docs/Web/HTTP/Reference/Headers/Permissions-Policy#syntax) for more details.

## Default policy

The default allowlist for `gyroscope` is `self`.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{HTTPHeader("Permissions-Policy")}} header
- [Permissions Policy](/en-US/docs/Web/HTTP/Guides/Permissions_Policy)

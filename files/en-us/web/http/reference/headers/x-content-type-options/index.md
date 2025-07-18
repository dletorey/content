---
title: X-Content-Type-Options header
short-title: X-Content-Type-Options
slug: Web/HTTP/Reference/Headers/X-Content-Type-Options
page-type: http-header
browser-compat: http.headers.X-Content-Type-Options
sidebar: http
---

The HTTP **`X-Content-Type-Options`** {{Glossary("response header")}} indicates that the [MIME types](/en-US/docs/Web/HTTP/Guides/MIME_types) advertised in the {{HTTPHeader("Content-Type")}} headers should be respected and not changed.
The header allows you to avoid [MIME type sniffing](/en-US/docs/Web/HTTP/Guides/MIME_types#mime_sniffing) by specifying that the MIME types are deliberately configured.

Site security testers usually expect this header to be set.

> [!NOTE]
> The `X-Content-Type-Options` header only apply request-blocking [due to `nosniff`](https://fetch.spec.whatwg.org/#ref-for-determine-nosniff) for [request destinations](/en-US/docs/Web/API/Request/destination) of `"script"` and `"style"`.

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">Header type</th>
      <td>{{Glossary("Response header")}}</td>
    </tr>
    <tr>
      <th scope="row">{{Glossary("Forbidden request header")}}</th>
      <td>No</td>
    </tr>
  </tbody>
</table>

## Syntax

```http
X-Content-Type-Options: nosniff
```

## Directives

- `nosniff`
  - : Blocks a request if the request destination is of type
    `style` and the MIME type is not `text/css`,
    or of type `script` and the MIME type is not a [JavaScript MIME type](https://html.spec.whatwg.org/multipage/scripting.html#javascript-mime-type).

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{HTTPHeader("Content-Type")}}
- The [original definition](https://learn.microsoft.com/en-us/archive/blogs/ie/ie8-security-part-vi-beta-2-update) of X-Content-Type-Options by Microsoft.
- Use [HTTP Observatory](/en-US/observatory) to test the security configuration of websites (including this header).
- [Mitigating MIME Confusion Attacks in Firefox](https://blog.mozilla.org/security/2016/08/26/mitigating-mime-confusion-attacks-in-firefox/)

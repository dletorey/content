---
title: "GPUComputePassEncoder: label property"
short-title: label
slug: Web/API/GPUComputePassEncoder/label
page-type: web-api-instance-property
browser-compat: api.GPUComputePassEncoder.label
---

{{APIRef("WebGPU API")}}{{SecureContext_Header}}{{AvailableInWorkers}}

The **`label`** read-only property of the
{{domxref("GPUComputePassEncoder")}} interface is a string providing a label that can be used to identify the object, for example in {{domxref("GPUError")}} messages or console warnings.

This can be set by providing a `label` property in the descriptor object passed into the originating {{domxref("GPUCommandEncoder.beginComputePass()")}} call, or you can get and set it directly on the `GPUComputePassEncoder` object.

## Value

A string. If no label value has previously been set, getting the label returns an empty string.

## Examples

Setting and getting a label via `GPUComputePassEncoder.label`:

```js
const commandEncoder = device.createCommandEncoder();
const passEncoder = commandEncoder.beginComputePass();

passEncoder.label = "my_compute_pass_encoder";
console.log(passEncoder.label); // "my_compute_pass_encoder"
```

Setting a label via the originating {{domxref("GPUCommandEncoder.beginComputePass()")}} call, and then getting it via `GPUComputePassEncoder.label`:

```js
const commandEncoder = device.createCommandEncoder();
const passEncoder = commandEncoder.beginComputePass({
  label: "my_compute_pass_encoder",
});

console.log(passEncoder.label); // "my_compute_pass_encoder"
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- The [WebGPU API](/en-US/docs/Web/API/WebGPU_API)

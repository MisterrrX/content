---
title: z
slug: Web/SVG/Reference/Attribute/z
page-type: svg-attribute
spec-urls:
  - https://drafts.fxtf.org/filter-effects/#element-attrdef-fepointlight-z
  - https://drafts.fxtf.org/filter-effects/#element-attrdef-fespotlight-z
sidebar: svgref
---

The **`z`** attribute defines the location along the z-axis for a light source in the coordinate system established by the {{SVGAttr("primitiveUnits")}} attribute on the {{SVGElement("filter")}} element, assuming that, in the initial coordinate system, the positive z-axis comes out towards the person viewing the content and assuming that one unit along the z-axis equals one unit in x and y.

## Elements

You can use this attribute with the SVG elements described in the sections below.

### `<fePointLight>`

For {{SVGElement("fePointLight")}}, `z` defines the location along the z-axis for the light source in the coordinate system established by the {{SVGAttr("primitiveUnits")}} attribute on the {{SVGElement("filter")}} element.

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">Value</th>
      <td>{{cssxref("number")}}</td>
    </tr>
    <tr>
      <th scope="row">Default value</th>
      <td><code>1</code></td>
    </tr>
    <tr>
      <th scope="row">Animatable</th>
      <td>Yes</td>
    </tr>
  </tbody>
</table>

### `<feSpotLight>`

For {{SVGElement("feSpotLight")}}, `z` defines the location along the z-axis for the light source in the coordinate system established by the {{SVGAttr("primitiveUnits")}} attribute on the {{SVGElement("filter")}} element.

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">Value</th>
      <td>{{cssxref("number")}}</td>
    </tr>
    <tr>
      <th scope="row">Default value</th>
      <td><code>1</code></td>
    </tr>
    <tr>
      <th scope="row">Animatable</th>
      <td>Yes</td>
    </tr>
  </tbody>
</table>

## Examples

```css hidden
html,
body,
svg {
  height: 100%;
}
```

```html
<svg viewBox="0 0 420 200" xmlns="http://www.w3.org/2000/svg">
  <filter id="diffuseLighting1" x="0" y="0" width="100%" height="100%">
    <feDiffuseLighting in="SourceGraphic">
      <fePointLight x="60" y="60" z="10" />
    </feDiffuseLighting>
  </filter>
  <filter id="diffuseLighting2" x="0" y="0" width="100%" height="100%">
    <feDiffuseLighting in="SourceGraphic">
      <fePointLight x="340" y="60" z="50" />
    </feDiffuseLighting>
  </filter>

  <rect x="0" y="0" width="200" height="200" filter="url(#diffuseLighting1)" />
  <rect
    x="200"
    y="0"
    width="200"
    height="200"
    filter="url(#diffuseLighting2)" />
</svg>
```

{{EmbedLiveSample("Examples", "420", "200")}}

## Specifications

{{Specifications}}

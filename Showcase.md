# Blubook Modest

> **Blubook Modest** adapts the original *Blubook* theme to become even more <u>minimal</u> and <u>modest</u>. Major changes are less striking headings and numbering.

## Features

### Stylish Document Title

`H1` is the single title of the document and thus stands out centered at the top of the document. It has a slight color gradient giving it a "final touch".

### Numbered Headings

The following two headings are prefixed by unobtrusive numbers for `H2` or uppercase letters for `H3`. The former one is supported by horizontal dividers to support splitting up the document into sections.

### Enumerations & Lists

*Blubook Modest* supports all common forms of enumerations.

1. Like numbered lists.

* Or bullet lists.

### Code

Like with the original theme you get code fences in a nice blue context. Nothing was changed here so far.

```javascript
class Utils {
  animate(element: Element, attr: string, change: { from: number, to: number, duration?: number }, onEnd?: () => void) {
    if (change.from = = change.to) return;

    if (!change.duration)
      element[attr] = change.to;

    const easing = (t, b, c, d) => c * ((t = t / d - 1) * t * t + 1) + b,
      { from, to } = change,
      during = Math.ceil((change.duration || 300) / 17) || 1;

    let start = 0,
      instance = null;

    step();

    function step() {
      const value = Math.ceil(easing(start, from, to - from, during));

      start++;
      if (start <= during) {
        element[attr] = value;
        instance = requestAnimationFrame(step);
      }
      else {
        if (onEnd) onEnd();
        cancelAnimationFrame(instance);
      }
    }
  }
}
```


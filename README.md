# Masking Plugin

A lightweight and customizable JavaScript masking plugin for formatting user input in real-time. The plugin helps enforce consistent data entry for phone numbers, dates, national IDs, credit card numbers, and custom patterns.

## Features

* Lightweight and dependency-free
* Real-time input formatting
* Custom mask patterns
* Supports numeric and alphanumeric masks
* Automatic cursor positioning
* Easy integration with existing forms
* Configurable placeholder characters
* Validation-friendly output

## Installation

### NPM

```bash
npm install masking-plugin
```

### Manual Installation

```html
<script src="dist/masking-plugin.min.js"></script>
```

## Quick Start

```javascript
const input = document.getElementById('phone');

new MaskingPlugin(input, {
    mask: '(999) 999-9999'
});
```

## Usage Examples

### Phone Number

```javascript
new MaskingPlugin('#phone', {
    mask: '(999) 999-9999'
});
```

### Date

```javascript
new MaskingPlugin('#date', {
    mask: '99/99/9999'
});
```

### Credit Card

```javascript
new MaskingPlugin('#card', {
    mask: '9999 9999 9999 9999'
});
```

### Custom Pattern

```javascript
new MaskingPlugin('#code', {
    mask: 'AAA-999'
});
```

## Mask Tokens

| Token | Description            |
| ----- | ---------------------- |
| 9     | Numeric digit (0-9)    |
| A     | Alphabetic character   |
| *     | Alphanumeric character |

## Configuration

| Option         | Type    | Description                     |
| -------------- | ------- | ------------------------------- |
| mask           | string  | Input mask pattern              |
| placeholder    | string  | Placeholder character           |
| autoClear      | boolean | Clear invalid values            |
| validateOnBlur | boolean | Validate when input loses focus |

## API

### Apply Mask

```javascript
mask.apply();
```

### Remove Mask

```javascript
mask.destroy();
```

### Get Raw Value

```javascript
mask.getRawValue();
```

### Set Value

```javascript
mask.setValue('1234567890');
```

## Browser Support

* Chrome
* Firefox
* Edge
* Safari

## Development

Install dependencies:

```bash
npm install
```

Run development build:

```bash
npm run dev
```

Create production build:

```bash
npm run build
```

## Contributing

Contributions are welcome. Please open an issue or submit a pull request.


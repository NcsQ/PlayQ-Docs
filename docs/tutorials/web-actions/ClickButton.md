---
sidebar_position: 1
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Overview

The `clickButton` function clicks a button element on the page using Playwright. It supports both Playwright and Cucumber test runners with comprehensive error handling and screenshot capabilities.

## Syntax

```javascript
clickButton(page: Page, field: string | Locator, options?: string | Record<string, any>)
```

## Parameters
### Required Parameters
- page: Playwright Page instance
- field: Button identifier (string or Locator)
    Can be button text, label, id, name, or selector
    Examples: "Submit", "Save", "#submit-btn"

## Optional Parameters

```
options: {
    actionTimeout?: number;      // Default: from config or 10000ms
    pattern?: string;            // Custom pattern for element search
    isDoubleClick?: boolean;     // Default: false
    screenshot?: boolean;        // Default: false
    screenshotText?: string;     // Screenshot description
    screenshotFullPage?: boolean; // Default: true
    screenshotBefore?: boolean;  // Take screenshot before click
}
```

## Usage Examples

### Basic Usage

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
```javascript
    // Simple button click
    await webActions.clickButton(page, "Goto Home");
```
  </TabItem>
    <TabItem value="Cucumber" label="Cucumber" default>
```javascript
```
  </TabItem>
</Tabs>

### Custom Timeout

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
```javascript
    // Button click with custom timeout
    await webActions.clickButton(page, "Goto Home", {
        timeout: 20000
    });
```
  </TabItem>
    <TabItem value="Cucumber" label="Cucumber" default>
```javascript
```
  </TabItem>
</Tabs>

### Using Pattern

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
```javascript
    // Button click with pattern
    await webActions.clickButton(page, "Home", {
        pattern: "letcodesamples"
    });
```
</TabItem>
    <TabItem value="Cucumber" label="Cucumber" default>
```javascript
```
  </TabItem>
</Tabs>

### Double Click
<Tabs>
  <TabItem value="playwright" label="Playwright" default>
```javascript
    // Double click
    await webActions.clickButton(page, "Goto Home", {
        doubleClick: true
    });
```
    </TabItem>
<TabItem value="Cucumber" label="Cucumber" default>
```javascript
```
  </TabItem>
</Tabs>

### Screenshot Options
<Tabs>
  <TabItem value="playwright" label="Playwright" default>
```javascript
    // Take screenshot after click action
    await webActions.clickButton(page, "Goto Home", {
        screenshot: true,
        screenshotText: "After clicking Goto Home button"
    });

     // Take screenshot before click action
    await webActions.clickButton(page, "Goto Home", {
        screenshot: true,
        screenshotBefore: true,
        screenshotText: "Before clicking Goto Home button"
    });
```
    </TabItem>
<TabItem value="Cucumber" label="Cucumber" default>
```javascript
```
  </TabItem>
</Tabs>

## Error Handling
- Throws error if page is not initialized
- Waits for page load state after click
- Supports custom timeouts for element location
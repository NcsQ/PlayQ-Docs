---
sidebar_position: 4
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Overview

The `clickRadioButton` function selects a radio button element on the page with support for screenshots, patterns, and error handling.

## Syntax

```javascript
clickRadioButton(page: Page, field: string | Locator, options?: string | Record<string, any>)
```

## Parameters

### Required Parameters
|**Parameter** |**Type**|**Description**|
|--------------|--------|---------------|
| page | Page | Playwright page instance |
| Field | string / Locator | Radio button identifier (text, label, selector, or Locator) |

### Optional Parameters

```javascript
{
    actionTimeout?: number;      // Default: from config or 30000ms
    pattern?: string;           // Custom pattern for element search
    force?: boolean;           // Force click, ignore actionability checks (Default: true)
    screenshot?: boolean;       // Take screenshot after click (Default: false)
    screenshotText?: string;   // Screenshot description
    screenshotFullPage?: boolean; // Full page screenshot (Default: true)
    screenshotBefore?: boolean;  // Take screenshot before click
}
```

## Usage Examples

### Basic Usage

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
    ```javascript
    test('radio click test', async ({ page }) => {
        await web.openBrowser(page, "https://letcode.in/radio");
        // Simple radio button click with pattern - select 'Yes' in 'Select any one' field
        await web.clickRadioButton(page, "{field::Select any one} Yes");
    });

    ```
  </TabItem>
  <TabItem value="Cucumber" label="Cucmber" default>

  </TabItem>
</Tabs>
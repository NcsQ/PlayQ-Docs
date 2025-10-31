---
sidebar_position: 5
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Overview

The clickCheckbox function checks/unchecks a checkbox element on the page with support for screenshots, patterns, and error handling.

## Syntax

```javascript
clickCheckbox(page: Page, field: string | Locator, options?: string | Record<string, any>)
```

## Parameters

### Required Parameters
|**Parameter** |**Type**|**Description**|
|--------------|--------|---------------|
| page | Page | Playwright page instance |
| Field | string / Locator |Checkbox identifier (text, label, selector, or Locator) |

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

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
    ```javascript
    // Simple checkbox selection test
    test('Checkbox selection test', async ({ page }) => {
        await web.openBrowser(page, "https://letcode.in/radio");
        // Simple checkbox selection - select 'Remember me'
        await web.clickCheckbox(page, "Remember me");
    });

    ```
  </TabItem>
  <TabItem value="Cucumber" label="Cucumber" default>

  </TabItem>
</Tabs>


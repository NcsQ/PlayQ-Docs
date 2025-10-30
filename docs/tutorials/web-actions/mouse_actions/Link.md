---
sidebar_position: 2
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Overview

The `clickLink` function clicks a link element on the page with comprehensive support for screenshots, logging, and error handling across both Playwright and Cucumber test runners.

## Syntax

```javascript
clickLink(page: Page, field: string | Locator, options?: string | Record<string, any>)
```

## Parameters
### Required Parameters
- page: Playwright Page instance
- field: Link identifier (text, selector, or Locator)

## Optional Parameters

```
{
    actionTimeout?: number;      // Default: from config or 10000ms
    pattern?: string;           // Custom link search pattern
    screenshot?: boolean;       // Take screenshot after click
    screenshotText?: string;   // Screenshot description
    screenshotFullPage?: boolean; // Full page screenshot
    screenshotBefore?: boolean; // Take screenshot before click
}
```

## Usage Examples

### Basic Usage

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
```javascript
test('link click test', async ({ page }) => {
    await webActions.openBrowser(page, "http://the-internet.herokuapp.com/");
    // Simple link click
    await webActions.clickLink(page, "Broken Images");
});
```

  </TabItem>
    <TabItem value="Cucumber" label="Cucumber" default>
```javascript
```
  </TabItem>
</Tabs>
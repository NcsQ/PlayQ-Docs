---
sidebar_position: 2
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Overview

The `navigateByPath` function navigates to a relative path from the current URL in the browser. 

## Syntax

```javascript
navigateByPath(page: Page, relativePath: string, options?: string | Record<string, any>)
```

## Parameters
### Required Parameters
- page: Playwright Page instance
- relativePath:  The relative path to navigate to (e.g., "/products", "/account/settings")

## Optional Parameters

```
options: {
    screenshot?: boolean;        // Take screenshot after navigation
    screenshotText?: string;    // Description for screenshot
    screenshotFullPage?: boolean; // Capture full page screenshot
}
```

## Usage Examples

### Basic Navigation

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
```javascript
//NavigateByPath action tests
test('navigation by path test', async ({ page }) => {
    await webActions.openBrowser(page, "https://letcode.in/");
    // Navigate by path
    await webActions.navigateByPath(page, "/button");
});
```
  </TabItem>
    <TabItem value="Cucumber" label="Cucumber" default>
```javascript
```
  </TabItem>
</Tabs>

---
sidebar_position: 1
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Overview

The `openBrowser` function navigates to a specified URL and supports both Playwright and Cucumber test runners with automatic screenshot capabilities and logging..

## Syntax

```javascript
openBrowser(page: Page, url: string, options?: string | Record<string, any>)
```

## Parameters
### Required Parameters
|**Parameter** |**Type**|**Description**|
|--------------|--------|---------------|
|page | Page | Playwright Page instance |
|url  | string | URL to navigate to (e.g., "https://example.com") |
|options | string | object | Optional configuration|

## Optional Parameters

```
{
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

    test('basic navigation', async ({ page }) => {
        await webActions.openBrowser(page, 'https://letcode.in/');
    });
```
  </TabItem>
    <TabItem value="Cucumber" label="Cucumber" default>
```javascript
```
  </TabItem>
</Tabs>

### With Screenshot

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
```javascript
       await webActions.openBrowser(page, 'https://letcode.in/', {
        screenshot: true,
        screenshotText: 'Homepage Navigation',
        screenshotFullPage: true
    });
```
  </TabItem>
    <TabItem value="Cucumber" label="Cucumber" default>
```javascript
```
  </TabItem>
</Tabs>

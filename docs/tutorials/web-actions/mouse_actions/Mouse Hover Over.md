---
sidebar_position: 3
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Overview

The mouseoverOnLink function performs a mouse hover action over a link element on the page with support for screenshots and error handling.


## Syntax

```javascript
mouseoverOnLink(page: Page, field: string | Locator, options?: string | Record<string, any>)
```

### Required Parameters
|**Parameter** |**Type**|**Description**|
|--------------|--------|---------------|
| page | Page | Playwright page instance |
| Field | string / Locator | Link identifier (text, selector, or Locator) |

### Optional Parameters

```javascript
{

    actionTimeout?: number;      // Default: from config or 30000ms
    pattern?: string;           // Custom pattern for element search
    screenshot?: boolean;       // Take screenshot after hover (Default: false)
    screenshotText?: string;   // Screenshot description
    screenshotFullPage?: boolean; // Full page screenshot (Default: true)
}
```

## Usage Examples

### Basic Usage

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
    ```javascript
        test('mouse hover test', async ({ page }) => {
            await web.openBrowser(page, "http://the-internet.herokuapp.com/hovers");
            // Simple mouse hover - hover over user1
            await web.mouseoverOnLink(page, locHeroku.heroku_hover_page.link_user1(page) );
            await web.verifyTextOnPage(page, "name: user1")
        });

    ```
  </TabItem>
  <TabItem value="Cucumber" label="Cucmber" default>

  </TabItem>
</Tabs>

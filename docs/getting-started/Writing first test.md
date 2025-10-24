---
sidebar_position: 2
---

## Writing a simple test

Take a look at the following example to see how to write a simple test.

In folowing test 'first test', the actions performed are:
    1. Open web browser
    2. Navigate to the 'https://ecommerce-playground.lambdatest.io/'
    3. Verify the page title is 'Your Store'

```typescript
import { test } from '@setup/playwrightTest';
import * as webActions from '@src/helper/actions/webActions';

test('first test', async ({ page }) => {
    await webActions.openBrowser(page, "https://ecommerce-playground.lambdatest.io/");
    await webActions.verifyPageTitle(page,"Your Store")
});
```

## Execute the test

Once we have written the test, we can execute it with the following command:

```
npx cross-env PLAYQ_GREP='first test' npm run test
```


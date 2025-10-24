---
sidebar_position: 4
---

## Overview

PlayQ supports both Playwright and Cucumber test runners. This guide explains available options and provides examples for both styles.


 #### Environment Variables
|Variable	|Description	|Example|
|------------|-----------|---------|
|PLAYQ_RUNNER	|Test runner type (playwright/cucumber)	|playwright|
|PLAYQ_ENV	|Target environment	|staging|
|PLAYQ_GREP	|Filter tests by pattern	|@smoke|
|PLAYQ_TAGS	|Filter cucumber scenarios	|@regression|

## Playwright Style Tests

#### Basic Test Structure

```typescript
import { ur } from '@faker-js/faker/.';
import { test } from '@setup/playwrightTest';
import * as webActions from '@src/helper/actions/webActions';


test('exact title match test @smoke_test', async ({ page }) => {
    await webActions.openBrowser(page, "https://ecommerce-playground.lambdatest.io/");
    await webActions.verifyPageTitle(page,"Your Store")
});

test.describe('@smoke_test', () => {
    test('partial title match test', async ({ page }) => {
        await webActions.openBrowser(page, "https://ecommerce-playground.lambdatest.io/");
        await webActions.verifyPageTitle(page,"Your",{
            partialMatch: true,
        })
    });
});
```

#### Running the tests

```
npx cross-env PLAYQ_GREP='@smoke_sample' npm run test
```
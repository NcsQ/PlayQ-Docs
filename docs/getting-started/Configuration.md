---
sidebar_position: 4
---

## Overview

This document details the configuration options available in the PlayQ automation framework. 

The configuration file manages test execution settings, browser behavior, reporting, and various framework features.

```
playq/resources/config.ts
```


### Base URL Configuration

```
baseUrl: "https://your-app.com"  // Base URL for tests
```

### Cucumber Settings

```
cucumber: {
    featureFileCache: false,  // Cache feature files for faster execution
    stepGroupCache: true      // Cache step definitions
}
```

### Browser Configuration

```
browser: {
    playwrightSession: "shared",    // Options: "shared" | "isolated" | "perTest" | "perFile" | "none"
    cucumberSession: "perScenario", // Options: "shared" | "perScenario" | "perFeature"
    headless: true,                 // Run tests in headless mode
    browserType: "chromium"         // Options: "chromium" | "firefox" | "webkit"
}
```

### Artifacts Configuration

```
artifacts: {
    screenshot: true,        // Enable screenshot capture
    video: true,             // Enable video recording
    trace: true,             // Enable trace capture
    onFailureOnly: true,     // Capture artifacts only on test failure
    onSuccessOnly: false,    // Capture artifacts on test success
    cleanUpBeforeRun: true   // Clean artifacts before test run
}
```

### Test Execution Settings

```
testExecution: {
    timeout: 60000,          // Global test timeout (ms)
    actionTimeout: 30000,    // Action timeout (ms)
    navigationTimeout: 60000, // Navigation timeout (ms)
    retryOnFailure: true,    // Retry failed tests
    parallel: true,          // Run tests in parallel
    maxInstances: 5,         // Maximum parallel instances
    maxRetries: 2,           // Maximum retry attempts
    retryDelay: 1000,        // Delay between retries (ms)
    retryInterval: 2000,     // Interval between retries (ms)
    retryTimeout: 30000,     // Timeout for retries (ms)
    order: "sequential",     // Test execution order
    autoReportOpen: true     // Open report automatically
}
```

### API Test Configuration

```
apiTest: {
    maxUrlRedirects: 5,  // Maximum URL redirects
    timeout: 10000       // API request timeout (ms)
}
```
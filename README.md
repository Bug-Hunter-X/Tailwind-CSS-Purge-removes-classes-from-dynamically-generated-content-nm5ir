# Tailwind CSS Purge Removes Classes from Dynamic Content

This repository demonstrates a common issue in Tailwind CSS where the purge process removes classes used in dynamically generated content.  The bug occurs because the classes aren't present in the initial HTML passed to PurgeCSS.  The solution explores various ways to address this problem, including configuration changes and alternative approaches.

## Bug
The `dynamicContentBug.js` file shows how dynamically adding a class leads to missing styles because PurgeCSS has already removed the unused class from the final CSS bundle.

## Solution
The `dynamicContentSolution.js` file provides several solutions:

* **Custom PurgeCSS Configuration:**  Adds the missing class to the whitelist or modifies the configuration to avoid removing it.
* **Adjusting build process:** Adjusting the build process to ensure dynamic classes are correctly identified

This example highlights the importance of understanding how Tailwind's purge mechanism works and the need for careful configuration when dealing with dynamic content generation.
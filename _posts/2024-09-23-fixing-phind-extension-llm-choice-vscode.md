---
layout: post
title: "Quick Fix: Keeping Your LLM Choice in VSCode's Phind Extension"
date: 2024-09-23 12:00:00 -0000
categories: VSCode Extension Phind LLM
---

# Quick Fix: Keeping Your LLM Choice in VSCode's Phind Extension

If you're a VSCode user who frequently works with the Phind extension (version 0.25.4), you might have encountered an annoying issue: the extension keeps forgetting your chosen Language Model (LLM). This can be frustrating, especially if you have a preferred model that you use regularly. Luckily, there's a simple fix for this problem.

## The Problem

By default, the Phind extension resets to its default LLM engine ("Phind-45B") every time you restart VSCode or the extension. This means you have to manually select your preferred model each time, which can be a time-consuming and irritating process.

## The Solution

To solve this issue, we need to modify a file in the extension's directory. Here's how:

1. Locate the following file on your system:
   ```
   /home/$USER/.vscode/extensions/phind.phind-0.25.4/compiled-react/webview.bundle.js
   ```
   Replace `$USER` with your actual username.

2. Open this file in a text editor.

3. Find the line that sets the default LLM engine to "Phind-45B".

4. Change "Phind-45B" to your preferred LLM. For example, "Claude 3.5 Sonnet".

5. Save the file and restart VSCode.

After making this change, the Phind extension should remember your LLM choice and use it as the default option.

## Caution

Keep in mind that this modification directly changes the extension's code. It's a good idea to make a backup of the original file before making any changes. Also, be aware that this change might be overwritten when the extension updates, so you may need to reapply it after updates.

## Conclusion

This simple fix can save you time and frustration by ensuring that your preferred LLM is always selected in the Phind extension. Happy coding!

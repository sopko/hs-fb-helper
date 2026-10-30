# HubSpot CLI transfer bundle

Includes @hubspot/cli 8.18.0, package manifests, and the complete installed node_modules directory. Node.js itself is not included; the CLI requires Node.js >=20. Verified with Node.js 22.23.2 on macOS x64.

After cloning the repository or extracting the ZIP, open a terminal in hubspot-cli-transfer and run:

    node node_modules/@hubspot/cli/bin/hs.js --version
    node node_modules/@hubspot/cli/bin/hs.js --help

Use that same command followed by your desired CLI arguments. Calling the JavaScript entry point directly also avoids reliance on Unix executable symlinks on Windows. Authenticate on the destination machine as needed.

Dependencies were installed on macOS x64. The matching macOS arm64 packages for Rollup (4.66.0) and esbuild (0.25.12) are also included for Apple Silicon Macs. Other platforms may require reinstalling platform-specific dependencies. Only x64 execution has been verified locally.

This repository includes the expanded node_modules tree intentionally so the installed CLI can be transferred without running npm install.

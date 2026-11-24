# marble 6.6 Kernel Build

Standalone Linux 6.6 GKI kernel build script and GitHub Actions workflow for Xiaomi Redmi Note 12 Turbo / POCO F5 (`marble`).

The build pipeline clones the `17-6.6` kernel sources, dynamically integrates KernelSU-Next (`dev-susfs`) and SuSFS (`gki-android15-6.6`), applies the reboot and multi-manager patches, compiles the `Image` with Alchemist LLVM Clang, and packages a flashable AnyKernel3 zip.

Configure `TG_BOT_TOKEN` and `TG_BUILD_CHAT_ID` in repository secrets (or a local `.secrets` file) to receive Telegram notifications and build uploads, then trigger the workflow manually from the Actions tab or run `./kernelsu-next-standalone-6.6.sh` directly.

# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.1] - 2025-01-31

### Added
- **Browse mode auto-disable**: Automatically disables browse mode on focus for better WhatsApp experience
- **Control+R**: Read complete message - clicks "read more" button and speaks full text automatically
- **Control+C**: Copy current message to clipboard
  - Searches for complete message text (>800 chars) first
  - Falls back to filtered text if complete message not found
  - All user-facing messages translatable

### Changed
- **Improved error messages**: All scripts now provide clear feedback
  - Alt+1: Reports "Conversation list not found" on failure
  - Alt+2: Reports "Message list not found" on failure
  - Alt+D: Reports "Message composer not found" on failure
  - Enter: Reports "No audio message found" when no slider detected
  - Shift+Enter: Reports "No menu found" when context menu unavailable
  - Control+R: Reports "Not in message list" or "No message found" on errors
  - Control+C: Reports "Cannot copy" when copy operation fails
- **Silent success**: Navigation commands (Alt+1, Alt+2, Alt+D) no longer speak on success (NVDA already announces focus)
- **All strings translatable**: Every user-facing message now uses `_()` function
- **Enter (play voice message)**: Improved logic using slider detection instead of counting buttons
- Cleaner event handling with focus-based browse mode management

### Fixed
- Alt+2 now correctly tries all navigation paths if first attempt fails
- Alt+1 and Alt+2 now correctly report errors when all navigation paths fail
- Optimized object filtering to reduce input lag during navigation

## [1.0.0] - 2025-01-29

### Added
- Initial release of WhatsApp NG add-on
- Alt+1: Navigate to conversation list
- Alt+2: Navigate to message list
- Alt+D: Focus message composer
- Enter: Play voice message (supports individual chats and groups)
- Shift+Enter: Open message context menu
- Toggle scripts for phone number filtering in conversations and messages
- Automatic focus mode activation in WhatsApp Desktop
- Phone number filtering for "Talvez" messages and international formats

### Technical
- Supports NVDA 2021.1 through 2025.3.1
- Based on web-based WhatsApp Desktop architecture
- Uses event_NVDAObject_init for real-time phone filtering
- Translation support for multiple languages
- SCons build system integration

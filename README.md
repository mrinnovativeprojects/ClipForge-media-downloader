# ClipForge

**ClipForge** is a fast, modern desktop media downloader designed to download supported online videos and audio with a simple, reliable interface.

## Features

* Download supported videos with audio
* Extract/download audio
* MP4 and other supported media formats
* Choose the download destination
* Real-time download progress and percentage
* Automatic dependency detection and recovery
* Automatic repair if required application components are missing
* Desktop and Start Menu shortcuts
* Fast startup with a single application launcher
* Safe local application architecture
* Clean, minimal user interface
* Open downloaded files and download folders directly from the app

## Supported Platforms

* YouTube
* Facebook
* Instagram
* TikTok

> Availability and downloading depend on the platform, content permissions, authentication requirements, and applicable terms.

## Requirements

ClipForge should automatically detect required components such as FFmpeg and install or repair missing components when possible.

The application should never silently fail because a required component was deleted. Instead, it should attempt recovery and clearly inform the user if manual action is required.

## Installer / Launcher

ClipForge uses **one primary launcher**.

Installation flow:

# Verify the installation.

# Create shortcuts using the correct ClipForge icon.

# Launch ClipForge automatically.

The launcher should not open a visible PowerShell or Command Prompt window during normal startup.

## Download Flow

1. User pastes a supported media URL.
2. ClipForge analyzes the media.
3. Available video/audio formats are displayed.
4. User selects the desired format and quality.
5. User selects the destination folder.
6. Download begins.
7. Progress, percentage, speed, and remaining information are displayed.
8. Video and audio are combined correctly when separate streams are required.
9. The completed file is verified.
10. The user can open the downloaded file or its containing folder.

## Reliability

ClipForge should:

* Handle missing dependencies gracefully.
* Automatically repair required components where possible.
* Avoid creating duplicate launchers or shortcuts.
* Prevent unnecessary startup delays.
* Verify downloaded media before reporting success.
* Preserve audio when video and audio are delivered as separate streams.
* Provide useful error messages instead of silently failing.

## Security

ClipForge should follow secure software-development practices:

* Download dependencies only from trusted sources.
* Validate downloaded files before installation.
* Avoid executing untrusted downloaded content.
* Store application data safely.
* Use least-privilege permissions whenever possible.
* Never claim that software is completely "virus-proof" or provides absolute security.
## Development

Clone the repository, install the required development dependencies, and run the application using the project's development command.

Before building a release, verify:

* Application launches without a visible terminal window.
* Only one launcher is created.
* Desktop shortcut works.
* Start Menu shortcut works.
* Correct ClipForge icon is displayed.
* Required dependencies are detected.
* Missing dependencies can be recovered.
* Video and audio are correctly combined.
* MP4 output plays correctly.
* Download progress is accurate.
* Open File and Open Folder actions work.
* Application closes cleanly.

## License

See the `LICENSE` file for the complete ClipForge license terms.

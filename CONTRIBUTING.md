# Contributing to 2chiefk-_-Updated

Thank you for your interest in contributing to this Android build tools project! This document provides guidelines and instructions for contributing.

## Code of Conduct

By participating in this project, you are expected to:
- Be respectful and constructive in all interactions
- Welcome newcomers and help them get started
- Focus on what is best for the community
- Show empathy towards other community members

## How to Contribute

### Reporting Bugs

If you find a bug, please create an issue with:
- A clear and descriptive title
- Detailed steps to reproduce the problem
- Expected behavior vs actual behavior
- Your environment (OS, NDK version, Android API level, architecture)
- Relevant logs or error messages

### Suggesting Enhancements

Enhancement suggestions are welcome! Please create an issue that includes:
- A clear description of the enhancement
- The motivation/use case for the change
- Potential implementation approaches
- Any potential drawbacks or concerns

### Pull Requests

1. **Fork the repository** and create your branch from the default branch
2. **Make your changes** following the coding standards below
3. **Test your changes** thoroughly
   - Build the tools for multiple architectures if applicable
   - Verify the built tools work correctly
4. **Update documentation** if you changed functionality
5. **Commit your changes** with clear, descriptive commit messages
6. **Push to your fork** and submit a pull request

#### Pull Request Guidelines

- Keep changes focused and atomic (one feature/fix per PR)
- Include relevant issue numbers in the PR description
- Update README.md if you add new features or tools
- Ensure all build scripts work correctly
- Test on at least one target architecture before submitting

## Development Guidelines

### Project Structure

- `build-tools/` - CMake files for build tools (aapt, aapt2, aidl, etc.)
- `platform-tools/` - CMake files for platform tools (adb, fastboot, etc.)
- `lib/` - CMake files for required libraries
- `patches/` - Patch files for Android source code
- `build.py` - Main build script
- `get_source.py` - Script to fetch Android sources

### Building the Project

Please refer to the [README.md](README.md) for detailed build instructions.

#### Prerequisites

- Python 3.8 or higher
- CMake 3.18 or higher
- Ninja build system
- Android NDK (latest version recommended)
- Git
- Go (for some tools)

### Coding Standards

#### Python Code

- Follow PEP 8 style guidelines
- Use meaningful variable and function names
- Add comments for complex logic
- Keep functions focused and concise

#### CMake Files

- Follow the existing CMake file structure
- Use consistent indentation (4 spaces)
- Comment complex build configurations
- Test with multiple architectures

#### Patch Files

- Keep patches minimal and focused
- Document why each patch is needed
- Test patches apply cleanly to specified versions
- Update patch files when Android source versions change

### Testing

Before submitting a pull request:

1. Test the build process completes successfully
2. Verify built tools execute correctly
3. Test on multiple architectures if possible (arm64-v8a, armeabi-v7a, x86_64, x86)
4. Check for any warnings or errors in the build output

## Adding New Tools

To add a new Android tool:

1. Create a new CMake file in `build-tools/` or `platform-tools/`
2. Follow the pattern of existing tool CMake files
3. Add the tool to the appropriate CMakeLists.txt
4. Update the finish() function in build.py to include the new tool
5. Test building the new tool
6. Update README.md with information about the new tool

## Need Help?

- Check existing issues and pull requests
- Review the README.md for build instructions
- Look at existing CMake files for examples
- Create an issue if you're stuck or need clarification

## License

By contributing, you agree that your contributions will be licensed under the Apache License 2.0, the same license as this project.

Thank you for contributing!

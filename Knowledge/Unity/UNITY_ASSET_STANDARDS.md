# Alkiren Studio: Unity Asset & Game Standards

## Core Configuration
- **Unity Version**: LTS versions preferred (e.g., 2022.3 LTS).
- **Scripting Backend**: IL2CPP for Production (Android/iOS).
- **Api Compatibility Level**: .NET Standard 2.1 (for maximum compatibility).

## Coding Standards (C#)
- **Namespacing**: Every asset must reside within `AlkirenStudio.[AssetName]`.
- **Assembly Definitions**: Use `.asmdef` files to minimize compile times and manage dependencies.
- **Documentation**: Use XML comments (`///`) for all public APIs.
- **FSM Pattern**: Prefer the "Code First FSM" architecture for complex state logic.

## Project Structure
- `Runtime/`: Main code and logic.
- `Editor/`: Custom inspectors and editor-only tools.
- `Samples~/`: Examples (using the Tilde folder to keep them out of default import).
- `Documentation~/`: Detailed guides.

## Android Specifics
- **Target Architectures**: ARMv7 and ARM64.
- **Graphics API**: Vulkan (with GLES3 fallback).
- **Compression**: ASTC for textures.

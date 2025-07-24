
## Commit


Create well-formatted commits with conventional commit messages and emojis.

## Features:
- Runs pre-commit checks by default (lint, build, generate docs)
- Automatically stages files if none are staged
- Uses conventional commit format with descriptive emojis
- Suggests splitting commits for different concerns

## Usage:
- `/commit` - Standard commit with pre-commit checks
- `/commit --no-verify` - Skip pre-commit checks

## Commit Types:
- ✨ feat: New features
- 🐛 fix: Bug fixes
- 📝 docs: Documentation changes
- ♻️ refactor: Code restructuring without changing functionality
- 🎨 style: Code formatting, missing semicolons, etc.
- ⚡️ perf: Performance improvements
- ✅ test: Adding or correcting tests
- 🧑‍💻 chore: Tooling, configuration, maintenance
- 🚧 wip: Work in progress
- 🔥 remove: Removing code or files
- 🚑 hotfix: Critical fixes
- 🔒 security: Security improvements

## Process:
1. Check for staged changes (`git status`)
2. If no staged changes, review and stage appropriate files
3. Run pre-commit checks (unless --no-verify)
4. Analyze changes to determine commit type
5. Generate descriptive commit message
6. Include scope if applicable: `type(scope): description`
7. Add body for complex changes explaining why
8. Execute commit

## Best Practices:
- Keep commits atomic and focused
- Write in imperative mood ("Add feature" not "Added feature")
- Explain why, not just what
- Reference issues/PRs when relevant
- Split unrelated changes into separate commits
## Check


Perform comprehensive code quality and security checks.

## Primary Task:
Run `npm run check` (or project-specific check command) and resolve any resulting errors.

## Important:
- DO NOT commit any code during this process
- DO NOT change version numbers
- Focus only on fixing issues identified by checks

## Common Checks Include:
1. **Linting**: Code style and syntax errors
2. **Type Checking**: TypeScript/Flow type errors
3. **Unit Tests**: Failing test cases
4. **Security Scan**: Vulnerability detection
5. **Code Formatting**: Style consistency
6. **Build Verification**: Compilation errors

## Process:
1. Run the check command
2. Analyze output for errors and warnings
3. Fix issues in priority order:
   - Build-breaking errors first
   - Test failures
   - Linting errors
   - Warnings
4. Re-run checks after each fix
5. Continue until all checks pass

## For Different Project Types:
- **JavaScript/TypeScript**: `npm run check` or `yarn check`
- **Python**: `black`, `isort`, `flake8`, `mypy`
- **Rust**: `cargo check`, `cargo clippy`
- **Go**: `go vet`, `golint`
- **Swift**: `swift-format`, `swiftlint`
## Bug Fix


Streamline bug fixing workflow from issue creation to pull request.

## Process:

### Before Starting:
1. **GitHub**: Create an issue with a short descriptive title
2. **Git**: Create and checkout a feature branch (`git checkout -b fix/<issue-description>`)

### Fix the Bug:
1. Reproduce the issue
2. Write failing test that demonstrates the bug
3. Implement the fix
4. Verify test passes
5. Run full test suite
6. Review code changes

### On Completion:
1. **Git**: Commit with descriptive message referencing the issue
   - Format: `fix: <description> (#<issue-number>)`
2. **Git**: Push the branch to remote repository
3. **GitHub**: Create PR and link the issue
   - Use "Fixes #<issue-number>" in PR description
   - Add relevant labels and reviewers

## Best Practices:
- Keep changes focused on the specific bug
- Include regression tests
- Update documentation if behavior changes
- Consider edge cases and related issues
## Implement Task


Approach task implementation methodically with careful planning and execution.

## Process:

### 1. Think Through Strategy
- Understand the complete requirement
- Identify key components needed
- Consider dependencies and constraints
- Plan the implementation approach

### 2. Evaluate Approaches
- List possible implementation strategies
- Compare pros and cons of each
- Consider:
  - Performance implications
  - Maintainability
  - Scalability
  - Code reusability
  - Testing complexity

### 3. Consider Tradeoffs
- Short-term vs long-term benefits
- Complexity vs simplicity
- Performance vs readability
- Flexibility vs focused solution
- Time to implement vs perfect solution

### 4. Implementation Steps
1. Break down into subtasks
2. Start with core functionality
3. Implement incrementally
4. Test each component
5. Integrate components
6. Add error handling
7. Optimize if needed
8. Document decisions

### 5. Best Practices
- Write tests first (TDD approach)
- Keep functions small and focused
- Use meaningful names
- Comment complex logic
- Handle edge cases
- Consider future maintenance

## Checklist:
- [ ] Requirements fully understood
- [ ] Approach documented
- [ ] Tests written
- [ ] Code implemented
- [ ] Edge cases handled
- [ ] Documentation updated
- [ ] Code reviewed
- [ ] Performance acceptable
## Code Analysis


Perform advanced code analysis with multiple inspection options.

## Analysis Menu:

### 1. Knowledge Graph Generation
- Map relationships between components
- Visualize dependencies
- Identify architectural patterns

### 2. Code Quality Evaluation
- Complexity metrics
- Maintainability index
- Technical debt assessment
- Code duplication detection

### 3. Performance Analysis
- Identify bottlenecks
- Memory usage patterns
- Algorithm complexity
- Database query optimization

### 4. Security Review
- Vulnerability scanning
- Input validation checks
- Authentication/authorization review
- Sensitive data handling

### 5. Architecture Review
- Design pattern adherence
- SOLID principles compliance
- Coupling and cohesion analysis
- Module boundaries

### 6. Test Coverage Analysis
- Coverage percentages
- Untested code paths
- Test quality assessment
- Missing edge cases

## Process:
1. Select analysis type based on need
2. Run appropriate tools and inspections
3. Generate comprehensive report
4. Provide actionable recommendations
5. Prioritize improvements by impact

## Output Format:
- Executive summary
- Detailed findings
- Risk assessment
- Improvement roadmap
- Code examples where relevant
## Context Prime


Prime Claude with comprehensive project understanding.

## Standard Context Loading:
1. Read README.md for project overview
2. Read CLAUDE.md for AI-specific instructions
3. List project files excluding ignored paths
4. Review key configuration files
5. Understand project structure and conventions

## Steps:
1. **Project Overview**:
   - Read README.md
   - Identify project type and purpose
   - Note key technologies and dependencies

2. **AI Guidelines**:
   - Read CLAUDE.md if present
   - Load project-specific AI instructions
   - Note coding standards and preferences

3. **Repository Structure**:
   - Run: `git ls-files | head -50` for initial structure
   - Identify main directories and their purposes
   - Note naming conventions

4. **Configuration Review**:
   - Package manager files (package.json, Cargo.toml, etc.)
   - Build configuration
   - Environment setup

5. **Development Context**:
   - Identify test framework
   - Note CI/CD configuration
   - Review contribution guidelines

## Advanced Options:
- Load specific subsystem context
- Focus on particular technology stack
- Include recent commit history
- Load custom command definitions

## Output:
Establish clear understanding of:
- Project goals and constraints
- Technical architecture
- Development workflow
- Collaboration parameters
## Create Docs


Create comprehensive documentation for specified components or features.

## Analysis Areas:
1. Code structure and purpose
2. Inputs, outputs, and behavior
3. User interaction flows
4. Edge cases and error handling
5. Integration points with other components/systems

## Documentation Template:

### Overview
Brief 1-2 paragraph overview explaining purpose and value

### Usage
How to use this component/feature with examples

### API / Props / Parameters
Detailed specification of interfaces

### Component Hierarchy
Structure and relationships (if applicable)

### State Management
How state is handled and flows through the system

### Behavior
Expected behavior in different scenarios

### Error Handling
How errors are caught, handled, and reported

### Performance Considerations
Optimization notes and performance characteristics

### Accessibility
Accessibility features and compliance

### Testing
How to test this component/feature

### Related Components/Features
Links to related documentation

## Process:
1. Analyze the target code thoroughly
2. Identify all public interfaces
3. Document expected behaviors
4. Include code examples
5. Add diagrams where helpful
6. Follow project documentation standards
7. Ensure clarity, completeness, and actionability

## Output Formats:
- Markdown for general documentation
- JSDoc/TSDoc for code comments
- API documentation format
- README files
- Architecture decision records (ADRs)
## MCP Best Practices


**I. General Tool Configuration & Behavior**

1.  **Sensible Defaults:** All environment variables must have sensible defaults for easy out-of-the-box usage.
2.  **Dynamic Versioning:** The tool's version is emitted in its description. This version must be read dynamically (e.g., from `package.json`) and not hardcoded.
3.  **Tool & Parameter Descriptions:**
    *   **Tool Titles:** Use descriptive, human-friendly titles for tools.
    *   **Parameter Descriptions:** All parameters must offer a clear description.
    *   **Optional/Required Parameters:** Parameters must be explicitly noted as "optional" or "required."
    *   **Default Values:** If a parameter is optional, its default value must be explained.
    *   (These details should be verifiable by hovering over the tool in clients like Cursor or using the MCP inspector.)
4.  **Parameter Parsing:** Parameter parsing should be lenient (e.g., accept `path` if `project_path` is formally defined). Generally, advertise stricter schemas but be more lenient in execution to accommodate variations from agents.
5.  **Runtime Error Handling:** In case of an error, emit a helpful message to the caller with information to potentially recover.
6.  **Configuration Error Handling:** Misconfigurations (e.g., wrongly set environment variables) must not crash the tool. Instead, provide a useful explanation when the tool is run, enabling the user to self-correct their setup.
7.  **No stdio Output:** **CRITICAL: There must be absolutely NO output to stdout or stderr during any tool operation.** This includes:
    *   No `console.log()`, `console.error()`, `console.warn()`, etc.
    *   No `process.stdout.write()` or `process.stderr.write()`
    *   No print statements or debug output to stdio
    *   Even during errors or initialization, all output must go through the file logger
    *   Any stdio output will disrupt MCP clients (like Claude) and cause loading errors
    *   File-based logging (e.g., Pino to log files) is the only acceptable method for operational output
8.  **`info` Command:**
    *   At least one tool must offer an `info` sub command (find the most appropriate tool and add there)
    *   This command shall list:
        *   The version of the MCP tool.
        *   The status of any required native dependencies (if applicable), including tests for their presence and functionality.
        *   Any detected configuration issues or missing environment variables (e.g., problems with the logger path).

**II. Logging (Pino)**

1.  **Default File Logger:** Pino is used for logging with a default file logger in the system's log directory (e.g., `~/Library/Logs/`). The log file path is configurable via the `[ProjectName]_LOG_FILE` environment variable.
2.  **Log Path Resilience:**
    *   Pino logic must automatically create missing parent directories for the specified log file path.
    *   If pino cannot write to the `[ProjectName]_LOG_FILE` path, it must fall back to logging to the default temporary directory path.
3.  **Configurable Log Level:** The log level is set using the `[ProjectName]_LOG_LEVEL` environment variable (accepts upper, lower, or mixed case values).
4.  **Optional Console Logging:** An environment variable, `[ProjectName]_CONSOLE_LOGGING=true`, enables logging to the console in addition to the pino file logger.
5.  **Logger Flush:** The logger must be flushed before the process exits to ensure all log messages are written.

**III. Code, Dependencies & Build**

1.  **Dependency Management:** All dependencies should be kept at their latest stable versions. (The release script will warn for outdated dependencies).
2.  **Static Analysis:** There must be no linter (e.g., ESLint) or TypeScript errors.
3.  **File Size:** No single file should exceed 500 lines of code (LOC); aim for below 300 LOC.
4.  **Execution with Compiled Code:** The startup logic and all tool operations must always use the compiled JavaScript output (e.g., from the `dist` folder).
5.  **Shebangs:** Compiled JavaScript files intended for direct execution must have the correct shebang (e.g., `#!/usr/bin/env node`).
6.  **NPM Package Contents:** The published npm package must contain only the absolute minimum files: the `dist/` folder, any potential native components, the `README.md`, and a `LICENSE` file.

**IV. Testing**

1.  **Test Framework:** Tests must use `vitest`.
2.  **TypeScript Test Suite:** A comprehensive test suite for the TypeScript layer is required.
3.  **End-to-End (E2E) Tests:** E2E tests that validate the complete setup are necessary. (These might be run as release preparation if CI execution is challenging due to permissions like macOS access).
4.  **NPM Scripts:**
    *   `npm run prepare-release` executes a comprehensive test suite (detailed in Section VI).
    *   `npm run inspector` executes `npx @modelcontextprotocol/inspector node path/to/server/index.js`.

**V. Native Binary Rules (If Applicable)**

1.  **macOS Compatibility:** The binary must be universal (Apple Silicon & Intel) and support the current macOS version and the previous major version (n-1, e.g., macOS >= 14 if current is 15).
2.  **Build Optimization:** Compiler and linker flags must be set to achieve a minimal binary file size.
3.  **Native Test Suite:** A comprehensive test suite using Swift's native testing tools (e.g., `swift-test` or XCTest) is required.
4.  **Custom Path Configuration:** An environment variable must allow setting a custom absolute path to run the native binary.
5.  **Error Communication:** If the tool uses a native library, `errno` (or an equivalent mechanism) must be used to pass error and execution issues to the TypeScript logger and back to the tool.
6.  **Version Synchronization:** The native CLI and the MCP tool (TypeScript package) must have the same version number. This version must be injected during the build process, not hardcoded, while still allowing easy development (e.g., in Xcode using current source, with the script replacing the version on build).
7.  **Native Code Quality:**
    *   The CLI must have no linter issues (e.g., SwiftLint for Swift).
    *   A formatter must be applied (e.g., SwiftFormat for Swift).
    *   The CLI must show no analyzer issues.
8.  **JSON Communication:** The native binary part of the tool must have a mode to communicate in JSON back to the TypeScript server for easier parsing. JSON responses should include debug logs if requested (e.g., by passing a log level).
9.  **CLI Help Command:** The binary must respond to `--help` with a helpful command explaining its use and all options.
10. **Argument Parsing Framework:** The binary must use a robust argument parser framework (e.g., `swift-argument-parser` for Swift).
11. **Single File Distribution:** For native CLIs, consider options for distributing as a single, statically linked binary if feasible and beneficial for simpler installation by end-users who might use the CLI directly.

**VI. Rules to Check Before a Release (`scripts/prepare-release.js`)**

*   There is a `scripts/prepare-release.js` that runs an extensive test suite. The script runs these checks sequentially and stops at the first failure.

    **Git & Version Control:**
    1.  Check current branch (warns if not on main or designated release branch).
    2.  Check for uncommitted changes.
    3.  Check if synced with origin/main (or designated release branch).
    4.  Version availability check (ensures version isn't already published).
    5.  Version consistency between `package.json` and `package-lock.json`.
    6.  **Changelog Check:** Check for a changelog entry corresponding to the current version.

    **Code Quality & Security:**
    1.  Dependency installation check.
    2.  Outdated dependencies check (warning only).
    3.  Security audit (fails on critical/high vulnerabilities).
    4.  TypeScript compilation.
    5.  TypeScript tests.
    6.  TypeScript declaration files generation.
    7.  Delete any build folders and reset package caches before building.
    8.  *If native binary exists:* Swift analyze.
    9.  *If native binary exists:* Swift formatting (SwiftFormat).
    10. *If native binary exists:* Swift linting (SwiftLint).
    11. *If native binary exists:* Swift tests.
    12. No build warnings.

    **Binary & CLI Validation (If Applicable):**
    13. *If native binary exists:* Swift CLI command tests (help, version, and other key functionalities).
    14. *If native binary exists:* Swift CLI error handling tests (invalid commands, missing args, invalid window index, etc.).
    15. *If native binary exists:* Swift CLI JSON output validation.
    16. *If native binary exists:* Binary exists and is executable.
    17. *If native binary exists:* Binary contains both architectures (arm64 + x86_64, verifiable via `lipo -info`).
    18. *If native binary exists:* Binary responds correctly to `--help`.

    **Package Validation:**
    19. Required fields in `package.json`.
    20. Package size check (warns if >2MB, configurable threshold).
    21. Executable permission check in `postinstall` (if a CLI is present).
    22. Critical files included (e.g., `dist/index.js`, native binary name, `README.md`, `LICENSE`).
    23. MCP server smoke test (JSON-RPC request/response).
    24. Full integration tests.

*   Releases are first done with a `beta` tag to the npm registry so they can be tested via the `npx [packageName]@beta install` method.
## Swift Observable

Here is the content from the Apple Developer documentation page "Migrating from the Observable Object protocol to the Observable macro" converted to Markdown format.

# Migrating from the Observable Object protocol to the Observable macro

Update your existing app to leverage the benefits of Observation in Swift.

***

## Overview

Starting with iOS 17, iPadOS 17, macOS 14, tvOS 17, and watchOS 10, SwiftUI provides support for Observation, a Swift-specific implementation of the observer design pattern. Adopting Observation provides your app with the following benefits:

> *   Tracking optionals and collections of objects, which isn't possible when using `ObservableObject`.
> *   Using existing data flow primitives like `State` and `Environment` instead of object-based equivalents such as `StateObject` and `EnvironmentObject`.
> *   Updating views based on changes to the observable properties that a view's body reads instead of any property changes that occur to an observable object, which can help improve your app's performance.

To take advantage of these benefits in your app, you'll discover how to replace existing source code that relies on `ObservableObject` with code that leverages the `@Observable()` macro.

***

## Use the Observable macro

To adopt Observation in an existing app, begin by replacing `ObservableObject` in your data model type with the `@Observable()` macro. The `@Observable()` macro generates source code at compile time that adds observation support to the type.

**BEFORE**
```swift
// BEFORE
import SwiftUI

class Library: ObservableObject {
    // ...
}
```

**AFTER**
```swift
// AFTER
import SwiftUI

@Observable
class Library {
    // ...
}
```

Then remove the `@Published` property wrapper from observable properties. Observation doesn't require a property wrapper to make a property observable. Instead, the accessibility of the property in relationship to an observer, such as a view, determines whether a property is observable.

**BEFORE**
```swift
// BEFORE
@Observable
class Library {
    @Published var books: [Book] = [Book(), Book(), Book()]
}
```

**AFTER**
```swift
// AFTER
@Observable
class Library {
    var books: [Book] = [Book(), Book(), Book()]
}
```

If you have properties that are accessible to an observer that you don't want to track, apply the `@ObservationIgnored()` macro to the property.

***

## Migrate incrementally

You don't need to make a wholesale replacement of the `ObservableObject` protocol throughout your app. Instead, you can make changes incrementally. Start by changing one data model type to use the `@Observable()` macro. Your app can mix data model types that use different observation systems. However, SwiftUI tracks changes differently based on the observation system that a data model type uses, `Observable` versus `ObservableObject`.

You may notice slight behavioral differences in your app based on the tracking method. For instance, when tracking as `@Observable()`, SwiftUI updates a view only when an observable property changes and the view's body reads the property directly. The view doesn't update when observable properties not read by body changes. In contrast, a view updates when any published property of an `ObservableObject` instance changes, even if the view doesn't read the property that changes, when tracking as `ObservableObject`.

> **Note:** To learn more about when SwiftUI updates views when observable properties change, see [Managing model data in your app](https://developer.apple.com/documentation/swiftui/managing-model-data).

***

## Migrate other source code

After applying the `@Observable()` macro, you can update your data flow primitives. Although `StateObject` and `EnvironmentObject` support types using the `@Observable()` macro for incremental migration, you should replace them with `State` and `Environment` to fully adopt Observation.

**BEFORE**
```swift
// BEFORE
@main
struct BookReaderApp: App {
    @StateObject private var library = Library()

    var body: some Scene {
        WindowGroup {
            LibraryView()
                .environmentObject(library)
        }
    }
}
```

**AFTER**
```swift
// AFTER
@main
struct BookReaderApp: App {
    @State private var library = Library()

    var body: some Scene {
        WindowGroup {
            LibraryView()
                .environment(library)
        }
    }
}
```

Similarly, replace `@EnvironmentObject` with the `@Environment` property wrapper.

**BEFORE**
```swift
// BEFORE
struct LibraryView: View {
    @EnvironmentObject var library: Library

    var body: some View {
        List(library.books) { book in
            BookView(book: book)
        }
    }
}
```

**AFTER**
```swift
// AFTER
struct LibraryView: View {
    @Environment(Library.self) private var library

    var body: some View {
        List(library.books) { book in
            BookView(book: book)
        }
    }
}
```

***

## Remove the ObservedObject property wrapper

To complete the migration, change other data model types to support Observation by replacing `ObservableObject` with the `@Observable()` macro and removing `@Published`.

**BEFORE**
```swift
// BEFORE
class Book: ObservableObject, Identifiable {
    @Published var title = "Sample Book Title"
    let id = UUID() // A unique identifier that never changes.
}
```

**AFTER**
```swift
// AFTER
@Observable
class Book: Identifiable {
    var title = "Sample Book Title"
    let id = UUID() // A unique identifier that never changes.
}
```

Next, remove the `@ObservedObject` property wrapper. SwiftUI automatically tracks any observable properties that a view's body reads directly.

**BEFORE**
```swift
// BEFORE
struct BookView: View {
    @ObservedObject var book: Book
    @State private var isEditorPresented = false

    var body: some View {
        HStack {
            Text(book.title)
            Spacer()
            Button("Edit") {
                isEditorPresented = true
            }
        }
        .sheet(isPresented: $isEditorPresented) {
            BookEditView(book: book)
        }
    }
}
```

**AFTER**
```swift
// AFTER
struct BookView: View {
    var book: Book
    @State private var isEditorPresented = false

    var body: some View {
        HStack {
            Text(book.title)
            Spacer()
            Button("Edit") {
                isEditorPresented = true
            }
        }
        .sheet(isPresented: $isEditorPresented) {
            BookEditView(book: book)
        }
    }
}
```

If a view needs a binding to an observable type, replace `@ObservedObject` with the `@Bindable` property wrapper.

**BEFORE**
```swift
// BEFORE
struct BookEditView: View {
    @ObservedObject var book: Book
    @Environment(\.dismiss) private var dismiss

    var body: some View {
        VStack() {
            TextField("Title", text: $book.title)
                .textFieldStyle(.roundedBorder)
                .onSubmit {
                    dismiss()
                }
            Button("Close") {
                dismiss()
            }
            .buttonStyle(.borderedProminent)
        }
        .padding()
    }
}
```

**AFTER**
```swift
// AFTER
struct BookEditView: View {
    @Bindable var book: Book
    @Environment(\.dismiss) private var dismiss

    var body: some View {
        VStack() {
            TextField("Title", text: $book.title)
                .textFieldStyle(.roundedBorder)
                .onSubmit {
                    dismiss()
                }
            Button("Close") {
                dismiss()
            }
            .buttonStyle(.borderedProminent)
        }
        .padding()
    }
}
```
## GitHub Issue Creation


Credit: This rule is based on instructions by @nityeshaga (https://x.com/nityeshaga/status/1933113428379574367)

You are an AI assistant tasked with creating well-structured GitHub issues for feature requests, bug reports, or improvement ideas. Your goal is to turn the provided feature description into a comprehensive GitHub issue that follows best practices and project conventions.

First, you will be given a feature description and a repository URL. Here they are:

<feature_description> #$ARGUMENTS </feature_description>

Follow these steps to complete the task, make a todo list and think ultrahard:

### 1. Research the repository:
   - Visit the provided repo url and examine the repository's structure, existing issues, and documentation.
   - Look for any CONTRIBUTING.md, ISSUE_TEMPLATE.md, or similar files that contain guidelines for creating issues.
   - Note the project's coding style, naming conventions, and any specific requirements for submitting issues.

### 2. Research best practices:
   - Search for current best practices in writing GitHub issues, focusing on clarity, completeness, and actionability.
   - Look for examples of well-written issues in popular open-source projects for inspiration.

### 3. Present a plan:
   - Based on your research, outline a plan for creating the GitHub issue.
   - Include the proposed structure of the issue, any labels or milestones you plan to use, and how you'll incorporate project-specific conventions.
   - Present this plan in <plan> tags.
   - Include the reference link to featurebase or any other link that has the source of the user request
   *K for Command, *L for Cascade

### 4. Create the GitHub issue:
   - Once the plan is approved, draft the GitHub issue content.
   - Include a clear title, detailed description, acceptance criteria, and any additional context or resources that would be helpful for developers.
   - Use appropriate formatting (e.g., Markdown) to enhance readability.
   - Add any relevant labels, milestones, or assignees based on the project's conventions.

### 5. Final output:
   - Present the complete GitHub issue content in <github_issue> tags.
   - Do not include any explanations or notes outside of these tags in your final output.

Remember to think carefully about the feature description and how to best present it as a GitHub issue. Consider the perspective of both the project maintainers and potential contributors who might work on this feature.

Your final output should consist of only the content within the <github_issue> tags, ready to be copied and pasted directly into GitHub. Make sure to use the GitHub CLI `gh issue create` to create the actual issue after you generate. Assign either the label `bug` or `enhancement` based on the nature of the issue.
## MCP Peekaboo Setup


This rule sets up the Peekaboo MCP server, which provides screenshot capture and AI-powered vision analysis capabilities.

## Overview

Peekaboo is a Model Context Protocol server that enables Claude to:
- Take screenshots of your screen
- Analyze images using AI vision models
- Support both OpenAI and Ollama providers

## Prerequisites

- macOS 14.0+ (Sonoma or later)
- Node.js 20.0+
- OpenAI API key (stored in `~/.zshrc`)
- Optional: Ollama with vision models installed

## Configuration

Add this to your Claude Desktop configuration (`~/Library/Application Support/Claude/claude_desktop_config.json`):

```json
{
  "mcpServers": {
    "peekaboo": {
      "command": "npx",
      "args": [
        "-y",
        "@steipete/peekaboo-mcp"
      ],
      "env": {
        "PEEKABOO_AI_PROVIDERS": "openai/gpt-4o,ollama/llava:latest",
        "OPENAI_API_KEY": "<READ_FROM_ZSHRC>",
        "PEEKABOO_LOG_LEVEL": "info",
        "PEEKABOO_DEFAULT_SAVE_PATH": "~/Desktop"
      }
    }
  }
}
```

## Security Setup

To securely extract the OpenAI API key from `~/.zshrc`:

```bash
# Extract API key from .zshrc
export OPENAI_API_KEY=$(grep "export OPENAI_API_KEY=" ~/.zshrc | cut -d'"' -f2)

# Update Claude config with the actual key
jq --arg key "$OPENAI_API_KEY" \
  '.mcpServers.peekaboo.env.OPENAI_API_KEY = $key' \
  ~/Library/Application\ Support/Claude/claude_desktop_config.json > tmp.json && \
  mv tmp.json ~/Library/Application\ Support/Claude/claude_desktop_config.json
```

## Available Tools

Once configured, you'll have access to:

1. **peekaboo_capture_screenshot**
   - Takes a screenshot of the entire screen or a specific display
   - Saves to the default path or specified location

2. **peekaboo_analyze_screenshot**
   - Captures and analyzes a screenshot with AI
   - Uses the configured AI providers for vision analysis

## Usage Examples

### Basic Screenshot
```
Take a screenshot of my screen
```

### Screenshot with Analysis
```
Take a screenshot and tell me what application is currently in focus
```

### Multi-monitor Support
```
Take a screenshot of display 2
```

## Troubleshooting

1. **Permission Issues**
   - Grant screen recording permission to Terminal/Claude
   - System Preferences → Privacy & Security → Screen Recording

2. **API Key Issues**
   - Verify `OPENAI_API_KEY` is set in `~/.zshrc`
   - Check the key is valid and has sufficient credits

3. **Ollama Connection**
   - Ensure Ollama is running: `ollama serve`
   - Verify vision model is installed: `ollama pull llava:latest`

## Provider Configuration

### OpenAI Only
```json
"PEEKABOO_AI_PROVIDERS": "openai/gpt-4o"
```

### Ollama Only
```json
"PEEKABOO_AI_PROVIDERS": "ollama/llava:latest"
```

### Multiple Providers (Fallback)
```json
"PEEKABOO_AI_PROVIDERS": "openai/gpt-4o,ollama/llava:latest"
```

## Log Levels

- `error`: Only errors
- `warn`: Errors and warnings
- `info`: General information (default)
- `debug`: Detailed debugging information

## Related Resources

- [Peekaboo MCP Repository](https://github.com/steipete/peekaboo-mcp)
- [Model Context Protocol Docs](https://modelcontextprotocol.io)

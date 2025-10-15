# Smart Assets Documentation Repository Guidelines

**Note:** For general Smart Assets workspace guidelines, see [../CLAUDE.md](../CLAUDE.md) at the SA workspace root. This file contains specific guidance for this documentation repository.

## Project Context
- This is the original Smart Assets documentation and reference code repository.
- Contains conceptual documentation for Smart Assets using purses and smart wallets.
- Originated from Chapman University course "Introduction to Smart Contracts"
- This project has been moved to GitLab: https://gitlab.com/smart-assets.io/
- Repository serves as historical reference and documentation hub

## Project Overview
Smart Assets are conceptualized as containers providing:
- Purse and Smart Wallet capabilities across various blockchains
- Framework implementations using channel encapsulation and linear channels
- Support for Bitcoin, Ethereum, and other blockchain platforms

## Reference Implementations
Documentation and reference code for the following smart contract languages:
- **Rholang** - RChain's concurrent smart contract language
- **Metta** - SingularityNET's language
- **Move** - Aptos/Sui blockchain language
- **Solidity** - Ethereum and EVM-compatible chains
- **Rust** - Solana and other Rust-based platforms

## Documentation Structure
- **docs/drawings/** - Conceptual diagrams including Containerized_diagram.png
- **README.md** - Main project overview and concept explanation
- **src/** - Reference implementations (if present)

## Commands

### Git Interaction

**For LLM assistance in multi-repo workspace:**
See [Git Interaction Policy](../top-level-gitlab-profile/docs/common/git-interaction-policy.md)

**For reference (GitLab):**
[Git Interaction Policy](https://gitlab.com/smart-assets.io/gitlab-profile/-/blob/master/docs/common/git-interaction-policy.md)

**Summary for this project:**
- This is primarily a documentation repository
- DO NOT ever `git add`, `git rm` or `git commit` code
- `git mv` is permitted with user confirmation
- YOLO mode exceptions apply in git worktrees

## Code Style
- When adding reference implementations:
  - Follow language-specific best practices for each blockchain platform
  - Include comprehensive comments explaining the purse/container concepts
  - Provide clear examples demonstrating channel encapsulation
  - Document security considerations for each implementation

## Best Practices
- Maintain conceptual clarity in documentation
- Keep diagrams up to date with evolving concepts
- Cross-reference between different language implementations
- Link to active GitLab repositories for current development
- Preserve historical context and evolution of ideas

## Common Tasks
- If connected to a `mcp-shell-server` also known as just a "shell", run all shell commands through that mcp server
- Review `git history` to understand the evolution of Smart Assets concepts
- Reference this repository for foundational concepts when working on active GitLab projects

## Project Specifics
- This repository serves as the conceptual foundation for the Smart Assets ecosystem
- Active development has moved to GitLab: https://gitlab.com/smart-assets.io/
- Use this repository for:
  - Understanding core Smart Assets concepts
  - Historical reference
  - Educational materials
  - Cross-platform implementation patterns

## Testing

**For LLM assistance in multi-repo workspace:**
See [Testing Guidelines](../top-level-gitlab-profile/docs/common/testing-guidelines.md)

**For reference (GitLab):**
[Testing Guidelines](https://gitlab.com/smart-assets.io/gitlab-profile/-/blob/master/docs/common/testing-guidelines.md)

**Project-specific approach:**
- This is primarily a documentation repository with reference code
- Reference implementations should include example tests demonstrating:
  - Testing patterns for each blockchain platform
  - Security testing for purse/wallet implementations
  - Channel encapsulation verification
- Test coverage targets apply to any reference code (90%+)
- Example tests serve as educational material

## Security Considerations

**For LLM assistance in multi-repo workspace:**
See [Security Best Practices](../top-level-gitlab-profile/docs/common/security-best-practices.md)

**For reference (GitLab):**
[Security Best Practices](https://gitlab.com/smart-assets.io/gitlab-profile/-/blob/master/docs/common/security-best-practices.md)

**Project-specific considerations:**
- Document security patterns for purse implementations
- Highlight channel encapsulation security benefits
- Explain linear type system advantages for asset management
- Never commit secrets or private keys in example code
- Follow smart contract security best practices for each language (Solidity, Move, Rholang, Rust)

## Related Projects
- GitLab: https://gitlab.com/smart-assets.io/ (active development)
- See other directories in parent SA/ for related projects:
  - BountyForge - Bounty and incentive systems
  - SA_build_agentics - Autonomous AI development framework
  - samplesmartassets - Sample implementations
  - SATCHEL - Authentication and security
  - smart-assets.io - SSL projects
  - SovereignLicense - License framework
  - Websites_apps - Website and application projects

# important-instruction-reminders
Do what has been asked; nothing more, nothing less.
NEVER create files unless they're absolutely necessary for achieving your goal.
ALWAYS prefer editing an existing file to creating a new one.
NEVER proactively create documentation files (*.md) or README files. Only create documentation files if explicitly requested by the User.

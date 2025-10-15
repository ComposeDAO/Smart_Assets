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

### Cross-Platform Smart Asset Patterns

```yaml
reference_implementations:
  rholang:
    name: Rholang
    platform: RChain
    description: Concurrent smart contract language with process calculus foundation
    purse_implementation:
      approach: Process-based purse using channel encapsulation
      linear_types: Built-in support for linear channels
      concurrency: Native concurrent operations with actors
      security: Capability-based security model
    reference_files:
      - docs/rholang/purse_implementation.rho
      - docs/rholang/smart_wallet.rho
    key_concepts:
      - Process calculus for contract logic
      - Channel-based communication
      - Linear types for asset safety
      - Concurrent transaction processing

  metta:
    name: Metta
    platform: SingularityNET
    description: AI-focused smart contract language with advanced type system
    purse_implementation:
      approach: Type-safe purse with AI integration capabilities
      linear_types: Advanced type system for resource management
      ai_integration: Native AI model integration
      security: Formal verification support
    reference_files:
      - docs/metta/purse_implementation.metta
      - docs/metta/ai_smart_wallet.metta
    key_concepts:
      - Type-safe asset management
      - AI-enhanced contract logic
      - Formal verification patterns
      - Integration with AI services

  move:
    name: Move
    platform: Aptos/Sui
    description: Resource-oriented programming language with linear types
    purse_implementation:
      approach: Resource-based purse using Move's linear type system
      linear_types: Native resource types ensure asset safety
      modules: Modular contract architecture
      security: Formal verification with Move Prover
    reference_files:
      - docs/move/purse_module.move
      - docs/move/smart_wallet.move
    key_concepts:
      - Resource types for assets
      - Module-based architecture
      - Formal verification
      - Cross-chain compatibility (Aptos/Sui)

  solidity:
    name: Solidity
    platform: Ethereum and EVM-compatible chains
    description: Most widely used smart contract language for EVM blockchains
    purse_implementation:
      approach: Contract-based purse with ERC standards
      linear_types: Implemented through design patterns (not native)
      standards: ERC-20, ERC-721, ERC-1155 integration
      security: Audited patterns and best practices
    reference_files:
      - docs/solidity/Purse.sol
      - docs/solidity/SmartWallet.sol
    key_concepts:
      - Contract-oriented architecture
      - ERC standard compliance
      - Gas optimization patterns
      - Reentrancy protection

  rust:
    name: Rust
    platform: Solana and Rust-based platforms
    description: Systems programming language with ownership model
    purse_implementation:
      approach: Account-based purse using Rust ownership model
      linear_types: Ownership and borrowing ensure asset safety
      performance: High-performance concurrent operations
      security: Memory safety without garbage collection
    reference_files:
      - docs/rust/purse_program.rs
      - docs/rust/smart_wallet.rs
    key_concepts:
      - Ownership and borrowing
      - Account model (Solana)
      - Zero-cost abstractions
      - Concurrent programming
```

### Cross-Platform Development Guidance

```yaml
cross_platform_considerations:
  choosing_platform:
    rchain_rholang:
      best_for:
        - Concurrent transaction processing
        - Process calculus-based logic
        - Native channel communication
      trade_offs:
        - Smaller ecosystem
        - Fewer tooling options
        - Learning curve for process calculus

    singularitynet_metta:
      best_for:
        - AI-integrated smart contracts
        - Advanced type systems
        - Formal verification requirements
      trade_offs:
        - Emerging platform
        - Limited production usage
        - AI integration complexity

    aptos_sui_move:
      best_for:
        - Resource-oriented programming
        - Formal verification
        - Linear type safety
      trade_offs:
        - Newer ecosystem
        - Platform-specific variations (Aptos vs Sui)
        - Limited DeFi integrations

    ethereum_solidity:
      best_for:
        - Maximum ecosystem compatibility
        - Extensive tooling and libraries
        - Large developer community
      trade_offs:
        - Gas costs can be high
        - Linear types not native
        - Reentrancy and security complexity

    solana_rust:
      best_for:
        - High-performance applications
        - Low transaction costs
        - Concurrent processing
      trade_offs:
        - Account model complexity
        - Rust learning curve
        - Different programming model

  security_patterns_by_platform:
    channel_encapsulation:
      platforms: [Rholang, Metta]
      approach: Use process channels to encapsulate purse state
      benefits: Natural isolation and capability-based security

    linear_types:
      platforms: [Move, Rust, Rholang]
      approach: Use type system to ensure assets aren't duplicated or lost
      benefits: Compile-time safety for asset management

    design_patterns:
      platforms: [Solidity]
      approach: Implement linear type behavior through patterns
      benefits: Works on established platforms without native support
      caution: Requires careful implementation and auditing

    ownership_model:
      platforms: [Rust, Move]
      approach: Use language ownership semantics for asset safety
      benefits: Memory and resource safety guarantees
```

### Blockchain-Specific Implementation Notes

```yaml
blockchain_considerations:
  bitcoin_integration:
    approach: Layer 2 solutions and RGB protocol
    reference_project: https://gitlab.com/smart-assets.io/SATCHEL/f1r3fly-rgb
    purse_implementation:
      - RGB assets on Bitcoin
      - Lightning Network integration
      - UTXO-based asset management
    security_focus:
      - Bitcoin transaction security
      - RGB state verification
      - Lightning channel safety

  ethereum_evm:
    approach: Smart contracts on EVM-compatible chains
    purse_implementation:
      - ERC standards for tokens
      - Contract wallet patterns
      - Meta-transactions for UX
    security_focus:
      - Reentrancy protection
      - Integer overflow/underflow
      - Access control patterns
      - Gas optimization

  rchain:
    approach: Native Rholang smart contracts
    purse_implementation:
      - Process-based purses
      - Channel encapsulation
      - Concurrent operations
    security_focus:
      - Capability security
      - Process isolation
      - Channel safety

  aptos_sui:
    approach: Move modules and resources
    purse_implementation:
      - Resource types for assets
      - Module-based architecture
      - Object model (Sui) vs Account model (Aptos)
    security_focus:
      - Resource safety
      - Formal verification
      - Module composition

  solana:
    approach: Rust programs with account model
    purse_implementation:
      - Account-based state
      - Program-derived addresses
      - Cross-program invocation
    security_focus:
      - Account validation
      - Ownership checks
      - Signer verification
```

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

# YAMO Examples

Example YAMO files and starter templates for the YAMO Protocol.

## Overview

This repository contains reference implementations and examples of YAMO blocks demonstrating various use cases, patterns, and best practices.

## Examples

### `skill-adapter.yamo`

Demonstrates skill adaptation and learning patterns. Shows how an agent can:
- Receive a skill definition
- Adapt it to a new context
- Document the adaptation process
- Hand off to validation

**Use Case**: Skill transfer between agents or contexts

### `translate.yamo`

Large-scale translation workflow showing:
- Multi-stage processing
- Extensive logging
- Output artifact generation
- Detailed metadata tracking
- Quality assurance steps

**Use Case**: Complex document processing pipelines

### `yamo-super.yamo`

Comprehensive "super block" demonstrating:
- All YAMO DSL features
- Multiple constraint types
- Rich metadata
- Multi-agent handoffs
- Priority management
- Context tracking

**Use Case**: Reference implementation for protocol features

### `test_bundle.yamo`

Minimal test case for:
- IPFS deep bundling
- Output artifact inclusion
- Basic block structure

**Use Case**: Testing and validation

### `code_analysis_report.json`

Example output artifact showing:
- Structured analysis results
- JSON format output
- Integration with YAMO blocks

**Use Case**: Bundled artifacts with YAMO blocks

## YAMO File Structure

Basic YAMO block structure:

```yamo
agent: AgentName;
intent: describe_what_agent_is_doing;
context: relevant;context;info;
constraints:
  - constraint_type;value;
  - another_constraint;value;
priority: low|medium|high;
output: output_file.ext;
meta: key;value;
log: event_name;field;value;
handoff: NextAgentName;
```

## Using Examples

### With YAMO CLI

```bash
# Submit an example to the blockchain
yamo submit skill-adapter.yamo

# Calculate hash
yamo hash translate.yamo

# Audit a block
yamo audit block_001
```

### With MCP Server

Use the examples as templates when calling the MCP server tools from Claude or other AI agents.

### As Templates

Copy and modify these examples for your own YAMO blocks:

```bash
cp skill-adapter.yamo my-agent-block.yamo
# Edit my-agent-block.yamo
yamo submit my-agent-block.yamo
```

## Best Practices

1. **Clear Intent**: Use descriptive intent statements
2. **Rich Context**: Provide sufficient context for verification
3. **Meaningful Constraints**: Add constraints that matter
4. **Structured Logging**: Log key events and decisions
5. **Output Artifacts**: Include relevant output files
6. **Handoff Clarity**: Specify next steps explicitly

## Contributing

Have a useful YAMO example? Submit a PR with:
- The `.yamo` file
- Any associated output artifacts
- Description in this README
- Use case explanation

## License

MIT

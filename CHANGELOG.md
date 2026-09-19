# Changelog

All notable changes to **AlphaRoute** are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-09-19

### Added
- **Unified Multi-Broker Gateway**:
  - Declarative schema normalization layer using `@pre` and `@post` decorators with YAML mappings.
  - Native broker adapters for Zerodha Kite, Finvasia Shoonya, ICICI Direct Breeze, Kotak Neo, and an embedded Paper Broker.
- **Deterministic Order State Engine**:
  - Pydantic v2 data models with strict validation across all order fields and attributes.
  - Comprehensive lifecycle states: `PENDING`, `SUBMITTED`, `TRIGGER_PENDING`, `OPEN`, `PARTIALLY_FILLED`, `COMPLETE`, `CANCELLED`, and `REJECTED`.
  - Thread-safe safety locks (`OrderLock`) to prevent concurrent modification or cancellation race conditions.
  - Built-in time-in-force timers (`expires_in`) with automated actions (auto-cancellation, market conversion on expiry).
- **Multi-Leg Strategy Baskets (`CompoundOrder`)**:
  - Atomic execution of complex multi-leg structures (options straddles, strangles, spreads, brackets, pairs).
  - Real-time Mark-to-Market (MTM) calculations and net position reconciliation from live ticker streams.
  - Batch order modifications and synchronization with exchange trade feeds.
- **Algorithmic Execution Suite**:
  - Dynamic pegged orders (`PegNew`, `PegExisting`) tracking Level 2 market depth and best bid/ask.
  - Multi-tier trailing stop-loss algorithms with configurable step increments.
  - Automated options straddle engine for systematic volatility trading.
- **Simulation and Testing Sandbox**:
  - In-memory virtual exchange and matching engine simulating realistic slippage, fill latencies, and partial fills.
  - Standalone simulation server for end-to-end integration and algorithmic testing.
- **Crash-Resilient Audit Logging**:
  - Embedded SQLite database integration for synchronous order tracking, state persistence, and session recovery.

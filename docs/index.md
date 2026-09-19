# AlphaRoute Documentation

AlphaRoute is a high-performance, broker-agnostic Python library for algorithmic order management, multi-broker routing, and execution strategies.

## Overview

AlphaRoute provides quantitative and algorithmic traders with a unified, deterministic framework to create, execute, track, and manage orders across different brokers and trading venues without rewriting strategy code.

### Key Highlights

- **Multi-Broker Connectivity**: Support for Zerodha, Finvasia, ICICI Direct, Kotak Neo, and Paper trading.
- **Deterministic State Machine**: Pydantic-validated order states with thread-safe execution locks.
- **Multi-Leg Strategy Baskets**: Atomic execution of options straddles, spreads, and pairs with real-time MTM.
- **Smart Execution Primitives**: Pegged orders, trailing stops, and market depth routers.
- **Embedded Simulation**: Virtual order matching engine with slippage and latency modeling.
- **Session Persistence**: Automated SQLite audit trail and session recovery.

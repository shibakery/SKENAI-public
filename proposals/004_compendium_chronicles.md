# SIP-004: The Chronicles Compendium - A Living Memory

*Proposed: 2024-12-18 10:26 UTC+2*

## Abstract

This proposal establishes the SKENAI Chronicles Compendium, a living document system that tracks the evolution of our infinite game. Contributors will be compensated through a flexible SAFT-like agreement, allowing them to choose between immediate USDT payments or future token allocations in SBX and SBV.

## Motivation

As SKENAI grows, we need a systematic way to document our journey, track proposals, and engage our community. The Chronicles Compendium will serve as both historical record and future roadmap, maintained by dedicated chroniclers who are invested in our success through token-based incentives.

## Specification

### 1. Compendium Structure

#### 1.1 Core Components
- Timeline View (weekly, monthly, quarterly updates)
- Status Dashboard (proposal tracking)
- Implementation Progress
- Community Metrics
- Market Analysis
- Technical Documentation Links

#### 1.2 Update Frequency
- Real-time proposal status updates
- Weekly community summaries
- Monthly retrospectives
- Quarterly strategic reviews

### 2. Chronicler Roles

#### 2.1 Primary Chronicler
- Maintains core documentation
- Coordinates with other chroniclers
- Reviews and merges updates
- Ensures consistency and quality

#### 2.2 Technical Chronicler
- Documents technical implementations
- Maintains API documentation
- Tracks smart contract deployments
- Updates technical specifications

#### 2.3 Community Chronicler
- Tracks community engagement
- Documents governance decisions
- Maintains social metrics
- Creates community summaries

### 3. Compensation Structure

#### 3.1 Payment Options
Contributors can choose their compensation in:
1. USDT (immediate payment)
2. SBX tokens (future allocation)
3. SBV tokens (future allocation)
4. Mixed payment (combination of above)

#### 3.2 SAFT-Like Agreement Terms
```solidity
struct ChroniclerAgreement {
    address chronicler;
    uint256 usdtAmount;      // Optional immediate payment
    uint256 sbxAllocation;   // Future SBX tokens
    uint256 sbvAllocation;   // Future SBV tokens
    uint256 vestingPeriod;   // In days
    uint256 cliffPeriod;     // In days
    bool isActive;
}
```

#### 3.3 Vesting Schedule
- 6-month cliff period
- 24-month linear vesting
- Emergency provisions for quality assurance

#### 3.4 Performance Metrics
- Documentation quality score (1-100)
- Update frequency compliance
- Community feedback rating
- Technical accuracy score

### 4. Implementation Phases

#### Phase 1: Foundation (Weeks 1-4)
- [x] Basic compendium structure
- [ ] Initial chronicler onboarding
- [ ] SAFT agreement templates
- [ ] Basic metrics dashboard

#### Phase 2: Expansion (Weeks 5-12)
- [ ] Advanced analytics integration
- [ ] Automated update system
- [ ] Community feedback loops
- [ ] Cross-chain payment integration

#### Phase 3: Optimization (Weeks 13-24)
- [ ] Machine learning for metrics
- [ ] Automated report generation
- [ ] Advanced visualization tools
- [ ] DAO integration

### 5. Technical Integration

```solidity
contract ChroniclerRegistry {
    mapping(address => ChroniclerAgreement) public agreements;
    
    event NewChronicler(address indexed chronicler, uint256 timestamp);
    event CompensationClaimed(address indexed chronicler, uint256 amount);
    
    function registerChronicler(
        uint256 _usdtAmount,
        uint256 _sbxAllocation,
        uint256 _sbvAllocation,
        uint256 _vestingPeriod
    ) external {
        // Implementation details
    }
    
    function claimCompensation() external {
        // Implementation details
    }
}
```

### 6. Governance Rights

Chroniclers receive additional voting power in governance decisions related to:
- Documentation standards
- Compensation adjustments
- Process improvements
- Quality metrics

## Security Considerations

1. Multi-sig requirement for compensation changes
2. Time-locked modifications to agreements
3. Quality assurance checkpoints
4. Regular security audits

## Backwards Compatibility

The proposal maintains compatibility with:
- Existing governance structures
- Current token systems
- Documentation standards
- Smart contract architecture

## Test Cases

1. Chronicler registration
2. Compensation calculation
3. Vesting schedule verification
4. Performance metric tracking

## Implementation

```typescript
interface IChronicler {
    function updateCompendium(bytes32 section, string memory content) external;
    function claimRewards() external;
    function getMetrics() external view returns (uint256[4] memory);
}
```

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

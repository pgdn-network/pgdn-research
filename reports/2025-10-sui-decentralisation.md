# Sui Validator Decentralization Analysis

## Executive Summary

Analysis of 122 Sui validators reveals moderate centralization concerns with significant concentration in specific hosting providers and geographic regions.

You can see the **Dataset here:** [`2025-10-decentralisation-sui.csv`](../data/2025-10-decentralisation-sui.csv).

## Key Findings

### Cloud Provider Distribution
- **Latitude.sh**: 22 validators (18.0%)
- **OVH**: 22 validators (18.0%)
- **The Constant Company**: 9 validators (7.4%)
- **Top 3 providers control**: 43.4% of all validators

### Hosting Type Breakdown
- **Dedicated/Colocation**: 68% (83 validators)
- **Cloud (AWS/GCP/Azure/etc)**: 32% (39 validators)

### Major Cloud Providers
- **AWS**: 6 validators (4.9%)
- **GCP**: 6 validators (4.9%)
- **Azure**: 1 validator (0.8%)
- **Combined**: 10.7% of total validators

## AWS Regional Distribution

Out of 6 AWS validators:
- **ap-northeast-1** (Tokyo): 2 validators (33.3%)
- **eu-west-1** (Ireland): 2 validators (33.3%)
- **us-east-1** (Virginia): 1 validator (16.7%)
- **us-east-2** (Ohio): 1 validator (16.7%)

## Geographic Concentration

### Top Countries
1. **United States**: 38 validators (31.1%)
2. **Germany**: 14 validators (11.5%)
3. **United Kingdom**: 14 validators (11.5%)
4. **France**: 14 validators (11.5%)
5. **Japan**: 5 validators (4.1%)
6. **Lithuania**: 5 validators (4.1%)
7. **Netherlands**: 5 validators (4.1%)
8. **Singapore**: 5 validators (4.1%)

## Centralization Risks

### Herfindahl-Hirschman Index (HHI)
- **Score**: 859
- **Classification**: **Unconcentrated** (HHI < 1500)
- This suggests relatively healthy distribution across providers

### Single Points of Failure
1. **Latitude.sh + OVH** = 44 validators (36.1%)
   - These two providers alone host over 1/3 of the network
   
2. **US Geographic Risk** = 38 validators (31.1%)
   - Nearly 1/3 of validators subject to US jurisdiction
   
3. **Western Europe** (GB+DE+FR+NL+IE) = 50 validators (41.0%)
   - Concentrated regulatory risk

## AWS-Specific Concerns

While only 6 validators run on AWS (4.9%), the distribution shows:
- **No single-region dominance**: Spread across 4 regions
- **Multi-region resilience**: 2 in APAC, 2 in EU, 2 in US
- **Availability zone risk**: Unknown (requires AWS API access)

### Critical Note
Within AWS, validators could still be in the same **availability zones** within these regions, which would represent a hidden centralization risk not visible in this analysis.

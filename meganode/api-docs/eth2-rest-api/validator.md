---
description: Endpoints intended for validator clients
---

# Validator

| POST | Endpoint                                                                                                                               |
| ---- | -------------------------------------------------------------------------------------------------------------------------------------- |
| POST | [/eth/v1/validator/duties/attester/{epoch}](https://ethereum.github.io/beacon-APIs/#/Validator/getAttesterDuties)                      |
| GET  | [/eth/v1/validator/duties/proposer/{epoch}](https://ethereum.github.io/beacon-APIs/#/Validator/getProposerDuties)                      |
| POST | [/eth/v1/validator/duties/sync/{epoch}](https://ethereum.github.io/beacon-APIs/#/Validator/getSyncCommitteeDuties)                     |
| GET  | [/eth/v2/validator/blocks/{slot}](https://ethereum.github.io/beacon-APIs/#/Validator/produceBlockV2)                                   |
| GET  | [/eth/v1/validator/blinded\_blocks/{slot}](https://ethereum.github.io/beacon-APIs/#/Validator/produceBlindedBlock)                     |
| GET  | [/eth/v1/validator/attestation\_data](https://ethereum.github.io/beacon-APIs/#/Validator/produceAttestationData)                       |
| GET  | [/eth/v1/validator/aggregate\_attestation](https://ethereum.github.io/beacon-APIs/#/Validator/getAggregatedAttestation)                |
| POST | [/eth/v1/validator/aggregate\_and\_proofs](https://ethereum.github.io/beacon-APIs/#/Validator/publishAggregateAndProofs)               |
| POST | [/eth/v1/validator/beacon\_committee\_subscriptions](https://ethereum.github.io/beacon-APIs/#/Validator/prepareBeaconCommitteeSubnet)  |
| POST | [/eth/v1/validator/sync\_committee\_subscriptions](https://ethereum.github.io/beacon-APIs/#/Validator/prepareSyncCommitteeSubnets)     |
| GET  | [/eth/v1/validator/sync\_committee\_contribution](https://ethereum.github.io/beacon-APIs/#/Validator/produceSyncCommitteeContribution) |
| POST | [/eth/v1/validator/contribution\_and\_proofs](https://ethereum.github.io/beacon-APIs/#/Validator/publishContributionAndProofs)         |
| POST | [/eth/v1/validator/prepare\_beacon\_proposer](https://ethereum.github.io/beacon-APIs/#/Validator/prepareBeaconProposer)                |
| POST | [/eth/v1/validator/register\_validator](https://ethereum.github.io/beacon-APIs/#/Validator/registerValidator)                          |

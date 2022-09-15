---
description: Set of endpoints to query beacon chain.
---

# Beacon

| Method | Endpoint                                                                                                                               |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------- |
| GET    | [/eth/v1/beacon/genesis](https://ethereum.github.io/beacon-APIs/#/Beacon/getGenesis)                                                   |
| GET    | [/eth/v1/beacon/states/{state\_id}/root](https://ethereum.github.io/beacon-APIs/#/Beacon/getStateRoot)                                 |
| GET    | [/eth/v1/beacon/states/{state\_id}/fork](https://ethereum.github.io/beacon-APIs/#/Beacon/getStateFork)                                 |
| GET    | [/eth/v1/beacon/states/{state\_id}/finality\_checkpoints](https://ethereum.github.io/beacon-APIs/#/Beacon/getStateFinalityCheckpoints) |
| GET    | [/eth/v1/beacon/states/{state\_id}/validators](https://ethereum.github.io/beacon-APIs/#/Beacon/getStateValidators)                     |
| GET    | [/eth/v1/beacon/states/{state\_id}/validators/{validator\_id}](https://ethereum.github.io/beacon-APIs/#/Beacon/getStateValidator)      |
| GET    | [/eth/v1/beacon/states/{state\_id}/validator\_balances](https://ethereum.github.io/beacon-APIs/#/Beacon/getStateValidatorBalances)     |
| GET    | [/eth/v1/beacon/states/{state\_id}/committees](https://ethereum.github.io/beacon-APIs/#/Beacon/getEpochCommittees)                     |
| GET    | [/eth/v1/beacon/states/{state\_id}/sync\_committees](https://ethereum.github.io/beacon-APIs/#/Beacon/getEpochSyncCommittees)           |
| GET    | [/eth/v1/beacon/headers](https://ethereum.github.io/beacon-APIs/#/Beacon/getBlockHeaders)                                              |
| GET    | [/eth/v1/beacon/headers/{block\_id}](https://ethereum.github.io/beacon-APIs/#/Beacon/getBlockHeader)                                   |
| POST   | [/eth/v1/beacon/blocks](https://ethereum.github.io/beacon-APIs/#/Beacon/publishBlock)                                                  |
| POST   | [/eth/v1/beacon/blinded\_blocks](https://ethereum.github.io/beacon-APIs/#/Beacon/publishBlindedBlock)                                  |
| GET    | [/eth/v2/beacon/blocks/{block\_id}](https://ethereum.github.io/beacon-APIs/#/Beacon/getBlockV2)                                        |
| GET    | [/eth/v1/beacon/blocks/{block\_id}/root](https://ethereum.github.io/beacon-APIs/#/Beacon/getBlockRoot)                                 |
| GET    | [/eth/v1/beacon/blocks/{block\_id}/attestations](https://ethereum.github.io/beacon-APIs/#/Beacon/getBlockAttestations)                 |
| GET    | [/eth/v1/beacon/pool/attestations](https://ethereum.github.io/beacon-APIs/#/Beacon/getPoolAttestations)                                |
| POST   | [/eth/v1/beacon/pool/attestations](https://ethereum.github.io/beacon-APIs/#/Beacon/submitPoolAttestations)                             |
| GET    | [/eth/v1/beacon/pool/attester\_slashings](https://ethereum.github.io/beacon-APIs/#/Beacon/getPoolAttesterSlashings)                    |
| POST   | [/eth/v1/beacon/pool/attester\_slashings](https://ethereum.github.io/beacon-APIs/#/Beacon/submitPoolAttesterSlashings)                 |
| GET    | [/eth/v1/beacon/pool/proposer\_slashings](https://ethereum.github.io/beacon-APIs/#/Beacon/getPoolProposerSlashings)                    |
| POST   | [/eth/v1/beacon/pool/proposer\_slashings](https://ethereum.github.io/beacon-APIs/#/Beacon/submitPoolProposerSlashings)                 |
| POST   | [/eth/v1/beacon/pool/sync\_committees](https://ethereum.github.io/beacon-APIs/#/Beacon/submitPoolSyncCommitteeSignatures)              |
| GET    | [/eth/v1/beacon/pool/voluntary\_exits](https://ethereum.github.io/beacon-APIs/#/Beacon/getPoolVoluntaryExits)                          |
| POST   | [/eth/v1/beacon/pool/voluntary\_exits](https://ethereum.github.io/beacon-APIs/#/Beacon/submitPoolVoluntaryExit)                        |

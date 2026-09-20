# SL Labs — SL Protocol (Save the Life)

**SL Labs Pte. Ltd.** (Singapore, UEN 202638264E) builds **SL Protocol**, a revenue-first Health-Data DePIN on BNB Chain. AI services across the network are settled in a single utility credit, **$SL**.

| | |
|---|---|
| Website | https://www.savethelife.io |
| Whitepaper | https://www.savethelife.io/whitepaper.pdf |
| Audit report (QuillAudits, Aug 2026) | https://www.savethelife.io/audit-quillaudits.pdf |
| Token & vesting contracts | [save-the-life/SL_TOKEN](https://github.com/save-the-life/SL_TOKEN) |
| X | https://x.com/savethelife_SL |
| Telegram | https://t.me/slfoundation |
| LinkedIn | https://www.linkedin.com/company/slfoundation |

## $SL token — current status

- ERC-20, fixed supply of 2,000,000,000, no mint, no transfer tax, no pause, no blacklist.
- Network: opBNB (BNB Chain Layer-2), with a BSC (BEP-20) representation through the official opBNB bridge.
- Token and vesting contracts were audited by QuillAudits (August 2026, all findings resolved) with Certora formal verification. The audited source is in `SL_TOKEN` and CI checks that the two audited files stay byte-identical to the audited commit.
- **Mainnet deployment has not happened yet.** Only testnet deployments exist (opBNB testnet / BSC testnet). Official contract addresses will be published here and on savethelife.io. Any token presented as $SL before that announcement is not ours.

## Architecture

![SL Protocol system architecture](https://raw.githubusercontent.com/save-the-life/.github/main/profile/architecture.svg)

Solid boxes are live today; dashed boxes are planned from the token launch. The apps, the HealthFi API, the ECG risk-screening model and the veterinary reading pipeline run off-chain. On-chain, the audited `SLToken` and `SLVesting` contracts sit behind a 48-hour timelock owned by a 2-of-3 multisig. Points earned in the apps are non-transferable and are never pegged 1:1 to $SL; conversion runs through a fixed monthly pool with KYC, region checks and a 6-month lock, and tokens are sent from a multisig to the user's own wallet — the servers hold no keys.

## Products

- **HealthFi** — companion app for the SL Watch ECG smartwatch (iOS / Android). The SL Watch is a wellness device, not a medical device; medical-device features will only be offered after regulatory approval.
- **Pet Tooth AI** — veterinary dental X-ray reading assistant, built with technology partner DIGIRAY Co., Ltd.
- **Thor** — ambassador hub for the community.
- **Health Hero** — health mini-app on Toss (Korea).

## Repositories

Public: [`SL_TOKEN`](https://github.com/save-the-life/SL_TOKEN) (contracts, tests, deployment and rehearsal scripts) and [`slhomepage`](https://github.com/save-the-life/slhomepage) (website). Repositories marked *archived* are 2024 prototypes kept for history and do not describe the current project.

## Notice

$SL is a functional access credit for AI services in the SL network. Nothing here is investment advice or an offer of securities. Some features are restricted in certain jurisdictions, including the Republic of Korea and the United States. See the whitepaper for details.

Contact: partners@savethelife.io

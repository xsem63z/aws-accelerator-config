# AWS Landing Zone Accelerator Starter Bundle

This is a minimal starter repo structure for AWS Landing Zone Accelerator (LZA).

## Files included

- `global-config.yaml`
- `organization-config.yaml`
- `accounts-config.yaml`
- `iam-config.yaml`
- `network-config.yaml`
- `security-config.yaml`
- `customizations-config.yaml`

## Before you deploy

Update the placeholder email addresses in `accounts-config.yaml`:

- `management-placeholder@example.com`
- `logarchive-placeholder@example.com`
- `audit-placeholder@example.com`

If needed, change the AWS Region in `global-config.yaml`:

```yaml
homeRegion: us-east-1
enabledRegions:
  - us-east-1
```

## Recommended folder layout

```text
lza-config/
├── accounts-config.yaml
├── customizations-config.yaml
├── global-config.yaml
├── iam-config.yaml
├── network-config.yaml
├── organization-config.yaml
└── security-config.yaml
```

## Suggested first commit

```bash
git init
git add .
git commit -m "Add minimal LZA starter configuration"
```

## Suggested validation step

Run validation from your LZA installer repo:

```bash
npm run validate-config
```

## Notes

- This bundle is intentionally minimal.
- It is designed to help you get the first deployment working with the fewest moving parts.
- Add workload accounts, networking, guardrails, and security services after the baseline deployment succeeds.

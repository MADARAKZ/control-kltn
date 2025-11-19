# Validation Report
_Generated_: 2025-11-19T15:07:53.352084Z

## Static Validation
- **kubeconform** (/tmp/mcp-wlhsvaoe/base/cis_policies_v1.10.0/templates/no-root-containers-template.yaml): PASS
- **kubeconform** (/tmp/mcp-wlhsvaoe/base/cis_policies_v1.10.0/constraints/no-root-containers-constraint.yaml): PASS

## LLM Validation
- Status: PASS
- Score: 95
- Suggestions:
    - The schema could be more descriptive. While functionally correct, it only indicates the presence of `runAsNonRoot` without specifying how the policy uses it. Clarifying that `runAsNonRoot` in the schema refers to the policy requiring `securityContext.runAsNonRoot` to be `true` in the container spec would enhance clarity.
# Validation Report
_Generated_: 2025-11-20T04:02:26.757867Z

## Static Validation
- **kubeconform** (/tmp/mcp-ly1tpbju/base/cis_policies_v1.10.0/templates/no-root-containers-template.yaml): PASS
- **kubeconform** (/tmp/mcp-ly1tpbju/base/cis_policies_v1.10.0/constraints/no-root-containers-constraint.yaml): PASS

## LLM Validation
- Status: PASS
- Score: 95
- Suggestions:
    - The schema contains the definition for `runAsNonRoot`, but the rego doesn't use it, implying that this is an optional parameter and doesn't influence the policy. If the intent is for this value to be utilized within the rego, adjustments should be made accordingly.
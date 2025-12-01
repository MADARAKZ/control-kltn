# Validation Report
_Generated_: 2025-11-18T16:06:50.354787Z

## Static Validation
- **kubeconform** (/tmp/mcp-rdp2jh_7/base/cis_policies_v1.10.0/templates/cis-requiredlabels-template.yaml): PASS
- **kubeconform** (/tmp/mcp-rdp2jh_7/base/cis_policies_v1.10.0/constraints/cis-requiredlabels-constraint.yaml): PASS

## LLM Validation
- Status: PASS
- Score: 95
- Suggestions:
    - Consider adding more detailed descriptions to the schema for each parameter to improve usability.
    - The array_contains function can be replaced with the built-in `contains` function in Rego for simpler and potentially more performant code. It would require minor adjustments to the logic in the 'labelValues' violation rule.
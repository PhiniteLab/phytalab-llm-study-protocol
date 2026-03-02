# Prompt Template — Strict JSON Output

Use this when you want a **machine-checkable** result.  
If the model fails, ask it to rewrite until the output parses as JSON.

---

## Prompt
Return **ONLY** a valid JSON object that matches the schema below.  
Do not include Markdown fences. Do not include commentary outside JSON.

Schema (informal):
{
  "topic": str,
  "assumptions": [str],
  "definitions": [{"term": str, "definition": str}],
  "theorems": [{
    "name": str,
    "statement_latex": str,
    "assumptions": [str],
    "proof_steps": [str],
    "algorithmic_consequences": [str]
  }],
  "key_equations": [{"name": str, "latex": str, "notes": str}],
  "algorithm": {
    "name": str,
    "pseudocode": [str],
    "complexity": str
  },
  "math_to_code": [{"equation_name": str, "implementation_notes": str}],
  "tests": [{"test_name": str, "description": str}],
  "references": [{"type": "book|paper|web", "citation": str, "identifier": str}],
  "uncertainties": [str],
  "verification_plan": [str]
}

Topic: {TOPIC_NAME}

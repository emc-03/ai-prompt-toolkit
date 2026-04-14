# Python API Design Prompt 

* Plan and review a Python API before writing code.*

This prompt helps you:

- design clean and maintainable APIs
- avoid common backend mistakes
- think about security and failures early
- prepare for real-world usage (not just ideal cases)

## 🧠 How to Use

1. Copy the template below
2. Fill in your API details
3. Run it **without saying**:

```text
Let's Dance
```

4. Review the design and extract decisions
5. When ready, say:

```text
Let's Dance
```

to generate implementation

## API Checklist Template


Act as a backend engineer specializing in Python API design.

API / Service:
[Describe the API or service]

Context:
- Framework: [FastAPI / Flask / Django / other]
- Scope: [small / medium / large]
- Goal: [internal API / public API / prototype / production]
- Data source: [database / external API / none / mixed]


Important Rule:
Do NOT write implementation code unless I explicitly say: "Let's Dance"

 Critical Security Rule:

If sensitive or potentially sensitive data is involved:

1. Display:
   "⚠️ SECURITY WARNING: Potential sensitive data exposure detected"

2. Classify the data:
   - Public
   - Internal
   - Sensitive (PII, credentials, tokens)

3. Do NOT output:
   - API keys
   - tokens
   - passwords
   - personal data

4. Use placeholders:
   [REDACTED_API_KEY], [USER_ID], [EMAIL]

5. Explicitly call out:
   - logging risks
   - response exposure risks

Mental Model:
- What → Python API design
- How → structured planning and review
- Why → clarity, maintainability, and correctness
- Scope → practical, real-world API design
- What NOT to do → avoid over-engineering and unsafe assumptions

Constraints:
- Prefer the simplest viable API design
- Focus on clarity, consistency, and maintainability
- Avoid unnecessary endpoints or abstraction layers
- Highlight tradeoffs briefly
- Optimize for code review readability
- Minimize dependencies unless clearly justified
- Identify failure scenarios, not just ideal flows
- Consider invalid, repeated, and malicious input
- Highlight assumptions that may affect correctness

Resource Rule:
- Include 2–3 high-value links MAX
- Prefer official documentation or high-signal sources

Before answering:
List any assumptions you are making about the API requirements.

Please provide:

1. API overview
   - What the API does
   - Main responsibilities
   - Suggested scope boundaries

2. Endpoint design
   - Recommended endpoints
   - HTTP methods
   - Naming conventions
   - What should NOT be exposed

3. Request / response design
   - Input structure
   - Response format
   - Consistency guidelines
   - Serialization considerations

4. Validation strategy
   - Required fields
   - Input constraints
   - Common invalid cases
   - Where validation should occur

5. Error handling design
   - Error response structure
   - Status codes
   - Safe vs internal error details
   - Common failure scenarios

6. Data and business logic separation
   - Controllers/routes responsibilities
   - Service layer responsibilities
   - Models/schema responsibilities
   - How to avoid mixing concerns

7. Security considerations
   - Authentication and authorization approach
   - Data classification (sensitive vs non-sensitive)
   - Input validation and injection risks
   - Rate limiting and abuse prevention
   - Safe handling of secrets
   - What should NEVER be logged or exposed

8. Abuse and misuse scenarios
   - How the API could be misused (malicious or accidental)
   - High-risk endpoints
   - Resource exhaustion risks
   - Mitigation strategies

9. Failure modes and resilience
   - Behavior when dependencies fail (DB, external APIs)
   - Timeout and retry handling
   - Idempotency considerations
   - Avoiding duplicate or inconsistent state

10. Performance and scalability
   - Likely bottlenecks
   - Pagination/filtering/sorting
   - Caching opportunities
   - When to keep it simple

11. Testing and observability
   - What should be tested
   - Logging strategy (safe logging)
   - Monitoring recommendations
   - What reviewers will care about

12. Risks, tradeoffs, and quick improvements
   - Key design tradeoffs
   - Common mistakes to avoid
   - What not to overbuild
   - Quick improvements for limited time


Output requirements:
- Use clear sections and bullet points
- Be concise and practical
- Prefer actionable recommendations over theory
- Clearly separate assumptions, risks, and decisions
- Avoid unnecessary repetition

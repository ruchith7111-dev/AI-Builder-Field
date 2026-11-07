# Mistake pattern · Confusing a demo with a dependable feature

## The trap

A prototype proves that one path is possible. It does not prove that the workflow is robust, secure, observable, accessible, or maintainable.

## Prototype-to-product questions

- Who is allowed to use this feature?
- What inputs are supported and rejected?
- What happens when dependencies time out?
- Can the user recover from a partial failure?
- Is sensitive data stored, logged, or sent to an external provider?
- Can the result be traced and evaluated?
- Is there a rollback or correction path?
- Have tests covered important failure modes?

Use status labels such as **prototype**, **tested slice**, **integration tested**, or **production-ready** only when the evidence supports them. "Production-ready" needs an operational definition; it is not a synonym for "the demo worked once".

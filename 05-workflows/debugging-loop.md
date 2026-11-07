# Workflow · Evidence-led debugging loop

<ol>
<li><strong>Reproduce:</strong> record exact steps, input, environment, and observed output.</li>
<li><strong>Minimise:</strong> reduce the case while preserving the failure.</li>
<li><strong>Locate:</strong> inspect logs, stack traces, data boundaries, and recent changes.</li>
<li><strong>Hypothesise:</strong> write down one or more possible causes.</li>
<li><strong>Discriminate:</strong> choose the smallest test that separates those causes.</li>
<li><strong>Change:</strong> make one focused correction.</li>
<li><strong>Regress:</strong> rerun the reproduction and nearby tests.</li>
<li><strong>Record:</strong> note cause, evidence, fix, and any remaining uncertainty.</li>
</ol>

## Ask AI for investigation, not a random fix

    First, explain the error from the evidence I provide.
    List plausible causes and what would distinguish them.
    Do not modify code yet.
    Suggest one minimal diagnostic step.
    Wait for the result before proposing a fix.

## Avoid

- Changing multiple unrelated things at once.
- Removing validation because it blocks the demo.
- Suppressing an exception without understanding it.
- Calling a bug fixed before the original reproduction passes.

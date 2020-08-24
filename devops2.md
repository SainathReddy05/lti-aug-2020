Continuous Integration:
  Developers to publish their code changes frequently into Central repository. 
  After each code change, code should be BUILT,(Unit/Integration) TESTED, SCANNED for Vulnarabilities & Quality. Once code PASSES all these TEST, then it should be MARKED for RELEASE.

----
Early Feedback !!
==========================================================
Continuous Deployment
-----
Create either "Test" or "Staging" environment which is Identical to production.

Take "RELEASE" artifact from "CI" and Deploy it on Envs
Run all your UAT, Perf, Regre, Load, Stres.....

Once All test Passed, move it in production.

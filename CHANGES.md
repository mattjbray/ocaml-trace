
# 0.3


- add explicit spans, for more precise tracing
- rename repo to ocaml-trace
- trace-tef: add a ticker thread to ensure we flush the file regularly

# 0.2

- trace-tef: additional argument to `with_setup`; env for "stdout"/"stderr"
- refactor: avoid conflicting with stdlib `Trace` module by adding sublibrary `trace.core`.
    Programs that use `compiler-libs.toplevel` should use `trace.core`
    directly, because using `trace` will cause linking errors.
- perf(trace-tef): improve behavior of collector under contention by
    pulling all events at once in the worker

# 0.1

initial release

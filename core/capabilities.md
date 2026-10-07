# Capability contract

Read the [execution contract](contract.md). Capabilities describe desired operations, not permission.

| Capability | Minimum evidence before use | Missing-capability behavior |
|---|---|---|
| source.read | Exact repository/document and granted read access | Report evidence gap |
| source.compare | Exact base/head or versions | Do not claim diff coverage |
| execution.run | Selected permitted environment, scoped command and applicable approval | Deliver analysis; block execution |
| artifacts.write | Approved target, writable scope and preservation plan | Keep a draft in supported task storage |
| delegation | Real worker capacity and lifecycle tools | Work serially if safe |
| history.search | Supported authorized history interface | Use supplied context; do not scan protected files |
| forge.read | Verified repository and PR/commit identity | Report unknown external state |
| forge.publish | Explicit delivery scope and destination | Prepare draft only |
| forge.merge | Explicit merge scope, current checks and verified patch | Do not arm or merge |
| app.control | Authorized environment/browser and safe test surface | Report verification gap |
| schedule | User-requested schedule, scope and destination | Keep disabled proposal |
| webhook | Verified provider, validated payload contract and authenticated routing | Keep static prototype |
| secrets.handoff | Host-supported secure mechanism and necessary authorization | Never request secret in chat |
| worker.isolation | Technical absence of prohibited credentials and tools | Block isolation-dependent delegation |
| external.write | Resolved recipient, bounded content/purpose and approval | Return draft/findings |

The adapter records actual operations and uncertainty. A plugin being listed does not prove its connection, target access or write permission. A successful read does not prove write access.

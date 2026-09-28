# Tempo take-home assessment

## Task 1: Hierarchy filter

My implementation of `Hierarchy.filter()` with additional test cases is on the [`task-1-code`](https://github.com/lukens-private/tempo.io/tree/task-1-code) branch, in [`Hierarchy.kt`](https://github.com/lukens-private/tempo.io/blob/task-1-code/task-1-code/Hierarchy.kt).

The filter makes a single pass over the hierarchy, then builds the output from the kept node indexes, so O(n) time overall. Kept node indexes are tracked in a list, so working memory is O(n) in the worst case. When a node fails the predicate, the following nodes are skipped until the depth returns to that node's level or shallower, and the predicate isn't called for nodes inside an excluded subtree.

The input is assumed to satisfy the invariants documented on `Hierarchy`, and isn't validated.

### Running the tests

```
git clone https://github.com/lukens-private/tempo.io.git
cd tempo.io
git checkout task-1-code
cd task-1-code
./gradlew test
```

## Task 2: Code review

My review of `SimpleCache` is on [PR #1](https://github.com/lukens-private/tempo.io/pull/1), from the [`task-2-code-review`](https://github.com/lukens-private/tempo.io/tree/task-2-code-review) branch. The overall summary is in the review comment, with individual issues and suggestions commented on the relevant lines.

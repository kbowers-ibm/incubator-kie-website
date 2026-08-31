---
slug: kie_10_3_0_sneak_peek
title: A Sneak Peek into the Upcoming Apache KIE (Incubating) 10.3.0 Stream
authors: [bento, bowers]
tags: [apache, 10, kie, release, development]
---

# A Sneak Peek into the Upcoming Apache KIE (Incubating) 10.3.0 Stream

Following the milestone release of Apache KIE (Incubating) 10.2.0, our development community has been hard at work behind the scenes. Today, we are excited to share a sneak peek into the upcoming **Apache KIE (Incubating) 10.3.0** stream! 

This next stream represents a massive leap forward in how KIE is built, maintained, and delivered. Rather than just introducing new features, we have completely overhauled our core repository architecture and release tooling to make the entire ecosystem more agile, reliable, and developer-friendly.

## The Great Repository Consolidation

Historically, the Apache KIE codebase was spread across several independent repositories, including OptaPlanner, Kogito-Runtimes, and Kogito-Apps. While this modularity was useful in our early stages, it introduced significant maintenance overhead, complex cross-repository pull requests, the infamous build-chain, and version alignment challenges during release cycles.

To solve this once and for all, we have successfully completed a major consolidation effort! We have merged the Git histories and codebases of **OptaPlanner, Kogito-Runtimes, and Kogito-Apps** into a single, unified monorepo. 

To match this evolution, our primary repository has been officially renamed to:

👉 **[apache/incubator-kie](https://github.com/apache/incubator-kie)**

In addition, our examples repository has been consolidated and renamed to **`incubator-kie-examples`**.

### What this means for the community:
- **Unified Pull Requests:** You no longer need to coordinate and synchronize multiple PRs across separate repositories for cross-cutting changes. Everything can now be reviewed, tested, and merged in a single pull request.
- **Perfect Dependency Alignment:** Keeping frameworks like Quarkus and Spring Boot perfectly aligned is now automatic, preventing version drift.
- **Smarter CI and Fast Feedback:** We have optimized our CI system to use advanced build-scope computation, which automatically detects what has changed and only builds the necessary modules—giving contributors incredibly fast test feedback.

## Overhauling the Release Experience

In tandem with the repository consolidation, we have completely redesigned our release process. We are introducing a new **local-first release script framework**.

These scripts allow a Release Manager to build, package, and verify the entire KIE suite entirely from their local machine. Whether we are producing an Apache-compliant Release Candidate (RC) or publishing artifacts (such as NPM packages, VS Code extensions, container images, and Helm charts) to public registries, the entire process is now standardized, highly transparent, and fully reproducible. The actual release process will still take place with the use of Jenkins.

## Expect More Reliable and Frequent Releases

All of this structural work has one ultimate goal: **delivering a better, more stable experience to our community.**

By eliminating repository fragmentation and automating our release paths, we are drastically reducing the cycle time required to get updates out to you. Going forward, you can expect:
- **Faster Turnaround on Bug Fixes:** Critical patches can be merged and released without waiting for a lengthy multi-repository pipeline.
- **Predictable Release Cadence:** Releases will become lightweight and routine rather than major, complex orchestrations.
- **Increased Quality & Stability:** Testing the entire module graph together upfront catches integration issues before they ever reach a release candidate.

## Looking Ahead to 10.3.0

We are putting the final touches on our release scripts, running verification tests, and preparing to propose the first 10.3.0 Release Candidate. 

Stay tuned to the dev mailing list and our Zulip channels for upcoming community votes and progress updates. The future of KIE is consolidated, streamlined, and faster than ever and we can't wait for you to experience it!

We welcome your feedback and contributions. Thank you for being part of this growing community and supporting our journey toward a more modern, Apache-compliant future.




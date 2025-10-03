# SWE guidelines

Welcome! This handbook outlines the core principles for collaboration, code quality, and version control in our shared environment.

---

## Write Clean and Thoughtful Code

Our primary goal is to write code that is **maintainable, testable, and efficient**. Your code should be easy for any teammate—and your future self—to understand months down the line.

* **Prioritize Readability:** Use descriptive naming for all variables and functions. Write self-documenting code so that excessive comments are rarely needed.

* **Strive for Efficiency:** Always consider the performance implications of your algorithms, especially in loops or data processing. Use the best tool for the job.

* **Avoid Redundancy (DRY):** If logic is repeated, abstract it into a reusable function or utility.

---

## Respect the Monorepo Structure

We use a **monorepository**—a single repository that houses code for many distinct projects. This requires a **global mindset** and good digital citizenship.

* **Think Like a Neighbor:** Changes to shared packages or core tooling impact every other project. You must think about the stability of the entire repository.

* **No Breaking Changes:** Before changing or deleting shared code, verify that your modifications will not break existing packages. This is the most critical step of your code review.

---

## Enforce the GitFlow Process

We use the **GitFlow** branching strategy to ensure a predictable and stable path to production. Strict adherence to this model is mandatory.

* **Standard Branches:**

    * **`main`**: Always represents the current production code. **Protected from direct commits, only after PR.**

    * **`develop`**: The main integration branch for all new, incoming features. **Protected from direct commits, only after PR.**

* **Feature Development:** All new work starts by branching off of `develop` into a `feature/<description>` branch.

* **Pull Requests (PRs):** Features and releases are merged back into `develop` or `main` only after an approved Pull Request (PR) has confirmed code quality and stability.

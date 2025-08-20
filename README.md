[![Releases](https://img.shields.io/badge/Releases-Download-blue?logo=github&style=for-the-badge)](https://github.com/gitsaurab/LeetCode/releases)

# LeetCode Java Paths: Topic Solutions, Patterns, Progress

![coding-hero](https://images.unsplash.com/photo-1515879218367-8466d910aaa4?auto=format&fit=crop&w=1650&q=80)

A focused, topic-based Java collection of LeetCode solutions. This repo groups problems by pattern and data structure. It contains code examples, short explanations, and a study plan you can follow week by week. Use it to practice interview problems, learn patterns, and track progress.

Releases: Download the release asset (zip or jar) from the Releases page and execute the included file if provided. Visit the Releases page and run the released artifact as described in the release notes:
https://github.com/gitsaurab/LeetCode/releases

Badges
- Language: ![Java](https://img.shields.io/badge/Language-Java-brightgreen)
- Topics: ![Topics](https://img.shields.io/badge/Topics-Algorithms%20|%20Data-Structures-blue)
- License: ![MIT](https://img.shields.io/badge/License-MIT-lightgrey)

Contents
- What this repo contains
- How the repo is organized
- How to run examples and tests
- Study plan and learning flow
- Common patterns and cheat sheet
- Contributing guide
- Contact and license

What this repo contains 🚀
- Topic-based solutions: one folder per topic (arrays, dynamic-programming, trees, graphs).
- Problem implementations in Java with clear method signatures.
- Short explanations and complexity notes in each solution file.
- Unit tests for many solutions using JUnit.
- A set of practice schedules and weekly milestones.
- Example projects with main methods and small runners.
- Study notes and pattern summaries in markdown.

Why follow topic-based learning
- You learn by pattern rather than by chance.
- You reuse the same concept across multiple problems.
- You build intuition for common interview questions.
- You track progress by topic and difficulty.

Repository structure (example)
- /arrays
  - TwoSum.java
  - TwoSumTest.java
  - README.md
- /linked-list
  - ReverseLinkedList.java
  - MergeTwoLists.java
- /dynamic-programming
  - ClimbingStairs.java
  - LongestIncreasingSubsequence.java
- /graphs
  - BFS.java
  - DFS.java
- /utils
  - ListNode.java
  - TreeNode.java
- /notes
  - patterns.md
  - big-o-cheatsheet.md
- pom.xml or build.gradle (if included)
- README.md

Getting started — local setup 🛠️
1. Clone the repo
   - git clone https://github.com/gitsaurab/LeetCode.git
2. Open the project in your IDE
   - IntelliJ IDEA, Eclipse, or VS Code work well.
3. Build the project
   - Maven: mvn clean test
   - Gradle: ./gradlew test
4. Run specific examples
   - Use the main class in an examples folder or run the unit tests.
5. If a release file is provided, download and run it
   - Download the release asset (zip/jar) from the Releases page.
   - If the asset is a jar, run:
     - java -jar LeetCode-examples.jar
   - If the asset is a zip, extract and run the included runner or follow the release notes.

Running single problems
- Each problem class uses a single public method that accepts standard inputs. For example:
  - int[] twoSum(int[] nums, int target)
  - ListNode reverseList(ListNode head)
- Use sample input in the test files or create a small main method to call the methods.

Testing and CI
- The repo includes JUnit tests for many problems.
- Run tests with:
  - mvn test
  - ./gradlew test
- Tests show expected outputs and edge-case coverage for many problems.

Patterns cheat sheet — what to learn first 📘
- Two pointers: sorted arrays, reverse, merge
- Sliding window: subarray sums, maximum subarray
- Fast and slow pointers: cycle detection, linked list mid
- Binary search: search and boundary find
- DFS / BFS: trees and graphs traversal
- Dynamic programming: state definition, memoization vs tabulation
- Greedy: choose locally optimal moves
- Backtracking: permutations, combinations
- Union Find: disjoint sets for connectivity

Sample pattern quick notes
- Two pointers: move pointers based on condition. Use when input is sorted or can be scanned from both ends.
- Sliding window: expand until condition breaks; shrink to restore.
- DFS: use recursion or stack. Track visited nodes.
- DP: define dp[i] as answer for subproblem i. Check transitions and base cases.

Study plan — 8-week example schedule 📅
Week 1: Arrays and Strings — run easy to medium problems. Learn two pointers and sliding window.
Week 2: Linked Lists — reverse, merge, cycle detection.
Week 3: Stacks and Queues — monotonic stacks, sliding window max.
Week 4: Trees — recursion, tree traversals, lowest common ancestor.
Week 5: Hashing and Sets — frequency maps, two-sum family.
Week 6: Dynamic Programming I — fibonacci, climb stairs, knapsack basics.
Week 7: Graphs — BFS, DFS, shortest path basics.
Week 8: Advanced DP & Greedy — patterns across problems and optimization.

Tips for solving problems
- Read the prompt and ask what output you expect for simple inputs.
- Write the brute force solution if you get stuck. Then optimize.
- Identify which pattern fits the problem.
- Write tests for edge cases.
- Keep time complexity in mind. Aim for O(n log n) or O(n) where possible.
- Keep space usage low by reusing input or using constant space when allowed.

Contribution guide — how to add a solution 🤝
1. Fork the repo.
2. Create a branch named feature/topic-problem (e.g., feature/arrays-two-sum).
3. Add your solution in the correct folder.
   - Use the repo utility classes for ListNode and TreeNode.
   - Add a JUnit test covering normal and edge cases.
   - Add a small explanation header in the Java file with time and space complexity.
4. Run all tests.
5. Open a pull request with a clear title and short description:
   - Title: Add [Two Sum] solution in arrays
   - Description: include complexity, pattern, and test summary.
6. Keep commits focused and atomic.

Code style
- Use clear names for variables and methods.
- Keep methods short and focused.
- Add Javadoc for public methods.
- Prefer immutable data when possible.
- Use utility nodes from /utils for consistency.

Example Java snippet
```java
// Two Sum example
public int[] twoSum(int[] nums, int target) {
    Map<Integer, Integer> idx = new HashMap<>();
    for (int i = 0; i < nums.length; i++) {
        int need = target - nums[i];
        if (idx.containsKey(need)) {
            return new int[] { idx.get(need), i };
        }
        idx.put(nums[i], i);
    }
    return new int[] {-1, -1};
}
```

Progress tracking suggestions
- Create a CSV or Markdown table to mark solved problems.
- Track difficulty and date solved.
- Use GitHub issues or projects to mark weekly goals.
- Add tags to PRs to classify topics solved.

Search engine optimization (SEO) tips for this repo
- Use clear problem names and include LeetCode IDs in filenames.
- Keep README headings descriptive.
- Add keywords in repository topics and file front matter:
  - algorithms, data-structures, interview-preparation, java, leetcode, problem-solving

Related resources
- LeetCode patterns by topic (use this repo's notes/patterns page).
- Official Java docs for language specifics.
- JUnit documentation for writing tests.

License and code of conduct
- The repository uses MIT license. See LICENSE file.
- Follow the code of conduct in the repo when you contribute.

Contact and links
- Repository Releases page: https://github.com/gitsaurab/LeetCode/releases
- Use the Releases page to download artifacts. If a release provides an executable file (jar or script), download it and run the included instructions. The Releases page contains notes for each asset.

Screenshots and gallery
![example-solution](https://raw.githubusercontent.com/gitsaurab/LeetCode/main/assets/solutions-screenshot.png)

Common folder tags
- easy, medium, hard
- arrays, strings, dp, graph, tree, linked-list, stack, queue, greedy

Keep practice steady. Open issues for missing problems. Create PRs for improvements. License and contribution guidelines live in the repo.
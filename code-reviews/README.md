# 🧪 Code Review Examples

I put a lot of care into code review. This page highlights a selection of my code review comments and pull request discussions that demonstrate my attention to detail, focus on maintainability, and commitment to improving code quality through constructive feedback. 

These examples reflect how I contribute to projects not just by writing code, but by thoughtfully reviewing and elevating others’ work to ensure clean, reliable, and efficient software.

Feel free to explore the examples and get a sense of how I contribute to high-quality software development.

## General Feedback
1. Discussion around balancing [code organization](https://github.com/department-of-veterans-affairs/vets-website/pull/21061#pullrequestreview-995442273), co-location vs. reuse, and when to generalize for maintainability and clarity. 
1. Noted [potential concern with using array index as a key in React](https://github.com/department-of-veterans-affairs/vets-website/pull/35600#discussion_r2025136962), but acknowledged it as acceptable in this specific static context.
1. Appreciation for a refactor’s clarity and cleanliness, coupled with expressing a [preference for pure functions](https://github.com/department-of-veterans-affairs/vets-website/pull/33428#discussion_r1879294023), while still being open to the current approach.

## Celebrating Great Work
1. Positive reinforcement for [a particularly simple and elegant implementation](https://github.com/department-of-veterans-affairs/vets-website/pull/35359#discussion_r2007753194) of a boolean-returning function.
1. Acknowledging impressive overall work and [excitement about nearing a major functional milestone](https://github.com/department-of-veterans-affairs/vets-website/pull/33234#pullrequestreview-2466030779).
1. Positive feedback [highlighting a clean and effective organizational refactor](https://github.com/department-of-veterans-affairs/content-build/pull/2454#discussion_r1967710132).

## Suggestions for Possible Improvement
1. Consideration of [extracting repeated UI elements into reusable components](https://github.com/department-of-veterans-affairs/vets-website/pull/21642#discussion_r919198716) to improve maintainability, balanced against the risk of overengineering when duplication is minimal and proximity reduces the cost of updates.
1. Suggestion to simplify function component syntax by combining props into a single destructured parameter for [cleaner and more idiomatic code](https://github.com/department-of-veterans-affairs/vets-website/pull/22942#discussion_r1048693725).
1. Naming and testing practice considerations, including the [distinction between stubs and mocks](https://github.com/department-of-veterans-affairs/vets-website/pull/31346#discussion_r1718464002) and choosing terminology that reflects their intended use—particularly when verifying call behavior.
1. Affirmed the correctness of the logic, while suggesting a small optimization to [avoid redundant operations by consolidating related logic into a single place](https://github.com/department-of-veterans-affairs/vets-website/pull/24524#discussion_r1228759458).
1. Identified tight coupling in a component’s implementation and [suggested using inversion of control by passing in behavior as a callback](https://github.com/department-of-veterans-affairs/vets-website/pull/23010#discussion_r1055805843).
1. Raised concerns about [mixed data types causing potential confusion](https://github.com/department-of-veterans-affairs/vets-website/pull/21267#discussion_r890204405) and recommended using consistent default values for clarity and predictability.
1. Noted that setTimeout is unreliable for controlling flow and [recommended using promises or await for more reliable and deterministic asynchronous handling](https://github.com/department-of-veterans-affairs/vets-website/pull/21136#discussion_r879695692).
1. Pointed out that the function mixes responsibilities by both returning data and updating state. Recommended it [focus on a single responsibility](https://github.com/department-of-veterans-affairs/vets-website/pull/21136#discussion_r879700400), such as returning data only.
1. Noted that [a test is too specific and may be brittle](https://github.com/department-of-veterans-affairs/content-build/pull/1532#discussion_r1176817650), suggesting it could be made more flexible to better accommodate content changes.
1. Proposed efficiency improvements, including [replacing substring parsing with a direct object-based lookup](https://github.com/department-of-veterans-affairs/content-build/pull/1487#discussion_r1126411611) for header levels, and [avoiding unnecessary DOM updates](https://github.com/department-of-veterans-affairs/content-build/pull/1487#discussion_r1126427567) by checking if headers are already correctly set before modifying them.

## Required Changes
1. Noted presence of [code that should be changed or clarified to prevent confusion](https://github.com/department-of-veterans-affairs/vets-website/pull/22942#discussion_r1048694209).
1. Identified a [breaking issue where a feature toggle is referenced incorrectly](https://github.com/department-of-veterans-affairs/vets-website/pull/23691#discussion_r1147935086), and recommended using either the correct naming convention or the provided selector to ensure consistency and functionality.
1. Highlighted that implemented [grouping logic uses an incorrect data attribute](https://github.com/department-of-veterans-affairs/content-build/pull/1585#discussion_r1213546694), which may cause inaccurate classification, and recommended explicitly defining group membership to avoid false positives.
1. Called out a [mismatch between a function’s name and its actual behavior](https://github.com/department-of-veterans-affairs/content-build/pull/1409#discussion_r1054817005), noting that it contributed to a broader issue with the code not working as intended. 

## Attention to Detail
1. Pointing out an incorrect variable reference causing [an unintended closure](https://github.com/department-of-veterans-affairs/vets-website/pull/33428#discussion_r1879263820) over an outer variable instead of using the intended passed-in parameter.
1. Noticed [a missing closing >](https://github.com/department-of-veterans-affairs/vets-website/pull/35359#discussion_r2007760220) in a type definition.
1. Noticed a [potentially outdated import path](https://github.com/department-of-veterans-affairs/vets-website/pull/24089#discussion_r1184199381) and suggested a more appropriate shared location.
1. Pointed out an [unnecessary call to Object.keys on a variable that is already an array](https://github.com/department-of-veterans-affairs/vets-website/pull/20790#discussion_r853428399).

## Process & Consistency Recommendations
1. Discussion about [ensuring consistency when removing deprecated features](https://github.com/department-of-veterans-affairs/vets-website/pull/22494#issuecomment-1307761540) across multiple code locations, recommending addressing all related instances together or deferring a complete cleanup to a separate dedicated ticket.
1. Noted the current pattern of importing the module where the widget is mounted and [suggested maintaining consistency with that approach unless there is a strong reason to change](https://github.com/department-of-veterans-affairs/vets-website/pull/20790#discussion_r853387734).

## Strategic Architectural Considerations
1. Questions about [avoiding collisions on user-generated keys](https://github.com/department-of-veterans-affairs/vets-website/pull/34882#discussion_r1973838631) and [managing deduplication](https://github.com/department-of-veterans-affairs/vets-website/pull/34882#discussion_r1973845462), along with some [general discussion on solving the problem within the current architecture](https://github.com/department-of-veterans-affairs/vets-website/pull/34882#pullrequestreview-2648234062).
1. Emphasized that handling invalid API responses is likely the application's responsibility, and that embedding this logic in the template [introduces unnecessary complexity in the wrong layer](https://github.com/department-of-veterans-affairs/content-build/pull/1416#pullrequestreview-1233148208).
1. [Encouraged a significant refactor](https://github.com/department-of-veterans-affairs/content-build/pull/1399#pullrequestreview-1218230040) of code that carries considerable technical debt and is highly prone to subtle bugs and unexpected issues.

## Asking Questions for Understanding
1. Questions to [clarify the purpose and role of certain data structures](https://github.com/department-of-veterans-affairs/vets-website/pull/32019#discussion_r1781282525) and how they fit into the overall testing or development workflow, particularly around temporary configuration and testing strategies.
1. Digging into a key change to understand its necessity by comparing it to the previous behavior and [asking about the rationale](https://github.com/department-of-veterans-affairs/vets-website/pull/33428#discussion_r1879291913) behind its introduction. 

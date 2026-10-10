# Meta coding interview questions: the data structures Meta tells you to study, the questions that keep repeating, and a 6-week prep plan

Most people preparing for Meta start in the wrong place. They open a list of 500 tagged LeetCode problems, work through them alphabetically, and hope volume turns into readiness. Then they bomb a 45-minute screen on a problem they have technically seen before.

The fix starts with reading Meta's own prep notes. For the graduate software engineer pipeline, Meta publishes a selection-process guide that narrows the coding assessment to a much smaller surface than the internet usually admits: four problems of increasing difficulty, 70 minutes, any language you like, delivered through CodeSignal. And then this line, which saves people entire weekends: "We do not ask dynamic programming questions so don't spend time prepping for that technique."

That is not a general rule for every Meta round, and it doesn't cover system design or behavioral. But it tells you something about how the company thinks about coding interviews. They test a specific, repeatable set of skills, and they'd rather you spend your time on those than on the long tail.

## What Meta's coding rounds actually look like

Two different processes get mixed together online, so it helps to separate them.

**The intern and new-grad assessment.** Meta runs two online assessments in the first round: an online coding assessment and a "Preferences @ Work" assessment, done in whichever order you prefer. The coding one is the CodeSignal-based piece. Four problems, increasing difficulty, up to 70 minutes, no pausing once you start. Everything is monitored, and Meta states that submissions go through an integrity review. Consulting ChatGPT, another website, or even an IDE outside the browser is grounds for rejection.

The prep advice in that same document is unusually specific about what to prioritize:

- Algorithmic techniques: iteration, sorting, divide and conquer, recursion
- Data structures: arrays, stacks and queues, hash tables, trees including binary search trees, graphs, heaps
- Prioritize breadth over depth. Solving fewer problems across many types beats mastering one type
- Practice medium and hard problems under a time constraint

**The experienced-hire loop.** Candidate write-ups from recent loops describe the same general shape: a recruiter call, a technical phone screen of about 45 minutes with around two questions, then an onsite loop with two coding rounds, each roughly 45 minutes and each built around two problems of medium to medium-hard difficulty. The phone screen is usually the easier of the two stages; the onsite rounds come with more aggressive follow-ups.

One report from a recent Meta SDE loop put the difficulty split bluntly: phone screen medium, virtual onsite medium-to-hard. The same person noted that the hardest part wasn't the algorithms. It was maintaining clear reasoning while the interviewer kept extending the problem.

## The questions that keep showing up

Nobody can promise you a specific question list. But across candidate write-ups, company-specific guides, and prep platforms, the same families repeat far more often than random chance would suggest.

**Sliding window and string work**

Longest Substring Without Repeating Characters is close to a Meta staple — it shows up in phone screens and gets pushed on time complexity, variable naming, and edge cases rather than the algorithm itself. Alongside it: count palindromic substrings, and longest valid parentheses.

**Intervals**

Merge Intervals appears constantly, and the interesting part is what comes after. One write-up describes the follow-up going straight into streaming interval processing, distributed merges, and memory constraints. Sorting the intervals is the warm-up; the conversation is about what changes when the data doesn't fit.

**Trees and BFS**

Binary Tree Vertical Order Traversal shows up with a column-indexing and ordering-guarantee discussion attached. Buildings With an Ocean View is the same instinct in miniature: a right-to-left scan tracking the maximum so far, O(n), no extra structure needed.

**Graphs**

Course Schedule, solved with topological sort and in-degree counting, is the standard cycle-detection question. Meta-flavored variants tend to arrive as feed or friendship-graph problems, which is where the graph question turns into a product question.

**Heaps and top-K**

Kth Largest Element in an Array and K Closest Points to Origin both belong to the top-K family, and Meta interviewers seem to like them because there are two legitimate approaches with different tradeoffs. Choosing between a heap and quickselect is itself the interview.

**Binary search beyond the basics**

Random Pick with Weight (also called Pick Index) is the modified-binary-search favorite, sometimes with a follow-up asking you to do it in O(1) extra space by mutating the input. First and last position of a target in a sorted array is the classic form and should be automatic.

**Design-flavored data structure questions**

LRU Cache is the one to know cold, including the follow-ups: how you guarantee O(1), what thread safety costs you, and where lock contention bites. Design an in-memory file system with `create`, `get`, and `list` is the other recurring shape, and it almost always escalates into trie-versus-hashmap tradeoffs and what happens at millions of paths.

**O(1)-space twists**

A recurring Meta pattern: take a question you can already solve and ask for an O(1) extra space version. Evaluating an arithmetic expression with no parentheses in constant extra space is the clearest example, and it exposes whether you actually understand the two-pass structure or just memorized it.

One thing tying these together: Meta questions often have a real-world texture. A guide written by interview coaches describes the style as "given a feed of events, compute the top K most active users in the last hour" — a streaming-plus-data-structures problem dressed up as a product question. The algorithm is familiar. The framing is not.

## The follow-ups are the real screening layer

Read enough recent interview reports and a pattern emerges that has little to do with problem selection.

The initial solution is rarely what eliminates candidates. The extensions are. Interviewers ask how the approach changes if the input is streamed rather than loaded into memory. They ask what happens to your complexity after the last optimization. They ask about concurrency, about cold-start problems in a recommendation system, about avoiding popularity bias when ranking mutual friends.

That's a different skill from pattern recall. Pattern recall gets you to the right approach quickly, which matters because spending 15 of your 45 minutes on approaches that don't fit is the most common way prepared candidates still fail. But the follow-up conversation needs you to reason about tradeoffs out loud, with someone probing your reasoning the whole way.

Meta also cares about code quality in a way that surprises people who only practice for correctness. Clean naming, readable structure, and deliberate edge-case handling are part of the score. A candidate report from a recent loop sums it up: Meta is less interested in memorized answers and more interested in how you think, communicate, and reason in real time.

## Why pattern training maps well onto Meta specifically

Put the official details next to the recurring question list and a mismatch becomes obvious.

Meta's coding assessment explicitly excludes dynamic programming and focuses on a handful of data structures. The onsite coding rounds draw repeatedly from a small number of families: sliding window, intervals, trees and BFS, graphs, heaps, binary search, and design-flavored structure questions. That's a narrow tested surface spread across thousands of available practice problems.

Grinding 400 random problems is a volume strategy applied to a pattern-shaped test. Learning the ~48 core patterns — the number AlgoMonster builds its curriculum around — and then practicing recognition under time pressure is a different bet, and for Meta's format it's the better-fitting one.

## Where AlgoMonster fits into a Meta prep plan

AlgoMonster is a coding-interview course built by ex-Google engineers and competitive programmers, organized around patterns rather than a flat problem list. For Meta prep, the parts that matter most:

- **Pattern flowcharts.** A dedicated section maps keywords in a problem statement to the algorithm family it implies. That's directly useful for the "which approach is this?" moment that eats interview minutes.
- **Templates in six languages.** Every pattern comes with template code you can adapt, which pairs well with Meta's tolerance for any language.
- **Speedrun mode.** Timed drills, unlimited on Pro plans. Timed practice is the part most self-directed prep skips, and it's the part Meta's 70-minute assessment actually measures.
- **AI woven through the content.** Hints when you're stuck, code debugging on submission, plain-language explanations of any section.
- **Company question sets updated monthly.** Meta appears in the question banks alongside Google and Amazon.

A note on the numbers, since they get quoted loosely. AlgoMonster's own pricing page advertises 500+ lessons across six courses, 1,000+ illustrations, and 3,000+ editorials. Third-party reviews consistently describe 48 patterns and 231 practice problems. Those aren't contradictory — lessons and editorials aren't the same thing as practice problems — but it does mean the problem volume is smaller than a platform like LeetCode, and that's the tradeoff you're accepting.

### What AlgoMonster doesn't cover

Worth knowing before you buy, because these gaps are predictable:

- **System design.** There's introductory material, but not enough for L5-and-above Meta loops where a dedicated design round is standard. Budget separate time and resources for that.
- **Behavioral prep.** Some content exists, but Meta's behavioral rounds reward real STAR-format preparation about conflict, impact, and learning fast. This platform isn't built for that.
- **Live interview pressure.** Every problem is solved at your own pace with no one watching. AlgoMonster builds the knowledge; it doesn't simulate the room. Practicing with a human, or at minimum narrating your reasoning out loud while recording yourself, closes that gap.
- **Video.** There is none. Everything is text and interactive diagrams. Readers love it, video learners won't.

If your gap is pattern selection speed and you already write correct code in one language, the fit is good. If you're learning what a hash map is, start elsewhere. If you've mastered the patterns and just want raw volume, LeetCode is the cheaper tool for that specific job.

## AlgoMonster pricing: every plan currently on the page

AlgoMonster has no monthly option. The choice is between the free tier, annual access, and a one-time lifetime purchase.

| Plan | What you get | Price | Billing cycle | Get it |
| --- | --- | --- | --- | --- |
| Free | Limited access to sample patterns and problems | $0 | None | [Explore the free tier](https://algo.monster?fpr=li69) |
| Pro – Yearly | All patterns, lessons and problems unlocked; unlimited AI assistant; unlimited Speedrun; real questions from top tech companies updated monthly; 500+ lessons across 6 courses, 1,000+ illustrations, 3,000+ editorials; member discount on live bootcamps | $99/year (listed as $8.25/mo billed annually) | 12 months of full access, cancel or upgrade anytime | [See the yearly plan](https://algo.monster?fpr=li69) |
| Pro – Lifetime | Everything in the annual plan plus lifetime updates | $189 | One-time payment | [See the lifetime plan](https://algo.monster?fpr=li69) |

Both paid plans include bonus courses at no extra cost: a Foundation Course covering data structures and algorithms from the ground up, and a "Build an LLM" course that goes past API usage into tokenization, attention, and training. Some specialized courses developed with external partners, like Quant Interview Prep, are sold separately.

Two honest caveats about those figures.

First, AlgoMonster runs sales frequently, and third-party trackers publish wildly different numbers — you'll see $459 lifetime, $299 per year, and $69.99 per year cited across review sites, some of it stale or inaccurate. Check the checkout page for what's actually applied rather than trusting any review, including this one.

Second, for a Meta loop you're targeting in the next two to three months, the yearly plan is the straightforward choice. The lifetime option makes more sense if you expect to interview again in a couple of years, which for engineers chasing promotions or external offers is common enough to be the default assumption.

## A six-week prep plan built around Meta's rounds

This assumes you can write correct code in one language and can give up 1–2 hours a day.

**Weeks 1–2: the tested surface.** Work the pattern curriculum in the order Meta's own guide implies: arrays, hash tables, stacks and queues, then two pointers and sliding window. Do every problem twice — once untimed to learn it, once at 45 minutes with a timer running. Skip dynamic programming for now.

**Week 3: trees and graphs.** Binary tree traversals, BFS with column or level indexing, then graph traversal, cycle detection, and topological sort. Course Schedule and Binary Tree Vertical Order Traversal belong in this week because they cover the two shapes Meta returns to most.

**Weeks 4: heaps, binary search, and design questions.** Top-K with a heap, quickselect, binary search on a transformed array, then LRU Cache and the in-memory file system. Implement LRU twice: once with a dictionary and a doubly linked list, once explaining out loud why each operation is O(1).

**Week 5: weak spots and O(1)-space variants.** Go back through everything you got wrong and also practice the "now do it with constant extra space" version of problems you already solved. This is where Meta's follow-up style gets rehearsed.

**Week 6: simulation and communication.** Do full 45-minute mock rounds with two problems each, narrating your reasoning the entire time, including the parts where you're unsure. Record at least one and listen back. Fumbling for words while you code is a fixable problem, and it only surfaces under a timer.

Keep backtracking and recursion in the plan even though the assessment skips dynamic programming — reported onsite questions do touch recursion-heavy territory, and the assessment rules only apply to the assessment.

## Quick answers to the questions people actually ask

**Does Meta ask dynamic programming?** Not in the graduate coding assessment. Meta's own prep page says so directly and tells candidates to spend their time elsewhere. Onsite coding rounds for experienced hires are a different story, so don't delete the topic from your brain entirely.

**Which language should I use?** Candidate reports commonly list Java, Python, C++, JavaScript, and Go as accepted, with Python and Java most common. The practical rule is to use your strongest language and confirm with your recruiter. Writing production-quality code matters more than the choice itself.

**How many problems should I solve?** Fewer than you think, done better than you'd like. Meta's own advice is breadth across problem types rather than depth in one. If you're using AlgoMonster, its 231 mapped problems are the intended amount; if you're supplementing with LeetCode, add volume from the same families rather than random tags.

**Is the free tier enough to prepare?** No. It's enough to decide whether the text-and-diagram teaching style works for you before you pay, which is its actual purpose.

**Yearly or lifetime?** Yearly if you have an interview date within a few months. Lifetime if you expect to do this again.

**Is one platform enough for the whole Meta loop?** No, and it's worth being clear-eyed about it. Coding prep covers the coding rounds. Meta's onsite for experienced hires usually includes system design and behavioral rounds, and neither is a strength of a pattern-based coding course. Plan your stack accordingly: a coding platform for the coding rounds, something dedicated for design, and real practice talking about your impact for behavioral.

<blockquote>
If your bottleneck is recognizing which pattern a problem needs within the first five minutes, that's the gap AlgoMonster was built to close, and the yearly plan at $99 covers a typical Meta prep timeline. 👉 <a href="https://algo.monster?fpr=li69">Start with AlgoMonster's current plans</a>.
</blockquote>

# Reviewing Code with Intent

Code reviews are a common (and important) part of the software development process, however, all to often they can be overlooked as a simple "+1" formality.  On the other end of the spectrum, for "important" code reviews, there can be a perception that the only review of value is that of the person most knowledgeable of that piece of code.  While technical expertise is certainly important when it comes to peer code review, there are muliple angles from which to approach a review - all of which can bring value.  While it is certainly possible for one person to cover all perspectives, more often than not, it can be helpful to have multiple reviewers, each who can (and do _intentionally_) check one or more boxes for thorough review coverage.

In this post, I'd like to explore a few of the perspectives from which to approach a review and how they can combine for the optimal outcome.

### Review as a functional expert

As mentioned above, one of the most important roles in any code review is that of functional expert.  This reviewer should not only be familiar with the code in question, but the larger system into which the code fits.  This person should be able to think through the changes being made, and look for any un-intended, or un-considered negative effects on the rest of the system.

### Review as a language expert

Another important role is that of language expert.  While the functional expert focuses more on high-level design and system impact beyond the code in question, the language expert focuses more on the specific language features and constructs being used to implement the logic.  This may include simplifying logic, common language 'gotchas', suggestions of new/alternate features, or any other suggestion to make a given module or function as usable and performant as possible.

### Review for API passivity

Another review intent that might less obvious, but is no less valuable is that of reviewing for API passivity.  Reviewing for API passivity is a way of considering _potential_ impact to the larger system (specifically consumers of the module) without actually having to know the system itself.  Even though they might not know with certainty that changes _will_ impact consumers negatively, by flagging changes that _may_ impact consumers, this reviewer can start the conversation that the code author can then track down to ensure they aren't.

### Review to learn

While the first couple of items on this list focus on perspectives that benefit the code in question, performing code reviews is also a highly underrated way of _learning_.  One of the most valuable skills that an engineer can possess is the ability to dive into unfamiliar code, read it, synthesize it, and make sense of it.  And what better way to get experience at reading code than to jump on code reviews.  At the very least, you can gain repetition and practice at reading unfamiliar code, at best, you might uncover an issue!  But either way, making time to review code is a very low cost way to flex the muscle memory of 'translating' unfamiliar code and building a valueable skill.

But regardless of which perspective (or perspectives) you choose to review from, always approach a review with **_intent_**.

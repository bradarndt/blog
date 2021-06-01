# Reviewing Code with Intent

Code reviews are a common (and important) part of the software development process, however, all to often they can be overlooked as a simple "+1" formality.  On the other end of the spectrum, for "important" code reviews, there can be a perception that the only review of value is that of the person most knowledgeable of that piece of code.  While technical expertise is certainly important when it comes to peer code review, there are muliple angle from which to approach a review - all of which can bring value.  While it is certainly possible for one person to cover all perspectives, more often than not, it can be helpful to have multiple reviewers, each who can (and do _intentionally_) check one or more boxes for thorough review coverage.

In this post, I'd like to explore a few of the perspectives from which to approach a review and how they can combine for the optimal outcome.

### Review as a functional expert

As mentioned above, one of the most important roles in any code review is that of functional expert.  This reviewer should not only be familiar with the code in question, but the larger system into which the code fits.  This person should be able to think through the changes being made, and look for any un-intended, or un-considered negative effects on the rest of the system.

### Review as a language expert

Another important role is that of language expert.  While the functional expert focuses more on high-level design and system impact beyond the code in question, the language expert focuses more on the specific language features, constructs, and features being used to implement the logic.  This may include simplifying logic, common language 'gotchas', suggestions of new/alternate features, or any other suggestion to make a given module or function as usable and performant as possible.

### Review for API passivity

Another review intent that might less common, but is no less valuable is that of reviewing for API passivity.  Reviewing for API passivity is a way of considering _potential_ impact to the larger system (specifically consumers of the module) without actually having to know the system itself.  Even though they might not know with certainty that changes _will_ impact consumers negatively, by flagging changes that _may_ impact consumers, this reviewer can start the conversation that the code author can then track down to ensure they aren't.

### Review to learn

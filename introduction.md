Before jumping right into the content, I thought it might be helpful to provide some quick context on how I approach problems, which will in turn help inform as to the level of detail and approach to many of the topics on this blog.

I believe that one of the most beneficial things that an engineer can do is to gain a firm understanding of concepts and primitives, and become adept at _applying_ those primitives to solve problems.  If you memorize one solution, you know one solution.  But if you know how to _**get to**_ the solution, you are able to solve a wide array of problems.  Because I believe this is an important aspect of Engineering, most of the topics on this site will have a similar level of granularity.  Will you find a deep dive into the python requests library?  No.  But might I discuss higher-level concepts like network latency and how to account for it in system design (agnostic of specific technology or language)?  Absolutely!

To further illustrate this point with a little different angle, let's consider a problem I worked through today:

**What is a simple algorithm to determine whether two intervals [a1, a2] and [b1, b2] intersect?**

The solution to that _**specific**_ problem is well known (and can easily be found via [a quick google search](https://www.google.com/search?q=how+to+determine+if+two+intervals+overlap) leading to [stack overflow](https://stackoverflow.com/questions/3269434/whats-the-most-efficient-way-to-test-two-integer-ranges-for-overlap)).

But what if the question you need to answer has variation?  What if your range is not a simple end-inclusive range, but instead, the endpoint is exclusive and can optionally be null to indicate an un-ending upper bound?  Googling for a specific canned solution is not so easy now!  So instead, let's start with the primitives and apply them.

So what do we know?

1. From the above post, we know that two end-inclusive intervals DO NOT intersect if and only if the first ends before the second begins `a2 < b1 or` vice versa `b2 < a1`
2. We know some basic boolean algebra
    1. `NOT(a AND b) <==> NOT(a) OR NOT(B)`

So let's apply!

First we'll start with our original premise:
Two end-inclusive intervals intersece if and only if the first ends before the second begins `a2 < b1 or` vice versa `b2 < a1`

Then let's modify it to handle end-exclusive ranges.
Now that the ends are exclusive, two intervals no longer overlap when the begin of one is exactly equal to the end of the other.  This means that we need to exclude the cases where `a2 == b1` and `b2 == a1`

And finally one last thing that might be helpful to explicitly call out is that while the thoughts and ideas expressed on this site are my own, they are by no means novel and are very common in industry.  And because of that, I will not attempt to present an exhaustive analysis of every thought, and fully acknowledge that a good google search will turn up more in depth reading on many of the topics.  Enjoy!

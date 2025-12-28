# How do HTTP Servers get overloaded?!

### Entry #1: The Late Night Realization

**_December 28, 2025_**


It was late in the evening. My friend and I just started a few days of holiday—school was out for us both, and he was finally off-work for Christmas. We were small-talking about how I’d decided to spend my break switching to Arch (BTW ;)), while he was mostly just trying to rehabilitate from the whole year's work. He honestly didn’t want anything to do with computers, until he mentioned he’d been looking into some resources on Load Testing.

We went down the rabbit hole. I told him how I’ve developed a habit of load testing simultaneously with development, using closures (basically HOFs) as decorators. I use them to wrap whatever module I’m working on to get insights into execution time and memory usage—heap allocations, stack usage, and the like—optimizing as I go.

He told me that’s a good start, but it isn't enough. He argued that true Load Testing is a prerequisite for enterprise-level applications; you have to test things from a broader perspective, like how server behavior corresponds to traffic activity, spikes, and spike duration. That is where standardized benchmarking tools and methods really come into play.

He kept explaining, and for the next three days, I couldn’t stop thinking: How do servers actually get overloaded? I mean on a really deep level. Are requests just queued up until a classic overflow happens? Or is it about asynchronous and concurrent processes causing CPU hangs?

I’ve carried those thoughts for three days, and here I am. It's December 28th, and I’m embarking on a journey to build an HTTP server from scratch and stress-test it myself. I want to find out exactly how a server breaks.

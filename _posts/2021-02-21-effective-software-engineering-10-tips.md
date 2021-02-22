---
layout: post
title:  "Effective Software Engineering"
---
For a prettier viersion, please see the article [Effective Software Engineering](https://fayvor.medium.com/effective-software-engineering-10-tips-to-take-to-your-next-job-58ed3a126618) on Medium.

Programming is a powerful skill, and I’ve been using it for the past 2 decades to make a living, pursue scientific interests and try and have a positive impact in the world. I’ve had a lot of fun, made friends, and helped some companies do things they might not have done without my involvement. I’ve also made many mistakes along the way, wasted plenty of time, struggled and injured myself on more than a few sharp edges. Below are a few of the lessons I’ve learned about how to apply my software engineering skills effectively and to a positive end. I hope new engineers just getting into the field, and even more experienced ones, will take something from this list.
Keep in mind: this is what has worked for me, and your mileage may vary. My experience is largely with small startup engineering teams of 10 people or fewer. You may find a different combination of techniques works better for you, given your interests, aptitudes and environment. Please let me know in the comments if anything in this article is helpful to you.


### 1. Know your customer.

Whether your customer is internal or external, you are always developing software, directly or indirectly, to serve a person. What you know about that person’s needs and wants can guide the decisions you are empowered to make. For an external customer, you will often not have direct access to them, in which case, learn about them through the product and customer success teams. If your customer is internal, make direct contact with them if you can. Perform the product function of gathering user feedback if nobody is doing that for you.
   

### 2. Ship Early and Often.

When I went scuba diving in the Caribbean, I learned a saying: “Equalize early and often.” This refers to equalizing the pressure in your inner ear as you dive or ascend, before it builds up to the point where equalization becomes difficult and the pressure damaging. Most senior software engineers I’ve worked with know the value of shipping, and are always looking for opportunities to ship what they’ve built. Especially those engineers who have taken contract work. In some environments this might mean getting feature acceptance and merging into the main branch; in other cases, this might mean deploying to production. Getting your code working is one thing. Getting it merged and into production is another. It takes time and care to tidy up your code, document, go through code review, get sign-off from product, resolve conflicts, merge, and deploy. It might seem like excessive overhead for a small feature, and you may feel the desire to bundle more work together, or optimize a bit more, before delivering your work. But shipping early and often is essential to shortening the feedback loop with customers, which is a key part of agile software development. You will also find it is gratifying the product and business teams to see a steady stream of features getting released.

### 3. Set Daily Targets.

In preparing for battle I have always found that plans are useless, but planning is indispensable. — Dwight D. Eisenhower
I always introduce a daily standup to teams at companies where I work that don’t already have one. I see the act of recapitulating yesterday’s accomplishments, and projecting today’s, as reflective practice and an exercise in mindfulness. It orients me at a place and time, and pushes me to break my work up into activities that can fit into a day and be summarized and communicated at that scale. For an individual contributor, this parallels the work that is done at the product and project management level to break up larger product development arcs into smaller ones and apportion the work in chunks that fit into a 2-week sprint. I find it is best to keep a work log of these daily targets, and add notes to that log throughout the day.

### 4. Develop with Tests.

When I discovered test-driven development, everything became clear. I practice a form of TDD where I set up the object model and interfaces in the code and then write tests for them. As the code develops, whenever I add a new function or an object, in most cases I will write tests for it before the implementation. I like to test the natural interfaces in the code rather than using mocking to patch behaviors and values deep within the code I’m testing. This way, the tests serve as examples of how the functions and objects are to be used. They support the development effort, as well as debugging and maintenance. And they will create robust defenses around your code, giving you the confidence that it will perform as expected in production, even as the code around it is refactored.

### 5. Shorten the Feedback Loop

It seems to me that the primary meta-activity of writing software is to shorten the iterations in the development cycle. As I program, I am always asking: how can I get the answer I’m looking for as quickly as possible? Is it worthwhile to invest in additional scaffolding to reduce the iteration time? This is especially true for debugging, where reproducing a failure can sometimes take hours or days. But it is also true for development, which in many projects can be described as search in solution space. The feedback loop also includes your product manager and, by extension, the customer. If you discover something during development that wasn’t anticipated during design, for better or worse, it is almost always worth propagating upstream. Best if you have a product manager who is adaptable and can modify requirements to take advantage of emergent opportunities or re-route around roadblocks.

### 6. Keep it simple.

At the beginning of a large project, you may have a green field. Lots of choices about technology and design. You have an opportunity to try new things. Use a mix of new and proven technologies. Over-engineering is ok, as long as you save time for reduction. Much of the work should go into simplifying the design. Of poetry, from the poem Adam’s Curse by William Butler Yeats:
“A line will take us hours maybe; Yet if it does not seem a moment’s thought, Our stitching and unstitching has been naught.”
Software architecture is like poetry in this sense. The design principles should be simple to diagram and simple to grasp. There should be a symmetry that holds from the larger system to its components. If it’s not simple and elegant, rework it until it is. I find that drawing pictures helps to get it right, and to document design decisions.
You might think yourself very clever, having applied a new coding pattern or algebraic principle you just learned. It may have taken you days or weeks to get everything lined up just right in your head, and it all works out. But if, in 6 months’ time, you can’t find your way back to the precise state of mind that gave birth to your mini-magnum opus, it will be useless to you and others that have to extend and maintain it. Be kind to yourself and to them, and keep it simple.

### 7. Draw pictures.

Communicate and document your architecture through diagrams. Display a key for shapes, arrows, and colors, and let all objects of a kind or color mean the same thing in your diagram. Pictures can be powerful engineering tools when used in this way. They can help you reason about a system and record decisions you’ve made. In discussions with other engineers, a picture can serve as a common point of reference. When demonstrating backend work that you’ve accomplished, architectural diagrams can show how the system has simplified or allowed for horizontal scaling. Use ERDs for database and software design; Data Flow diagrams to show processing pipelines; Sequence or Messaging diagrams for communication sequences between components; Component diagrams to show how a system is broken up into smaller subsystems; Critical Path diagrams to examine project dependencies. Pictures complement words so that everyone can form a fuller understanding of the work being done, and the results they can expect. I always try to represent the people in the system somewhere on the diagram, and relate things back to the customer.

### 8. Stay Healthy

Take care of yourself. I know it’s tempting to stay up late, drink energy drinks, and bang out that feature that was mentioned in the company meeting overnight to impress everyone. Ok, go for it, but don’t back yourself into a corner by setting unhealthy expectations. You can burn yourself out this way. Your company needs you to produce work consistently and sustainably, not erratically.

Take breaks. Use a standing desk. Stretch. Run in the mornings. Walk in the evenings. Get outdoors and play on the weekends. Whatever kind of physical activity works for you. Eat well. Learn to cook. Avoid a long string of pizza and beer meetups and 24-hour hackathons. Have a regular sleep cycle. You will probably be surprised to find how much you can get done by keeping your schedule free during your high-throughput hours and applying them in a focused way, undistracted. You can build up incredible momentum with a healthy rhythm.

### 9. Go for Coffee, Go for Lunch

Engineering well-functioning software systems is a team effort, and team culture is everyone’s responsibility. The best teams I’ve been on, and the most fun I’ve had, is at companies where people share some of their break time with colleagues. Not at the bar, but over coffee and lunch. Talk shop, talk sports, talk video games, talk politics, whatever. At a company where people care about the mission, socializing is a great way to reinforce the great feeling that the team is doing something impactful and good for the world.

### 10. Have a Purpose

As a software engineer, you have a very powerful skillset. And with great power comes great responsibility. You will not have control over every step in your career. You may feel the need to take a job to maximize your earnings or acquire essential skills or experience. But with a little extra effort you can give yourself the option to contribute your skillset to something more significant and lasting than mobile games or ad-targeting.

The best minds of my generation are thinking about how to make people click ads. 
— Jeff Hammerbacher, Cloudera founder and ex-Facebook employee.

There are some great socially and environmentally responsible companies out there, with clear missions and values, looking to make a real difference in the quality of people’s lives. They know they have to have a viable business to have an impact, and one factor in that is to hire people who are both talented and passionate about their mission. You are one of those people.
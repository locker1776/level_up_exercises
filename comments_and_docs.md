## Thoughts on comments and documenting
#### Why do we say "comment lie?"
Every single software shop I have worked for, always has the Developers fighting for good code quality, and no other parts of the business. I have never heard project manager say: "Why don't you take a few more days to make sure everything is good with what you have done. I can wait on the other stuff." This is the environment in which we work.

In such and environment, we feel like we are always pushed to deliver as much as possible in the least amount of time. This goes doubly for fixes to problem software. Which leads us to lying comments.  You or someone else writes a comment. But then you find a bug at the last second, so you need to change the method. But you don't want to or just forget to change the comment to include how the method has changed. Rinse and repeat 300 more times, and eventually every comment in the system lies about the methods or APIs they talk about.

If the documentation is not a deliverable that the project management or other engineers find valuable, it always gets left behind, and starts lying.
#### Explaining code without comments
The best way to explain code to others is for the code to talk for itself. If you use descriptive variable and method names, keep methods small, manage your dependencies, and have a logical flow to your design, the code itself should explain what it is doing. This is the ideal behind self-documenting code. And the beauty of it is that good design, good development practices, all lead you to self documenting code automatically.

It can also be very helpful to provide documentation about the interface (human or machine) that provides how the use and run the program that you have spend so much time creating. Of course this is for only one aspect of the system, and not at the unit level.

Finally, tests should be able to describe the functionality of the methods, and should let you know all the things that the developers who came before you thought were important enough to write a test to make sure that certain behaviors were included in the application. If you are not sure what a method should do, the tests should shine a light on your cloud of confusion.

*For my thoughts on self documenting code, see the 1st paragraph under Explaining code without comments.*

#### When you should add comments to your code  
There are certain times were a quick comment to your code can be valuable, and is small/short enough to where it won't go out of date.

1. Whenever I need to use some type of advanced math function, I like to include a link or an explanation about where the math function came from, otherwise that portion of the code will not be understandable. An example would be the equation to find an angle of a triangle given the sides of the triangle.
2. Another time I like to include comments, is when I am patching some type of error or problem in the stack. Many times the fixes to these are blocks of dense unreadable code, or creating lines of code that make no sense without that context. Then developers know they can get rid of the awfulness of that code when they upgrade to the version that fixes the problem.
3. Some teams like to keep track of TO-DOs in the code base to identify places of technical debt. This is one type of comment that developers are happy to delete when they can remove the offending pieces of code. So you don't have the problems with the comments not staying up to date. And being able to aggregate the TO-DOs through is a good way to understand the health of your application and the team working on it.

---
layout: post
title:  "Sim-U-Duck Project"
categories: project
---
# About

The purpose of this project is to get you acclimated to using the Eclipse IDE, the Java programming language, and Git version control using our GitLab server.

# Prerequisites

* Download and install [Java SE 8 Update 60](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
* Download and install the Eclipse IDE for Java Developers, or the Eclipse IDE for Java EE Developers from [eclipse.org](http://www.eclipse.org/downloads/)
* Log in to our [GitLab server](http://gitlab.camp.clarkson.edu)
* Follow the instructions I posted last week to [create your ee363-fall-2015 project](http://ee363f15.fanel.li/gitlab/2015/09/03/GitLab.html)

# Project Description

You must read the SimUDuck chapter of Head First Design Patterns, and implement the SimUDuck application several iterations. Each iteration must be committed to your Git repository individually. When I grade the project, I'll be looking for each specific iteration of development.

You may make as many commits as you like, at any intervals you like. The only requirement is that you MUST also commit after you complete each iteration, and "tag" that commit in GitLab (I'll show you how in a moment...)

## Iterations

### Iteration 1: Create the project
In iteration 1, you must complete several tasks:

* Create a new Java project. You may call the project anything you like, but "SimUDuck" is a pretty good choice. Remember to avoid using names like "Project1" because they're not descriptive.
* Share your project. Remember to add the project to the index, and commit it! This is covered in the Getting Started with GitLab guide linked in the Prerequisites.
* Implement the design shown on Page 2: "It started with a simple SimUDuck app".

At the end of the iteration, be sure to add your project to the index, and commit it again. Every time a file is created or modified, it must be added to the index; otherwise, Git will ignore the file or the changes made to it!

### Push Your Changes Upstream
If you haven't already done so, push your changes upstream. Remember that you can make as many commits as your like before you push. Each commit will be sent upstream.

### Tag your iteration
Now that you've made commits and pushed upstream, you can create tags. A tag is simply a lotical name that we put on a project at a specific commit. Since Git uses hashcodes to name each commit, tags give us a simple way to put a meaningful name on the project at a specific point in time.

To tag your project, log into [https://gitlab.camp.clarkson.edu] and go to your ee363-fall-2015 project. On the project page, you'll see blue buttons to "Star", "Fork" or "Download" the project, and then a blue "+" button.

Click the "+" button and choose "New tag".

Enter the following values:

* Name: iteration1
* Create from: master

Then, click "Create tag". You'll be taken to the "tags" page where you can see all the tags in your project. After you tag a couple more iterations, you should spend some time browsing through and observing your project in its various states.

### Iteration 2
In iteration 2, we need the ducks to fly. Continue with the implementation through page 4: "But something went horribly wrong".

In this iteration, you must also define a JUnit test case. Your test class should have a single method, which does the following:

{% highlight java %}
public class FlyingDuckTester {
  @Test
  public void testRubberDuck() {
    Duck duck = new RubberDuck();
    duck.fly();

    if ( duck.isFlying() )
      fail( "Rubber ducks can't fly!!" );
  }
}
{% endhighlight %}

Note that you'll need to take some liberties in your implementation -- add the isFlying method, and make sure it returns the correct state after "fly" is called. You might also add a "land" method.

To finish this iteration:
* Run your unit tests and make sure it fails ... our requirement is that rubber ducks can't fly, and at this phase, our rubber duck is coded to fly.
* Add your project to the index, commit it, and push it upstream
* Create a new tag called "iteration2" using the same instructions as above.

### Iteration 3
Implement the design change shown on page 6: "How about an interface?". Then commit and push your project, and create a new tag called "iteration3".

### Iteration 4
Read through page 14, and implement the Duck Behaviors shown on page 13. Just implement the behaviors, we won't change the Duck classes until iteration 5.

Commit and push, and tag it using the name: "duck behaviors"

### Iteration 5
Integrate your Duck Behaviors into the Ducks, as shown on pages 15 through 22.

Commit, push, and tag it as "strategy pattern"

# Grading Notes
This assignment will be aggregated into your cumulative "Project 1" score. I'm primarily looking to see that you:

* Adopt Java naming conventions and styles
* Learn to use and integrate with Git
* Can adjust to the Java programming language and Eclipse IDE.

# Office Hours
My regular office hours are M/W/F from 12-1:45P in CAMP 143. However, I'm available virtually any time this week. Feel free to swing by my office, or shoot me an email, or ping me on Google Hangouts at: tfanelli@clarkson.edu

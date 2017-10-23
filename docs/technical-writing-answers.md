# Intro
The following document was created by :octocat: Jenn Leaver (@jleaver) and :octocat: Matt Desmond (@beardofedu) based on [questions asked](https://github.com/campus-experts/fall-2016/issues/32) by some of the members Campus Experts program.  

- Fall 2016: Video Link: https://vimeo.com/192706314/ee4a9e52ab
- Spring 20117 Video: 

## Questions

@gillchristian

#### Best practices for writing, not only how the article/post/whatever should look like but also about the process of writing it?

Within the GitHub help docs, we use several content models. For our team, this essentially amounts to several types of content that we create: conceptual, reference, and procedural. We explain complex concepts and functionality in conceptual articles, lay out important information in reference articles, and give detailed steps for procedures in procedural articles. We try not to document the user interface; people are interested in performing tasks, not getting a written description of where buttons are located. To this end, we create guides that tell stories and bring people on task-based journeys. Instead of telling people about a new feature, we focus on specific tasks that different audiences may want to perform to take advantage of new functionality. We don't use FAQ's in our help docs, as FAQ's generally aren't questions asked by people using the product or technology, but rather questions internal contributors feel they need to answer. If your documentation uses FAQ's, people will have a very hard time finding the content they need to answer their questions.

In terms of laying out content, you should limit articles to a single content model focused for a specific audience. In the article, you should include the most important information near the top. In our documentation at GitHub we include an introduction at the top of each article that gives people an overview of the topic. We try to use specific language that we know people use when talking about that topic as the article introductions are tied to our SEO results.

The content in the article should be written in active voice. At GitHub, we have a conversational, friendly voice and adjust our tone as needed to match the type of content we're discussing. Our tone is more lighthearted when discussing topics like emoji reactions and more serious when discussing safety issues.

There are a lot of great resources to help you create meaningful help content for people. One of my favorites is 18F's "[Content Guide](https://pages.18f.gov/content-guide/)."

-@jleaver

#### How to find topics to write about?

Sometimes new topics are really obvious: a new feature, different software requirements, or UI changes that affect procedures. Other times, potential topics are a bit more abstract. It's difficult to _start_ writing when you're not entirely sure _what_ to write about. The best thing to do is find pain points for your users, concepts that are difficult to understand and will negatively impact the user experience if they're not well understood, procedures that require multiple steps or screens, or important reference information that users need to know to prevent significant difficulties or loss of data. To find these pain points, you can search user forums, Twitter, or identify trends in customer help tickets. Don't underestimate your own understanding (or misunderstanding!) of a product. Often the procedures and concepts that you're struggling to understand as a new user are also causing issues for other users. If you're using a new product, keep a running list of issues you overcame or concepts and procedures that could have helped you accomplish your tasks more quickly.

-@jleaver

---

@ruxiang05

#### How to write about technical topics when you aren't confident about it?

I think the adage 'fake it until you make it' is perfect for this question. It isn't uncommon for a technical writer to create content for something they aren't completely familiar with. When I started as a technical writer I created content for Laboratory Information Systems (aka software for hospitals) and rarely stepped into a hospital let alone familiar with the software lab technicians were using to review my tests. The first thing you need to remember is you aren't alone when trying to create content for something, and there are more knowledgeable individuals who would love to make sure their content is documented accurately. Using an open source project as an example, if you were to volunteer to create content for an open source project that you were interested in but weren't at an 'expert knowledge level', I would imagine the project owner would just be thrilled that someone wanted to create the content they didn't have the time to create. Additionally, your inexperience can be viewed as a positive, who better to create content on a project than a user who isn't an expert? You are going to run into the novice-level problems that most project owners probably won't identify.

Without diving into this topic for pages and pages, I think the biggest thing to remember is, everyone has been a novice before and your inexperience with something shouldn't be a detractor to creating content. As silly as it sounds, if you believe in your ability to do the necessary research to create awesome content, you can 'literally' write about anything.

-@beardofedu

#### Best practices for writing

From a software documentation thought process, identify your needs and wants early and often. It might be awesome to create content for an extreme edge-case because you are excited about it, but how many users are actually going to need that content over some basic workflow content? Try and find the issues that the user is going to run into when going through a process and highlighting those issues in the documentation with 'notes' or 'labeled content'.

Iteration is key. Before I started teaching GitHub I transition documentation from CHM-based documents to HTML-based documentation that could easily be updated as the product changed. Don't be afraid to release content that covers 90% of the use cases for a product and adjusting on the fly as time allows. It isn't uncommon for a feature to be incomplete by the time documentation is needed, get your documentation as close to done as possible and adjust or fix it as needed once the product has been released.

Take chances; change your the delivery format (users accustomed to paper manuals? move to web-based content as an example), encourage users to discuss issues on a forum monitored by the documentation team as opposed to sending emails to support (MadCap Software fostered an amazing forum community which I'm sure reduced support ticket submission), etc.

Encourage users to suggest changes or provide their own content. Advanced users enjoy providing how they accomplish tasks in a more streamlined process than the one you provide documentation for. Adjust your documentation based on the input from users and your documentation will definitely benefit and be better.

-@beardofedu

#### How to get ideas on technical writing

For this question, I  think you can group 'technical writing' into two categories: Software Documentation and Technical Concepts content. My experience as a technical writer focused on developing content for applications that were in development or already released for internal/external use.

From a software documentation standpoint, I typically identified the 'standard' use case of the software and developed an outline of the content that would be most beneficial to the user(s) (EDIT: go into detail about identifying users in @kim-codes question about defining an audience).

On the other hand, creating content that is more conceptual in nature, let's say, using GitHub Pages for Product Documentation, you could identify what delivery methods are currently used by most organizations, describe how GitHub Pages would be used as a delivery method, identify the pros and cons of the various delivery methods ('typical delivery method' vs GitHub Pages), etc.

If you are planning on creating content for Open Source projects or conceptual  content (for a blog or something similar), focus on topics you have are interested in, you are more likely to finish a document if you would benefit or be interested in the final product as a reader.

-@beardofedu

---

@kim-codes

#### How does technical writing differ from any other type of writing? What should we pay attention to/be mindful of?

I remember taking a creative writing class in college as the only 'technical writing' major and the teacher reference my degree choice as a 'writer who wanted to make a living as opposed to being creative' which needless to say didn't get a standing ovation from me...

Depending on your content, my background is software documentation, technical writing is typically more 'process driven' aka how does a user successfully complete a task. The field definitely has room for creativity, but typically in how you can deliver content more efficiently (what delivery method will actually get views? are users able to read your instructions and actually use them? etc.) as opposed to say marketing writing where you make a pair of pants sound like the only thing that is keeping you from enjoying your life (subtle jab at marketing writing).

My personal opinion on technical writing is to deliver content in an easy-to-read format and get the user to their desired destination as quickly and efficiently as possible. If we used giving directions as an example. informing a driver about the lefts and rights they need to take to successfully reach their destination is important, informing them that their is an amazing diner along the way is extraneous and takes away from their desired goal.

-@beardofedu

#### How in-depth do we go? Does it depend on our audience? Is that something we should define before (define our audience)?

When creating software documentation, the team I was on used a 60-30-10 rule to identify what content we should focus on. The breakdown for this rule looked something like this:
- 30: Below Average User - User unfamiliar with using software to complete a specific task. Uncomfortable using a computer for day-to-day activities. Need content that some would identify as incredibly basic / rudimentary. Some examples of content I created for this range included: Identifying how to use a mouse and What a keyboard shortcut was.
- 60: Typical User - Potentially had previous experience using software to complete similar tasks. Comfortable using a computer to complete daily activities. Borderline expert user but still gets hung up on some of the advanced uses of the software (either needs to look at documentation to complete the task or ask a co-worker for assistance). Some examples of content at this level includes: Performing X task (essentially 'out of the box' workflows aka what the user bought to software to accomplish) and similar content.    
- 10: Advanced User - Learns software to complete daily tasks easily. Looks for workarounds or shortcuts to complete tasks. Identified as the 'go-to person' when teammates encounter issues. Potentially creates internal content for their team on how they should be utilizing the software. Some examples of content at this level includes: Administrating your team on <software> and Creating custom workflows.

-@beardofedu

#### Is writing in first person for technical writing 'bad'?

My experience as a technical writer revolved around creating content for software and providing instructions for how to use said software. Using 'first person' language in that capacity wouldn't have been helpful for the user and really didn't fit with the overall narrative of the content I was producing. When creating instructions for a product, you are typically identifying what the *user* should be doing so using *I* or *We* wouldn't really fit.

If you are creating content for a technical blog (product review, researching a new trend, etc.) the use of first person writing might seem viable, however a basic Google search for `first person technical writing` identified that most scientific documentation guidelines prefer avoiding the use of *I* and *We* (It was found that vs I found). Off the top of my head, it isn't uncommon to see something like 'We tested the iPad's battery by....' in a product review, so it might be best to identify how you want to relay information to your reader and be consistent about it.

-@beardofedu

#### If it would be possible to see a 'bad' technical post vs a 'good' technical post.

An article from GitHub help that _isn't_ super helpful: "[Can I archive a repository?](https://help.github.com/articles/can-i-archive-a-repository/)"

*Cons:*
- The article title is in the form of a question. People generally don't search for questions. Instead, someone might search for "Archiving a repository."
- The article doesn't follow any of GitHub's content models. It's not quite a conceptual article or a procedural article. To help a user understand the concept of archiving _and_ the procedure to archive content on GitHub, there should be separate articles: a conceptual article and a procedural article. Without a clear point of view, this article doesn't really help solve any problems for users.
- There isn't an introduction to the article, so users have to read all of the content to understand what information the article is trying to convey.
- There aren't helpful links to other GitHub articles or external URLs. If a user didn't know how to clone a repository or understand information about wiki's, they'd need to search on their own.
- There's a link to contact GitHub support, but the button immediately below that also contacts GitHub support. It's confusing to offer multiple avenues to users who are trying to accomplish a task.

An article from GitHub help that _is_ helpful:
"[Moving a file in your repository to Git Large File Storage](https://help.github.com/articles/moving-a-file-in-your-repository-to-git-large-file-storage/)"

*Pros:*
- The article is appropriately titled for a search someone might perform.
- There's an introduction that helps orient the user and set expectations for the rest of the article's content.
- Links to applicable content are used throughout the article. Rather than replicating this content, the links provide users the option to navigate away from the primary procedural content if necessary.
- There are links to other articles in a "Further reading" section to give the user options to gain a more in-depth understanding of the concept.

-@jleaver

---

@shubheksha

#### How much do you need to know about the topic?

This is pretty closely related to a question that @beardofedu answered above about writing about topics that you're not super comfortable with. Most of the writing I've done has been about topics that I have absolutely no previous knowledge of. Before joining GitHub, I'd never used Git or GitHub; even my knowledge of the command line was fairly limited. It seems scary sometimes to write about a topic that you're not already an expert in, but by the time you're done researching, testing, and writing, you'll have a much more advanced understanding of the topic!

To write about a topic, you need to do enough preliminary research and testing to inform the type of article you're writing and the audience you're writing it for. Once you're writing about a topic, you can perform more research and testing, talk to stakeholders and (if possible!) users, and find holes in your understanding. If you're feeling really unsure about the technical accuracy of your content, you can ask experts for a review around the 30% completion mark; asking for a preliminary review can help make sure you're going down the right path with your content.

-@jleaver

#### How do we decide the difficulty level of the post?

At GitHub, we don't focus much on the "difficulty level" or the perceived expertise of the reader. We focus more on specific audiences; for instance, an organization owner might need very different content than an individual contributor. We separate the content for those audiences into different articles (and different guides). These guides may have some content that lends itself to people just starting out and other content that's more focused on advanced concepts. A single article can span the gamut from "easy" to "difficult" content. Rather than trying to assess the expertise level of our users, we focus on identifying difficult problems and helping people solve them.

-@jleaver

#### Average amount of research needed for a topic you're not to familiar with/an expert on?

It depends on the topic. Sometimes a topic may only require a few hours of research. Other topics take days or even weeks of research. Only about 10 - 15% of my time is actually spent writing. The rest of my time is spent working on content strategy, research, testing, editing, and reviewing other people's work. While I'm writing, I continue to research and revise my content accordingly.

-@jleaver

#### How to choose a title that caters to the majority of the audience w/o evading anyone?

In another question, @jleaver identified how the title of a help topic in GitHub's documentation could potentially limit the amount of people who found it because it was written as a question. If the content you are creating is focused on completing a specific task; 'Editing a User Profile', 'Adding a Repository', 'Creating a Blog using GitHub Pages' (or 'Setting Up a Blog' in the GitHub Pages documentation could also work, since GitHub Pages is implied) are all titles that cater to the majority of your audience as they focus on a specific task.

Going back to my discussion of identifying your user's knowledge levels can also improve the efficiency of how you title your topics. Unfortunately, you will always encounter examples of users not finding your content no matter how carefully you title your content. Using analytics to identify if users are finding the content you are creating can be helpful in defining the style in which you title your topics. If given the opportunity to run user tests, you can also observe the road blocks that you, as a subject matter expert, didn't even think of.

To sum it up, choosing how you title your content is an iterative process and you should become comfortable with the fact that no matter how much research you do in regards to content titles, layout, and subject matter, you might need to go back to the drawing board from time to time to improve the experience of your end user/audience.  

---

@lionex

#### How do we find or identify an audience?

When I created content outside of typical software documentation, I created content that would benefit me. When I first started using a software tool, MadCap Flare, I found that there was a lack of content for people who were trying to push the software past the typical use-case so I began creating content for how I was implementing various features that were outside the scope of the out-of-the-box functionality.

My suggestion would be to create content that benefits you or a group of people you know and 'if you write it, they will come'-mentality your project. Don't focus on building your audience as the key reason to begin writing. Focus on providing a solution to an existing gap in the available content and your audience should organically grow.

One way to find your audience is to review popular forums that your audience may use. This might help identify topics that your potential audience would be interested in reading.

-@beardofedu

#### What helps to reach a wide audience?

Something to consider when trying to identify your audience or the number of people you are reaching with your content is what percentage of the population your expected audience takes up. If you are tasked with creating content on Information Security you probably aren't going to be the most 'liked' or 'shared' link on Facebook, but you should be focusing on getting experts in the field to appreciate your content. Building a reputable brand with other established individuals in your field is a great way of reaching a broader audience.

Obviously writing content as a technical evangelist sometimes requires you to create content that identifies how _your_ product solves the problems people face regularly. With that in mind, some posts can just simply mention, 'if you have questions on how Acme Industries can help secure your information, hit us up' and just providing your point of view on current events or advancements in a specific field.

Find your voice and the things you are passionate within a certain field. I really like business continuity and disaster recovery planning, so if I was going to write about information security, a blog that I would create content for would include information about those two items as well as posts about the product(s) I was responsible for promoting, even if the product(s) had limited functionality within that space.

-@beardofedu

#### How should we approach pedagogical writing, and what kinds of supporting or supplementary materials should we provide?

I briefly touched on this in another answer, but when you set out to create content focus on the specific task at hand. If I was to use an example of creating a blog on GitHub Pages, the primary content would discuss the different steps necessary to successfully create the blog. As far as supporting / supplementary content, I might include things like Markdown 'cheat sheets', additional GitHub Pages themes, advanced topics outside of the scope of a traditional blog setup, and other content along those lines.

Essentially, your content should answer the question or process at hand, then supply additional content that provides context to members of your audience on both ends of the 'knowledge-level spectrum'.

-@beardofedu

#### What style, in a literary and grammatical sense, do we employ in technical writing?

At GitHub, we use a conversational voice and tone. We try to "write like a human," which means we avoid robotic, formal language. By using [plain language](https://pages.18f.gov/content-guide/plain-language/), we increase comprehension and accessibility. It's easier for people to understand the topics we're writing about. We never want the language to be something that users need to overcome. They're reading the documentation so they can solve a difficult problem they're facing and the language we use to help them should be clear, concise, and free of jargon.

We're also mindful of the difference between [voice and tone](http://voiceandtone.com/). Our GitHub voice is friendly, conversational, and helpful. The tone we use is dependent on the topic we're discussing. For instance, the tone we use for error messages, warnings about data loss, or issues of safety are very different than the tone we use for articles about fun UI features. To understand the _tone_ you should use when talking about a topic, you should put yourselves in the user's shoes and understand what their state of mind may be when they're approaching that topic. If they've just gotten an error message about catastrophic data loss, finding an article about their issue with lighthearted language won't feel appropriate.

-@jleaver

#### How can we create effective supporting documents? (I mean items like meeting notes, design specs, etc)

When creating content, I typically write from a 'less is more' perspective and use additional links to provide context outside of the scope of the identified solution my document is providing. For instance, if I was creating content for "Adding a User Account", the primary content for the document would identify how to add a user account to the system and I would provide additional links to things to either related content or typical next steps. As an example, I might include links to content related to 'Modifying an Existing User Account' or 'Deleting a User Account', other content like 'Creating Teams' or 'Organizing User Accounts' might be identified as content that is useful for a small subset of users and not directly related to the task at hand. I might also link to things more descriptive or reference like as opposed to linking to additional processes. An article like 'User Accounts' might provide context as to why you would create a user account, but isn't necessary to complete the process of creating a new user account.

To create effective supporting materials, identify what questions your user or reader might encounter while using your materials and create content that can be read separately from the article they are currently reading. In terms of tools I have used to create said content, outside of typical text editors, I have used SnagIt and Gimp/PhotoShop to create images, Camtasia and ScreenFlow to create videos, and have started using tools to create .gifs as opposed to full fledged videos for minor processes (but the software name escapes me at the moment).

Although you might be considered an expert at the topic you are creating content for, trying to read your content from the perspective of your typical user can provide a great context for what content you need to add to your documentation. Using analytical tools like Google Analytics can help identify if the supporting documentation you are creating is being utilized by your readers or if it being ignored. If you can identify that your 'beginner' level content is getting a lot of traffic, creating more supporting materials that provides context to why you would perform a task is an example of creating effective supporting documents that your audience is 'demanding'.

-@beardofedu

### What are some common mistakes people make in things like project README's or documentation aimed towards people using and developing for the project?
  
So, I searched for "awesome README files" to show what great projects are doing and I immediately started nitpicking the sites this [repo](https://github.com/matiassingers/awesome-readme) selected as "awesome".

Quick breakdown of some sites:

- [gaze](https://github.com/shama/gaze) - putting the release notes in the README seems like an incoherent use of space. They could just as easily link to their release notes that are hosted elsewhere. This would reduce the length of their README.

- [bluebird](https://github.com/petkaantonov/bluebird) - putting the license in the README seems redudant. The license is available in the link at the top of the repo and as a file within the repo.

- [pageres](https://github.com/sindresorhus/pageres) - Why list the API content in your README? Just link to content about your API. As the scope of your project expands, having solid API documentation outside of a text based list will be helpful for your users.

- [httpie](https://github.com/jakubroztocil/httpie) - So. Long. Can't. Stop. Scrolling. The README has a lot of great information with an emphasis on A LOT. The README could build a solid GitHub Pages-based website.

So, my thoughts on README files and documentation in general (without stepping on Jenn's section):

- **Step Back**
   Disconnect yourself from how "you" use your project / product and identify how an end user is going to use it. If you can't think of it, ask a friend, preferably someone who isn't making as many commits as you to the project.
- **Right Place, Right Time**
    If you were looking for content on "how to do an advanced function", would you look on the same page that described how to "install the service"?
- **Delivery Methods**
    The beauty of Git is the ability to work without an internet connection, however, if I'm learning new content without an internet connection and you only provide content online, how can I learn how to use it while, say on a plane? Create a really basic "print friendly" version of your content for your users.

### If I create a new library, I tend to make a blog post to help demo the use case a bit. Is there a rough structure structure you've noticed which works best for this? Such as, is it sensible to talk about the use case first, or are code snippets best placed towards the top?

Without an example (which is not a big deal), I have a couple of suggestions:

- Describing why I would use your library should be first, I don't care about your code snippets if I don't know why I would use it.
- Think of the top _X_ (maybe try to hit 3) use cases for your library / product / project and identify the process to complete that.
- Use other projects as an example for what you want to do and what you *do not* want to do.

### Within an open source project, what tends to be the most useful form of documentation? I'm wondering where might be best to spend time, perhaps architectural overviews in a wiki or maybe it's code level comments, perhaps auto-gen docs, or the README.

If I had to organize your "documentation plan" into a sort of NEED to NICE to have list, it would look something like this*:


- README, project introduction, primary contacts, how to contribute, install instructions
  - Getting Started Guide - probably created when README starts to become "too big"
- For an API, I think Apiary[www.apiary.io] looks pretty solid, but, a GitHub Pages [site](https://facebook.github.io/react/docs/hello-world.html) for your API can look pretty solid as well.

Bottom line, make it easy for other contributors to assist with content creation. Maybe start a GitHub Pages site and if you need to scale up, check out Apiary or one of their competitors? I just learned about them recently, so I'm fairly new to that specific space.

_*disclaimer:_ the _type_ of project you are working on will most likely alter the importance of your documentation deliverables.

### What sort of tools do you tend to use in different types of documentation? Most of my docs are markdown and blog posts, is there something big I'm missing out on?

I used to use Flare, which was an XML / HTML documentation tool that would create Online and Print content from the same source content. It was a GUI environment and I'm a Windows user, don't hate me. From Flare, I moved to Indesign to create mammoth text book files and didn't get to digital very much. Now, I write primarily in Markdown, actually, I do everything in Markdown at this point.

### One question I have to do with blogging, is how to deal with varying skill levels of readers.

10-30-60.

10% of your users are going to be advanced and potentially be subject matter experts on your product(s) for their company / local <insert hobby> group

30% of your users won't know how to use your project without very detailed documentation and will require the most assistance if your content is missing basic concepts. As an example: I had created hospital software documentation that in 2007 still needed documentation on what a mouse was. 🖱 :

60% of your users are going to have the technical accumen to pick up your product and use it with some help. Spend your time here.


### I'd love to hear a bit about voice for technical writing. Both in terms of style, and also active vs passive voice

On Style:

I prefer not to take myself too seriously, so my documentation typically doesn't either. My primary goal is identify the expected outcome and get the reader there. If I use 17 terrible git puns along the way, they are probably better because of it.

Active vs Passive:

- Use Active if: the user needs to do something
- Use Passive if: someone needs to do something

I'm pretty terrible at active vs passive conversations, so I'm going to let this random blog provide insight: [random blog](https://freelance-writing-articles.knoji.com/technical-writing-basics-using-the-active-voice/)

On Grammar:
- Pick a style guide and "use it". "Use it" meaning, try really hard to use it in your content, but if you miss an Oxford comma, the world isn't going to end. However, if you _click_ buttons, don't tell people to _press_ them on another page. Consistency is really important, especially with instructions.

## Related Links
- Blogs: [I'd Rather Be Writing](http://idratherbewriting.com/) | [Docs Like Code](http://docslikecode.com/) | [FFeathers](https://ffeathers.wordpress.com/)
- Conferences / Meetups: [Write the Docs](http://www.writethedocs.org/) | [Confab](http://confabevents.com/) | [IA Summit](http://www.iasummit.org/) | [Tech Comm on a Map (interactive map of all tech comm conferences)](http://sarahmaddox.github.io/techcomm-map/)
- Slack teams: [Write the Docs](http://slack.writethedocs.org/) | [Content + UX](http://mjmetts.com/content-ux-slack/)
- Markdown Guides: [GitHub's Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
 | [Adam P's Cheat Sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
- Content Guides: [18F's Content Guide](https://pages.18f.gov/content-guide/) | [MailChimp Content Style Guide](http://styleguide.mailchimp.com/)
- Documentation Outline Tool: [Mindmup](https://www.mindmup.com)

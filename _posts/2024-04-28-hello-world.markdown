---
layout: post
title:  "2024 W17: Hello, World!"
date:   2024-04-28 08:12:11 -0400
categories: weeknotes
---

# Week 17 - Hello, World!

Hello! We are 17 weeks into the year, but it's not too late for me to complete my news resolution and get this site up and running and start posting weeknotes. In service of that goal I created this site with Jekyll and for now have done no customization or tinkering. Chalk that up as a win for "Just doing the thing". I credit my colleague Matt Valentine-House consistently posting [interesting weeknotes](https://www.eightbitraptor.com/weeknotes/) as the kick I needed to get going with this site.

So here we go...

- At work, I am finishing up a project. In Rails 7.2 new apps will ship a [Dev Container](https://containers.dev/) setup. I have spent the last couple months creating this functionality and building up the Dev Container ecosystem for Rails applications. I'll be posting something more detailed about that on the Shopify blog soon, which I'll link to here.

  The experience working with Dev Containers is quite nice. I recently set one up for a (non-Rails) side project and was able to get working in under 10 minutes. Meanwhile, setting up this Jekyll site locally on my machine was a pain because I tried installing ruby 3.3.1 and immediately ran into issues with my OpenSSL version. Right now I have been using Dev Containers on a per-project basis, but after today's experience I'm thinking about setting up a container right in my `src` directory. On the rails side we solved this problem with the [`rails-new` tool](https://github.com/rails/rails-new), which can create a Rails project on a machine on any machine, even one that does not have Ruby installed.

  Working with Dev Containers has motivated me to switch to using VSCode. VSCode is the blessed editor at Shopify but I have stubbornly stuck with Rubymine. But I finally made the switch so I can dogfood my work, and I am adjusting reasonably well. (NOTE: Rubymine does have Dev Container functionality, though I haven't used it)


- I fixed a problem in Rails where the state of the `BacktraceCleaner` was being cached by Spring. By default the `BacktraceCleaner` is configured to silence lines from Rails and other gems. But it can be turned off when running tests by passing the `BACKTRACE` env variable. My team and I tend to use this a lot as we are troubleshooting issues with Rails and need to see the full backtrace.

  A change was recently made to Rails to allow the `BACKTRACE` env var to unsilence the backtrace everywhere (console, server, runner etc.), not just in tests, which is really useful. However, the implementation had a side effect of caching the state of the cleaner (silenced or unsilenced) in spring, meaning spring needs to be reset everytime you want to silence or unsilence the backtrace. Which is annoying. The fewer times I need to say "it's not working because I forgot to reset spring" the better. You can see my fix [here](https://github.com/rails/rails/pull/51670).

---


- Outside work and programming topics, I plan to use this space to discuss my reading. I read a lot, although I have been in a bit of slump the last couple weeks.

  Currently I am reading [Auto-da-Fé](https://en.wikipedia.org/wiki/Auto-da-F%C3%A9_(novel)) by Elias Canetti and really enjoying it. Canetti's writing is intense and hard-edged. There's a kind of malicious intelligence here, that feels like it prefigures Bernhard and Jelinek. It makes me wonder if there is an "Austrian style" I am detecting through the translation. Another thing those three have in common is they were all accomplished playwrights, which shows in their dialogue - and their narration, which typically reads like monologue.

  On the topic of translation, I noticed this was translated by CV Wedgewood, who I believe was something of an auto-didact. Her [history of 30 years war](https://www.nyrb.com/products/the-thirty-years-war) is the kind of opinionated, well-read yet un-academic fiction writing that seems to be an extinct species now. The translation is good, but old translations (this one is about 80 years old) tend to feel dated in a way that the originals do not, and I feel that here a bit. You have to wonder what was lost when the radical writing of modernists like Canetti was filtered through British translators of that era.

- It's been two years since I stopped using Good Reads to track my reading. I stopped for no other reason than I just didn't feel like using the site anymore. Since then I have been tracking my reading in a small journal. I plan to put my 2023 and 2024 reading logs on this site in the near future.

- I am watching The Sopranos with my wife. It's her first time. I haven't watched it since 2012 and I'm finding I remember very little. We are on the fourth season at the moment, and I do feel things dragging a bit. I can't help but compare this show to Mad Men, and the comparison is mostly not positive. I'd say The Sopranos is fundamentally pessimistic about people, but (so far) doesn't reach moments of true darkness that Mad Men does. Those moments are built on compassion for the characters, but the characters in the Sopranos are treated like grotesques. Compare the handling of Rachel's death in Mad Men and Gloria's in The Sopranos. At heart The Sopranos is a comedy. It works best when it leans into its absurdity, and kind of falls over when it gets too serious.

- We are dog sitting! It has been a lot of fun. Paisley is our friend's 5 year-old golden-doodle. She is a rescue and extremely sweet, but very shy. We have her for 2.5 weeks while our friends are away visiting family.

---

- What I am listening to this week:

<iframe style="border-radius:12px" src="https://open.spotify.com/embed/album/1XEPKavl3nlI2qVt8HuA5n?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>

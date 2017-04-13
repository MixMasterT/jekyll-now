---
layout: post
title: React-Native at Wallmart Labs
---

## Great Learning Experience

Last night I ventured further South than I have been in a while. I took
BART all the way down to San Bruno in orter to attend a React-Native
conference at Wallmart Labs.

I was hoping to find a job lead, since I have been contacted by recruiters
claiming to work with Wallmart Labs a few times in the past few weeks.
No one at the conference mentioned anything about hoping to grow their
team, but I still found the experience quite rewarding. I learned a lot
so I am very glad I went.

We heard talks from three different speakers at this meetup including Matt
Bresnan, Software Engineer at Walmart Labs, Benoit Lemaire, principal engineer
at Walmart Labs, Lucian Masalar, Mobile Architect at GoDaddy. Each speaker
presented interesting information and food for thought relating to React-Native.

Matt Bresnan explained the decision-making process that motivated Wallmart
to adopt React-Native for their mobile platform, and gave some performance
metrics. He explained that they chose React-Native as a compromise between
ideal efficiency, which could be achieved with two teams focused on iOS
and Android separately, and easy development, which could be achieved by
wrapping their website in a Webview and packaging that as an Android and
iOS app. He explained that Wallmart didn't have the resources to assemble
two separate teams of engineers focused on two separate platforms, so that
was not going to work. However, they use of a web-view had already proven
to be too slow. Therefore, they chose to give React-Native a try, and they
were very happy with the results. Load times and UI response improved significantly
after they rebuilt their mobile experiences in React-Native. The only
exception to this was slightly increased memory requirements on Android
devices. I figure this anomaly may have resulted from the fact that their
webview rendering benefitted from server-side rendering. If the backend
was building up their DOM tree and sending it in pre-assembled form, that
might explain the increase in memory required then that work was handed
back to the local device. Everything else was improved, however, including
CPU usage, and most importantly load times. Better user experiences were
also correlated to better mobile sales. React-Native proved to be a big
win for Wallmart Labs. For more details, see this post[http://brianyang.com/react-native-at-walmartlabs-walmartlabs/]
by Brian Yang.

Benoit Lemaire spoke about Wallmart Labs' new Madgellan open-source
project. This is a pretty sophisticated project that is built on top of
React-Native. That is really fascinating when you think about it. React-Native
uses JavaScript and JSX to build native Android (Java-like) code, and iOS
(Swift) code. And here they are, building another framework on top of a
framework to enhance the features and usability of React-Native. Magellan
helps modularize React-Native projects into 'MiniApps', and supports lots
of automation, including test automation. You can learn more about this
project at the github repo[https://github.com/TestArmada/magellan]

Finally, Lucian Masalar shared his opinions, advice, and suggestions with
regard to using React-Native. This was very interesting to me, because I am
completely new to mobile development, whereas he has years of experience
in this area. He highly recommends using React-Native, but also warns that
serious mobile developers will need at least access to experts in Android
and iOS development who might be able to help them deal with some of the
platform-specific sticky points, such as cocoapods for iOS. I was pleasantly
surprised that most of his advice about React-Native itself was familiar to me.
The most important point being to understand how React works, and build
accordingly. He strongly recommended using Redux and Redux-thunk to manage
data. I liked that because I am familiar with these technologies.I asked
him specifically about his suggestions regarding when to separate components
with their own containers, and when to combine components by passing props
between them. He explained that although he was tempted to combine things
together and reduce the total number of files in a project at first, he now
believes it is best to keep everything as small and modular as possible.
The main reason behind this suggestion was for maintainability and testability.
It certainly makes sense that small, modular components are easier to write
tests for than large tangles of code. I would say that was the most important
take-home point for me of the night.

I am really lucky to get to attend these high-quality events. If you
are in San Francisco, be sure to get on Meetup.com and don't miss out on
these great learning experiences.

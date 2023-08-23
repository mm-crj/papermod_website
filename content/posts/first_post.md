---
title: "The Derivative Dilemma"
date: 2020-09-15T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ['first','math','derivatives']
author: "Mainak Mandal"
# author: ["Me", "You"] # multiple authors
katex: true
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "The Derivative Dilemma"
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/<path_to_repo>/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---
We all have seen the logic defying calculations proving $1=2$ in school, haven't we? The simple ones are based on the mathematical fallacy of division by zero _i.e.,_ cancelling an algebraic expression from both sides which is equal to zero. I have one such trick calculation to show you, its a bit more sophisticated (than division by zero) based on the concept of "derivative". The problem goes as follows, $x^2$ can be written as sum like this:
\\[ x^2=x+x+x+\cdots +x \qquad \textit{    x times}\\]

differentiating both sides $w.r.t$ $x$ we get,

\begin{align}
\frac{d}{dx}x^2&=\frac{d}{dx}(x+x+x+\cdots +x ),\\nonumber \\\
\implies 2x&=1+1+\cdots +1 \qquad \textit{ x times},\\nonumber\\\
\implies 2x&=x.\\nonumber
\end{align}

Which is simply not true, so where is the error? While you ponder about the error in the steps shown above, I would like to tell you a little bit about my history with the problem.

A friend of mine had first shown me this "paradox" in school, when we were first learning about derivatives. I don't remember if he knew or had shown me the solution, but I do remember the next time I had seen the problem. In the spring of 2013 in LH3, pre-fab IISER Kolkata. Prof. Ananda Dasgupta was teaching us about differential equations and someone probably got bored and to slow down the fast paced Prof. Dasgupta had asked the same question. I was half asleep, so the explanation that Prof. Dasgupta offered flew over my head. The next encounter was in L'aquila Italy, the first time I met Ankan da. Somehow this came up, and finally, this time I understood the trick in the computation. The next time this came up was while I was visiting a friend Dr. Arun Pandey in Leuven, Belgium in 2019. We were in his office scribbling on his white board and I showed him the problem. Funnily enough, by then I myself had forgot the explanation! Anyhow, it bugged him so much that he dug up MathStack and texted me the solution as I was on my trip back to Dresden. Finally, I am writing it down, so that if I forget it again(almost sure), then I can always refer back to this.

So what was the issue with the calculation? Some of us, who are handy with the first principle definition of a derivative, must have tried that way. But in-fact it is much simpler than that. In the first step, we asserted that $x^2=x+x+x+\cdots +x \quad \textit{ x times}$. But if we give it a moment's thought you will realise that it is only true when $x$ is a natural number($\mathbb{N}$). Can we expand $1.1^2$ as the sum of $1.1$, $1.1$ times? That doesn't make sense. So the first equality is valid only on natural numbers, and there lies the catch. We cannot define derivatives on sets like natural numbers, but why?  

Let's explore that further, the definition of the derivative of a function $f(x)$ is a infinitesimal definition, given by
\begin{align}
\frac{df(x)}{dx}=\lim_{h\rightarrow 0}\frac{f(x+h)-f(x)}{h}, \\nonumber
\end{align}
if both $\lim_{h\rightarrow 0^+}\frac{f(x+h)-f(x)}{h}$  and $\lim_{h\rightarrow 0^-}\frac{f(x+h)-f(x)}{h}$ existed and were equal. $0^+$ and $0^{-}$  are just mathematical jargon to say a little to the right and left of zero respectively, but as close as we want. Let's say we want to the derivative of $f(x)$ at $x=2$(which is a natural number). Does the derivative at a single point makes sense? To find the right hand limit $\lim_{h\rightarrow 0^+}\frac{f(x+h)-f(x)}{h}$, we have to evaluate it at a series of points closer and closer to 2 and then take the limiting value at $x=2^+$ when $h=0^+$. Similarly for the left hand limit. To take the limit at a point we need to see it as a series of approximations approaching it from the right, or the left. If the equality doesn't hold except on natural numbers, how are we supposed to take a series of approximations approaching from either side? Therefore the limit doesn't exist on the set of natural numbers. The derivative of a function is not a point property. This is not to say that $x^2$ is not differentiable, it is differentiable on $\mathbb{R}$ but not on $\mathbb{N}$.

Me and Arun later published a [YouTube Video](https://www.youtube.com/watch?v=jrNnyHzv1H0) about this, and sent it to [Summer Of Math Exposition 2](https://www.3blue1brown.com/blog/some2)(2022) by Grant Sanderson's [3Blue1Brown](https://www.3blue1brown.com/). I think we stood 105 out of several thousand entries and that was great fun. 

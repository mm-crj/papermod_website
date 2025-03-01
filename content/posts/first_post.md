---
title: "The Derivative Dilemma"
date: 2023-09-01T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ['first','math','derivatives']
author: ["Mainak Mandal", "Arun Pandey"]
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
We all have seen the logic-defying calculations proving $1=2$ in school, haven't we? The simple ones are based on the mathematical fallacy of division by zero _i.e.,_ cancelling an algebraic expression from both sides which is equal to zero. I have one such trick calculation to show you, it is a bit more sophisticated (than division by zero) based on the concept of "derivative". The problem goes as follows, $x^2$ can be written as a sum like this:
\begin{align} 
x^2=x+x+x+\cdots +x \qquad \textit{    x times}
\end{align}

differentiating both sides $w.r.t$ $x$ we get,

\begin{align}
\frac{d}{dx}x^2&=\frac{d}{dx}(x+x+x+\cdots +x ),\\nonumber \\\
\implies 2x&=1+1+\cdots +1 \qquad \textit{ x times},\\nonumber\\\
\implies 2x&=x.\\nonumber
\end{align}

That is simply not true, so where is the error? While you ponder about the error in the steps shown above, I would like to tell you a little bit about my history with the problem.

A friend of mine had first shown me this "paradox" in school when we were first learning about derivatives. I don't remember if he knew or had shown me the solution, but I do remember the next time I saw the problem. In the spring of 2013 in LH3, pre-fab IISER Kolkata. [Prof. Ananda Dasgupta](https://www.iiserkol.ac.in/web/en/people/faculty/dps/adg/) was teaching us about differential equations and someone probably got bored and to slow down the fast-paced Prof. Dasgupta had asked the same question. I was half asleep, so the explanation that Prof. Dasgupta offered flew over my head. The next encounter was in L'Aquila Italy, the first time I met Ankan da. Somehow this came up, and finally, this time I understood the trick in the computation. The next time this came up was while I was visiting a friend [Dr. Arun Pandey](https://github.com/MrPandey01) in Leuven, Belgium in 2019. We were in his office scribbling on his whiteboard and I showed him the problem. Funnily enough, by then I myself had forgotten the explanation! Anyhow, it bugged him so much that he dug up MathStack and texted me the solution as I was on my trip back to Dresden. Finally, I am writing it down, so that if I forget it again(almost sure), then I can always refer back to this.

So what was the issue with the calculation? Some of us, handy with the first principle definition of a derivative, must have tried that way. But in fact, it is much simpler than that. In the first step, we asserted that $x^2=x+x+x+\cdots +x \quad \textit{ x times}$. But if we give it a moment's thought you will realise that it is only true when $x$ is a natural number($\mathbb{N}$). Can we expand $1.1^2$ as the sum of $1.1$, $1.1$ times? That doesn't make sense. So the first equality is valid only on natural numbers, and there lies the catch. We cannot define derivatives on sets like natural numbers, but why?  

The definition of the derivative uses the concept of a limit, let's look at the mathematical definite first then we will also look at an example. The derivative of a function $f$ is given by 
\begin{align}
\frac{df(x)}{dx}=\lim_{h\rightarrow 0}\frac{f(x+h)-f(x)}{h}, \nonumber
\end{align}

if both $\lim_{h\rightarrow 0^+}\frac{f(x+h)-f(x)}{h}$(the right hand limit) and $\lim_{h\rightarrow 0^-}\frac{f(x+h)-f(x)}{h}$(the left hand limit) exists and are equal. $0^+$  means little to the right zero and similarly $0^{-}$ means a little to the left of zero, as close as we want. 

We now look at an example to clarify the definition. Let's say, we want the derivative of $f(x)$ at $x=2$(which is a natural number). So we must compute the left and right-hand limits and see if they are equal, right? So the RHL at $h=0.5$ is 

\begin{align}
\lim_{h\rightarrow 0^+}\frac{f(x+h)-f(x)}{h}=\frac{2.5^2-2^2}{0.5} = 4.5 .\nonumber
\end{align}

Similarly the LHL at $h =0.5$ is
\begin{align}
\lim_{h\rightarrow 0^-}\frac{f(x+h)-f(x)}{h} = \frac{1.5^2 - 2^2}{0.5} =   3.5 . \nonumber
\end{align}
Continuing in this way,

|h  | 0.5| 0.4 | 0.2 | 0.01   |
|---|----|-----|-----|--------|
|RHL| 4.5|4.39 | 4.20| 4.0099 |
|LHL| 3.5|3.59 | 3.79| 3.9899 |
------------------------------
We will see that this approaches 4. But we missed one very important point, _these numbers(2.5,1.5,2.4,1.6,2.2,1.8 ...) are not natural numbers._ Hence the equality (1) doesn't hold, and the derivative doesn't exist on natural numbers. But if we added all such fractions(and their limit points) to $\mathbb{N}$ and formed the set of real numbers($\mathbb{R}$) then the derivative would exist and $f^{\prime}(2)=4$ as we have already shown before. 

Me and Arun later published a [YouTube Video](https://www.youtube.com/watch?v=jrNnyHzv1H0) about this and sent it to [Summer Of Math Exposition 2](https://www.3blue1brown.com/blog/some2)(2022) by Grant Sanderson's [3Blue1Brown](https://www.3blue1brown.com/). I think we stood 105 out of several thousand entries, even though we had to learn some animations, sound recording, audio cleaning etc, in under 2 months. Nevertheless, it has always been fun for me to explore simple looking problems with not so simple solutions. So I would try and use the skills from that project to bring out more such problems! Till next time, tschüß!

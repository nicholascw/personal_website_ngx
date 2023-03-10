---
title: "Security Mindset: or say \"Engineering Engineering\""
date: 2023-03-10T15:57:36-06:00
draft: false
---

*DISCLAIMER: THIS ARTICLE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE ARTICLE OR THE USE OR OTHER DEALINGS IN THE ARTICLE.

To begin with, this article is not a good introductory material for you to learn seucrity mindset. It is extremely biased towards the attack perspective and at the same time a piece of summary that only reflects personal experience and impression of my own.

It's been a long time since last time I actually tries to write an article.
However, moving along the path doing cybersecurity-related works,
I feel that I have more and more stuff I want express, explain, and discuss with anybody who is or is not related to the field.
I finally decided to share my very personal and impressonal understanding to the security mindset in a few words today.

I have always been saying "I am an extremely engieenring person." So, what is engineering in the first place?
According to Wikipedia, "Engineering is the use of scientific principles to design and build machines, structures,
and other items, including bridges, tunnels, roads, vehicles, and buildings."[\[1\]](https://en.wikipedia.org/wiki/Engineering)
Why does it matter? Well, if you happen to notice the title, I call security works "Engineering Engineering."
While other Engineering fields utilize their related field to build "useful stuff", security people,
tend to take what's already there and think how exactly can we make use of them, potentially in an unintended way.
Whenever I have anything new in my view, it quickly goes into the following sequence:

(sorry, but it feels more comfortable for me to describe soemthing with C-style pseudo code when logic and control flow is needed):


```
auto *capabilities[];

void search(auto obj_in){
    auto *obj = &obj_in;
    while(obj) {
        What is *obj?

        What does or can *obj do? => save into capabilities[];

        What does it mean it have such capability? => develop aliases to the capability, save into capabilities[];
            - what does it actually allowing me to to?
            - try explain it in different ways;
            - try identify the features of the subject and object;

        How does it achieve such capability? => discover "children" or "private properties" of *obj (think it as a tree or a class);
            - learn its internanl mechenaism;
            - learn what does it utilized in order to achieve such capability;
            - sometimes, what are required in order to do such capabilities? what's not required?

        and, finally we fork bomb it by for(i : children)search(children);
    }
}

int main() {
  run search() against anything I randomly in mind;
  wait until my brain hangs, or memory exhausted;
  look into my capabilities[] in the end;
  do "capabilities[] engineering" with my best effort;
  return 0;
}

```

It may be hard for some people to understand without a more vivid example to this process:

*< TODO: But I am not coming up with any elegant examples to help you at this moment ◔ ‸◔ , sorry! >*


Essentially, yes, I do enjoy the process of tearing down whatever stuff in my hand to see what can it do in different states.
Quoting Kirill, "You like breaking up things." Obviously it does not only apply to Computer Security,
so I totally understand that sometimes people see me as a paranoid when I start to argue against some natural,
plain languages, questioning absolute statements, come up with ridiculous exceptions, etc. However, sorry,
I do intrinsically thinking like that even before I have anything to do with security researches. Quoting Michel,
"It's definitely not only about computers."

Repurposing. Yes, a lot of the times it's exactly to repurpose to an extreme, and a lot of the rest are looking for minorities in sets: people always say that I'm somewhat "general purpose edge cases generator" when it comes to poll option designing.

There are some thoughts from the defense side but much less that I would like to cover. Think this is enough for today.

*< TODO: I'll call this article WIP, but probably I will never come back to update >*



--
Nicholas Wang

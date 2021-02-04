---
layout:      post
title:      "马普所·非平衡态系统中的集体过程·语音转录 | 03.非平衡态场论"
keywords:   "mpipks-note"
excerpt:    ""
date:        2021-02-04
categories:  post
milestoneID: 29
---

# 3. Non-equilibrium Field Theory

> The slide 8 of examples was talked about at the end of the lecture rather than between neighboring slides. 

### random

<br>
`(00:00)` so i i have to set this sound to you so<br>
`(00:02)` you hear them as well so you're using<br>
`(00:04)` headphones okay right that goes<br>
`(00:08)` okay so then let's start uh so welcome<br>
`(00:11)` uh to our third lecture in collective<br>
`(00:14)` processes and this will be<br>
`(00:17)` the final lecture that is more<br>
`(00:18)` methodology methodological<br>
`(00:21)` and technical so today we'll talk about<br>
`(00:24)` a field theory representations of<br>
`(00:28)` the kind of processes that we've been<br>
`(00:29)` looking at last time<br>
`(00:32)` let me just share the screen<br>
`(00:42)` okay<br>

### slide 1

<br>
`(00:49)` here we go so if you remember the<br>
`(00:52)` lecture so you can see that<br>
`(00:54)` great uh so you remember if you remember<br>
`(00:56)` lecture that we had last time<br>
`(00:59)` uh i gave a little introduction to the<br>
`(01:02)` mathematics that is<br>
`(01:04)` behind the description of the stochastic<br>
`(01:07)` processes<br>
`(01:09)` and we discussed two kinds<br>
`(01:12)` of stochastic processes alternatives not<br>
`(01:15)` two kinds of stochastic processes but<br>
`(01:17)` two ways<br>
`(01:18)` of describing sarcastic processes the<br>
`(01:21)` first way<br>
`(01:22)` that was associated with the name<br>
`(01:24)` nonzero<br>
`(01:25)` that we already featured in the very<br>
`(01:26)` first lecture<br>
`(01:28)` relied on deriving<br>
`(01:32)` a stochastic differential equation that<br>
`(01:34)` describes<br>
`(01:36)` the time evolution of a single<br>
`(01:38)` realization<br>
`(01:39)` of such a stochastic process and the<br>
`(01:41)` alternative approach that einstein<br>
`(01:44)` applied for the description of broad<br>
`(01:46)` emotion<br>
`(01:47)` was to derive an equation<br>
`(01:52)` for the time evolution of the<br>
`(01:54)` probability density<br>
`(01:56)` itself yeah and that was the master<br>
`(01:58)` equation this master equation is not a<br>
`(02:00)` stochastic<br>
`(02:01)` differential equation is a deterministic<br>
`(02:04)` equation<br>
`(02:05)` but it's typically high dimensional and<br>
`(02:09)` relies as you saw last time on some<br>
`(02:13)` integrations over the possible states<br>
`(02:16)` that you can jump into<br>
`(02:18)` and then for those of you who remained<br>
`(02:21)` for the example<br>
`(02:23)` section last time you would have seen<br>
`(02:26)` that these master equations although<br>
`(02:29)` they look<br>
`(02:30)` pretty complicated can be derived<br>
`(02:32)` phenologically<br>
`(02:34)` phenologically actually<br>
`(02:37)` in most cases in a very simple way yeah<br>
`(02:41)` so these are the two kinds of<br>
`(02:42)` description and why are we not<br>
`(02:44)` completely happy with that<br>
`(02:48)` so there exists approximately<br>
`(02:52)` suppose both in general conditions both<br>
`(02:54)` of these different kinds of equations<br>
`(02:55)` cannot be solved<br>
`(02:57)` there exists approximative methods that<br>
`(03:00)` we discussed last time for example the<br>
`(03:01)` focal plunk equation<br>
`(03:03)` that was an approximation for the master<br>
`(03:06)` equation<br>
`(03:07)` and these appropriate approximative<br>
`(03:09)` methods that work in certain special<br>
`(03:11)` cases<br>
`(03:13)` now the focal planck equation as you<br>
`(03:15)` remember the<br>
`(03:16)` derivation relied on making strong<br>
`(03:19)` assumptions<br>
`(03:20)` on how these jumps in states state space<br>
`(03:24)` look like they're very nicely behave<br>
`(03:26)` these jumps are very small<br>
`(03:28)` and that they effectively rely on very<br>
`(03:32)` large<br>
`(03:32)` system size and<br>
`(03:36)` in other cases there are no<br>
`(03:39)` approximative<br>
`(03:40)` methods at all so what field theory<br>
`(03:44)` does for us is it gives us a flexible<br>
`(03:47)` framework a general<br>
`(03:48)` and flexible framework that allows us to<br>
`(03:51)` describe a large class of stochastic<br>
`(03:54)` systems<br>
`(03:55)` and it is even<br>
`(03:59)` maybe if you remember from statistical<br>
`(04:01)` physics or quantum mechanics<br>
`(04:03)` it's uh so general that you can apply it<br>
`(04:06)` to<br>
`(04:06)` a very diverse set of systems that's<br>
`(04:10)` one thing is for example spatially<br>
`(04:12)` extended systems<br>
`(04:13)` yes you can see on the bottom uh right<br>
`(04:16)` yeah so this is a system where<br>
`(04:20)` the evolution over the spatial<br>
`(04:22)` information<br>
`(04:23)` itself is very important not because you<br>
`(04:26)` see here there's a chemical<br>
`(04:28)` system you see that here structures form<br>
`(04:31)` it's an example of what's called binodal<br>
`(04:33)` decomposition<br>
`(04:35)` now so here the spatial component is<br>
`(04:36)` very important<br>
`(04:38)` and this has to be taken into account<br>
`(04:41)` when you want to understand of course<br>
`(04:43)` collective processes<br>
`(04:45)` another example are non-linearities in<br>
`(04:48)` stochastic differential equations<br>
`(04:51)` now these become especially if they<br>
`(04:53)` affect an oyster and become pretty hard<br>
`(04:55)` very quickly<br>
`(04:56)` and another example is that i would have<br>
`(04:58)` showed you last time<br>
`(05:00)` that field theory that typical<br>
`(05:02)` approximative methods like the focal<br>
`(05:04)` planck<br>
`(05:06)` method or other kinds of expansions<br>
`(05:10)` uh are not very suitable for rare events<br>
`(05:14)` for the tales of probability<br>
`(05:16)` distributions<br>
`(05:17)` so in fields here we have a general<br>
`(05:19)` framework<br>
`(05:20)` of understanding these variables<br>
`(05:24)` and so there has been a lot of work on<br>
`(05:26)` how to make approximations to these<br>
`(05:28)` field theories<br>
`(05:30)` that allow us to understand the tales of<br>
`(05:32)` probability distributions and very often<br>
`(05:34)` these tales<br>
`(05:36)` are pretty important so they are not<br>
`(05:39)` they're rare<br>
`(05:40)` but uh if you think about a nuclear<br>
`(05:44)` reactor or something like this yes these<br>
`(05:46)` rare events are rare<br>
`(05:47)` but you want to know how often they hear<br>
`(05:49)` and there are a few theoretic methods<br>
`(05:51)` that allow you<br>
`(05:52)` to calculate the tails of probability<br>
`(05:54)` distributions<br>
`(05:56)` very nicely so<br>
`(06:00)` this is what we'll do and in this<br>
`(06:02)` lecture<br>

### slide 2

<br>
`(06:03)` i want to show you how we can derive<br>
`(06:07)` a field theory description um<br>
`(06:11)` for the longitudinal equation for<br>
`(06:13)` stochastic differential equations<br>
`(06:15)` we'll be looking at very simple a<br>
`(06:20)` very simple automatic equation that<br>
`(06:22)` doesn't have any<br>
`(06:23)` explicit time derivative that doesn't<br>
`(06:25)` have<br>
`(06:26)` multiplicative noise and we can<br>
`(06:30)` nevertheless in the framework of field<br>
`(06:31)` theory we can<br>
`(06:33)` straightforwardly uh extend<br>
`(06:36)` this methodology to more complicated<br>
`(06:38)` systems so we restrict ourselves<br>
`(06:40)` to this very simple larger equation uh<br>
`(06:43)` with gaussian white noise<br>
`(06:45)` that is as last time uncorrelated<br>
`(06:50)` so if you<br>
`(06:54)` so the first step here is to discretize<br>
`(06:58)` time yeah and uh so we take<br>
`(07:02)` the logical equation and we write it<br>
`(07:03)` down in discrete time<br>
`(07:06)` and uh as you saw uh last time<br>
`(07:09)` uh or in the first of what was the first<br>
`(07:12)` lecture already i saw<br>
`(07:13)` two lectures ago oh wait whatever yeah<br>
`(07:16)` so so no last time last time was the<br>
`(07:18)` catholic processes<br>
`(07:19)` yeah so as you saw last time the way we<br>
`(07:22)` discretize<br>
`(07:24)` stochastic differential equations and i<br>
`(07:27)` showed you that for uh stochastic<br>
`(07:28)` integrals is very important<br>
`(07:32)` yeah and in this case we also have to<br>
`(07:34)` discretize<br>
`(07:35)` our stochastic differential equation in<br>
`(07:37)` a certain way<br>
`(07:39)` which is called the ito discretization<br>
`(07:43)` and but if we do that if we discretize<br>
`(07:47)` our stochastic differential equation in<br>
`(07:49)` this way<br>
`(07:50)` the idea is that in principle we can<br>
`(07:53)` write down<br>
`(07:55)` averages over any<br>
`(07:58)` observable you know that's here on the<br>
`(08:01)` left left hand side by some complicated<br>
`(08:04)` thing that is on the right hand side<br>
`(08:07)` so this what is on the right hand side<br>
`(08:09)` and this equation looks pretty<br>
`(08:10)` complicated but it's not that<br>
`(08:12)` complicated so let's have a look<br>
`(08:14)` at these different terms in the first<br>
`(08:18)` term here<br>
`(08:19)` on the left right hand side the red term<br>
`(08:22)` we just integrate over all possible<br>
`(08:25)` realizations<br>
`(08:27)` that a stochastic trajectory can take<br>
`(08:32)` on the right hand side<br>
`(08:35)` now if you look at the right hand side<br>
`(08:37)` oh there's a delta function missing here<br>
`(08:40)` right at here delta here<br>
`(08:43)` on the right hand side you have this<br>
`(08:45)` delta function<br>
`(08:49)` here you have this delta function and<br>
`(08:52)` this delta function<br>
`(08:54)` just makes sure that whatever we<br>
`(08:56)` integrate here whatever trajectories we<br>
`(08:59)` integrate over<br>
`(09:01)` that they fulfill the discretized<br>
`(09:04)` version<br>
`(09:05)` of the larger equation<br>
`(09:08)` yeah so the delta function is just the<br>
`(09:11)` left-hand side<br>
`(09:12)` minus the right-hand side of this launch<br>
`(09:15)` of our equation<br>
`(09:16)` and if the left-hand side is equal to<br>
`(09:18)` the right-hand side<br>
`(09:20)` then we take that trajectory into<br>
`(09:22)` account<br>
`(09:23)` you know and then sandwiched between<br>
`(09:26)` that we have<br>
`(09:27)` our observable o that is some functional<br>
`(09:31)` of our trajectory x<br>
`(09:34)` now as i say functional so i don't know<br>
`(09:37)` how much uh<br>
`(09:37)` functional analysis all of you had so<br>
`(09:40)` most<br>
`(09:41)` so i would expect that most of you would<br>
`(09:44)` have that<br>
`(09:44)` until the first fourth term<br>
`(09:48)` or so also but just just to make sure a<br>
`(09:51)` functional<br>
`(09:52)` is basically a function that maps um<br>
`(09:56)` that maps this that maps<br>
`(09:59)` this function x uh yes that map<br>
`(10:03)` a function to a real number yeah<br>
`(10:06)` and this is our how we define these<br>
`(10:08)` observables<br>
`(10:09)` now you take a trajectory and you map it<br>
`(10:12)` to them to a number<br>
`(10:16)` okay so this looks very complicated it<br>
`(10:18)` doesn't help us<br>
`(10:19)` anything at all and uh<br>
`(10:22)` one the other step that we need to make<br>
`(10:24)` on the slide is we that we<br>
`(10:26)` introduce some notations here<br>
`(10:29)` and uh of course we don't always want to<br>
`(10:32)` write<br>
`(10:33)` all of these integrals here on the left<br>
`(10:36)` hand side<br>
`(10:37)` we just say we write that in this<br>
`(10:39)` functional form here<br>
`(10:41)` and of course many of you will know that<br>
`(10:43)` this is just<br>
`(10:44)` a functional integral or a path into<br>
`(10:47)` yeah that's how we define it here<br>

### slide 3

<br>
`(10:49)` and now for uh notational convenience<br>
`(10:54)` now we just go to a continuum locate<br>
`(10:56)` notation now we forget that we<br>
`(10:58)` discretize time in the previous step<br>
`(11:01)` and we write the equation back in<br>
`(11:03)` continuous form<br>
`(11:05)` just for the sake of simplicity and we<br>
`(11:07)` define<br>
`(11:08)` some delta functional<br>
`(11:11)` that is just equal to the product over<br>
`(11:14)` all data functions that we had on the<br>
`(11:16)` previous slide<br>
`(11:17)` now if you look here are the product of<br>
`(11:20)` our data functions<br>
`(11:21)` just make sure that you fulfill the<br>
`(11:23)` larger equation really at each time<br>
`(11:25)` point<br>
`(11:27)` and we just define like a super delta<br>
`(11:29)` function or delta functional<br>
`(11:31)` that makes sure that we really satisfy<br>
`(11:33)` the larger equation for each time point<br>
`(11:41)` so now we make a little trick<br>
`(11:45)` now we say we have this delta function<br>
`(11:47)` or this product of delta functions<br>
`(11:50)` and what we say is that in fourier space<br>
`(11:54)` the delta function is represented by a<br>
`(11:58)` plane<br>
`(11:58)` wave yeah so we fully transform the<br>
`(12:02)` delta function<br>
`(12:15)` or a functional is now and<br>
`(12:18)` the fourier transform of the delta<br>
`(12:20)` function<br>
`(12:21)` just becomes delta x dot<br>
`(12:25)` minus f of x minus<br>
`(12:29)` sine because our delta our function<br>
`(12:31)` equation<br>
`(12:33)` is equal to a fury space<br>
`(12:38)` d x tilde<br>
`(12:43)` e to the minus i x to the<br>
`(12:48)` x dot minus<br>
`(12:52)` f of x minus c<br>
`(12:56)` now we now get this variable x tilde<br>
`(13:00)` so this is nothing there's nothing<br>
`(13:01)` happening it's just the definition of<br>
`(13:03)` the forage in the form<br>
`(13:04)` of a delta function and because we have<br>
`(13:08)` this<br>
`(13:08)` product for many delta functions here<br>
`(13:12)` we have the integral here that the path<br>
`(13:15)` integral here will also get a path<br>
`(13:17)` integral<br>
`(13:18)` delta x total you know that's that just<br>
`(13:22)` the definition of the fury transform<br>
`(13:24)` and now we plug this<br>
`(13:28)` in again so<br>
`(13:32)` we obtain from that<br>
`(13:35)` that the expectation value of our<br>
`(13:39)` observable yeah<br>
`(13:43)` taken to the average now this average is<br>
`(13:45)` over the distance<br>
`(13:47)` over over a different voice realizations<br>
`(13:52)` yeah it is equal now we plug that in<br>
`(13:55)` an integral now over<br>
`(13:58)` x and x tilde so it's a path integral<br>
`(14:03)` over x and x tilde so we there's an<br>
`(14:06)` integral<br>
`(14:07)` over all realization of x and all<br>
`(14:10)` realization<br>
`(14:11)` of x2 now so now this x still that pops<br>
`(14:14)` up yeah so we don't really know what it<br>
`(14:15)` is<br>
`(14:16)` but it will hang around and it will show<br>
`(14:18)` you later what it actually mean<br>
`(14:21)` means so we have this fourth integral<br>
`(14:25)` so our observable of x and then<br>
`(14:33)` plugging in e to the minus<br>
`(14:37)` i x tilde<br>
`(14:40)` um sorry<br>
`(14:44)` we've got an integral so we have here a<br>
`(14:46)` little<br>
`(14:47)` integral dt<br>
`(14:52)` and this integral<br>
`(14:56)` we get because we had this<br>
`(15:00)` product over here now so here the<br>
`(15:03)` product<br>
`(15:04)` we had here gives us an integral so our<br>
`(15:07)` sum<br>
`(15:08)` in the exponential so this was<br>
`(15:10)` originally like a product of many<br>
`(15:12)` exponential<br>
`(15:14)` and uh so this is this and then we have<br>
`(15:18)` our<br>
`(15:18)` x tilde x dot minus<br>
`(15:23)` f of x minus x psi<br>
`(15:28)` and then we close the average<br>
`(15:32)` and then we just plug this in yeah we<br>
`(15:34)` can move out<br>
`(15:36)` everything that does not depend on psi<br>
`(15:39)` or the noise<br>
`(15:41)` out of the average because average is<br>
`(15:43)` over the noise<br>
`(15:46)` b x x to the<br>
`(15:51)` power of x right now comes the stuff<br>
`(15:54)` that does not depend<br>
`(15:56)` on x under x i integral<br>
`(16:00)` e t x to the<br>
`(16:04)` x dot minus f of x<br>
`(16:08)` and now we have some<br>
`(16:12)` average over minus i<br>
`(16:15)` dt x tilde<br>
`(16:19)` times psi<br>

### slide 4

<br>
`(16:23)` you know so<br>
`(16:26)` now the question is what is this here<br>
`(16:32)` can we calculate this at the moment we<br>
`(16:34)` cannot do anything with this equation<br>
`(16:36)` with this expression can you can we<br>
`(16:38)` calculate<br>
`(16:40)` this last term that involves a noise<br>
`(16:44)` average<br>
`(16:45)` over e to the minus dt<br>
`(16:49)` and psi now and there's hope that we can<br>
`(16:52)` calculate this because we know what<br>
`(16:54)` psi is now we said that x i<br>
`(16:58)` is a gaussian random variable<br>
`(17:01)` yeah it has follows a normal<br>
`(17:03)` distribution<br>
`(17:04)` it's uncorrelated so we know a lot of<br>
`(17:07)` things about this<br>
`(17:08)` sign and what we do right now<br>
`(17:12)` right because psi is gaussian there's<br>
`(17:14)` also hope that we can actually<br>
`(17:17)` solve or integrate this integral that is<br>
`(17:20)` this average here<br>
`(17:21)` now i'll show you now how this works in<br>
`(17:24)` detail<br>
`(17:25)` yeah so we make use of the definition of<br>
`(17:28)` phi<br>
`(17:30)` so let's see what this second average<br>
`(17:32)` looks like<br>
`(17:34)` now that's o of x<br>
`(17:38)` uh sorry it's not o of x it is<br>
`(17:42)` e to the minus i dt<br>
`(17:47)` integral x of<br>
`(17:50)` sine<br>
`(17:54)` now and this is<br>
`(17:58)` by definition by the definition of the<br>
`(18:00)` average<br>
`(18:03)` is equal to the integral over dxi<br>
`(18:08)` times the probability over the<br>
`(18:11)` probability distribution of<br>
`(18:13)` psi which is a gaussian or a normal<br>
`(18:15)` distribution<br>
`(18:18)` 2 pi a a is the strength of our noise<br>
`(18:23)` e to the minus psi<br>
`(18:26)` squared over 2a<br>
`(18:29)` yeah so this is the probability<br>
`(18:31)` distribution<br>
`(18:33)` and we know that psi is normally<br>
`(18:36)` distributed<br>
`(18:37)` yeah and that's why we have this normal<br>
`(18:40)` distribution here<br>
`(18:42)` at now we multiply this by the thing<br>
`(18:45)` we're averaging over<br>
`(18:48)` yeah e to the minus i<br>
`(18:51)` d t x to the sine<br>
`(18:57)` now so this excuse me yes isn't it<br>
`(19:00)` supposed to be exponential<br>
`(19:02)` plus psi integral delta t whatever<br>
`(19:08)` integral over let me see<br>
`(19:12)` you mean the second integral this one<br>
`(19:13)` here<br>
`(19:16)` yeah okay so this one is that minus or<br>
`(19:18)` plus<br>
`(19:20)` let me just check<br>
`(19:23)` let me check my notes<br>
`(19:27)` okay<br>
`(19:31)` so here we go<br>
`(19:35)` so no there's a minus<br>
`(19:39)` i i wouldn't be able to find him i<br>
`(19:42)` wouldn't be able to find it<br>
`(19:43)` [Music]<br>
`(19:45)` on the previous slide you can go and<br>
`(19:47)` just<br>
`(19:48)` okay so let me see maybe there's a here<br>
`(19:51)` we have the minus<br>
`(19:54)` here we have the minus u of the minus<br>
`(19:57)` here we have the minus and another minus<br>
`(20:00)` yeah you're right<br>
`(20:01)` let me see what's wrong here uh<br>
`(20:04)` okay oh yes okay so here<br>
`(20:12)` i think this minus here is not right<br>
`(20:17)` now that's just the definition here wait<br>
`(20:20)` minus my i don't know<br>
`(20:22)` okay minus minus is plus<br>
`(20:28)` minus minus with plus i think i think<br>
`(20:29)` you're right<br>
`(20:31)` but then here should be a minus so where<br>
`(20:33)` does the<br>
`(20:34)` is there an i squared somewhere<br>
`(20:44)` excuse me i think there should be a<br>
`(20:46)` minus sign<br>

### slide 4

<br>
`(20:47)` um in the first exponential as well in<br>
`(20:50)` the last step on this particular slide<br>
`(20:52)` there are two exponential studies yes<br>
`(20:54)` yes yes yes yes<br>
`(20:56)` that's what i'm wondering about um let<br>
`(20:58)` me see if it's<br>
`(20:59)` actually the final result<br>
`(21:02)` um i x minus minus<br>
`(21:08)` [Music]<br>
`(21:14)` okay so so mike<br>
`(21:17)` let me let me just see<br>
`(21:24)` let me just see<br>
`(21:28)` so let's let's put this minus here in<br>
`(21:30)` brackets<br>
`(21:31)` now so this one minus this should have<br>
`(21:34)` the opposite<br>
`(21:35)` i don't wait with me okay this is the<br>
`(21:37)` minus then<br>
`(21:38)` this should be plus you say<br>
`(21:42)` you know i think i think it i think it<br>
`(21:45)` will come out correctly later<br>
`(21:46)` now let's see how it goes um let's see<br>
`(21:50)` how it goes<br>
`(21:51)` now it makes sense<br>
`(21:56)` now we have to have a gaussian integral<br>
`(22:00)` and that will determine whether what<br>
`(22:04)` we're doing is right<br>
`(22:05)` okay so let's let's go on so this here<br>
`(22:08)` is the integral and now we just<br>
`(22:12)` put everything together and say<br>
`(22:15)` that the sign 1 over<br>
`(22:20)` 2 a e<br>
`(22:24)` minus dt x to the<br>
`(22:28)` psi<br>
`(22:32)` now that's the first one so that would<br>
`(22:34)` be a plus then<br>
`(22:36)` minus i dt x<br>
`(22:40)` to the sine<br>
`(22:43)` now i just i just uh i just combined the<br>
`(22:46)` exponentials<br>
`(22:47)` now thanks for thanks for paying so much<br>
`(22:49)` attention<br>
`(22:51)` um so yeah and this is here<br>
`(22:54)` a gaussian integral and if you don't<br>
`(22:57)` know remember<br>
`(22:58)` the gaussian integrals and you can look<br>
`(23:00)` at the bottom here<br>
`(23:01)` these gaussian intervals are pretty easy<br>
`(23:04)` to solve<br>
`(23:05)` probably most of you have heard of that<br>
`(23:08)` and we can also solve<br>
`(23:10)` this gaussian integral here and what we<br>
`(23:13)` get<br>
`(23:13)` is that this is just e to the a over 2<br>
`(23:18)` dt x to the squared<br>
`(23:23)` yeah because we know yeah and here<br>
`(23:27)` one thing you have to make uh you need<br>
`(23:29)` to remember<br>
`(23:30)` is that this here has eyes in it<br>
`(23:33)` now if you look at this formula at the<br>
`(23:35)` bottom you need to take into account<br>
`(23:36)` that these are complex<br>
`(23:38)` integrals so we can calculate<br>
`(23:42)` this quantity here<br>
`(23:45)` we can calculate this quant this<br>
`(23:46)` quantity here because we know<br>
`(23:49)` how psi looks like and that we integrate<br>
`(23:52)` over the distribution of<br>
`(23:53)` sine of the noise organization and we<br>
`(23:56)` get<br>
`(23:56)` the term that we have here yeah<br>
`(23:59)` and now we already have arrived at the<br>
`(24:02)` famous<br>
`(24:03)` no at least famous for a very small<br>
`(24:05)` number of people<br>

### slide 5

<br>
`(24:06)` and this is the so-called martin citra<br>
`(24:09)` rose johnson they dominicus<br>
`(24:12)` uh functional integral yeah that's what<br>
`(24:14)` you see here<br>
`(24:16)` in the red box now we just now put<br>
`(24:18)` everything together<br>
`(24:19)` here we have our noise here we have<br>
`(24:23)` uh what we had before and here<br>
`(24:28)` is so to say that it's a deterministic<br>
`(24:30)` part that came from the larger equation<br>
`(24:33)` yeah and uh so what this tells us now<br>
`(24:37)` here<br>
`(24:38)` and maybe it looks familiar to some of<br>
`(24:40)` you yet quantum field theory<br>
`(24:42)` this looks very familiar so what we do<br>
`(24:45)` now is<br>
`(24:46)` we want to calculate the average over<br>
`(24:49)` some observable<br>
`(24:52)` we integrate over all possible<br>
`(24:56)` realizations and over all possible<br>
`(24:58)` realizations of some weird quantity<br>
`(25:00)` x tilde so we got a second field here<br>
`(25:05)` and weight the contributions of<br>
`(25:08)` different trajectories<br>
`(25:11)` by this exponential factor here<br>
`(25:14)` now and this exponential factor looks<br>
`(25:16)` very much like what you know from<br>
`(25:19)` other field theories like quantum field<br>
`(25:21)` theory and this is why this is very<br>
`(25:23)` often called<br>
`(25:24)` an action<br>
`(25:28)` now that's the martin sutra rose or ms<br>
`(25:31)` rjd functional<br>
`(25:34)` integral that allows us to really write<br>
`(25:37)` a field theory<br>
`(25:39)` for stochastic processes<br>
`(25:42)` now so here our axes are not fields yet<br>
`(25:45)` now they're trajectories they don't have<br>
`(25:47)` a space component now they don't have<br>
`(25:49)` spatial dimensions<br>
`(25:51)` but as you can see later the structure<br>
`(25:53)` of a real spatial<br>
`(25:55)` the the integrals they will look very<br>
`(25:58)` similar<br>
`(26:00)` now we can also rewrite this a little<br>
`(26:04)` bit here and look at specific<br>
`(26:05)` trajectories and then we can look for<br>
`(26:09)` example at a special case<br>
`(26:11)` where it is observable is just<br>
`(26:14)` the propagator here or this will<br>
`(26:16)` propagate as the probability<br>
`(26:18)` that we end up at some state x at a time<br>
`(26:22)` t<br>
`(26:23)` if we start it add some x naught<br>
`(26:27)` at a time t naught you know and we<br>
`(26:30)` obtain this<br>
`(26:31)` not by just requiring that this<br>
`(26:33)` observable is a delta function<br>
`(26:36)` where uh we say that the x the specific<br>
`(26:39)` time<br>
`(26:40)` t at a time t needs to be equal<br>
`(26:43)` to the x that we give to the probability<br>
`(26:46)` distribution here<br>
`(26:50)` and then we plug that in and<br>
`(26:53)` what we now need to say is that we only<br>
`(26:56)` integrate<br>
`(26:57)` over trajectories that actually started<br>
`(27:00)` it's not an end<br>
`(27:01)` and x at a given times now that's that's<br>
`(27:04)` what we have to take to account for in<br>
`(27:06)` the boundaries and the bounds of the<br>
`(27:07)` integrals<br>
`(27:08)` yeah and then we get this form here<br>
`(27:13)` now that looks very similar and that's a<br>
`(27:16)` different representation if you remember<br>
`(27:18)` last time we had the<br>
`(27:19)` koi maguro of uh chap and komogorov<br>
`(27:21)` equation<br>
`(27:22)` it was an equation for the same quantity<br>
`(27:25)` and the idea was a little bit similar<br>
`(27:27)` in this technical mcgovern<br>
`(27:30)` equation we had the same spirit<br>
`(27:33)` and we looked at different sums of<br>
`(27:35)` different paths<br>
`(27:37)` um a process could take to go from x<br>
`(27:40)` naught to x<br>
`(27:41)` and here we do the same thing in a more<br>
`(27:43)` fancy way<br>
`(27:49)` just to reflect on this a little bit<br>
`(27:51)` more<br>
`(27:52)` so what happened now so we started<br>
`(27:55)` here with<br>
`(27:59)` a longer equation we discretized it<br>
`(28:03)` and if you remember uh quantum fields<br>
`(28:06)` theory that's also the step that you do<br>
`(28:08)` there<br>
`(28:08)` you discretize time into small intervals<br>
`(28:12)` as the first step if you derive<br>
`(28:13)` a quantum fluid theory and then<br>
`(28:17)` we wrote expectation values of some<br>
`(28:19)` observables<br>
`(28:20)` formally in a way that involved<br>
`(28:23)` integrals of<br>
`(28:23)` all possible trajectories and the<br>
`(28:25)` resultant trajectories<br>
`(28:27)` filtered four trajectories that solve<br>
`(28:30)` the launch of a creation<br>
`(28:32)` now that was to say self uh<br>
`(28:35)` circular starting point and in the next<br>
`(28:39)` uh step we then got this field<br>
`(28:42)` side tilde now that we still don't know<br>
`(28:44)` what it is exactly about<br>
`(28:46)` now we got that from the fourier<br>
`(28:47)` transform of the delta function<br>
`(28:52)` and now now we have two fields we<br>
`(28:54)` integrate over two fields<br>
`(28:56)` x and x x tilde and<br>
`(28:59)` in the end we managed to integrate out<br>
`(29:03)` the noise so what we have here<br>
`(29:07)` now is something that does not depend on<br>
`(29:09)` the sign anymore<br>
`(29:11)` it's a deterministic<br>
`(29:14)` equation and deterministic integral so<br>
`(29:17)` somehow<br>
`(29:18)` our noise was observed observed absorbed<br>
`(29:23)` into a new field a new fluctuating field<br>
`(29:28)` x tilde yeah and that's how<br>
`(29:31)` it very often goes now that you<br>
`(29:34)` make a field theory and what you gain is<br>
`(29:37)` you get a nice nice integral but you<br>
`(29:39)` have to pay for<br>
`(29:40)` it by having additional fields conjugate<br>
`(29:43)` fields<br>
`(29:44)` that you have to integrate over and the<br>
`(29:47)` same is true here<br>
`(29:48)` and i'll show you later what these x<br>
`(29:50)` tilde actually mean before i do that let<br>

### slide 6

<br>
`(29:55)` me just mention so so now we have a few<br>
`(29:56)` theory i have a path integral and these<br>
`(29:59)` path integrals are very useful<br>
`(30:01)` because we can make use of a lot of<br>
`(30:03)` tools<br>
`(30:04)` from other field fields from quantum<br>
`(30:06)` field theory<br>
`(30:08)` renormalization perturbation theory and<br>
`(30:10)` so we can<br>
`(30:11)` make use of these tools very powerful<br>
`(30:14)` frameworks developed in the last 70<br>
`(30:18)` years or so<br>
`(30:20)` we can make use of these frameworks and<br>
`(30:21)` apply them to these<br>
`(30:23)` few theories for stochastic processes<br>
`(30:27)` and one of the things that we can do is<br>
`(30:29)` we can<br>
`(30:30)` define a so-called generating functional<br>
`(30:35)` that's maybe something that you already<br>
`(30:36)` know from other field theories<br>
`(30:38)` so what you do is you add some auxiliary<br>
`(30:42)` fields<br>
`(30:43)` external fields h and h<br>
`(30:46)` tilde and these fields cuddle<br>
`(30:51)` to x and x tilde the accelerations<br>
`(30:55)` respectively<br>
`(30:57)` and what is this is then the generating<br>
`(31:00)` function<br>
`(31:01)` and of course we know that these fields<br>
`(31:04)` don't really exist<br>
`(31:05)` now we just added them and the reason<br>
`(31:08)` why we added them<br>
`(31:10)` is that if we take derivatives<br>
`(31:13)` with respect to these fields h or this<br>
`(31:16)` external<br>
`(31:17)` forces or external fields h here<br>
`(31:21)` and here what will happen is that each<br>
`(31:24)` time<br>
`(31:25)` because this is an in exponential<br>
`(31:28)` the x<br>
`(31:31)` let or just draw that now the x<br>
`(31:36)` or the x tilde<br>
`(31:40)` will go down here<br>
`(31:44)` yeah and if we do that if we take these<br>
`(31:46)` derivatives<br>
`(31:48)` you know so we can therefore get the<br>
`(31:52)` expectation values of combinations of<br>
`(31:56)` the x<br>
`(31:56)` and x tildes just by differentiating<br>
`(31:59)` this<br>
`(32:01)` generating functional with respect to<br>
`(32:04)` these<br>
`(32:05)` weird virtual fields<br>
`(32:08)` yeah and when we've done that we have to<br>
`(32:12)` remove these fields again so we have to<br>
`(32:14)` set them back to zero<br>
`(32:15)` now for example if you want to have the<br>
`(32:17)` correlation the autocorrelation function<br>
`(32:19)` so how much<br>
`(32:21)` is the process at a time t correlated to<br>
`(32:24)` the state at a time t<br>
`(32:25)` prime yeah then we<br>
`(32:28)` differentiate and we<br>
`(32:32)` take the derivative first with respect<br>
`(32:34)` to<br>
`(32:35)` with respect to h at a certain time t<br>
`(32:39)` yeah and then we get one of these axes<br>
`(32:42)` here and then we take the derivative<br>
`(32:44)` with uh to h at<br>
`(32:48)` a time a different time t prime and then<br>
`(32:50)` we get the field again<br>
`(32:52)` at a different time here<br>
`(32:55)` yeah and these are of course functional<br>
`(32:57)` derivatives now that was<br>
`(32:59)` uh functional calculus if you haven't<br>
`(33:01)` done that<br>
`(33:02)` it's uh for these what you what you do<br>
`(33:04)` is you<br>
`(33:05)` look at the change of a functional<br>
`(33:08)` now for example this here is a<br>
`(33:10)` functional<br>
`(33:12)` we look at the change of a functional<br>
`(33:15)` with respect to small<br>
`(33:16)` changes of its argument also you have a<br>
`(33:20)` look at<br>
`(33:20)` perturbations in age and h tilde<br>
`(33:24)` around some value yeah and then you<br>
`(33:28)` see how your function changes that's<br>
`(33:30)` called a functional derivative<br>
`(33:32)` and if you do that you get very<br>
`(33:34)` conveniently these pre-factors here<br>
`(33:39)` right here in front of the action and if<br>
`(33:42)` you look at<br>
`(33:43)` the definition here this is just what<br>
`(33:46)` gives us our observable<br>
`(33:48)` as for example if our observable is x<br>
`(33:52)` that we just take the derivative once<br>
`(33:55)` we get an x here yeah<br>
`(33:58)` and if we have the x here we have the<br>
`(34:01)` first moment so the mean<br>
`(34:03)` of x the average of x if we take the<br>
`(34:06)` derivative twice<br>
`(34:07)` at different times then we get a<br>
`(34:09)` correlation here on the left-hand side<br>
`(34:13)` so this is a very convenient tool and as<br>
`(34:15)` i said<br>
`(34:16)` if you want to have a correlation<br>
`(34:18)` function for example we take the<br>
`(34:19)` derivative<br>
`(34:20)` twice and you must always remember to<br>
`(34:23)` set<br>
`(34:23)` these fields to zero again it's actually<br>
`(34:26)` the same approach as you do in the<br>
`(34:28)` quantity<br>
`(34:29)` and classical field theory the<br>
`(34:31)` equilibrium equilibrium field t<br>
`(34:37)` okay so now what is this x<br>
`(34:40)` of t that's just a remark so i'm not<br>
`(34:42)` doing the calculations like<br>

### slide 7

<br>
`(34:44)` what is this x tilde of t that we get<br>
`(34:48)` got in this process<br>
`(34:52)` there are different uh<br>
`(34:55)` c theories for stochastic processes and<br>
`(34:57)` for master equations<br>
`(34:58)` and you always get some kind of<br>
`(35:01)` auxiliary<br>
`(35:02)` field some some conjugate field that you<br>
`(35:05)` have to pay for<br>
`(35:07)` and uh this x tilde from here from here<br>
`(35:10)` you can<br>
`(35:12)` get an intuition about that i'm not<br>
`(35:14)` super rigorous but you can get<br>
`(35:16)` your intuition about this if you write<br>
`(35:18)` down the master equation<br>
`(35:20)` sorry the larger equation with respect<br>
`(35:24)` and add some external source<br>
`(35:27)` capital h of t<br>
`(35:32)` you know and if you add this external<br>
`(35:34)` force capital h<br>
`(35:36)` of t now some temporally fluctuating<br>
`(35:39)` force<br>
`(35:40)` that doesn't depend on x itself<br>
`(35:43)` and you plug that in into this martin<br>
`(35:46)` sergio rose<br>
`(35:47)` functional integral or martin citra ruse<br>
`(35:50)` johnson did you limit it to minikit<br>
`(35:54)` then you see a formal analogy that if<br>
`(35:57)` you<br>
`(35:57)` that this you get a term that looks like<br>
`(36:00)` h tilde<br>
`(36:04)` if you define this to be minus i this<br>
`(36:07)` external field<br>
`(36:09)` yeah and now we can see what happens<br>
`(36:14)` to x what is the effect of this external<br>
`(36:17)` field<br>
`(36:19)` h of t on x so there's a little bit in<br>
`(36:22)` an<br>
`(36:23)` analogy already here now so here on the<br>
`(36:25)` left hand side it has something to do<br>
`(36:27)` with this uh external field from the<br>
`(36:31)` generating functional that couples to x<br>
`(36:33)` tilde<br>
`(36:34)` now let's see what this does to x to the<br>
`(36:37)` actual stochastic process<br>
`(36:39)` now to this end we calculate a response<br>
`(36:43)` function<br>
`(36:43)` and this response function is just the<br>
`(36:47)` change<br>
`(36:48)` in the average of f x with respect<br>
`(36:52)` to changes in this external field<br>
`(36:55)` that's called the response so how does<br>
`(36:56)` the system respond<br>
`(36:58)` to changes in this external field<br>
`(37:01)` yeah and so as you remember the average<br>
`(37:05)` here we just get by<br>
`(37:08)` integrating uh by by taking this for<br>
`(37:12)` this this generating functional<br>
`(37:15)` and taking the derivative with respect<br>
`(37:17)` to h<br>
`(37:18)` once so that's the first moment<br>
`(37:22)` and because of this equality here<br>
`(37:27)` now we see that this year<br>
`(37:30)` this response function is we also get<br>
`(37:33)` that<br>
`(37:33)` if we take the derivative with respect<br>
`(37:36)` to h<br>
`(37:37)` and then h tilde at a certain time<br>
`(37:41)` t let me see let me just say<br>
`(37:45)` here that's the tilde<br>
`(37:51)` yeah and this here what this is<br>
`(37:59)` as on the last slide is the correlation<br>
`(38:02)` between<br>
`(38:02)` x of t and x tilde of t<br>
`(38:06)` now somehow the response of the system<br>
`(38:10)` with respect to an external force<br>
`(38:13)` or an infinitely miserable external<br>
`(38:16)` force<br>
`(38:17)` is given by how the x total<br>
`(38:21)` couples to x<br>
`(38:24)` so it describes the activity or is<br>
`(38:27)` related<br>
`(38:28)` to an infinitesimal response<br>
`(38:32)` of x of the field x with respect<br>
`(38:35)` to a small perturbation and that's why<br>
`(38:39)` this field x tilde is also called the<br>
`(38:41)` response field<br>
`(38:44)` now there's just a little bit of<br>
`(38:46)` intuition and very often this these<br>
`(38:48)` conjugate variables somehow in some way<br>
`(38:51)` encode the noise<br>
`(38:56)` now i have an example uh let me just<br>
`(38:59)` check the time whether we do it now or<br>
`(39:01)` at the end of the lecture<br>
`(39:05)` let's do it at the end of the lecture<br>
`(39:06)` again not this example for those of you<br>
`(39:09)` or who<br>
`(39:10)` heard a few theory course last year uh<br>
`(39:13)` there were no<br>
`(39:14)` examples so i'll leave that to the to<br>
`(39:16)` the end of the lecture that<br>
`(39:17)` people can dial out uh if they're tired<br>

### slide 9

<br>
`(39:24)` now i want to just give you a second<br>
`(39:26)` remark<br>
`(39:28)` so we are now in the framework of<br>
`(39:29)` physicians<br>
`(39:31)` and in field theory now if you remember<br>
`(39:34)` we can have different formulations of<br>
`(39:36)` field theories otherwise the lagrangian<br>
`(39:39)` field theory and the hamiltonian field<br>
`(39:42)` and we can translate these two into each<br>
`(39:45)` other<br>
`(39:45)` and we can do the same things here for<br>
`(39:49)` the non-equilibrium for the stochastic<br>
`(39:51)` process<br>
`(39:53)` yeah and it's also just a remark no it's<br>
`(39:56)` not<br>
`(39:57)` so important for the rest of the lecture<br>
`(40:00)` but you can formally define<br>
`(40:03)` new variables q and<br>
`(40:07)` p by these relations here<br>
`(40:10)` and then this probability will take the<br>
`(40:14)` form<br>
`(40:14)` that i wrote down here now so this<br>
`(40:18)` has formally the form of a hamiltonian<br>
`(40:22)` action oh or having a hamiltonian theory<br>
`(40:25)` so we have<br>
`(40:26)` p times q dot minus<br>
`(40:29)` some hamiltonian and this hamiltonian<br>
`(40:32)` is given by this term here this looks a<br>
`(40:35)` little bit like a kinetic energy so it's<br>
`(40:38)` just<br>
`(40:38)` just just saying that we can write by<br>
`(40:41)` variable transformation we can write<br>
`(40:42)` these<br>
`(40:43)` field theories uh then quite analogously<br>
`(40:47)` to feed theories that we already know<br>
`(40:51)` and we can even go one step further<br>
`(40:55)` now we can take this here and integrate<br>
`(40:58)` out the piece<br>
`(40:59)` now because it's just gradually<br>
`(41:01)` quadratic in p<br>
`(41:03)` so these are just essentially gaussian<br>
`(41:05)` integrals that you can integrate over<br>
`(41:06)` them<br>
`(41:07)` and just to tell you the results that we<br>
`(41:09)` then get<br>
`(41:10)` a field theory that looks like a<br>
`(41:13)` lagrangian field theory<br>
`(41:16)` now we have a lagrangian that depends on<br>
`(41:17)` q and the<br>
`(41:19)` derivative of q with respect to time<br>
`(41:22)` and if you then look at the analogy<br>
`(41:26)` at this hammer at this land range here<br>
`(41:28)` then<br>
`(41:29)` this looks like it describes some kind<br>
`(41:31)` of particle<br>
`(41:32)` with that has some mass one over a uh<br>
`(41:35)` that lays<br>
`(41:36)` like in a potential that happens that's<br>
`(41:38)` coupled to some<br>
`(41:39)` q dot here and uh we have now here<br>
`(41:43)` the quadratic potential of laughter now<br>
`(41:46)` so now these analogies they're not very<br>
`(41:48)` helpful yeah they don't tell you<br>
`(41:49)` anything<br>
`(41:50)` uh these hamiltonians that you get here<br>
`(41:53)` uh<br>
`(41:53)` they're not comparable to hamiltonians<br>
`(41:55)` that you get important systems<br>
`(41:57)` for example these hamiltonians they're<br>
`(42:01)` not emission quantities<br>
`(42:05)` for quantum physicists<br>
`(42:10)` and just to say that they're different<br>
`(42:11)` ways of formulating these<br>
`(42:13)` theories that you get by variable<br>
`(42:16)` transformations<br>
`(42:17)` uh this second equation here has a name<br>
`(42:19)` that's the own sagar<br>
`(42:21)` mac look functional you know and like<br>
`(42:24)` you will<br>
`(42:25)` pop up these these these kind of<br>
`(42:27)` functional<br>
`(42:28)` um pop up in papers if you read papers<br>
`(42:31)` that<br>
`(42:32)` they they pop up in different ways but<br>
`(42:34)` in the end<br>
`(42:35)` the same uh um<br>
`(42:40)` implementations as a few implementations<br>
`(42:43)` of the same<br>
`(42:44)` stochastic differential equation but<br>
`(42:46)` just reformulations of the same thing<br>

### slide 10

<br>
`(42:52)` okay now<br>
`(42:55)` i told you in the beginning of the<br>
`(42:57)` lecture that um<br>
`(43:01)` i actually what most of the cases<br>
`(43:03)` interested in<br>
`(43:04)` now and what field theories are also<br>
`(43:07)` good for<br>
`(43:08)` are spatially extended systems<br>
`(43:13)` now how do you write down a larger<br>
`(43:16)` equation or a spatially extended system<br>
`(43:19)` now it gets of course a little bit more<br>
`(43:20)` complicated but there's actually a<br>
`(43:22)` classification<br>
`(43:23)` theme for a long general equation that<br>
`(43:27)` describes systems<br>
`(43:28)` that have spatial degrees of freedom<br>
`(43:32)` and this classification scheme you can<br>
`(43:34)` see on the slide<br>
`(43:36)` and so we're looking here at some time<br>
`(43:40)` evolution of some field phi<br>
`(43:43)` at a position x at a time t<br>
`(43:47)` and this time evolution is given by<br>
`(43:49)` different components<br>
`(43:51)` yeah that's r on the right hand sides on<br>
`(43:54)` the very right we have the noise<br>
`(43:56)` as always yeah and this noise<br>
`(44:01)` now has the usual properties the average<br>
`(44:04)` of the noise is zero<br>
`(44:06)` and it also has correlations so how is<br>
`(44:09)` a fluctuation a fluctuating force of<br>
`(44:12)` that xi represents how is that<br>
`(44:15)` correlated between different time points<br>
`(44:18)` and how they correlated between<br>
`(44:20)` different positions<br>
`(44:21)` in space so while the assumption that<br>
`(44:24)` different<br>
`(44:25)` correlations that this noise is<br>
`(44:28)` uncorrelated in time so that<br>
`(44:30)` you don't have memory is something that<br>
`(44:32)` is<br>
`(44:33)` very reasonable and that we that we<br>
`(44:35)` typically make<br>
`(44:37)` it's not so clear that the noise is also<br>
`(44:40)` independent at each position in space<br>
`(44:44)` you know so generally there will be some<br>
`(44:47)` some<br>
`(44:48)` length you perturb the system and then<br>
`(44:49)` you don't perturb a single atom<br>
`(44:51)` yeah but you deter like a small region<br>
`(44:54)` for example<br>
`(44:55)` and then these fluctuating forces are<br>
`(44:58)` correlated<br>
`(45:00)` over small regions and these<br>
`(45:02)` correlations in the spatial<br>
`(45:06)` uh in these spatial systems and the<br>
`(45:09)` fluctuating force that act on these<br>
`(45:11)` systems<br>
`(45:13)` are given by so-called spatial<br>
`(45:15)` correlation<br>
`(45:16)` now that just says how are these<br>
`(45:19)` fluctuating forces<br>
`(45:21)` how are they correlated between two<br>
`(45:24)` given positions<br>
`(45:25)` in space yeah and<br>
`(45:28)` now we have the rest here<br>
`(45:32)` the black parts here<br>
`(45:35)` yeah it's just a fancy way of writing<br>
`(45:38)` down<br>
`(45:39)` the deterministic part of what's<br>
`(45:42)` actually happening<br>
`(45:44)` yeah and it's just a fancy way of<br>
`(45:47)` writing down uh the actual<br>
`(45:50)` uh for example chemical reactions<br>
`(45:53)` that change the value of the field at a<br>
`(45:56)` given position<br>
`(45:58)` yeah and we can formally write down this<br>
`(46:01)` uh this term by saying okay so we have<br>
`(46:04)` some kind of potential<br>
`(46:06)` and the dynamics will go so to some<br>
`(46:09)` minimum<br>
`(46:10)` of this potential not just some some<br>
`(46:13)` equilibrium state<br>
`(46:15)` yeah and then uh we can formally write<br>
`(46:18)` this<br>
`(46:18)` this way here that we have some<br>
`(46:21)` functions and free energy functional<br>
`(46:23)` f that depends on the fields and this is<br>
`(46:26)` given by some input<br>
`(46:28)` space integral uh where we have this<br>
`(46:31)` term here that will flatten<br>
`(46:33)` the field that something like can become<br>
`(46:36)` a diffusion term<br>
`(46:37)` and on the right hand side we have<br>
`(46:40)` something<br>
`(46:41)` that is a potential that describes<br>
`(46:43)` what's actually which where we're going<br>
`(46:44)` to with the field<br>
`(46:46)` now if you have to have heard<br>
`(46:48)` statistical physics<br>
`(46:50)` yeah then uh these will look familiar to<br>
`(46:53)` them<br>
`(46:53)` to you like fight to the force theory<br>
`(46:55)` ginsburg londo and so on<br>
`(46:58)` now there's this red stuff here yeah and<br>
`(47:01)` this red stuff is just a way<br>
`(47:03)` of classifying different kinds of<br>
`(47:06)` systems<br>
`(47:07)` and people distinguish between system<br>
`(47:10)` where the order parameter so our phi<br>
`(47:13)` is not conserved for example in chemical<br>
`(47:16)` systems where you can<br>
`(47:17)` convert one chemical species to another<br>
`(47:20)` chemical species<br>
`(47:21)` yeah and then another chemical species<br>
`(47:23)` and so on then the con<br>
`(47:25)` concentration of one chemical species is<br>
`(47:28)` not<br>
`(47:28)` conserved in the entire system<br>
`(47:32)` yeah and this is what you get if you set<br>
`(47:34)` this exponent to zero<br>
`(47:36)` that means you don't have this laplacian<br>
`(47:38)` the second derivative here<br>
`(47:42)` the other case is when you have<br>
`(47:45)` set this to one here set this n to one<br>
`(47:49)` then this will here be part of<br>
`(47:52)` something like a diffusion term yeah<br>
`(47:55)` this will go into a diffusion term<br>
`(47:57)` and what you uh will then get is uh what<br>
`(48:00)` is<br>
`(48:00)` what what these kind of systems that<br>
`(48:02)` describe are<br>
`(48:04)` situations where the field supply is<br>
`(48:06)` conserved<br>
`(48:07)` now so you remove stuff at one point of<br>
`(48:09)` the system if you remove stuff at one<br>
`(48:11)` point of the system<br>
`(48:12)` it has to pop up in another point<br>
`(48:16)` an example is for example uh if you have<br>
`(48:18)` something like hydrodynamics also where<br>
`(48:20)` you just<br>
`(48:20)` move mars around and uh but it doesn't<br>
`(48:24)` really disappear<br>
`(48:25)` and you just move things around but<br>
`(48:27)` things don't disappear<br>
`(48:28)` that's an example for these kind of<br>
`(48:30)` model b<br>
`(48:32)` systems yeah and<br>
`(48:35)` uh so if you plug these things in so<br>
`(48:37)` typical examples very famous example<br>
`(48:39)` systems also called reaction diffusion<br>
`(48:43)` systems<br>
`(48:44)` now so and the typical reaction<br>
`(48:45)` diffusion equation<br>
`(48:47)` is seen here on the right hand side that<br>
`(48:50)` describes a situation<br>
`(48:52)` where uh the phi if you look here at the<br>
`(48:55)` phi<br>
`(48:56)` now then what happens what this term<br>
`(48:59)` here does<br>
`(49:00)` is a 5 is just a little bit larger than<br>
`(49:03)` 0<br>
`(49:04)` yeah then this term will be positive<br>
`(49:07)` yeah and this this<br>
`(49:10)` this will give to rise an increase in<br>
`(49:12)` the field<br>
`(49:14)` now this term is a diffusion term uh<br>
`(49:17)` that just<br>
`(49:17)` transports information to the set<br>
`(49:19)` between different positions<br>
`(49:21)` in the system and then we have our noise<br>
`(49:24)` and this noise typically has<br>
`(49:26)` prefactors it's multiplicative uh if you<br>
`(49:29)` look for example at biological systems<br>

### slide 11

<br>
`(49:34)` so at the take home message for these<br>
`(49:36)` spatial systems<br>
`(49:38)` now we you can think about okay we just<br>
`(49:40)` add an x variable well what i just said<br>
`(49:42)` is just a complicated way of<br>
`(49:44)` saying okay so we have some x variable<br>
`(49:47)` and some diffusion yeah but everything<br>
`(49:50)` else will look very similar as before<br>
`(49:53)` now and indeed we can follow exactly the<br>
`(49:56)` same steps now<br>
`(49:57)` now we take the long-term equation<br>
`(49:59)` general launch of my equation here<br>
`(50:02)` you know which is this one i do exactly<br>
`(50:05)` the same steps as before<br>
`(50:07)` and now this here would be the first<br>
`(50:10)` step<br>
`(50:13)` now where we have this delta functions<br>
`(50:16)` now now we don't only have a product<br>
`(50:18)` over i<br>
`(50:19)` that is already in the over time that is<br>
`(50:21)` already in this delta function here<br>
`(50:23)` but also over x yeah and then we just<br>
`(50:26)` plug in this<br>
`(50:27)` generalized launch of our equation and<br>
`(50:29)` do the same step<br>
`(50:31)` and then we get the field theory the<br>
`(50:33)` martin citra rose functional<br>
`(50:35)` for the spatially extended system so<br>
`(50:38)` this looks pretty complicated<br>
`(50:40)` but it is actually the same as before<br>
`(50:43)` you know so we have we integrate again<br>
`(50:46)` over the field fine and the response<br>
`(50:50)` field<br>
`(50:50)` file tilde and<br>
`(50:54)` then we sum up different contributions<br>
`(50:59)` to our variable to our observable like<br>
`(51:02)` the second term<br>
`(51:03)` and then as before we wait that<br>
`(51:06)` with some exponential that essentially<br>
`(51:10)` quantifies<br>
`(51:10)` how far we are away from a realistic<br>
`(51:14)` realization of the launching equation<br>
`(51:17)` yeah and here we have<br>
`(51:19)` exactly the same structure as before<br>
`(51:22)` here you have the launch of the equation<br>
`(51:25)` now you see you say that you need to<br>
`(51:27)` solve the deterministic part of the<br>
`(51:29)` moisture equation<br>
`(51:31)` and this was previously just<br>
`(51:34)` x tilde squared i said previously<br>
`(51:40)` this was this term here<br>
`(51:43)` was something like a<br>
`(51:46)` over 2 x to the squared<br>
`(51:50)` well now that looks more complicated<br>
`(51:52)` yeah but it has the same form as if you<br>
`(51:54)` look at this<br>
`(51:56)` you have here your x tilde or phi tilde<br>
`(52:00)` here you have another one that just<br>
`(52:03)` coupled by the correlations in the noise<br>
`(52:07)` uh that is described by this voice<br>
`(52:10)` kernel<br>
`(52:11)` now but the structure is the same as<br>
`(52:14)` before<br>
`(52:15)` yeah and uh so so uh so this is the<br>
`(52:18)` martial citra rose<br>
`(52:20)` functional for the noise for the<br>
`(52:22)` spatially extended system<br>
`(52:25)` yeah and with this uh i'm done with the<br>
`(52:29)` definitions<br>
`(52:29)` and with the actual<br>
`(52:33)` derivation of the field theory now<br>

### slide 8

<br>
`(52:36)` let's see if we can apply it and now i<br>
`(52:39)` go back<br>
`(52:40)` to the example and just see how we're<br>
`(52:43)` doing in time<br>
`(52:47)` okay great i think almost exactly an<br>
`(52:49)` hour<br>
`(52:50)` so if you don't already know all of this<br>
`(52:52)` maybe from last year's lecture<br>
`(52:53)` then uh feel free to feel free for her<br>
`(52:56)` to drop out<br>
`(52:56)` and for the rest i'll go through one<br>
`(52:58)` example<br>
`(53:00)` and i'll double check so if i upload<br>
`(53:02)` when i upload the uh<br>
`(53:04)` the lecture notes i'll try to make sure<br>
`(53:06)` that actually these minus signs<br>
`(53:09)` are correct yeah so so if there was a<br>
`(53:11)` mistake i'll correct it<br>
`(53:12)` in the uploaded version that you find on<br>
`(53:15)` the website<br>
`(53:17)` excuse me yes so<br>
`(53:20)` when you wrote the response function<br>
`(53:23)` there was this i guess heavyside<br>
`(53:28)` function multiplied with<br>
`(53:29)` your autocorrelation so<br>
`(53:33)` does that come up because uh you have<br>
`(53:36)` a kind of the etho formalism<br>
`(53:39)` into your system the point<br>
`(53:44)` the response function if you have a<br>
`(53:46)` perturbation here<br>
`(53:48)` if you perturb at t prime and you look<br>
`(53:50)` at the response at t<br>
`(53:52)` now that's how this response function is<br>
`(53:55)` defined<br>
`(53:56)` answer you should have here that's a d<br>
`(53:58)` prime<br>
`(53:59)` here as you perturb at t prime and you<br>
`(54:02)` look<br>
`(54:03)` at the time t yeah then<br>
`(54:06)` oh the other way around actually the<br>
`(54:08)` answer so then then this<br>
`(54:12)` herbicide function just ensures<br>
`(54:15)` causality<br>
`(54:16)` that you cannot observe the response<br>
`(54:19)` that hap that happens before you could<br>
`(54:20)` do the perturbation before you apply the<br>
`(54:22)` force<br>
`(54:25)` now so that's that's that's the reason<br>
`(54:27)` why you get these tata functions<br>
`(54:30)` okay okay thanks for the question<br>
`(54:35)` let's go then to the<br>
`(54:42)` first example<br>
`(54:46)` here we go yeah and<br>
`(54:49)` uh so let's let's have a look at the<br>
`(54:52)` fields here for a very<br>
`(54:54)` simple example and all like in the<br>
`(54:56)` stochastic processes<br>
`(54:58)` also simple examples quickly become<br>
`(55:04)` complicated<br>
`(55:06)` so let me find the notes<br>
`(55:11)` here we go<br>
`(55:18)` okay we start with a simple<br>
`(55:22)` with probably one of the simplest larger<br>
`(55:24)` way equation uh you can<br>
`(55:26)` imagine and uh because it's so simple<br>
`(55:29)` uh it has a name because it has been<br>
`(55:32)` extensively<br>
`(55:33)` studied and it's called the einstein<br>
`(55:35)` ruling<br>
`(55:36)` process and this process is just given<br>
`(55:40)` by the time<br>
`(55:41)` by the time derivative of x<br>
`(55:45)` dot and this is equal to<br>
`(55:48)` some restoring force all right so plus<br>
`(55:51)` sometimes<br>
`(55:52)` uh some external fluctuating force<br>
`(55:56)` side and as always we have the usual<br>
`(55:59)` conditions that are outside<br>
`(56:00)` very nicely behaved doesn't have a mean<br>
`(56:04)` and it's uncorrelated in time<br>
`(56:08)` so now writing down the margin citra<br>
`(56:12)` rose<br>
`(56:13)` function integral easy because we just<br>
`(56:16)` have to plug in this laundromate<br>
`(56:18)` equation<br>
`(56:19)` so martin<br>
`(56:23)` martin cedar rose johnson the dominicus<br>
`(56:28)` some people say martin said rose i did<br>
`(56:30)` that once and i happened to be in munich<br>
`(56:32)` and then i they were very angry that i<br>
`(56:34)` forgot johnson<br>
`(56:36)` my parents apparently had some<br>
`(56:37)` connections to munich<br>
`(56:40)` and uh now so that's the full<br>
`(56:43)` that that that contains i think<br>
`(56:45)` everybody who contributed<br>
`(56:47)` uh<br>
`(56:52)` reads now so what is the action now just<br>
`(56:56)` i don't write the full integral just<br>
`(56:57)` write the action<br>
`(56:59)` so the action is<br>
`(57:03)` dt i x tilde<br>
`(57:12)` del t x plus alpha x<br>
`(57:19)` now let's make sure that we fulfill the<br>
`(57:21)` login equation<br>
`(57:23)` plus a over 2<br>
`(57:27)` dt<br>
`(57:31)` x tilde now that would be squared<br>
`(57:37)` now we can write down the generating<br>
`(57:39)` function<br>
`(57:41)` generating<br>
`(57:47)` functional yeah and this is just as<br>
`(57:50)` before<br>
`(57:52)` that of h is tilde<br>
`(57:57)` is equal to the integral<br>
`(58:00)` over our two fields function interval of<br>
`(58:02)` the word two fields<br>
`(58:04)` field response field uh<br>
`(58:07)` e to the minus s<br>
`(58:11)` plus dt<br>
`(58:15)` h x so that the external auxiliary field<br>
`(58:19)` that comes to x<br>
`(58:21)` plus an external field that couples<br>
`(58:24)` to x tilde<br>
`(58:28)` yeah and uh just<br>
`(58:31)` just to make sure everybody understands<br>
`(58:33)` now so why do i say that this field<br>
`(58:35)` couples to x<br>
`(58:36)` and x tilde here so these and why are<br>
`(58:38)` these external fields<br>
`(58:40)` provided like this this just follows if<br>
`(58:42)` you write down<br>
`(58:43)` um something like for example the<br>
`(58:45)` ginsburg landlord theory also<br>
`(58:48)` or you look at the icing model now then<br>
`(58:50)` terms like this here<br>
`(58:55)` will tilt the potential in one direction<br>
`(58:59)` yeah and here this tilts the potential<br>
`(59:04)` in the x-direction and this tills the<br>
`(59:06)` potential in the axillary<br>
`(59:07)` direction this tilts it in the x<br>
`(59:10)` direction<br>
`(59:12)` and this tilts it in the x tilde<br>
`(59:14)` direction<br>
`(59:16)` now so this is why we call these<br>
`(59:17)` external fields<br>
`(59:19)` and that they couple to uh<br>
`(59:22)` these fields x and x that's the analogy<br>
`(59:26)` to uh the ginsberg london theory and<br>
`(59:29)` other fields<br>
`(59:32)` okay so let's go this is the<br>
`(59:35)` um functional generating functional<br>
`(59:40)` and now we use that<br>
`(59:44)` integral over dx e to the iq x<br>
`(59:48)` is just delta of q so we use the<br>
`(59:52)` definition of the fourier transform of<br>
`(59:54)` the delta function<br>
`(59:56)` and by doing that we get that<br>
`(60:00)` this functional generative function<br>
`(60:04)` is equal to d of<br>
`(60:07)` x to the e<br>
`(60:11)` to the a over two<br>
`(60:16)` integral dt x to the squared<br>
`(60:22)` plus dt<br>
`(60:26)` our two fields h x<br>
`(60:29)` plus h tilde x<br>
`(60:33)` yeah and now we've got our delta<br>
`(60:37)` function<br>
`(60:39)` i del t minus alpha<br>
`(60:44)` x to the plus h<br>
`(60:53)` now when is this delta function here the<br>
`(60:56)` delta function<br>
`(60:58)` actually non-zero now so the delta<br>
`(61:02)` delta functional<br>
`(61:08)` is non zero<br>
`(61:11)` if our x tilde<br>
`(61:15)` solves this ordinary differential<br>
`(61:18)` equation<br>
`(61:20)` you know that we have here in the delta<br>
`(61:22)` function now we can just write it down<br>
`(61:26)` i times t to infinity<br>
`(61:30)` dt prime e to the minus<br>
`(61:35)` alpha t minus p prime<br>
`(61:39)` h of t prime yeah<br>
`(61:45)` now we substitute that so we saw that we<br>
`(61:48)` already got rid of<br>
`(61:49)` one field here by doing this reverse<br>
`(61:53)` fury transform now we substitute that we<br>
`(61:56)` get<br>
`(61:57)` rid of our second field now we<br>
`(61:59)` substitute<br>
`(62:05)` into that<br>
`(62:11)` and what we get<br>
`(62:14)` is age h tilde<br>
`(62:17)` is equal to and now comes a large<br>
`(62:20)` exponential<br>
`(62:21)` to see how to write that on the screen<br>
`(62:26)` minus integral dt<br>
`(62:30)` integral dt prime the second it comes<br>
`(62:34)` from this x tilde<br>
`(62:35)` and then we have<br>
`(62:39)` a over 2 e to the minus<br>
`(62:42)` alpha t minus t prime<br>
`(62:48)` times h of t<br>
`(62:53)` h of t prime plus<br>
`(62:57)` i theta<br>
`(63:00)` t minus t prime<br>
`(63:03)` e to the minus alpha t<br>
`(63:07)` minus t prime<br>
`(63:10)` times i'm sorry i said it like<br>
`(63:14)` even for the simplest process it gets<br>
`(63:16)` lengthy<br>
`(63:17)` h of t h of t prime<br>
`(63:21)` yeah but what's happening here is<br>
`(63:24)` nothing magical it's just a calculation<br>
`(63:26)` such<br>
`(63:26)` integrals well we substituted that x<br>
`(63:29)` total<br>
`(63:31)` into our generating functional and then<br>
`(63:34)` we collected the terms<br>
`(63:35)` and made sure<br>
`(63:40)` that the right time order<br>
`(63:43)` is given and now we have this generating<br>
`(63:46)` function it looks a little bit<br>
`(63:47)` complicated<br>
`(63:48)` but we can deal with that now so we can<br>
`(63:51)` take<br>
`(63:52)` functional derivatives with this now for<br>
`(63:54)` example to get a correlation function<br>
`(64:02)` and so we have x<br>
`(64:06)` of the x of t prime<br>
`(64:10)` now we take the second<br>
`(64:14)` derivative<br>
`(64:19)` once at time t<br>
`(64:24)` and once at time t prime<br>
`(64:30)` and then we must not forget<br>
`(64:33)` to set the fields equal to zero again<br>
`(64:40)` now and if you look at this equation if<br>
`(64:43)` we do that<br>
`(64:44)` then and do a little bit of calculations<br>
`(64:48)` don't<br>
`(64:48)` get that actually this correlation<br>
`(64:50)` function is<br>
`(64:51)` a over alpha e to the minus alpha<br>
`(64:56)` t minus t prime<br>
`(65:02)` so that's just uh an example yeah so<br>
`(65:05)` these actual calculations<br>
`(65:06)` are a little bit messy but that's not<br>
`(65:09)` just how you use these field theories<br>
`(65:12)` that you have the field theory you write<br>
`(65:14)` down the general functional<br>
`(65:16)` yeah and then you look that you are able<br>
`(65:19)` to<br>
`(65:19)` take these functional derivatives with<br>
`(65:22)` respect to these external fields<br>
`(65:24)` and the rest is then say<br>
`(65:28)` mathematics yeah<br>
`(65:32)` okay great so this was an example and<br>
`(65:35)` from next week<br>
`(65:35)` we'll be a little bit more intuitive<br>
`(65:37)` again now we've covered the technical<br>
`(65:39)` stuff<br>
`(65:40)` uh and we can look into some real uh<br>
`(65:43)` physics<br>
`(65:44)` and physics problems okay see you all<br>
`(65:47)` next week<br>
`(65:48)` bye <br>
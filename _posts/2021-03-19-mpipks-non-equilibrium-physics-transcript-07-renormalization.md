---
layout:      post
title:      ".mpipks-transcript | 07. Renormalization Group"
keywords:   "mpipks-transcript"
excerpt:    "重整化群！冲！"
date:        2021-03-19
categories:  post
milestoneID: 35
---

### introduction

<br>`00:00` to our little uh lecture
<br>`00:03` so meanwhile uh most of my group
<br>`00:07` are in current time and i'm one of the
<br>`00:09` few people left
<br>`00:11` and um and ethan detang who used to join
<br>`00:15` me here in the lecture hall
<br>`00:17` uh has escaped to a safer place
<br>`00:20` and so now uh buddy tang is watching the
<br>`00:24` chat and
<br>`00:25` the participantsness and we'll let you
<br>`00:26` in and
<br>`00:29` moderate a little bit the chat and um
<br>`00:34` so it's a good time actually to be
<br>`00:35` working on some epidemic models that we
<br>`00:37` start
<br>`00:38` that we started working on last time and
<br>`00:42` uh in particular last time

### slide 1

<br>`00:46` we were looking at the simplest possible
<br>`00:49` epidemic model you might think about
<br>`00:52` so let me share the screen just to give
<br>`00:54` you a little bit of an
<br>`00:56` um
<br>`01:01` of reminder
<br>`01:10` okay
<br>`01:32` okay
<br>`01:39` okay here we go so we introduced this
<br>`01:43` little epidemic model where you had
<br>`01:46` two kinds of people infected one
<br>`01:50` and the susceptible ones and the model
<br>`01:53` was very simple so these infected ones
<br>`01:55` could uh meet up with an affected one uh
<br>`01:58` within with a susceptible one
<br>`02:00` that's that maybe they weren't uh to a
<br>`02:01` party or so it just
<br>`02:03` used the same train yeah and then the
<br>`02:05` susceptible one uh
<br>`02:07` got infected and then you have the
<br>`02:11` second process
<br>`02:12` where if you are infected with a certain
<br>`02:15` rate also probability
<br>`02:17` per unit of time you get rid of your
<br>`02:20` disease
<br>`02:21` and you recover and go back to
<br>`02:23` susceptible
<br>`02:25` you know so you're a recovered person
<br>`02:28` so and then we went one step further and
<br>`02:31` we
<br>`02:31` put this very simple model on a lattice
<br>`02:34` in a spatial context
<br>`02:36` the simplest spatial context you can
<br>`02:38` think about is just having
<br>`02:40` lattice in one dimension yeah
<br>`02:43` so suppose that this letter looks a
<br>`02:45` little like the train like a train
<br>`02:47` and uh so on this little letters you
<br>`02:50` react
<br>`02:51` basically with your nearest neighbors if
<br>`02:53` you if you infect somebody
<br>`02:55` you're in fact your nearest neighbor but
<br>`02:57` uh not
<br>`02:58` anybody else yeah and then

### slide 2

<br>`03:02` we saw that such a simple model gave
<br>`03:04` rise
<br>`03:05` uh to rich phenomenology depending on
<br>`03:08` the relation between the rate of
<br>`03:10` infection
<br>`03:11` and the rate of recovery which was set
<br>`03:14` to one
<br>`03:15` now if the infection rate was very large
<br>`03:18` then
<br>`03:18` we got a state where we had a large
<br>`03:22` fraction of individuals constantly
<br>`03:24` carrying the disease
<br>`03:26` and when the rate of infection was very
<br>`03:29` low
<br>`03:30` then we ended up in a stainless
<br>`03:31` so-called absorbing state
<br>`03:33` where the disease got extinct
<br>`03:37` now in between that we found that there
<br>`03:39` is a value of this infection rate
<br>`03:41` where infection and recovery just
<br>`03:43` balance
<br>`03:44` and this state was characterized uh
<br>`03:47` very in a very similar way to the ising
<br>`03:50` model
<br>`03:51` in equilibrium was characterized by
<br>`03:54` scale and variance
<br>`03:55` that means that these correlation
<br>`03:57` lengths that we looked at
<br>`03:59` along the space axis
<br>`04:03` and along the time axis we had two
<br>`04:05` correlation lengths
<br>`04:06` they both diverged that means we had
<br>`04:09` self-similarity
<br>`04:10` in this critical point

### slide 3

<br>`04:15` yeah and then we went on and we derived
<br>`04:17` the launch of the equation
<br>`04:19` and from this launch of an equation we

### slide 4

<br>`04:21` then just wrote down
<br>`04:22` the martin citra rose functional
<br>`04:26` integral and i'll show you that later
<br>`04:28` when we actually used it
<br>`04:30` when we'll actually use it for the
<br>`04:31` realization procedure
<br>`04:33` and for once we once we had written down
<br>`04:36` these actions at the margin et cetera
<br>`04:38` rose function integral
<br>`04:40` of course we can go to free of space and
<br>`04:42` write down
<br>`04:43` this action also in fourier space

### slide 5

<br>`04:47` now that's the formalities yeah
<br>`04:50` that looks pretty complicated now
<br>`04:55` we have a problem right so this looks
<br>`04:57` pretty complicated
<br>`04:59` and uh we have a situation
<br>`05:02` where we have divergences where we our
<br>`05:06` correlation length is infinite infinite
<br>`05:10` and we don't really know how to deal
<br>`05:12` with this infinite correlation

### slide 6

<br>`05:16` and this is exactly the situation where
<br>`05:19` we have developed in the last
<br>`05:21` 70 years or so mathematical techniques
<br>`05:25` originally in
<br>`05:26` quantum field theory that allow us to
<br>`05:29` deal with these
<br>`05:30` divergences with these infinities
<br>`05:33` now we've made two observations here so
<br>`05:36` one is
<br>`05:37` scale scale invariance that i just
<br>`05:38` mentioned yeah scale variance
<br>`05:40` at this critical point there's no
<br>`05:43` distinguished length scale we zoom
<br>`05:45` in and the picture we get is
<br>`05:48` statistically
<br>`05:49` still the same as the original picture
<br>`05:54` the second observation is
<br>`05:57` that so and as a result of the scale
<br>`05:59` invariance we saw that
<br>`06:00` in equilibrium all of these
<br>`06:03` thermodynamic quantities
<br>`06:05` i like the like the free energy
<br>`06:08` the magnetization and icing model obey
<br>`06:10` power laws
<br>`06:12` as you approach the critical point so
<br>`06:14` they diverge with certain power laws
<br>`06:17` and the second observation is
<br>`06:20` that at this critical point
<br>`06:23` our empirical observation is for example
<br>`06:26` in the equilibrium but also in
<br>`06:27` non-equilibrium
<br>`06:29` that there are a lot of different
<br>`06:32` real world systems that are described by
<br>`06:36` the same
<br>`06:38` theory the same simple theory so for
<br>`06:42` example
<br>`06:43` you have the icing more you know the
<br>`06:44` icing model is super simple it's much
<br>`06:46` simpler than actually a real magnet
<br>`06:49` nevertheless the icing motor can predict
<br>`06:52` exponents
<br>`06:54` near the critical point of real magnets
<br>`06:58` also of different materials very nicely
<br>`07:03` and it even the icing model even can
<br>`07:05` predict
<br>`07:07` critical phenomena in completely
<br>`07:09` unrelated systems
<br>`07:12` like phase transitions in water if you
<br>`07:14` put water in a high pressure then you
<br>`07:15` have a phase where you have
<br>`07:17` like a coexistence of water and steam
<br>`07:20` and this you can predict these exponents
<br>`07:22` you can predict with the icing water
<br>`07:24` and this power of such simple models to
<br>`07:28` predict a large
<br>`07:29` range of critical phenomena is called
<br>`07:33` universality and both of these
<br>`07:36` observations
<br>`07:37` are the scale and variance the cell
<br>`07:39` similarity
<br>`07:40` and universality can be systematically
<br>`07:43` started with a renormalization group
<br>`07:46` the first thing you might actually think
<br>`07:47` about okay so why do we need actually
<br>`07:49` something complicated
<br>`07:51` now we just do a naive approach
<br>`07:54` uh similar to the one that we used
<br>`07:57` implicitly in these lectures about
<br>`07:59` pattern formation
<br>`08:00` and non-linear dynamics now what we
<br>`08:03` could do is okay we say okay so we just
<br>`08:06` instantaneously zoom out of the system
<br>`08:09` yeah go to
<br>`08:10` wave vector zero so in finite wavelength
<br>`08:13` you look only at the very large
<br>`08:15` properties
<br>`08:16` and just pretend that we can average
<br>`08:18` over everything we just look at average
<br>`08:20` quantities
<br>`08:21` that's that should be called mean field
<br>`08:23` theory where you pretend
<br>`08:25` that your system the state of the system
<br>`08:28` at a certain
<br>`08:28` site is governed by
<br>`08:32` a field that rises over
<br>`08:35` basically an average over the entire
<br>`08:37` system
<br>`08:38` yeah so this mean field theory where you
<br>`08:41` instantaneously
<br>`08:42` go to the macroscopic scale
<br>`08:46` this doesn't work in others it fails to
<br>`08:49` predict these exponents that we get at a
<br>`08:51` critical point
<br>`08:52` and it also doesn't give any uh reason
<br>`08:55` why we should have universality
<br>`08:59` now renewalization does something very
<br>`09:02` smart now that provides a systematic way
<br>`09:06` of connecting these microscopic degrees
<br>`09:09` of freedom that are described for
<br>`09:10` example by hamiltonian
<br>`09:13` to uh macroscopic descriptions
<br>`09:17` now it does so by taking into account
<br>`09:21` all the intermediary scales between
<br>`09:24` micro
<br>`09:24` the microscopic level and the
<br>`09:26` macroscopic level
<br>`09:28` and as you uh my guess from these
<br>`09:30` critical phenomena if you have scale
<br>`09:32` environments and all
<br>`09:33` scales are equal and equally important
<br>`09:36` this approach where you
<br>`09:38` take into account all of these scales
<br>`09:41` one at a time
<br>`09:43` now going from microscopic to
<br>`09:44` macroscopic which
<br>`09:46` makes much more sense than arbitrarily
<br>`09:48` focusing only on the largest scale as
<br>`09:50` you do in new york theory
<br>`09:54` now so rememberization group the
<br>`09:56` romanization
<br>`09:57` group allows us to go from the
<br>`09:59` microscopic
<br>`10:00` level now that is described by some
<br>`10:03` hamiltonian
<br>`10:04` by some symmetries all the way to the
<br>`10:07` macroscopic
<br>`10:08` level without ever forgetting what is
<br>`10:11` going on
<br>`10:12` in between now that's the power of the
<br>`10:14` renalization group and in this lecture i
<br>`10:16` will show you
<br>`10:18` how this is actually implemented
<br>`10:21` now how we can actually do that
<br>`10:30` okay so there's a little bit of a lot of
<br>`10:33` information i should have split this
<br>`10:34` slide

### slide 7

<br>`10:35` um so
<br>`10:39` so so we are now going to follow this
<br>`10:41` program now going from microscopic
<br>`10:43` to macroscopic one scale
<br>`10:46` one length scale at a time now we're
<br>`10:49` starting with something microscopic that
<br>`10:51` is super complicated don't think about
<br>`10:53` the icing model
<br>`10:54` think about something that has 10 000
<br>`10:57` different couplings or so
<br>`11:00` now we take that model with 10 000
<br>`11:03` different parameters
<br>`11:05` on the microscopic scale so the real
<br>`11:07` physics
<br>`11:08` that's going on on the microscopic scale
<br>`11:10` that's complicated
<br>`11:12` yeah it's much more complicated than the
<br>`11:13` icing model and it just as the disease
<br>`11:16` is much more complicated as the ice i
<br>`11:18` model that i showed you
<br>`11:21` and then we go to larger and larger
<br>`11:24` scales
<br>`11:26` and hope to end up with something that
<br>`11:28` is simpler
<br>`11:30` and less correlated than on the
<br>`11:32` microscopic scale
<br>`11:34` yeah so how do we do that so realization
<br>`11:37` consists of three
<br>`11:38` steps uh the most important step
<br>`11:42` now the the actual uh what's actually
<br>`11:46` underlying renovation
<br>`11:48` is a course grading step now in this
<br>`11:51` course grading step
<br>`11:53` you can think about uh that you
<br>`11:57` unsharpen an image suppose you take a
<br>`11:59` photo
<br>`12:00` and then you can focus you can make the
<br>`12:02` picture
<br>`12:04` uh sharp or less sharp yeah by turning
<br>`12:07` like the lens
<br>`12:08` and the ring on the lens if you still
<br>`12:10` use a rear camera
<br>`12:11` yeah so you can make a job or let's try
<br>`12:13` or think about the microscope
<br>`12:15` you can have to turn some knobs to make
<br>`12:17` the image sharp or not sharp
<br>`12:19` and the first step we
<br>`12:22` cause grain so we cause grain
<br>`12:26` and that means literally that we make
<br>`12:28` the image that we're looking at in the
<br>`12:30` system
<br>`12:31` unsharp so that we that's what we do
<br>`12:35` yeah so we
<br>`12:36` mathematically that means if you uh if
<br>`12:39` you close grain if you make something
<br>`12:41` out sharp unsharp then that means that
<br>`12:43` you integrate out
<br>`12:46` fast fluctuations or short range
<br>`12:48` fluctuations
<br>`12:49` i'll show you on the next slide how this
<br>`12:51` looks like intuitively so first you get
<br>`12:53` rid of
<br>`12:53` all these uh fluctuations that happen on
<br>`12:56` very small length scales
<br>`12:59` and you have to perform an integral to
<br>`13:01` do that
<br>`13:02` and this integral of course is very
<br>`13:05` complicated
<br>`13:06` to calculate now the second state
<br>`13:10` we have a new field yeah
<br>`13:13` now let's say phi average
<br>`13:17` but because we have course grade this
<br>`13:19` new field
<br>`13:21` our new image is blurry but
<br>`13:25` it is also not on the same length scale
<br>`13:27` as before
<br>`13:29` yeah so it's just blurry but what we now
<br>`13:32` have to do
<br>`13:33` is to rescale length
<br>`13:36` to make the structures that we have in
<br>`13:38` this new image
<br>`13:40` similar to the structures that we had in
<br>`13:42` the original image
<br>`13:43` now so that means we need to rescale
<br>`13:45` length scales
<br>`13:48` by a factor of b
<br>`13:52` and the other thing that happens if you
<br>`13:53` make things blurry
<br>`13:55` is that you lose contrast in the image
<br>`13:58` so the image looks a bit dull so we
<br>`14:02` also need to now to increase the
<br>`14:03` contrast again
<br>`14:05` and we do that by rescaling our
<br>`14:09` fields as well so these are the three
<br>`14:12` steps of renormalization as if we first
<br>`14:14` integrate out very short
<br>`14:18` fluctuations happening on the smallest
<br>`14:20` length scales
<br>`14:22` and the second step and the third step
<br>`14:25` make sure that once we have integrated
<br>`14:28` out
<br>`14:29` these uh these short length skills
<br>`14:32` that our new theory that we get is
<br>`14:34` actually comparable
<br>`14:36` to the previous one so we have to reset
<br>`14:39` the length scales and we have to reset
<br>`14:41` the fields the contrast of the field by
<br>`14:44` multiplying them
<br>`14:45` with appropriate numbers

### slide 8

<br>`14:50` so how does that look like so we start
<br>`14:52` with a field file
<br>`14:53` now that has short range fluctuations
<br>`14:56` you know fast fluctuations in space
<br>`14:58` now for example um
<br>`15:02` yeah here these wobbly things yeah these
<br>`15:04` are fast fluctuations
<br>`15:07` but it also has slow fluctuations that
<br>`15:09` would be
<br>`15:11` that would be here a slow fluctuation
<br>`15:15` now you have fluctuations on all
<br>`15:17` different length scales and now
<br>`15:19` we cause grain that means we integrate
<br>`15:21` out
<br>`15:22` these fast fluctuations and what we get
<br>`15:25` is a new field if i uh this phi
<br>`15:29` average here because phi r
<br>`15:33` that is smooth that doesn't have these
<br>`15:35` small
<br>`15:36` wiggles anymore but it is smooth here
<br>`15:41` now so we have course grade the fields
<br>`15:44` and now we have coarse grains the field
<br>`15:46` we reset the length
<br>`15:48` rescale the length scale
<br>`15:51` x prime to make fluctuations on the new
<br>`15:57` field comparable to typical fluctuations
<br>`16:00` on the
<br>`16:00` original field the second step
<br>`16:05` we then renormalize um
<br>`16:08` there's actually no three here because i
<br>`16:11` started
<br>`16:12` i know there is a three okay so uh
<br>`16:16` as a final step and we have to rescale
<br>`16:18` the fields now we have to
<br>`16:20` change the magnitude of the signal here
<br>`16:23` to make it comparable
<br>`16:24` to the original signal over here
<br>`16:28` now this sounds very intuitive
<br>`16:31` and very simple but of course in reality
<br>`16:34` it's quite difficult

### answering a question

<br>`16:39` so let's see how this works uh
<br>`16:42` what's the result so can i have a
<br>`16:45` question here
<br>`16:50` um in the previous slide
<br>`16:54` when we re-normalize uh fi
<br>`16:57` prime we essentially doing it
<br>`17:01` because we want uh whatever abs
<br>`17:04` magnitude or value of phi prime is to
<br>`17:07` equal
<br>`17:08` uh the value of five the original field
<br>`17:11` yes
<br>`17:11` exactly so what we want to do is so so
<br>`17:14` we do this procedure not only once
<br>`17:16` but many times now the next step will do
<br>`17:18` that many times
<br>`17:20` and uh each time we do these three steps
<br>`17:24` we get a new hamiltonian or a new action
<br>`17:28` and this new action will be
<br>`17:31` different to the original action
<br>`17:35` it will be different for trivial reasons
<br>`17:38` namely because once we cause when
<br>`17:41` think about this course grading as an
<br>`17:43` average instead
<br>`17:44` now you have i'll show you later a
<br>`17:47` specific example suppose you average
<br>`17:49` uh in some area here and that's why
<br>`17:52` that's how you smooth
<br>`17:54` yeah when you average you know think
<br>`17:56` about the spin system you average
<br>`17:59` then you don't have plus minus plus one
<br>`18:01` or minus one
<br>`18:02` but the new average field will be plus
<br>`18:04` 0.1
<br>`18:06` and minus 0.1 now just because you
<br>`18:08` averaged
<br>`18:09` over in the field yeah but you don't
<br>`18:11` want the new spins to live in this world
<br>`18:13` of plus
<br>`18:14` 0.1 and minus 0.1 but you'd want them
<br>`18:18` also
<br>`18:18` live on the scale of plus minus 1 just
<br>`18:21` to make the
<br>`18:21` hamiltonians comparable now so this is a
<br>`18:24` trivial effect that you get by course
<br>`18:26` grading that you don't want to have
<br>`18:28` to dominate your results and we need to
<br>`18:31` get rid of that
<br>`18:32` this trivial rescalings of the fields
<br>`18:35` and of the
<br>`18:36` of the um of the length scales just by
<br>`18:39` explicitly taking the step and saying
<br>`18:41` okay
<br>`18:42` now i have co-strained my field now i
<br>`18:45` have to reset the length scales
<br>`18:46` and i have to reset the amplitude of my
<br>`18:49` fields
<br>`18:50` by multiplying these these quantities
<br>`18:53` with appropriate numbers
<br>`18:56` i just want to have comparable things at
<br>`18:58` each step
<br>`19:00` yes thank you so much uh but regarding
<br>`19:03` this particular point
<br>`19:04` you showed in the first slide that phi
<br>`19:07` prime
<br>`19:07` phi is divided by b uh in the
<br>`19:10` in introductory slide remember
<br>`19:12` normalization i couldn't understand that
<br>`19:15` yes here yeah five in the next one
<br>`19:19` five bar by b or um
<br>`19:23` so which which one third point
<br>`19:26` third point yeah that's just a number
<br>`19:28` yeah we don't know this number yet
<br>`19:31` we don't know it yet we can get it by
<br>`19:33` dimensional analysis
<br>`19:34` uh very often um so we don't know this
<br>`19:37` number yet
<br>`19:38` it doesn't the same b okay it's not
<br>`19:42` from one i think it's an s actually
<br>`19:47` so so it doesn't have to be b it depends
<br>`19:50` on the dimensions of your field
<br>`19:53` typically b to the power of something
<br>`19:55` also
<br>`19:56` that doesn't have to be b and it depends
<br>`19:58` on the on the dimensions of your fields
<br>`20:00` here
<br>`20:01` um okay just at this point we just say
<br>`20:03` okay so we have to do something with our
<br>`20:05` fields to make them comparable
<br>`20:08` now think about an average now you can't
<br>`20:10` get average and if you're doing average
<br>`20:12` all the time
<br>`20:13` yeah then your uh the central limited
<br>`20:16` theorem will be that the
<br>`20:17` average like in a disordered system will
<br>`20:20` get very very small
<br>`20:22` yes the variance of this average will
<br>`20:24` get very very small
<br>`20:26` and we don't want this effect to happen
<br>`20:28` because it destroys this basically
<br>`20:30` or if i what we actually want to look at
<br>`20:33` now what we actually want to look at is
<br>`20:34` how does the theory in itself the
<br>`20:36` structure of the theory
<br>`20:38` change as we go through the scale and we
<br>`20:41` don't want to have these effects that
<br>`20:42` come
<br>`20:43` by uh by uh
<br>`20:46` just that we that we can't compare
<br>`20:49` um suppose you compare like uh uh
<br>`20:53` you compare um the velocity of a car
<br>`20:56` you live in the uk also or in the united
<br>`20:57` states and you compare the velocity of
<br>`20:59` the car in miles per hour
<br>`21:01` or in kilometers per hour now you have
<br>`21:04` to you cannot compare that
<br>`21:05` but pure numbers you have to do
<br>`21:07` something you have to be scared by 1.6
<br>`21:09` to make them comparable and here also we
<br>`21:12` go through these scales look
<br>`21:13` like meters uh kilo kilometers miles and
<br>`21:17` so on
<br>`21:18` and to make these things comparable all
<br>`21:20` the different lengths that we have to
<br>`21:21` rescale
<br>`21:22` them all the time yeah just that way
<br>`21:24` that we're all the way talking about
<br>`21:26` um the same thing um
<br>`21:30` so in germany we say we uh you cannot
<br>`21:32` compare apples and oranges
<br>`21:34` different things you have to uh
<br>`21:37` if you compare apple and origins then um
<br>`21:40` then then you're doing something wrong
<br>`21:43` in other words to compare apples
<br>`21:45` to different kinds of apples so to say
<br>`21:48` yes but we always want to talk about
<br>`21:50` apples and not about miles and
<br>`21:52` kilometers now so that's that's the idea
<br>`21:55` about this rescaling step
<br>`21:59` i'll show you later an example where
<br>`22:00` this rescaling step is already implicit
<br>`22:02` of course you can choose this course
<br>`22:06` grading step in a way
<br>`22:07` that it doesn't change the magnitude of
<br>`22:10` the field
<br>`22:12` yeah so that you can choose the course
<br>`22:14` grading step in a way here this one
<br>`22:16` in a way that it doesn't change the
<br>`22:18` magnitude of this field and then you
<br>`22:19` don't have to do this renormalization
<br>`22:21` step
<br>`22:24` now but the principle you will have to
<br>`22:26` do that
<br>`22:28` okay so now we have these three points
<br>`22:31` now we rescale uh we of course grain

### slide 9

<br>`22:35` rescale and renormalize and once we do
<br>`22:39` that
<br>`22:39` our action or our equilibrium or
<br>`22:41` hamiltonian
<br>`22:43` will become a new action
<br>`22:48` now s prime and say we
<br>`22:52` did this rescaling on a very small
<br>`22:54` length scale
<br>`22:55` dl now this s prime
<br>`23:00` is then given by some operator r
<br>`23:03` of s and if we do that repeatedly
<br>`23:08` you know so what we then get is a
<br>`23:11` remoralization group flow our g
<br>`23:13` flow and that's basically
<br>`23:17` the differential equation for the action
<br>`23:21` yeah the s over the l
<br>`23:26` is then something like this r
<br>`23:29` of s so we normalize one step further
<br>`23:33` minus the previous step
<br>`23:38` you know so we change we do these three
<br>`23:41` steps
<br>`23:41` just a little bit not just and we call
<br>`23:44` square
<br>`23:45` we integrate out a very small additional
<br>`23:48` scale
<br>`23:50` yeah and our action is then different on
<br>`23:53` the next scale
<br>`23:54` of course we assume that this is somehow
<br>`23:55` continuous and well behaved
<br>`23:58` and then we'll have a flow equation
<br>`24:01` of our action and of course in reality
<br>`24:04` this will not be a flow equation of our
<br>`24:06` action
<br>`24:06` but of the parameters that define our
<br>`24:09` action
<br>`24:10` now suppose so how does it look like
<br>`24:18` now so here is in some space of all
<br>`24:21` possible actions
<br>`24:23` of some parameters p1
<br>`24:27` p2 p3
<br>`24:32` now and this action now think about the
<br>`24:34` uh
<br>`24:35` think about our non-linear dynamics or
<br>`24:37` dynamical systems lecture
<br>`24:39` what we can this is this is a
<br>`24:41` differential equation here
<br>`24:44` it looks complicated but this is a
<br>`24:46` differential equation it tells you
<br>`24:47` how the parameters of our action
<br>`24:51` change as we cause gradients we do this
<br>`24:54` renormalization procedure
<br>`24:57` now and this gives us a differential
<br>`24:59` equation
<br>`25:01` and if you have a differential equation
<br>`25:02` that will be highly non-linear of course
<br>`25:05` now we can do the same thing as we did
<br>`25:07` in this lecture or nonlinear system we
<br>`25:09` can
<br>`25:10` derive a phase portrait now in the space
<br>`25:12` of all possible actions
<br>`25:14` of all possible models where does this
<br>`25:17` minimalization group
<br>`25:18` group flow carry us
<br>`25:22` so let's start with a very simple
<br>`25:27` line
<br>`25:31` that's the line in the space of all
<br>`25:33` possible models
<br>`25:34` now this is the line of models
<br>`25:37` that actually describe our physical
<br>`25:39` systems
<br>`25:40` now think about different combinations
<br>`25:42` of temperature
<br>`25:43` and magnetic fields in the icing model
<br>`25:48` now so this is this is where this model
<br>`25:50` lives in this space
<br>`25:52` now if we take the right parameter
<br>`25:55` combinations
<br>`25:58` we will be at some critical point
<br>`26:06` yeah so there's no flow yet now so this
<br>`26:09` is just
<br>`26:10` uh the the the the range of different
<br>`26:13` models that we can have for example in
<br>`26:15` eisenhower that correspond to some real
<br>`26:17` physical system
<br>`26:18` but there of course there are many other
<br>`26:20` model in the models in this space
<br>`26:22` that don't describe our physical system
<br>`26:24` now they don't describe a magnet but
<br>`26:26` something else or that there are not
<br>`26:28` given by a simple hamiltonian with
<br>`26:29` nearest neighbors
<br>`26:30` interactions but by something that has
<br>`26:33` long-range interactions or something
<br>`26:35` very weird
<br>`26:36` now there's a space of all possible
<br>`26:37` models is very large
<br>`26:40` now we have this critical point and
<br>`26:43` other models in this space also have
<br>`26:46` critical points
<br>`26:47` now and these critical points live on a
<br>`26:51` manifold
<br>`26:58` now they leave on a manifold you know
<br>`27:01` that is the critical manifold
<br>`27:09` you know so that's all the points of
<br>`27:11` this critical manifolds are critical
<br>`27:13` points
<br>`27:14` of some actions
<br>`27:17` and our action our critical point of our
<br>`27:20` action
<br>`27:21` is also on this manifold but all
<br>`27:24` other points of this manifolds are also
<br>`27:26` some critical points of some other
<br>`27:29` actions so
<br>`27:33` what happens now now
<br>`27:37` we are close to the critical point let's
<br>`27:39` say
<br>`27:40` we're here now very close to the
<br>`27:44` critical point
<br>`27:46` and now we really normalize
<br>`27:50` we go through we make this procedure of
<br>`27:53` renormalizing
<br>`27:54` the core straining going to larger and
<br>`27:56` larger scales and rescaling our fields
<br>`27:59` and lengths
<br>`28:00` and then our anatomy or our action will
<br>`28:03` change
<br>`28:04` so it will flow in this space
<br>`28:07` in some direction
<br>`28:11` so where does it flow to in the
<br>`28:13` non-dynamics lecture
<br>`28:16` we've seen that what determines such
<br>`28:18` dynamical systems
<br>`28:20` are fixed points and
<br>`28:24` what you typically have to assume in the
<br>`28:25` real normalization group theory
<br>`28:28` that there is some fixed point
<br>`28:31` on this critical manifold yeah
<br>`28:36` the fixed point of the realization would
<br>`28:39` flow
<br>`28:40` on this critical manifold
<br>`28:44` and now what happens with our flow
<br>`28:50` of course we will go to this fixed point
<br>`28:55` and then we might go away again
<br>`28:59` now the sixth point the fixed points
<br>`29:02` like in the dynamic resistance lectures
<br>`29:04` determine the flow of our dynamical
<br>`29:07` system
<br>`29:09` now what is this fixed point here this
<br>`29:11` fixed point is not the critical point
<br>`29:14` it's the critical point of some other
<br>`29:16` model
<br>`29:18` but this critical point here
<br>`29:23` has stability yeah just like in normal
<br>`29:25` domains so this is non-linear dynamics
<br>`29:27` here
<br>`29:28` so it's very often exactly what we did
<br>`29:30` in this lectures before
<br>`29:31` so we asked what is the flow now we ask
<br>`29:33` them to ask about the stability
<br>`29:35` of this fixed point now so this fixed
<br>`29:39` point
<br>`29:40` has stable directions now you perturb
<br>`29:44` and you get pushed out and unstable
<br>`29:46` directions
<br>`29:48` yeah typically or by definition
<br>`29:52` the directions on the critical manifolds
<br>`29:55` are stable now that's how this manifold
<br>`29:59` is actually defined
<br>`30:00` you can and there's a theory and only
<br>`30:02` resistance
<br>`30:04` that tells you that and there are also
<br>`30:07` other directions
<br>`30:09` that are not stable now let's have them
<br>`30:12` in green
<br>`30:14` for example the way i drew this these
<br>`30:17` are the ones
<br>`30:19` in this direction
<br>`30:26` so this determines the stability of the
<br>`30:28` flow of our fix
<br>`30:29` of our our system and if we have only
<br>`30:32` one fixed point this one fixed point
<br>`30:35` will tell us what happens to the flow of
<br>`30:37` our system just like in nonlinear
<br>`30:39` dynamics
<br>`30:40` lecture okay so
<br>`30:43` now we re-normalize
<br>`30:46` it because we didn't start exactly at
<br>`30:48` the critical point we stay in the
<br>`30:50` vicinity of this manifold here
<br>`30:52` here and this critic this fixed point of
<br>`30:55` the flow will do
<br>`30:56` something to us no it will push us away
<br>`30:59` or will attract us and now you can
<br>`31:04` do the same thing that you do in
<br>`31:05` learning your dynamics namely you linear
<br>`31:07` wise
<br>`31:08` around this fixed point so we say that
<br>`31:11` our action
<br>`31:13` [Music]
<br>`31:16` called linear stability
<br>`31:21` you linearize around this fixed point so
<br>`31:24` you say
<br>`31:25` that our action is equal to the action
<br>`31:29` at this fixed point
<br>`31:32` plus sum over different
<br>`31:35` directions i who operate is i
<br>`31:39` h i
<br>`31:45` times b to the power of lambda i
<br>`31:52` times
<br>`31:56` q i yeah so this here are
<br>`32:01` these two eyes are the eigen directions
<br>`32:08` so these are operators you can think
<br>`32:09` about this as operators so like eigen
<br>`32:12` direction of these operators and
<br>`32:16` the b is our course grading scale
<br>`32:30` the h tells us
<br>`32:34` how far we are away from the fixed point
<br>`32:42` and the s tells us uh is just the action
<br>`32:48` that we have at this fixed point
<br>`32:51` you know so we it's the same thing for
<br>`32:53` all of this was once we have once we
<br>`32:55` have this mineralization group flow
<br>`32:58` we're in the subject of non-linear
<br>`32:59` dynamics and we use the tools
<br>`33:02` of nonlinear dynamics renalization group
<br>`33:05` theory this language is slightly
<br>`33:09` different
<br>`33:10` you know so that's that's why you have
<br>`33:12` this b to the lambdas and so on
<br>`33:14` here and you separate the h i from the b
<br>`33:17` to the lambda
<br>`33:18` that's just the framework the how you
<br>`33:20` write it in the realization
<br>`33:23` theory for convenience reasons but what
<br>`33:26` we do here is
<br>`33:27` a simple linear stability analysis
<br>`33:30` of a non-linear system i will
<br>`33:34` re-linearize around the fixed point
<br>`33:36` we see how whether perturbations grow or
<br>`33:39` shrink
<br>`33:40` in different directions yeah and that
<br>`33:43` characterizes
<br>`33:44` then our nonlinear system and now we can
<br>`33:47` ask if we perturb around this fixed
<br>`33:50` point
<br>`33:51` in one direction i does it grow
<br>`33:54` this perturbation or does it shrink
<br>`33:57` lambda i
<br>`33:58` is larger than zero now this bi
<br>`34:03` is larger than one or b is larger than
<br>`34:07` one
<br>`34:08` now so lambda i is larger than zero then
<br>`34:11` our perturbation will grow
<br>`34:13` yeah perturbation
<br>`34:20` growth and then we say this direction or
<br>`34:23` this operator q
<br>`34:24` i you can also think about q i as one of
<br>`34:27` the
<br>`34:28` terms in the action now think about one
<br>`34:31` of the terms in the action
<br>`34:32` or one of the terms in the hamiltonian
<br>`34:36` this direction qi
<br>`34:40` is then called relevant
<br>`34:45` why is this relevant what we call when
<br>`34:46` do we call this relevance
<br>`34:48` you know if this perturbation grows we
<br>`34:51` are in this green direction here that
<br>`34:53` pushes us away from the critical point
<br>`34:56` so that means
<br>`34:56` that if we are an experimentalist
<br>`35:00` and if we want to tune our system
<br>`35:03` to get into the critical point
<br>`35:07` then
<br>`35:10` then we know that we have to turn
<br>`35:13` these relevant parameters qi
<br>`35:18` now this relevant parameter for which
<br>`35:19` this uh that are
<br>`35:21` unstable directions of this fixed point
<br>`35:25` now and if we have a relevant directions
<br>`35:28` we also have irrelevant directions
<br>`35:30` lambda is smaller than zero
<br>`35:32` and these directions are called
<br>`35:34` irrelevant
<br>`35:35` now perturbation
<br>`35:43` shrinks that means that
<br>`35:47` qi is irrelevant
<br>`35:53` that means the qi in this case is not a
<br>`35:56` parameter that drives us into this
<br>`35:58` critical point
<br>`36:01` and then we have the case that lambda i
<br>`36:03` is exactly equal to zero
<br>`36:05` then we don't really know what to do
<br>`36:08` then this q
<br>`36:09` i is
<br>`36:12` marginal and we cannot tell from this
<br>`36:15` linear stability analysis alone
<br>`36:17` from the linear realization around this
<br>`36:19` fixed bond we cannot tell alone
<br>`36:21` whether this perturbation will grow or
<br>`36:24` shrink and we have to use
<br>`36:25` other methods okay
<br>`36:28` so what happened now so we
<br>`36:31` started our theory close to the critical
<br>`36:34` point
<br>`36:35` we did this rememberization group
<br>`36:37` procedure
<br>`36:39` course grading rescaling renormalization
<br>`36:43` and then in this procedure
<br>`36:46` our action or our model will flow
<br>`36:49` through the space of all possible models
<br>`36:52` yeah
<br>`36:55` and then we ask where does it flow to
<br>`37:00` and we look at the non-linear dynamics
<br>`37:01` lecture and ask
<br>`37:03` so where does such a nonlinear system
<br>`37:05` drive us to
<br>`37:07` and our nonlinear dynamics lecture will
<br>`37:09` tell us look at the fixed points
<br>`37:12` right and in this realization flow you
<br>`37:14` also have fixed points you assume that
<br>`37:15` you have a fixed point
<br>`37:17` and this fixed point tells us about
<br>`37:21` what is going on on the macroscopic
<br>`37:24` scale now that determines this fixed
<br>`37:26` point
<br>`37:26` determines which is the end result of
<br>`37:28` our minimization group
<br>`37:30` procedure
<br>`37:33` so at this fixed point is characterized
<br>`37:36` by stability
<br>`37:38` it has a finite number of relevant
<br>`37:40` directions
<br>`37:43` now it's had a finite number of
<br>`37:44` parameters that are actually important
<br>`37:47` to change if you want to go to the
<br>`37:48` critical point
<br>`37:51` and because you only have a finite
<br>`37:53` number of directions that are relevant
<br>`37:56` you usually get away with models that
<br>`37:58` also have this very finite number
<br>`38:01` of parameters instead of models like a
<br>`38:04` bigger magnet or so that is a very
<br>`38:06` complicated geometry and everything
<br>`38:08` there are instead of model that has 15
<br>`38:10` 000 parameters
<br>`38:12` now you get away with a finite number of
<br>`38:13` parameters that are given
<br>`38:15` by the relevant eigen directions
<br>`38:19` of this fixed point now so now what
<br>`38:22` happens if we have a different model so
<br>`38:24` now this is now the
<br>`38:25` magnet one that this is not a
<br>`38:29` magnet or material one we can also look
<br>`38:31` at a magnet at another of another
<br>`38:33` material
<br>`38:34` now so this magnet one
<br>`38:40` and now we have here
<br>`38:47` a magnitude
<br>`38:51` now each of them at the physical real
<br>`38:53` microscopic level is destroyed by 15 000
<br>`38:56` parameters or whatever something very
<br>`38:57` complicated
<br>`38:59` and for this magnitude we can do the
<br>`39:02` same procedure
<br>`39:04` we renormalize
<br>`39:07` and we while we renormalize we will end
<br>`39:10` up at the vicinity of this fixed point
<br>`39:14` and in the vicinity of the fixed point
<br>`39:17` the behavior of the flow is determined
<br>`39:20` by a finite number
<br>`39:22` of parameters again
<br>`39:26` and both of these magnets here are
<br>`39:29` under renormalization now on the large
<br>`39:31` scale repeat these
<br>`39:33` procedures determined by the same fixed
<br>`39:37` point
<br>`39:37` about the same point but this one here
<br>`39:41` and because they're determined by the
<br>`39:42` same fixed point with the same stability
<br>`39:46` and with the same properties of how they
<br>`39:48` go
<br>`39:49` uh of how the flow behaves around this
<br>`39:51` fixed point
<br>`39:53` that's why these two magnets here are
<br>`39:55` described macroscopically by the same
<br>`39:57` theory
<br>`39:58` and that's then the reason why we have
<br>`40:01` universality
<br>`40:03` so in this way in this very general way
<br>`40:05` so we look of course in our in
<br>`40:07` more detail the renal isolation group
<br>`40:10` theory gives us a justification for why
<br>`40:14` only a finite number of parameters
<br>`40:17` matter
<br>`40:17` on the or finite a limited level of
<br>`40:21` description is sufficient to describe
<br>`40:23` large scale properties of a large
<br>`40:26` number of very different systems and the
<br>`40:29` reason is
<br>`40:30` at this critical point they're
<br>`40:33` described macroscopically by the same
<br>`40:36` fixed point of the renewalization
<br>`40:39` workflow

### slide 10

<br>`40:42` now how does this look in detail
<br>`40:47` so the very first or the
<br>`40:50` most uh simple way of doing
<br>`40:53` remoralization
<br>`40:55` is to take what i said initially about
<br>`40:58` this
<br>`40:59` defocusing about this course training
<br>`41:01` literally
<br>`41:02` and do the whole procedure in real space
<br>`41:06` now suppose you have here a lattice
<br>`41:09` system
<br>`41:11` and also suppose you have this lattice
<br>`41:12` system here and you have some
<br>`41:15` spins here and what you can do then to
<br>`41:19` cause grain
<br>`41:20` is to
<br>`41:24` you know what you can do to coarse grain
<br>`41:26` is to create
<br>`41:27` boxes or blocks now of a certain size
<br>`41:31` and then to calculate this cross here
<br>`41:34` that is a representation of all of these
<br>`41:37` microscopic spin for each block
<br>`41:40` yeah so we have this uh spins here
<br>`41:44` like what are 16 in each block and you
<br>`41:48` now transform them to a single number
<br>`41:50` you can do that by averaging over them
<br>`41:52` or you can take
<br>`41:54` you can say that i take the spin
<br>`41:58` that is the majority of these other
<br>`42:01` spins here
<br>`42:02` if the majority goes up then my new spin
<br>`42:06` that describes the entire block
<br>`42:07` will also go up and this would be a way
<br>`42:11` to get a rid of this renormalization
<br>`42:14` step if you say i take the majority
<br>`42:18` i take a majority rule so this new spin
<br>`42:20` here x
<br>`42:21` will take the value of the majority of
<br>`42:24` the original spins
<br>`42:27` then the new spin will also be plus or
<br>`42:29` minus one
<br>`42:31` if my new spin yeah and i don't have to
<br>`42:33` renormalize them because it has the same
<br>`42:35` values as the original splits
<br>`42:38` if i take the new spin as the average
<br>`42:43` over all of these spins here then
<br>`42:47` i typically get a very small number the
<br>`42:49` average won't be one or minus one but it
<br>`42:51` will be
<br>`42:52` 0.3 or 0.1 or 0.5 or so but it will not
<br>`42:57` be
<br>`42:57` one or minus one in most cases yeah so
<br>`43:00` in this case if i perform this procedure
<br>`43:02` i would have to renormalize
<br>`43:04` you know and i have to would have to
<br>`43:05` rescale my fields
<br>`43:08` to make them comparable to the original
<br>`43:10` step
<br>`43:12` yeah so now we have these blocks
<br>`43:17` and we define some new spin that
<br>`43:20` describes each of these blocks
<br>`43:23` and now we write down a new model
<br>`43:26` a new hamiltonian for these new spins
<br>`43:29` here
<br>`43:31` and what we hope is that the spins that
<br>`43:35` we have here
<br>`43:38` in this new system this course-grade
<br>`43:40` system are described by a theory
<br>`43:43` that is structurally very similar to the
<br>`43:45` original theory
<br>`43:48` and this hope is actually justified by
<br>`43:52` the observation of
<br>`43:55` scale and variance now so if your system
<br>`43:58` is scaled in variance we can hope that
<br>`43:59` if we zoom out
<br>`44:01` and our system is statistically the same
<br>`44:04` then then our partition function
<br>`44:06` or our action will also be the same
<br>`44:09` just with some different parameters now
<br>`44:11` that is the hope that is underlying
<br>`44:13` renewalization group procedures with
<br>`44:16` these
<br>`44:16` block spins here what you typically get
<br>`44:19` is that you get
<br>`44:20` higher order turns all the time you know
<br>`44:23` so that's this hope is not
<br>`44:24` mathematically super precise uh but
<br>`44:28` that's what you have to assume in order
<br>`44:30` to achieve anything
<br>`44:33` okay yeah
<br>`44:36` okay so we call screen and then
<br>`44:40` we rescale the second step so that the
<br>`44:42` distance between these
<br>`44:44` spins here the new spins is the same
<br>`44:47` distance as we had
<br>`44:49` between the original spins now that's
<br>`44:52` what we have to do anyway
<br>`44:53` and that's why how we divide length
<br>`44:55` scales
<br>`44:57` by the same factor that corresponds to
<br>`45:00` the size of our boxes
<br>`45:02` yeah and now the lengths are the same as
<br>`45:04` before

### slide 11

<br>`45:09` so let's do this procedure in a very
<br>`45:13` simple case which is the 1d
<br>`45:16` ising model
<br>`45:21` now so the one deising model now is
<br>`45:24` written the tradition function
<br>`45:26` it can be written in like a long form
<br>`45:30` in this way here that i sum up
<br>`45:33` all combinations of nearest neighbor
<br>`45:36` interactions
<br>`45:38` now that's just the hamiltonian here of
<br>`45:40` the ising model without an external
<br>`45:42` field
<br>`45:43` now and then i have to have a sum about
<br>`45:45` all possible values of the sigma i's
<br>`45:48` of the of the that my fee that my all
<br>`45:51` the possible values
<br>`45:52` that the sigma can take that gives me my
<br>`45:54` partition function
<br>`45:57` now what i do know is the first
<br>`46:01` course grading stuff now this first
<br>`46:04` coast grading step
<br>`46:06` means that these red spins here
<br>`46:09` like with the all these these black
<br>`46:11` spins are the white splits
<br>`46:13` now i'll integrate out the white spins
<br>`46:17` here in this picture i'll integrate
<br>`46:20` these ones out
<br>`46:23` now every second spin all even spins
<br>`46:26` and if i do that i will get a new theory
<br>`46:30` that is described by interactions
<br>`46:32` between these
<br>`46:33` uneven spins that are and these
<br>`46:36` interactions occurred to us are
<br>`46:37` depicted in these red with these red
<br>`46:41` lines
<br>`46:44` okay so and the stars is actually very
<br>`46:47` simple activated talks
<br>`46:49` so that's so for if we just do it for
<br>`46:56` for sigma 2 now we just sum
<br>`46:59` out we take the terms that correspond to
<br>`47:02` sigma 2
<br>`47:04` and we get that that is equal to
<br>`47:08` not many terms and then we have the
<br>`47:11` contribution from sigma 2
<br>`47:14` uh k sigma 1
<br>`47:17` plus sigma 3 now that's what what's left
<br>`47:20` plus e to the minus k sigma 1
<br>`47:25` sigma 3
<br>`47:28` and then all the rest e to the k
<br>`47:32` sigma 3 sigma
<br>`47:36` 4 plus four sigma
<br>`47:40` five and all the other splits
<br>`47:44` so what i just that said is that sigma
<br>`47:46` two can have two values
<br>`47:48` minus one plus one yeah and i just
<br>`47:51` substituted i expected
<br>`47:53` explicitly now set sigma 2 to plus 1 and
<br>`47:56` minus 1
<br>`47:57` and perform the sum and that's what i
<br>`47:59` get then here for this first
<br>`48:01` term and now i can do that for all
<br>`48:12` even sigmas and then what i get is
<br>`48:16` exactly the same thing sum over
<br>`48:20` many terms e to the k
<br>`48:23` sigma 1 plus sigma 3 as before
<br>`48:27` plus e to the minus k sigma 1
<br>`48:31` sigma 3. now that was the original one
<br>`48:34` where we set sigma
<br>`48:36` 2 to -1 and then we get the same thing
<br>`48:42` e to the k for the next
<br>`48:45` term now for the next interaction sigma
<br>`48:48` 3
<br>`48:49` plus sigma 5
<br>`48:54` e to the minus k sigma 3
<br>`48:58` sigma 5
<br>`49:01` and so on yeah
<br>`49:07` for all the other terms yeah

### slide 12

<br>`49:13` so now the idea is
<br>`49:18` that because when we are at a critical
<br>`49:21` state
<br>`49:23` that we expect our partition function to
<br>`49:25` be self-similar when we call screen
<br>`49:28` the statistics of the system remains the
<br>`49:31` same as we zoom out
<br>`49:33` and that's why we also expect
<br>`49:36` the quantity that gives us the statistic
<br>`49:40` statistics the partition function to be
<br>`49:42` self-similar as well
<br>`49:45` and what we now do is that we find
<br>`49:49` a new value of k prime
<br>`49:53` and some function f
<br>`49:56` of k that tells us that we
<br>`49:59` that these terms that we got
<br>`50:02` here sigma 1 sigma 3 we always got the
<br>`50:06` sum for each coupling
<br>`50:08` they should take the same form as the
<br>`50:11` original hamiltonian but with some
<br>`50:14` pre-factor here
<br>`50:17` and some new coupling here
<br>`50:20` but the form should be the same as
<br>`50:22` before
<br>`50:24` now as i said this is not usually
<br>`50:27` well justified but we have to do that in
<br>`50:29` order to do anything
<br>`50:31` and if you require that if you do some
<br>`50:33` algebra you will find that if you set
<br>`50:36` k prime to this one one half
<br>`50:39` logarithm hyperbolic cosine of 2k
<br>`50:44` and the function f of k to this year
<br>`50:48` then it fulfills this condition yeah
<br>`50:54` so now we can plug this in now so if we
<br>`50:59` if we use that
<br>`51:01` then our hammer tilt our partition
<br>`51:05` function
<br>`51:06` will read again we have many
<br>`51:10` terms f of k
<br>`51:14` e to the k prime
<br>`51:17` sigma 1 sigma 3
<br>`51:21` f of k e to the k
<br>`51:24` prime sigma 3 sigma 5
<br>`51:29` and so on
<br>`51:32` now and this is just the same we can
<br>`51:35` write this now
<br>`51:36` as a new partition function that has a
<br>`51:40` new prefactor
<br>`51:42` f of k now we pull this out this
<br>`51:45` prefactor
<br>`51:46` f of k and we have that n over two times
<br>`51:51` times a new partition function that
<br>`51:55` depends on the new system size
<br>`52:00` and a new coupling k prime
<br>`52:04` yeah so we have this down this one
<br>`52:06` renormalization step
<br>`52:08` we get a new partition function that
<br>`52:10` looks exactly the same as the old one
<br>`52:12` in structure but we have a new coupling
<br>`52:15` k prime
<br>`52:17` and a pre-factor here that is this
<br>`52:20` function
<br>`52:21` f and that also depends on the coupling
<br>`52:25` also what we did here is that we now
<br>`52:27` have
<br>`52:31` a relationship between the partition
<br>`52:34` functions
<br>`52:35` at different stages of the
<br>`52:38` renewalization procedure
<br>`52:45` yeah and now
<br>`52:50` what does it mean look at
<br>`52:53` this one here k prime
<br>`52:57` this is already a description
<br>`53:02` now this is already a description of how
<br>`53:04` our coupling
<br>`53:05` one parameter k prime
<br>`53:09` depends on the value of this okay now
<br>`53:12` how this parameter k
<br>`53:13` evolves in this course grading procedure
<br>`53:17` in this renewalization procedure
<br>`53:20` you know so this k that gets updated
<br>`53:23` now it's not in differential form yeah
<br>`53:26` like in
<br>`53:26` like uh like we did in the non-linear
<br>`53:28` dynamics
<br>`53:29` actually but it's in this uh other way
<br>`53:32` that you can describe non-linear
<br>`53:34` systems but by iterative updating now so
<br>`53:38` the new value of k
<br>`53:39` prime is given by the old value
<br>`53:43` is by this function here applied to the
<br>`53:45` old value
<br>`53:47` and now now is this is this updating
<br>`53:50` scheme here
<br>`53:52` and we can expand this term here the
<br>`53:54` logarithm
<br>`53:55` of the hyperbolic cosine and so for low
<br>`53:58` values of this coupling
<br>`54:00` this goes with k squared now so normally
<br>`54:03` i have an idea
<br>`54:05` about how this looks like i have already
<br>`54:08` prepared this
<br>`54:09` very nice and we can now solve this
<br>`54:11` equation here
<br>`54:13` graphically so we want to get the flow
<br>`54:15` and we can solve this graphically
<br>`54:17` and see where this linearization
<br>`54:19` procedure
<br>`54:20` carries our k our coupling k
<br>`54:23` now and because our partition function
<br>`54:27` remains invariant

### slide 13

<br>`54:30` well our k the update of our k
<br>`54:35` describes actually the behavior of our
<br>`54:37` hamiltonian
<br>`54:38` under renormalization
<br>`54:41` okay so this is the plot here so what i
<br>`54:44` what you do
<br>`54:44` is that you plot the left hand side
<br>`54:48` of this equation k prime it's just
<br>`54:51` linear with slope one
<br>`54:54` and uh the right hand side
<br>`54:58` now this is uh this here
<br>`55:02` and where the left hand side is equal to
<br>`55:04` the right hand side there you have a
<br>`55:06` fixed point
<br>`55:07` now so this is here the way you need to
<br>`55:10` read this this is the next value of the
<br>`55:11` realization
<br>`55:12` this is the previous one if you start
<br>`55:14` here we'll go
<br>`55:15` here then here and here and here
<br>`55:19` and at some point these two lines meet
<br>`55:22` and that's
<br>`55:22` that's where your fixed point is so this
<br>`55:25` humanization procedure
<br>`55:27` will bring us to some fixed point which
<br>`55:29` happens
<br>`55:30` to be uh down here at zero
<br>`55:36` yeah and then we can look at how this
<br>`55:39` uh we can also then plot
<br>`55:42` a flow diagram as i did in a more
<br>`55:45` complicated way before
<br>`55:47` and how we also did it in the actual
<br>`55:49` nonlinear dynamics lecture
<br>`55:51` now we can plot it on this in this
<br>`55:53` one-dimensional line
<br>`55:55` then we have a stable fixed point at
<br>`55:57` zero
<br>`55:58` now that's here stable
<br>`56:02` and any value where we start with our
<br>`56:04` course grading procedure
<br>`56:06` will be driven to a value of k equals
<br>`56:09` zero
<br>`56:10` now we start with a very strong coupling
<br>`56:12` we renormalize
<br>`56:14` and we will be driven to zero
<br>`56:17` that means that this renormalization
<br>`56:21` procedure this course grading procedure
<br>`56:24` in this one-dimensional icing model
<br>`56:28` will always on the macroscopic skin on
<br>`56:31` large
<br>`56:31` length scales always lead to a model
<br>`56:35` that is effectively described by
<br>`56:40` a system that has zero coupling
<br>`56:43` yeah this coupling here vanishes and if
<br>`56:46` we have zero coupling that means that
<br>`56:48` our system
<br>`56:49` is above the critical point that's
<br>`56:52` non-critical
<br>`56:54` so we will normalize we go on and on
<br>`56:57` and we always end up on the system that
<br>`56:59` has very high temperature
<br>`57:01` or very low coupling yeah that's a it is
<br>`57:04` a disordered system
<br>`57:06` and that's just a reflection of the fact
<br>`57:07` that the one deicing model
<br>`57:10` doesn't have any order for a finite
<br>`57:12` temperature
<br>`57:15` now so you have to start with coupling
<br>`57:18` exactly equal to infinity
<br>`57:21` to get an order over the temperature
<br>`57:24` exactly
<br>`57:24` equal to zero only then you can have
<br>`57:26` order everything else
<br>`57:28` will drive you to this fixed point here
<br>`57:32` that corresponds to a system where you
<br>`57:35` have no
<br>`57:36` coupling at all now so the one that we
<br>`57:39` knew that already that the 1d
<br>`57:40` system doesn't show all in the ising
<br>`57:42` model doesn't have order
<br>`57:44` it doesn't have a really critical point
<br>`57:47` and that's why our flow
<br>`57:48` tells us that macroscopic scales this
<br>`57:51` system
<br>`57:51` goes to a system that doesn't have
<br>`57:55` any interaction so it's completely
<br>`57:56` disordered

### slide 14

<br>`57:59` of course you can do the same procedure
<br>`58:01` for um
<br>`58:04` for the 2d system yeah and there is of
<br>`58:06` course
<br>`58:07` again much more complicated then this 2d
<br>`58:10` system
<br>`58:12` you get a flow diagram that looks like
<br>`58:15` this here
<br>`58:17` on the bottom so here you suddenly
<br>`58:21` have another fixed point an unstable
<br>`58:23` fixed point
<br>`58:25` in between these two extremes now this
<br>`58:28` unstable fixed point
<br>`58:30` here if you start to the left of this
<br>`58:33` unstable fixed point you were driven to
<br>`58:36` a state
<br>`58:37` without that that we had previously
<br>`58:40` where the coupling is very low
<br>`58:42` or that corresponds to the system at
<br>`58:43` very high temperature
<br>`58:45` if you start to the right of this you'll
<br>`58:47` be driven to a state
<br>`58:49` where you have order you know where your
<br>`58:51` coupling is basically infinity or your
<br>`58:53` temperature effective temperature
<br>`58:55` is zero and because you have now this
<br>`58:58` fixed point here this new fixed point
<br>`59:00` right you get
<br>`59:02` this singularity or this discontinuity
<br>`59:05` of the free energy because if you go a
<br>`59:06` little bit to the left
<br>`59:08` you go to another a different
<br>`59:10` macroscopic state
<br>`59:11` then if you go a little bit to the right
<br>`59:14` and of course you can test that with
<br>`59:15` numerical simulations
<br>`59:17` now so that's here from the book of
<br>`59:19` cardi which is a very very nice book um
<br>`59:22` scaling and renormalization and
<br>`59:23` statistical physics
<br>`59:26` and i have to say that
<br>`59:29` the class don't look very good on this
<br>`59:32` ipad
<br>`59:34` so what you see here are just
<br>`59:36` simulations of the two the eisenmann
<br>`59:39` and what they did is they performed one
<br>`59:42` block spin removalization procedure
<br>`59:45` that's that's what we did right now
<br>`59:47` that's the coarse grain so one step of
<br>`59:50` this coarse graining
<br>`59:52` and uh if you are right at the critical
<br>`59:55` point on the left hand side
<br>`59:57` you do the coarse graining step yeah
<br>`59:59` then
<br>`60:00` the system remains invariant if you
<br>`60:02` start in a fixed point you'll stay there
<br>`60:05` if you start a little bit this course
<br>`60:07` grading procedure
<br>`60:08` and here that's not there's nothing
<br>`60:10` fancier they just took the simulations
<br>`60:13` and they did one course grading step
<br>`60:15` they averaged you have maybe over a
<br>`60:17` block of spins or so
<br>`60:19` and if you are above this
<br>`60:23` critical temperature that means you
<br>`60:24` start here on the left of this fixed
<br>`60:26` point
<br>`60:27` and if you do this course grading step
<br>`60:29` then your system looks more disordered
<br>`60:31` than before
<br>`60:33` yeah so this year it looks like a higher
<br>`60:35` temperature than this year because you
<br>`60:37` have a lot of these small domains
<br>`60:39` now this is just a reflection of this
<br>`60:41` stat like an intuitive
<br>`60:43` picture of how you go in this
<br>`60:45` reunionization procedure
<br>`60:47` to the left to a state that has no
<br>`60:49` coupling at all
<br>`60:50` k equals zero and if you're coupling a
<br>`60:53` zero that's the same as when your
<br>`60:54` temperature
<br>`60:55` is very large and if you want to read
<br>`60:58` more about this
<br>`60:59` have a look at the book of john carty
<br>`61:01` and there's also of what i just showed
<br>`61:03` you
<br>`61:04` there is a there is a nice book by um
<br>`61:11` so there's a nice book there's a nice
<br>`61:13` article by karanov
<br>`61:15` um by teaching the immunization group
<br>`61:17` and he does these calculations also for
<br>`61:19` the 2d
<br>`61:20` model okay so now
<br>`61:23` we state in a real space yeah and in
<br>`61:26` real space
<br>`61:28` uh is very intuitive now
<br>`61:31` and it works for the one deising model
<br>`61:33` for the 2d eisen model gets already
<br>`61:34` complicated
<br>`61:36` and it's basically impractical to do
<br>`61:38` that
<br>`61:39` for general um
<br>`61:43` for for general physical models now it
<br>`61:46` gets very complicated to do that
<br>`61:47` procedure
<br>`61:48` in real space and the reason is that
<br>`61:50` there's no small parameter involved
<br>`61:53` that you can use for an expansion

### slide 15

<br>`61:57` then there was another guy called wilson
<br>`61:59` who came up with another idea
<br>`62:01` now that was actually and that's called
<br>`62:03` the wilson
<br>`62:05` momentum shell idea
<br>`62:09` that's the world's in momentum shell
<br>`62:11` idea so what does it mean so what was
<br>`62:14` wilson's idea was that we caused grain
<br>`62:18` by integrating out fast degrees of
<br>`62:21` freedom
<br>`62:22` or degrees of freedom that have a very
<br>`62:24` short wavelength
<br>`62:26` in fourier space that's the way you do
<br>`62:29` that
<br>`62:30` is uh you look at free space also this
<br>`62:33` is our
<br>`62:34` free space let's say we have two
<br>`62:35` directions in free space
<br>`62:38` then we have here
<br>`62:44` a maximum wave vector that's the maximum
<br>`62:52` wave vector and this wave vector let's
<br>`62:55` call it
<br>`62:56` capital omega is the same
<br>`63:00` just given by that's the smallest
<br>`63:02` structure we can have in the system
<br>`63:04` that's a microscopic length scale
<br>`63:06` yeah and that's in these lattice systems
<br>`63:08` this typical
<br>`63:09` uh one over the the lattice the
<br>`63:12` microscopic level the lattice spacing
<br>`63:15` yeah so we cannot go any smaller than
<br>`63:17` that
<br>`63:19` now starting from the smallest length
<br>`63:21` scale now so a description of our system
<br>`63:24` on the smallest length scale
<br>`63:27` we now integrate out the blue stuff here
<br>`63:32` that's this one here that's the momentum
<br>`63:35` shell
<br>`63:42` and we integrate out this momentum shell
<br>`63:45` until we reach
<br>`63:48` a new wavelength a new y vector of a new
<br>`63:51` length scale
<br>`63:54` omega prime is equal to the original
<br>`63:57` omega
<br>`63:58` divided sum by some number lambda
<br>`64:01` yeah so
<br>`64:05` we integrate out one bit in momentum
<br>`64:08` space
<br>`64:10` at a time and that means that we perform
<br>`64:13` an integration
<br>`64:15` uh on a momentum shell on a tiny shell
<br>`64:18` in momentum space and also our new field
<br>`64:26` in the momentum shell
<br>`64:32` is then called typically something like
<br>`64:35` feel
<br>`64:36` find larger of q
<br>`64:40` and this is just undefined by
<br>`64:43` phi of q
<br>`64:46` with q in this interval
<br>`64:51` omega over lambda to omega
<br>`64:56` yeah so we integrate
<br>`65:00` out one step and now wilson's scheme is
<br>`65:03` actually very similar
<br>`65:08` to what we've done already yes the first
<br>`65:10` step will be
<br>`65:12` recall screen
<br>`65:18` now by rescaling oops sorry
<br>`65:29` no by rescaling
<br>`65:34` and that will give rise to some
<br>`65:38` change in the coefficients
<br>`65:46` in the action
<br>`65:49` and the second step is that we perform
<br>`65:56` this integration in the momentum shell
<br>`66:00` integrate out
<br>`66:04` short range
<br>`66:08` fluctuations
<br>`66:12` or momentum
<br>`66:19` a second step and we'll in the next
<br>`66:22` lecture
<br>`66:22` we do exactly this yeah we performed
<br>`66:24` this wilson's ruralization group
<br>`66:26` procedure that is much more practical
<br>`66:29` than the
<br>`66:29` block spin immunization group that we
<br>`66:32` had in the
<br>`66:32` beginning of this lecture and the good
<br>`66:36` thing about this wilson's
<br>`66:38` of wilson's idea is that it actually has
<br>`66:40` a small parameter
<br>`66:41` this momentum shell is very small
<br>`66:44` and uh yes so this
<br>`66:48` has a small parameter that means that we
<br>`66:50` can actually then
<br>`66:51` hope to get some approximative um
<br>`66:55` uh scheme out of this approximative
<br>`67:00` so that we can approximate our integrals
<br>`67:02` that we get from the course grade
<br>`67:04` yeah so we'll do that uh next week
<br>`67:07` for our little epidemic model and we'll
<br>`67:10` derive
<br>`67:11` the renalization group flow from our
<br>`67:13` equity epidemic model
<br>`67:15` and from this flow we'll then get the
<br>`67:17` exponents that derive that describe
<br>`67:20` the action of the the the behavior
<br>`67:23` of this epidemic model near the critical
<br>`67:26` point
<br>`67:27` yeah and um
<br>`67:30` exactly yeah so so that's what we'll do
<br>`67:33` i'll
<br>`67:33` just leave it for here today because and
<br>`67:35` then next week we do the calculation and
<br>`67:37` if you're
<br>`67:38` not interested in calculating that
<br>`67:41` because it's so
<br>`67:42` uh so uh
<br>`67:46` so uh short before christmas if you're
<br>`67:48` free to skip the next lecture
<br>`67:50` yeah and uh officially i think it's not
<br>`67:53` a lecture data
<br>`67:56` but i wanted to get that done before
<br>`67:57` christmas that we can after christmas at
<br>`68:00` january what is that fifth or so i can't
<br>`68:03` remember
<br>`68:03` um we'll start actually done with data
<br>`68:06` science and
<br>`68:07` to look at some real data yeah okay
<br>`68:10` great
<br>`68:11` so that was today only the intuitive
<br>`68:13` part about romanization so next week
<br>`68:15` we'll do
<br>`68:15` we'll see that in action and see how it
<br>`68:18` actually works in the non-equilibrium
<br>`68:19` system
<br>`68:22` bye

### answering a question

<br>`68:28` excuse me yes
<br>`68:31` um could you please explain again why
<br>`68:33` were we trying to reach the fixed point
<br>`68:35` from the critical point
<br>`68:37` so so we're not trying to
<br>`68:41` it's just that you assume for this to
<br>`68:44` work that there is such a fixed point
<br>`68:47` that determines the flow of the
<br>`68:50` renormalization group yeah in this
<br>`68:53` generality you have to assume that that
<br>`68:55` there is
<br>`68:56` such a fixed point and from nonlinear
<br>`68:58` dynamics dynamical system
<br>`69:00` lecture that we have we know that once
<br>`69:02` we have such a fixed point
<br>`69:04` we basically know already how the system
<br>`69:07` behaves also in other parts
<br>`69:09` of uh of the faith yeah so that's why
<br>`69:12` the system these fixed points are so
<br>`69:14` important now we have to assume that
<br>`69:16` there exists some verb
<br>`69:17` uh but we have to basically for every
<br>`69:19` individual model that we look at we have
<br>`69:21` to show that they actually
<br>`69:23` that they that we have actually
<br>`69:25` meaningful
<br>`69:27` or moral more than one thing of course
<br>`69:31` yeah so but once you have the flow it's
<br>`69:33` a problem in normal dynamics
<br>`69:35` that's that once you have the flow you
<br>`69:36` do what you do in non-aerodynamic
<br>`69:38` dynamic dynamics so typically in these
<br>`69:40` books of linearization they use a
<br>`69:42` different language that's a little bit
<br>`69:43` disconnected from this dynamical systems
<br>`69:47` field
<br>`69:48` no but what you do is you have
<br>`69:50` non-linear
<br>`69:51` differential equations and then you just
<br>`69:53` want to see what happens to these
<br>`69:55` nonlinear differential equations
<br>`69:57` and then if you ask this question then
<br>`70:00` and non-in your system you need to ask
<br>`70:01` about the fixed points
<br>`70:03` and about the stability of yeah and
<br>`70:05` that's why this fixed point
<br>`70:07` in the randomization group flow is so
<br>`70:10` important
<br>`70:11` now if there wasn't any fixed point at
<br>`70:13` all yeah then
<br>`70:14` it would be a very good system so we
<br>`70:16` have to have such a big
<br>`70:19` point on the critical manifold for this
<br>`70:22` uh for this procedure to work
<br>`70:25` now we have to assume at this stage here
<br>`70:27` we have to assume
<br>`70:29` that it exists and if it exists then it
<br>`70:31` will determine
<br>`70:32` our flow yeah
<br>`70:36` but we don't want to we don't want to do
<br>`70:38` so once we have to fix the the system
<br>`70:40` the renewalization group will
<br>`70:41` automatically
<br>`70:42` carry us to the fixed point now we don't
<br>`70:44` we don't want to go the system to
<br>`70:47` the system to go there if the fixed
<br>`70:49` point exists
<br>`70:50` we'll have to uh we know that the flow
<br>`70:54` will determine we will be determined by
<br>`70:56` this
<br>`70:58` yeah so that's the that's the that's the
<br>`71:01` idea
<br>`71:02` but there's non-linear systems that in
<br>`71:04` principle has not much to do with
<br>`71:06` renormalization
<br>`71:07` yeah it is a general property of the
<br>`71:10` dynamic
<br>`71:14` okay thank you okay great
<br>`71:24` any other questions
<br>`71:28` um i have a question um so
<br>`71:32` does this does this um
<br>`71:35` require you to have a very
<br>`71:38` good understanding of the microscopic
<br>`71:42` um dynamics i guess
<br>`71:45` you have to have a model to start with i
<br>`71:48` mean
<br>`71:48` um but that's kind of what i mean is
<br>`71:51` if you have some model that's leaving
<br>`71:55` out certain things that are
<br>`71:57` that maybe
<br>`72:01` you know you thought wasn't so important
<br>`72:03` or something like that
<br>`72:04` but then as you core scream more and
<br>`72:08` more
<br>`72:08` like does it like um
<br>`72:11` will it give rise to like a different rg
<br>`72:14` flow than
<br>`72:15` if you had included you know other other
<br>`72:19` uh okay i think i think that that
<br>`72:21` depends on
<br>`72:22` what you leave away and what you leave
<br>`72:24` out and what you can use so in principle
<br>`72:28` for the usual model including this si
<br>`72:30` model that we have here
<br>`72:32` that we're looking at and also but also
<br>`72:34` for the icing model and
<br>`72:36` they they fall a little bit out of the
<br>`72:37` blue when somebody presents them to you
<br>`72:40` and for example in the lecture now they
<br>`72:43` completely make sense that they
<br>`72:45` destroyed these systems
<br>`72:47` but usually people have used
<br>`72:50` renormalization studies
<br>`72:52` to show that additional terms don't
<br>`72:55` don't matter for these yeah also for
<br>`72:57` this active
<br>`72:58` uh for these active systems that we
<br>`73:00` talked about
<br>`73:02` with these aligning uh with these
<br>`73:04` aligning directions
<br>`73:05` and so on now for these systems i showed
<br>`73:08` you briefly a larger way equation and
<br>`73:09` people did a
<br>`73:10` lot of work to show that this is
<br>`73:12` actually the simplest
<br>`73:14` uh description that you can have that
<br>`73:15` describes this system now because the
<br>`73:18` rigid rimmelization they found
<br>`73:20` that all other terms so this is the
<br>`73:22` minimal set of terms that i need
<br>`73:24` to describe still the same
<br>`73:26` renewalization
<br>`73:27` or still renumerization yeah
<br>`73:31` and uh whether you get new terms i
<br>`73:34` so i i would i wouldn't expect that if
<br>`73:35` you
<br>`73:37` i wouldn't expect to get new relevant
<br>`73:39` terms
<br>`73:40` out of nothing yeah in general you know
<br>`73:43` otherwise you could start with just
<br>`73:45` nothing at all and see what happens and
<br>`73:47` then you get like a theory of everything
<br>`73:49` i wouldn't expect these things to pop up
<br>`73:52` yeah but of course you get all kind of
<br>`73:53` messy things
<br>`73:55` now you can have if you start with the
<br>`73:57` icing more then in reality then you get
<br>`73:59` higher order
<br>`74:00` interactions and so on and
<br>`74:04` and you have to basically have to get
<br>`74:06` rid of them
<br>`74:08` okay i think let's uh okay great
<br>`74:18` okay so if there are no more questions
<br>`74:20` then uh
<br>`74:21` see you all next week so as as
<br>`74:25` as usual next week i'll uh
<br>`74:28` start with a repetition of this and
<br>`74:31` explain explain it again before we
<br>`74:33` actually do the
<br>`74:34` real calculation okay bye see you next
<br>`74:40` week
<br>`74:45` you 
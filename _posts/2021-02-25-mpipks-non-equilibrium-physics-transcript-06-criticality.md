---
layout:      post
title:      "马普所·非平衡态系统中的集体过程·语音转录 | 06. Non-equilibrium Criticality"
keywords:   "mpipks-transcript"
excerpt:    "下一讲就是重整化群了"
date:        2021-02-25
categories:  post
milestoneID: 33
---

### slide 1

<br>`00:00` there we go
<br>`00:07` okay so now you can see the screen i
<br>`00:09` hope
<br>`00:10` with a little overview so what where are
<br>`00:13` we actually
<br>`00:14` uh at the moment yeah so we had uh
<br>`00:18` two lectures ago we started thinking
<br>`00:20` about how order can emerge
<br>`00:22` you know and we said that this somehow
<br>`00:25` um very often uh relies on a balance
<br>`00:29` between
<br>`00:30` fluctuations you know that favor
<br>`00:31` disorder and
<br>`00:33` interactions that favor order
<br>`00:37` and then we went on next week last week
<br>`00:40` to study how we can have transitions
<br>`00:44` between different non-equilibrium states
<br>`00:48` for example between a
<br>`00:49` disordered and an order state or between
<br>`00:52` different kinds of ordered states
<br>`00:54` and we started that in a situation where
<br>`00:56` we neglected
<br>`00:58` moles we pretended that our
<br>`01:00` non-equilibrium system
<br>`01:01` or our general system could also be an
<br>`01:04` equilibrium system is very very large
<br>`01:06` and then we were basically back in the
<br>`01:08` framework
<br>`01:09` of non-linear differential equations and
<br>`01:12` non-linear partial differential
<br>`01:14` equations
<br>`01:15` and to understand then what kind of
<br>`01:17` order we had
<br>`01:19` we looked at specific situations here
<br>`01:21` where this order
<br>`01:23` or these patterns arose continuously
<br>`01:26` or not abruptly but they first were
<br>`01:28` small and then we can larger larger
<br>`01:31` and in these situations were allowed and
<br>`01:33` to linearize
<br>`01:34` and to ignore these difficult
<br>`01:38` non-linearities in these equations
<br>`01:42` so today we're now in a state where we
<br>`01:44` want to
<br>`01:46` join these two lectures now we're
<br>`01:49` looking at transitions between
<br>`01:51` non-equilibrium
<br>`01:53` steady states where
<br>`01:57` we have noise yeah and i wouldn't tell
<br>`02:01` you that i wouldn't have a lecture on
<br>`02:02` this if
<br>`02:03` the noise these fluctuations in these
<br>`02:06` transitions weren't super important
<br>`02:09` and maybe yeah then
<br>`02:12` once we've understood that we are in a
<br>`02:15` position
<br>`02:16` uh just to understand how does actually
<br>`02:19` order look like
<br>`02:20` how can we identify order and after that
<br>`02:23` we'll then
<br>`02:23` go to data and actually learn some tools
<br>`02:26` from data science
<br>`02:27` on how to extract such order
<br>`02:31` from complex and big data sets
<br>`02:34` and then at the end of this lecture of
<br>`02:37` this uh this term
<br>`02:38` uh we'll have a specific example from
<br>`02:40` research where we bring that all
<br>`02:42` together and we see
<br>`02:43` how this works together uh in the
<br>`02:45` context of
<br>`02:46` current research

### slide 2

<br>`02:50` okay so to start
<br>`02:54` let's remind ourselves about
<br>`02:57` how we actually transit from order to
<br>`03:00` from disorder to order in equilibrium
<br>`03:03` yeah and we'll continue we'll
<br>`03:06` continue looking at continuous phase
<br>`03:09` transition and
<br>`03:10` in equilibrium these continuous phase
<br>`03:12` positions are characterized
<br>`03:14` by a critical point and this is just the
<br>`03:16` point where this balance
<br>`03:18` between fluctuations and interactions
<br>`03:21` this ordering and these disordering
<br>`03:24` forces
<br>`03:25` are just equal now the system doesn't
<br>`03:27` really know
<br>`03:28` exactly where to go whether to create an
<br>`03:30` ordered state or to a completely
<br>`03:32` disintegrated
<br>`03:33` order state and it's somewhere in
<br>`03:34` between and
<br>`03:36` uh so i i suppose
<br>`03:39` uh you've you you'll have had that in
<br>`03:42` your
<br>`03:42` statistical physics lecture normally
<br>`03:44` yeah but at the end of the first
<br>`03:46` statistical physics lectures but i'll
<br>`03:49` just give you
<br>`03:51` a little reminder of the most important
<br>`03:54` concepts
<br>`03:55` so here you see like this example from
<br>`03:58` equilibrium
<br>`03:59` this very powerful and intuitive model
<br>`04:02` system which is called the izing model
<br>`04:04` which is essentially modeling a
<br>`04:05` ferromagnet magnet
<br>`04:07` and on the left hand side you can see
<br>`04:10` simulations
<br>`04:12` for three different temperatures it's
<br>`04:15` just
<br>`04:16` such an icing model and what you see
<br>`04:18` here if the temperature is very low
<br>`04:21` you get an ordered state now everything
<br>`04:23` is black
<br>`04:24` all spins are putting the same
<br>`04:26` directions
<br>`04:27` in the same direction and if the
<br>`04:29` temperature is high
<br>`04:32` then you get a disordered state and this
<br>`04:35` disorder state as you see as a kind of
<br>`04:37` salt and pepper state now the average
<br>`04:40` magnetization is zero
<br>`04:43` but and locally uh you will always find
<br>`04:46` spin that goes up and down
<br>`04:48` go up and down and then you have that
<br>`04:50` thing in between these states
<br>`04:52` yeah when the temperature is exactly
<br>`04:56` equal to a critical temperature and this
<br>`04:59` is where
<br>`04:59` there is a balance between energy and
<br>`05:02` entropy of
<br>`05:03` fluctuations and order and
<br>`05:06` what you see here is this state
<br>`05:09` where you have these domains here
<br>`05:11` domains of these black domains
<br>`05:14` and if you zoom in to such a system
<br>`05:18` what you'll see at the critical point
<br>`05:19` you'll see that it looks exactly the
<br>`05:21` same
<br>`05:21` now you zoom in and you would wouldn't
<br>`05:24` be able to say whether this is a
<br>`05:25` snapshot a zoomed in version of the one
<br>`05:27` on the left hand side
<br>`05:29` or whether this is an entirely different
<br>`05:32` simulation
<br>`05:34` and then you can zoom in further and
<br>`05:35` further and
<br>`05:37` you again all the time get the same
<br>`05:39` impression that you can't really make
<br>`05:41` out
<br>`05:42` uh what is now the typical length how
<br>`05:44` large are these classes
<br>`05:46` you have here these domains of all sizes
<br>`05:49` equally now because you have domains
<br>`05:53` these white things or black things of
<br>`05:55` all
<br>`05:56` size is equally represented you can't
<br>`05:59` make out a single sound you can't make a
<br>`06:01` typical
<br>`06:02` length scale here because you can't say
<br>`06:04` that
<br>`06:06` the typical size of such a cluster here
<br>`06:10` is for example that large
<br>`06:13` as you always find clusters that are
<br>`06:15` much smaller you find glasses that are
<br>`06:17` much
<br>`06:17` larger here's a cluster now that has the
<br>`06:20` size of the entire system that's
<br>`06:22` infinitely large
<br>`06:23` and then you have all a spectrum of
<br>`06:26` sizes in between that
<br>`06:28` yeah well here in this example you kind
<br>`06:31` of get an idea
<br>`06:33` that these clusters are typically very
<br>`06:35` small
<br>`06:36` these domains whereas pin points up or
<br>`06:38` so are very small they have a
<br>`06:40` typical size but you can't see it on the
<br>`06:42` left hand side
<br>`06:44` yeah same as if i would zoom in with
<br>`06:46` this camera you know so
<br>`06:49` if we do like this now you immediately
<br>`06:52` see
<br>`06:53` that i zoomed in now because i have a
<br>`06:56` characteristic size i'm
<br>`06:57` one meter 80 or something yeah and now
<br>`07:00` you
<br>`07:00` see that you that have zoomed in the
<br>`07:02` camera and the picture is not the same
<br>`07:04` as before
<br>`07:06` so i'm not in a critical state yeah but
<br>`07:09` the icing system is in a critical state
<br>`07:12` and this critical state is characterized
<br>`07:15` by self-similarity
<br>`07:17` so they have structures of all sizes
<br>`07:19` represented
<br>`07:21` in this system now this is the
<br>`07:23` self-similarity
<br>`07:24` and the mathematical representation of
<br>`07:27` the self-similarity
<br>`07:28` the fact that you don't have an average
<br>`07:30` cluster size
<br>`07:32` is that the correlation length diverges
<br>`07:35` now so the correlation length is
<br>`07:37` infinity
<br>`07:38` that means the correlation function you
<br>`07:41` know
<br>`07:41` so how that represents how large
<br>`07:45` these clusters are is scale in variance
<br>`07:48` that means
<br>`07:49` that really classes of different sizes
<br>`07:51` are equally represented
<br>`07:53` and such if you ask what is the
<br>`07:55` probability that i
<br>`07:56` am now in a white cluster that i'm in a
<br>`07:59` black cluster a certain distance away
<br>`08:01` then the answer to this doesn't depend
<br>`08:03` on any specific distance
<br>`08:05` you know it's the same this probability
<br>`08:07` is the same this
<br>`08:08` correlation function here it's the same
<br>`08:11` when we
<br>`08:12` calculated in the original version of
<br>`08:15` the simulation or a zoomed in
<br>`08:17` uh fraction of this this is the
<br>`08:19` self-similarity
<br>`08:21` the self-similarity at a critical point
<br>`08:23` goes along with power laws
<br>`08:26` you know so the power laws have the um
<br>`08:30` for example like this here the critical
<br>`08:31` length as you go the critical
<br>`08:34` correlation length as you go closer to
<br>`08:37` the
<br>`08:37` critical point diverges to infinity it
<br>`08:40` goes to infinity
<br>`08:42` and it does so with an exponent that's
<br>`08:44` to be
<br>`08:45` called new when this gets zero here
<br>`08:49` this term will be infinity and these
<br>`08:51` exponents
<br>`08:52` capture how fast you go to infinity
<br>`08:56` and these exponents are very the fact
<br>`08:58` that you have an exponent but
<br>`08:59` that you have such a power rule means
<br>`09:02` that yourself similar you have a power
<br>`09:04` law if you have
<br>`09:06` something like this you can zoom in and
<br>`09:08` you still have the same exponent here
<br>`09:10` and you can't do that with an
<br>`09:11` exponential function or so
<br>`09:14` now and it also tells you that this is
<br>`09:17` here
<br>`09:18` uh if you have power laws from some
<br>`09:20` distribution that goes over
<br>`09:22` that has a power law that has this long
<br>`09:25` tail some exponent you cannot typically
<br>`09:29` calculate averages or moments because
<br>`09:31` these integrals diverge
<br>`09:34` now you have the power law of the
<br>`09:35` correlation function and you have a
<br>`09:38` power law
<br>`09:38` now if you have a power of the
<br>`09:39` correlation function you also have the
<br>`09:41` power laws
<br>`09:42` for example in the density and the
<br>`09:44` magnetization
<br>`09:46` uh near the critical point and all kinds
<br>`09:48` of other thermodynamic
<br>`09:50` quantities and i just wanted to briefly

### slide 3

<br>`09:53` show you why this is the case
<br>`09:55` now it's actually the background of this
<br>`09:58` the background of this is actually an
<br>`09:59` assumption
<br>`10:01` that you say you have a free energy
<br>`10:05` and with this free energy uh
<br>`10:08` this free energy as you go to the
<br>`10:10` critical pound point uh
<br>`10:11` gets in finite it has singularity
<br>`10:15` and then you say that you assume
<br>`10:19` that the free energy here
<br>`10:23` this free energy has
<br>`10:26` one part that has all the physics and
<br>`10:29` all the details a regular part
<br>`10:32` but you say that the part of the free
<br>`10:33` energy that
<br>`10:35` diverges at a critical point
<br>`10:39` this one here so now it's is a
<br>`10:44` t t
<br>`10:46` is something like t minus
<br>`10:50` t c over t you know and h
<br>`10:53` is the external field if you have
<br>`10:56` something like this as a free energy as
<br>`10:58` the function of these parameters
<br>`11:00` yeah then the singular part the one that
<br>`11:03` goes to infinity
<br>`11:05` is a homogeneous function
<br>`11:08` homogeneous function just uh tells you
<br>`11:12` that if you have f of
<br>`11:15` lambda x that this is equal to
<br>`11:18` lambda to the power of some alpha
<br>`11:22` f on x yeah and this represents that
<br>`11:25` just this these gains zooming in you
<br>`11:28` have the same function you zoom in where
<br>`11:29` you rescale your variable
<br>`11:31` you zoom in and you get the same
<br>`11:33` function back
<br>`11:34` now this is a homogeneous function and
<br>`11:37` you still assume that this free energy
<br>`11:39` density in this case is a homogeneous
<br>`11:42` function
<br>`11:43` and this homogeneous function can only
<br>`11:45` depend
<br>`11:46` on dimensionless quantities now for
<br>`11:49` example
<br>`11:50` you wouldn't expect this divergence to
<br>`11:53` infinity
<br>`11:54` to depend on how you measure a length
<br>`11:58` now whether you measure the length in
<br>`12:01` units of centimeters or meters
<br>`12:04` whether you measure temperature in
<br>`12:07` kelvin or in units of one kelvin or two
<br>`12:10` kelvins or so
<br>`12:12` so you can see you these kind of things
<br>`12:15` these units
<br>`12:15` dimensions should be irrelevant for how
<br>`12:18` this quantity goes to infinity
<br>`12:22` yeah and if we say that then we say okay
<br>`12:24` so we have
<br>`12:26` here so-called scaling function that
<br>`12:29` depends on dimensional parameter
<br>`12:31` a dimensional dimensionless
<br>`12:34` combinations of our parameters so the
<br>`12:37` external field
<br>`12:38` divided to the temperature and then we
<br>`12:40` have to
<br>`12:41` take the temperature to some power of
<br>`12:43` something
<br>`12:45` to make everything dimensionless
<br>`12:48` so that it has no units no and there's
<br>`12:51` something that's not
<br>`12:52` something we don't know yeah and
<br>`12:56` this has the free energy has some units
<br>`12:59` therefore the whole thing gets doesn't
<br>`13:01` have the units you need a pre-factor
<br>`13:04` that gives you the right units you know
<br>`13:06` and then
<br>`13:08` you have this alpha which we don't know
<br>`13:11` yeah
<br>`13:11` this is some exponent that depends on
<br>`13:13` the specific model
<br>`13:14` for example for the eisenmann zero
<br>`13:17` you know and then you have these uh this
<br>`13:20` is the
<br>`13:21` consequence of how you translate this
<br>`13:23` homogeneity
<br>`13:25` here of the free energy to something
<br>`13:28` that you give names
<br>`13:29` as you have here this part that diverges
<br>`13:32` yeah that has the units
<br>`13:34` and this part here is the so-called
<br>`13:37` scaling function
<br>`13:38` that only depends on dimensionless
<br>`13:40` parameters
<br>`13:41` and it turns out that these exponents
<br>`13:43` and this scaling function are universal
<br>`13:45` so if you know it for one model then you
<br>`13:47` know it will know it
<br>`13:49` you will know it for a very large class
<br>`13:52` and we'll see that once we do
<br>`13:53` renormalization later today
<br>`13:57` so uh so what does it mean yeah so if we
<br>`13:59` make this
<br>`14:00` assumption that's really an assumption
<br>`14:02` about
<br>`14:04` homogeneity of the free energy then we
<br>`14:07` can calculate for example
<br>`14:09` the magnetization m of th
<br>`14:12` now this is in thermodynamics something
<br>`14:14` like
<br>`14:16` del f 2 del h
<br>`14:19` you know and then we just plug this in
<br>`14:22` and we get something like temperature
<br>`14:25` this reduced temperature
<br>`14:27` t to the power of minus 2 minus alpha
<br>`14:30` means
<br>`14:30` minus delta some other function that we
<br>`14:34` don't know
<br>`14:35` that again depends on a dimensionless
<br>`14:40` parameter and then
<br>`14:44` this scales like some better that's the
<br>`14:47` definition
<br>`14:48` of this exponent better of the
<br>`14:50` magnetization
<br>`14:52` yeah and uh so in thermodynamics this is
<br>`14:55` called
<br>`14:56` **rhythm scaling** basically in any textbook
<br>`14:59` on statistical physics
<br>`15:00` and it's just just to show you how the
<br>`15:04` assumption
<br>`15:05` of homogeneity near the critical point
<br>`15:09` leads to power laws in other
<br>`15:11` thermodynamic quantities
<br>`15:13` i've shown you here the magnetization
<br>`15:17` this was the magnetization
<br>`15:23` but the same holds true for example for
<br>`15:26` susceptibility
<br>`15:27` and other thermodynamic quantities that
<br>`15:29` you can get by taking derivatives of
<br>`15:31` your
<br>`15:32` energy so
<br>`15:35` this homogeneity or this self-similarity
<br>`15:39` that i showed you here that is a
<br>`15:41` reflection that is one of the hallmarks
<br>`15:44` of uh critical behavior and that's what
<br>`15:47` we're looking for when we look for
<br>`15:49` critical behavior
<br>`15:50` and now the question is can we see
<br>`15:53` something like this
<br>`15:55` also a non-equilibrium system

### slide 4

<br>`15:58` before before i start with that
<br>`16:01` uh let's just have a look at one
<br>`16:02` specific how this scaling
<br>`16:04` behaves if you look at these equations
<br>`16:08` here
<br>`16:10` what does it mean it means that
<br>`16:13` actually the curves that you get you
<br>`16:16` know so if you just divide so once you
<br>`16:19` make a measurement for example with a
<br>`16:21` known temperature
<br>`16:23` and a known magnetic field you measure
<br>`16:26` this function here
<br>`16:28` then you know that it doesn't depend
<br>`16:29` separately
<br>`16:31` on the age and the temperature
<br>`16:35` so you can rescale your axis so this is
<br>`16:37` what is your y
<br>`16:38` x axis you can use that your x axis and
<br>`16:41` your y
<br>`16:42` axis to make all of these curves
<br>`16:46` collapse onto each other yeah and this
<br>`16:49` is this uh
<br>`16:50` scaling form that we see in equilibrium
<br>`16:54` physics this is for the icing model
<br>`16:56` so on the x-axis we have this scaled
<br>`16:58` temperature
<br>`16:59` that would be t on the previous slide
<br>`17:02` lowercase t
<br>`17:04` uh times something so this is v scale
<br>`17:08` and then these uh people in these
<br>`17:11` experiments
<br>`17:12` for uh for
<br>`17:15` for a ferro ferromagnet measured
<br>`17:18` the magnetization for different values
<br>`17:20` of the
<br>`17:22` of different experimental parameter
<br>`17:24` values
<br>`17:25` like magnetic field external magnetic
<br>`17:27` field temperature
<br>`17:30` and by making use of this formula here
<br>`17:33` you see that uh the scaling
<br>`17:37` behavior what is where is my
<br>`17:40` is it going down here yeah that's the
<br>`17:42` scaling behavior here
<br>`17:45` yeah that the only thing
<br>`17:49` that you don't know is this g of m that
<br>`17:52` you have to measure
<br>`17:53` yeah once you know the h and the
<br>`17:56` temperature
<br>`17:58` you can make all of these different g of
<br>`18:00` m's the gms
<br>`18:02` this scaling function you can rescale
<br>`18:05` these axes
<br>`18:06` to make them collapse onto each other
<br>`18:09` yeah and this is this observation this
<br>`18:11` is how you observe
<br>`18:12` scaling an experiment so you manage to
<br>`18:15` collapse
<br>`18:16` your experimental curves by multiplying
<br>`18:19` this x-axis and the y-axis with certain
<br>`18:23` values
<br>`18:23` of offense you have to guess you can
<br>`18:27` collapse all of these curves on the same
<br>`18:30` uh universal so-called scaling form
<br>`18:34` now this is the manifestation of scaling
<br>`18:36` and that's of course
<br>`18:37` also something we'll be looking at and
<br>`18:39` non-equilibrium systems
<br>`18:41` but also in data
<br>`18:44` now scaling is a whole mark of critical
<br>`18:48` behavior and today

### slide 5

<br>`18:52` we want to see whether these concepts
<br>`18:56` of scaling and criticality yeah
<br>`18:59` where and these these continuous
<br>`19:02` phase transitions actually also extend
<br>`19:05` to non-equilibrium systems
<br>`19:07` yeah and it turns out so now we first we
<br>`19:10` need to find a non-equilibrium system
<br>`19:12` that is as intuitive
<br>`19:15` as the ising model and the icing model
<br>`19:18` is very intuitive
<br>`19:19` you have that in your lectures when
<br>`19:21` you're a student and
<br>`19:22` in your later life as a scientist you
<br>`19:24` always refer to that because it's so
<br>`19:26` simple and intuitive that uh you can
<br>`19:28` explain a lot of things a lot of
<br>`19:30` things about continuous phase
<br>`19:32` transitions in equilibrium
<br>`19:33` just based on this very simple model
<br>`19:35` like i did in the beginning of this
<br>`19:37` lecture
<br>`19:38` and it turns out now that the uh
<br>`19:41` icing model of non-equilibrium physics
<br>`19:44` of course is
<br>`19:46` that so people would dig a disagree but
<br>`19:48` one of the simplest models in
<br>`19:49` mono-equilibrium physics that shows
<br>`19:52` critical behavior
<br>`19:53` is an epidemic model and this epidemic
<br>`19:56` model we knew already
<br>`19:57` from the previous lectures here we have
<br>`20:02` our good old si model again
<br>`20:06` now so this epidemic model is this is
<br>`20:08` the simplest model
<br>`20:10` that you can think about so you have
<br>`20:11` infected individuals
<br>`20:14` i and susceptible individuals or
<br>`20:17` healthier people's less
<br>`20:19` now if an i meets an s
<br>`20:22` then the s gets infected with the rate
<br>`20:25` say lambda half
<br>`20:27` and turns into an affected infidel and
<br>`20:30` in the end you have two of them
<br>`20:33` then you have the other process that we
<br>`20:34` recover
<br>`20:36` and we set this rate to one now we can
<br>`20:38` just set that to one
<br>`20:40` without any loss of generality and uh
<br>`20:43` so that infected we measure units
<br>`20:46` time in units of this recovery rate
<br>`20:50` you know service infected individuals
<br>`20:52` can also
<br>`20:54` then recover and become
<br>`20:57` healthy again we have these two kinds of
<br>`21:00` individuals
<br>`21:01` and now we put them in the real world so
<br>`21:04` last time we were only looking at some
<br>`21:06` well-mixed
<br>`21:07` average quantities but now we put them
<br>`21:10` into the real world like the city of
<br>`21:11` brisbane also
<br>`21:13` where they actually can where actually
<br>`21:16` space
<br>`21:17` matters yeah so i'm more likely to
<br>`21:19` infect somebody else working at the
<br>`21:22` mp rpk pks than somebody looking at
<br>`21:25` another max planck institute for example
<br>`21:28` yeah so
<br>`21:29` so here uh these spatial structures
<br>`21:32` these special degrees of freedom
<br>`21:34` uh are taken into account and the
<br>`21:36` simplest way of you
<br>`21:38` how you can think about this is at the
<br>`21:40` bottom here
<br>`21:42` now that you look at letters
<br>`21:45` you have a letters each site
<br>`21:48` carries either an affected individual or
<br>`21:51` a recovered individual and
<br>`21:55` you know an infected or a recovered
<br>`21:56` individual and
<br>`21:58` when an infected individual
<br>`22:02` is next to a recovered a healthy one
<br>`22:05` then
<br>`22:05` the healthy one can turn into an
<br>`22:07` infected one
<br>`22:09` with a certain probability of with a
<br>`22:10` certain rate lambda over two
<br>`22:13` yeah and also there's another process
<br>`22:16` here if i saw if the
<br>`22:18` individual on a certain position is
<br>`22:21` infected
<br>`22:21` it can turn into a healthy one at a rate
<br>`22:24` lambda
<br>`22:26` so this is this simple spatial version
<br>`22:29` that you can think about for this and
<br>`22:32` simple epidemic model and it's also the
<br>`22:35` literature is often called the contact
<br>`22:38` process
<br>`22:40` so of course real epidemic model models
<br>`22:43` have
<br>`22:44` typically one more component namely the
<br>`22:47` um
<br>`22:49` [Music]
<br>`22:51` the infected recovered uh wait
<br>`22:54` is this also here okay so so the third
<br>`22:57` component that you normally have
<br>`22:59` and these models are the recovered one
<br>`23:01` the immune people
<br>`23:02` now you have the disease yeah and then
<br>`23:04` you are fine for the rest of your life
<br>`23:06` and you're immune to this disease
<br>`23:08` so you can only forget in fact one then
<br>`23:11` you have a third
<br>`23:12` species here a third kinds of particles
<br>`23:15` which would be the recovered ones
<br>`23:17` or the immune ones and they cannot be a
<br>`23:21` faculty again
<br>`23:22` but this slightly more complicated model
<br>`23:25` uh is shows very similar behavior to the
<br>`23:28` model that we're studying here
<br>`23:31` for the things that we're interested in
<br>`23:32` so here we're interested in infinities
<br>`23:34` in singularities so once you
<br>`23:38` once you look at these kind of things
<br>`23:40` then these models will qualitatively the
<br>`23:42` same
<br>`23:43` although also the exponents will be
<br>`23:45` different
<br>`23:47` but once you look of course into
<br>`23:49` non-singularities it's more critical
<br>`23:51` behavior
<br>`23:52` than the messiness of how wide your
<br>`23:55` roads are
<br>`23:57` how often the tram goes uh between the
<br>`24:00` blasphemy institutes and so on these
<br>`24:02` things will matter
<br>`24:05` yeah but close to the critical point uh
<br>`24:07` we'll be fine

### slide 6

<br>`24:10` so this is a stochastic simulation of
<br>`24:13` such a system
<br>`24:14` and we can just see what happens on the
<br>`24:17` left hand side
<br>`24:18` you see a simulation of such a lattice
<br>`24:20` system
<br>`24:21` where you initially have random random
<br>`24:25` random initialization so every site
<br>`24:28` is either with the probability of one
<br>`24:30` half
<br>`24:32` a certain probability infected or
<br>`24:35` not infected and what you see here
<br>`24:39` now is in blue infected
<br>`24:42` individuals now if this lambda
<br>`24:46` now this infection rate is smaller
<br>`24:49` than a certain critical value
<br>`24:52` then what you will see is that this
<br>`24:54` infraction
<br>`24:55` this infection can spread for a while
<br>`24:58` but most of the time with a certain
<br>`24:59` probability
<br>`25:00` it will uh disappear
<br>`25:04` now so in this regime here in this phase
<br>`25:08` the recovery rate outweighs
<br>`25:11` the infection rate you know and
<br>`25:14` uh so that's what we're supposed to be
<br>`25:17` on in this regime we're supposed to be
<br>`25:19` investing
<br>`25:19` starting next week and then on the right
<br>`25:23` hand side
<br>`25:24` that's the regime that we're currently
<br>`25:26` in now then the infection rate
<br>`25:28` is larger than the uh
<br>`25:31` than the recovery rate now so the
<br>`25:33` infection probability is higher
<br>`25:36` and what you will then end up is is a
<br>`25:39` state where most of the individuals will
<br>`25:42` carry the disease will be infected
<br>`25:45` so you will you will reach a steady
<br>`25:47` state
<br>`25:49` not everybody is all the time in fact
<br>`25:50` that you will reach some steady state
<br>`25:52` with a certain percentage of infected
<br>`25:55` people
<br>`25:57` and now we have this situation in
<br>`26:00` between
<br>`26:02` that's this one here and this is
<br>`26:05` where the um where
<br>`26:08` the infection rate is more or less
<br>`26:11` balanced
<br>`26:12` with the recovery rate it's not exactly
<br>`26:15` equal to one
<br>`26:16` so that's these things are complicated
<br>`26:18` yeah you might think that
<br>`26:20` okay if this this lambda is equal to one
<br>`26:23` or one half or so
<br>`26:25` yeah then uh then that's the critical
<br>`26:27` point of these systems i'll show you are
<br>`26:29` more complicated than you might think
<br>`26:32` because the noise is so important here
<br>`26:35` and here
<br>`26:36` what you see is that you have domains
<br>`26:39` that become larger and larger over time
<br>`26:41` so from
<br>`26:42` when we go from top to bottom we have
<br>`26:43` time now so we go we start here at the
<br>`26:46` top
<br>`26:47` and then this domain goes large and
<br>`26:49` larger you have merging
<br>`26:51` of domains with infected individuals
<br>`26:54` and then we have branches that they die
<br>`26:56` out
<br>`26:57` like this one here and uh
<br>`27:00` it looks a little bit like a
<br>`27:02` self-similar state
<br>`27:04` now we have domains of all sizes for
<br>`27:07` example
<br>`27:08` in the time domain or from top to bottom
<br>`27:11` you have some branches that die out
<br>`27:13` quite quickly here
<br>`27:15` but then you have other branches like
<br>`27:17` the big one in the middle
<br>`27:19` where that just go on for uh forever
<br>`27:23` without really occupying the whole
<br>`27:24` system
<br>`27:26` and then if you look take a slice in
<br>`27:28` this direction here
<br>`27:30` these simulations are very small also
<br>`27:33` it's not like a design
<br>`27:34` you can't see that well you'll also see
<br>`27:36` that here you have
<br>`27:37` structures of all different sizes
<br>`27:41` there are small ones like this one here
<br>`27:44` yeah and the larger ones like this one
<br>`27:46` and so you have these structures of all
<br>`27:48` different sizes
<br>`27:51` and this is again reminiscent of cell
<br>`27:53` similarity
<br>`27:54` and the critical point so it turns out
<br>`27:57` our little empiric model has a critical
<br>`28:00` point
<br>`28:00` can i ask a question um i i think i
<br>`28:04` roughly understand the model
<br>`28:06` but this simulation is the simulation of
<br>`28:08` what
<br>`28:09` so is it a hamiltonian system where the
<br>`28:12` um just yes so what is this basically
<br>`28:15` nothing
<br>`28:16` yeah so uh you just take what it is here
<br>`28:19` or you take that just this year the way
<br>`28:21` here that you write these simulations
<br>`28:23` the different ways to write them you
<br>`28:25` have a lattice you know you have a
<br>`28:26` numerical simulation you have a vector
<br>`28:28` an array and you either have like
<br>`28:31` one or zero and then you pick a side
<br>`28:35` randomly
<br>`28:36` and perform these reactions here
<br>`28:39` you know so so the one way to do that is
<br>`28:41` to pick a side randomly
<br>`28:44` and check if your neighbors overcome if
<br>`28:45` you pick this side
<br>`28:47` and if your neighbor is susceptible or
<br>`28:49` it does not is not infected
<br>`28:52` then you infect the neighbor with the
<br>`28:53` probability
<br>`28:55` lambda over two so like a monte carlo
<br>`28:58` simulation it's a monte carlo simulation
<br>`29:00` the different ways you can also think of
<br>`29:02` a cellular automaton
<br>`29:04` yeah but uh the typical way to simulate
<br>`29:06` these things are multicolored
<br>`29:08` simulations
<br>`29:09` okay but there's no hamiltonian there's
<br>`29:10` no deeper insight you can just take
<br>`29:12` these rules
<br>`29:13` and simulate them on a lattice and the
<br>`29:15` only thing you have to do
<br>`29:16` is to take into account that this is not
<br>`29:19` a deterministic process here
<br>`29:21` but it's a random process with a
<br>`29:23` probability one-half
<br>`29:25` you turn this one here lambda over two
<br>`29:27` you turn this one here
<br>`29:29` into an infected blue one can i then
<br>`29:32` properly
<br>`29:33` um make a make a statement about the
<br>`29:36` **time scale** how
<br>`29:37` some how this thing spreads because it's
<br>`29:40` it's random right so i can
<br>`29:44` that's what we'll be trying to do today
<br>`29:47` okay uh but we'll
<br>`29:48` uh only be managing to do that tomorrow
<br>`29:50` uh let me just go on
<br>`29:52` so here you get some kind of idea
<br>`29:55` already
<br>`29:56` in this slide here you can get us some
<br>`29:58` kind of idea here so that
<br>`30:00` that you have here a time scale yeah
<br>`30:03` it's not
<br>`30:04` where things uh where things uh
<br>`30:06` disappear
<br>`30:08` yeah so you say that for example here
<br>`30:10` the typically the
<br>`30:12` the number of infected individuals will
<br>`30:14` go down with an exponential function
<br>`30:17` yeah and then this has a typical time
<br>`30:18` and then you get rid of most of the
<br>`30:20` infected ones
<br>`30:22` this has some certain time at this
<br>`30:25` typical
<br>`30:25` this certain time where you say okay
<br>`30:29` at this time i'm i have lost most of my
<br>`30:31` infected
<br>`30:32` people now that they're healthy again
<br>`30:35` this is then called
<br>`30:36` psi parallel
<br>`30:39` yeah so this is like a correlation
<br>`30:41` length so i'm actually actually getting
<br>`30:43` a hat a little bit too far so so this
<br>`30:45` you have here a correlation length in
<br>`30:47` time
<br>`30:48` but that tells you exactly that how f
<br>`30:51` how quickly
<br>`30:52` does this disease disappear
<br>`30:55` yes you have a correlation length in
<br>`30:57` space like this
<br>`30:59` so for example this one here
<br>`31:03` now our analysis is it depends on how
<br>`31:05` you define it it can relate to that
<br>`31:07` uh this is typically called psi
<br>`31:10` perpendicular
<br>`31:12` you have a correlation length in space
<br>`31:13` now that tells you how large are your
<br>`31:15` clusters
<br>`31:16` but you also have a correlation length
<br>`31:18` and time how long
<br>`31:20` lived are your clusters how long does it
<br>`31:23` take for them to disappear
<br>`31:25` and it turns out that both of these
<br>`31:27` things at the critical point are
<br>`31:29` infinite
<br>`31:30` so the system is not only self-similar
<br>`31:32` in space but also in time
<br>`31:37` yeah but first before we before we do
<br>`31:39` that um
<br>`31:40` uh before we do that formally so what i
<br>`31:43` see here
<br>`31:44` is is the stochastic simulation uh we'll
<br>`31:46` later
<br>`31:48` motivate some larger equation that we
<br>`31:50` actually will be studying
<br>`31:52` but for now now the system is as simple
<br>`31:54` as it gets now you have a neighbor
<br>`31:56` if this neighbor is not infected you
<br>`31:58` infect it with a certain probability
<br>`32:00` yeah it's the simplest there's like five
<br>`32:03` lines of code also
<br>`32:04` in matlab now there's nothing there's
<br>`32:08` nothing
<br>`32:09` uh in terms of the simulation the modal
<br>`32:11` definition is nothing
<br>`32:12` that is nothing deep in there but of
<br>`32:15` course the consequences as we see on the
<br>`32:16` slide
<br>`32:17` are rather non-trivial

### slide 7

<br>`32:22` so now we want to go one step
<br>`32:26` ahead and try to formalize this
<br>`32:29` mathematically
<br>`32:32` and um to formalize this we first need
<br>`32:36` to
<br>`32:36` have something to put into our larger
<br>`32:39` equation
<br>`32:40` yeah and that something that we put into
<br>`32:42` our laundry equation
<br>`32:44` is the density of this or this order
<br>`32:47` parameter
<br>`32:49` is the density of infected
<br>`32:52` individuals all right to get this we uh
<br>`32:58` um we we do a double average
<br>`33:02` so this average here is over the lattice
<br>`33:06` now we sum over the letters and we count
<br>`33:10` now with this si variable like a spin
<br>`33:14` how many infected individuals we have
<br>`33:17` and divide it by the total number of
<br>`33:19` lattice sites
<br>`33:20` the system size and then we average
<br>`33:23` again
<br>`33:23` over the ensemble now this is our order
<br>`33:26` parameter and this parameter this order
<br>`33:28` parameter
<br>`33:29` tells us whether we have order or not
<br>`33:33` you know if this is one then everybody
<br>`33:35` is infected
<br>`33:36` yeah it's not or not order or not if
<br>`33:38` this is one
<br>`33:39` everybody's infected and if this is zero
<br>`33:42` then everybody is healthy
<br>`33:45` so this is our like our magnetization
<br>`33:48` and now
<br>`33:49` we want to do the same thing as an
<br>`33:52` equilibrium
<br>`33:53` i also want to ask what are we actually
<br>`33:56` looking at yeah so
<br>`34:00` what we say is we don't know
<br>`34:04` but we make the assumption
<br>`34:07` that in this non-equilibrium critical
<br>`34:10` point
<br>`34:11` we also have scaling behavior and we
<br>`34:14` also have self-similarity
<br>`34:16` now and of course you can test this
<br>`34:18` assumption if you do large enough
<br>`34:20` computer simulations
<br>`34:22` so one thing is that this
<br>`34:25` if our system obtains a steady state
<br>`34:28` with some density
<br>`34:30` you know so that's a row
<br>`34:33` stationary density something like the
<br>`34:36` magnetization you know the process of 90
<br>`34:39` of the people
<br>`34:40` are infected uh
<br>`34:43` this goes with
<br>`34:48` lambda minus lambda c to the power
<br>`34:51` of beta it's like the magnetization we
<br>`34:54` don't know what beta is
<br>`34:56` but there is some better that we want to
<br>`35:00` know
<br>`35:02` now as i've discussed already before we
<br>`35:04` have now not just
<br>`35:05` one correlation length but two so one is
<br>`35:08` the spatial
<br>`35:13` correlation length
<br>`35:18` and this is typically denoted by psi
<br>`35:21` perpendicular
<br>`35:22` because it's perpendicular to time and
<br>`35:26` perpendicular so if you look at these
<br>`35:28` pictures here
<br>`35:30` you can kind of get an idea
<br>`35:33` why this is called perpendicular and
<br>`35:35` parallel
<br>`35:37` suppose that this is here whether this
<br>`35:39` actually an
<br>`35:40` equivalent model is the one of water
<br>`35:43` pouring
<br>`35:44` into soil you know so you have little
<br>`35:48` channels
<br>`35:48` it's a rough thing yeah and then for
<br>`35:51` example here
<br>`35:52` the water flows down
<br>`35:56` but at some point now the density of the
<br>`35:59` soil is too large
<br>`36:00` and the water stops this is
<br>`36:03` this is an example where the soil is
<br>`36:05` like the soil is like
<br>`36:06` it's very open it's not very dense you
<br>`36:09` put water in it
<br>`36:10` and it flows all the way to the bottom
<br>`36:13` so that's
<br>`36:14` what is what is sorry yes um you said
<br>`36:17` that
<br>`36:19` in case of critical systems the
<br>`36:20` correlation length in space can be
<br>`36:22` divergent
<br>`36:24` yes and also the correlation length in
<br>`36:27` time could be divergent
<br>`36:28` yes so if the correlation length in time
<br>`36:31` is divergent then in this specific
<br>`36:33` example
<br>`36:35` the it'll the number of infected
<br>`36:38` clusters will always be present
<br>`36:40` right yes exactly you will not you will
<br>`36:43` never get rid of this
<br>`36:44` disease but of course this infinities
<br>`36:47` when i talk about infinity
<br>`36:49` these infinities are not defined really
<br>`36:52` in this small simulation where we maybe
<br>`36:54` have
<br>`36:54` 100 individuals also now these
<br>`36:57` infinities are defined for
<br>`36:58` systems that don't really have an
<br>`37:00` infinite infinitely large size
<br>`37:03` now this here what you see the
<br>`37:05` simulation in the middle
<br>`37:07` can just by chance disappear
<br>`37:11` and it will disappear and i can tell you
<br>`37:15` even that the disease in this case here
<br>`37:18` the right hand side will disappear with
<br>`37:21` a very small probability
<br>`37:23` right so it's a very nice feature of
<br>`37:25` this model that will turn out to be very
<br>`37:28` important
<br>`37:29` what happens if all individuals
<br>`37:32` are healthy what happens if all
<br>`37:36` individuals are healthy
<br>`37:39` then there's no process here
<br>`37:44` there are only s's there's no process
<br>`37:46` here that can give you the disease back
<br>`37:49` once the disease is extinct
<br>`37:52` it will never come back and because this
<br>`37:55` is a stochastic system
<br>`37:57` you just have to wait long enough and
<br>`37:59` just by chance
<br>`38:01` even this is casey on the right hand
<br>`38:03` side will turn into the
<br>`38:05` case just because it's stochastic just
<br>`38:08` by chance
<br>`38:09` maybe you have to wait 100 billion years
<br>`38:11` or so for this to happen but you know
<br>`38:13` that at some point you will end up in
<br>`38:15` this state
<br>`38:17` where the disease went extinct by chance
<br>`38:20` you have to wait extremely long for that
<br>`38:22` but you know that it will happen
<br>`38:24` and these states here now like in this
<br>`38:27` system here
<br>`38:28` you go to zero and then there's no way
<br>`38:30` it can come back
<br>`38:32` yeah in reality you will have to wait
<br>`38:34` for evolution
<br>`38:36` to create another virus that has the
<br>`38:39` same properties
<br>`38:40` now to come back so that texas goes
<br>`38:42` extremely long
<br>`38:43` yeah it's a much it's much longer than
<br>`38:45` the spreading of the disease itself it
<br>`38:47` happens in one or two years
<br>`38:50` you know and so these are called
<br>`38:52` absorbing states you can go in there
<br>`38:54` but you can never go out again
<br>`38:58` so in other words this means that in
<br>`39:00` these absorbing states
<br>`39:02` they're very important for not only for
<br>`39:03` virus spreading but in any ecological
<br>`39:05` model
<br>`39:06` now we have extinction and this
<br>`39:09` absorbing states
<br>`39:10` uh you can get in but you will never be
<br>`39:12` able to get out
<br>`39:14` now once you're in there you're trapped
<br>`39:16` and these absorbing states they don't
<br>`39:18` have
<br>`39:19` fluctuations they don't have any noise
<br>`39:21` and we'll see that in the larger
<br>`39:22` equation you know so these absorbing
<br>`39:25` states don't have any noise
<br>`39:28` and by this you can already see that
<br>`39:30` this whole system
<br>`39:31` is a non-equilibrium system because if
<br>`39:34` you have a state that has no noise
<br>`39:36` this is not a thermal system where you
<br>`39:38` have a temperature
<br>`39:40` now so this here is a system where you
<br>`39:41` have noise now for example here you have
<br>`39:44` noise but once you reach the state
<br>`39:47` where there's no disease no virus left
<br>`39:51` you don't have any noise anymore you
<br>`39:54` know and that cannot happen in a
<br>`39:55` thermodynamic system that is an
<br>`39:57` equilibrium
<br>`39:58` that you always have your temperature
<br>`40:00` and this will always give you noise
<br>`40:01` regardless of how many
<br>`40:03` particles you have or whatever yeah so
<br>`40:06` this already tells you that this is a
<br>`40:07` non-equilibrium system
<br>`40:09` and it's a very interesting system and
<br>`40:11` the system is actually one of the
<br>`40:13` universality classes non-equilibrium
<br>`40:15` physics
<br>`40:16` so that's once you are getting a little
<br>`40:19` bit ahead
<br>`40:20` once you know that your system has one
<br>`40:22` absorbing state
<br>`40:24` many ecological systems for example one
<br>`40:26` absorbing state
<br>`40:28` then it's quite likely that what i'll
<br>`40:29` show you in these
<br>`40:31` uh renewalization calculations today and
<br>`40:34` next week
<br>`40:35` will also apply to these systems is a
<br>`40:37` very powerful
<br>`40:38` you know universality class and
<br>`40:40` universal system
<br>`40:42` for non-equilibrium systems
<br>`40:45` yeah but let's let's i was here talking
<br>`40:47` about did i actually answer your
<br>`40:49` question so i got a little bit
<br>`40:50` uh distracted uh i i distracted myself
<br>`40:55` a little bit yeah did i do that
<br>`40:58` okay okay i i forgot it at the end i
<br>`41:01` forgot this question but i hope i
<br>`41:02` answered it at some point
<br>`41:04` okay so you have the two correlations
<br>`41:06` just spatial correlation length
<br>`41:07` you know that's uh sigma
<br>`41:11` uh side perpendicular and actually
<br>`41:14` what i want to say here is actually
<br>`41:16` that's that's what i would say
<br>`41:18` yeah so you have here you have soul and
<br>`41:20` you have water
<br>`41:21` flowing through this then the parallel
<br>`41:23` length here
<br>`41:26` this one it's called parallel because
<br>`41:28` it's parallel to the direction of
<br>`41:29` gravitation
<br>`41:31` and the other length here is
<br>`41:34` perpendicular because it's perpendicular
<br>`41:36` to the
<br>`41:37` direction of gravitation now that's
<br>`41:38` where these names come from
<br>`41:40` because these models called direct or
<br>`41:42` the directed percolation
<br>`41:44` is that you have something flowing
<br>`41:47` through a rough
<br>`41:48` medium like soil and then you have a
<br>`41:51` direct gravitation force that pulls the
<br>`41:54` fluid into one direction
<br>`41:55` but not in the other direction and
<br>`41:57` that's where these parallel and
<br>`41:58` perpendicular
<br>`42:00` yeah so and then we give that some
<br>`42:02` exponent
<br>`42:04` lambda minus lambda c to the power of
<br>`42:08` minus
<br>`42:09` mu perpendicular
<br>`42:12` now that we have the temporal or dynamic
<br>`42:22` correlation length
<br>`42:25` side parallel and this
<br>`42:28` we call and very surprisingly minus
<br>`42:32` new parallel
<br>`42:35` and this is now as you said so
<br>`42:38` our temporal correlation can become
<br>`42:41` infinity
<br>`42:42` what does it mean yeah so i have a
<br>`42:45` perturbation
<br>`42:46` to the system so what so if you have a
<br>`42:49` the spatial correlation and infinity
<br>`42:52` like an isomorph
<br>`42:53` you make a perturbation and this
<br>`42:56` perturbation will in principle
<br>`42:58` affect all parts of the magnet
<br>`43:01` yeah you will have a very very long
<br>`43:03` range correlation you flip a spin
<br>`43:05` somewhere
<br>`43:05` and it has an effect somewhere
<br>`43:07` completely somewhere else
<br>`43:10` now we have an infinite correlation
<br>`43:13` length
<br>`43:13` in time what does that mean so that
<br>`43:16` means that if we perturb the system we
<br>`43:18` are at a critical point
<br>`43:19` we will perturb the system and the time
<br>`43:23` that it takes the system to go back to
<br>`43:26` forget this perturbation
<br>`43:27` is infinitely long yeah
<br>`43:30` so so you have again now processes in
<br>`43:33` all time scales and parallel
<br>`43:35` very long very slow process and also
<br>`43:37` infinitely long processes
<br>`43:39` yeah it's like like the space in the
<br>`43:41` isis mode you have classes of all
<br>`43:43` different sizes now you have also
<br>`43:44` processes
<br>`43:45` of all different length scales at the
<br>`43:48` same time
<br>`43:49` now and this is what this criticality
<br>`43:51` does to time
<br>`43:52` the time domain you make it perturbation
<br>`43:55` and it never just disappears again
<br>`43:57` that the effects of this particular
<br>`43:59` perturbation you will see in this system
<br>`44:01` infinitely long now so that's the cool
<br>`44:04` thing about critical systems that does
<br>`44:06` uh
<br>`44:08` it does uh they do very straight things
<br>`44:11` and then now we define another uh
<br>`44:15` i've got a question yes sorry is are we
<br>`44:18` still dealing with a mean field model
<br>`44:21` uh i i didn't tell you yet uh but we'll
<br>`44:24` we won't be dealing with the mean field
<br>`44:26` of model
<br>`44:27` yeah so mean field is not very good for
<br>`44:30` these kind of things
<br>`44:32` yeah so we're not uh we're not dealing
<br>`44:34` with the mean fit model
<br>`44:35` last last time last week we were dealing
<br>`44:37` with mean field models
<br>`44:39` but this time we have to take propaganda
<br>`44:41` fluctuations properly into account
<br>`44:44` and we will have also to take into
<br>`44:46` confluctuations on all
<br>`44:48` different temporal and spatial scales
<br>`44:51` you know so that's that's what we will
<br>`44:53` have to do and that's what we will uh do
<br>`44:55` with the renovation group
<br>`44:58` so mean field theory is typically pretty
<br>`45:00` bad for these things
<br>`45:03` even just for the getting what is this
<br>`45:05` lambda c i'm going to show you what this
<br>`45:06` lambda c is but this is
<br>`45:08` in the mean field version we would say
<br>`45:10` okay this is just one half or something
<br>`45:12` like this
<br>`45:12` yeah where you write down some
<br>`45:14` differential equation like you did last
<br>`45:16` time
<br>`45:16` you write you guess some differential
<br>`45:18` equation you motivate it
<br>`45:20` and then you get some lambda c but i'll
<br>`45:22` show you today
<br>`45:23` now that this is actually not how it
<br>`45:26` works if you have these
<br>`45:27` strong fluctuations to get different
<br>`45:29` results
<br>`45:31` okay so then we have a third exponent
<br>`45:35` the dynamic critical exponents
<br>`45:39` and that means that near lambda c near
<br>`45:42` the critical point
<br>`45:45` we say that uh these correlation lengths
<br>`45:49` now they they both follow power rules
<br>`45:52` you know and we say that they are
<br>`45:54` connected
<br>`45:55` by this exponent called z
<br>`45:59` and this is called
<br>`46:02` a dynamical
<br>`46:07` critical
<br>`46:11` exponent yeah so we what we did now
<br>`46:14` is okay we said okay these systems look
<br>`46:17` self-similar
<br>`46:18` uh like in equilibrium and we assume
<br>`46:21` that the same concepts of scaling
<br>`46:23` and power laws also apply to
<br>`46:26` non-equilibrium systems

### slide 8

<br>`46:30` and now i have a slide here that we
<br>`46:31` already talked about
<br>`46:33` this is just what are these correlation
<br>`46:35` lengths now so what are these
<br>`46:37` correlation uh
<br>`46:40` what are what are these correlation
<br>`46:41` lengths these two and we discussed that
<br>`46:44` basically already
<br>`46:45` and so if you look here on the right
<br>`46:49` hand side for example
<br>`46:51` so on the left hand side i have two
<br>`46:53` simulations
<br>`46:55` that were started from an initial seat
<br>`46:58` from this just one
<br>`46:59` infected individual and on the right
<br>`47:02` hand side
<br>`47:03` these figures uh they are from
<br>`47:06` assimilation
<br>`47:06` were maybe 50 percent of the letters
<br>`47:10` was infected you know other
<br>`47:13` simulations i didn't show you uh there's
<br>`47:16` a nice review
<br>`47:17` article by hindi uh
<br>`47:24` about a non-equilibrium criticality and
<br>`47:26` face transitions
<br>`47:28` and that's where it took this pair this
<br>`47:30` uh it's a very nice review
<br>`47:32` uh about the kind of things that we're
<br>`47:34` doing this week and next week
<br>`47:37` so here now we this is just an intuition
<br>`47:40` about what these correlation lengths are
<br>`47:42` uh i told you already you know that this
<br>`47:45` um that this temporal correlation length
<br>`47:49` side parallel gives you to say the time
<br>`47:52` that the disease
<br>`47:54` dies out as you can see that here
<br>`47:57` in this simulation here that the
<br>`47:59` parallel correlation length
<br>`48:01` that's the time for such a droplet here
<br>`48:04` to go away again now we know that
<br>`48:08` if we're below the critical point that
<br>`48:09` at some point it will disappear
<br>`48:12` and this has a typical time and this is
<br>`48:14` just the excite
<br>`48:16` parallel and then you have also a
<br>`48:18` typical size of such a droplet here
<br>`48:21` that's psi perpendicular that's just how
<br>`48:24` large
<br>`48:25` do these domains get and you can also
<br>`48:28` see that here on the right hand side of
<br>`48:29` course
<br>`48:30` how long does how large does the domain
<br>`48:33` of uninfected
<br>`48:34` or infected individuals get now there's
<br>`48:37` this one here and how long does it
<br>`48:39` survive
<br>`48:41` now that's how these correlation lengths
<br>`48:44` are to be
<br>`48:45` interpreted intuitively

### slide 9

<br>`48:49` okay now
<br>`48:53` i'm going to do a little step
<br>`48:57` uh that where i'm trying to avoid a long
<br>`49:02` calculation
<br>`49:05` what we usually would do now is we would
<br>`49:08` take this lattice model and we would
<br>`49:11` try to derive a master equation
<br>`49:15` and also this probability that the
<br>`49:17` lattice
<br>`49:18` has a certain configuration and then we
<br>`49:21` would be looking
<br>`49:22` at this master equation uh
<br>`49:25` this very complex master equation that
<br>`49:27` tells us the time evolution of this
<br>`49:29` vector and we try to get the rates
<br>`49:33` and then we would uh do approximations
<br>`49:36` uh like the system size expansion or the
<br>`49:38` chromosomes
<br>`49:39` expansion and so on and then we would
<br>`49:41` try to derive this large
<br>`49:43` which now that's a lengthy business and
<br>`49:46` it's not the subject of our
<br>`49:48` lecture what i just want to show you is
<br>`49:52` that why does this larger equation that
<br>`49:55` i'll show you
<br>`49:56` later not look like what you naively
<br>`49:59` would expect
<br>`50:01` to this end you can just show you that
<br>`50:03` such a letter
<br>`50:04` system you can interpret in different
<br>`50:06` ways
<br>`50:08` one way is to say that it won't give you
<br>`50:11` like
<br>`50:12` the mathematical rigorous form of the
<br>`50:14` larger equation but it shows you why
<br>`50:16` it looks not like you expect it to look
<br>`50:19` like
<br>`50:20` so the first way we can interpret
<br>`50:24` this lattice system is to say what
<br>`50:27` happens
<br>`50:28` at t and what is the state at some d
<br>`50:32` plus dt some like a very short time
<br>`50:35` interval after that
<br>`50:38` and now i'm taking like in this master
<br>`50:40` equation i'm taking the perspective
<br>`50:43` of the state in a certain site
<br>`50:48` and then ask what are the previous
<br>`50:51` states
<br>`50:52` that give rise to me being infected
<br>`50:57` you know what gives rises yeah and
<br>`51:00` suppose that i was not infected before
<br>`51:03` yeah then my left neighbor could have
<br>`51:05` been infected
<br>`51:07` my right neighbor could have been
<br>`51:09` infected or both of them could have been
<br>`51:12` infected
<br>`51:12` and have affected me these are the three
<br>`51:15` processes that
<br>`51:16` lead to me being infected and then
<br>`51:19` if it was there's another process
<br>`51:23` and i should use here different colors
<br>`51:25` it's not the recovery
<br>`51:35` i switched the colors not red is
<br>`51:39` healthy sorry
<br>`51:43` red is healthy and blue is infected
<br>`51:48` okay yeah if i in this recovery process
<br>`51:53` it doesn't matter what my neighbors were
<br>`51:54` i would just i just know that was
<br>`51:56` previously infected
<br>`51:57` if i'm now in the process of recovery
<br>`52:01` now this is this master equation picture
<br>`52:03` where we ask the word which state do i
<br>`52:04` come from
<br>`52:06` and now we can take an equivalent
<br>`52:09` description
<br>`52:10` and take more a lattice picture now that
<br>`52:13` corresponds more a little bit left to
<br>`52:14` the longer
<br>`52:15` picture yeah where update where i say
<br>`52:18` what is the state of the lattice now
<br>`52:20` and what is the state of the lattice the
<br>`52:21` next step
<br>`52:23` now that corresponds to this
<br>`52:24` differential equation picture
<br>`52:28` yeah and then how can i update it so
<br>`52:32` then i need at least two lattice points
<br>`52:35` at the same time to update to define
<br>`52:37` these updating rules
<br>`52:39` and then i have different possibilities
<br>`52:41` here
<br>`52:42` yeah if my two lattice points are
<br>`52:45` infected
<br>`52:46` that previously either the left one or
<br>`52:49` the right one
<br>`52:50` was infected
<br>`52:54` the recovery process is no more
<br>`52:56` complicated
<br>`52:57` yeah if i have known that in this two
<br>`53:00` side picture i have one
<br>`53:03` infected and one one infected and one
<br>`53:07` not affected once this white is down
<br>`53:09` here
<br>`53:10` this is
<br>`53:13` healthy this is
<br>`53:17` infected
<br>`53:21` now if i have one infected and one
<br>`53:24` healthy one
<br>`53:25` previously my system could have been
<br>`53:29` must have been in a state now if i'm
<br>`53:31` looking at the
<br>`53:32` recovery process where both of them were
<br>`53:35` infected
<br>`53:37` now so with the probability one half i
<br>`53:39` have either this
<br>`53:41` or this one here and then
<br>`53:44` if both of the states in the second time
<br>`53:47` step
<br>`53:48` are healthy then one of them was in fact
<br>`53:52` before now so here i update two sides at
<br>`53:55` the same time
<br>`53:57` or i can also say i updated the whole
<br>`53:59` letters at the same time
<br>`54:00` in parallel and now
<br>`54:04` the thing is what is this here
<br>`54:09` what is this here these two processes
<br>`54:11` here
<br>`54:12` suddenly i have a process a process for
<br>`54:15` recovery
<br>`54:17` that involves two individuals
<br>`54:20` yeah formally that involves two
<br>`54:22` individuals so here have two individuals
<br>`54:25` to infect it
<br>`54:26` and after that only one of them is
<br>`54:28` infected

### slide 10

<br>`54:30` now suddenly i have two individuals and
<br>`54:32` if i ask how
<br>`54:33` such a term here if i take this
<br>`54:37` description as the basis for my larger
<br>`54:40` equation
<br>`54:41` how will this term pop up in my larger
<br>`54:44` equation
<br>`54:45` then it's this term is proportional to
<br>`54:49` one-half
<br>`54:50` times
<br>`54:55` the probability that one of them is
<br>`54:57` infected and the probability that the
<br>`54:59` other one is
<br>`55:00` also infected so we will have something
<br>`55:03` like rho
<br>`55:04` of x t squared
<br>`55:08` and we'll get a minus because we
<br>`55:10` decrease the number
<br>`55:11` of infected individuals
<br>`55:15` now this is just to show you yeah by
<br>`55:16` this uh
<br>`55:18` magnesium inside the exotic lattice
<br>`55:20` representation
<br>`55:22` that you suddenly get a term you write
<br>`55:25` down the larger equation here
<br>`55:27` this is the larger equation
<br>`55:30` and this is here what you expect the
<br>`55:32` first thing is what you expect is an
<br>`55:34` infection term
<br>`55:35` you have the density of infected people
<br>`55:37` at a certain position x
<br>`55:40` and this depends on how many infected
<br>`55:43` people i already have
<br>`55:44` that is this typical exponential
<br>`55:47` increase of the infection rate
<br>`55:51` now we get another term here
<br>`55:55` this term that describes the recovery
<br>`55:58` process now this describes
<br>`56:02` the recovery process and
<br>`56:05` it suddenly has this quadratic term
<br>`56:08` although this recovery process like this
<br>`56:10` picture looked completely linear because
<br>`56:12` every individual was doing it
<br>`56:14` individually now we have now the second
<br>`56:18` degree term here and that looks like an
<br>`56:21` interaction
<br>`56:22` and this comes just because we're
<br>`56:23` updating all the letters in parallel in
<br>`56:25` this
<br>`56:26` lingerie equation and that's why we get
<br>`56:29` this
<br>`56:30` second degree term here we have a
<br>`56:33` diffusion term
<br>`56:34` this one here that was also not in our
<br>`56:36` model description
<br>`56:38` you know that we never said that these
<br>`56:41` particles are actually moving around
<br>`56:44` but there is some spread of spatial
<br>`56:46` information because you
<br>`56:47` interact with the nearest neighbor yeah
<br>`56:50` and this
<br>`56:51` is models if you zoom out and go to a
<br>`56:54` continuous picture
<br>`56:56` it's a spread diffusive spread of
<br>`56:58` infection information
<br>`57:00` and that's why you effectively get a
<br>`57:02` term here you need to have a term
<br>`57:05` that involves spatial derivatives now
<br>`57:07` where you actually spread something over
<br>`57:09` space you spread the infection of
<br>`57:11` space and that's why you get this term
<br>`57:13` here
<br>`57:14` and you have of course again a noise
<br>`57:16` term
<br>`57:18` now and i'll give these here parameters
<br>`57:20` and also new names the combinations of
<br>`57:22` the old parameters
<br>`57:24` and we want to keep this we want to have
<br>`57:26` different parameters at each of these
<br>`57:28` rates because we in the next step want
<br>`57:30` to renormalize these parameters that we
<br>`57:33` we need them and the noise here
<br>`57:36` on the right hand side is our good old
<br>`57:39` gaussian noise now that has
<br>`57:41` zero mean and
<br>`57:44` correlations in space and time
<br>`57:47` that are luckily delta distributors so
<br>`57:50` they're
<br>`57:50` memory less they don't have memory in
<br>`57:52` space or in time
<br>`57:54` but they depend on this density here
<br>`58:00` they depend on this density and what
<br>`58:03` this means
<br>`58:04` is that this noise
<br>`58:08` the correlation
<br>`58:11` in the noise or the strength of this
<br>`58:13` noise that's the strength of
<br>`58:15` noise
<br>`58:19` is zero
<br>`58:24` if the disease
<br>`58:28` is extinct that's called
<br>`58:31` multiplicative noise because now the
<br>`58:33` density
<br>`58:35` rho of x and t is a pre-factor in the
<br>`58:39` noise term that
<br>`58:40` if is it is contributing
<br>`58:43` or defining the strength of the nodes
<br>`58:45` and once we have
<br>`58:46` zero infected individuals left then the
<br>`58:49` noise disappeared and we can never have
<br>`58:51` get away out of this term out of this
<br>`58:53` point
<br>`58:54` where the infection is lost

### slide 11

<br>`58:59` so maybe
<br>`59:02` quite late in time as a next step
<br>`59:10` um we get a little bit more formal so
<br>`59:12` now we have the larger
<br>`59:13` equation now and what you see here
<br>`59:16` already
<br>`59:17` is the martensite rose functional
<br>`59:20` integral that we derived
<br>`59:22` and this functional martin citra rose
<br>`59:24` function integral
<br>`59:25` or **martensite rules johnson the dominic**
<br>`59:27` is functional integral
<br>`59:29` you can divide very easily we remember
<br>`59:32` the equation that we had
<br>`59:33` a few lectures ago first
<br>`59:36` part of this function integral
<br>`59:42` what was it here
<br>`59:45` it's just the launch of a equation
<br>`59:48` yeah that that makes sure that you
<br>`59:50` actually solve the launcher equation
<br>`59:52` here you have the laundry equation and
<br>`59:55` then you have these terms here
<br>`59:57` on the right hand side there are higher
<br>`60:00` order
<br>`60:01` here we have this phi squared
<br>`60:04` that's just this one here and here
<br>`60:08` you have a noise term that we also had
<br>`60:10` before now that was this
<br>`60:12` gaussian noise term that we came from
<br>`60:14` integrating out the psi
<br>`60:16` in the martensitic rows formula now so
<br>`60:19` we have this term here
<br>`60:21` is quite noise but in contrast to the
<br>`60:23` previous case
<br>`60:25` where the noise didn't depend on the
<br>`60:27` density itself
<br>`60:28` we now here that's the only difference
<br>`60:31` have
<br>`60:31` another phi here
<br>`60:35` now we have another phi here
<br>`60:38` that's the only difference that we get
<br>`60:40` for multiplicative noise
<br>`60:42` and because we have multiplicative noise
<br>`60:46` you can see that somehow now the noise
<br>`60:50` term
<br>`60:51` here looks a little bit like another
<br>`60:55` term that is
<br>`60:55` actually as an interaction term where we
<br>`60:58` couple the two fields
<br>`61:00` one linearly to each other this term and
<br>`61:03` suddenly the noise term is not
<br>`61:04` simple a gaussian it's not simple a
<br>`61:07` gaussian that the inti can integrate
<br>`61:08` over
<br>`61:09` suddenly it couples to the other fields
<br>`61:11` now the strength of this noise curve
<br>`61:13` is proportional to phi that's this
<br>`61:16` multiplicative noise that makes life
<br>`61:18` complicated
<br>`61:20` now we now do a simple step now we
<br>`61:23` re-scale we now
<br>`61:24` we now we take this martensitic rows
<br>`61:27` generating function that i wrote down
<br>`61:29` here we take this
<br>`61:31` yeah and we just make our lives easier
<br>`61:33` life easier for later
<br>`61:35` yeah and by doing this to do this
<br>`61:39` we rescale some of these
<br>`61:42` fields and parameters so rescale
<br>`61:47` the fields so what we do
<br>`61:50` is we want to
<br>`61:53` get rid of
<br>`61:59` we have had two terms this one and this
<br>`62:02` one
<br>`62:03` they look kind of similar and the idea
<br>`62:06` is now
<br>`62:06` that if we have a proper transformation
<br>`62:09` or fields
<br>`62:10` that we can make them exactly equal up
<br>`62:13` to some pre-factors
<br>`62:15` yeah so that's what we want to do we
<br>`62:16` want to simplify this action
<br>`62:19` and uh to symmetrize it now so that we
<br>`62:22` can treat these two terms
<br>`62:23` and e equally now that's how we may we
<br>`62:26` want to make the prefactor here
<br>`62:28` this and this prefactor equal
<br>`62:32` now we can summarize these two trends
<br>`62:35` now so really scared the fields but just
<br>`62:37` tell you how to do that you have phi
<br>`62:40` goes over to 2 lambda
<br>`62:43` over gamma times phi
<br>`62:46` if i tilde the response field goes over
<br>`62:50` to
<br>`62:52` gamma to lambda
<br>`62:56` and gamma goes over to
<br>`63:00` two gamma lambda
<br>`63:05` yeah so we rescale this we are allowed
<br>`63:07` to do that
<br>`63:08` and then we get our new generating
<br>`63:11` functional
<br>`63:13` and this generating functional is again
<br>`63:16` of this form
<br>`63:17` d phi d phi tilde
<br>`63:22` e to the some action as naught and we
<br>`63:26` find that
<br>`63:26` what this is phi
<br>`63:30` by children
<br>`63:33` plus now this is has a naught the others
<br>`63:36` the non-interacting term
<br>`63:38` and now we have a term that of course
<br>`63:40` that describes interactions
<br>`63:43` now that's where the fun is happening
<br>`63:46` by artillery and just write that down
<br>`63:50` this as not phi
<br>`63:54` phi tilde this action is the integral
<br>`63:57` over dx
<br>`63:59` dt
<br>`64:03` so here we should have
<br>`64:06` dt as well
<br>`64:10` yeah so at the x dt
<br>`64:13` and now we um have
<br>`64:17` 5 x t
<br>`64:21` tau sorry what we need that
<br>`64:25` del t minus d naught
<br>`64:28` squared minus kappa
<br>`64:32` phi of x t
<br>`64:37` and then we have another part as
<br>`64:40` interaction phi phi to the
<br>`64:45` gamma over two integral dx
<br>`64:49` dt phi tilde
<br>`64:53` x t minus i sorry that looks
<br>`64:56` not so nice
<br>`65:01` all right tilde of x and t
<br>`65:05` times phi of x
<br>`65:09` t minus phi to the
<br>`65:13` of x and t
<br>`65:17` phi of x
<br>`65:20` t so this is this interaction term
<br>`65:24` and it's called interaction term because
<br>`65:26` we have here
<br>`65:27` higher orders of the field coupling to
<br>`65:29` each other
<br>`65:31` yeah so
<br>`65:34` this is now our martin's intervals
<br>`65:37` integral
<br>`65:38` yeah and this is what we'll be dealing
<br>`65:41` with and this is what we'll define
<br>`65:43` the result renormalization group on and
<br>`65:46` because i knew that we would be doing
<br>`65:48` renormalization
<br>`65:50` i have already introduced this little
<br>`65:54` towel here now because in
<br>`65:57` renormalization
<br>`65:58` we want to cause grain we want to
<br>`66:00` transform this action
<br>`66:02` and we want to see how our action and
<br>`66:04` how the parameters are
<br>`66:06` of our action change in this procedure
<br>`66:09` and that's why all our terms here need
<br>`66:11` to have a prefactor
<br>`66:14` yeah and that's why i introduced this
<br>`66:15` tau that's why i have this d
<br>`66:18` you know and this kappa here i have them
<br>`66:20` all
<br>`66:21` giving them different names although
<br>`66:22` they're not independent of each other
<br>`66:25` because our original model just had one
<br>`66:27` parameter that was the lambda
<br>`66:29` yeah so that's the uh that's the martin
<br>`66:32` sutra rose
<br>`66:34` functional integral and um
<br>`66:38` next so we're already quite late now
<br>`66:41` next time
<br>`66:42` we start right away with uh first with
<br>`66:47` introducing renormalization intuitively
<br>`66:51` and then as a second step you'll then
<br>`66:53` apply that
<br>`66:54` to this epidemic model and re-normalize
<br>`66:57` this margin central rows
<br>`66:58` functional integral now apparently i was
<br>`67:01` always
<br>`67:01` very optimistic and it was trying to
<br>`67:04` introduce already
<br>`67:05` the renomination today but we can do
<br>`67:07` that just next week
<br>`67:08` now because it's already quite late
<br>`67:11` today 
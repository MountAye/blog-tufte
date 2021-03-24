---
layout:      post
title:      ".mpipks-transcript | 08. Renormalization Group (continued)"
keywords:   "mpipks-transcript"
excerpt:    "还是重整化群，冲不动了……"
date:        2021-03-23
categories:  post
milestoneID: 36
---

<br>`00:11` [Music]
<br>`00:14` hmm
<br>`00:23` i didn't expect so many people to join
<br>`00:25` shortly before christmas
<br>`00:26` i thought you were all already
<br>`00:30` traveling
<br>`00:33` so today we have a little
<br>`00:36` extra lecture yeah it's not only
<br>`00:40` christmas but it's also the lecture
<br>`00:43` where we finally got to do some
<br>`00:44` calculations some realization
<br>`00:46` calculations and uh because this is a
<br>`00:50` lecture focused on calculations
<br>`00:54` um it of a little bit of an add-on
<br>`00:58` lecture
<br>`00:59` yeah so we have the intuitive stuff we
<br>`01:02` did last time
<br>`01:04` and now we see how it works in practice
<br>`01:06` but you don't need this lecture
<br>`01:08` actually for the remainder of this
<br>`01:09` course
<br>`01:11` so let me share the screen um
<br>`01:15` so you see as you see before i switch
<br>`01:17` off the video so you see that i
<br>`01:19` brought a little uh pyramid here it's
<br>`01:21` one of the traditional
<br>`01:22` things that is produced in the mountains
<br>`01:25` around grayson
<br>`01:27` and uh that's what a lot of people now
<br>`01:30` have in their windows
<br>`01:32` or in their uh apartments
<br>`01:35` and uh there's a lot of tradition
<br>`01:38` christmas traditions in germany actually
<br>`01:39` come from this area here around dresden
<br>`01:42` and so let's
<br>`01:46` move on and let me give you a little
<br>`01:49` reminder um

### slide 1

<br>`02:07` there we go let's start with a little
<br>`02:11` reminder
<br>`02:14` there we go yeah so you've seen that
<br>`02:16` already
<br>`02:17` now many times for some reason it took
<br>`02:19` us an entire lecture to just
<br>`02:21` define this model and
<br>`02:24` so this is the epidemic model we want to
<br>`02:27` treat
<br>`02:28` analytically today as this analysis this
<br>`02:31` epidemic model
<br>`02:32` consists of two kinds of people the
<br>`02:36` infected ones the susceptible ones
<br>`02:38` and then we have we put these people on
<br>`02:40` the lettuce and the world
<br>`02:42` and when uh and these infected people
<br>`02:45` can infect
<br>`02:47` uh susceptible ones or non-infected
<br>`02:49` people
<br>`02:51` if they are on the neighboring letter
<br>`02:53` side
<br>`02:54` and then infected people can also
<br>`02:56` recover and turn
<br>`02:58` into susceptible or non-infected people
<br>`03:02` so this is the little model that we
<br>`03:03` introduced and uh

### slide 2

<br>`03:05` i also just a quick reminder that this
<br>`03:08` model
<br>`03:09` produces uh critical behavior that means
<br>`03:13` that we have
<br>`03:14` a value where we balance uh the
<br>`03:18` interaction and recovery
<br>`03:19` rate in a certain way uh where
<br>`03:23` uh the there's a such a balance between
<br>`03:26` between
<br>`03:27` infection and recovery and uh if we
<br>`03:29` attune this parameters to be in the
<br>`03:31` state
<br>`03:32` then we get these self-similar states
<br>`03:34` that you see in this in the middle
<br>`03:36` where both the spatial correlation
<br>`03:38` length but also the temporal correlation
<br>`03:42` is infinite yeah

### slide 3

<br>`03:45` then we moved on and we uh
<br>`03:49` inferred the field theory description
<br>`03:52` of this uh s i model
<br>`03:55` yeah and the future description the
<br>`03:57` martian citra rose function integral is
<br>`03:59` here on the top
<br>`04:01` now that's the that's the margin as it
<br>`04:04` was the generating functional
<br>`04:06` and you can see here we essentially have
<br>`04:09` an order of equation
<br>`04:10` and then we get these additional terms
<br>`04:12` here
<br>`04:14` that's because we have effective
<br>`04:16` interactions between letter size
<br>`04:17` and multiplicative noise that means that
<br>`04:20` the noise
<br>`04:21` itself depends on the strength
<br>`04:24` of these feet on the concentration of
<br>`04:27` these
<br>`04:28` individuals now the function integrands
<br>`04:30` has
<br>`04:31` the function integrals has two kinds of
<br>`04:34` fields
<br>`04:35` now the five field which is the density
<br>`04:37` of
<br>`04:38` infected people but we also have the phy
<br>`04:41` to the field which is the response field
<br>`04:43` a couple of lectures ago
<br>`04:45` we discussed that this is describes the
<br>`04:48` instantaneous response of our field
<br>`04:51` to very small perturbations that's the
<br>`04:54` intuition about this response
<br>`04:57` and we get this response here because we
<br>`04:59` don't have the
<br>`05:00` noise explicitly here anymore so the
<br>`05:03` response field
<br>`05:04` uh in some way mimics the noise
<br>`05:09` yeah so we can write this functional
<br>`05:13` uh generating functional by separating
<br>`05:17` the action into two parts we are a free
<br>`05:20` part
<br>`05:21` so we call that free part because in
<br>`05:23` this free part
<br>`05:25` we have terms
<br>`05:29` that are quadratic in the fields
<br>`05:32` now so this is the gaussian part that we
<br>`05:34` could integrate if you want
<br>`05:36` now is this first part here that's
<br>`05:38` quadratic and then we have terms
<br>`05:41` that have higher order interactions
<br>`05:43` between the fields
<br>`05:45` yeah phi squared times phi tilde and so
<br>`05:48` on
<br>`05:48` yeah and these we call this we call the
<br>`05:51` interaction
<br>`05:52` part and uh we treat this interaction
<br>`05:56` part the first part is essentially
<br>`05:58` gaussian as we have second order in the
<br>`06:00` field
<br>`06:01` and we can hope that you can deal with
<br>`06:03` that
<br>`06:04` but the other parts are non-gaussian so
<br>`06:06` we have higher orders
<br>`06:08` in these fields and we don't know how to
<br>`06:10` perform integrals
<br>`06:11` around this last interacting part so we
<br>`06:14` separate these two
<br>`06:16` and if we separate this two and we do
<br>`06:17` some rescaling
<br>`06:19` you know of these parameters to make
<br>`06:21` things look simple
<br>`06:22` we get to this form where the three part
<br>`06:25` is given
<br>`06:26` as usual yeah and the interacting part
<br>`06:29` now has a more compact form that we also
<br>`06:32` already derived

### slide 4

<br>`06:34` two lectures ago now we can
<br>`06:37` transform this to fourier space
<br>`06:40` and uh in this fourier space uh this
<br>`06:44` uh the spatial derivatives this one here
<br>`06:48` uh become algebraic quantities so
<br>`06:52` the wave vector squared here represents
<br>`06:55` diffusion
<br>`06:56` and here the omega i omega
<br>`07:00` is what we get from the time derivative
<br>`07:02` and then we have here
<br>`07:04` these interaction terms that you look at
<br>`07:06` as complex
<br>`07:08` as usual

### slide 5

<br>`07:12` so now we want to understand the
<br>`07:16` critical behavior of this model
<br>`07:18` that means what we want to understand is
<br>`07:21` the
<br>`07:22` macroscopic behavior of
<br>`07:26` macroscopic quantities in the vicinity
<br>`07:28` of the critical point
<br>`07:30` and i told you already that in the
<br>`07:31` vicinity of the critical point just like
<br>`07:33` in the
<br>`07:34` equilibrium system that we get
<br>`07:38` divergences now so for example the
<br>`07:40` correlation length diverge
<br>`07:43` with uh power laws you know and to
<br>`07:46` understand these power laws and to get
<br>`07:48` the exponent
<br>`07:49` we have uh we could the principle
<br>`07:53` naively you know if you want to have a
<br>`07:55` system at a critical point we want to
<br>`07:57` understand the macroscopic behavior
<br>`07:59` we could naively just say okay let's
<br>`08:01` just average
<br>`08:03` over the entire system over large areas
<br>`08:05` in the system
<br>`08:06` and write down a macroscopic theory of
<br>`08:08` these averages
<br>`08:11` yeah but that's not what's working out
<br>`08:13` that's called mean field theory
<br>`08:15` that's not working out very well because
<br>`08:18` in mean field theory we
<br>`08:20` basically immediately go to the
<br>`08:22` macroscopic scale
<br>`08:23` at a critical point we have the
<br>`08:26` self-similarity
<br>`08:27` now we zoom in and the system looks the
<br>`08:30` same as before
<br>`08:32` and because we have the similarity all
<br>`08:34` length scales
<br>`08:36` are equally important they all matter
<br>`08:39` so we need an approach that allows us to
<br>`08:41` go from a microscopic scale
<br>`08:44` step-by-step scale by scale to the
<br>`08:46` macroscopic scale
<br>`08:49` and renormalization allows us to do that
<br>`08:52` we start with a microscopic theory like
<br>`08:55` our lattice model
<br>`08:57` and then renormalization
<br>`09:01` renewalization allows us to go
<br>`09:05` from the microscopic scale step by step
<br>`09:09` to the macroscopic scale
<br>`09:12` now i derive a description on the
<br>`09:14` macroscopic scale
<br>`09:16` now this renewalization has two steps
<br>`09:19` the first step was
<br>`09:21` coarse graining
<br>`09:26` that's the basic idea and with this
<br>`09:29` course gradient i showed you that
<br>`09:31` you have a lattice system for example an
<br>`09:34` ising model
<br>`09:36` that consists of lattice points
<br>`09:42` then this course graining step you can
<br>`09:44` think about
<br>`09:45` as for example defining blocks
<br>`09:49` of such spins now think about a magnet
<br>`09:52` or so
<br>`09:54` and then representing each block
<br>`09:57` by a new variable by a new
<br>`10:00` effective lattice side or new effective
<br>`10:03` spin
<br>`10:05` now the second and third steps were
<br>`10:09` rescaling
<br>`10:14` schooling and renormalization steps
<br>`10:21` now that means we need to make sure that
<br>`10:23` we when we do this
<br>`10:24` procedure of course green is essential
<br>`10:27` essentially makes
<br>`10:28` our system look fuzzy i think if i do
<br>`10:31` like this with our
<br>`10:33` with with my glasses here then
<br>`10:34` everything everything is fuzzy
<br>`10:36` and my eyes are doing cold straight yeah
<br>`10:39` so
<br>`10:39` if i do that procedure of these blocks i
<br>`10:42` now have to make sure that the length
<br>`10:44` scale
<br>`10:45` that i get in my new system corresponds
<br>`10:47` to the old length scale
<br>`10:48` so that we can compare this distance and
<br>`10:51` about this we everest rescale lengths
<br>`10:57` so that our sites have the same
<br>`11:00` letters as spacing at the old level
<br>`11:02` sides
<br>`11:04` and we also need to rescale energies to
<br>`11:07` renormalize the field
<br>`11:11` now to so that the new spins have the
<br>`11:13` same magnitude for example plus one and
<br>`11:15` minus one
<br>`11:16` as the old states now if we do that
<br>`11:19` then we go from a microscopic if this
<br>`11:23` was the
<br>`11:24` described by a microscopic some action
<br>`11:27` here
<br>`11:29` some action if we do these steps
<br>`11:33` we get a new action as prime
<br>`11:37` and if we do this course grading
<br>`11:39` correctly
<br>`11:40` then we can hope that the new action has
<br>`11:43` the same structure as the old
<br>`11:45` action that means that the old that the
<br>`11:47` new action has the same terms
<br>`11:49` in it just with rescaled
<br>`11:52` parameters now and
<br>`11:56` the the way this looks then also i also
<br>`11:58` showed you already this
<br>`11:59` picture is that if you consider the
<br>`12:02` space of all
<br>`12:03` actions p1 p2 that is described by some
<br>`12:07` parameters
<br>`12:09` then our physical epidemic model
<br>`12:14` has some space in this
<br>`12:18` has some subspace of the space of action
<br>`12:20` and somewhere in the subspace is our
<br>`12:22` critical point
<br>`12:25` now we renormalize we start with a
<br>`12:28` microscopic
<br>`12:30` critical description for microscopic
<br>`12:33` critical action
<br>`12:35` and then we normalize and ask where does
<br>`12:37` this renormalization
<br>`12:39` lead to

### audio problem

<br>`14:13` uh stefan uh we are unable to hear your
<br>`14:16` audio
<br>`14:17` like it's a problem with all of us and
<br>`14:20` everyone's writing in the chat
<br>`14:22` there's some problem with the audio
<br>`15:16` okay can you hear me now
<br>`15:21` yes so now you can know you can hear me
<br>`15:24` now i'm using
<br>`15:25` the macbook microphone
<br>`15:47` okay so
<br>`15:56` so it's always killing the bluetooth
<br>`16:00` connection for some reason
<br>`16:22` [Music]
<br>`16:27` okay i have to
<br>`16:48` can you hear me
<br>`16:54` okay but i think it's the
<br>`16:57` is it correct that the quality is not
<br>`16:58` very good
<br>`17:05` no it's not working it's okay okay let
<br>`17:08` me know if
<br>`17:09` it's uh not okay because i'm using the
<br>`17:11` thing that should give you the echo
<br>`17:14` um let me know it's not okay i'm gonna
<br>`17:17` try again with
<br>`17:18` the headphones okay so i don't know
<br>`17:22` where i actually
<br>`17:23` stopped yeah uh can you let me know when
<br>`17:26` you when you stopped
<br>`17:28` being able to listen to did you hear me
<br>`17:32` uh you were talking about uh where the
<br>`17:34` si model lies and then
<br>`17:37` you started drawing the subspace and
<br>`17:38` then we stopped hearing
<br>`17:40` from the when you started drawing the
<br>`17:41` fixed point okay
<br>`17:44` okay
<br>`18:03` yeah it says strange that it's working
<br>`18:05` all the time
<br>`18:06` and then suddenly it stops working okay
<br>`18:09` so let's see

### audio back normal

<br>`18:10` okay so i stopped basically
<br>`18:16` with the critical point of the si model
<br>`18:20` then we normalized and this
<br>`18:22` renormalization process
<br>`18:24` leads us to a fixed point
<br>`18:27` once we are in the fixed point the
<br>`18:29` action is always
<br>`18:30` mapped onto itself
<br>`18:34` yeah that means in this fixed point once
<br>`18:36` we are in this fixed point
<br>`18:38` or the sixth point describes the
<br>`18:40` macroscopic
<br>`18:42` properties of our system
<br>`18:47` and then i defined the set of all
<br>`18:51` actions that are also drawn into the
<br>`18:55` same fixed point
<br>`18:57` and that's called the critical manifold
<br>`19:02` pretty cool manifold
<br>`19:08` yeah and this critical manifold yeah
<br>`19:11` and then we looked at a different action
<br>`19:14` for example this one
<br>`19:17` here and if you look at this different
<br>`19:19` action that's called micro is going for
<br>`19:21` example to a different
<br>`19:22` epidynamic model and this
<br>`19:25` other action also intersects
<br>`19:29` has a critical point and intersects this
<br>`19:31` critical manifold somewhere
<br>`19:33` and when we normalize this other
<br>`19:36` microscopic theory then
<br>`19:40` the action will be drawn into the
<br>`19:42` facility of the very same fixed point
<br>`19:45` that means on the macroscopic level
<br>`19:49` both modal artists are described
<br>`19:53` by the same theory by the same action
<br>`19:56` and that's called universality
<br>`20:02` that different theories that different
<br>`20:05` systems
<br>`20:06` uh that differ on the microscopic scale
<br>`20:10` show the same marvelous microscopic
<br>`20:13` behavior
<br>`20:14` and that allows us for some of you you
<br>`20:16` know that from
<br>`20:18` statistical physics uh magnets you can
<br>`20:21` have
<br>`20:21` different ferric magnets of different
<br>`20:23` materials and they all show the same
<br>`20:25` critical behavior
<br>`20:26` and we're able to describe all of them
<br>`20:28` or many of them
<br>`20:30` with a very simple model that's called
<br>`20:32` the icing board
<br>`20:34` and that's because of this universality
<br>`20:36` on the macroscopic scale
<br>`20:38` only a few things matter and many
<br>`20:41` different microscopic
<br>`20:42` theories microscopic descriptions show
<br>`20:45` the same microscopic behavior
<br>`20:48` and the renormalization group allows us to
<br>`20:51` understand
<br>`20:51` why this is the case
<br>`20:55` so and this in reality
<br>`20:59` is also the reason why we're here
<br>`21:01` looking at such a simple model
<br>`21:04` for an epidemic epidemic is something
<br>`21:07` super complex
<br>`21:08` there's so many variables and parameters
<br>`21:11` but if you're interested in the critical
<br>`21:12` behavior
<br>`21:14` then we can show that in this action
<br>`21:17` that we have
<br>`21:18` if we added more and more processes to
<br>`21:20` it more and more turns more
<br>`21:22` interactions but at least interactions
<br>`21:24` in many cases
<br>`21:25` are much relevant on the macroscopic
<br>`21:28` scale
<br>`21:30` and then the next step you can take this
<br>`21:32` fixed point
<br>`21:33` and calculate exponents and we do this
<br>`21:36` by looking
<br>`21:36` by looking into the directions that
<br>`21:39` drive us
<br>`21:40` away from the critical manifold these
<br>`21:43` are the relevant
<br>`21:46` directions
<br>`21:51` yeah and if we ask how fast the systems
<br>`21:54` these are the parameters that
<br>`21:56` experimentalists needs to tune
<br>`21:58` in order to bring the system to the
<br>`22:00` critical point
<br>`22:02` and if you ask how quickly
<br>`22:05` is the renovation flow driven out
<br>`22:09` of the critical point or talking about
<br>`22:12` to the critical manifolds
<br>`22:15` then this describes uh then we can
<br>`22:18` derive
<br>`22:18` exponents from this exponents
<br>`22:22` tell us how fast the system goes out of
<br>`22:25` the critical manifold
<br>`22:27` once we renovate so that's the
<br>`22:30` general idea now let's see how this
<br>`22:33` looks in practice
<br>`22:34` we started already as another another
<br>`22:38` reminder is the wilson's renovation
<br>`22:41` momentum shell renovation

### slide 6

<br>`22:44` wilson's idea was that what i showed you
<br>`22:46` on the last
<br>`22:47` slide here is these blocks the problem
<br>`22:50` with these blocks is that you
<br>`22:54` there's no small parameter you cannot
<br>`22:57` make an epsilon block or something like
<br>`22:59` this
<br>`23:00` yeah so that's that's that's a that's a
<br>`23:03` problematic thing
<br>`23:04` and that's why these blocks also called
<br>`23:07` real space criminalization
<br>`23:09` is very often very often doesn't work or
<br>`23:11` is very difficult
<br>`23:13` so wilson idea wilson's idea was to do
<br>`23:16` the regularization
<br>`23:17` in momentum space and that's also a
<br>`23:20` reminder
<br>`23:22` because we had that already last time
<br>`23:24` what we do
<br>`23:25` in wilson's momentum shell
<br>`23:27` renormalization
<br>`23:29` is that we take a look at the space of
<br>`23:32` all
<br>`23:32` wave vectors and integrate out
<br>`23:37` uh the smallest wave vectors
<br>`23:40` and so again as before there's like two
<br>`23:43` steps to rescaling
<br>`23:44` the ends a realization and the cause
<br>`23:47` training and here in this case we do the
<br>`23:49` course training
<br>`23:50` by integrating out a tiny
<br>`23:53` shell in momentum space we integrate out
<br>`23:56` the fastest wave vectors which
<br>`23:58` corresponds
<br>`23:59` to the shortest length scales
<br>`24:04` and then we can formally
<br>`24:07` describe our fields as fine for example
<br>`24:12` is the component by a short wavelength
<br>`24:16` plus
<br>`24:25` the slower wave vectors and the fast
<br>`24:27` wavelengths rather we integrate out
<br>`24:29` these
<br>`24:30` fast wave vectors at each steps
<br>`24:33` at each step
<br>`24:37` yeah that means that we define
<br>`24:41` our action on the
<br>`24:45` long so small wave vectors with the long
<br>`24:48` wavelengths
<br>`24:49` as the integral over the entire reaction
<br>`24:53` but we only perform this integral
<br>`24:57` over the very this momentum shell
<br>`25:01` on this very highest wave vectors
<br>`25:04` in the system yeah and if we integrate
<br>`25:07` this out
<br>`25:08` now that our momentum shell our momentum
<br>`25:11` space gets smaller and smaller
<br>`25:13` until we arrive at momentum
<br>`25:16` zero that corresponds with very small
<br>`25:20` values of these skews that corresponds
<br>`25:23` to very large length scales and so
<br>`25:24` therefore
<br>`25:25` macroscopic behavior

### slide 7

<br>`25:29` okay so let's begin
<br>`25:32` so we begin we begin
<br>`25:37` by doing the rescaping stuff and this
<br>`25:40` lecture is different from mass vectors
<br>`25:41` but this will
<br>`25:42` probably mostly be a chalk chalkboard
<br>`25:46` lecture
<br>`25:46` and we'll have to see how this works on
<br>`25:48` an ipad
<br>`25:50` and so so let's let's see i hope it's
<br>`25:53` not too confusing
<br>`25:57` okay so first we do rescaling
<br>`26:06` and is rescaling
<br>`26:09` to say that we have to
<br>`26:13` rescale our length skills
<br>`26:17` by some
<br>`26:21` like london
<br>`26:25` with the value of longer than smaller
<br>`26:26` than one
<br>`26:31` if we rescan our length skills we also
<br>`26:34` have to rescale all
<br>`26:35` other things the answer for length here
<br>`26:39` goes like this so our x and our action
<br>`26:44` the time
<br>`26:48` also needs to be scaled that's not
<br>`26:51` independent
<br>`26:52` of space because it connects to space
<br>`26:55` by this dynamic exponent z
<br>`26:59` yeah that was the ratio between the
<br>`27:01` perpendicular and the parallel
<br>`27:04` correlation exponents um
<br>`27:07` so that's not independent of space we
<br>`27:09` have to reschedule as well
<br>`27:11` and we don't know what that is by the
<br>`27:13` way but that's our goal
<br>`27:15` and then we have to escape our fields
<br>`27:19` what our fields we scale with some
<br>`27:21` exponent
<br>`27:23` chi when we
<br>`27:26` rescale our x and our
<br>`27:30` time this way
<br>`27:34` and our other field
<br>`27:38` now the volatility we scales in the same
<br>`27:42` way
<br>`27:43` 5 tilde lambda
<br>`27:47` x lambda z
<br>`27:51` t yeah
<br>`27:54` so we don't know what chi is now we
<br>`27:57` don't know what
<br>`27:59` that is but if we rescale the length we
<br>`28:02` have to rescale the other things as well
<br>`28:06` yeah and kind at five
<br>`28:09` sorry fine
<br>`28:12` and fragile have the same scale
<br>`28:16` because uh if we replace
<br>`28:19` one by the other and we switch time to
<br>`28:22` the action
<br>`28:23` and then we get the same action back so
<br>`28:25` these 5 and 5 total fields
<br>`28:27` are the same thing if we transform the
<br>`28:30` action
<br>`28:31` accordingly okay so now we just plug
<br>`28:35` this
<br>`28:35` in into the action with this
<br>`28:39` we get that as not
<br>`28:43` let's find phi together
<br>`28:46` we have these integrals here d dx
<br>`28:52` dt
<br>`28:55` by children of x t
<br>`29:01` and then comes this part
<br>`29:04` of tom times
<br>`29:08` lambda two
<br>`29:12` coin plus b where does that come from
<br>`29:15` possibly data
<br>`29:16` delta t so we have here
<br>`29:21` one length scale that gives us the d
<br>`29:25` lambda to the power of d
<br>`29:28` we have a times the integral over time
<br>`29:31` that gives us uh that cancels out with
<br>`29:34` this one that is one over time
<br>`29:36` this time so we don't have anything and
<br>`29:39` the two kai
<br>`29:40` can't because we have the kai from the
<br>`29:42` the five the field from the left hand
<br>`29:44` side
<br>`29:45` and later they flew from the right hand
<br>`29:46` side
<br>`29:48` so now we have this part
<br>`29:52` minus d
<br>`29:55` lambda 2 chi
<br>`29:59` plus d plus z minus 2
<br>`30:04` times
<br>`30:07` uh sort of minus
<br>`30:11` here it's again this this comes from the
<br>`30:13` fields the two fields
<br>`30:16` this comes from the uh
<br>`30:20` sorry
<br>`30:23` so this comes from the from the integral
<br>`30:26` of a space
<br>`30:28` this comes from the integral over time
<br>`30:31` and the minus 2 comes because this was
<br>`30:36` originally a second derivative in space
<br>`30:39` we had a diffusion trip here so that's
<br>`30:42` how we get this
<br>`30:46` so minus pepper lambda
<br>`30:50` [Music]
<br>`30:55` phi of x t
<br>`30:58` so now i just assume we did the
<br>`31:00` resetting step
<br>`31:02` just zoomed out and this
<br>`31:05` already gives us some change of
<br>`31:08` parameters
<br>`31:11` and we can now call these parameters
<br>`31:15` give them new names for example
<br>`31:19` this one here is now tau prime
<br>`31:24` this one is d prime
<br>`31:28` and this one is kappa prime
<br>`31:34` now so this was the the part of the
<br>`31:37` action at this
<br>`31:38` second order now we take the part of the
<br>`31:40` action that has higher organisms
<br>`31:47` and this part is also an integral dd
<br>`31:50` x integral dt
<br>`31:55` gamma that is the strength of the voice
<br>`32:13` in third order
<br>`32:18` to coin plus a from the integral
<br>`32:22` over space and plus z from the integral
<br>`32:25` over time
<br>`32:26` now
<br>`32:32` of x t times
<br>`32:37` y of x t minus phi tilde
<br>`32:43` of x t
<br>`32:46` also you see that these fields
<br>`32:50` always appear that cubic order
<br>`33:05` yeah so now we have already
<br>`33:08` an equation that updates
<br>`33:11` our parameters by this one step

### slide 8

<br>`33:15` right so now we say that for
<br>`33:21` [Music]
<br>`33:22` infinity
<br>`33:24` small uh coarse graining
<br>`33:31` that means our momentum shell is very
<br>`33:34` small
<br>`33:35` so we said that that this capital wonder
<br>`33:38` is something like one
<br>`33:40` plus l
<br>`33:46` we obtain
<br>`33:50` the first order
<br>`33:54` the following updating scheme tau
<br>`33:57` prime is equal to
<br>`34:00` one plus that's of course the taylor
<br>`34:03` expansion
<br>`34:04` l times two chi plus d
<br>`34:10` times tau
<br>`34:14` we have copper prime
<br>`34:17` sorry x one is d
<br>`34:20` this d prime
<br>`34:21` [Music]
<br>`34:23` one plus l two comma plus
<br>`34:27` d plus z minus two
<br>`34:34` [Music]
<br>`34:37` prime is one plus
<br>`34:41` l two pi plus
<br>`34:45` d plus z times copper
<br>`34:49` and gamma prime is one plus
<br>`34:53` l three chi plus
<br>`34:56` d plus z
<br>`35:00` times so that's the updating
<br>`35:04` of our parameters based on the restated
<br>`35:07` steps
<br>`35:08` now and this updating of these
<br>`35:11` parameters
<br>`35:12` is a result of that is dimensional
<br>`35:14` [Music]
<br>`35:15` same principle you can look at this you
<br>`35:18` can get these
<br>`35:19` updating just by looking at the
<br>`35:20` dimensions of things
<br>`35:25` and so this part here
<br>`35:28` was mathematically so let's say zero
<br>`35:32` effort
<br>`35:33` but in the second part the course
<br>`35:36` burning part
<br>`35:37` you have to invest a little bit more
<br>`35:39` thought
<br>`35:42` so how do we do that

### slide 9

<br>`35:46` no so how do we do the cosplay instead
<br>`35:48` cosplayer stuff
<br>`35:49` is difficult because we have to
<br>`35:51` integrate
<br>`35:54` over the momentum shell in this action
<br>`35:57` and this action
<br>`35:59` has parts that are cubic in the fields
<br>`36:03` that we don't know how to integrate
<br>`36:06` we know how to perform gaussian
<br>`36:07` integrals we have second order terms in
<br>`36:10` the fields
<br>`36:11` but we don't know how to integrate third
<br>`36:13` order terms in the field of higher order
<br>`36:15` terms
<br>`36:17` yeah so think about uh also like
<br>`36:20` statistical physics five to the four
<br>`36:22` terms
<br>`36:23` in the fight to the lambda we have a
<br>`36:26` five to the fourth term
<br>`36:28` and we don't know how to integrate these
<br>`36:30` things
<br>`36:31` so what we do is
<br>`36:34` what we say so and only so these
<br>`36:38` these calculations are really empty what
<br>`36:41` i'm
<br>`36:42` doing here i just give you for this
<br>`36:45` course grading stuff i just give you
<br>`36:46` sort of an overview of the steps
<br>`36:48` but i don't perform the actual integrals
<br>`36:51` now if you're interested
<br>`36:53` in the details
<br>`36:57` there is a review by hindelison
<br>`37:04` and this review is about
<br>`37:10` non-equilibrium
<br>`37:14` what is it molecule or phase conditions
<br>`37:16` or some non-including
<br>`37:18` something and but you immediately find
<br>`37:21` it because there's not
<br>`37:22` so many people who are archimedes and
<br>`37:25` write revenues with
<br>`37:26` uh 1 600 citations
<br>`37:30` uh on one equilibrium phase positions
<br>`37:33` and there you can find in the appendix
<br>`37:35` all of these calculations and how to
<br>`37:38` perform these calculations
<br>`37:40` so i'll just give you uh
<br>`37:44` a glimpse of how this works so the first
<br>`37:48` step is to say
<br>`37:49` okay we expand our action
<br>`37:52` to first order and that's called the
<br>`37:56` cumulative expansion we do this
<br>`37:59` accumulated
<br>`38:01` equivalent expansion then we see that
<br>`38:04` our
<br>`38:04` next action our updated action
<br>`38:08` is equal to the action
<br>`38:15` in the double wave vector so on the
<br>`38:17` larger length sets it inside
<br>`38:19` the momentum shell so in the core
<br>`38:23` of mental space plus
<br>`38:26` the first moment of this interacting
<br>`38:30` action
<br>`38:33` so plus the average expectation value
<br>`38:38` of this interaction part of the action
<br>`38:42` evaluated for the in the momentum shell
<br>`38:48` and evaluated in the context of the free
<br>`38:53` action that only has the gaussian term
<br>`38:56` so that's
<br>`38:57` what we see what we see here then the
<br>`38:58` higher order terms
<br>`39:00` so this contribution that we get is
<br>`39:02` integral
<br>`39:05` where the action here
<br>`39:10` so the definition of this average
<br>`39:13` is like this that we integrate only over
<br>`39:16` the
<br>`39:17` momentum shell so the very the highest
<br>`39:20` the highest momentum we have
<br>`39:21` in this in the system uh and we
<br>`39:24` wait for the for the average weight not
<br>`39:27` by the full action
<br>`39:29` but by the gaussian action
<br>`39:32` now that's the approximation then there
<br>`39:34` are higher order terms
<br>`39:35` that come on top of that and so what you
<br>`39:39` see here is a little bit what happened
<br>`39:40` here
<br>`39:41` is that we expanded the exponential in
<br>`39:44` this
<br>`39:45` action here by assuming that these
<br>`39:48` [Music]
<br>`39:50` interactions are actually weak now that
<br>`39:52` we expand the exponential
<br>`39:54` and we have a linear term here in front
<br>`39:57` of that
<br>`39:58` and if these interactions are weak
<br>`40:02` then we can make this expansion here and
<br>`40:05` we
<br>`40:05` for now which for today we truncated
<br>`40:07` after the first order and the whole
<br>`40:10` problem reduces
<br>`40:11` to calculating this thing here
<br>`40:15` or to calculating this thing
<br>`40:19` now we still don't know how to calculate
<br>`40:21` it
<br>`40:22` but it involves something that is second
<br>`40:25` order in the fields
<br>`40:27` yeah so that might actually be something
<br>`40:29` that we can do
<br>`40:30` and there's a theorem that helps us
<br>`40:33` helps
<br>`40:33` uh helps us to do these things let's go
<br>`40:36` to rick's
<br>`40:38` so this theorem tells us that if we have
<br>`40:41` such an
<br>`40:41` average so for example this is some
<br>`40:44` product of some fields here
<br>`40:48` and if we have an average of a product
<br>`40:50` of fields
<br>`40:53` and if we evaluate this average or if we
<br>`40:56` calculate this average
<br>`40:57` in the framework of the gaussian or the
<br>`40:59` second order
<br>`41:01` action then this complicated thing
<br>`41:05` can be expressed by a sum
<br>`41:08` over all pairwise contractions
<br>`41:11` of these fields yeah that means that we
<br>`41:16` look at all pairs of the things that we
<br>`41:18` have on the left hand side
<br>`41:21` put them together into groups of two
<br>`41:25` average around them
<br>`41:28` yeah averaged around them yeah
<br>`41:32` and then and then multiply and sum
<br>`41:35` over all possible ways of how you can
<br>`41:39` partition this product here in the
<br>`41:41` groups of twos
<br>`41:43` now so for example the bottom if you
<br>`41:46` have four
<br>`41:48` fields or fields evaluated at four
<br>`41:51` point in times so here's signify by phi
<br>`41:53` one five two five eight
<br>`41:55` three five four then we just have to
<br>`41:58` look at
<br>`41:59` all possible combinations of how to
<br>`42:03` make groups of twos out of these four
<br>`42:07` fields that we have yeah so
<br>`42:10` that reduces the problem
<br>`42:14` of calculating something that is highly
<br>`42:16` familiar
<br>`42:18` to something much more simple
<br>`42:21` we only have to write down all possible
<br>`42:24` combinations of these pairs called
<br>`42:26` contractions
<br>`42:27` of pairwise pairwise these pairwise
<br>`42:31` contractors here
<br>`42:32` those are these groups of twos and
<br>`42:36` just have to sum up all possible ways of
<br>`42:38` how we can do that
<br>`42:40` yeah and each of these states here is
<br>`42:43` now an integral sorry
<br>`42:44` there's one thing i forgot that should
<br>`42:47` have a zero here
<br>`42:48` as always in the context of this
<br>`42:51` simplified
<br>`42:52` action
<br>`42:55` now so that reduces the complexity of
<br>`42:58` the problem
<br>`43:00` to something that is only second order
<br>`43:02` in the fields
<br>`43:04` from something in general and
<br>`43:07` what we don't get then is what we have
<br>`43:10` to pay for
<br>`43:11` is a bookkeeping problem because if you
<br>`43:14` can imagine right
<br>`43:16` if this thing on the left-hand side is
<br>`43:17` sufficiently complex
<br>`43:20` then what you have on the right-hand
<br>`43:22` side involves a lot
<br>`43:23` of different terms so yeah that's a
<br>`43:26` bookkeeping exercise
<br>`43:28` i mean because it's a bookkeeping giving
<br>`43:31` exercise
<br>`43:32` that's difficult to overview because you
<br>`43:34` get many
<br>`43:35` if you have like one more four terms but
<br>`43:38` eight terms
<br>`43:39` the many possible ways of how you can
<br>`43:41` make these pairs of tools
<br>`43:43` yeah and this is
<br>`43:47` why we people invented
<br>`43:50` a graphical language of how to represent
<br>`43:54` these terms and this graphical language
<br>`43:57` in statistical physics
<br>`43:59` or in quantum frequency is called fame
<br>`44:01` and diagrams
<br>`44:03` in our case this graphical language is
<br>`44:06` actually pretty simple so we also have
<br>`44:09` famous
<br>`44:09` diagrams that we place that describe
<br>`44:14` such terms here but in our case these
<br>`44:18` diagrams have a
<br>`44:19` real meaning that is connected
<br>`44:22` or an intuitive meaning that is
<br>`44:24` connected to the time evolution of the
<br>`44:25` system
<br>`44:27` so first what they found with the
<br>`44:29` derivative say
<br>`44:31` is that if you have something
<br>`44:35` if you have in terms of this structure
<br>`44:37` here
<br>`44:38` then each of these here
<br>`44:42` the answer that we've also called the
<br>`44:44` propagator that we already had
<br>`44:46` in the action so these propagators here
<br>`44:48` these three propagators
<br>`44:53` they all become like a line
<br>`44:58` yeah and this also becomes a line
<br>`45:01` and once you have things
<br>`45:04` that are integrated over
<br>`45:08` for example you have here integral over
<br>`45:11` the coordinate set that the same
<br>`45:13` coordinate appears twice
<br>`45:15` in your turn then you have to connect
<br>`45:18` these things
<br>`45:20` these legs it is fine in that one

### slide 10

<br>`45:23` so we won't do that here today actually
<br>`45:26` that's
<br>`45:26` that's that's the subject of the quantum
<br>`45:28` fields just say
<br>`45:30` just say that there exists this
<br>`45:32` graphical language
<br>`45:34` now in our case because we only go to
<br>`45:37` first order
<br>`45:38` uh we don't have to deal with that but i
<br>`45:40` just want to say that these feminine
<br>`45:42` diagrams that popped up
<br>`45:44` in this uh that usually pop up in
<br>`45:46` quantum field theory
<br>`45:48` have a very nice intuition in these uh
<br>`45:51` directed percolation problems
<br>`45:53` so here it's actually i
<br>`45:57` copy they copied that from the from the
<br>`45:59` revenue of henryson
<br>`46:01` uh you
<br>`46:04` these diagrams for example look like
<br>`46:07` this one this loop here
<br>`46:09` corresponds actually to trajectories
<br>`46:11` that you have
<br>`46:13` in space not something like this now
<br>`46:16` basically what you do is you have your
<br>`46:19` building blocks
<br>`46:20` of your theory you are for example the
<br>`46:22` free propagator
<br>`46:24` now that would just be the gaussian term
<br>`46:27` and but you also have this other
<br>`46:29` building block that corresponds to
<br>`46:30` higher auditors
<br>`46:32` and then you just put them together and
<br>`46:36` these higher order terms of example this
<br>`46:38` one here have a real meaning in this
<br>`46:40` theory
<br>`46:41` in this framework because for example
<br>`46:43` this one would correspond
<br>`46:45` to a branching event or this one would
<br>`46:48` correspond
<br>`46:49` to a coalescent event
<br>`46:51` [Music]
<br>`46:52` where one of these if you look at this
<br>`46:57` space-time cross that we previously had
<br>`46:59` the upside down
<br>`47:01` then um that this would
<br>`47:05` correspond to events versus a separate
<br>`47:08` goblets form and then emerge again
<br>`47:10` so that's that's how these diagrams are
<br>`47:13` interpreted
<br>`47:14` in the frame of directed combination
<br>`47:18` now but as i said it's just a side
<br>`47:19` remark and we don't actually need that
<br>`47:21` today
<br>`47:23` because what we get is not that
<br>`47:25` complicated

### slide 11

<br>`47:26` what we do today is
<br>`47:31` that we
<br>`47:35` now proceed with the
<br>`47:39` integration of this uh
<br>`47:42` of the different parts of our action
<br>`47:46` so using what we said two slides away
<br>`47:50` is 274 this formula here
<br>`47:53` so that we expand our reaction in this
<br>`47:55` frame
<br>`47:57` and wix theory
<br>`48:01` okay so let's begin
<br>`48:04` so this is now the second step is the
<br>`48:08` course training
<br>`48:12` also so let's let's say let's say course
<br>`48:14` training
<br>`48:18` integrating
<br>`48:21` out
<br>`48:22` [Music]
<br>`48:24` the short leg scales
<br>`48:29` on the momentum shell
<br>`48:36` and we start
<br>`48:40` by looking at the free propagator
<br>`48:45` i'll show you now how this looked like
<br>`48:54` what the slides go so here we have the
<br>`48:57` action and momentum space
<br>`48:58` and the free propagator it's just
<br>`49:01` what is in between uh
<br>`49:05` this is what is between the inverse of
<br>`49:08` what is between
<br>`49:09` and between the the second order part
<br>`49:13` of the action so that's the same as a
<br>`49:16` quantum p theory of if you have already
<br>`49:18` quantum
<br>`49:18` theory or statistical fluid theory uh so
<br>`49:21` that's
<br>`49:22` just the very same thing so this one is
<br>`49:24` called
<br>`49:25` the inverse of the free propagator it's
<br>`49:28` called free propagator because it gives
<br>`49:30` you
<br>`49:30` the propagator that means how you uh go
<br>`49:33` from one
<br>`49:34` point in space and time to another point
<br>`49:37` in space and time
<br>`49:39` using only the frequent theory without
<br>`49:42` interactions
<br>`49:45` so this is the free propagator and this
<br>`49:48` term here is what we have to
<br>`49:54` integrate first
<br>`50:01` okay so the free propagation was that
<br>`50:04` this
<br>`50:05` do not okay
<br>`50:08` omega that was just defined
<br>`50:12` by the okay we actually use k
<br>`50:16` [Music]
<br>`50:20` we'll just check
<br>`50:24` okay okay
<br>`50:29` dk squared is just the definition
<br>`50:32` um
<br>`50:35` minus kappa minus i tau
<br>`50:38` omega
<br>`50:41` now to
<br>`50:46` first order
<br>`50:52` the propagator
<br>`50:56` is we normalized
<br>`51:02` by formulating so what we actually have
<br>`51:06` is the inverse of this
<br>`51:07` one over this
<br>`51:14` prime prime is the pre-propagated after
<br>`51:17` the first step
<br>`51:20` also
<br>`51:34` mathematical minus
<br>`51:38` gamma squared over 2 and the integration
<br>`51:42` over this momentum shell
<br>`51:46` dk prime e omega
<br>`51:59` plus omega times
<br>`52:11` minus omega prime so now you see we have
<br>`52:14` these two
<br>`52:15` propagators these propagators
<br>`52:19` you see here and that's what we had in
<br>`52:23` the quick symbol
<br>`52:26` is basically phi
<br>`52:29` of k
<br>`52:32` phi of k prime now these kind of things
<br>`52:36` right so now we let's just speak theory
<br>`52:38` and in the same
<br>`52:39` language this is just
<br>`52:48` uh this guy so we have these two arms
<br>`52:52` here and we integrate
<br>`52:56` over the case so
<br>`53:03` so that's why they have a loop
<br>`53:11` don't get distracted by these diagrams
<br>`53:14` it's not so
<br>`53:15` not so important it's just for those of
<br>`53:16` you who have already had
<br>`53:19` quantum theory just to see the
<br>`53:26` connection okay
<br>`53:28` [Music]
<br>`53:30` and now we can write that
<br>`53:36` explicitly so this first term is
<br>`53:40` k prime prime minus value d prime prime
<br>`53:44` k squared plus i prime prime
<br>`53:48` omega now let's adjust this on the left
<br>`53:52` hand side that's how we define that it
<br>`53:53` should have the same form as before
<br>`53:57` that's equal to k prime minus
<br>`54:00` d prime k squared plus i
<br>`54:05` tau squared minus
<br>`54:09` what now comes this integral here
<br>`54:13` and i'm just telling you the solution of
<br>`54:15` course the intervals
<br>`54:17` you know to say diagrams of everything
<br>`54:19` are just a way of writing things down
<br>`54:21` but in the end you have to solve
<br>`54:22` integrals yeah and you can if you're
<br>`54:24` interested in how this works
<br>`54:26` now you can look into the appendix of
<br>`54:29` this revenue of hinduism
<br>`54:32` i show you here just the results because
<br>`54:34` what we actually want to focus on is
<br>`54:38` integral integration techniques done so
<br>`54:41` i'll just give you the result
<br>`54:42` l k d i'll tell you about this what is
<br>`54:46` omega to the power of d
<br>`54:52` two tau
<br>`54:56` one over omega
<br>`55:00` squared d minus comma minus
<br>`55:03` omega square d over
<br>`55:08` 4 omega squared
<br>`55:11` d minus kappa
<br>`55:15` squared k squared
<br>`55:21` plus i tau
<br>`55:24` over 2
<br>`55:29` omega squared d minus
<br>`55:32` kappa squared omega plus
<br>`55:36` higher volatility so
<br>`55:40` this kd here
<br>`55:43` is just a surface area
<br>`55:49` of surface
<br>`55:52` area of
<br>`55:56` the domain
<br>`55:59` genome sphere
<br>`56:02` yeah and that just comes from the
<br>`56:04` integration by just integrating
<br>`56:06` over a mental shell that's what you
<br>`56:08` expect to get some kind of
<br>`56:10` seriousness of the sphere but now the
<br>`56:13` important thing
<br>`56:14` is that we don't have three different
<br>`56:15` troops i'll just
<br>`56:17` mount them in colors
<br>`56:21` we have this term we have
<br>`56:25` the d term
<br>`56:28` and we have the i
<br>`56:31` tau prime prime
<br>`56:35` double beta and now we have the same
<br>`56:38` term
<br>`56:38` on the right hand side as you have the
<br>`56:42` capacitor that pops up
<br>`56:46` here and here again we have
<br>`56:49` the d that pops up here
<br>`56:54` and here so that's the prefecture of
<br>`56:58` this k squared and we have the
<br>`57:03` tone that we have
<br>`57:06` here
<br>`57:09` and here
<br>`57:14` and this should have on the ground okay
<br>`57:18` okay so now we have kappa squared on the
<br>`57:21` left hand side
<br>`57:22` and we have terms on the right hand side
<br>`57:24` that look exactly
<br>`57:26` in structure like the ones on the left
<br>`57:28` hand side
<br>`57:29` and now we can compare them one by one
<br>`57:32` these terms and these two
<br>`57:35` this one and these two
<br>`57:39` and get our
<br>`57:42` prime prime d prime prime and target
<br>`57:46` by comparison to the right hand side
<br>`57:50` so i'll just tell you
<br>`57:54` the result that's the

### slide 12

<br>`57:59` renormalization
<br>`58:03` of the model parameters
<br>`58:09` okay so we have tau prime prime
<br>`58:12` is equal to tau prime minus
<br>`58:16` well that is right both
<br>`58:20` it was just comparing the left and the
<br>`58:22` right hand side of this equation
<br>`58:24` and putting terms together that have the
<br>`58:26` same
<br>`58:27` uh the same structure
<br>`58:31` okay d over
<br>`58:35` 8 omega squared d minus
<br>`58:38` kappa squared
<br>`58:42` d prime prime is equal to d
<br>`58:45` prime minus gamma squared
<br>`58:49` l k d omega squared
<br>`58:52` e over
<br>`58:56` 16 omega squared d minus
<br>`59:00` kappa squared and
<br>`59:03` final one is k squared
<br>`59:06` twice is equal to
<br>`59:11` minus down prime l
<br>`59:15` kd over
<br>`59:19` four tau omega squared
<br>`59:22` d minus
<br>`59:25` and for convenience we define this one
<br>`59:30` here
<br>`59:33` now as a
<br>`59:37` and we define this one here
<br>`59:45` sp
<br>`59:57` so now we have three in the updating
<br>`60:00` scheme
<br>`60:01` total updating scheme of three of the
<br>`60:03` parameters
<br>`60:05` that in principle allows us to link tau
<br>`60:07` prime prime
<br>`60:09` so after the two or the three steps of
<br>`60:11` the minimization group procedure
<br>`60:14` we update our parameters
<br>`60:18` uh in this form here and we still have
<br>`60:20` to plug in
<br>`60:21` the tau prime from previously from the
<br>`60:23` rescaling step
<br>`60:25` but there's one parameter missing and
<br>`60:27` that's the ugly one
<br>`60:28` now that's the one that describes our
<br>`60:30` higher order terms
<br>`60:33` you can imagine these
<br>`60:36` integrals of the higher order terms are
<br>`60:40` bonds more that's beautiful
<br>`60:44` but i'll just tell you the results
<br>`60:47` mainly that the cubic
<br>`60:54` sorry
<br>`60:58` the cubic so-called vertices
<br>`61:04` that's just cubic terms in the fields
<br>`61:08` we normalize
<br>`61:12` as
<br>`61:15` the proton is gamma prime
<br>`61:19` that we have to we have these diagrams
<br>`61:23` here
<br>`61:28` this one here and
<br>`61:33` this one
<br>`61:39` this one here now so you can see that
<br>`61:41` these are interaction terms that's third
<br>`61:43` quarter
<br>`61:44` that's why they have three legs but
<br>`61:47` they're also connected
<br>`61:48` here yeah and uh but both of them
<br>`61:52` one of them is just a time reversion
<br>`61:54` reversion of the other one
<br>`61:56` so both of them have the same value
<br>`61:59` so let me just now tell you the result
<br>`62:03` of this step here gamma prime prime
<br>`62:09` is gamma prime minus l
<br>`62:12` gamma to the power of 3 k
<br>`62:16` d over
<br>`62:19` two tau omega squared
<br>`62:23` d minus kappa squared
<br>`62:28` now so now we have the updating of all
<br>`62:30` of these parameters
<br>`62:35` and what we now do
<br>`62:38` is that we go to the limit
<br>`62:42` of so so this is not very convenient
<br>`62:45` right because we have to
<br>`62:46` still to plug in the tau prime and d
<br>`62:48` prime and
<br>`62:51` then we don't have to we still don't
<br>`62:52` have anything
<br>`62:54` uh that we can deal with so we don't
<br>`62:57` know how to deal with these updating
<br>`62:59` schemes
<br>`63:00` it's much more convenient to have
<br>`63:01` something that gives a differential
<br>`63:03` equation
<br>`63:04` you know but it's easy for us to derive
<br>`63:08` a differential equation

### slide 13

<br>`63:10` mainly we just set the limit
<br>`63:14` in the limit
<br>`63:17` l to zero so that we
<br>`63:21` really just integrate out a tiny bit
<br>`63:24` each step so then the momentum shell is
<br>`63:28` small
<br>`63:30` we can write
<br>`63:33` we can
<br>`63:37` write these
<br>`63:42` relations in differential form
<br>`63:52` yeah and i'll just give you the result
<br>`63:56` delta l tau
<br>`64:00` is equal to tau times two k
<br>`64:04` plus v minus two times
<br>`64:08` a and then the a was the thing but for
<br>`64:10` the integral
<br>`64:16` [Music]
<br>`64:23` [Music]
<br>`64:25` to coil plus b plus z
<br>`64:28` minus a
<br>`64:33` and then the pepper
<br>`64:38` is equal to whether the
<br>`64:41` scale derivative of color is
<br>`64:46` 2 plus d
<br>`64:49` plus z minus b
<br>`64:53` and gamma interactions
<br>`64:57` are given by gamma times
<br>`65:00` 3
<br>`65:04` minus 8 a
<br>`65:08` this is not called
<br>`65:11` the realization flow
<br>`65:16` this is what i showed you at the
<br>`65:17` beginning of the lecture where i said
<br>`65:19` okay so we have this space of all
<br>`65:21` possible actions
<br>`65:23` our minimalization brings us
<br>`65:26` lets us travel place through the space
<br>`65:29` of all possible actions
<br>`65:34` okay now that's the realization group
<br>`65:37` workflow
<br>`65:38` and now we're in the framework of
<br>`65:41` bonding and dynamics
<br>`65:42` and number we have some differential
<br>`65:45` equations
<br>`65:46` that are coupled and these differential
<br>`65:50` equations
<br>`65:52` we now need to treat with the tools
<br>`65:56` of non-linear dynamics
<br>`66:00` okay so first we simplify that a little
<br>`66:02` bit
<br>`66:06` and what we do is when we do the course
<br>`66:08` grading
<br>`66:10` in space and time anything that we
<br>`66:12` should get
<br>`66:15` should be independent of the scale of
<br>`66:17` courseware because our system is
<br>`66:18` self-similar
<br>`66:20` yeah and so that means we have to
<br>`66:24` we have a choice to set the length scale
<br>`66:27` and the time scale to whatever is good
<br>`66:31` for us
<br>`66:32` and i'll tell you what is good for us
<br>`66:35` we set a time scale
<br>`66:36` [Music]
<br>`66:39` set the time scale
<br>`66:44` such that dell
<br>`66:47` tau is zero
<br>`66:53` and length scale
<br>`66:59` such that dell
<br>`67:04` is it d is equal to zero
<br>`67:10` and then we get
<br>`67:13` two equations from that by just by
<br>`67:16` setting the left-hand side to zero
<br>`67:18` it's four minus epsilon which are
<br>`67:20` everybody fine
<br>`67:22` plus two chi b minus two a
<br>`67:26` is zero and two minus
<br>`67:30` epsilon plus two chi
<br>`67:33` plus z minus a
<br>`67:39` is equal to zero
<br>`67:42` yeah and here i set
<br>`67:45` epsilon equal to 4 minus d
<br>`67:56` and with this
<br>`67:59` i'm left with two flow equations
<br>`68:03` one for copper and one for
<br>`68:08` gout
<br>`68:11` copper is 2 plus
<br>`68:14` a minus b
<br>`68:18` gamma x1 over 2
<br>`68:22` minus six eight
<br>`68:27` so that that looks already a little bit
<br>`68:29` nicer

### slide 14

<br>`68:35` okay so the next step
<br>`68:39` we're always almost done with the
<br>`68:42` hot stuff in the next step
<br>`68:52` next step we're interested in the fixed
<br>`68:54` point
<br>`68:55` we've got the fixed point determines our
<br>`68:57` microscopic
<br>`68:58` behavior okay so behavior
<br>`69:06` near
<br>`69:11` the fixed point
<br>`69:19` where by definition of the fixed point
<br>`69:22` cover
<br>`69:23` the derivative of capital gamma
<br>`69:27` about equal to zero
<br>`69:31` what we then get is the value of
<br>`69:35` a star that a
<br>`69:39` our complex term that we had before at
<br>`69:41` the fixed point
<br>`69:42` takes the value of epsilon over 12
<br>`69:46` and b takes the value
<br>`69:50` 2 plus epsilon over 12.
<br>`69:56` and now we substitute that
<br>`69:59` into let me see
<br>`70:04` this equation here
<br>`70:18` we substitute into this equation and we
<br>`70:21` get
<br>`70:21` our first two critical exponent
<br>`70:28` exponents
<br>`70:31` chi is minus two
<br>`70:34` plus seven epsilon divided by twelve
<br>`70:40` let's say it is equal to 2 minus
<br>`70:44` epsilon divided by 12.
<br>`70:49` thus we have our first two critical
<br>`70:50` exponents
<br>`70:54` now
<br>`70:57` as a
<br>`71:01` we substitute just this into the proper
<br>`71:04` definition of the fixed points
<br>`71:06` our a's and b's are something
<br>`71:07` complicated
<br>`71:11` and uh we'll just write it down
<br>`71:14` substitute
<br>`71:18` definition of a
<br>`71:21` and b and what then
<br>`71:33` squared epsilon divided by
<br>`71:36` 24 plus epsilon
<br>`71:41` so everything i'm doing right now now is
<br>`71:44` not
<br>`71:44` complicated mathematics that's just
<br>`71:46` algebra
<br>`71:49` gamma star is 2
<br>`71:52` d 24 plus epsilon
<br>`71:56` over 24 plus
<br>`71:59` 5 epsilon
<br>`72:03` epsilon tau over
<br>`72:08` kd
<br>`72:11` okay so this is our fixed point and the
<br>`72:14` next step
<br>`72:16` we linearize around our phase point
<br>`72:23` linear rise rg flow
<br>`72:29` around fixed point remember
<br>`72:32` a little non-linear dynamics what we do
<br>`72:35` is we
<br>`72:36` look we put ourselves into the fixed
<br>`72:39` point
<br>`72:41` so now we've got the fixed point now we
<br>`72:42` want to say is it stable or is it
<br>`72:44` unstable
<br>`72:45` now will we be pushed out of the fixed
<br>`72:47` point or will be
<br>`72:48` sucked in is it attractive or not
<br>`72:52` now and the way we do that is we look go
<br>`72:54` into the fixed point
<br>`72:56` and what we said this dynamical systems
<br>`72:59` lecture
<br>`73:00` is that we then look at the derivative
<br>`73:03` 1d system the derivative of this fixed
<br>`73:05` point and here
<br>`73:06` what we do is linear wise around the
<br>`73:08` fixed point and then the
<br>`73:10` derivative in higher dimensions is
<br>`73:12` called jacobian
<br>`73:13` now that's what we do just it's just an
<br>`73:16` expansion
<br>`73:17` around the value of this point
<br>`73:20` and what we get is l in
<br>`73:23` vector form kappa gamma
<br>`73:29` is equal to
<br>`73:32` that's the jacobian
<br>`73:35` of our flow equation also 2
<br>`73:38` minus epsilon over 4 0
<br>`73:42` 0 minus epsilon
<br>`73:47` and then here the distance to the fixed
<br>`73:49` point copper star
<br>`73:51` minus copper and gamma star
<br>`73:55` minus gum and of course we have higher
<br>`73:59` orders
<br>`74:02` so the eigen values of this
<br>`74:07` jacobian they tell us whether this fifth
<br>`74:11` bond is stable or not
<br>`74:13` so here we're just looking at a
<br>`74:14` non-linear dynamical
<br>`74:17` system but we use the same tools yeah
<br>`74:19` and and if you have
<br>`74:20` not just one dimension but two
<br>`74:22` dimensions like here
<br>`74:24` we're now looking at jacobian and then
<br>`74:27` the eigenvalues of this jacobian we're
<br>`74:30` now looking at the slope
<br>`74:31` in the fixed bond as an 1d and
<br>`74:33` simplified
<br>`74:34` now look at the iron bonds
<br>`74:39` this is the
<br>`74:47` okay the eigenvalues
<br>`74:54` determine
<br>`74:58` stability
<br>`75:04` so we have that 2 minus epsilon over 4
<br>`75:09` is larger than 0
<br>`75:14` that means that the fixed point
<br>`75:20` is unstable
<br>`75:24` in the direction of the parameter cover
<br>`75:30` minus epsilon sorry that's not a real
<br>`75:32` epsilon here
<br>`75:39` epsilon minus epsilon
<br>`75:43` is smaller than zero that means the
<br>`75:46` fixed point
<br>`75:50` is
<br>`75:58` and what this means if you think about
<br>`76:00` our
<br>`76:03` language that we introduce at the
<br>`76:05` beginning of the lecture
<br>`76:06` is that the parameter kappa draws us
<br>`76:10` away from the critical manifold
<br>`76:13` and the parameter gamma pulls us
<br>`76:16` here basically pulls us into the
<br>`76:18` critical
<br>`76:19` into the relationship
<br>`76:24` that's another requisition to draw that

### slide 15

<br>`76:28` so we can have a little diagram
<br>`76:31` it looks like this
<br>`76:40` and so here we have our fifth point
<br>`76:44` and that will flow
<br>`76:50` lines
<br>`76:54` our flow will go into the fifth point
<br>`76:58` along the gamma direction
<br>`77:07` and out of the fixed point along the
<br>`77:09` copper direction
<br>`77:13` that means lots of points
<br>`77:20` points on blue line
<br>`77:26` flow into the fixed point
<br>`77:30` that means we need
<br>`77:38` to tune cathode
<br>`77:42` to reach the fixed point
<br>`77:51` so now we get the final response
<br>`77:56` now with
<br>`78:00` the definition of physics
<br>`78:06` this time
<br>`78:09` was this at the very beginning we
<br>`78:11` introduced the kai
<br>`78:13` as how the fields we scale
<br>`78:17` when we change the length scale and by
<br>`78:20` this definition
<br>`78:21` of coin this is equal to our older
<br>`78:24` definition of these
<br>`78:25` problems better over
<br>`78:29` new perpendicular
<br>`78:36` [Music]
<br>`78:37` that was defined as
<br>`78:40` the dynamical critical exponent as new
<br>`78:44` parallel over new of a new
<br>`78:47` perpendicular and kappa
<br>`78:53` is our distance to the critical point
<br>`78:58` lambda minus lambda c and that's how we
<br>`79:01` call it
<br>`79:06` okay and then we just plug these things
<br>`79:08` in and we get these three exponents
<br>`79:10` yeah beta is equal to one minus epsilon
<br>`79:14` over six
<br>`79:16` new perpendicular is equal to one half
<br>`79:19` plus
<br>`79:20` epsilon over 60 and
<br>`79:24` new parallel is equal to 1 plus
<br>`79:29` epsilon over 12. and these are our
<br>`79:35` exponents now that we got from the
<br>`79:39` linearization
<br>`79:40` procedure
<br>`79:43` so how general
<br>`79:46` are these results these exponents took
<br>`79:50` a simple epidemic model and derived
<br>`79:52` exponents

### slide 16

<br>`79:54` at the beginning of this lecture i told
<br>`79:56` you something about universality
<br>`79:58` now that different models are different
<br>`80:02` microscopic theories
<br>`80:04` are described by the same macroscopic
<br>`80:06` behavior
<br>`80:09` so and this is something that's not
<br>`80:11` completely understood
<br>`80:14` but the models that are disqualified by
<br>`80:16` the same critical exponents
<br>`80:18` are says that they belong to the
<br>`80:21` directed
<br>`80:22` preparation class
<br>`80:26` and the model
<br>`80:31` belongs to
<br>`80:34` the directed
<br>`80:39` percolation
<br>`80:44` universality
<br>`80:48` class if that's the so-called directed
<br>`80:51` percolation conjecture
<br>`80:56` this base phase transition
<br>`81:01` it displays
<br>`81:05` the face transition
<br>`81:12` between
<br>`81:14` active and
<br>`81:21` absorbing
<br>`81:24` phase so this existence of one absorbing
<br>`81:28` point
<br>`81:29` is very important the second thing
<br>`81:32` is after the adobe point was when the
<br>`81:35` disease got extinct the second is
<br>`81:40` order parameter the order parameter
<br>`81:48` is positive
<br>`81:52` now the system is a one-dimensional
<br>`81:54` system
<br>`81:57` so the spatial dimensions uh changes as
<br>`82:00` you see from the exponents
<br>`82:02` [Music]
<br>`82:08` the order parameter is one-dimensional
<br>`82:10` that's the other which is one
<br>`82:11` one-dimensional parameter this the whole
<br>`82:14` parameter is scalar so it's not spatial
<br>`82:18` okay the third one is
<br>`82:23` there's no other bells and whistles so
<br>`82:26` you have no
<br>`82:27` special attributes no
<br>`82:32` special attributes
<br>`82:39` like spatial
<br>`82:42` heterogeneity
<br>`82:48` yeah so if for example the infection
<br>`82:50` rate depends
<br>`82:51` on where you which letter side you are
<br>`82:53` on
<br>`82:54` then these exponents could be different
<br>`82:57` difficult they are different
<br>`82:59` so what they said is if these three
<br>`83:01` conditions
<br>`83:02` are fulfilled you can't expect your
<br>`83:05` system
<br>`83:06` to be in the directed population in
<br>`83:09` reality class
<br>`83:11` and to have the same critical exponents
<br>`83:16` now just uh before we all go into
<br>`83:18` christmas
<br>`83:20` there's now a little uh final
<br>`83:23` reveal for you yeah so
<br>`83:26` in the beginning of the lecture i
<br>`83:29` we talked about what is a
<br>`83:31` non-equilibrium system
<br>`83:34` and the way we defined it different ways
<br>`83:38` to define it
<br>`83:39` the way to define it the way we defined
<br>`83:41` it is that we said
<br>`83:43` okay the system has a contact with
<br>`83:46` different paths
<br>`83:49` and these bars are incompatible
<br>`83:53` so what are the paths in direct
<br>`83:56` percolation or in this epidemic model
<br>`84:02` normally only if anybody was in the room
<br>`84:04` now we would
<br>`84:05` try to solve that together uh but as
<br>`84:08` you're all sitting
<br>`84:10` in front of your computer and maybe
<br>`84:12` watching netflix
<br>`84:13` in parallel yeah so i'll give you the
<br>`84:16` answer
<br>`84:17` so what is actually here the bath
<br>`84:20` directed percolation
<br>`84:21` so so it's actually uh
<br>`84:24` it's actually quite difficult to see
<br>`84:27` that what are the heat
<br>`84:28` what are the paths what drives direct
<br>`84:32` percolation out of equilibrium
<br>`84:34` it's the absorbing point now that you
<br>`84:37` have a point
<br>`84:38` where you can go in but it can never go
<br>`84:41` out
<br>`84:42` and when you're in that point then
<br>`84:45` you're clearly not an equilibrium
<br>`84:47` because there's no terminal there are no
<br>`84:49` terminal fluctuations
<br>`84:52` now in reality so and this is an
<br>`84:54` approximation
<br>`84:56` that you have an absorbent state in
<br>`84:58` reality
<br>`84:59` you can get out of the absorbing point
<br>`85:02` you just have to wait a few hundred
<br>`85:03` million years
<br>`85:05` for the virus one that had gone extinct
<br>`85:09` to come back by evolution that takes a
<br>`85:11` long time but this process exists
<br>`85:13` but we say in this theory that
<br>`85:17` this probability of this rate which you
<br>`85:19` get out of this
<br>`85:20` point out of the absorbing state is
<br>`85:23` exactly equal to zero
<br>`85:26` now that's the tiny thing that we do and
<br>`85:30` what this means is that the system is
<br>`85:32` coupled
<br>`85:33` to two heat bars
<br>`85:39` and these defaults are incompatible
<br>`85:41` there's one heat bath
<br>`85:43` that has a temperature zero and the
<br>`85:46` other bath that has a temperature
<br>`85:49` that is larger than zero that causes
<br>`85:52` really some fluctuations
<br>`85:55` now what are these heat buffs coupled
<br>`85:59` to now the final thing is that these
<br>`86:02` heat bars are coupled into time
<br>`86:05` so in one pound direction dt
<br>`86:08` smaller than zero yeah you have a zero
<br>`86:12` temperature
<br>`86:13` in the vicinity of the abdominal state
<br>`86:15` and in the other direction
<br>`86:17` d2 larger than zero never find that
<br>`86:20` temperature now and this two heat parts
<br>`86:23` coupled to different type directions
<br>`86:25` makes the system allow to go into the
<br>`86:28` absorbing state
<br>`86:30` but never leave it now that's this
<br>`86:32` asymmetry
<br>`86:34` that of these two incompatible bars
<br>`86:37` that makes this one of the hallmark
<br>`86:40` non-equilibrium systems in one
<br>`86:42` equilibrium
<br>`86:44` physics and what i showed you actually
<br>`86:46` here
<br>`86:47` this is extremely powerful
<br>`86:50` there's a lot of models that have
<br>`86:52` nothing to do with epidemics that fall
<br>`86:54` into this impossibility class
<br>`86:57` and so it's one of the
<br>`87:01` paradigmatic moments of non-acrylic
<br>`87:04` non-equilibrium statistical physics
<br>`87:09` okay so that was quite a tough lecture
<br>`87:12` yes
<br>`87:12` also for me i'm quite exhausted and what
<br>`87:15` i would
<br>`87:16` say is that uh you will have a great
<br>`87:19` christmas
<br>`87:20` and after uh the new year i'm joining
<br>`87:24` the fifth i think that's our next
<br>`87:27` lecture and then
<br>`87:28` actually we'll do something completely
<br>`87:29` different different and we have a look
<br>`87:31` at some real data
<br>`87:33` and we'll get into data science and see
<br>`87:35` what actually to do with data
<br>`87:38` this data is really really large how
<br>`87:40` actually you see these things that we've
<br>`87:41` studied
<br>`87:42` in the last lectures in the last three
<br>`87:45` months how to actually see that
<br>`87:47` in data now that's not very trivial if
<br>`87:50` somebody comes
<br>`87:51` up to you with 10 terabytes of data then
<br>`87:53` you can't just start matlab and start
<br>`87:55` phishing around
<br>`87:56` and you need special tools from data
<br>`87:58` science that allow you to extract
<br>`88:01` such features from data that can have
<br>`88:04` 100 millions of dimensions that's what
<br>`88:07` we do right after the
<br>`88:09` after christmas on january 5th and when
<br>`88:12` once we've done that we'll also have
<br>`88:13` some guest
<br>`88:14` lectures done by real experts
<br>`88:18` in this field and
<br>`88:22` and once we've learned like the
<br>`88:24` fundamentals of data science
<br>`88:26` we'll have put that all together and
<br>`88:28` look into some actual
<br>`88:29` research data and see how we can
<br>`88:33` uh use these two tools from the
<br>`88:36` visualization
<br>`88:38` data science to actually dig into some
<br>`88:42` current experimental data okay so then
<br>`88:45` uh merry christmas everyone if you
<br>`88:47` celebrate that
<br>`88:49` and uh see you all next week next year
<br>`88:52` okay bye i'll stay there are
<br>`88:55` any questions 

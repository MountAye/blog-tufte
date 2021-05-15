---
layout:      post
title:      ".mpipks-transcript | 10. Dimension Reduction"
keywords:   "mpipks-transcript"
excerpt:    "这一讲由嘉宾给出，官网没有课件。所以不再做课件帧数的标记了。作为替代，随堂做了笔记，参见[笔记部分]"
date:        2021-05-14
categories:  post
milestoneID: 39
---

> 这一讲由嘉宾给出，官网没有课件。所以不再做课件帧数的标记了。作为替代，随堂做了笔记，参见[笔记部分]({% post_url 2021-05-15-mpipks-non-equilibrium-physics-note-10-dimension-reduction %})。

<br>`00:07` okay so let's
<br>`00:08` uh let's join uh so welcome
<br>`00:12` to our uh lecture again now to this uh
<br>`00:16` today we have a special guest as we uh
<br>`00:19` which is fabian
<br>`00:21` ross that you see on the other window
<br>`00:23` and as you remember
<br>`00:25` uh we before christmas we introduced uh
<br>`00:28` theoretical physics concepts that
<br>`00:30` explain how order emerges
<br>`00:33` in non-equilibrium systems and then last
<br>`00:36` week i started
<br>`00:37` introducing some basic tools
<br>`00:40` from data science namely what are the
<br>`00:43` tools that we can use
<br>`00:45` to computationally deal with large
<br>`00:48` amounts of data
<br>`00:50` and today so i need some special help
<br>`00:53` from somebody who's a real expert
<br>`00:56` which is far beyond you know fabian is a
<br>`00:59` trained
<br>`01:00` uh physicist and did a phd in
<br>`01:02` mathematical biology
<br>`01:04` i then did a postdoc in my group at the
<br>`01:07` max plain institute in dresden and now
<br>`01:10` he's a professional
<br>`01:12` uh data scientist and bioinformatician
<br>`01:16` at the center for regenerative therapies
<br>`01:18` in dresden
<br>`01:20` and so he's talking actually about
<br>`01:21` something that he's uh
<br>`01:23` doing for his professional job which is
<br>`01:25` very nice
<br>`01:26` and uh over to you fabian thanks a lot
<br>`01:29` for
<br>`01:30` for sharing your expertise yeah
<br>`01:33` thanks thanks for having me here uh for
<br>`01:36` giving miss
<br>`01:37` uh giving me this opportunity so to give
<br>`01:39` a lecture on
<br>`01:40` exploring high dimensional data so i
<br>`01:42` think uh stefan
<br>`01:44` introduced me very well thank you very
<br>`01:47` much and
<br>`01:48` and also made the point of where we are
<br>`01:51` in the course
<br>`01:53` so i just wanted to ask you i just would
<br>`01:56` uh to say that uh whenever you
<br>`01:58` uh wanna ask something i think during
<br>`02:00` the course you just like uh unmuted
<br>`02:01` yourself and ask the question so that's
<br>`02:03` totally fine to me also
<br>`02:05` type something in the chat and i try to
<br>`02:07` try to answer and then uh
<br>`02:09` like if you're not saying anything uh
<br>`02:11` please mute yourself to reduce noise
<br>`02:14` um
<br>`02:18` all right so um okay i'm
<br>`02:22` i'm going to start right away
<br>`02:25` um so today will be about um exploring
<br>`02:29` uh high dimensional data
<br>`02:30` right and as many of you
<br>`02:34` know with a high dimensional and in high
<br>`02:36` dimensions
<br>`02:37` strange things can happen so if you for
<br>`02:39` instance look at this thing here what
<br>`02:41` you see here is a three-dimensional
<br>`02:42` projection
<br>`02:43` of a four-dimensional object rotating
<br>`02:46` and this
<br>`02:47` looks very funny right and i mean like
<br>`02:49` four dimensions is where we kind of
<br>`02:51` still can kind of get a glimpse but but
<br>`02:53` what if it gets to
<br>`02:54` thousands or millions of dimensions what
<br>`02:56` do we do with these kind of data
<br>`02:59` um so before i start
<br>`03:02` uh let me let me give you a brief
<br>`03:04` structure of the course
<br>`03:06` today of the lecture um
<br>`03:18` might have to click into the window
<br>`03:21` no i actually want to share okay
<br>`03:25` my ipod screen yes sorry for the delay
<br>`03:29` um all right so so i basically start
<br>`03:33` by introducing what i mean by high
<br>`03:35` dimensional data
<br>`03:41` um i will then
<br>`03:44` cover two dimension
<br>`03:48` dimensionality reduction methods
<br>`03:51` [Music]
<br>`03:58` and also talk a bit like what's the idea
<br>`04:01` of of
<br>`04:01` reducing dimensions and third if we
<br>`04:04` still have time i'll talk a little bit
<br>`04:06` about
<br>`04:06` clustering which we kind of can think of
<br>`04:08` as a discrete form of dimensionality
<br>`04:11` reduction i'd say
<br>`04:13` so what do i mean by high dimensional
<br>`04:16` data
<br>`04:18` well let's let's start with an object
<br>`04:21` that i call a data matrix
<br>`04:28` um x which is of shape n by m
<br>`04:41` and maybe you remember from last week um
<br>`04:45` tidy data formats so this um uh
<br>`04:49` matrix should be in a tidy format
<br>`04:50` already so in the rows we have
<br>`04:52` n samples
<br>`04:57` and in the columns we have m
<br>`04:59` measurements or observables
<br>`05:08` um so what do i mean by this so so an
<br>`05:11` example could be what you what you
<br>`05:12` measure here is for instance you um
<br>`05:15` uh take a uh take yourself right and you
<br>`05:19` measure for instance the length of your
<br>`05:21` thumb and the length of your index
<br>`05:22` finger and the length of your middle
<br>`05:24` finger and so on you do the same thing
<br>`05:26` on there
<br>`05:26` with the other hand you measure your
<br>`05:28` foot size your body height
<br>`05:30` maybe uh the heartbeat rate and so on
<br>`05:32` and and uh
<br>`05:33` you end up gathering more and more
<br>`05:35` observables
<br>`05:38` and that's m observables and this gives
<br>`05:40` us the dimensionality of our data
<br>`05:44` um and now you can do this with yourself
<br>`05:47` and you can do this well you can ask
<br>`05:49` your friends to do it with them and so
<br>`05:50` on and then
<br>`05:52` you can maybe do it with all people in
<br>`05:55` asia all over the world and this uh
<br>`05:57` gives you the number of samples that you
<br>`05:58` have right
<br>`06:00` um now how do you how do you treat these
<br>`06:04` this kind of data right if we go one
<br>`06:06` step back
<br>`06:07` and uh think about how how can we
<br>`06:10` visualize
<br>`06:11` and uh stephan uploaded some slides on
<br>`06:14` that and and maybe we'll also talk on
<br>`06:16` that a little bit but
<br>`06:18` what can we what can we actually
<br>`06:20` visualize easily
<br>`06:22` um
<br>`06:28` so if you uh if you would have one
<br>`06:31` dimensional data right that's rather
<br>`06:33` easy right
<br>`06:34` you you can um just uh plot your data
<br>`06:38` on a one-dimensional line for instance
<br>`06:40` and also
<br>`06:41` for two dimensions
<br>`06:45` um i think this is pretty
<br>`06:47` straightforward right
<br>`06:49` um so if this would be the
<br>`06:53` entries of our data matrix x1 x2
<br>`06:57` um we can just plot them as a scatter
<br>`07:00` plot right
<br>`07:02` and we could for instance see whether
<br>`07:03` they are correlated or not
<br>`07:05` but um as soon as we are like
<br>`07:08` in in three dimensions or larger like
<br>`07:10` three dimensions we can still
<br>`07:11` handle we can do a three-dimensional
<br>`07:13` plot maybe but this is still
<br>`07:15` hard to quantify um this this gets um
<br>`07:19` this gets uh non-trivial right and so we
<br>`07:22` need techniques to
<br>`07:24` to uh think about how to actually look
<br>`07:26` at these data and how to analyze these
<br>`07:28` data so
<br>`07:30` the aim of dimensionality reduction then
<br>`07:35` i'd say is to reduce the number of
<br>`07:42` observables
<br>`07:50` while keeping
<br>`07:57` relevant information
<br>`08:04` and what this relevant information is
<br>`08:06` right this is something uh
<br>`08:08` you you have to decide by the problem at
<br>`08:11` hand
<br>`08:12` um now um
<br>`08:15` before i go
<br>`08:18` into talking about how you can reduce
<br>`08:21` dimensionality
<br>`08:22` i wanted to show you some examples
<br>`08:26` so i'll share some slides for this
<br>`08:33` um and so
<br>`08:37` i think as many physicists are in the
<br>`08:39` audience one example i wanted to share
<br>`08:41` something
<br>`08:41` that i think many of you are already
<br>`08:44` know
<br>`08:45` which is um where we know where many of
<br>`08:48` you know that a
<br>`08:49` low number of observables actually
<br>`08:51` suffice to to describe the system very
<br>`08:53` well and that's in the realm of
<br>`08:54` statistical physics and you
<br>`08:56` saw a lot of uh examples from stefan by
<br>`08:58` that
<br>`08:59` but even in a rather easy example like
<br>`09:01` an and paramagnetic
<br>`09:03` iso model right you know that there's uh
<br>`09:07` there's many many spins in this system
<br>`09:09` right and imagine you could measure all
<br>`09:11` these spins
<br>`09:12` um you have a very high dimensional
<br>`09:15` representation of the state of the
<br>`09:17` system then
<br>`09:18` but many of these spins will be
<br>`09:20` correlated and we know from statistical
<br>`09:22` physics that actually you can
<br>`09:24` very well describe the microscopic state
<br>`09:26` of such a system
<br>`09:27` with just the magnetization
<br>`09:30` now what will happen if we come from the
<br>`09:32` other side from the data science
<br>`09:34` perspective and that's a
<br>`09:36` paper here an archive by sebastian
<br>`09:38` vetzel and what he did was
<br>`09:40` um he
<br>`09:44` did a simulation of a ferromagnetic
<br>`09:46` icing model on a 28 by 28 letters
<br>`09:49` at different temperatures and so 28 by
<br>`09:52` 28 gives
<br>`09:53` you 784 spins right and we he recorded
<br>`09:57` the state of all these spins and 50 000
<br>`09:59` different samples at different
<br>`10:00` temperatures
<br>`10:02` and now you have a data matrix with 784
<br>`10:04` dimensions right and then you can start
<br>`10:07` to
<br>`10:07` say okay if i just would have this
<br>`10:10` matrix and i wouldn't know nothing about
<br>`10:11` the system how can i look for order in
<br>`10:14` this system and how can i reduce
<br>`10:15` dimension and one of these techniques is
<br>`10:18` called principal components analysis and
<br>`10:20` i'll explain later what this actually is
<br>`10:22` but if you do this you get a result like
<br>`10:24` this the first principal component
<br>`10:27` which is a one-dimensional
<br>`10:28` representation of of this
<br>`10:31` high-dimensional data matrix perfectly
<br>`10:33` scales with the magnetization
<br>`10:35` so in this way you would actually be
<br>`10:37` able to kind of discover
<br>`10:39` an order parameter without knowing
<br>`10:42` anything about the system
<br>`10:43` by having detailed microscopic data of
<br>`10:45` the system
<br>`10:47` so this is rather an artificial example
<br>`10:50` right because we know very well but how
<br>`10:52` how an ising model is behaved but what
<br>`10:54` about
<br>`10:55` systems where we don't really know how
<br>`10:57` they work for instance humans
<br>`11:00` um so this is a paper from nature in
<br>`11:02` 2008
<br>`11:04` last authors bustamante and
<br>`11:07` what they did was they quantified human
<br>`11:09` dna
<br>`11:10` so they took 3 000 european humans
<br>`11:14` and now you can imagine that the dna is
<br>`11:18` a long string of
<br>`11:19` characters right and and to a large part
<br>`11:22` these this is conserved from one human
<br>`11:25` to
<br>`11:25` an to another human so the dna will be
<br>`11:28` pretty much the same
<br>`11:29` but at some positions we have variations
<br>`11:31` right the dna from one human to another
<br>`11:33` is not exactly the same and at half a
<br>`11:35` million positions
<br>`11:37` the orthos quantified the dna state
<br>`11:40` and so this gives you a a a data set
<br>`11:43` with a dimension of half a million
<br>`11:45` approximately for 3 000 humans and then
<br>`11:48` they did the dimensionality reduction
<br>`11:49` and again they did a
<br>`11:51` principal component analysis and this is
<br>`11:53` a two-dimensional representation of this
<br>`11:55` high dimensional data set
<br>`11:57` and what i want to ask you now is to
<br>`12:00` look at the picture and you don't
<br>`12:01` yet have to understand what the
<br>`12:03` principal components mean but i i want
<br>`12:05` to ask you to type in the ted
<br>`12:07` in the chat if you can what you see in
<br>`12:10` this picture
<br>`12:23` it's a very difficult or very shy
<br>`12:25` audience
<br>`12:30` what does it look like it look
<br>`12:33` if the meat looks like an elephant
<br>`12:38` it is a scatter plot yes and uh we see
<br>`12:41` some clusters yes
<br>`12:43` there's also uh some sensible answers
<br>`12:47` yes and it's actually um uh the uh
<br>`12:53` now i don't see my mouse anymore i think
<br>`12:57` adolfo got it right
<br>`12:58` yes i don't forgot it right it's already
<br>`13:00` the second answer
<br>`13:01` um it resembles a map of europe and
<br>`13:09` that's exactly what the title of the
<br>`13:11` paper was uh jeans mirrored geography
<br>`13:13` within europe right so
<br>`13:15` this was uh i think it's quite amazing
<br>`13:17` so you just
<br>`13:18` record the dna of humans right
<br>`13:21` and basically this gives you a map of
<br>`13:24` europe
<br>`13:25` approximately it kind of makes sense
<br>`13:26` right that the genes are
<br>`13:28` like um uh like um
<br>`13:31` well somewhat remain local
<br>`13:36` um so here's another example
<br>`13:40` um there's a very i'd say maybe
<br>`13:42` unphysical example but i think it
<br>`13:44` it works nicely these kind of examples
<br>`13:47` using
<br>`13:48` images work nicely to explain
<br>`13:50` dimensionality reduction techniques
<br>`13:52` so this is a fashion data set called
<br>`13:55` fashion mnist
<br>`13:56` provided by zalando research and
<br>`14:01` again you can uh these these images are
<br>`14:04` on a 28 by 28 letters
<br>`14:06` uh in a gray scale so you can record the
<br>`14:10` intensity of each pixel and you end up
<br>`14:12` with having 784 pixels on
<br>`14:14` of 60 000 pictures and there's different
<br>`14:17` kinds of pictures
<br>`14:18` like there's uh shirts and tops and
<br>`14:21` trousers
<br>`14:22` and there's also shoes i think in there
<br>`14:24` and then you can do a dimensionality
<br>`14:26` reduction and here
<br>`14:29` this is an example for a umap a uniform
<br>`14:32` manifold approximation i'll explain
<br>`14:34` later what this is it's a non-linear
<br>`14:36` dimensionality reduction technique
<br>`14:38` and again you can see a number of things
<br>`14:41` um
<br>`14:42` by just taking this as as vectors right
<br>`14:45` and
<br>`14:45` projecting them in two dimensions you
<br>`14:47` see that uh for instance
<br>`14:50` um i think this up here which is
<br>`14:51` trousers forms one cluster
<br>`14:54` which is very different for instance
<br>`14:56` from a cluster which consists of
<br>`14:59` sandals and sneakers and
<br>`15:02` ankle boots so this is the kind of shoes
<br>`15:04` cluster
<br>`15:05` uh you have bags here which seem to have
<br>`15:07` some similarity to
<br>`15:09` tops at some point in a certain way
<br>`15:13` so um this is a again dimensionality
<br>`15:16` reduction right and
<br>`15:18` you can see how you can how you can use
<br>`15:20` it to group together different kinds of
<br>`15:22` things in in this case just pictures uh
<br>`15:25` what you also see
<br>`15:26` here is that these things cluster so
<br>`15:28` there's a discrete kind of order
<br>`15:32` and i'll talk about clustering also
<br>`15:35` again
<br>`15:35` in the second part of the lecture
<br>`15:38` um so the now i'll go into
<br>`15:42` dimensionality reduction
<br>`15:44` and how it works and i'll start with a
<br>`15:46` linear dimensionality reduction
<br>`15:48` there's a number so so this is just the
<br>`15:50` linear transformation of your data
<br>`15:52` there's a number of techniques around um
<br>`15:55` for instance principle component
<br>`15:57` analysis i'll explain this and there's
<br>`15:59` other
<br>`15:59` uh techniques like uh non-negative
<br>`16:02` metrics factorization or independent
<br>`16:04` component analysis
<br>`16:06` or factor analysis they are they are
<br>`16:09` kind of similar in that they are linear
<br>`16:12` but i only have time to cover one of
<br>`16:14` them which is the easiest one which is
<br>`16:15` pca
<br>`16:17` um for that i'll again
<br>`16:21` share my ipad
<br>`16:41` all right what's principal component
<br>`16:42` analysis i'll first sketch the idea
<br>`16:47` um so for the i for forgetting the idea
<br>`16:50` it's sufficient to go into two
<br>`16:51` dimensions and i'll
<br>`16:53` make a plot a scatter plot of
<br>`16:56` two-dimensional data
<br>`16:58` where let's assume our data looks a bit
<br>`17:02` like this
<br>`17:06` all right it's essentially very well
<br>`17:08` correlated and
<br>`17:09` from looking at this now if you would uh
<br>`17:12` give me
<br>`17:12` x1 right and i would know x1 i could
<br>`17:16` very well predict x2 because i
<br>`17:18` i see that these two observables are
<br>`17:21` very well correlated and then
<br>`17:23` pca is a way to formalize
<br>`17:26` this and the first principle component
<br>`17:28` is designed in a way that it points in
<br>`17:30` the direction
<br>`17:32` of highest variability of the data and
<br>`17:35` in this example this would be this
<br>`17:36` direction
<br>`17:38` and this would be principal component
<br>`17:40` one and then the next principal
<br>`17:41` component
<br>`17:42` has to be orthogonal to the uh to pc1
<br>`17:46` and again point in the direction of uh
<br>`17:48` maximum variability of the data and
<br>`17:50` there's only one direction left here
<br>`17:52` which is
<br>`17:53` uh the orthogonal direction here and
<br>`17:54` that's pc2 principle component two
<br>`17:58` so then you just change the bases of
<br>`18:00` your data
<br>`18:03` through the directions of the principal
<br>`18:05` components
<br>`18:06` and then you end up with your
<br>`18:08` representation of your data
<br>`18:13` like this
<br>`18:19` where now in this directions your data
<br>`18:21` would be uncorrelated
<br>`18:24` and you would have
<br>`18:27` most of the variability in this
<br>`18:29` direction right
<br>`18:32` so the aim will be
<br>`18:38` to find a transformation
<br>`18:50` such that the components are
<br>`18:54` uncorrelated
<br>`19:03` and that and that they are ordered
<br>`19:08` by the explained variability
<br>`19:28` now how does the math of this look like
<br>`19:36` sorry
<br>`19:50` mathematically we would start with
<br>`19:53` a cr with an eigen decomposition of the
<br>`19:56` covariance matrix
<br>`19:58` um the
<br>`20:01` covariance matrix is an object which we
<br>`20:03` get from
<br>`20:04` or at least this is proportional to this
<br>`20:07` object it's the
<br>`20:08` data matrix transformed times the data
<br>`20:11` matrix itself
<br>`20:13` and you will see that this is um
<br>`20:16` a matrix of the shape m by m so it has
<br>`20:19` the dimensionality of
<br>`20:21` our data and
<br>`20:24` if you if you do the computations you
<br>`20:27` will see that the
<br>`20:28` diagonal elements of these objects are
<br>`20:31` proportional to the variability of our
<br>`20:33` data in this direction and the
<br>`20:35` off-diagonal elements
<br>`20:37` are proportional to the covariance of
<br>`20:39` components and then we do an item
<br>`20:46` decomposition
<br>`20:50` and from this we get m eigenvectors
<br>`20:53` lambda
<br>`20:53` i am eigenvalues lambda and a
<br>`20:57` and m i vectors and i group them
<br>`20:59` together in a matrix w
<br>`21:02` so the columns
<br>`21:07` of this matrix are eigenvectors
<br>`21:14` of the covariance matrix and importantly
<br>`21:18` what we do
<br>`21:19` here and we can always do this is we
<br>`21:21` sort them by the
<br>`21:23` we sort them by the magnitude
<br>`21:29` of the eigenvalues lambda i
<br>`21:33` and this ensures that the first
<br>`21:34` principal component points in the
<br>`21:35` direction of highest variability
<br>`21:38` now w is just the new uh
<br>`21:42` basis for our data and then we can
<br>`21:44` transform our data
<br>`21:47` so like this the the transformed data
<br>`21:51` will look like this we take the data
<br>`21:52` matrix
<br>`21:53` x times w
<br>`21:56` um so in the language of principal
<br>`21:58` components this is what's called
<br>`22:00` loadings
<br>`22:04` or also the rotation
<br>`22:09` and this the transformed data is called
<br>`22:11` scores
<br>`22:20` now i leave it to you as an exercise to
<br>`22:22` show that
<br>`22:24` the transformed data matrix
<br>`22:28` is a dynamic is a diagonal matrix
<br>`22:33` which basically means in this transform
<br>`22:36` space the components are uncorrelated
<br>`22:39` now the data matrix again here is of
<br>`22:43` shape
<br>`22:43` n by m
<br>`22:47` so the dimensionality of this
<br>`22:50` is just the same as the dimensionality
<br>`22:53` of our original data so how does this
<br>`22:56` help in reducing the dimensions
<br>`22:58` well there the idea is because the
<br>`23:00` eigenvectors are sorted
<br>`23:03` by the magnitude of lambda i that we can
<br>`23:05` truncate it
<br>`23:07` and if we define wr
<br>`23:11` which is an n by r matrix as the
<br>`23:16` first r columns of w
<br>`23:24` then we can get a a projection in lower
<br>`23:28` dimensions of our data
<br>`23:30` just by using rw
<br>`23:34` at wr
<br>`23:39` and this will this object will be of
<br>`23:40` shape n by r
<br>`23:42` and if we for instance select r equals
<br>`23:44` two we have a two dimensional
<br>`23:46` representation of our data of course
<br>`23:47` this
<br>`23:48` throws away some information but most of
<br>`23:50` the variability of our data is captured
<br>`23:59` um yes so so the take home is that that
<br>`24:03` is that principle component
<br>`24:07` analysis is a linear transformation of
<br>`24:09` the data such that the components
<br>`24:11` are uncorrelated and ordered by the
<br>`24:13` amount of explained variability
<br>`24:16` and what i want to do next is i want to
<br>`24:20` show you how you can actually do this
<br>`24:22` in r which is uh quite easy and you
<br>`24:25` don't actually need to know the math for
<br>`24:26` this
<br>`24:28` um so let me
<br>`24:31` um excuse me yes uh could you
<br>`24:34` repeat how do we decide uh at what
<br>`24:39` at which point to truncate w and what
<br>`24:42` exactly do we mean by sorting my
<br>`24:43` magnitude of the eigenvalues lambda
<br>`24:47` okay um if you
<br>`24:54` uh this this is the
<br>`24:58` covariance matrix right so essentially
<br>`25:00` if i
<br>`25:01` if i look at this um i saw you didn't
<br>`25:05` do you see my mouse yes yes
<br>`25:08` um so lambda 1
<br>`25:11` will be proportional to the variability
<br>`25:13` in this direction
<br>`25:14` okay yes and lambda 2 to the variability
<br>`25:18` in this direction
<br>`25:21` okay and and so this
<br>`25:24` sorting by uh
<br>`25:28` by the eigenvalues ensures that the
<br>`25:31` first component
<br>`25:32` of the first principal component will
<br>`25:35` point in this direction of highest
<br>`25:36` variability of the data
<br>`25:38` right yes
<br>`25:42` um so this is what the what the sorting
<br>`25:45` means
<br>`25:47` uh okay so in this case lambda 1 is
<br>`25:51` that the reference that we sort through
<br>`25:54` that we get w
<br>`25:55` from because lambda 1 is proportional to
<br>`25:57` the pc
<br>`25:58` one direction um
<br>`26:00` [Music]
<br>`26:02` lambda lambda 1 is the eigenvalue right
<br>`26:05` that corresponds to the
<br>`26:06` to the eigenvector which is in this
<br>`26:08` direction yes
<br>`26:10` yes and it is actually and if you
<br>`26:13` if you uh if you if you do kind of
<br>`26:17` um
<br>`26:17` [Music]
<br>`26:20` if you look at this at the transformed
<br>`26:22` cobra covariance matrix
<br>`26:24` right you will see that in the diagonal
<br>`26:26` elements of this you just have the uh
<br>`26:29` lambdas right so it's the that's the the
<br>`26:32` variable the variance in this direction
<br>`26:35` okay
<br>`26:36` yes thank you exactly so
<br>`26:39` was this all i think i remember
<br>`26:42` there was another question uh you also
<br>`26:44` asked how to drink it how to decide
<br>`26:46` uh uh where we trunk it
<br>`26:50` um this is not
<br>`26:53` this is up to us um you can kind of you
<br>`26:57` you can
<br>`26:57` uh what you can what i will show you in
<br>`26:59` a moment is that you can decide that you
<br>`27:01` wanna
<br>`27:02` keep like uh ninety percent of the
<br>`27:05` variability of your data and this would
<br>`27:06` give you a threshold of where you
<br>`27:08` where you stop for instance but
<br>`27:11` uh this threshold again is arbitrary so
<br>`27:13` you can also just
<br>`27:15` i mean one usual decision that you do is
<br>`27:17` if you want to visualize your data you
<br>`27:18` truncate at two
<br>`27:20` because that's easy to visualize um
<br>`27:23` you might also take this as an initial
<br>`27:25` step
<br>`27:26` of dimensionality reduction to maybe
<br>`27:29` just like
<br>`27:30` going from half a million to 50 or
<br>`27:32` something and then do a non-linear
<br>`27:33` transformation
<br>`27:35` but essentially like in my everyday work
<br>`27:37` this is a uh
<br>`27:39` it's an arbitrary it's often an
<br>`27:40` arbitrary choice and yeah in the end
<br>`27:42` have to see whether it works or not
<br>`27:44` whether it's sensible
<br>`27:45` so that's a tough question and
<br>`27:48` there's also some research still on that
<br>`27:51` okay um
<br>`28:03` all right so i prepared a
<br>`28:06` um a
<br>`28:10` a document a markdown
<br>`28:13` document a notebook in our studio and i
<br>`28:15` think stefan briefly introduced our
<br>`28:17` studio to do
<br>`28:18` to you last week you can also
<br>`28:22` get the code on from this url and it's
<br>`28:25` also
<br>`28:26` by now on the on the course home
<br>`28:28` homepage
<br>`28:30` um also the code from the last lecture i
<br>`28:33` forgot to mention that it's also on
<br>`28:34` github
<br>`28:37` in the same folder yeah exactly
<br>`28:40` and then um well i wanted to show you
<br>`28:43` before is that like i i want to just
<br>`28:45` show you as an example one of these uh
<br>`28:47` famous uh uh data sets you you might
<br>`28:51` have heard of the uh it's it's a data
<br>`28:52` set where uh
<br>`28:53` botanist and statistician fisher
<br>`28:56` collected
<br>`28:56` uh flowers from a flower called iris
<br>`29:01` and there's different species iris
<br>`29:04` guinea car aristotoza iris versicolor
<br>`29:07` and these have different leaves the
<br>`29:10` petal and the sepal
<br>`29:12` and he measured the the sample length
<br>`29:14` and the sample width and the petal
<br>`29:16` length and the petal with
<br>`29:17` all these species
<br>`29:21` and it's a it's a data set that you can
<br>`29:23` easily load in in
<br>`29:24` r that's why i used it and you can it's
<br>`29:27` four dimensional so here you see the
<br>`29:29` data it's uh
<br>`29:31` the length width and length and width
<br>`29:33` for one species
<br>`29:34` and then the other species follow
<br>`29:36` somewhere in the data
<br>`29:38` and you have this four numbers
<br>`29:41` now you can try to visualize this uh in
<br>`29:44` a
<br>`29:44` for instance pair wise ghetto plots
<br>`29:47` plotting the length
<br>`29:48` of the sepal against the sample width
<br>`29:50` and so on
<br>`29:51` and here this is color coded by species
<br>`29:54` and you already see some separation
<br>`29:56` but it's hard to choose like in this
<br>`29:58` four-dimensional plot
<br>`30:00` what you actually what to actually look
<br>`30:02` at and so you can perform a principal
<br>`30:04` component analysis on this
<br>`30:06` four-dimensional data set and then r
<br>`30:08` this is just a one-liner
<br>`30:10` so the principal components analysis is
<br>`30:12` done by p or comp
<br>`30:14` and here i plug in the four-dimensional
<br>`30:17` data set
<br>`30:20` and then you get all the things out that
<br>`30:23` we just talked about you get this uh
<br>`30:25` transformation matrix w called rotation
<br>`30:28` here
<br>`30:29` um where now you see that the
<br>`30:32` the principal the direction of principle
<br>`30:34` component one in this four dimensional
<br>`30:36` space
<br>`30:37` right it's it's a vector um you see
<br>`30:40` you can look at the transformed data
<br>`30:43` um which is again four dimensional
<br>`30:46` at first um here you can
<br>`30:50` uh look at the explained uh uh
<br>`30:53` variability or explain variance
<br>`30:55` um and this is maybe for the question of
<br>`30:59` where to
<br>`31:00` cut off so that they explained
<br>`31:03` variance here you can see the cumulative
<br>`31:05` proportion of this
<br>`31:07` and with the first two principal
<br>`31:09` component you explain
<br>`31:10` 95 96 of the variability of your data
<br>`31:14` and you might say okay
<br>`31:16` that's enough with uh and in in pc4
<br>`31:19` uh you from pc3 to pc4 you hardly add
<br>`31:23` something so the fourth dimension of the
<br>`31:24` data set is probably very
<br>`31:26` it's very correlated to the first three
<br>`31:29` there's not much information left and
<br>`31:31` then this is how the data looks now
<br>`31:34` in in the direction of principal
<br>`31:35` components one and two and what you can
<br>`31:37` observe is that
<br>`31:39` uh cross principle component one that's
<br>`31:41` the main direction which kind of
<br>`31:44` um discriminates between the species
<br>`31:47` you can also see that the setoza is very
<br>`31:50` different from
<br>`31:51` versicolor and virginica and here it's
<br>`31:54` hard to actually draw a boundary
<br>`31:56` but just based on the measurements
<br>`32:01` this is what's called a scree plot and
<br>`32:03` this is just again a visualization of
<br>`32:05` the variance
<br>`32:06` explained by each principal component
<br>`32:10` now i want to also show you an another
<br>`32:13` data set
<br>`32:14` where actually principal component
<br>`32:16` analysis has a hard job
<br>`32:18` to work so this is
<br>`32:21` again an image data set where images
<br>`32:24` were collected of different objects and
<br>`32:25` they are rotated
<br>`32:27` right
<br>`32:31` and now you can again do a vector
<br>`32:34` representation of these images to a
<br>`32:35` principal component analysis and this is
<br>`32:38` what the
<br>`32:38` picture looks like and what the plot
<br>`32:41` looks like now and
<br>`32:42` and the colors now uh represent
<br>`32:45` different objects
<br>`32:46` and the dots of the same color are then
<br>`32:52` pictures of the objects at different
<br>`32:54` angles and you can see
<br>`32:56` that if you do this dimensionality
<br>`32:58` reduction you can see some structure
<br>`33:00` right but it's not really uh doesn't
<br>`33:03` really work good in discriminating the
<br>`33:05` different
<br>`33:06` objects and you would expect that maybe
<br>`33:09` you can
<br>`33:09` reveal this discrete kind of order
<br>`33:11` different kinds of objects
<br>`33:15` or that's maybe what you want by doing a
<br>`33:18` dimensionality reduction
<br>`33:23` here's another example that that i made
<br>`33:26` up
<br>`33:26` which is uh a dimensionality reduction
<br>`33:29` of a swiss roll so what's this with
<br>`33:31` actually a swiss roll with a hole so
<br>`33:33` what i did here was to say okay i
<br>`33:36` um uh randomly place
<br>`33:39` uh points on a on a two-dimensional
<br>`33:43` surface
<br>`33:43` but there's a hole in the middle and
<br>`33:45` then i wrap this up
<br>`33:47` in 3d like this um
<br>`33:50` i transform it like this okay it's
<br>`33:53` it's this role and it's it's called it's
<br>`33:56` it's a suite actually in in switzerland
<br>`33:58` that's why it's called a swiss roll and
<br>`34:00` desk you can still see this uh
<br>`34:02` this uh hole in the middle now what will
<br>`34:04` happen
<br>`34:05` if you do a principal components
<br>`34:07` analysis of this
<br>`34:10` the example is shown here and this is
<br>`34:13` the same
<br>`34:14` data shown in principle component space
<br>`34:21` actually in 3d and so
<br>`34:24` what you can see is that
<br>`34:28` not much happened right it's pretty much
<br>`34:30` the same as before
<br>`34:31` just stay the principal component and
<br>`34:34` the reason for this is
<br>`34:35` that what we do is a linear
<br>`34:38` transformation of the data right
<br>`34:40` but what i did before was to take two
<br>`34:42` dimensional data and
<br>`34:43` non-linearly
<br>`34:47` projected into 3d well use the
<br>`34:50` non-linear function
<br>`34:51` and so um projecting this back to 2d
<br>`34:54` in a way cannot work with a linear
<br>`34:58` dimensionality reduction technique and
<br>`34:59` that's why
<br>`35:02` non-linear dimensionality reduction
<br>`35:04` techniques are also very useful
<br>`35:07` so this leads me to the second part of
<br>`35:10` dimensionality reduction
<br>`35:13` which is about nonlinear dimensionality
<br>`35:15` reduction techniques and
<br>`35:17` as it's usually the case with non-linear
<br>`35:20` things
<br>`35:21` there's many of them and then actually
<br>`35:23` about one year ago
<br>`35:24` i had a look at wikipedia at the
<br>`35:28` like a list of some prominent algorithms
<br>`35:32` for dimensionality reduction and there
<br>`35:34` were 29 i'm sure now
<br>`35:36` there's more and this this doesn't claim
<br>`35:39` to be complete right so
<br>`35:41` um this makes very clear that depending
<br>`35:43` on what you want
<br>`35:44` there's different things that you can do
<br>`35:47` today i will concentrate on uniform
<br>`35:49` manifold approximation a rather
<br>`35:51` recent one introduced i think in 2018 so
<br>`35:54` three years ago
<br>`35:58` and it's used a lot in single cell
<br>`36:00` sequencing data in single cell genomics
<br>`36:03` nowadays
<br>`36:05` um so what is this
<br>`36:08` technique about so don't be scared
<br>`36:11` there's a lot of mathematics on this
<br>`36:13` page and you don't have to understand
<br>`36:15` all of that right away i won't also i
<br>`36:18` also won't have the time to fully
<br>`36:20` explain this in detail but i will give
<br>`36:22` you an intuition
<br>`36:23` of what this does uh
<br>`36:26` the basic idea is
<br>`36:30` that
<br>`36:32` [Music]
<br>`36:36` so the basic idea is that we have a
<br>`36:39` higher dimensional data set
<br>`36:41` but we hypothesize that there's a low
<br>`36:43` dimensional manifold so think of
<br>`36:45` a for means for instance there could be
<br>`36:47` a line in a two-dimensional manifold
<br>`36:50` right and then we want to discover this
<br>`36:53` dimensional
<br>`36:54` manifold so this
<br>`36:57` there's a couple of assumptions that are
<br>`36:59` made in new map one that the data is
<br>`37:01` distributed uniformly on a romanian
<br>`37:04` manifold
<br>`37:05` that the romanian metric is locally
<br>`37:07` constant and that the manifold is
<br>`37:09` locally connected
<br>`37:11` and what umap then gives you is
<br>`37:14` it models this manifold with a fuzzy
<br>`37:16` topological structure
<br>`37:18` and it finds a low dimensional
<br>`37:20` projection of the data
<br>`37:22` that has a very similar fuzzy
<br>`37:25` topological structure
<br>`37:26` to your original data so what does all
<br>`37:29` this mean

### white board 1

<br>`37:30` um let's let's start
<br>`37:33` by i will start by by introducing
<br>`37:36` briefly very briefly introducing an an
<br>`37:40` important idea from topological data
<br>`37:42` analysis because
<br>`37:43` uh this algorithm is or this idea is
<br>`37:47` heavily based on topological data
<br>`37:50` analysis and this is simplices
<br>`37:53` a zero simplex is a point one simplex is
<br>`37:56` a connection of two zeros implices which
<br>`37:58` is a line then there's a two simplex
<br>`38:00` which is a triangle
<br>`38:02` a three simplex which is a tetrahedra
<br>`38:05` and you can see that you can easily
<br>`38:07` extend this contact
<br>`38:09` con concept to higher dimensions so you
<br>`38:12` can introduce a four simplex five
<br>`38:13` simplex and so on
<br>`38:16` and these objects are rather easy
<br>`38:19` to construct and the nice thing that you
<br>`38:22` can do is you can glue together such
<br>`38:24` objects such simplices
<br>`38:26` and by gluing them together
<br>`38:30` you can basically approximate um
<br>`38:33` money folds so um you might all have
<br>`38:37` seen already some point where you
<br>`38:39` uh triangulate the surface right and
<br>`38:41` this is nothing
<br>`38:42` then uh approximating this manifold with
<br>`38:45` simplices
<br>`38:51` now let's look at this example which i
<br>`38:54` took from the umap homepage actually
<br>`38:56` where you can see points which are
<br>`38:59` uniformly sampled actually equidistantly
<br>`39:02` sampled i think
<br>`39:03` on a not equidistant but uniformly
<br>`39:06` sampled on a
<br>`39:10` on a line
<br>`39:14` in a two-dimensional space right so we
<br>`39:16` have a one-dimensional manifold
<br>`39:18` in a two-dimensional space and
<br>`39:22` uh um so this would be could be our data
<br>`39:25` points that were measured
<br>`39:26` right and we would be interested in
<br>`39:28` finding the topological
<br>`39:30` structure of this manifold um so what
<br>`39:33` has been done
<br>`39:34` here is to draw some spheres around
<br>`39:36` these dots
<br>`39:38` and the union of all these spheres i
<br>`39:40` mean all these spheres are sets
<br>`39:42` and the union of all this is what's
<br>`39:44` called an open cover
<br>`39:45` open cover is just the thing that uh is
<br>`39:49` this is a um is a collection of sets
<br>`39:52` that span the whole manifold right so
<br>`39:54` the line
<br>`39:55` that we see here is inside this open
<br>`39:57` cover
<br>`39:58` and now you can do some heavy
<br>`40:00` topological and mathematics
<br>`40:02` and you can then prove that if you now
<br>`40:05` contract
<br>`40:05` uh construct simplices by uh all
<br>`40:09` groups of sets that in that that have a
<br>`40:12` non empty intersection which in this
<br>`40:14` case basically would mean
<br>`40:15` you construct a one simplex here line
<br>`40:18` here
<br>`40:19` and one simplex here and so on you i
<br>`40:21` think you get the picture
<br>`40:23` then if you do this and this would look
<br>`40:25` like
<br>`40:26` no um then this
<br>`40:29` structure this graph-like structure that
<br>`40:32` you get out of
<br>`40:33` this captures the topology of the
<br>`40:35` manifold
<br>`40:37` the information is encoded in there and
<br>`40:38` i think in this uh
<br>`40:40` two-dimensional example this this is uh
<br>`40:44` quite intuitive that the connection of
<br>`40:46` all these points
<br>`40:51` tells you about uh tells you that this
<br>`40:54` is a connected line
<br>`40:56` and there's no loops for instance
<br>`41:01` um so that's pretty cool and now we
<br>`41:04` would like to use this concept to
<br>`41:06` uh to learn something about our high
<br>`41:09` dimensional data
<br>`41:12` is the criterion for the connection
<br>`41:14` always like the
<br>`41:15` shortest distance between the points
<br>`41:18` because i mean here i could
<br>`41:20` see it but if i have more complex
<br>`41:22` structure
<br>`41:23` exactly exactly i'm actually coming to
<br>`41:25` this point in a second in this case
<br>`41:27` it was a bit like okay let's just guess
<br>`41:30` uh the size of the sphere
<br>`41:31` make it a good guess such that it works
<br>`41:33` right but if you have high dimensional
<br>`41:35` data
<br>`41:36` what would be the size of this sphere
<br>`41:37` that would be super unclear
<br>`41:39` so um i'll come back to this question in
<br>`41:42` a moment
<br>`41:46` it's also connected to a situation with
<br>`41:48` like this
<br>`41:49` right because um
<br>`41:52` our points might not actually be
<br>`41:54` uniformly distributed
<br>`41:55` okay so um if we would do the same thing
<br>`41:59` here
<br>`42:00` drawing these circles and
<br>`42:04` uh construct the simplices out of that
<br>`42:07` we would actually get disconnected parts
<br>`42:10` okay
<br>`42:11` and this is not what we would
<br>`42:13` intuitively like to get right
<br>`42:15` because here we
<br>`42:19` we saw this line um
<br>`42:24` now and this is also this kind of breaks
<br>`42:26` the assumption
<br>`42:28` of umap which is the uniform
<br>`42:30` distribution of uh
<br>`42:32` of data points on the money fold so
<br>`42:35` how can we circumvent this or how can we
<br>`42:37` solve this problem we can
<br>`42:38` kind of turn the problem upside down and
<br>`42:41` say
<br>`42:42` no these data points are uniformly
<br>`42:46` distributed we see different distances
<br>`42:50` if we apply a constant metric so this
<br>`42:52` has to be wrong the
<br>`42:53` metric is not constant actually we
<br>`42:56` couldn't
<br>`42:57` try to construct the metric like this
<br>`42:58` and this comes back to your question
<br>`43:01` we might say that the distance in this
<br>`43:02` case to the fifth
<br>`43:04` neighbor should always on average give
<br>`43:06` us a distance of five
<br>`43:08` right such that we say um distances
<br>`43:10` between neighboring data points should
<br>`43:12` on average be one
<br>`43:15` um and this would mean that that a
<br>`43:18` distance of
<br>`43:19` five for instance for this uh data point
<br>`43:22` would be rather large
<br>`43:23` and a distance of 5 for this standard
<br>`43:26` point would be rather small
<br>`43:28` so we define
<br>`43:34` we now use nearest neighbors k nearest
<br>`43:37` neighbors
<br>`43:38` to define a local metric
<br>`43:42` and we then turn this local metric
<br>`43:47` again and i'm skipping a lot of details
<br>`43:49` which are important here into a
<br>`43:53` construction of simplices into a
<br>`43:54` construction of graphs where the
<br>`43:56` edges now are weighted and the reason
<br>`44:00` that they are weighted now is that the
<br>`44:02` uh the distances between
<br>`44:04` uh points are different and also that uh
<br>`44:06` we actually have two measures of
<br>`44:09` um of distance one
<br>`44:12` using the local metric from here to
<br>`44:15` there and one using the local metric
<br>`44:16` from here to there because they might
<br>`44:18` not be the same
<br>`44:22` um but if you properly do the math
<br>`44:25` behind all that
<br>`44:26` you can show that this construction now
<br>`44:29` um captures essential parts of the
<br>`44:32` what's now called the fuzzy topology
<br>`44:35` of this manifold okay so we have a graph
<br>`44:39` representation now
<br>`44:41` that captures a topological structure
<br>`44:44` of our of the manifold we're interested
<br>`44:47` in
<br>`44:49` um how can we do that how can we use
<br>`44:50` this now to find low dimensional
<br>`44:52` representation
<br>`44:54` well the idea is that now you start
<br>`44:57` um you have this this graph defined and
<br>`45:01` now you start
<br>`45:02` with a low dimensional representation
<br>`45:05` you just place your points randomly
<br>`45:07` basically
<br>`45:08` and then you construct a similar
<br>`45:12` graph representation of your low
<br>`45:14` dimensional representation and then you
<br>`45:15` shuffle your points around
<br>`45:17` until the the topology the graph
<br>`45:20` representations kind of match
<br>`45:26` so yes you have a graph representation
<br>`45:30` of your high dimensional
<br>`45:31` data of your low dimensional data you
<br>`45:33` interpret the edge weights
<br>`45:35` as probabilities and then you minimize
<br>`45:38` the cross
<br>`45:39` entropy given here where basically
<br>`45:42` the important thing is that you try to
<br>`45:44` match the
<br>`45:46` edge weights in your higher dimensional
<br>`45:48` representation with the edge weights and
<br>`45:50` the low dimensional representation like
<br>`45:52` when this
<br>`45:53` ratio gets one the term vanishes and the
<br>`45:57` same happens over here
<br>`46:01` now how does this work in practice like
<br>`46:05` if you want to read more about this
<br>`46:06` there's a nice home page
<br>`46:11` i just wanted to show an animation here
<br>`46:15` which is called understanding umap there
<br>`46:18` for instance here you have an example
<br>`46:20` in 3d you have um dots
<br>`46:23` which run out from a center in a star
<br>`46:26` like fashion right and that's a 3d
<br>`46:28` represent this is a three-dimensional
<br>`46:30` data
<br>`46:31` and well actually it's
<br>`46:34` 10 dimensional data in this case i think
<br>`46:37` and this is a three-dimensional
<br>`46:38` projection maybe
<br>`46:40` and now if you run umap
<br>`46:44` these dots are shuffled around randomly
<br>`46:47` and you stop
<br>`46:48` when you have a topological
<br>`46:50` representation which is very similar and
<br>`46:51` in this case this is also
<br>`46:53` this starship star-shaped pattern but
<br>`46:56` now in two dimensions
<br>`46:58` and if you want there's many more
<br>`47:00` examples here and you can
<br>`47:02` play around with this
<br>`47:09` um you can of course do the same thing
<br>`47:12` in
<br>`47:12` r um i i don't know
<br>`47:16` like i know this was a lot of
<br>`47:18` information and i've
<br>`47:19` i didn't go into the details are there
<br>`47:21` questions about umap at this point
<br>`47:28` otherwise i just show you how to do this
<br>`47:31` in r
<br>`47:35` it's essentially again a one-liner
<br>`47:38` where you have a function umap and what
<br>`47:41` i feed in here
<br>`47:43` is the swiss roll that i created
<br>`47:45` previously
<br>`47:47` okay and then um
<br>`47:50` i just i i do the um
<br>`47:54` dimensionality reduction here with a one
<br>`47:56` liner
<br>`47:57` then i convert the whole thing in a data
<br>`47:59` table object
<br>`48:00` to uh to have a nice plotting
<br>`48:03` and this is what the result looks like
<br>`48:05` now a new map coordinate
<br>`48:08` the the swiss role was kind of unrolled
<br>`48:11` but it
<br>`48:12` heavily lost its shape but what you can
<br>`48:15` see is that the topology is preserved
<br>`48:17` right
<br>`48:18` um so so the hole in the center is still
<br>`48:21` there
<br>`48:25` um i also want to show you a review map
<br>`48:29` representation of the coil 20 data that
<br>`48:31` i showed you above so remember this was
<br>`48:33` the data set
<br>`48:36` where we had pictures which are rotated
<br>`48:42` and where the the pca didn't look very
<br>`48:46` informative
<br>`48:48` now if we do the same thing with a umap
<br>`48:50` and we feed in these pictures this is
<br>`48:52` what we get
<br>`48:54` so most of the images nicely separate
<br>`48:57` right different colors mean different
<br>`48:59` objects
<br>`49:01` they nicely separate and what the umab
<br>`49:03` also gives us
<br>`49:04` is this kind is is the topology of this
<br>`49:07` data in the sense of that we can see
<br>`49:09` that this is a rotation
<br>`49:10` right so neighboring
<br>`49:14` pictures are similar and you
<br>`49:18` rotate the object until you come back to
<br>`49:20` the other side
<br>`49:27` okay i think yes that's it for um
<br>`49:30` [Music]
<br>`49:31` dimensionality reduction just one
<br>`49:35` example
<br>`49:36` for linear dimensionality reduction
<br>`49:37` which was printable components
<br>`49:39` and one for non-linear topology
<br>`49:42` preserving dimensionality reduction
<br>`49:44` which was umap and i now wanted to talk
<br>`49:47` a little bit about clustering
<br>`49:50` um so
<br>`49:53` you can as you already saw in some of
<br>`49:56` the
<br>`49:56` reduced dimensionality in in the some of
<br>`49:59` the
<br>`50:00` representations of the data and reduced
<br>`50:01` dimensions uh clusters can appear in
<br>`50:04` your data which
<br>`50:05` essentially mean you have qualitatively
<br>`50:08` different
<br>`50:09` objects in your data different different
<br>`50:11` samples and
<br>`50:15` you sometimes you you
<br>`50:18` and and it's good to have a way to group
<br>`50:22` different kinds of different classes of
<br>`50:24` objects together
<br>`50:26` and clustering is nothing
<br>`50:29` which is um there is no one definition
<br>`50:33` of clustering
<br>`50:34` the idea is to find clusters such that
<br>`50:37` the data within clusters are similar
<br>`50:40` while data from different clusters are
<br>`50:42` dissimilar
<br>`50:43` but what you define a similarity or
<br>`50:46` dissimilarity that's
<br>`50:48` basically up to you and so a lot of
<br>`50:50` different clustering algorithms exist
<br>`50:54` and i just wanted to introduce three of
<br>`50:56` them today
<br>`50:58` um and you use this a lot in or at least
<br>`51:01` i use this a lot in trying to understand
<br>`51:03` high dimensional data
<br>`51:05` i'm just going to share my
<br>`51:10` ipad again
<br>`51:27` and i wanted to show you first i want to
<br>`51:29` give you three examples and the first
<br>`51:30` one would be hierarchical clustering
<br>`51:32` which you
<br>`51:33` which uh
<br>`51:36` we're here i just plotted some
<br>`51:40` some data in two-dimensional space to
<br>`51:42` illustrate the concept of clustering
<br>`51:44` and what you need for hierarchical
<br>`51:47` clustering
<br>`51:48` is first of all a metric
<br>`51:54` which defines distance between your
<br>`51:57` objects
<br>`51:57` that you have here and this could just
<br>`52:00` be for instance the euclidean metric or
<br>`52:02` manhattan metric or a correlation
<br>`52:04` metric you're basically free to choose
<br>`52:06` and then what you do
<br>`52:08` is you um you group together
<br>`52:12` the two objects which are closest
<br>`52:15` together biometrics so with the
<br>`52:16` euclidean metric for this example
<br>`52:18` this would be those two guys right
<br>`52:30` so
<br>`52:35` what you then create is a kind of tree
<br>`52:37` where where um
<br>`52:39` okay we say i said we grow group
<br>`52:41` together those two guys so that's the
<br>`52:42` first thing to do
<br>`52:48` um and now next we need another thing
<br>`52:52` which is called the linkage criterion
<br>`53:03` um and this tells you how to now treat
<br>`53:06` these clusters because
<br>`53:08` uh now you need a way to uh
<br>`53:11` to give get the distance between the
<br>`53:14` clusters
<br>`53:21` and this could for instance be the
<br>`53:23` minimum distance
<br>`53:27` so this would mean if you want to now
<br>`53:29` get the
<br>`53:30` the distance between uh this cluster
<br>`53:33` and uh this object you would
<br>`53:36` take the distance between b and d and c
<br>`53:39` and d
<br>`53:39` and take the minimum distance or you
<br>`53:43` could also
<br>`53:44` for instance use the centroid there's
<br>`53:46` many of the clusters there's many
<br>`53:48` choices right
<br>`53:51` um now if we kind of go on we maybe take
<br>`53:54` the centroid here then the next cluster
<br>`53:56` would probably be a grouping of d
<br>`54:00` and e
<br>`54:06` then i'd say i would add
<br>`54:09` those three in one cluster
<br>`54:18` then group all these b c d
<br>`54:21` e and f until finally we arrive
<br>`54:25` at one at an object which
<br>`54:29` contains all the elements
<br>`54:35` and now if we want to define clusters in
<br>`54:38` our data we
<br>`54:39` need to define a precision threshold
<br>`54:42` along this axis
<br>`54:46` and we could for instance put it here
<br>`54:53` um and then
<br>`55:01` this would cut the tree in this
<br>`55:05` in in separate subtrees and we would
<br>`55:08` have a
<br>`55:08` subtree here that's up three here and
<br>`55:11` it's up to here and then this would be
<br>`55:12` our three different clusters so we would
<br>`55:14` have a cluster one
<br>`55:15` cluster two and a cluster three and if
<br>`55:18` we uh
<br>`55:20` increase the precision like up here then
<br>`55:22` we would get more and more clusters
<br>`55:28` and as this basically
<br>`55:31` just needs some uh
<br>`55:34` distance computations um it's it's this
<br>`55:37` is rather easily done in in
<br>`55:39` uh also in higher dimension i don't know
<br>`55:46` um
<br>`55:48` next i wanted to show you
<br>`55:58` um another important one which is a
<br>`56:02` centroid-based clustering called k-means
<br>`56:04` clustering and you
<br>`56:07` one comes across this quite often as
<br>`56:09` well when working with high-dimensional
<br>`56:10` data
<br>`56:11` so here in this case
<br>`56:17` um you pre-specify the number of
<br>`56:19` clusters k
<br>`56:20` so that's what you have to start with
<br>`56:23` how many clusters do you want to get
<br>`56:26` you might try out different case in
<br>`56:28` practice
<br>`56:29` and then you partition your data such
<br>`56:31` that the square distance to the cluster
<br>`56:34` mean position so that that would be the
<br>`56:37` centroid is minimal
<br>`56:41` um so how would this look like
<br>`56:45` um actually maybe let's look at the
<br>`56:49` final result
<br>`56:50` first we're kind of uh here you see an
<br>`56:53` algorithm converging but what you try to
<br>`56:55` do is to
<br>`56:55` talk to do a grouping of the data such
<br>`56:59` that oh no it doesn't stop there
<br>`57:06` sorry so so how do you how do you get
<br>`57:08` this partitioning of your data
<br>`57:11` one way would be the lloyd algorithm you
<br>`57:13` start with random centers that you place
<br>`57:15` somewhere so in this case
<br>`57:17` this is an example taking from wikipedia
<br>`57:20` there's a center here a center there in
<br>`57:22` the center there and then
<br>`57:23` for each of your data points you assign
<br>`57:26` the data point to the cluster
<br>`57:28` where the center is nearest right so the
<br>`57:30` yellow center is here so everything here
<br>`57:32` would be assigned to the yellow
<br>`57:34` cluster now once you did this you
<br>`57:39` update the centers of your clusters
<br>`57:42` now you take the centroid of this yellow
<br>`57:45` cluster for instance
<br>`57:46` and the yellow center ends up here
<br>`57:50` and now you do a new assignment of your
<br>`57:54` data points to the nearest center in
<br>`57:57` this case all the
<br>`57:58` yellow ones up here would be assigned to
<br>`58:01` the blue center actually
<br>`58:03` so they are assigned to the blue and
<br>`58:04` then you iteratively go on and do this
<br>`58:07` go on and go and go on until this
<br>`58:10` algorithm converges and you end up
<br>`58:12` having three clusters defined by this
<br>`58:16` criterion of course there's other more
<br>`58:17` complicated more sophisticated
<br>`58:19` algorithms but this approximates the
<br>`58:20` solution
<br>`58:27` a third algorithm that i wanted to show
<br>`58:29` you and i want to show you this because
<br>`58:31` i
<br>`58:31` work with it every day comes from social
<br>`58:34` systems which is a graph based
<br>`58:36` clustering
<br>`58:38` when you start with your high
<br>`58:39` dimensional data you first need a graph
<br>`58:41` representation of your data and we
<br>`58:43` already saw this in you
<br>`58:44` in the u-map example you could for
<br>`58:47` instance
<br>`58:48` do a k-nearest neighbor network on your
<br>`58:50` data and then
<br>`58:51` you partition your data such that the
<br>`58:53` modularity
<br>`58:54` queue is optimized um
<br>`58:59` modularity in this case is defined as
<br>`59:02` this object where where e i j are the
<br>`59:05` fraction of
<br>`59:06` links between cluster i and j
<br>`59:09` right and what you try to do then in
<br>`59:12` this object is that
<br>`59:14` the links between
<br>`59:17` cluster i and i which is the internal
<br>`59:19` links this
<br>`59:20` it's this eii right this is it's the
<br>`59:22` links inside the cluster
<br>`59:24` you try to maximize this
<br>`59:27` and uh you in in this ai term you have
<br>`59:30` the
<br>`59:30` ij from i to another cluster
<br>`59:34` so this is links out out of the cluster
<br>`59:36` you minimize this right so you have
<br>`59:38` very
<br>`59:42` clusters means a cluster in this case
<br>`59:45` means that it's
<br>`59:46` it's a
<br>`59:49` parts of your graph which are densely
<br>`59:51` connected inside but only sparsely
<br>`59:53` connected to the outside
<br>`59:56` there's a particular algorithm which is
<br>`59:59` used a lot nowadays which is the longer
<br>`60:01` algorithm so how do you solve this
<br>`60:03` because this is not
<br>`60:05` uh you can't so if this brute force
<br>`60:08` um you start with a network like this
<br>`60:12` for instance uh this would be your
<br>`60:15` nearest neighbor graph that you created
<br>`60:17` from your data and then you do copy
<br>`60:18` attempts you
<br>`60:19` start with node zero so all these now
<br>`60:23` you start with all these being separate
<br>`60:25` clusters
<br>`60:26` and then you copy cluster identity zero
<br>`60:29` to neighboring nodes
<br>`60:30` and you again compute the modularity and
<br>`60:32` if the modularity is increased you
<br>`60:34` accept this copy step
<br>`60:36` and if it's decreased you uh you reject
<br>`60:39` the copy step and you
<br>`60:40` do so um until you arrive
<br>`60:45` at a steady state like this where copy
<br>`60:47` attempts
<br>`60:49` don't increase your modularity anymore
<br>`60:52` would be in this case something like
<br>`60:54` that where you end up with four clusters
<br>`60:56` and then you do an aggregation and this
<br>`60:59` means
<br>`61:00` now that you
<br>`61:03` define a new graph representation of
<br>`61:05` your data where this
<br>`61:07` cluster here the blue cluster is now a
<br>`61:09` single node
<br>`61:12` it gets four internal connections
<br>`61:14` because there's
<br>`61:15` one two three four internal connections
<br>`61:19` and there is
<br>`61:20` four connections to cluster green
<br>`61:24` one two three four
<br>`61:28` and one connection to the light blue
<br>`61:30` cluster
<br>`61:31` and so you aggregate this you do the
<br>`61:33` copy attempt again
<br>`61:35` and so on and so on until you finally
<br>`61:38` arrive at a picture where you
<br>`61:40` where you um at a state where
<br>`61:44` you can't optimize modularity anymore
<br>`61:46` and this is um
<br>`61:48` how you this is how the algorithm works
<br>`61:50` to solve the problem
<br>`61:52` of modularity optimization and this
<br>`61:54` algorithm
<br>`61:56` works very well with many kinds of data
<br>`61:58` again for instance it's
<br>`62:00` used a lot to identify
<br>`62:03` cell types in a single cell genomics
<br>`62:12` all right that's it already i realize
<br>`62:14` i've been
<br>`62:15` quite fast we would have some time but
<br>`62:19` i'm i'm sorry
<br>`62:22` good timing one hour um
<br>`62:27` so just as a summary um the question
<br>`62:30` i wanted to talk about is how do you
<br>`62:32` explore high dimensional data
<br>`62:34` to identify order in this high
<br>`62:36` dimensional data set and i showed you
<br>`62:39` a couple of dimensionality reduction
<br>`62:41` techniques to visualize your
<br>`62:42` in-dimensional data
<br>`62:44` and that allow you to identify a small
<br>`62:46` set of
<br>`62:47` observables to describe the data um
<br>`62:51` i showed you a couple of approaches for
<br>`62:53` clustering to this
<br>`62:54` to identify discrete order in high
<br>`62:56` dimensional data and
<br>`62:58` i think one important point that i want
<br>`63:00` to make is the methods to use to work
<br>`63:03` with high dimensional data
<br>`63:05` depend on the problem at hand so really
<br>`63:08` depends on what you're looking for and
<br>`63:09` often it's just
<br>`63:10` trying out a lot of things to see what
<br>`63:12` makes sense
<br>`63:14` to understand your data and with this um
<br>`63:17` i'm at the end and
<br>`63:20` there's some references in the back
<br>`63:22` which i will upload uh
<br>`63:24` with the slides and with this yes i'm
<br>`63:26` i'm happy to take questions
<br>`63:29` okay perfect uh thanks a lot fabian yeah
<br>`63:32` thanks for taking the time and
<br>`63:35` especially since
<br>`63:36` uh data people like you are so in such
<br>`63:39` high demand these days and very busy so
<br>`63:41` it's great that you took the time to
<br>`63:43` to show us some of your stuff and
<br>`63:46` so uh i think what we usually do is that
<br>`63:49` we hang around a little bit
<br>`63:51` yeah on zoom and then if you have any
<br>`63:53` questions you just stay online
<br>`63:56` and ask your questions
<br>`63:59` yeah and uh other than uh that
<br>`64:02` yeah so then see you all next week and
<br>`64:05` there's already a question in the chat
<br>`64:13` there were questions in the chat during
<br>`64:15` the year during the lecture and i didn't
<br>`64:16` see the chat so yes you can't see that
<br>`64:18` very well if you're sharing the screen
<br>`64:20` yes but i think they were answered
<br>`64:22` already by other people
<br>`64:24` so so now the latest question is how
<br>`64:26` computationally intensive is um
<br>`64:29` that's that's a good question and it's
<br>`64:31` actually that's another uh
<br>`64:33` advantage of umap it's pretty fast
<br>`64:38` um it's
<br>`64:40` it also it's you don't you don't need a
<br>`64:42` lot of memory
<br>`64:43` um it scales very well with the
<br>`64:46` dimension of your data and also the
<br>`64:47` amount of data points so i think
<br>`64:49` it's it's um i mean just like
<br>`64:56` it's one of the fastest things around at
<br>`64:58` the moment um
<br>`65:01` i mean if you look at the typical data
<br>`65:02` sets uh that that you're looking at
<br>`65:05` where you have i mean 15 thousand
<br>`65:07` dimensions
<br>`65:08` and then maybe a few hundred thousand or
<br>`65:11` ten thousands of uh samples yeah you you
<br>`65:14` end up
<br>`65:15` with a few seconds yes yes on my machine
<br>`65:18` like the with the largest data sets i
<br>`65:20` have which are
<br>`65:21` of the order that you described um it
<br>`65:24` takes about
<br>`65:25` 30 seconds maybe to compute the uh
<br>`65:29` compute the u map which is much faster
<br>`65:32` for instance there's
<br>`65:33` this name i don't know whether you know
<br>`65:36` about it but this was used a lot before
<br>`65:38` and
<br>`65:38` this is much slower usually
<br>`65:41` and actually there's um i didn't try
<br>`65:44` this out but there's also gpu
<br>`65:46` of implementations of umap nowadays and
<br>`65:48` this again
<br>`65:50` you can easily you can nicely
<br>`65:51` parallelize it and so this should be
<br>`65:53` much faster again
<br>`65:59` you're welcome
<br>`66:04` great thanks so are there any other
<br>`66:07` questions
<br>`66:08` um i have a question it's from
<br>`66:12` umap
<br>`66:15` so when we uh in all the examples of
<br>`66:18` umap we saw approximating a high
<br>`66:20` dimensional data
<br>`66:21` is there any isn't there any parameter
<br>`66:23` in the algorithm that quantifies
<br>`66:25` the uh
<br>`66:28` the acceptability of the approximation
<br>`66:30` whether the approximation is cur
<br>`66:32` how how much is it acceptable or not
<br>`66:34` because
<br>`66:35` or will it approximate any uh high
<br>`66:37` dimensional data
<br>`66:40` there didn't seem to be any parameter
<br>`66:41` that quantified or helped us to
<br>`66:44` understand if the result of the umap
<br>`66:47` approximation is
<br>`66:48` good or not uh obviously concerning the
<br>`66:51` problem at hand
<br>`66:53` i'm not fully sure whether i completely
<br>`66:56` understand the question but here are a
<br>`66:57` few thoughts on this um
<br>`67:02` so the approximation in umap is that you
<br>`67:05` you approximate
<br>`67:07` that um
<br>`67:10` your your approximation is that the data
<br>`67:12` is uniformly distributed
<br>`67:14` on the manifold right and the question
<br>`67:17` is
<br>`67:18` and maybe the question is is this a good
<br>`67:19` approximation or is it not a good
<br>`67:21` approximation
<br>`67:22` the problem is that we that we hardly
<br>`67:25` know the real metric
<br>`67:27` of the underlying space so
<br>`67:30` if you for instance think of these
<br>`67:33` examples with
<br>`67:34` pictures right what is a distance
<br>`67:36` between two pictures
<br>`67:37` what is this metric um
<br>`67:41` it's it's um i i think this is the you
<br>`67:45` you can't actually like
<br>`67:46` unless you have a unless you have a good
<br>`67:49` microscopic model
<br>`67:50` which in this case we don't have it's uh
<br>`67:53` not really possible to
<br>`67:55` to define a good metric and therefore to
<br>`67:58` judge whether whether the
<br>`68:00` whether the approximation is a good one
<br>`68:02` or not
<br>`68:04` um it's not
<br>`68:08` um yes i mean the way here that you you
<br>`68:12` do it is
<br>`68:13` there's no there's no uh right rigorous
<br>`68:16` way of doing that and that's why people
<br>`68:17` like fabian exist
<br>`68:18` who have experience and have consistency
<br>`68:21` checks
<br>`68:23` that with some experience can check
<br>`68:25` whether you map
<br>`68:26` makes sense or not yeah or whether it's
<br>`68:29` so one of the standard problem is that a
<br>`68:31` umap can be dominated by noise by
<br>`68:33` technical artifacts for example
<br>`68:35` yeah and then you need to have some
<br>`68:37` insights into data and some experience
<br>`68:40` that tell you whether uh whether uh
<br>`68:43` uh what you see actually represents
<br>`68:46` something that's real in the data
<br>`68:48` or whether that's something just just an
<br>`68:50` artifact you know so that's
<br>`68:52` uh that's basically one of the the jobs
<br>`68:55` that bioinformaticians or data science
<br>`68:58` scientists do
<br>`68:59` because there's just no rigorous way
<br>`69:02` where you just push a button and it
<br>`69:03` tells you whether
<br>`69:04` whether what you've done is is right or
<br>`69:06` not so
<br>`69:07` it needs some experience and some some
<br>`69:09` insights and understanding
<br>`69:11` of the data and the for example the ball
<br>`69:14` biology
<br>`69:15` uh that is underlying the the data
<br>`69:18` so typically with the typical um
<br>`69:22` method would be to use multiple
<br>`69:24` reduction methods and see which one is
<br>`69:26` giving us
<br>`69:27` an order which is much more perceptible
<br>`69:29` in our in our plots
<br>`69:31` you know i guess mean you also have to
<br>`69:34` to know the strengths and weaknesses of
<br>`69:36` each method
<br>`69:38` yeah for example what uh fabian told
<br>`69:41` about
<br>`69:41` previous uh before t-sne that had a
<br>`69:45` tendency
<br>`69:45` uh to perform to to give you clusters of
<br>`69:49` data points
<br>`69:50` yeah it was not very good at
<br>`69:52` representing global structures of data
<br>`69:54` sets
<br>`69:55` yeah and once you know that you can
<br>`69:57` interpret
<br>`69:58` interpret what you see and then you can
<br>`70:00` be careful
<br>`70:01` in interpreting uh basically clusters as
<br>`70:05` real physical or biological objects
<br>`70:09` yeah you maps the you are what you what
<br>`70:12` you've seen now
<br>`70:12` that overcame this limitation that it's
<br>`70:15` basically
<br>`70:16` also represented the global structure of
<br>`70:18` data quite well
<br>`70:20` but i guess also in umab you can have
<br>`70:22` artifacts
<br>`70:23` especially if your data has noise yeah
<br>`70:25` technical noise
<br>`70:27` you can have very weird artifacts so you
<br>`70:30` need to treat the data
<br>`70:32` before you can give it to youmap in in
<br>`70:34` typical instances
<br>`70:36` yeah so for example log you have to log
<br>`70:38` transform data very often
<br>`70:40` if your data is says spends huge orders
<br>`70:44` of magnitude
<br>`70:46` in quant in in in values yeah then then
<br>`70:49` sometimes you have the log
<br>`70:50` transformations for not the
<br>`70:52` the very few very large data points to
<br>`70:54` dominate everything
<br>`70:57` and so you have to treat the data in a
<br>`70:59` way to make it
<br>`71:00` say digestible for these methods
<br>`71:04` but then maybe i mean
<br>`71:07` the the other part of the question was
<br>`71:09` in in a way parameters and i didn't talk
<br>`71:10` about parameters at all and there are a
<br>`71:12` couple of parameters in the algorithm
<br>`71:14` um and i i skipped a lot of details but
<br>`71:17` the most important parameter
<br>`71:19` is the number of neighbors you look at
<br>`71:22` in your
<br>`71:24` when you construct the graph if you take
<br>`71:26` the first neighbor right you you
<br>`71:28` kind of um what you do is you
<br>`71:32` um estimate your metric very locally
<br>`71:36` um so so this is very this is very fine
<br>`71:38` but it's also very noisy so you often
<br>`71:40` will estimate the wrong metric if you
<br>`71:42` if you uh increase the number of
<br>`71:45` neighbors in there
<br>`71:46` um you will get a more robust estimate
<br>`71:50` of the local metric but you will
<br>`71:52` miss some fine structure of the data and
<br>`71:54` maybe actually there's a there's one
<br>`71:55` example that i can show
<br>`71:57` uh from here where if you look at
<br>`72:01` i don't know whether you can see this
<br>`72:02` here this is a
<br>`72:04` um maybe you can can you see this or is
<br>`72:07` this too small
<br>`72:08` i'm sorry you're not sharing the screen
<br>`72:12` ah sorry i don't share the screen so you
<br>`72:14` can't see anything
<br>`72:16` um let me show
<br>`72:18` [Music]
<br>`72:20` let me show this example um
<br>`72:22` [Music]
<br>`72:27` kind of if you that's maybe maybe a
<br>`72:32` actually a good example for for your
<br>`72:33` question where kind of okay here we have
<br>`72:35` a circle
<br>`72:37` with uh with dots and they on um
<br>`72:41` and then like like the distance between
<br>`72:43` the dots is not always the same right
<br>`72:46` um and so actually if we
<br>`72:49` take just this example and we say okay
<br>`72:51` here we know the euclidean metric
<br>`72:54` uh we can think of how how well does the
<br>`72:56` approximation now
<br>`72:58` or or how does umap behave if um
<br>`73:03` uh in this case right and
<br>`73:06` one thing that you can see here is that
<br>`73:08` if i increase the number of neighbors
<br>`73:13` that this will
<br>`73:16` usually lead to a
<br>`73:19` actually not
<br>`73:25` so you can see that sometimes you manage
<br>`73:28` to
<br>`73:28` for for some uh there is kind of an
<br>`73:31` optimum
<br>`73:33` um for looking at the number of
<br>`73:35` neighbors which allows you to actually
<br>`73:37` capture
<br>`73:39` um the the
<br>`73:42` circular topology the hole in the middle
<br>`73:44` right but
<br>`73:46` if you if like if you go too big you'd
<br>`73:48` kind of lose
<br>`73:49` to start to lose the information about
<br>`73:52` the order of these dots
<br>`73:54` of these uh measurements right they
<br>`73:57` start to get more and more noisy
<br>`73:59` if you look at less neighbors
<br>`74:03` you get nice ordered lines but you start
<br>`74:06` to miss
<br>`74:08` things where you have these gaps and you
<br>`74:10` start to create clusters
<br>`74:11` where there shouldn't be clusters so
<br>`74:14` this is the
<br>`74:15` most important
<br>`74:17` [Music]
<br>`74:19` parameter of the of the method
<br>`74:22` i'd say there is like if you if you uh
<br>`74:27` the umap home page the like from the
<br>`74:29` umap algorithm
<br>`74:31` they uh feature a nice section of what
<br>`74:33` parameters do you have for your map and
<br>`74:36` and uh
<br>`74:37` what influence do they have but it's
<br>`74:40` it is generally relatively robust also
<br>`74:44` compared to other methods
<br>`74:45` if you go for typical like
<br>`74:49` it just but this is just empirical kind
<br>`74:51` of if you go with
<br>`74:52` about 15 to 30 neighbors
<br>`74:56` or something you usually derive good
<br>`74:59` representations
<br>`75:00` of the topology of your data if you have
<br>`75:02` enough data points
<br>`75:04` um so it's relatively robust uh to the
<br>`75:08` choice of
<br>`75:08` of parameters you don't have to play
<br>`75:10` around with it too much
<br>`75:14` thank you
<br>`75:19` okay perfect very nice do we have any
<br>`75:21` other questions
<br>`75:22` yeah there's a question from kai muller
<br>`75:25` from the chat which i will read
<br>`75:26` which is uh he asked for high
<br>`75:28` dimensional data how does human
<br>`75:30` umap determine the manifold dimension
<br>`75:36` um
<br>`75:38` i don't think that it does
<br>`75:41` and
<br>`75:47` i don't think that it does and this
<br>`75:51` might be related to that it only
<br>`75:54` in the u-map algorithm what you do is
<br>`75:56` when you when you construct
<br>`75:59` this uh the graph representation
<br>`76:02` um from the intersecting
<br>`76:06` spheres you only look at the
<br>`76:10` one simplicity so you only construct a
<br>`76:12` graph and you don't look at
<br>`76:15` [Music]
<br>`76:18` at higher order simplices i'm not sure
<br>`76:20` what this could be used to
<br>`76:22` to say something about the
<br>`76:23` dimensionality
<br>`76:26` um of your manifold i'm i'm unsure there
<br>`76:31` but you might by default it doesn't tell
<br>`76:33` you the dimensionality
<br>`76:40` okay um any other question a lot of
<br>`76:44` questions today
<br>`76:55` okay so if there are no more questions
<br>`76:57` you know then uh
<br>`76:58` let's end the meeting you know thanks
<br>`77:00` all for joining and thanks again for
<br>`77:02` fabian thank you well thank you for
<br>`77:05` having me
<br>`77:06` yeah thank you okay perfect
<br>`77:10` yeah see you all next week bye
<br>`77:16` you 

---
layout:      post
title:      ".mpipks-transcript | 09. Data Wrangling"
keywords:   "mpipks-transcript"
excerpt:    "一节课速成R语言……"
date:        2021-04-27
categories:  post
milestoneID: 38
---

### intro and slide 1

<br>`00:07` so
<br>`00:11` okay so you think i made you co-host
<br>`00:19` it's not working
<br>`00:42` okay
<br>`00:50` [Music]
<br>`00:56` so
<br>`01:05` okay i think there are no more people in
<br>`01:08` the waiting room
<br>`01:09` so we have a slightly different setting
<br>`01:11` this time
<br>`01:12` uh can somebody confirm that you can
<br>`01:15` hear me
<br>`01:17` yes okay perfect great so we have a
<br>`01:20` slightly different setting because
<br>`01:22` i um today we start a new topic and i
<br>`01:25` need my computer for that
<br>`01:27` and um so
<br>`01:31` in in the previous lectures before
<br>`01:33` christmas i gave you
<br>`01:35` an intro introduction uh about the
<br>`01:38` methods
<br>`01:39` that we need the theoretical methods
<br>`01:40` that we need in order to understand how
<br>`01:43` order emerges in non-equilibrium systems
<br>`01:47` and i also we also discuss how
<br>`01:50` order manifests in non-equilibrium
<br>`01:54` systems so now in the new
<br>`01:57` year we will look at the other side
<br>`02:01` we'll now introduce methods
<br>`02:04` that allow us actually to identify order
<br>`02:08` in experimental data
<br>`02:12` and of course i'm not talking about a
<br>`02:15` few
<br>`02:16` data points here we're talking about
<br>`02:18` large
<br>`02:19` high dimensional data sets as have
<br>`02:21` become common
<br>`02:23` in many fields of science like social
<br>`02:25` science but also biology now
<br>`02:28` so to begin let me share the screen
<br>`02:31` so i hope that rooks
<br>`02:37` so i hope that works
<br>`02:49` so actually that was a lecture that i
<br>`02:50` gave last year already
<br>`02:53` you know and um so
<br>`02:56` can you see you can't you can see the
<br>`02:58` screen i hope right
<br>`03:00` okay so just trying to get the meeting
<br>`03:02` controls
<br>`03:05` [Music]
<br>`03:11` okay it doesn't matter okay so i i
<br>`03:14` assume you can see the slides
<br>`03:15` now let me just uh make them full screen
<br>`03:20` now that's actually from a course that i
<br>`03:22` gave last year together with
<br>`03:24` fabian ross of course data science for
<br>`03:26` physicists
<br>`03:28` and today we'll discuss the methods that
<br>`03:30` we need
<br>`03:31` that actually allow us to identify
<br>`03:35` order in high dimensional data sets
<br>`03:38` and what is what do i mean with high
<br>`03:40` dimensional and large data sets

### slide 2

<br>`03:42` this is one of the data sets that i
<br>`03:45` showed you in the very
<br>`03:46` beginning of the lecture that motivated
<br>`03:49` partially this lecture and this is a
<br>`03:52` data set that
<br>`03:53` was produced by collaborators in
<br>`03:55` cambridge
<br>`03:57` and in this data set on the x-axis you
<br>`04:00` basically have part of the dna
<br>`04:03` so in the dna you have maybe a billion
<br>`04:06` or three billion base pairs
<br>`04:08` three billion base pairs roughly and
<br>`04:10` mouse and human
<br>`04:12` and in these experiments for each of
<br>`04:14` these base pairs on the dna
<br>`04:16` or each of these positions for each of
<br>`04:18` these three million
<br>`04:20` uh sites of the dna we can make take a
<br>`04:24` measurement
<br>`04:25` and measure whether there is a chemical
<br>`04:28` modification
<br>`04:29` on the dna or not yeah and
<br>`04:34` on the y axis we have different cells so
<br>`04:38` we can do that
<br>`04:39` in individual cells and on the y axis we
<br>`04:41` have roughly 600 cells
<br>`04:43` from a mouse embryo so from each of for
<br>`04:47` each of these
<br>`04:50` cells we can take roughly 3 billion
<br>`04:53` measurements here along the sequence of
<br>`04:56` the dna
<br>`04:58` that means that we have a data set here
<br>`05:00` that is typically a few terabyte in size
<br>`05:03` and that has three billion dimensions
<br>`05:06` of course not all of these dimensions
<br>`05:08` are really meaningful
<br>`05:10` but to start with we have something that
<br>`05:12` is very
<br>`05:13` huge in terms of size and now we need
<br>`05:17` something we now release some tools some
<br>`05:19` computational tools
<br>`05:21` to process such data sets
<br>`05:26` yeah so what we want to do is we want to
<br>`05:29` start with
<br>`05:31` these measurements that i just showed
<br>`05:32` you now for example we use
<br>`05:35` we measure that that's a biological
<br>`05:37` figure it's not so important to
<br>`05:38` understand the details
<br>`05:40` i'm sorry because i think i only can see
<br>`05:44` your first
<br>`05:45` slide which slide can you see
<br>`05:48` data science oh now it's uh
<br>`05:52` okay okay okay okay so
<br>`05:55` how can we do that now it's working i
<br>`05:58` think
<br>`05:58` now it's working uh go to the next slide
<br>`06:00` is that working
<br>`06:01` it is the second slide sequencing cells
<br>`06:03` yes
<br>`06:04` no it's not okay okay let me stop
<br>`06:08` sharing
<br>`06:11` let me share the desktop maybe
<br>`06:15` um okay can you see
<br>`06:20` the title slide yes now the first slide
<br>`06:24` is that when i think so yes yes and now
<br>`06:27` uh
<br>`06:28` another slide yes okay great great
<br>`06:31` so i was talking all the time probably
<br>`06:32` you didn't see this cell this slide
<br>`06:34` before here
<br>`06:36` yeah so this is what was on the x-axis
<br>`06:38` here
<br>`06:39` on the x-axis we have these three
<br>`06:41` billion base pairs
<br>`06:43` and for these base pairs we can make
<br>`06:44` measurements on the x-axis let me
<br>`06:48` get a pointer
<br>`06:51` so we have here the x-axis and this
<br>`06:53` x-axis
<br>`06:54` has these three billion dimensions
<br>`06:57` these three billion measurements for
<br>`06:59` every base pair of the dna
<br>`07:01` that we can take on the y-axis
<br>`07:04` each row on the y-axis is a different
<br>`07:07` cell
<br>`07:08` and for each of these cells that are
<br>`07:09` taken from a mouse embryo
<br>`07:11` we can take these measurements these
<br>`07:15` hugely dimensional measurements uh
<br>`07:18` in this case a living embryo now
<br>`07:22` these are breakthroughs that happen in
<br>`07:23` biology but also similar breakthroughs
<br>`07:25` with similar detail we can measure
<br>`07:28` social
<br>`07:29` systems for example if you think about
<br>`07:31` the social sciences social networks
<br>`07:33` and so on we have huge amounts of of
<br>`07:36` data

### slide 3

<br>`07:37` that we would like to understand yeah
<br>`07:39` this particular example
<br>`07:42` of biology we would like to understand
<br>`07:46` how we can transform the top part of
<br>`07:49` this big picture here
<br>`07:51` where we take measurements that have
<br>`07:53` lots of different dimensions
<br>`07:55` for this case many different cells you
<br>`07:58` can do that with
<br>`07:59` millions of cells if you want if you
<br>`08:00` have the money now
<br>`08:02` how can we transform these measurements
<br>`08:05` into a physical
<br>`08:06` theory of what's generating these
<br>`08:09` measurements
<br>`08:11` now that's what's that's what we want to
<br>`08:13` do and

### slide 4

<br>`08:14` uh to do this we need to identify
<br>`08:18` order in these structures in order to
<br>`08:20` build a hypothesis
<br>`08:22` now this is the rule this is how this
<br>`08:24` this kind of
<br>`08:26` data sets arrive on our desk
<br>`08:30` so here you see tables that contain
<br>`08:33` different bits of information
<br>`08:36` for example on the
<br>`08:40` top right here you have a table that
<br>`08:43` tells us
<br>`08:44` where on the dna we have chemical
<br>`08:46` modifications
<br>`08:47` now that has in this case 50 million
<br>`08:50` rows
<br>`08:51` we have another table here on the top
<br>`08:55` left that tells us something about
<br>`08:58` the same position on the dna it tells us
<br>`09:02` which what is the topological structure
<br>`09:05` of the dna is it
<br>`09:07` is it compact is it is it like a
<br>`09:09` spaghetti ball is it more open
<br>`09:11` or not tells us about the something
<br>`09:13` about how this dna
<br>`09:14` lives in real space now then we have
<br>`09:18` other kinds of information and we can
<br>`09:20` ask for example
<br>`09:21` how
<br>`09:24` how is this particular bit on the dna
<br>`09:29` what else do we know about that is there
<br>`09:32` a gene in this region
<br>`09:34` is there some other interesting stuff
<br>`09:35` going on in this region
<br>`09:37` now we can ask what happens by the to
<br>`09:40` these genes what are the
<br>`09:42` genes doing that's on the topic of
<br>`09:44` different experiments again
<br>`09:46` in these regions of the dna yeah and we
<br>`09:49` then have for example information about
<br>`09:51` these cells where are they located in
<br>`09:52` the embryo
<br>`09:54` uh what were the cultural conditions of
<br>`09:56` these cells for example and so on
<br>`10:00` now so now we have these uh
<br>`10:02` high-dimensional data sets from
<br>`10:03` different sources and we now
<br>`10:05` need to combine them to create a big
<br>`10:08` picture that allows us as physicists
<br>`10:11` to generate a hypothesis

### slide 5

<br>`10:14` yeah so
<br>`10:18` and this is an overview of this lecture
<br>`10:20` today and i have to uh
<br>`10:22` make a shocking uh confession that will
<br>`10:25` actually be using
<br>`10:26` r in this lecture that's something we're
<br>`10:28` not using typically in physics
<br>`10:30` but in this case it actually makes sense
<br>`10:32` it's actually suited but the syntax of
<br>`10:34` r is a little bit uh not what we're used
<br>`10:37` to in
<br>`10:37` physics so i'll give you a quick
<br>`10:40` introduction
<br>`10:41` to r to the language of r and
<br>`10:44` i assume that most of you have already
<br>`10:47` learned program and some programming in
<br>`10:49` some kind of other language like matlab
<br>`10:52` or python or c
<br>`10:55` so i'll just give you a quick
<br>`10:56` introduction to the syntax of
<br>`10:58` r and then i'll show you what are the
<br>`11:01` tools
<br>`11:02` that we have available to deal with
<br>`11:06` these large
<br>`11:07` data sets that are coming up in science
<br>`11:11` yeah so so what are the tools that we
<br>`11:13` have available what are the
<br>`11:14` computational tools and how do we select
<br>`11:17` the tools that we actually want to use
<br>`11:21` now then the very important thing is to
<br>`11:23` bring the data that has many dimensions
<br>`11:26` in a shape that we can actually deal
<br>`11:29` with
<br>`11:30` in a computationally efficient way now
<br>`11:33` that's called tidying the data to bring
<br>`11:35` it a specific format
<br>`11:36` so that we can vectorize our
<br>`11:39` computational or numerical operations on
<br>`11:42` this data sets
<br>`11:43` as i'll show you once we've done that
<br>`11:46` how we can then perform
<br>`11:48` very easily computations on
<br>`11:51` these data sets and uh and finally i'll
<br>`11:55` end with showing you how we can combine
<br>`11:57` this
<br>`11:59` these steps to produce data processing
<br>`12:01` pipelines
<br>`12:03` and of course we want to do all of this
<br>`12:05` in an elegant way
<br>`12:07` that is not so to say heavy in terms of
<br>`12:09` syntax we want to focus on the structure
<br>`12:11` of the data
<br>`12:12` but not on what is actually
<br>`12:15` on writing things and see also where you
<br>`12:18` have like hundreds of lines of codes for
<br>`12:20` a simple
<br>`12:21` operation yeah so this is the structure
<br>`12:24` and if you have time in the end i'll
<br>`12:26` uh show you something more
<br>`12:30` on data visualization

### slide 6

<br>`12:34` okay so this is arya so most of you
<br>`12:36` won't have used r before so we
<br>`12:39` don't use that in physics very much uh
<br>`12:42` r is um it's not better than python or
<br>`12:47` anything as it's very similar to python
<br>`12:49` and that it's an interpreted language
<br>`12:52` it's extremely flexible
<br>`12:54` so nothing is fixed in rng it's like you
<br>`12:56` have type function
<br>`12:58` that rewrites itself while
<br>`13:01` you execute this function it's called
<br>`13:03` extreme dynamism
<br>`13:06` um r is very popular in statistics
<br>`13:09` now you probably have heard in this
<br>`13:10` context
<br>`13:12` and uh it's very easy to include a c
<br>`13:15` code in r so if you worry about speed
<br>`13:17` you can always
<br>`13:18` write things and see and that's also
<br>`13:20` what we're usually doing
<br>`13:22` the main advantage of r is that's a huge
<br>`13:25` repository
<br>`13:27` of packages available particularly in
<br>`13:29` data science
<br>`13:31` genomics biology and so on
<br>`13:34` and one particular thing that is
<br>`13:37` actually
<br>`13:38` of the most practical relevant is that
<br>`13:41` it has
<br>`13:42` extremely convenient and high quality
<br>`13:45` plotting
<br>`13:46` functions yeah
<br>`13:49` so so these are the benefits of our that
<br>`13:51` of some downsides the syntax is very
<br>`13:54` difficult for our physicists to swallow
<br>`13:57` i'll show you later why and typically
<br>`13:59` because
<br>`14:00` nothing is fixed in r it's very dynamic
<br>`14:03` it's typically slower than python
<br>`14:05` in general terms so you wouldn't use
<br>`14:08` r to write as stochastic simulation or
<br>`14:11` something like this
<br>`14:13` but for the tasks that we're doing today
<br>`14:15` is actually uh
<br>`14:17` actually a very good choice now so it's
<br>`14:20` slowest
<br>`14:21` r is typically slow but the core
<br>`14:23` functions
<br>`14:24` are written in c so once you once you
<br>`14:27` rely on
<br>`14:28` core functions on vectorization and
<br>`14:30` things like that
<br>`14:31` then it's very fast but you know i have
<br>`14:33` to know how to use it
<br>`14:35` yeah but taken together there's no
<br>`14:37` particular reason
<br>`14:38` for for not using python for this
<br>`14:42` the only reason is that for the
<br>`14:45` for the um for the tables and for the
<br>`14:48` data i showed you the previous slides
<br>`14:50` r has been so to say the standard
<br>`14:53` language
<br>`14:54` in these experiments in genomics and
<br>`14:57` there's a lot of packages and a lot of
<br>`15:00` libraries developed for these genomics
<br>`15:03` data
<br>`15:05` that are collected in huge repositories
<br>`15:08` in our
<br>`15:10` meanwhile python is sketching a little
<br>`15:11` bit up uh
<br>`15:13` in this context so but that's why while
<br>`15:15` we're using r in
<br>`15:16` our group uh it's the context of
<br>`15:18` genomics these particular experiments
<br>`15:20` that i showed you on the previous slide

### slide 7

<br>`15:25` so typically when you use r you use it
<br>`15:28` in a
<br>`15:30` development environment an interacting
<br>`15:32` environment
<br>`15:34` that you can download from rstudio.com
<br>`15:36` and then you have
<br>`15:37` something that you looks very familiar
<br>`15:39` to you if you use matlab
<br>`15:41` or python you have a notebook here
<br>`15:44` a little bit like a jupiter notebook if
<br>`15:46` you use
<br>`15:47` python for example now where you can
<br>`15:50` write code and where you then have also
<br>`15:52` then directly the output of your code
<br>`15:54` and the same uh the same and the same
<br>`15:57` window in the same file you can
<br>`15:58` export html documents
<br>`16:03` if you want you have a console here to
<br>`16:06` type in
<br>`16:07` code now and then you have your
<br>`16:09` workspace like in matlab where you see
<br>`16:11` your variables
<br>`16:13` and you have a window that that is made
<br>`16:16` for looking at help
<br>`16:17` pages and looking at plots and other
<br>`16:20` stuff
<br>`16:22` now and um i'll show you
<br>`16:25` later getting a little bit more
<br>`16:26` interactive i'll show you later how this
<br>`16:28` works and
<br>`16:29` practice here but this is just how how
<br>`16:32` working in r looks like looks exactly
<br>`16:34` like working in any other language
<br>`16:36` actually

### slide 8, 9, 10, 11

<br>`16:38` yeah so so this is some basic r
<br>`16:41` so this this is just just to show you
<br>`16:44` that
<br>`16:44` r looks very familiar to uh
<br>`16:48` other languages actually in many in many
<br>`16:51` respects
<br>`16:52` and before i do that let me just show
<br>`16:54` you how these
<br>`16:55` what these boxes here mean and i'll
<br>`16:58` share
<br>`16:58` for that a little
<br>`17:02` our window
<br>`17:05` so let's go here
<br>`17:09` um
<br>`17:12` let me show the screen again
<br>`17:14` [Music]
<br>`17:16` okay now you should see an
<br>`17:19` r you know you should see this r studio
<br>`17:22` window
<br>`17:23` now so this that i just showed you and
<br>`17:26` here we have the code
<br>`17:28` now i can run the code and click on this
<br>`17:30` uh
<br>`17:31` little arrows here and then i run a
<br>`17:34` certain
<br>`17:34` chunk of code i can run this if i want
<br>`17:38` and load some data and i have a console
<br>`17:41` down here
<br>`17:43` that allows me to type commands if i
<br>`17:45` don't want to use this notebox here
<br>`17:47` and if you look at the bottom i can now
<br>`17:50` type assign a variable
<br>`17:51` here a and set it to one with these
<br>`17:54` weird assignment operators
<br>`17:57` as in set a to one and if i press a
<br>`18:01` i just type a and enter then i'll get
<br>`18:04` this
<br>`18:04` output the the value that is stored in
<br>`18:08` a now i can also output more complicated
<br>`18:13` values like like this table here that i
<br>`18:16` already loaded yeah and then i can look
<br>`18:19` at this in the console
<br>`18:21` and this console output is now what you
<br>`18:23` see in the slides
<br>`18:26` let me open the slides again can you see
<br>`18:27` the slides
<br>`18:32` are we back are we back with the slides
<br>`18:36` yes okay great perfect so it's working
<br>`18:38` yeah
<br>`18:39` so so here we have this i mean i've made
<br>`18:41` this fake console here and
<br>`18:43` and powerpoint now this is just to show
<br>`18:46` you
<br>`18:47` it's basically the same as in any as
<br>`18:49` many other languages like python
<br>`18:51` so here i call the function yeah and
<br>`18:54` the arguments are given in these
<br>`18:56` brackets uh
<br>`18:57` let me give you um
<br>`19:04` let me give you a pointer
<br>`19:09` here we go so somebody wrote in the chat
<br>`19:11` that the text is very
<br>`19:13` tiny was that related to our studio to
<br>`19:15` this
<br>`19:17` development environment
<br>`19:22` yeah probably yes and so so we don't
<br>`19:25` rely on that very much
<br>`19:27` um yes rc
<br>`19:30` okay okay so that's good to know
<br>`19:34` okay so just to just show you if i type
<br>`19:38` like a function
<br>`19:39` i would have called a function and an r
<br>`19:42` i do it in the usual way i can give
<br>`19:44` different arguments to this function in
<br>`19:46` this case
<br>`19:47` i take a normal normally distributed
<br>`19:50` random variable
<br>`19:52` and i tell r to give me five of them
<br>`19:55` and then i have some parameters that i
<br>`19:58` can identify by names
<br>`20:00` now so so the parameter mean are set to
<br>`20:03` one
<br>`20:04` and the parameter standard deviation are
<br>`20:06` also set to one
<br>`20:07` now these parameters have names
<br>`20:09` sometimes they have names
<br>`20:10` and they can call them with their names
<br>`20:12` it's very convenient some if you have a
<br>`20:14` long
<br>`20:15` list of parameters and you don't want to
<br>`20:18` give them all
<br>`20:19` i also can write my own functions that
<br>`20:22` looks a little bit like
<br>`20:24` mac and c so here i define a function
<br>`20:28` that's called my sum and this function
<br>`20:31` has three parameters
<br>`20:32` a b and c and c has
<br>`20:36` a default value 1.
<br>`20:39` now and then this function returns a
<br>`20:42` value that is just
<br>`20:43` equal to the sum of these three
<br>`20:46` arguments here
<br>`20:47` a plus b plus c now if i call this
<br>`20:50` function
<br>`20:50` i set a to 1 and b to 1
<br>`20:53` and c is 1 by d4 so i have don't have to
<br>`20:56` state that
<br>`20:58` i only have to state that if if i want c
<br>`21:00` to be a different value
<br>`21:02` then this function returns the value of
<br>`21:04` three not just like in
<br>`21:06` any other programming language
<br>`21:09` now we also have loops of course an r
<br>`21:12` and so this is a for loop
<br>`21:14` where you can for example have a loop
<br>`21:17` that goes from one to five
<br>`21:19` and then i can print something out or so
<br>`21:21` i have a while loop
<br>`21:23` now so while some condition is
<br>`21:26` a full fields or we want to print
<br>`21:28` something
<br>`21:30` now typically in r you don't want to
<br>`21:33` have loops if you have a loop in
<br>`21:34` r uh that means that you're doing
<br>`21:37` something wrong
<br>`21:38` so these loops are slow because r is
<br>`21:41` slow
<br>`21:42` and if you have such a loop then it
<br>`21:45` means that you didn't vectorize
<br>`21:47` your operation that you're doing
<br>`21:49` something bit by bit that you could also
<br>`21:51` do
<br>`21:52` in one step now typically if you have a
<br>`21:55` loop
<br>`21:55` then there's something wrong with your
<br>`21:58` code
<br>`22:00` or you're very extreme extremely
<br>`22:01` inefficient
<br>`22:03` and so i guess i'll have like written
<br>`22:06` like many
<br>`22:07` thousands of lines of r code
<br>`22:10` uh in my life and i have had uh exactly
<br>`22:13` one loop and uh in this
<br>`22:17` in these many thousands of lines and
<br>`22:19` several years
<br>`22:20` and this is one loop i use for a
<br>`22:22` stochastic simulation
<br>`22:25` now the mistake was that you would never
<br>`22:26` write a stochastic
<br>`22:28` simulation r but i did that because it
<br>`22:31` was very lazy
<br>`22:32` now so if you use these loops then
<br>`22:34` there's something wrong
<br>`22:35` because these loops are very you can
<br>`22:38` typically replace them with much more
<br>`22:40` efficient operations now so these are
<br>`22:44` the standard constructs that you have in
<br>`22:45` any programming language
<br>`22:47` you also have the if clauses here like
<br>`22:50` if
<br>`22:50` the value of i is smaller than 5 then
<br>`22:53` five
<br>`22:54` print hello and otherwise print not
<br>`22:56` hello yeah so that's
<br>`22:58` that's just also like in any other
<br>`23:00` language and you use
<br>`23:01` these curled brackets like in c to
<br>`23:04` define the scope
<br>`23:06` of a certain uh frame of the of the code
<br>`23:11` now that's very should all be very
<br>`23:14` familiar
<br>`23:16` now where things get a little bit
<br>`23:18` different different
<br>`23:19` are the data types of r
<br>`23:22` now so they our house has standard data
<br>`23:25` types
<br>`23:26` now so for example here we can define
<br>`23:29` vectors in principle everything is a
<br>`23:30` vector
<br>`23:31` or that's the most simple data type your
<br>`23:34` a
<br>`23:35` for example the data the the the vector
<br>`23:38` a
<br>`23:39` we define with this c here
<br>`23:42` now that's a little bit strange so in
<br>`23:48` matlab
<br>`23:58` was that a question probably not
<br>`24:03` i'll just just repeat it if it was a
<br>`24:05` question okay
<br>`24:06` so this is uh this is just a vector
<br>`24:09` how can i go back in the code
<br>`24:16` yeah okay so this is a typical vector we
<br>`24:19` we use the the letter c
<br>`24:22` to create such a vector that means
<br>`24:24` combine
<br>`24:26` and this vector has the elements one two
<br>`24:28` three
<br>`24:29` and we can also put other stuff in this
<br>`24:31` vector like this nas
<br>`24:33` that's for example a measurement that
<br>`24:36` is not available that didn't work for
<br>`24:38` example yeah but it's very convenient to
<br>`24:40` have
<br>`24:41` a representation on the computer for
<br>`24:43` measurements that
<br>`24:44` didn't work for example we can also have
<br>`24:47` a vector of
<br>`24:48` other types so here this is a string or
<br>`24:50` character vector
<br>`24:52` of m and f's so we can define this in
<br>`24:55` the very same way
<br>`24:57` and we can access elements of such
<br>`24:59` vectors
<br>`25:00` with these squared brackets yeah like in
<br>`25:03` c
<br>`25:03` for example but others but unlike in c
<br>`25:07` we start counting by one and not by zero
<br>`25:11` the next element is a list then the next
<br>`25:14` data type is a list
<br>`25:15` and then now it gets more interesting a
<br>`25:18` list
<br>`25:19` can contain several elements of any type
<br>`25:23` for example a list what elements of a
<br>`25:26` list
<br>`25:26` can be vectors now for example if i want
<br>`25:30` to make a list
<br>`25:31` and the first element of the list is our
<br>`25:34` vector
<br>`25:35` a and the second element of the list
<br>`25:38` is our vector b now they have
<br>`25:42` different types but you can nevertheless
<br>`25:44` put them
<br>`25:45` together in a list and then i can access
<br>`25:49` these uh then i can access these
<br>`25:53` lists here these list elements by the
<br>`25:56` name so i gave
<br>`25:57` gave it a name number and gender
<br>`26:01` and if i want to access the first
<br>`26:03` element number by name then i just use
<br>`26:05` these dollar signs here
<br>`26:07` and i can also assign access this first
<br>`26:10` element
<br>`26:11` by its number then i use the double
<br>`26:14` squared brackets that's not so important
<br>`26:17` just to show you that these title types
<br>`26:18` exist
<br>`26:20` when it gets more important for
<br>`26:22` statistics is that we also have
<br>`26:25` categorial variables and that's
<br>`26:26` something probably you don't know from
<br>`26:28` from matlab
<br>`26:29` or c i don't know about python category
<br>`26:32` so
<br>`26:33` so we have here a vector
<br>`26:36` that saves the gender of something
<br>`26:40` of somebody yeah so we have a long and
<br>`26:43` then
<br>`26:43` so suppose we do this measurements like
<br>`26:45` um 100 millions
<br>`26:47` of times yeah and then we have males and
<br>`26:50` females
<br>`26:51` and in principle we could store
<br>`26:54` the words male and female 100 million
<br>`26:57` times
<br>`26:58` in memory but that would be very
<br>`27:01` inefficient
<br>`27:02` what we could do instead is to say
<br>`27:05` okay i have a variable that i can only
<br>`27:07` take two values
<br>`27:10` yeah so i need this one byte at most
<br>`27:14` uh to store these which of these two
<br>`27:17` values
<br>`27:18` a given element has and then
<br>`27:23` i save an additional to that i save
<br>`27:26` labels to these two values
<br>`27:28` and that's what a factor is doing it's a
<br>`27:30` categorial variable
<br>`27:32` that can only take limited number of
<br>`27:35` values
<br>`27:36` for example uh this valve this vector b
<br>`27:39` here can only take two values
<br>`27:41` and i tell r that this can only take two
<br>`27:44` values
<br>`27:45` by making this a factor now this this
<br>`27:48` category variable is called a vector
<br>`27:51` and when i type then look at this vector
<br>`27:56` f here then it gives me the output
<br>`27:59` m f and f m f yeah and it tells me these
<br>`28:03` levels here
<br>`28:05` these are the typical values these
<br>`28:06` elements can take
<br>`28:08` yeah and if i want to make these these
<br>`28:11` levels
<br>`28:12` of these labels of these two values
<br>`28:14` different
<br>`28:16` i can call these two female and male
<br>`28:20` you know by changing these levels and
<br>`28:23` then
<br>`28:23` i have i can output this again
<br>`28:26` and have male female female male and so
<br>`28:29` on
<br>`28:30` so what happens here in r is that still
<br>`28:33` internally i don't use any more memory
<br>`28:36` although the strings are longer
<br>`28:38` what i changed here is a lookup table of
<br>`28:40` r
<br>`28:41` where r looks up where these two values
<br>`28:45` how these two values my vector can take
<br>`28:47` are called
<br>`28:49` for any plotting or any printing
<br>`28:51` purposes
<br>`28:52` now that's a that's a factor and it's
<br>`28:54` very efficient
<br>`28:55` if you think about for example biology
<br>`28:58` for these measurements that i showed you
<br>`29:02` in the beginning you have these hundreds
<br>`29:04` of millions of billions of measurements
<br>`29:06` and you have 200 million measurements
<br>`29:10` for chromosome 1. now you could either
<br>`29:13` write in your memory have a vector
<br>`29:15` that has the element chromosome 1 200
<br>`29:18` million times
<br>`29:21` or you just save a number an identifier
<br>`29:24` for chromosome one
<br>`29:26` and give it a label like this one here
<br>`29:30` with a real name in a separate table
<br>`29:33` then you don't have to save the string
<br>`29:36` chromosome one two one a million times
<br>`29:38` but only once in this table where you
<br>`29:41` look up what is actually the name
<br>`29:42` of this factory level so this is a very
<br>`29:44` efficient way of saving
<br>`29:47` variables that have that appear
<br>`29:50` very often but can only take a limited
<br>`29:54` number of values and that's that called
<br>`29:56` a factor
<br>`29:58` now that's the data type that you're
<br>`30:00` probably not familiar with
<br>`30:04` yeah and then we can go on yeah and we
<br>`30:07` can
<br>`30:07` now go to data types that can really
<br>`30:10` store
<br>`30:11` the data that we're looking at for
<br>`30:13` example experimental data
<br>`30:15` and the simplest way you can do that is
<br>`30:17` called an r a data frame
<br>`30:20` a data frame python also has data frames
<br>`30:25` and as far as i know and so these data
<br>`30:28` frames are nothing but lists
<br>`30:30` of vectors as i remember the lists
<br>`30:34` now this is a list it can save any kind
<br>`30:37` of element that you want
<br>`30:39` and if we can if we if each element of
<br>`30:42` this list here
<br>`30:43` has the same length then we can
<br>`30:46` interpret this list as a table
<br>`30:51` yeah and this is what we do in these
<br>`30:52` data frames so we here we have
<br>`30:54` three vectors x y and z
<br>`30:58` and they have different types so this is
<br>`30:59` a numerical vector
<br>`31:01` this is a character vector and this is a
<br>`31:04` boolean or logical vector
<br>`31:06` and we now can create this data frame
<br>`31:09` and say that the first element is x
<br>`31:12` the name of the first element is x and
<br>`31:16` there's the second element the second
<br>`31:18` column should be y
<br>`31:19` and the third one should be said sorry i
<br>`31:22` don't know why this has happened
<br>`31:23` all the time um
<br>`31:26` the third one should be that and what
<br>`31:28` you can see here
<br>`31:30` is how this is then represented if you
<br>`31:33` look at the output
<br>`31:35` of such a data frame so here is the
<br>`31:37` first vector
<br>`31:39` that's now the first column in our table
<br>`31:41` the second column result on our table
<br>`31:44` is this one and the third column of our
<br>`31:46` table is the boolean vector
<br>`31:48` now this is a data frame is it
<br>`31:50` essentially the
<br>`31:52` r version of a table and the only
<br>`31:56` and internally this data frame is
<br>`31:58` basically a list
<br>`32:00` of vectors that have the same length
<br>`32:07` okay so this is a data frame so and this
<br>`32:10` data frame looks close to what we could
<br>`32:13` be
<br>`32:14` dealing with or is actually what we
<br>`32:15` could be dealing with or
<br>`32:17` so sufficiently general to allow us to
<br>`32:20` store any amount of uh
<br>`32:24` experimental data now like a table is a
<br>`32:26` general way of storing data
<br>`32:28` and these data frames are essentially
<br>`32:31` tables
<br>`32:32` and they can they allow us to store any
<br>`32:35` kind of
<br>`32:36` data that we might measure

### slide 12

<br>`32:40` now the problem is now we have this data
<br>`32:42` table but what
<br>`32:43` as i told you in the beginning these
<br>`32:45` data frames
<br>`32:46` that i told you in the beginning that we
<br>`32:48` actually have
<br>`32:50` data data that is terabytes in size
<br>`32:55` so now we need a way of performing
<br>`32:59` operations on these tables in a very
<br>`33:02` efficient way now so we need the right
<br>`33:05` methods
<br>`33:06` and how important that is to pick the
<br>`33:09` right methods is here
<br>`33:11` on the left hand side so here you can
<br>`33:15` see these bars
<br>`33:16` and these bars are time measurements
<br>`33:19` that it takes to perform certain
<br>`33:22` operations on data size of
<br>`33:24` certain size yeah and
<br>`33:30` so so here this is 500 megabytes of data
<br>`33:33` so
<br>`33:34` pretty small data set and then you
<br>`33:36` measure this the length
<br>`33:37` of such an operation here that's denoted
<br>`33:39` by the bar
<br>`33:41` and you can compare different versions
<br>`33:44` different packages that allow you to
<br>`33:48` to look at this data so for example
<br>`33:52` one popular popular method in r is
<br>`33:55` called
<br>`33:56` dplyr the varia is extremely popular and
<br>`34:00` very easy to learn
<br>`34:01` way of managing these tables
<br>`34:05` another pandas
<br>`34:08` is basically the are the python version
<br>`34:12` of such a data frame and then we have
<br>`34:16` here data
<br>`34:17` table on the top the blue one
<br>`34:20` now so this is a very fast c
<br>`34:23` implementation of these
<br>`34:24` operations on these data frames it's
<br>`34:27` very fast and memory
<br>`34:28` efficient so identity you have some
<br>`34:31` things that are more
<br>`34:32` used and companies
<br>`34:35` uh also in this list now let's but this
<br>`34:38` all seems very reasonable so we have
<br>`34:41` here 12 seconds
<br>`34:43` 20 seconds 90 seconds
<br>`34:46` nothing of that stops us from doing from
<br>`34:48` getting results
<br>`34:50` now we increase the size of our data set
<br>`34:54` to 5 gigabytes or 50 gigabytes still
<br>`34:57` very small compared to what i've been
<br>`34:59` talking about
<br>`35:00` so here look let's let's have a look at
<br>`35:04` these 50
<br>`35:05` gigabytes now suddenly
<br>`35:08` there's a huge difference here
<br>`35:11` a lot of these packages a lot of these
<br>`35:13` methods you do not produce
<br>`35:15` any results at all yeah
<br>`35:18` they they run out of memory for example
<br>`35:22` and some of them like this very popular
<br>`35:25` one
<br>`35:26` takes just a huge amount of time
<br>`35:30` while others especially this data table
<br>`35:34` method here
<br>`35:34` performs very well so we have here
<br>`35:39` what is that 30 minutes so that sounds
<br>`35:42` reasonable
<br>`35:45` no no that's seconds there are 13
<br>`35:46` seconds so 13 seconds so this was
<br>`35:49` sorry so this was uh 0.2 seconds here at
<br>`35:52` the top
<br>`35:53` and now we're at uh at 13.56 because
<br>`35:56` that sounds pretty reasonable
<br>`35:58` but if you go down here to these methods
<br>`36:00` that we have here so the 13 seconds is
<br>`36:02` something that you can
<br>`36:03` wait in front of the computer
<br>`36:07` and still have some interactive way of
<br>`36:09` working
<br>`36:10` now if you go down here of course a lot
<br>`36:12` of these methods just fail
<br>`36:14` but there's also some of them just takes
<br>`36:16` so long
<br>`36:17` that any reasonable working like this
<br>`36:20` diploid here
<br>`36:21` takes so long that any reasonable way of
<br>`36:23` working with data
<br>`36:24` uh is that not possible yeah
<br>`36:28` so that's why choosing the right method
<br>`36:31` here
<br>`36:32` is uh important
<br>`36:35` and also what's important is to look at
<br>`36:37` how these methods
<br>`36:39` scale with the size and the complexity
<br>`36:41` and the dimensions of your data
<br>`36:44` so what this tells us here is there's a
<br>`36:49` huge difference
<br>`36:50` yeah and actually what i did when i
<br>`36:54` was a poster for example like every
<br>`36:56` physicist i used matlab i was used to
<br>`36:58` use
<br>`36:58` matlab yeah and then very quickly almost
<br>`37:01` immediately
<br>`37:02` matlab failed on such operations
<br>`37:05` yeah and then when these genomics
<br>`37:07` methods came up
<br>`37:09` yeah i used the red one here dipper
<br>`37:13` this is extremely popular and very easy
<br>`37:16` to get into it's very flexible
<br>`37:18` and very well documented and so on and i
<br>`37:21` used that
<br>`37:22` but then experimental progress moved on
<br>`37:25` exponentially now so when i started i
<br>`37:28` was looking at like data
<br>`37:29` a few hundred megabytes of size and
<br>`37:32` at the beginning of this talk i showed
<br>`37:35` you data that were
<br>`37:36` like a terabyte of size yeah and very
<br>`37:38` quickly i went into this problem here
<br>`37:41` that i wasn't able to get any results at
<br>`37:44` all and
<br>`37:44` meaningful times so at some point i had
<br>`37:46` to rewrite all my code
<br>`37:48` and what then turn out to be a
<br>`37:51` reasonable choice for really large data
<br>`37:53` is this data table package it is our
<br>`37:56` version
<br>`37:57` and also the python version as you see
<br>`38:00` here
<br>`38:01` is not much slower than that than the r
<br>`38:04` version
<br>`38:05` this data table is written in c is very
<br>`38:07` fast
<br>`38:08` and uh once you if you
<br>`38:12` stay strict to it then you can expect a
<br>`38:15` performance that is not much worse
<br>`38:17` than actually c but with orders of
<br>`38:19` magnitude less
<br>`38:22` programming work so
<br>`38:25` today i'll use this data table package
<br>`38:28` here
<br>`38:29` and i will also introduce some concepts
<br>`38:33` here
<br>`38:34` that are applicable to any other of
<br>`38:37` these methods or any other way
<br>`38:39` of dealing with data actually

### slide 13

<br>`38:43` okay so let's use this data table
<br>`38:46` package
<br>`38:47` now this is very fast and and works for
<br>`38:50` extremely large
<br>`38:52` uh data sets the downside is that this
<br>`38:54` syntax is not very friendly for
<br>`38:56` beginners
<br>`38:57` it's a little bit cryptic it's very
<br>`38:59` condensed and very compact
<br>`39:01` uh but it turns out that this at least
<br>`39:04` for me was the only
<br>`39:07` way that i could uh deal with data
<br>`39:10` like in an experimental field where the
<br>`39:13` sizes of data sets are exponentially
<br>`39:15` increasing
<br>`39:16` this was the only way that made me work
<br>`39:19` in an efficient way yeah so we start
<br>`39:22` this data table
<br>`39:23` we reload this package just by calling
<br>`39:26` library
<br>`39:26` data table no and then we if we have a
<br>`39:30` data frame we can just convert it to a
<br>`39:32` data table
<br>`39:33` by this command as data table that's
<br>`39:36` very simple
<br>`39:37` nothing else is necessary

### slide 14

<br>`39:41` so in this lecture uh i would like to
<br>`39:44` look at some real
<br>`39:45` data yeah so and this real data i could
<br>`39:48` now load like one terabyte of data of
<br>`39:51` experimental data
<br>`39:52` and uh but that would not be very
<br>`39:55` efficient actually for this lecture
<br>`39:56` because it would be very
<br>`39:59` slow and also very difficult
<br>`40:02` to follow so i'll look here at a simple
<br>`40:05` data set
<br>`40:06` and we'll do some operations on this
<br>`40:08` very simple data set and this is
<br>`40:10` actually data set that any of you can
<br>`40:11` download
<br>`40:12` and i'll also upload or share a link
<br>`40:15` where you can download the code of this
<br>`40:18` lecture that i'm
<br>`40:19` using in this lecture and the data
<br>`40:22` itself
<br>`40:24` okay so this is the data set this is a
<br>`40:26` called
<br>`40:27` new york city flights and these are all
<br>`40:31` flights
<br>`40:32` that departed
<br>`40:35` or arrived in new york city airports
<br>`40:39` in 2013.
<br>`40:42` yeah so the this uh this one that this
<br>`40:45` data set consists of
<br>`40:46` several files of several tables
<br>`40:50` one is the actual information about
<br>`40:53` these flights here
<br>`40:55` yeah so we have for each slide we have
<br>`40:57` information about the year
<br>`40:59` that's 2013. but we also have
<br>`41:02` information about the month
<br>`41:03` the day the hour we have an information
<br>`41:07` about the flight number and identifier
<br>`41:09` of the flight
<br>`41:10` we know we can uh know
<br>`41:14` where it came from this flight
<br>`41:17` now we have a tail number that is that
<br>`41:19` would that mean that we can identify
<br>`41:21` the airplane that was used the carrier
<br>`41:25` so is it united airlines american
<br>`41:27` airlines
<br>`41:28` lufthansa and then we have some
<br>`41:30` information about the delays
<br>`41:32` in these slides so delays in the
<br>`41:34` departure delays in the arrival
<br>`41:37` how long was the airplane in
<br>`41:40` air and many other bits of information
<br>`41:46` now this is the information for all
<br>`41:48` flights
<br>`41:49` now we want to interpret this
<br>`41:51` information that means that we need to
<br>`41:52` connect this information to other
<br>`41:55` uh other uh if you want to understand
<br>`41:59` for example where these
<br>`42:00` delays come from in this data set
<br>`42:04` we want to connect it to additional
<br>`42:05` information the one thing you might be
<br>`42:08` looking at
<br>`42:09` is the weather now if you ask for
<br>`42:12` whether why is a flight delayed we can
<br>`42:14` look at the weather
<br>`42:16` yeah and this weather is a different
<br>`42:19` source of data
<br>`42:20` and for this weather we can also get the
<br>`42:22` time
<br>`42:23` you know the month and day and hours we
<br>`42:26` can
<br>`42:27` look at the weather at a certain
<br>`42:29` airports
<br>`42:30` you know at certain locations we have
<br>`42:33` temperature humidity wind speed and
<br>`42:36` other information
<br>`42:37` about the weather at a certain location
<br>`42:39` at a certain time
<br>`42:42` now we have information about the planes
<br>`42:44` so we have this
<br>`42:45` tail number here so that it identifies
<br>`42:48` the planes
<br>`42:49` and then we can also download some
<br>`42:50` information about these airplanes
<br>`42:52` we can for example look
<br>`42:56` what manufacturer the airplane was made
<br>`42:59` we can look at the model we can look at
<br>`43:02` the
<br>`43:03` the year this airplane was built number
<br>`43:05` of engines the number of seats
<br>`43:08` the type of airplane and so on
<br>`43:11` we can get some information about the
<br>`43:13` airport
<br>`43:14` where we have uh airport information
<br>`43:17` an airport identify the name of the
<br>`43:20` airport
<br>`43:20` the longitude and latitude and altitude
<br>`43:23` of this
<br>`43:24` airport and so on and finally we can
<br>`43:27` also get some information about the
<br>`43:28` airline
<br>`43:29` now that corresponds to a certain flight

### slide 15

<br>`43:35` yeah so and now one thing you need to
<br>`43:37` notice
<br>`43:38` is that these tables here they share
<br>`43:41` information
<br>`43:43` yeah for example if we want to learn
<br>`43:47` uh what the weather was for a given
<br>`43:49` flight
<br>`43:50` then we can look at the year and the
<br>`43:52` month of the day
<br>`43:54` at the origin airport of this flight
<br>`43:58` and look and compare that to the same
<br>`44:00` columns
<br>`44:01` in this other table here
<br>`44:04` on the left hand side that contains the
<br>`44:06` weather information
<br>`44:08` now if we want to learn about the
<br>`44:10` airplane that was used
<br>`44:13` we can take this column here this bit of
<br>`44:15` information the tail number
<br>`44:18` and compare that to
<br>`44:22` this the corresponding tail number in
<br>`44:25` this planes data set
<br>`44:26` and look what kind of manufacturer this
<br>`44:28` plane was uh made by
<br>`44:30` uh which year it was produced and so on
<br>`44:34` yeah so these bits of information are
<br>`44:36` connected
<br>`44:38` uh by different variables and we can use
<br>`44:41` these overlaps between these datasets to
<br>`44:43` bring them all together later
<br>`44:46` but first let me show you how to load
<br>`44:48` data and loading data is actually also
<br>`44:50` not a trivial task
<br>`44:52` now the loading data can take hours or
<br>`44:55` minutes
<br>`44:56` depending on what function you use for
<br>`44:58` that
<br>`44:59` and in the scope of r the fastest
<br>`45:02` functions
<br>`45:03` are the ones from the data table package
<br>`45:07` they're called
<br>`45:07` f read now they're an f right that
<br>`45:10` allows you to write data
<br>`45:12` and they're basically parallelized
<br>`45:14` versions of reading
<br>`45:16` huge amounts of text data of ascii files
<br>`45:20` and it's very simple you just use the
<br>`45:23` command
<br>`45:23` f3 it's called fast read to load a
<br>`45:26` certain file here for example the text
<br>`45:29` file
<br>`45:30` and f read will do all of the rest
<br>`45:34` uh that you need to do that you need to
<br>`45:35` do it will identify the columns
<br>`45:37` will identify that the data types and so
<br>`45:39` on typically you don't need to do
<br>`45:41` anything
<br>`45:43` for example we can read in this flights
<br>`45:46` data sets
<br>`45:47` here that contains information about
<br>`45:50` flights
<br>`45:51` and it's actually the flights that
<br>`45:52` departed from new york city
<br>`45:54` and this is then how this data set looks
<br>`45:58` like
<br>`45:58` if we just print what is in once we load
<br>`46:01` these
<br>`46:02` flights we can we can print what is here
<br>`46:05` and see what's in there
<br>`46:07` we have these different columns they are
<br>`46:08` like 2030 that's the year
<br>`46:11` then we have different months we have
<br>`46:12` different days of the months
<br>`46:15` and we have departure times
<br>`46:19` and we have real departure times we have
<br>`46:22` scheduled departure times and we have
<br>`46:25` delays
<br>`46:27` now we have arrival times and so on we
<br>`46:30` have here carrier we have flight numbers
<br>`46:33` the airplane the tail number of the
<br>`46:34` airplane and so on
<br>`46:37` origin destination and so on yeah
<br>`46:41` and we have a timestamp here a time
<br>`46:43` signature
<br>`46:45` of when this flight actually took place
<br>`46:49` now so let's go uh
<br>`46:53` to our studio and see how this looks
<br>`46:55` like
<br>`46:56` [Music]
<br>`46:58` um
<br>`47:01` here we go now this is our studio i hope
<br>`47:04` you can see our studio now it should be
<br>`47:06` still
<br>`47:07` sharing yeah and uh
<br>`47:11` so here the top rows so okay so this was
<br>`47:14` a little bit small right
<br>`47:16` um let me zoom in
<br>`47:25` okay so i hope this is better um
<br>`47:29` so here we're loading
<br>`47:33` all of these files actually the same
<br>`47:35` thing that we did
<br>`47:38` [Music]
<br>`47:39` that i had on slides so for each of
<br>`47:41` these different bits of information
<br>`47:43` we now load these files into memory
<br>`47:47` now so i had already done that before so
<br>`47:49` here they are
<br>`47:50` in the workspace and we know we can
<br>`47:52` click on these files so we can
<br>`47:53` either now just type flights
<br>`47:57` yeah and get this huge table out
<br>`48:00` or you know so we see we have here
<br>`48:05` 300 more than 300 000 flights that we
<br>`48:08` have information about
<br>`48:10` or i can just click on this file here
<br>`48:14` and get a little nice table view of
<br>`48:17` the data that we have now this is the
<br>`48:20` flight information
<br>`48:21` it's also high dimensional not as
<br>`48:23` extremely high dimensional
<br>`48:25` as the example i gave you but it has
<br>`48:27` still enough
<br>`48:28` information that we cannot easily detect
<br>`48:31` patterns
<br>`48:32` in this data set yeah so this is
<br>`48:36` this is the data we have 300 000 flights
<br>`48:40` and now we can try to detect some
<br>`48:44` structures
<br>`48:45` in this data set
<br>`48:49` let's get back to powerpoint
<br>`48:55` okay here we go now we've loaded the
<br>`48:58` data we've got all of these different
<br>`49:00` data tables now or data frames and
<br>`49:03` memory

### slide 16

<br>`49:04` and now we're trying to make sense we're
<br>`49:06` trying to make sense out of these
<br>`49:08` statuses
<br>`49:09` the first thing that we always need to
<br>`49:12` do
<br>`49:13` is to bring data in a format
<br>`49:16` that we can deal with it that the data
<br>`49:19` and this format is typically called date
<br>`49:22` tidy data or a long data or long format
<br>`49:27` now that two simple rules that you can
<br>`49:31` use to decide whether
<br>`49:32` a data table or a data framework or
<br>`49:35` table is tidy
<br>`49:36` so one thing you need to make sure is
<br>`49:38` that every column
<br>`49:41` is a different observable for example
<br>`49:44` different types of measurements
<br>`49:47` every row are then different
<br>`49:50` observations of these measurements of
<br>`49:54` these observables or different or
<br>`49:56` variables
<br>`49:57` yeah once you stick to these rules your
<br>`50:00` data is tidy
<br>`50:02` and when your data is tidy so every
<br>`50:05` column
<br>`50:06` is a different observable and every row
<br>`50:09` is an observed observation
<br>`50:11` then we can use vectorized operations
<br>`50:15` in r or python to perform operations
<br>`50:19` on entire columns of these
<br>`50:22` data tables yeah and that
<br>`50:26` first is extremely fast you know because
<br>`50:28` it's vector-wise we've informed these
<br>`50:30` operations
<br>`50:31` one column at a time and it drastically
<br>`50:34` reduces the complexity
<br>`50:36` of the code now the
<br>`50:39` the data that i showed you are one of
<br>`50:41` the standards
<br>`50:43` data sets and data signs and uh
<br>`50:46` that that you you look at for for
<br>`50:49` teaching
<br>`50:50` and uh these date this data is already
<br>`50:53` tidy
<br>`50:54` so let's have a look now at these
<br>`50:56` flights
<br>`50:57` so every column is a different
<br>`51:00` observation this is a different
<br>`51:02` observable yeah for example a different
<br>`51:04` measurement
<br>`51:05` a different departure time a different
<br>`51:08` arrival time a different flight number
<br>`51:11` a different time points
<br>`51:15` and every row is a different observation
<br>`51:19` so a different flight
<br>`51:21` so this data table is already in a tidy
<br>`51:24` format
<br>`51:26` and it's already in a format that we can
<br>`51:28` deal with so we have nothing to do here

### slide 17

<br>`51:31` in a standard example of a non a messy
<br>`51:34` data set
<br>`51:36` that we also often find in physics but
<br>`51:38` also here in this case in
<br>`51:43` in in genomics is that we have
<br>`51:46` matrices that we share data as a matrix
<br>`51:50` for example in this matrix here that's a
<br>`51:52` typical matrix here
<br>`51:54` so this is a measurement one of these
<br>`51:55` genomics measurements so here on each
<br>`51:58` row
<br>`51:59` is a different gene now so and the first
<br>`52:02` column here is the name of this gene
<br>`52:05` that's a very cryptic name these genes
<br>`52:07` have cryptic names
<br>`52:10` each row is in gene and each column is a
<br>`52:13` different cell
<br>`52:16` yeah so this data set
<br>`52:19` is not tidy
<br>`52:23` because the same measurement so sorry
<br>`52:25` that these numbers
<br>`52:26` mean how many products of this given
<br>`52:30` gene
<br>`52:31` we have measured in a given cell
<br>`52:35` so these are the numbers it's not
<br>`52:37` important to understand the biological
<br>`52:38` context
<br>`52:40` and but this data set is not tidy
<br>`52:43` because the same
<br>`52:45` observable namely the number of these
<br>`52:48` these gene products is repeated in
<br>`52:51` different columns
<br>`52:54` and you can easily see that by having
<br>`52:57` this format
<br>`52:59` we're not very very flexible so if i now
<br>`53:01` for the same gene
<br>`53:03` and for the same cell make another
<br>`53:05` measurement
<br>`53:06` what do i do where do i put that in this
<br>`53:08` matrix so we have
<br>`53:10` then we have to have a separate matrix
<br>`53:12` and i have to live with separate
<br>`53:14` matrices
<br>`53:15` in parallel so this data set is not

### slide 18

<br>`53:18` it's not tidy and
<br>`53:22` i cannot perform easily parallelized
<br>`53:25` operations on this data table and now we
<br>`53:27` want to make this data table
<br>`53:29` tidy i know there are special functions
<br>`53:33` that allow us to do that and
<br>`53:37` these functions are
<br>`53:41` basically i just give you the names and
<br>`53:43` they have similar names basically in all
<br>`53:45` contexts to make such a data table tidy
<br>`53:48` like the one that i have here this
<br>`53:50` function is called
<br>`53:52` mels it's called you also said you melt
<br>`53:54` a data table
<br>`53:56` and that brings us from this matrix
<br>`53:58` format
<br>`54:00` to a format where every
<br>`54:03` column represents an observation and
<br>`54:06` each row
<br>`54:08` represents i sorry each column
<br>`54:10` represents an observable
<br>`54:11` like a measurement and each row
<br>`54:14` corresponds
<br>`54:15` to a measurement or an observable yeah
<br>`54:18` so
<br>`54:18` the right would you see on the right
<br>`54:20` hand side that would be
<br>`54:22` the tidy version of the data that show i
<br>`54:25` showed you on the
<br>`54:26` on the last slide so the first column
<br>`54:28` would be the cell
<br>`54:30` the second is the gene the name of the
<br>`54:32` gene the second column would be the name
<br>`54:34` of the cell
<br>`54:35` and the third column would be the value
<br>`54:38` that i measure
<br>`54:39` for the g products now so that would be
<br>`54:42` the tidy format
<br>`54:43` and now i can have a long i have a long
<br>`54:46` vector here
<br>`54:47` of numbers in this
<br>`54:50` one column and i don't have 200 columns
<br>`54:54` as in the previous slide
<br>`54:57` okay so how do we do that in our this on
<br>`55:00` data in this data table package the
<br>`55:02` command is called
<br>`55:03` melt we just give it the name of our
<br>`55:06` data table
<br>`55:08` and then we identify id variables
<br>`55:11` so these are variables uh
<br>`55:14` that need to remain so to say intact
<br>`55:19` uh once we once we reshape this matrix
<br>`55:22` now in our case this is the id column
<br>`55:26` yeah and the value name is
<br>`55:30` uh how we want to call
<br>`55:33` the values that are in these matrix
<br>`55:36` elements here now and we just call this
<br>`55:39` expression now that's what we call
<br>`55:42` and the variable name is the cell that
<br>`55:44` we have here already
<br>`55:46` that tells us that this variable name is
<br>`55:48` distributed
<br>`55:49` now into this column now and then if you
<br>`55:52` look at these colors here
<br>`55:54` you can see how this command distributes
<br>`55:56` what is actually now distributed
<br>`55:58` into several columns
<br>`56:01` how this reshapes this data table into
<br>`56:04` something that has a longer format it's
<br>`56:06` called actually also called long format
<br>`56:09` uh where we have uh the cell name
<br>`56:12` this column and then the corresponding
<br>`56:14` measurements in this column
<br>`56:17` for the products yeah you can look at
<br>`56:19` this i'll upload the slides of course so
<br>`56:21` you can look at this
<br>`56:22` uh in detail afterwards
<br>`56:25` it's a little bit abstract but this is
<br>`56:27` so say how we reshape
<br>`56:29` data tables to make them tidy

### slide 19

<br>`56:33` yeah and we can also uh make them messy
<br>`56:37` again now so i'll go quickly over that
<br>`56:39` because that's not something we use
<br>`56:41` but sometimes you just want to have your
<br>`56:43` good old matrix back
<br>`56:44` because some functions some other
<br>`56:46` package wants to have a matrix
<br>`56:48` yeah and that's called then this
<br>`56:50` function is called d
<br>`56:52` cast and that just reverses
<br>`56:55` uh that reverses the operation that i
<br>`56:58` told you on the last slide
<br>`56:59` where we give you where this function
<br>`57:02` takes the data table
<br>`57:04` uh the name of the data table variable
<br>`57:06` as the first
<br>`57:07` argument and then a formula of how the
<br>`57:11` rows and column columns
<br>`57:13` should be now separated in this new
<br>`57:17` matrix that we want to have now it's not
<br>`57:20` so
<br>`57:20` important so i'll not go into it it's
<br>`57:22` not so we
<br>`57:24` rarely use that and
<br>`57:28` now we have some mess some tidy data
<br>`57:30` yeah so
<br>`57:31` we have some tidy data now every column
<br>`57:34` is an observation every row sorry i
<br>`57:38` always mess it up
<br>`57:39` every column is an observable or a
<br>`57:41` variable
<br>`57:42` every row is an observation

### slide 20

<br>`57:45` once we're in this format we can now
<br>`57:47` have a very simple syntax
<br>`57:50` now and this syntax actually captures
<br>`57:53` ideas
<br>`57:54` that uh we also have in other
<br>`57:57` maybe more popular languages like sql or
<br>`58:01` sql that's that's
<br>`58:04` more that captures operations on this
<br>`58:07` data table
<br>`58:08` that are quite generic so so this is the
<br>`58:11` general syntax that we use in this data
<br>`58:14` table package
<br>`58:15` so we have three now we take this data
<br>`58:18` table
<br>`58:18` d and in squared brackets
<br>`58:22` we have three arguments
<br>`58:25` yeah and the way you read these three
<br>`58:28` arguments
<br>`58:29` is that you take the data table d
<br>`58:32` and then you have something at the first
<br>`58:34` argument that operates
<br>`58:36` on the rows yeah you have here a
<br>`58:39` condition that
<br>`58:40` tells you which kind of rows you want to
<br>`58:42` take
<br>`58:44` the second one operates on the columns
<br>`58:47` yeah and for example you can in the
<br>`58:51` second
<br>`58:51` argument you can perform a calculation
<br>`58:55` on the columns and the third ones the
<br>`58:58` third argument
<br>`58:59` is a grouping variable now the third one
<br>`59:02` is it's like it's like a typical matrix
<br>`59:05` a statement y and j the third one is a
<br>`59:07` grouping variable
<br>`59:09` where we can group rows together by
<br>`59:11` certain conditions
<br>`59:12` and perform these calculations here
<br>`59:16` group by group now so the way to read
<br>`59:19` that is to take
<br>`59:20` the data table d subset the rows using i
<br>`59:24` that can be some expression some logical
<br>`59:27` statement for example
<br>`59:28` we calculate what is in j
<br>`59:32` and do this calculation group grouped
<br>`59:36` by whatever is in this third argument
<br>`59:39` and i'll now show you step by step
<br>`59:41` how this looks in detail
<br>`59:44` and these uh arguments here these three
<br>`59:48` albums are
<br>`59:48` a very very general way this is also say
<br>`59:52` parametrize um operations on these
<br>`59:56` large tables now so with these just
<br>`59:58` three arguments we can do
<br>`60:00` a lot of stuff already and if you think
<br>`60:03` about it it's actually
<br>`60:04` abstract but it's very simple
<br>`60:09` so now first let's have a look at the
<br>`60:11` very first argument

### slide 21

<br>`60:15` yeah so let's just say we have a table
<br>`60:18` and we just want to get
<br>`60:19` a subset of rows from the table
<br>`60:22` now for example we want to look at all
<br>`60:26` planes
<br>`60:26` that have four engines
<br>`60:30` now the way we do that is we just
<br>`60:33` write this logical statement here as the
<br>`60:36` first argument
<br>`60:38` so engines equals four
<br>`60:41` and if we do that then we get back a
<br>`60:43` data table that only has the planes
<br>`60:48` that have for four engines
<br>`60:51` in them that have four engines now we
<br>`60:53` filtered
<br>`60:54` the rows of these data tables for the
<br>`60:57` rows that have
<br>`60:58` the value of the engine column equals to
<br>`61:02` four
<br>`61:04` now we can also select a subset of
<br>`61:07` columns here on the right hand side
<br>`61:10` and this we do by this notation here
<br>`61:12` this dot is actually a shortcut for
<br>`61:15` for for and for a list yeah so
<br>`61:18` what we do is we give a list of the
<br>`61:21` names of
<br>`61:22` columns that we want to extract
<br>`61:26` as the second argument so for example we
<br>`61:30` take this planes data set
<br>`61:32` and we want to get the tail number and
<br>`61:34` the year
<br>`61:35` this airplane was built and then we get
<br>`61:38` a shorter
<br>`61:39` a smaller data table back that only has
<br>`61:42` these two columns
<br>`61:44` in them yeah so this is all something
<br>`61:46` that you could also do with any other
<br>`61:48` package or any other programming
<br>`61:50` language of course
<br>`61:54` now we want to get a little bit more
<br>`61:58` complicated

### slide 22

<br>`61:59` now we want to do an operation on these
<br>`62:01` data tables on these
<br>`62:02` large data sets and these operations in
<br>`62:05` general have a quite general scheme
<br>`62:09` yeah so and this general scheme is
<br>`62:11` already
<br>`62:12` in this syntax notation that i showed
<br>`62:14` you a few slides ago with the i
<br>`62:17` and j and the group is already
<br>`62:21` so say in there so that the the steps
<br>`62:26` that we take
<br>`62:27` is called the group aggregate combine
<br>`62:29` scheme
<br>`62:30` so what we do the general operation on
<br>`62:33` such a data table looks like that we
<br>`62:36` first group our observations
<br>`62:40` by some meaningful way so for example we
<br>`62:43` want to group
<br>`62:44` all slides that happen in the same month
<br>`62:50` yeah and then we aggregate aggregates
<br>`62:52` means that we
<br>`62:53` put extract all of these groups all
<br>`62:56` flies from the same month
<br>`63:00` at a time and aggregates mean at the
<br>`63:04` third step that we
<br>`63:05` perform some kind of summary function
<br>`63:08` on these flights that departed in a
<br>`63:11` certain month for example we want to
<br>`63:13` then calculate
<br>`63:14` the average temperature or the average
<br>`63:16` delay
<br>`63:17` now this is the third thing here where
<br>`63:19` we aggregate
<br>`63:21` all of these different flies that belong
<br>`63:23` to the same group
<br>`63:25` and calculate a single result from that
<br>`63:30` and i'll also give you now a specific
<br>`63:32` example of this

### slide 23

<br>`63:34` so what we can do for example
<br>`63:37` is that we can group by carrier so we
<br>`63:40` want we might want to
<br>`63:42` ask are all carriers equally bad
<br>`63:46` or equally good or is there one carrier
<br>`63:49` that is worse than other carriers
<br>`63:51` now the way we do that is we
<br>`63:55` first group that's the last column
<br>`63:59` here we group all slides
<br>`64:03` and we take the flights data table and
<br>`64:06` then we group the flights
<br>`64:08` all flights together that have the same
<br>`64:10` carrier
<br>`64:13` and for each carrier we then calculate
<br>`64:17` the average delay using the mean
<br>`64:20` function
<br>`64:21` now we take the mean of the departure
<br>`64:24` delay and this third argument
<br>`64:27` just tells us that we should remove an
<br>`64:30` ace so
<br>`64:30` and not the numbers for example we're
<br>`64:32` not a proper measurement was taken where
<br>`64:34` this information is missing
<br>`64:36` now we just just ignore this yeah so for
<br>`64:39` every
<br>`64:40` carrier we take all flights
<br>`64:45` and calculate the average delay time
<br>`64:50` now so this is what we do here now all
<br>`64:52` carriers
<br>`64:54` that's here the grouping is the third
<br>`64:55` variable and then we perform this
<br>`64:58` operation and the second variable
<br>`65:00` because it operates on the columns
<br>`65:02` and the operation we do is we calculate
<br>`65:04` the average
<br>`65:05` of the delay and we save it in a new
<br>`65:08` column
<br>`65:09` that's called mean delay
<br>`65:13` now what we get from that is for every
<br>`65:15` carrier
<br>`65:18` we get one number which is this average
<br>`65:20` delay
<br>`65:23` now and you can see that basically that
<br>`65:26` confirms what you
<br>`65:27` expected already that united airlines is
<br>`65:30` not performing very well
<br>`65:34` now we can also have more complicated
<br>`65:36` procedures now we can for example
<br>`65:39` uh combine that with only
<br>`65:42` with a subsetting in the roads we don't
<br>`65:44` want to take all flights
<br>`65:46` we always want to look we only want to
<br>`65:48` look at flights
<br>`65:49` in the evenings you know very late
<br>`65:51` flights
<br>`65:53` and then we can for example do the same
<br>`65:55` thing we uh
<br>`65:57` yeah and we can we can also have a more
<br>`66:00` fine grade
<br>`66:02` fine-grained or we can look at different
<br>`66:06` combinations of variables here for
<br>`66:08` example
<br>`66:09` in this case here we
<br>`66:12` take all flights that
<br>`66:15` depart after 8 pm
<br>`66:21` and the remaining flights we group by
<br>`66:24` month at the origin airport
<br>`66:29` and we again calculate the average
<br>`66:32` departure delay
<br>`66:35` and now for every combination of month
<br>`66:38` and airport
<br>`66:40` we get a value for the average delay
<br>`66:42` here at the bottom
<br>`66:44` now for example in january uh the
<br>`66:47` newark airport had an average delay
<br>`66:50` of 14 minutes
<br>`66:55` yeah and jfk was doing much better
<br>`66:58` yeah and so you can see that this also
<br>`67:02` kind of is something that that people
<br>`67:05` expect to see here actually
<br>`67:07` yeah um okay so this is how you how this
<br>`67:12` group aggregate combined paradigm
<br>`67:16` can be fit into very compact syntax
<br>`67:20` on basically arbitrary complex tables
<br>`67:25` now we can also so this was
<br>`67:29` now a summary statistics where we
<br>`67:31` performed where we
<br>`67:32` summarized several rows yeah all flights
<br>`67:36` that have the same carrier
<br>`67:37` or all flights in a different in a
<br>`67:39` certain month and a certain
<br>`67:41` airport we summarize and summarize
<br>`67:44` all of these slides into just one
<br>`67:47` quantity for example the average delay
<br>`67:51` so we perform the summary here what we

### slide 24

<br>`67:54` can also do
<br>`67:56` is we can calculate we can add a new
<br>`67:59` column to our table
<br>`68:02` that has one new value for each
<br>`68:06` row that is in the original table so we
<br>`68:09` don't perform
<br>`68:10` a summary it's also sometimes called
<br>`68:12` windowing
<br>`68:13` for whatever reason and so we have
<br>`68:16` one new value for each row that we had
<br>`68:20` in our original data set for example
<br>`68:23` here the top row
<br>`68:24` if i don't want to have the flights
<br>`68:27` uh if i wanted to have this the speed in
<br>`68:30` kilometers per hour
<br>`68:32` now i can for example then get uh
<br>`68:35` calculate the distance over the air time
<br>`68:39` in minutes
<br>`68:40` now that's the speed and miles per
<br>`68:42` minute
<br>`68:44` and then i multiply by 60 and convert to
<br>`68:48` kilometers
<br>`68:49` and then i have the speed for every
<br>`68:51` flight i have the average speed in
<br>`68:53` kilometers
<br>`68:53` per hour i can also rescale for example
<br>`68:57` i can combine
<br>`68:59` now these simple computations here with
<br>`69:01` the grouping
<br>`69:02` for example i can rescale all distances
<br>`69:07` by the average distance
<br>`69:11` added of a certain carrier for example i
<br>`69:14` can ask
<br>`69:15` is this flight much further
<br>`69:18` or much shorter than a typical flight
<br>`69:21` conducted by the same carrier yeah so
<br>`69:25` then i can calculate a rescale
<br>`69:27` distance that is just the distance
<br>`69:30` divided by the average distance
<br>`69:33` of this carrier here and then again i
<br>`69:36` get a new
<br>`69:37` variable a new value for each row that i
<br>`69:41` had in my original table
<br>`69:44` and the way i do these operations is by
<br>`69:46` these symbols here these define
<br>`69:48` symbols column and equal signs
<br>`69:52` now the way this looks like is now that
<br>`69:54` we have fear
<br>`69:56` our original 300 000 rows
<br>`70:00` but for each row we have calculated now
<br>`70:03` a new
<br>`70:05` column a new value that we save in a new
<br>`70:07` column
<br>`70:08` speed uh kmh uh
<br>`70:11` that is the speed in kilometers
<br>`70:15` and we also have the the rescale
<br>`70:17` distance
<br>`70:19` now for example this flight here was a
<br>`70:21` little bit ten percent shorter
<br>`70:23` than the average flight of this carrier
<br>`70:27` now and uh this also is saved into a new
<br>`70:31` column
<br>`70:32` that we've given these names here
<br>`70:35` now this is something that is that is
<br>`70:38` also happening very fast
<br>`70:40` and memory efficient
<br>`70:45` so now comes now comes more complicated
<br>`70:49` things so this was in principle easy
<br>`70:52` step we add more columns
<br>`70:53` we perform a summary and this data table
<br>`70:58` package allows us to write a very simple
<br>`71:01` syntax
<br>`71:02` in order to do that now if you try to do
<br>`71:05` these groupings
<br>`71:06` in c also you write many many lines of
<br>`71:08` codes
<br>`71:09` to do that now

### slide 25, 26, 27, 28, 29

<br>`71:12` the next step we want to make use that
<br>`71:16` these that these to get some more
<br>`71:19` understanding about these delays here
<br>`71:22` in new york city we want to make use of
<br>`71:24` the fact that these whether we have
<br>`71:26` different bits of information
<br>`71:28` and these different bits of information
<br>`71:31` share
<br>`71:33` columns or share information that allows
<br>`71:35` us to link them
<br>`71:38` yeah for example we can link the weather
<br>`71:42` to a certain flight by matching the year
<br>`71:45` the month the day and the hour
<br>`71:49` and the airport yeah
<br>`71:52` and with this we can connect the flight
<br>`71:56` to the weather that that occurred when
<br>`71:58` this flight
<br>`71:59` departed yeah we can also
<br>`72:05` connect the airport information for
<br>`72:07` example
<br>`72:08` so this faa is an identifier that has a
<br>`72:11` different name in this table
<br>`72:13` but it's essentially the same as in the
<br>`72:15` origin airport
<br>`72:16` and we can link we have the information
<br>`72:18` to link these tables together
<br>`72:21` now the planes the the tail number is a
<br>`72:24` unique
<br>`72:24` identifier that allows us to look up the
<br>`72:27` plane
<br>`72:28` of our at our of our flight
<br>`72:31` in this data table this data set of all
<br>`72:34` plates
<br>`72:36` and also the same with an airline we can
<br>`72:38` look up the carrier
<br>`72:40` identifier in another data table and get
<br>`72:43` the name of the carrier
<br>`72:45` now so these these tables are
<br>`72:48` interlinked
<br>`72:49` and now we need efficient ways to merge
<br>`72:53` these these big different bits of
<br>`72:55` information together
<br>`72:58` yeah and this merging happens
<br>`73:03` in a way that is also often called joins
<br>`73:05` now this is a general principle that you
<br>`73:07` do basically
<br>`73:08` in any kind of of data handling uh
<br>`73:11` task independent of the
<br>`73:14` programming language that you're using
<br>`73:17` and
<br>`73:18` the first join and then you can perform
<br>`73:21` these joints or these mergings of these
<br>`73:23` data tables
<br>`73:24` in different ways and these different
<br>`73:27` ways
<br>`73:28` differ in the way which information you
<br>`73:31` keep in case you only find it in one
<br>`73:34` table but not in the other table
<br>`73:37` now for example so let's begin with one
<br>`73:41` kind of join
<br>`73:43` it's called the left join
<br>`73:47` that's called the left join and what you
<br>`73:49` do
<br>`73:50` is that you keep all rows
<br>`73:53` that are in the left data table now in
<br>`73:56` this a here
<br>`73:58` now we want to combine in this case the
<br>`73:59` information in a
<br>`74:01` and b yeah and then we can look up
<br>`74:06` okay so here we have a value x1
<br>`74:09` that corresponds to a
<br>`74:12` and we have a value of x one a and now
<br>`74:15` we can look up
<br>`74:16` what is the other columns x two and x
<br>`74:19` three
<br>`74:20` now so x two is one and x three is this
<br>`74:23` is true
<br>`74:25` yeah and then we can combine these two
<br>`74:27` columns in the right way
<br>`74:29` that they correspond to the value of x1
<br>`74:32` a same for b now we can look up b
<br>`74:36` in both columns so they don't need to be
<br>`74:37` in the same position
<br>`74:39` in both tables we can look up the b and
<br>`74:42` get the values of the remaining columns
<br>`74:45` and sort them here to the end of this
<br>`74:47` table
<br>`74:48` and now we have the three the c
<br>`74:52` now c is in table a and the first one
<br>`74:55` on the left one but not in the right one
<br>`74:59` and a left join means that we take c
<br>`75:05` from the left one we don't have
<br>`75:08` information
<br>`75:09` from the white one so x3 is empty
<br>`75:13` and we disregard all rows that are on
<br>`75:16` the right
<br>`75:17` table but not in the left table so
<br>`75:20` that's a left
<br>`75:21` join and an r or in this data table
<br>`75:24` framework this is done by the function
<br>`75:27` merge that takes two tables
<br>`75:31` and the left join is then specified by
<br>`75:33` saying that
<br>`75:34` all x so all first column all entries in
<br>`75:37` the first
<br>`75:38` column should be true should be taken
<br>`75:42` there's also a short notation for this
<br>`75:44` joining
<br>`75:45` and that's just when you index one data
<br>`75:47` table
<br>`75:48` by another data table so it's a very
<br>`75:50` compact syntax
<br>`75:51` for performing a very complex operation
<br>`75:56` and this is something these joints are
<br>`75:57` also something that are not trivial
<br>`75:59` computation think you're doing that with
<br>`76:01` with something that has terabytes
<br>`76:05` in size yeah so in principle you have to
<br>`76:07` look up
<br>`76:08` all rows in both data table and find the
<br>`76:10` corresponding matches
<br>`76:12` now you need to find have uh very
<br>`76:15` efficient algorithms
<br>`76:16` to do that and depending on what you
<br>`76:19` choose here
<br>`76:20` which package you choose to perform this
<br>`76:22` algorithm you can wait for days
<br>`76:24` or you can wait for minutes now that
<br>`76:26` makes a huge difference
<br>`76:29` so if there's a left join there's also a
<br>`76:30` right join and right join just means
<br>`76:32` that we
<br>`76:33` keep all rows from the right table
<br>`76:38` but we disregard rows from the left
<br>`76:40` table if they're not
<br>`76:42` in the right table that's the right join
<br>`76:45` and
<br>`76:45` in all this just is that works by uh
<br>`76:48` also by the merge command
<br>`76:50` and we just give the argument that oh y
<br>`76:53` yeah that you know that we should all
<br>`76:55` keep all
<br>`76:57` uh columns in the second y data set
<br>`77:01` and there's also then a short notation
<br>`77:03` for these right joints
<br>`77:07` there's so called inner join that's the
<br>`77:10` most restrictive joint
<br>`77:12` and this
<br>`77:16` inner join just keeps values
<br>`77:19` keeps rows where we have information
<br>`77:22` in both tables now if we don't have
<br>`77:26` information in both tables
<br>`77:28` then this row will not end up in the
<br>`77:30` final
<br>`77:31` data set for example c only is in the
<br>`77:34` left
<br>`77:35` table d is only in the right table
<br>`77:40` yeah and then we uh
<br>`77:44` none of these ends up in the final
<br>`77:46` results
<br>`77:48` that's the inner join yeah and uh
<br>`77:52` so again here there's a merge command
<br>`77:54` for that we just say all
<br>`77:56` equals false and there's always a
<br>`77:58` shorthand notation
<br>`78:00` with an additional argument for that
<br>`78:04` so in all of these commands here i
<br>`78:05` didn't specify
<br>`78:07` the column that we should use for
<br>`78:09` joining i didn't specify
<br>`78:11` that x1 is the column we should use for
<br>`78:14` comparing
<br>`78:15` now i didn't specify for example if you
<br>`78:18` look here
<br>`78:20` which column we should actually use to
<br>`78:22` match slides to the
<br>`78:23` together and i didn't do that
<br>`78:27` bef because this column has the same
<br>`78:30` name
<br>`78:32` in both data sets so x1 pops up
<br>`78:35` both in a and b and then r automatically
<br>`78:40` assigns these columns these columns that
<br>`78:42` have the same names
<br>`78:44` uh uses them to match these different
<br>`78:46` tables
<br>`78:48` so if there's an inner join there's also
<br>`78:50` an outer join
<br>`78:52` or a full join and this full join
<br>`78:55` retains
<br>`78:55` all values from all rows
<br>`78:59` so that it happens if we just now join
<br>`79:02` or merge these two tables
<br>`79:04` then we get our column x1 that is shared
<br>`79:07` between these tables
<br>`79:09` and our column x2 from this first table
<br>`79:13` where we don't have a value for d
<br>`79:17` and the column x3 from the right table
<br>`79:21` where we don't have a value for c
<br>`79:25` now so this retains the most information
<br>`79:32` okay so now we can do some

### slide 30, 31

<br>`79:36` merging so now we can for example ask
<br>`79:39` are these delays affected by bad
<br>`79:43` weather now so the first thing we need
<br>`79:45` to do
<br>`79:46` is to merge the flights
<br>`79:49` and the weather data sets because they
<br>`79:52` share columns with the same names
<br>`79:56` for example time hour or so of
<br>`79:59` our
<br>`80:03` whereas the origin airport now since i
<br>`80:05` didn't plot that here they share columns
<br>`80:07` with the same names that the ones that
<br>`80:08` are connected with these arrows
<br>`80:10` that works automatically so i merged
<br>`80:12` them
<br>`80:14` and now i have a new table that
<br>`80:19` contains information about the flight
<br>`80:22` the carrier
<br>`80:23` and also the delay but also at the same
<br>`80:27` time
<br>`80:27` the columns from the weather data set
<br>`80:30` that have information about
<br>`80:32` wind speed and precipitation and about
<br>`80:34` the temperature
<br>`80:37` now and now we can go on and ask for
<br>`80:40` example
<br>`80:42` let's group this combined
<br>`80:45` table here let's group that
<br>`80:49` on the one hand by the rows that have a
<br>`80:52` wind speed larger than 30
<br>`80:55` and by wind speeds smaller than 30.
<br>`81:00` yeah and then for each of these two
<br>`81:04` groups
<br>`81:05` calculate the average departure delay as
<br>`81:08` before
<br>`81:11` now so if the wind speed is smaller or
<br>`81:14` equals to 30
<br>`81:15` here then the departure delay was 12
<br>`81:19` minutes
<br>`81:21` if the wind speed was larger than 30
<br>`81:24` then the departure delay was 28 minutes
<br>`81:27` so much larger
<br>`81:29` and if i couldn't evaluate
<br>`81:33` this condition here for example if i
<br>`81:35` don't
<br>`81:36` have information about wind speed yeah
<br>`81:39` then i get
<br>`81:39` also a value for these nas for these
<br>`81:42` non-available data
<br>`81:44` so that means that that if it's very
<br>`81:47` windy there's a
<br>`81:48` higher chance or there's a typical
<br>`81:50` higher average delay
<br>`81:52` in these flights in new york city
<br>`81:57` now we can also ask we can also merge
<br>`82:00` the flights table with the plain table
<br>`82:09` oh so is anybody stuck at the joint
<br>`82:11` slide
<br>`82:18` now so which what is the slide that
<br>`82:19` you're seeing at the moment
<br>`82:24` are planes equally reliable
<br>`82:28` our place equal so that's the right so
<br>`82:30` matthew matthew is having a problem
<br>`82:32` um but at least some of you are seeing
<br>`82:36` the
<br>`82:37` the right slide okay um
<br>`82:42` okay so we can merge the flight
<br>`82:44` information
<br>`82:46` with information about planes
<br>`82:50` and now i give this additional column
<br>`82:52` here this additional
<br>`82:53` argument i tell the merged command to
<br>`82:56` use this column tail number
<br>`82:59` to to match the information to match the
<br>`83:01` rows
<br>`83:03` now if i do that then i get also my
<br>`83:05` flight information about the delay
<br>`83:08` about the carrier and so on but i know
<br>`83:11` also get information about the
<br>`83:12` manufacturer
<br>`83:14` about the model number and about
<br>`83:18` the year this airplane was created
<br>`83:21` and because we had already a year column
<br>`83:24` namely the year of the flight
<br>`83:26` we now have two different columns your x
<br>`83:29` and your y
<br>`83:30` your x is the column of the flight when
<br>`83:32` did the flight take place
<br>`83:34` and your why is the year when
<br>`83:37` the airplane was built
<br>`83:41` okay and now we can just
<br>`83:44` do our calculation now we can ask are
<br>`83:48` certain manufacturers uh more
<br>`83:51` or less reliable are the planes by
<br>`83:53` certain manufacturers more or less
<br>`83:55` reliable
<br>`83:56` yeah so that was we do the same thing
<br>`83:59` yeah so we group by manufacturer
<br>`84:04` now by this column here we group now the
<br>`84:07` rows
<br>`84:08` and then for each group we calculate
<br>`84:11` the average departure delay
<br>`84:16` here and save it into a new column mean
<br>`84:18` delay
<br>`84:20` and in this case we also calculate the
<br>`84:21` standard error now which is
<br>`84:23` just the standard deviation divided by
<br>`84:25` the square root
<br>`84:26` of the sample size now we can have two
<br>`84:29` computations or as many computations as
<br>`84:31` we want
<br>`84:32` in the same row yeah and here we see
<br>`84:36` that okay so we have here airboroughs
<br>`84:38` industries i don't know what
<br>`84:39` i forgot what is actually the uh the
<br>`84:42` outcome of this
<br>`84:43` boeing is a little bit later than airbus
<br>`84:47` and then we have here two two times uh
<br>`84:49` airbus
<br>`84:51` and uh the problem now here is that
<br>`84:54` airbus apparently changed its name and
<br>`84:56` one of them is older than the others and
<br>`84:58` that's why they have different delays
<br>`85:01` now these are smaller airplanes here
<br>`85:03` like
<br>`85:04` at this m and blair and bombardier these
<br>`85:07` are smaller planes
<br>`85:08` and these smaller planes have higher
<br>`85:12` delays now i can ideas like
<br>`85:15` uh i'm not kind of there there's also a
<br>`85:18` smaller
<br>`85:19` yeah and some of these smaller planes
<br>`85:21` seem to have
<br>`85:22` higher delays

### slide 32

<br>`85:25` yeah and then we can also do a trick now
<br>`85:28` so
<br>`85:29` typically you do many many operations
<br>`85:32` and such a processing of such data says
<br>`85:34` you do many many operations
<br>`85:37` after each other yeah and
<br>`85:40` what we typically do in programming we
<br>`85:43` do one operation
<br>`85:44` and save the result in a new variable
<br>`85:47` now then we do the next operation and
<br>`85:49` save the result in a new variable now we
<br>`85:51` do another operation and save the result
<br>`85:53` in a new variable
<br>`85:55` now this is very inefficient if you have
<br>`85:57` long pipelines
<br>`86:00` of maybe hundreds of different steps in
<br>`86:02` your analysis
<br>`86:03` and how you transform the data
<br>`86:06` yeah and in our
<br>`86:10` uh and also in other languages there are
<br>`86:13` ways
<br>`86:14` to chain operations after each other
<br>`86:18` now to make these pipelines in a very
<br>`86:21` efficient
<br>`86:22` and in condensed
<br>`86:25` condensed way in terms of syntax now so
<br>`86:28` there's a
<br>`86:29` there's a tailway that is implemented in
<br>`86:31` this data table package
<br>`86:33` now there you just change they just put
<br>`86:36` the squared brackets directly off with
<br>`86:39` each other
<br>`86:40` for example here we create a new column
<br>`86:45` wind speed and kilometers per hour and
<br>`86:48` here we just
<br>`86:49` multiply the wind speed in miles per
<br>`86:51` hour by
<br>`86:52` 1.61 to get the kilometers per hour
<br>`86:57` and then directly in the next step we
<br>`87:00` group by month
<br>`87:01` and calculate the average wind speed in
<br>`87:04` kilometers per hour so these are two
<br>`87:07` steps and we don't have to save the
<br>`87:09` results and intermediate variables
<br>`87:11` we just put them down we chain them
<br>`87:13` directly after each other
<br>`87:16` so there's a more common way to
<br>`87:20` chain or to make these pipelines and
<br>`87:22` this is
<br>`87:23` in another package that's called
<br>`87:24` magritter
<br>`87:26` now we load this package just at the
<br>`87:29` beginning of our code
<br>`87:31` and this package does one thing it
<br>`87:33` provides us with an
<br>`87:34` operator this one here
<br>`87:38` and everything this operator does is
<br>`87:41` it takes whatever is on the left of it
<br>`87:47` and pass it is to the first as the first
<br>`87:50` argument
<br>`87:51` to the function that is on the right of
<br>`87:52` this operator
<br>`87:55` now so this is very very simple we take
<br>`87:58` what is on the left
<br>`88:00` and pass it to the function of the on
<br>`88:02` the right as the first argument
<br>`88:05` now and with this we can then have
<br>`88:08` longer chains if we want
<br>`88:10` now for example we take weather
<br>`88:12` calculate the wind speed
<br>`88:14` in kilometers per hour and then
<br>`88:18` use this chaining upper this this pipe
<br>`88:21` operator here
<br>`88:22` from this package and pause it
<br>`88:25` to the next argument here we
<br>`88:29` have here an updated data table with
<br>`88:32` this new
<br>`88:33` package and that that's what we take
<br>`88:36` and we pass it to the next step of our
<br>`88:39` analysis
<br>`88:40` where we calculate the average wind
<br>`88:42` speed
<br>`88:44` per month and we take the result again
<br>`88:48` and passes to basically any function
<br>`88:51` that we want and here we pass it to for
<br>`88:53` example the the head
<br>`88:55` function and this head function just
<br>`88:57` gives us the first five rows or so
<br>`88:59` of our data table now so with these
<br>`89:02` operators here you can make very very
<br>`89:04` long pipelines
<br>`89:05` and you still have your codes uh in a
<br>`89:08` very
<br>`89:10` basic you have a list then in your code
<br>`89:11` you have a list of steps
<br>`89:13` that you perform one after each other
<br>`89:16` and so your code is still
<br>`89:17` in a very convenient way that you can
<br>`89:20` still

### slide 33

<br>`89:22` understand yeah so this is a more
<br>`89:25` uh more complex example of such a
<br>`89:28` pipeline here
<br>`89:29` that we take the flights data sets
<br>`89:34` now merge it with the weather data set
<br>`89:39` now merge it with a plane state merge
<br>`89:41` the result
<br>`89:42` now with the planes data set
<br>`89:45` merge the results with the air ports
<br>`89:48` data set
<br>`89:49` and here i have to specify the columns
<br>`89:52` yeah that because they have different
<br>`89:53` names in both data sets
<br>`89:56` and we merge it with the airlines data
<br>`89:58` sets at the very end
<br>`90:00` yeah and now we have a data set that has
<br>`90:02` all the different information
<br>`90:04` all the different source information the
<br>`90:06` same table
<br>`90:08` yeah and now we can for example remove
<br>`90:11` flights that don't have information
<br>`90:13` about the departure delay
<br>`90:15` and we can do the steps that we did
<br>`90:18` previously for example we can get the
<br>`90:20` speed of the plane the average speed
<br>`90:23` in kilometers per hour we get the
<br>`90:25` rescale speed so every faster or slower
<br>`90:30` than what is typical for a certain
<br>`90:32` airplane model
<br>`90:34` and a certain carrier now and we can
<br>`90:38` also calculate things like correlations
<br>`90:41` now so for example here
<br>`90:43` we calculate the correlation between the
<br>`90:46` temperature
<br>`90:49` and the rescape speed of the airplane
<br>`90:54` now and here what do we do here
<br>`90:59` ah so what do we do here so we calculate
<br>`91:03` the difference in speed of the airplane
<br>`91:08` for flights that have a delay larger
<br>`91:12` than 20 minutes
<br>`91:14` and where the delay is zero
<br>`91:18` or smaller than zero yeah so here's the
<br>`91:21` difference in the speeds that have a
<br>`91:23` large delay
<br>`91:24` and that have a negative delay or no
<br>`91:26` delay
<br>`91:28` i recalculate that by carrier that's
<br>`91:30` just an example here
<br>`91:32` and uh what we see here is that
<br>`91:35` uh now so here this this correlation
<br>`91:38` here
<br>`91:39` is typically positive now so this
<br>`91:42` correlation is positive
<br>`91:44` that means for some reason the warmer
<br>`91:46` the temperature
<br>`91:48` the higher the speed of the airplane
<br>`91:51` now there's a positive correlation yeah
<br>`91:56` now so whatever this means yeah and
<br>`91:59` also what we see here is that this
<br>`92:02` difference in speed
<br>`92:04` is very often positive now american
<br>`92:08` airlines are so it's positive
<br>`92:09` that means that these airplanes fly
<br>`92:11` faster
<br>`92:13` when they have a delay compared to when
<br>`92:16` they don't have a delay
<br>`92:18` and you can also compare the the
<br>`92:20` carriers
<br>`92:22` united airlines has a little bit more
<br>`92:25` speed
<br>`92:26` you know than than american airlines
<br>`92:29` and you can get all kinds of insights
<br>`92:31` here from that now that's of course not
<br>`92:33` extremely insightful yeah but it
<br>`92:35` illustrates
<br>`92:36` how you can do simple operations and
<br>`92:38` complex data sets
<br>`92:40` in just a few lines of codes and i don't
<br>`92:44` have to tell you that in c
<br>`92:45` or matlab you would be spend a lot of
<br>`92:47` time and a lot of lines of codes to
<br>`92:49` implement that

### slide 34

<br>`92:52` yeah just to summary this part and uh
<br>`92:55` if we have time i'll show you a little
<br>`92:56` bit about plotting no we don't have time
<br>`92:59` um so i showed you that these data
<br>`93:03` frames are efficient ways of storing
<br>`93:06` high dimensional data of different kinds
<br>`93:10` and
<br>`93:13` depending on
<br>`93:16` where your data is stored and how large
<br>`93:19` is it
<br>`93:20` you can choose different tools yeah if
<br>`93:23` your data is stored locally
<br>`93:25` and it's very large and you rely on
<br>`93:27` speed then data table
<br>`93:29` is a good way to go if your data is
<br>`93:34` is for example on a server on the
<br>`93:36` internet
<br>`93:37` yeah and it's not that large then you
<br>`93:40` would use
<br>`93:40` other codes that are better at
<br>`93:42` interacting with net network uh
<br>`93:44` resources
<br>`93:45` yeah for example like this diplo package
<br>`93:48` yeah and the key step is actually always
<br>`93:52` to bring it to clean up the data to
<br>`93:53` bring it to this tidy format
<br>`93:56` and once you've done that we have this
<br>`93:59` split
<br>`94:00` aggregate combine paradigm where you
<br>`94:03` group
<br>`94:04` your data by different conditions
<br>`94:07` by basically any condition you want and
<br>`94:10` then for each group
<br>`94:12` you extract the corresponding rows of
<br>`94:14` the data table
<br>`94:16` and perform operations on this for
<br>`94:18` example to perform summaries
<br>`94:20` on this data on this on these rows
<br>`94:23` and the package that i showed you here
<br>`94:25` allows you to do all of these steps
<br>`94:27` in a single very short line of code
<br>`94:31` yeah and finally i showed you how uh
<br>`94:34` pipelines actually help you to create
<br>`94:38` to structure your code uh if it gets
<br>`94:41` very complex which is usually usually
<br>`94:43` the case
<br>`94:44` yeah and uh what i will do is i will
<br>`94:47` upload some slides
<br>`94:48` that shows show you how to visualize
<br>`94:51` data
<br>`94:51` now that's just i mean you all have your
<br>`94:54` favorite topic plotting packages
<br>`94:56` i'll upload to some slides that shows
<br>`94:58` you how to basically
<br>`95:00` uh how people developed a grammar for
<br>`95:03` graphics that allows you basically to
<br>`95:05` make an infinitely complex
<br>`95:09` clause or data visualization using a
<br>`95:12` very simple
<br>`95:13` grammatical construct so i'll upload
<br>`95:16` this on the website
<br>`95:17` and then let me know if you have any
<br>`95:20` questions
<br>`95:21` and otherwise see you all next week
<br>`95:25` so next week i should say so the next
<br>`95:26` week we go into a machine learning and
<br>`95:28` we'll have a guest
<br>`95:29` speaker which is our local which is
<br>`95:33` basically that the chief data scientist
<br>`95:37` from on one of the json institutes here
<br>`95:40` from the
<br>`95:41` center for regenerative therapies
<br>`95:44` and he'll share fabian us and he'll
<br>`95:46` share some of his insights
<br>`95:48` into how to use machine learning to
<br>`95:51` detect that
<br>`95:51` actually low dimensional structures
<br>`95:56` and high dimensional data sets now as i
<br>`95:59` see as you probably realize now we're
<br>`96:01` able to
<br>`96:02` do computations fast computations on
<br>`96:06` on huge data sets but what i showed you
<br>`96:10` was a little bit tedious you know
<br>`96:12` this was i actually didn't show you
<br>`96:13` actually how to come up
<br>`96:15` with uh low dimensional structures or
<br>`96:17` with order and data
<br>`96:19` yeah so and this is something we'll deal
<br>`96:21` with uh next week
<br>`96:22` and we'll have a guest lecturer then
<br>`96:25` which is uh which is fabian here from
<br>`96:27` from dresden
<br>`96:28` okay see you all next week bye
<br>`96:32` i'll stay online for a while to case of
<br>`96:34` any questions
<br>`96:43` uh i was wondering if um
<br>`96:47` if you dealt with like temporal data
<br>`96:50` or are most of the data that's coming
<br>`96:53` out of these experiments just kind of
<br>`96:55` you know there there's some static
<br>`96:58` information about the
<br>`96:59` genomics and proteomics and all that yes
<br>`97:02` so that's typically static data
<br>`97:04` but this although it's static it
<br>`97:06` contains dynamic information
<br>`97:09` yeah um indirectly so you have
<br>`97:12` measurements so of course like like very
<br>`97:15` often biology you have to kill the cells
<br>`97:17` that you actually want to
<br>`97:19` want to measure or you have to kill the
<br>`97:21` animals that you actually want to
<br>`97:23` look into and but you have some
<br>`97:26` indirect dynamical information i'll
<br>`97:29` actually
<br>`97:30` share you send me an email about a paper
<br>`97:33` we just
<br>`97:34` uploaded something
<br>`97:39` that actually answers the question about
<br>`97:41` how this field theory
<br>`97:43` and data science approaches work
<br>`97:46` together and this is actually an example
<br>`97:48` from genomics
<br>`97:49` i share it with you in the chat um
<br>`97:58` just see where this is here we go
<br>`98:09` okay so i'll share it with you in the
<br>`98:11` [Music]
<br>`98:14` chat all right thank you
<br>`98:16` there you go and that that that that
<br>`98:18` actually answers the question in your
<br>`98:20` email
<br>`98:20` and just took and you needed the needed
<br>`98:22` the christmas holidays
<br>`98:24` some time to to finish and upload it
<br>`98:27` and um this is actually an example where
<br>`98:30` you have
<br>`98:31` static data in genomics you can only
<br>`98:34` have static data
<br>`98:36` but indirectly you have dynamic
<br>`98:39` information
<br>`98:40` so actually actually actually although
<br>`98:42` the map in this
<br>`98:43` this specific example here we have
<br>`98:46` static data because of course you have
<br>`98:48` to kill the cells you have to kill the
<br>`98:49` embryo
<br>`98:50` but you can still have time causes
<br>`98:54` with different embryos or different
<br>`98:56` cells now so that you
<br>`98:59` kill one embryo at one stage that's of
<br>`99:02` course mouse non-human
<br>`99:03` yeah so you kill one embryo at one stage
<br>`99:06` and then next embryo one day later
<br>`99:09` yeah and the next embryo one day later
<br>`99:11` so then the day you get some implicit
<br>`99:13` temporal information and actually in
<br>`99:16` this
<br>`99:16` same paper we also conducted a time
<br>`99:19` course
<br>`99:20` with a very high temporary resolution
<br>`99:23` but
<br>`99:24` you always have at each time when you
<br>`99:26` kill you look at different cells and
<br>`99:28` that's that's always the uh so
<br>`99:31` that's the best you can hope for is
<br>`99:33` something semi-static
<br>`99:35` yeah but but nevertheless yes so we
<br>`99:37` still have dynamic information
<br>`99:40` indirectly via the measurements that we
<br>`99:43` can make for example
<br>`99:44` along the dna yeah and
<br>`99:48` so that's although we cannot make direct
<br>`99:51` dynamic information we can have
<br>`99:54` indirectly generate hypothesis
<br>`99:57` that we then can indirectly basically
1<br>`00:00` test using state
1<br>`00:01` static data if you have a look at this
1<br>`00:04` at this manuscript and you'll see how it
1<br>`00:06` works and let me know if you have any
1<br>`00:07` questions
1<br>`00:08` it's very a little bit more logical and
1<br>`00:10` this method
1<br>`00:11` also has a supplement with all the field
1<br>`00:13` theory in it
1<br>`00:15` okay thank you
1<br>`00:18` okay great perfect
1<br>`00:29` okay so if there are no more questions
1<br>`00:31` then see you all next week
1<br>`00:34` bye

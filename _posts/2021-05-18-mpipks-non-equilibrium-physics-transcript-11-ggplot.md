---
layout:      post
title:      ".mpipks-transcript | 11. Data Visualization"
keywords:   "mpipks-transcript"
excerpt:    "前半截是数据可视化（ggplot 教程），后半截是一个实操演示（“格里沙你看好了，巨人之力是这样用的”），问题在于后半截的项目内容在课程网站和 github 页面上都没找到……"
date:        2021-05-18
categories:  post
milestoneID: 41
---

### Review of last lecture

<br>`00:01` uh just uh just to know that the lecture
<br>`00:03` is actually recorded
<br>`00:05` so you will be visible uh on the
<br>`00:07` recorded lecture at the end
<br>`00:09` if it doesn't bother you
<br>`00:13` just just let you know okay great
<br>`00:16` so hello everyone back to our lecture
<br>`00:21` last time we had a special lecture a
<br>`00:24` guest lecture
<br>`00:25` by one of our local data scientists
<br>`00:29` and uh he uh which was a fabian host
<br>`00:33` and fabian explained us from like a
<br>`00:36` hands-on perspective
<br>`00:38` because that's his job uh how
<br>`00:41` you can detect in
<br>`00:45` non-equilibrium systems and the
<br>`00:47` non-equilibrium systems that fabric is
<br>`00:49` working on are of course
<br>`00:50` biological systems and what he
<br>`00:54` basically showed is how biology how
<br>`00:57` older
<br>`00:58` and non-equitable systems manifest
<br>`01:00` itself
<br>`01:01` in low-dimensional structures in these
<br>`01:04` high-dimensional data sets that he
<br>`01:05` showed you some
<br>`01:07` methods that will also appear on the
<br>`01:10` website i didn't get to uploading uh the
<br>`01:12` slides in the video yet
<br>`01:13` um so so he showed you some methods of
<br>`01:17` how to
<br>`01:18` reduce dimensionality or how to extract
<br>`01:21` hidden dimensions in these
<br>`01:24` in the high dimensional data sets and

### introduction & slide 1

<br>`01:27` so today so i will start by giving you a
<br>`01:30` little bit of
<br>`01:31` more introduction to data science and
<br>`01:35` some of the things that we need for the
<br>`01:36` next lecture that's in the first part of
<br>`01:38` the lecture
<br>`01:40` and in the second part of the lecture i
<br>`01:43` will
<br>`01:43` give you another hands-on experience for
<br>`01:46` a practical
<br>`01:47` example of from start to finish of how
<br>`01:50` to
<br>`01:51` go through such a data science pipeline
<br>`01:55` now to start the beginning beginning of
<br>`01:58` the lecture
<br>`01:59` uh we'll go back to our new york city
<br>`02:01` flights
<br>`02:02` data set so there's a little gap because
<br>`02:05` we had to
<br>`02:06` find dates with uh fabian last time so
<br>`02:08` there's a little
<br>`02:09` gap this lecture is now connected to
<br>`02:11` what i told you
<br>`02:12` uh two lectures ago and uh
<br>`02:16` let me just share the slide i'll tell
<br>`02:18` you give you a little a brief
<br>`02:20` introduction
<br>`02:21` to data visualization
<br>`02:24` just a short one because the slides have
<br>`02:26` been already
<br>`02:28` on the website since two weeks or maybe
<br>`02:31` some of you have already looked at them
<br>`02:33` let me just share the screen
<br>`02:37` there we go
<br>`02:40` okay great perfect so so i'll give you a
<br>`02:44` quick
<br>`02:44` introduction before we go on an enhanced
<br>`02:46` on example
<br>`02:48` so today we'll have a hands-on data
<br>`02:50` science example and next week we'll have
<br>`02:52` a hands-on
<br>`02:53` field theory combined with data science
<br>`02:56` example now that will be
<br>`02:57` next week um so today i'll still need to
<br>`03:01` introduce you to some methods that we
<br>`03:03` will need
<br>`03:04` and um if you
<br>`03:08` can confirm now that you can see my
<br>`03:11` slides
<br>`03:12` can somebody confirm is that working
<br>`03:15` yes okay perfect yeah so i'll just give
<br>`03:18` you a quick introduction uh to
<br>`03:20` how to visualize uh data
<br>`03:24` and of course you're all in your work
<br>`03:25` you're all visualizing data all the time
<br>`03:27` but if your data is high dimensional
<br>`03:29` very uh uh and uh complex and structure
<br>`03:33` uh it actually matters what you use for
<br>`03:36` visualization
<br>`03:38` yeah and um so
<br>`03:41` with this lectures two lectures ago when
<br>`03:43` we talked about this new york city
<br>`03:45` data set about the flights that were
<br>`03:47` departing from the new york city
<br>`03:49` airports i showed you all kinds of ways
<br>`03:52` of how to
<br>`03:53` do very efficient computations
<br>`03:56` on these data sets but all these
<br>`03:59` competitions like it didn't
<br>`04:00` really give us any real insight
<br>`04:04` and the reason was that we were dealing
<br>`04:05` with plain numbers but we
<br>`04:07` never had anything to look at and uh
<br>`04:11` today in the first part of this lecture
<br>`04:13` i'll quickly
<br>`04:15` show you a plotting scheme so to say
<br>`04:18` that is very powerful
<br>`04:20` in visualizing a general and visualizing
<br>`04:23` high dimensional data so

### slide 2

<br>`04:27` before that just a quick reminder so
<br>`04:29` before we do
<br>`04:30` anything we always want to make our data
<br>`04:33` set uh
<br>`04:34` tidy you know so we typically we
<br>`04:37` collaborate with experimentalists they
<br>`04:39` give us the the
<br>`04:40` we obtain the data in a very messy
<br>`04:42` format and then the first step is to
<br>`04:45` tidy the data and that means that we
<br>`04:47` need to bring it in a form where
<br>`04:49` every column is an observable or
<br>`04:52` variable
<br>`04:53` and every row is it is an
<br>`04:56` observation or a sample sorry to
<br>`04:59` interrupt you did you change your
<br>`05:02` first slide yes oh you can't see that
<br>`05:05` no we cannot i don't know what this
<br>`05:06` always happens now in zoom
<br>`05:08` there was a zoom update
<br>`05:12` there's something maybe i have to share
<br>`05:15` the entire screen
<br>`05:17` let's try this um the problem is just
<br>`05:21` that i have like
<br>`05:21` 100 windows on my desktop
<br>`05:25` um if somebody has a system that happens
<br>`05:30` lately all the time right um that zoom
<br>`05:33` is not working properly okay let's share
<br>`05:37` the desktop
<br>`05:42` okay now i'm not having embarrassing
<br>`05:45` stuff on the
<br>`05:46` desktop but that's not the case okay so
<br>`05:49` you should be seeing my
<br>`05:52` uh desktop now
<br>`05:58` oh okay okay a lot of
<br>`06:01` lot of wind okay okay okay
<br>`06:05` now you now you know what i've been
<br>`06:07` working on okay
<br>`06:08` so
<br>`06:12` can you see uh this messy and tidy slide
<br>`06:17` and when i change the slides now can you
<br>`06:19` see that it's just
<br>`06:20` right now it works okay perfect
<br>`06:24` so so this is uh so so
<br>`06:27` just a just a reminder uh that the first
<br>`06:31` step that we always do is to make the
<br>`06:33` data tidy now where we if you have the
<br>`06:37` data in entire defaults format then we
<br>`06:39` can perform
<br>`06:40` column wise operations that are in most
<br>`06:44` programming language
<br>`06:45` highly optimized and very efficient
<br>`06:49` to run until to program
<br>`06:53` i introduced you to this very simple
<br>`06:58` r package that allows you to implement
<br>`07:01` all of these operations and data science
<br>`07:05` and there are many other packages of
<br>`07:06` course and other other statements

### slide 3

<br>`07:09` and typically such an operation
<br>`07:13` consists of three steps so you
<br>`07:16` filter the data that is in this data
<br>`07:18` table package the first
<br>`07:20` parameter then you group
<br>`07:24` the columns by some condition
<br>`07:27` now that's the third parameter and then
<br>`07:29` you perform
<br>`07:31` an operation independently on each group
<br>`07:33` that is the one in the middle
<br>`07:36` so this is a typical step in such a data
<br>`07:39` science
<br>`07:40` calculation and i showed you how you
<br>`07:42` then can combine these steps along
<br>`07:44` pipelines
<br>`07:46` uh to perform that complex operations

### slide 4

<br>`07:50` today i want to show you a way of how to
<br>`07:53` more intuitively
<br>`07:55` interact with the data and the way we
<br>`07:57` typically do that you all
<br>`07:59` are familiar with uh plotting of course
<br>`08:01` and the way we typically do that
<br>`08:03` is we have a plot in mind yeah and this
<br>`08:06` plot then has a name
<br>`08:08` that's a scatter plot a surface plot
<br>`08:11` a histogram and then you look for the
<br>`08:13` function
<br>`08:15` in and you look for the function and
<br>`08:17` matlab also that gives you this specific
<br>`08:19` kind of plot
<br>`08:21` yeah another way to do that and that
<br>`08:24` would
<br>`08:25` introduced by someone called leland
<br>`08:27` wilkins
<br>`08:28` in a book is that you don't give the
<br>`08:31` plots names
<br>`08:33` but you construct you construct these
<br>`08:35` plots with a grammar
<br>`08:37` that means that you have a set of rules
<br>`08:40` that allows you to construct
<br>`08:42` step-by-step almost any visualization of
<br>`08:45` your data
<br>`08:47` and once you have that you don't have to
<br>`08:49` remember long names of different kinds
<br>`08:51` of plots
<br>`08:52` you just add bit by bit like in a
<br>`08:54` sentence you add word or
<br>`08:56` or there's word by word to make this
<br>`08:59` sentence
<br>`09:00` more rich in information but the only
<br>`09:02` thing that you need to know
<br>`09:04` is the grammar itself and this allows
<br>`09:06` you to
<br>`09:07` create from the simple grammar uh very
<br>`09:09` different kinds of visualizations
<br>`09:12` now and this idea that you have a
<br>`09:14` grammar of graphics
<br>`09:16` you know i've got a set of rules that
<br>`09:17` allows you to construct
<br>`09:19` visualizations uh it is an r
<br>`09:22` implemented in the ggplot package
<br>`09:25` gtw 2 that's quite famous
<br>`09:29` and in python and that's a little bit
<br>`09:30` newer i don't know how well it works
<br>`09:33` it's called the plot
<br>`09:34` 9 package now that analyze the same idea
<br>`09:39` and in r we just load this using the dg
<br>`09:42` plot the library command and then we are
<br>`09:45` able to use all of these commands

### slide 5

<br>`09:47` in this package now so the basic idea is
<br>`09:52` that we start with a tidy
<br>`09:56` data table or data frame in r
<br>`09:59` and we take this and then we construct
<br>`10:03` assign different
<br>`10:06` visual characteristics of our plot
<br>`10:10` two different columns of this data table
<br>`10:15` yeah so the first thing we have to do
<br>`10:18` is uh the first thing we have to do is
<br>`10:21` we have to say
<br>`10:22` what to plot a plug the point or a line
<br>`10:25` and that's called the geometry
<br>`10:28` a point line bar circle whatever and
<br>`10:31` that's the geometry
<br>`10:33` then we have this mapping that i
<br>`10:34` mentioned yeah where we map
<br>`10:36` different aesthetic properties of our
<br>`10:40` plot
<br>`10:41` two different columns in this table here
<br>`10:45` now for example we could say that the
<br>`10:47` position on the x coordinate
<br>`10:50` should be what is in column a
<br>`10:53` the y coordinate should be what is in
<br>`10:55` column b
<br>`10:56` the size of our dots or whatever should
<br>`10:59` be whatever is
<br>`11:00` reflect whatever is in column d and the
<br>`11:03` column
<br>`11:04` should miss a c and the column the color
<br>`11:07` should be what is in column d
<br>`11:12` how these values are then translated
<br>`11:16` to specific colors or to specific size
<br>`11:19` or so
<br>`11:20` is a different question now we have the
<br>`11:24` static properties of our plots or our
<br>`11:26` dots so where are they located
<br>`11:28` how do they look like and then we just
<br>`11:30` have to define a coordinate
<br>`11:32` system to define where they appear
<br>`11:36` on the screen yeah and if you have these
<br>`11:39` things together
<br>`11:40` we have the simplest version of a plot
<br>`11:44` on the right hand side

### slide 6

<br>`11:48` so the way this works in practice is
<br>`11:51` that you
<br>`11:52` have these little building blocks
<br>`11:55` that you just put together
<br>`11:58` line by line now so
<br>`12:01` in r this looks like that you first have
<br>`12:03` to of course do
<br>`12:04` something to create an object and this
<br>`12:07` is just this ggplot command
<br>`12:10` where you tell the plot what data to use
<br>`12:13` as the first argument
<br>`12:15` and the second argument is then how to
<br>`12:18` map
<br>`12:18` different columns of your data
<br>`12:21` of your table to different pro visual
<br>`12:24` properties
<br>`12:25` of your plot and then you add a geometry
<br>`12:30` for example point or line and you have
<br>`12:32` your first plot already
<br>`12:35` you can of course also add more
<br>`12:37` properties yeah you can add more
<br>`12:39` geometries or you can add more
<br>`12:41` uh detailed properties of your plot for
<br>`12:44` example
<br>`12:45` if you are not happy with cartesian
<br>`12:48` coordinates then you can set your own
<br>`12:50` coordinate system
<br>`12:52` now you can have polar coordinates or
<br>`12:53` whatever
<br>`12:55` you can have subplots by
<br>`12:58` by adding this further rule here it's
<br>`13:01` called facets
<br>`13:03` you can change how values
<br>`13:06` in this data table how they map
<br>`13:10` to different properties so which color
<br>`13:12` represents
<br>`13:13` which value in your table you can change
<br>`13:17` themes for example or different uh the
<br>`13:20` way
<br>`13:20` lines and whatever are plotted and you
<br>`13:23` can of course also save your file
<br>`13:25` and these different building blocks of
<br>`13:27` your plots
<br>`13:28` are connected via these plus signs now
<br>`13:31` you put that
<br>`13:32` just as many as you want of these things
<br>`13:34` of these aspects
<br>`13:36` after each other and by this you
<br>`13:38` construct more and more complex
<br>`13:40` plots yeah and for
<br>`13:44` everything that you see here below there
<br>`13:45` are some sensible defaults for example
<br>`13:49` cartesian coordinates that in many cases
<br>`13:52` you don't need to touch
<br>`13:54` now let's have a little look at our new
<br>`13:56` york city data set
<br>`13:59` and this new york city data set right
<br>`14:02` here we go

### slide 7

<br>`14:02` now we already discussed that uh
<br>`14:06` two weeks ago and in this new york city
<br>`14:08` data set we have
<br>`14:09` information about flights departing from
<br>`14:13` new york city airports for each flight
<br>`14:16` we have
<br>`14:17` different information we have for
<br>`14:19` example the time
<br>`14:21` when this flight departed we have the
<br>`14:24` origin
<br>`14:24` airport we have the number of the plane
<br>`14:26` that was used
<br>`14:28` the carrier and so on and the delay
<br>`14:31` uh for this specific flight and also as
<br>`14:35` we already discussed
<br>`14:36` you can connect this table that we can
<br>`14:39` have
<br>`14:40` that you can download from our github uh
<br>`14:44` from the from the website um we can
<br>`14:47` connect
<br>`14:48` these flights then to other sources of
<br>`14:50` information for example
<br>`14:52` the weather that uh with the weather
<br>`14:55` information for a given
<br>`14:57` point in time and a given location
<br>`15:00` we can also connect that to airport
<br>`15:02` information
<br>`15:04` uh we can connect that to information
<br>`15:06` about the planes
<br>`15:07` yeah and we can also get information
<br>`15:10` about the airlines if you want
<br>`15:12` yeah and that's how we what we do yes we
<br>`15:15` reload
<br>`15:16` again just like last time where we load
<br>`15:19` again
<br>`15:20` all of these different files using the
<br>`15:23` function f
<br>`15:23` read and then we merge them together
<br>`15:27` using these merge commands and when we
<br>`15:30` merge them together we sometimes have to
<br>`15:32` give for example when we merge with the
<br>`15:35` planes
<br>`15:36` or let me see here for example when we
<br>`15:38` move with the airports that we merge
<br>`15:41` with the airports we have to say that
<br>`15:43` here the airport identifier is in the
<br>`15:46` column origin
<br>`15:48` and here the airport identifier is in
<br>`15:51` the column
<br>`15:52` faa now so we motor all of these things
<br>`15:56` together and we have a huge data set
<br>`15:58` a data table containing all of these
<br>`16:01` information line by line and
<br>`16:04` in a tiny format we already did that two
<br>`16:08` weeks ago
<br>`16:10` now let's have a simple look at these
<br>`16:13` plots let's just let's say let's have a
<br>`16:15` simple plot

### slide 8

<br>`16:16` and the first thing we can do is uh like
<br>`16:19` just like last time we can calculate
<br>`16:22` the average delay
<br>`16:27` for each month so we group the data by
<br>`16:29` month
<br>`16:31` and for each month we take the average
<br>`16:35` over all departure delays and save that
<br>`16:39` average
<br>`16:39` in the column mean delay
<br>`16:42` now so what we don't get is that for
<br>`16:44` each month
<br>`16:46` here in the first column we get a mean
<br>`16:49` departure delay this is the second
<br>`16:51` column
<br>`16:52` and below you can see now the simple
<br>`16:54` spot you can do you can
<br>`16:56` tell this ggplot function to take this
<br>`17:00` table
<br>`17:01` now a very simple table and map
<br>`17:04` the month to the x-axis and the delay to
<br>`17:08` the y-axis
<br>`17:10` and then you just add a geometry
<br>`17:13` which is just a point then you get what
<br>`17:16` you see on the right-hand side
<br>`17:18` and you see that something is happening
<br>`17:20` here in this summer months
<br>`17:22` and something is happening over
<br>`17:24` christmas apparently
<br>`17:26` okay
<br>`17:31` so okay there's something something in
<br>`17:33` the waiting room right
<br>`17:35` okay so something is happening over
<br>`17:37` christmas now let's go on

### slide 9 & 10: different types

<br>`17:40` uh we can of course also add different
<br>`17:42` geometries to a plot
<br>`17:44` yeah so these different geometries so we
<br>`17:46` just use the geometry
<br>`17:49` of a line now of a point we can also add
<br>`17:52` different geometries
<br>`17:54` and for the sake of simplicity what i'm
<br>`17:56` doing here i'm using the tools that i
<br>`17:58` introduced two weeks ago
<br>`18:01` not to do all of these things in one
<br>`18:03` line so we take the flights
<br>`18:06` data set calculate for each month the
<br>`18:08` average delay
<br>`18:11` and send everything with this pipe
<br>`18:14` operator here
<br>`18:16` to the g plot and in the g
<br>`18:19` plot we just need to define that this
<br>`18:22` aesthetic mapping
<br>`18:23` that the x coordinate is the month and
<br>`18:25` the y coordinate
<br>`18:27` is the delay and we save this everything
<br>`18:31` we just save in an object g on the left
<br>`18:34` hand side
<br>`18:36` and now we can take this g and add
<br>`18:38` different things to it
<br>`18:39` we can add different geometries on the
<br>`18:41` left here top left we have the
<br>`18:44` the point as before we can add a
<br>`18:47` geometry line
<br>`18:48` now then we get a line we can add a bar
<br>`18:52` that's called column we can add a bar
<br>`18:55` or we can add all of them together to
<br>`18:58` the plot
<br>`18:59` and then we have all of them together
<br>`19:01` this information of what
<br>`19:03` what happens with the data that's not
<br>`19:06` done in the geometry that's we have done
<br>`19:08` once in the beginning and now we can
<br>`19:10` just operate on this object and add
<br>`19:12` different things and change the part the
<br>`19:14` way we like it
<br>`19:18` yeah so there are also geometries that
<br>`19:21` are
<br>`19:21` that involve analysis now for example uh
<br>`19:25` if you have a background in biology
<br>`19:27` maybe then you know your favorite
<br>`19:29` dot box plot on the right hand side that
<br>`19:32` summarizes
<br>`19:33` different uh properties of the
<br>`19:36` statistical distribution
<br>`19:38` for example here in the left hand side i
<br>`19:41` take the flights
<br>`19:42` all this combined information i take it
<br>`19:46` use the x the carrier as the x
<br>`19:48` coordinate
<br>`19:49` and the logarithm of the departure delay
<br>`19:52` as the y-coordinate
<br>`19:53` and i add this box plot where i have
<br>`19:56` automatically
<br>`19:57` the median and this is some
<br>`20:01` inter-quarter range and then i
<br>`20:04` always forget uh forget what this means
<br>`20:06` is probably the range of the data
<br>`20:08` without
<br>`20:08` outliers or so now that's basically in
<br>`20:11` some disciplines these box plots are
<br>`20:13` used to characterize distributions
<br>`20:15` another way to characterize
<br>`20:17` distributions are violence
<br>`20:19` violent plots that essentially give you
<br>`20:22` a plot of the probability distribution
<br>`20:24` here
<br>`20:25` um just in a vertical manner the thicker
<br>`20:29` the violin is
<br>`20:30` the more the the higher the probability
<br>`20:32` to find a data point
<br>`20:34` there yeah and

### slide 11 & 12: aesthetic

<br>`20:37` uh so of course we can now also play
<br>`20:40` with
<br>`20:40` how these plots look like so
<br>`20:43` for example now i'm and if you look at
<br>`20:46` the red
<br>`20:47` i'm doing the same operation yeah i'm
<br>`20:50` calculating the average departure delay
<br>`20:54` for each month and each airport and each
<br>`20:57` carrier
<br>`20:58` but now i'm just for simplicity i only
<br>`21:01` take the big
<br>`21:02` three carriers united airlines delta and
<br>`21:04` american airlines
<br>`21:07` and now i create this plot again now i
<br>`21:09` have this aesthetic mapping
<br>`21:12` the month should be the x coordinate the
<br>`21:14` delay the y coordinate
<br>`21:16` and now i have another aesthetic which
<br>`21:19` is the color
<br>`21:20` i say the color should be the origin
<br>`21:23` airport
<br>`21:25` and the line type line type should
<br>`21:27` correspond to the carrier
<br>`21:30` and now i just add the geometry the line
<br>`21:32` and i get this plot that you see on the
<br>`21:34` bottom here
<br>`21:36` you can see that all carriers have a
<br>`21:38` problem in the summer month
<br>`21:40` and also in the over christmas you know
<br>`21:43` except for america so something is going
<br>`21:46` on with american
<br>`21:47` airlines around march uh no idea what
<br>`21:50` this is
<br>`21:52` yeah and uh
<br>`21:55` no wait that's not american airlines now
<br>`21:56` that that's new arc
<br>`21:58` newark american airlines has a problem
<br>`22:01` in march
<br>`22:02` yeah you see it's not the problem the
<br>`22:04` plot is not perfect yet
<br>`22:06` and uh okay so we can go on now we can
<br>`22:09` add
<br>`22:10` other aspect we can change other experts
<br>`22:13` of the plot
<br>`22:14` for example i here say that the film
<br>`22:18` should be the airport and then i use a
<br>`22:21` box plot
<br>`22:22` and then i get an overview over how the
<br>`22:25` difference
<br>`22:26` airport the airports the different
<br>`22:27` airports compared to each other
<br>`22:30` for each carrier and what you can see
<br>`22:34` is that jfk is doing well for
<br>`22:37` some of them but not for all
<br>`22:40` you know american airline and for united
<br>`22:43` and
<br>`22:44` and what is it where is it delta is
<br>`22:46` doing well
<br>`22:48` um but there is no clear trend here of
<br>`22:50` course

### slide 13: subplots

<br>`22:52` something that's more interesting is if
<br>`22:54` you plot these delays
<br>`22:57` for the big three carriers yeah
<br>`23:00` uh as a as a function of the hour of the
<br>`23:04` day
<br>`23:06` yeah so here the x-axis the x-coordinate
<br>`23:09` is the hour and i turn that into a
<br>`23:12` factor
<br>`23:13` from numeric to something that is
<br>`23:16` discrete just for plotting purposes
<br>`23:19` the the fill color is the origin airport
<br>`23:24` and i added here a
<br>`23:27` subplot now that's called a facet
<br>`23:30` by carrier if you remember the two
<br>`23:34` lectures ago this is a formula we can
<br>`23:36` use a formula in r
<br>`23:37` to specify how plots are distributed
<br>`23:40` across different subplots
<br>`23:42` and you can see that for a delta and
<br>`23:44` united airlines
<br>`23:46` you can nicely see how these delays
<br>`23:49` add up during the day
<br>`23:52` yeah and yeah and it looks a little bit
<br>`23:54` even that is
<br>`23:56` let's have a look at the next slide

### slide 14

<br>`23:58` maybe uh let's
<br>`23:59` have a look at the next slide so if we
<br>`24:01` can have also more complicated subplots
<br>`24:04` yeah so for example we have we can have
<br>`24:06` a grid
<br>`24:07` by using a more complicated formula
<br>`24:10` where the
<br>`24:11` y-axis yeah the y-direction should be
<br>`24:13` the origin
<br>`24:14` and the x-direction in this grid should
<br>`24:17` be the carrier
<br>`24:18` yeah and then we got these plots and you
<br>`24:21` can see
<br>`24:21` how you can actually see how these
<br>`24:23` delays
<br>`24:25` add up during the day and it seems like
<br>`24:28` a little bit yeah it's a speculation
<br>`24:30` but because we have a logarithm in the
<br>`24:32` y-axis
<br>`24:34` and we have linear linear increase
<br>`24:37` over time uh in these delays
<br>`24:41` uh over over time during the day that
<br>`24:44` you have an exponential
<br>`24:45` build up of delays now that's quite
<br>`24:47` quite interesting

### slide 15: plot of 3 variables

<br>`24:49` yeah okay so we can do all those kind of
<br>`24:53` other fancy thing we can if you have
<br>`24:55` more than two variables
<br>`24:57` now for example when we calculate the
<br>`24:59` average delay
<br>`25:02` as a function of the month the hour and
<br>`25:05` the origin
<br>`25:05` airport yeah then we have more than
<br>`25:09` we have then we have then even more
<br>`25:11` variables that we want to visualize
<br>`25:14` uh we can do that for example with such
<br>`25:16` something that's called a heat map
<br>`25:19` yeah and this heat map here the
<br>`25:24` the the fill and also the color of these
<br>`25:27` tiles
<br>`25:28` is given by the mean delay
<br>`25:31` while the month and the hour are plotted
<br>`25:34` on these axes here
<br>`25:36` then we add the geometry of the tile to
<br>`25:39` get these heat maps
<br>`25:41` then you can visualize relationships
<br>`25:44` between two variables namely month
<br>`25:47` and hour and it seems like this buildup
<br>`25:51` of delays is specifically drastic at the
<br>`25:54` summer months
<br>`25:56` while it's not that evident in other
<br>`25:58` months

### question on assigning facet

<br>`26:02` excuse me i have a question syntax
<br>`26:06` in this where you've written facet
<br>`26:10` underscore rap the first argument tells
<br>`26:13` us
<br>`26:13` the x argument and so origin will be
<br>`26:16` plotted on the x scale
<br>`26:18` yes so so this facet rep
<br>`26:21` is just to say okay take
<br>`26:25` one column of the data table yeah it is
<br>`26:28` already in this case origin
<br>`26:31` and group the data according to this
<br>`26:33` column your origin
<br>`26:35` and then make one plot for each of these
<br>`26:39` origin
<br>`26:40` airports and put them next to each other
<br>`26:44` as many as fit on the screen
<br>`26:47` now and if they don't fit on the screen
<br>`26:48` go to the next line
<br>`26:50` it's basically just this wrap what i'm
<br>`26:53` saying here is that you have a
<br>`26:54` one-dimensional so to say
<br>`26:56` line of plots uh compared to this grip
<br>`26:59` that is
<br>`27:00` this grid here where was that yeah this
<br>`27:03` grid
<br>`27:04` is the same thing it's basically the
<br>`27:06` same thing
<br>`27:07` uh so here we have these two coordinates
<br>`27:10` now these two
<br>`27:11` directions origin airport on the on the
<br>`27:14` y direction
<br>`27:17` and carrier on the x direction
<br>`27:20` now this is this this formula notation
<br>`27:22` and r
<br>`27:23` yeah so that's it's a little bit counter
<br>`27:25` intuitive but you give it a formula
<br>`27:28` uh in order to uh to to tell
<br>`27:32` r how all this this package how these
<br>`27:34` plots should be distributed
<br>`27:36` on your screen or on the on the in the
<br>`27:38` pdf file that you export
<br>`27:41` yeah and you can if you want you can use
<br>`27:46` the reason why the formula i used here
<br>`27:48` is that you could do something here
<br>`27:51` that you have here carrier plus
<br>`27:54` for example um what are we plotting here
<br>`28:00` carrier plus uh um
<br>`28:04` month or so yeah you can have here
<br>`28:08` uh if you do something like this
<br>`28:12` you can have more complicated formula
<br>`28:15` to say that a combination of carrier and
<br>`28:19` month of these two columns
<br>`28:21` should be on the x direction here
<br>`28:27` and on the y direction you have origin
<br>`28:30` now you can
<br>`28:30` you can construct more complicated
<br>`28:34` grids of plots if you wanted to
<br>`28:37` it's very often that's not very useful
<br>`28:40` and
<br>`28:41` just think about that that this is
<br>`28:43` what's on the uh
<br>`28:46` that was my that was my question because
<br>`28:48` in the next slide the
<br>`28:50` original argument the origins have been
<br>`28:52` plotted on the x
<br>`28:53` scale whereas in this particular case
<br>`28:55` the original airport has been plotted
<br>`28:56` along the y scale
<br>`28:59` so now i exactly so now i'm trying to
<br>`29:02` get my mouse cursor back is here
<br>`29:06` so okay now i can change the slide
<br>`29:08` hopefully
<br>`29:10` okay here we go so here i just left away
<br>`29:14` the first argument
<br>`29:17` and i left the the left one so that was
<br>`29:20` originally the y
<br>`29:21` direction and now i only have the x
<br>`29:24` direction left you know from left to
<br>`29:26` right
<br>`29:28` and i use here wrap and not grid because
<br>`29:30` i want
<br>`29:31` this these plots if i have not
<br>`29:34` three but like 15 different groups
<br>`29:38` i don't want them to be all in the same
<br>`29:40` line because i wouldn't be able to see
<br>`29:41` them on the screen
<br>`29:43` rep means once the screen is full go to
<br>`29:46` the next line
<br>`29:47` yeah nothing else that's not it's not a
<br>`29:50` complicated thing here let's just
<br>`29:52` just just make each plot for each origin
<br>`29:55` one plug for each origin
<br>`29:57` excuse me yes uh on this heat map
<br>`30:00` the color bar the minimum value is not
<br>`30:03` zero
<br>`30:05` does it mean that yes yes
<br>`30:08` rights that departed earlier than
<br>`30:10` scheduled
<br>`30:13` yes there are yes exactly exactly they
<br>`30:16` departed earlier oh
<br>`30:19` it's not very funny for the passengers
<br>`30:22` yes so so but but sometimes that happens
<br>`30:25` and it also it's also a question how the
<br>`30:27` data is recorded
<br>`30:29` um depends on how the data is recorded
<br>`30:33` so especially so this is position
<br>`30:37` specifically affects the early mornings
<br>`30:40` right and the very late times
<br>`30:44` now so this negative is negative
<br>`30:45` departure delays
<br>`30:47` um i mean that sometimes that can happen
<br>`30:51` you know so sometimes
<br>`30:52` the question is when that's not the time
<br>`30:56` when the gates close
<br>`30:58` uh it's probably the time when the
<br>`31:00` airplane starts or something like this
<br>`31:04` yeah and as you as you know if the
<br>`31:06` boarding is
<br>`31:07` so very often it happens that that once
<br>`31:09` boarding is completed
<br>`31:11` the the airport they will sometimes the
<br>`31:14` airplane leaves a little bit earlier
<br>`31:15` than uh than the schedules
<br>`31:18` okay thanks but as always there's a good
<br>`31:22` thing
<br>`31:22` it's always good to to to know how the
<br>`31:24` data was actually collected
<br>`31:26` now you think that a delay is well
<br>`31:28` defined but then you can
<br>`31:29` measure this in different ways yeah
<br>`31:32` that's always a very important aspect
<br>`31:34` aspect and here are also this data set
<br>`31:37` they're also
<br>`31:37` missing missing numbers a lot of missing
<br>`31:41` numbers
<br>`31:41` and that's when an airport started
<br>`31:44` somewhere but didn't end up on its
<br>`31:47` rival location but it's on other
<br>`31:49` airports yeah so that's also
<br>`31:51` that's also possible

### slide 16: error bar

<br>`31:54` okay so let's uh go on just uh
<br>`31:58` so we can also use uh gg plot you have
<br>`32:01` to do statistical computations
<br>`32:03` on the fly and this is uh particularly
<br>`32:06` useful for computating
<br>`32:08` fancy error bars that's that's
<br>`32:11` how i use it and so what
<br>`32:15` we can do for example here on the top is
<br>`32:18` that
<br>`32:19` we have the hour on the x-axis the
<br>`32:22` departure delay
<br>`32:24` on the y-axis and then
<br>`32:27` color and uh and fill as the origin
<br>`32:30` airport and then for each of these
<br>`32:33` combinations because we take on the left
<br>`32:35` and raw data
<br>`32:36` now we have many different values we
<br>`32:38` have many different flights
<br>`32:40` and we can then take just a summary
<br>`32:43` function
<br>`32:44` statistical summary function from the
<br>`32:46` gdg plot
<br>`32:48` tell this function to calculate the mean
<br>`32:53` and use the geometry of a line
<br>`32:56` to do the computation for us yeah so for
<br>`32:59` so simple things like the mean
<br>`33:00` calculation
<br>`33:01` that's pretty good but the nice thing is
<br>`33:03` that we can also do
<br>`33:05` uh summary functions that are more
<br>`33:08` complicated yeah for
<br>`33:10` example in this here we have a
<br>`33:11` bootstrapping
<br>`33:13` confidence intervals yeah that's that's
<br>`33:16` basically a fancy way of calculating
<br>`33:18` confidence intervals
<br>`33:20` and we use a geometry of a written
<br>`33:23` not to visualize these confidence
<br>`33:25` intervals
<br>`33:27` and if you deal with confidence
<br>`33:28` intervals you know that's quite
<br>`33:30` complicated to calculate and then you
<br>`33:32` somehow have to bring them into your
<br>`33:33` plot
<br>`33:34` so here you don't have to worry about
<br>`33:36` this you have the most fancy methods
<br>`33:37` just
<br>`33:38` uh in one line and you get a nice
<br>`33:41` visualization of the uncertainty of your
<br>`33:43` data
<br>`33:45` another thing we can do is also here in
<br>`33:47` this upper case our
<br>`33:49` x-axis is discrete because it's an hour
<br>`33:52` from from 0 to 24
<br>`33:55` or 23 or 5 to 23
<br>`33:58` but sometimes we have real number values
<br>`34:01` yeah and then we need to tell
<br>`34:03` these functions which values to put
<br>`34:06` together that means we can
<br>`34:07` bin the data an example here is the
<br>`34:10` temperature
<br>`34:11` in fahrenheit on the
<br>`34:15` x-axis and we cannot calculate for every
<br>`34:19` value of the temperature
<br>`34:21` uh we cannot calculate a separate mean
<br>`34:23` yeah because temperature is a real value
<br>`34:25` it's uh
<br>`34:27` a real valued uh quantity
<br>`34:30` yeah and we we need to define a bin to
<br>`34:33` summarize values of the temperature
<br>`34:36` and that we can do automatically also
<br>`34:38` with these start summary bin
<br>`34:40` functions where we just calculate
<br>`34:43` we just tell the function to bin the
<br>`34:45` data
<br>`34:47` and for each of these bins again
<br>`34:48` calculate the mean
<br>`34:50` and plot the result with the geometry of
<br>`34:53` a nine
<br>`34:54` and we can do the same fancy arrow bars
<br>`34:57` and confidence interval calculations
<br>`34:59` as before and also you know probably
<br>`35:03` that
<br>`35:03` these kind of processes are quite
<br>`35:05` complicated if you have to do them
<br>`35:07` yourself
<br>`35:10` and here probably the the me the the
<br>`35:12` message is that it's
<br>`35:14` not good if it's too cold or too hot
<br>`35:18` but then there are correlations right so
<br>`35:21` when it's hot here in on the right hand
<br>`35:25` side
<br>`35:25` there's also when the holidays take
<br>`35:27` place yeah that's july
<br>`35:29` and june yeah in these previous heat
<br>`35:32` maps
<br>`35:33` where we had these delays yeah so it's
<br>`35:35` not
<br>`35:36` it's not quite quite clear whether it's
<br>`35:38` the temperature that's bad for the for
<br>`35:40` the engines or something like this
<br>`35:42` or whether it's just the number of
<br>`35:44` people that
<br>`35:45` go on holiday and block the airport
<br>`35:48` and lead to delays there

### slide 17: interpolation

<br>`35:53` now we can do even more fancy things now
<br>`35:55` we can do
<br>`35:56` interpolation yeah on the right and the
<br>`35:59` left hand side you know i just
<br>`36:00` uh had the same plot as before
<br>`36:04` we had um yeah we have the month
<br>`36:08` wait okay here's a little error the hour
<br>`36:11` on the x-axis
<br>`36:13` and we do as the hour on the x-axis
<br>`36:17` yeah and now we can add like an
<br>`36:19` interpolation line
<br>`36:20` just in one line with this summary
<br>`36:23` function
<br>`36:24` and if we wanted to we would be able to
<br>`36:26` do like
<br>`36:27` non-linear interpolation linear
<br>`36:29` interpolation or anything we want just
<br>`36:31` with an argument
<br>`36:33` and we get our usual nice error bars for
<br>`36:36` free
<br>`36:38` of course if we can do non-linear fits
<br>`36:40` we can also do linear fits so we can fit
<br>`36:42` linear models to check for correlations
<br>`36:45` and that's what we do on the right hand
<br>`36:47` side and on this right hand side
<br>`36:50` what is actually quite interesting here
<br>`36:53` is that on the x-axis we have the month
<br>`36:56` on the y-axis we have the number of
<br>`36:59` seats
<br>`37:00` in an airplane and the color
<br>`37:04` is the origin airport
<br>`37:07` now what we find here is that there's a
<br>`37:09` perf almost perfect linear relationship
<br>`37:12` between the month and the number of
<br>`37:14` seats
<br>`37:15` yeah there's a perfect linear
<br>`37:16` relationship which is positive
<br>`37:20` for the for new arc and
<br>`37:23` jfk and uh
<br>`37:26` negative for lga which is i think
<br>`37:29` laguardia
<br>`37:30` yeah so no idea where this comes from
<br>`37:33` yeah but apparently you are sitting
<br>`37:37` in december in a smaller plane
<br>`37:40` higher likelihood to sit in a smaller
<br>`37:42` plane in december
<br>`37:44` if you are departing from laguardia
<br>`37:47` while the planes get larger
<br>`37:50` throughout the linearly larger
<br>`37:52` throughout the year
<br>`37:54` for some reason yeah so that's that's
<br>`37:56` one of these
<br>`37:57` one of these things where you should be
<br>`37:58` suspicious and check what is actually
<br>`38:01` the underlying
<br>`38:02` reasoning for this data yeah so so
<br>`38:05` that's that's something i will show you
<br>`38:06` also later
<br>`38:07` is that it's very important to check
<br>`38:10` whether
<br>`38:10` when you do statistical computations
<br>`38:12` whether they actually make sense or not
<br>`38:14` yeah big data gives you every result
<br>`38:18` that you want if you just look for it
<br>`38:21` now just because you have so many
<br>`38:23` dimensions so many samples you can
<br>`38:25` find every hypothesis you want in these
<br>`38:28` data sets
<br>`38:29` if you just keep looking for it

### slide 18: scales

<br>`38:33` yeah so we can play around with scales
<br>`38:36` yeah so that means that we can change
<br>`38:38` how our plots look like for example
<br>`38:42` uh in this plot here on the top that's
<br>`38:44` something we have shown
<br>`38:45` seen before that's the box plot we save
<br>`38:48` this
<br>`38:48` in a variable p now and now you see how
<br>`38:51` i this weird arrow assignment operator
<br>`38:55` in
<br>`38:55` r why why why why the r community
<br>`39:00` likes that you can have that you can
<br>`39:02` assign in the different direction
<br>`39:03` right so i have the plot and i assign
<br>`39:06` the results to a variable p
<br>`39:09` and that's not something so it's it's an
<br>`39:12` asymmetric
<br>`39:12` assignment and so now we have our plot
<br>`39:16` and we can add different
<br>`39:18` color scales and we can add different
<br>`39:20` ways of how our data values
<br>`39:23` map to visual characteristics of the
<br>`39:26` plot
<br>`39:28` for example we can add a new scale score
<br>`39:31` for some scale color blur then we get
<br>`39:33` different
<br>`39:34` blue tones we can also add
<br>`39:38` like a manual mapping where we say that
<br>`39:42` the uwt
<br>`39:43` want to have black gray and white as the
<br>`39:45` colors for our airports

### slide 19: positions

<br>`39:48` now so we can add change visual
<br>`39:50` characteristics and we can also change
<br>`39:52` of course how things are positioned
<br>`39:56` relative to each other yeah and i'll go
<br>`40:00` quickly over this because that's a
<br>`40:01` little bit of a detail
<br>`40:03` yeah so we have for example we can
<br>`40:05` create this uh plot here on the right
<br>`40:07` hand side
<br>`40:08` where we for each plot for each month
<br>`40:12` origin and carrier carrier calculate the
<br>`40:16` average delay
<br>`40:17` for the three carriers and then we can
<br>`40:20` make a plot
<br>`40:23` where we assign the month to the x-axis
<br>`40:25` now to the white
<br>`40:27` the delay to the y-axis the fill
<br>`40:30` color to the origin airport
<br>`40:34` and the transparency of this color
<br>`40:37` to the carrier yeah and then first
<br>`40:41` we can now plot all of this using a bar
<br>`40:44` plot
<br>`40:45` and if we have a bar plot we can decide
<br>`40:47` how to
<br>`40:48` put these bars relative to each other
<br>`40:51` and i'll just
<br>`40:52` give you three examples we can stack
<br>`40:55` them on top of each other
<br>`40:56` that's on the right hand side
<br>`40:59` now we can dodge them
<br>`41:02` that means that we put them next to each
<br>`41:05` other that's in the middle
<br>`41:07` and we can use a fill
<br>`41:10` position that means we always fill them
<br>`41:13` up to one
<br>`41:14` that means we look at the fraction that
<br>`41:16` a certain carrier
<br>`41:17` and origin airport contribute
<br>`41:21` to the total delays and
<br>`41:24` uh let me just see if there's any
<br>`41:28` yeah you can see here for example so
<br>`41:30` that that
<br>`41:32` that that here for example a large
<br>`41:35` fraction of the delays in march
<br>`41:37` comes actually from this newark airport
<br>`41:41` uh while other months uh for example in
<br>`41:44` the summer month
<br>`41:45` the larger fraction of the lace actually
<br>`41:47` comes from the other airports
<br>`41:49` um jfk and lga
<br>`41:53` yeah we can also do something

### slide 20: corrdinate system

<br>`41:56` we can also change how the data is
<br>`42:00` how we can change the coordinate system
<br>`42:02` you know so now we always assume that we
<br>`42:04` have
<br>`42:04` cartesian coordinates but we can of
<br>`42:06` course have any other coordinate system
<br>`42:09` so here for example we are plotting uh
<br>`42:12` as the x-coordinate the wind direction
<br>`42:16` as the y coordinate the departure delay
<br>`42:20` and then we just calculate the average
<br>`42:22` delay
<br>`42:23` again using the summary function
<br>`42:27` for a certain certain intervals of the
<br>`42:30` wind direction
<br>`42:33` yeah and we can then plot that for
<br>`42:35` example in different ways
<br>`42:38` um we can plot that of course in
<br>`42:41` cartesian co-coordinates
<br>`42:43` something that's more instructive is
<br>`42:45` actually when we talk about
<br>`42:46` directions is to use polar coordinates
<br>`42:50` yeah and you can see that i do that just
<br>`42:53` with one adding just one line
<br>`42:54` one more rule to the plot
<br>`42:58` and now i can add more
<br>`43:01` aesthetic mappings for example i can
<br>`43:03` separate
<br>`43:04` as before these different contributions
<br>`43:07` from the wind direction
<br>`43:09` by airport and this is what i've done
<br>`43:11` here i just added one more aesthetic
<br>`43:13` mapping here
<br>`43:15` i said that these bars should be next to
<br>`43:18` each other and not on top of each other
<br>`43:20` or so
<br>`43:21` and i have the polar coordinates as
<br>`43:23` before
<br>`43:24` yeah then you get the plot that you have
<br>`43:26` on the right hand side
<br>`43:28` and in this plot what you see
<br>`43:31` is that there is a relation with the
<br>`43:33` wind direction
<br>`43:35` of the departure delays specifically
<br>`43:38` when the wind
<br>`43:39` comes from what is that southwest
<br>`43:43` a little southwest west for the two
<br>`43:46` airports
<br>`43:47` uh lga
<br>`43:50` and newark you know whatever is the
<br>`43:53` reason for that
<br>`43:54` it's actually for all of them yes and
<br>`43:56` actually for all of them
<br>`43:58` uh it's actually for all of them
<br>`44:01` but it's specifically strong for lga and
<br>`44:04` new arc
<br>`44:05` and if you look at the location of new
<br>`44:07` york that's where the sea is
<br>`44:09` that's probably also where a lot of the
<br>`44:11` wind
<br>`44:13` the strong winds come from from this
<br>`44:15` direction
<br>`44:16` yeah okay yeah this was just playing
<br>`44:19` around with the data
<br>`44:20` and you get some some insights
<br>`44:23` from just looking visualizing the data
<br>`44:27` and these insights are of course much
<br>`44:29` harder to get if you just look at data
<br>`44:31` tables on the console as we did two
<br>`44:34` weeks ago
<br>`44:35` and what you can also see here if you
<br>`44:38` create such plots
<br>`44:40` yeah so you can make more and more
<br>`44:42` complicated plots
<br>`44:44` but the complexity of your code
<br>`44:47` never changes yeah it does only
<br>`44:50` increases just linearly because you're
<br>`44:51` adding just one bit by bit
<br>`44:53` to your plot one layer by layer to your
<br>`44:56` plot and you can make
<br>`44:57` as complicated plots as you want
<br>`45:00` from this now without adding
<br>`45:04` more and more complexity actually to
<br>`45:06` your code or with
<br>`45:07` without requiring requiring more and
<br>`45:11` more specialized
<br>`45:12` functions and that is the advantage of
<br>`45:17` having such a
<br>`45:19` grammar of graphics now that allows you
<br>`45:21` to to have simple rules
<br>`45:23` uh that visual rules that allow you to
<br>`45:26` add more and more components to a plot
<br>`45:29` and then of course we can make these
<br>`45:31` plots look

### slide 21

<br>`45:32` nice yeah we can add things like
<br>`45:35` axis labels for all of our columns
<br>`45:39` typically you get a data table that is
<br>`45:42` that where some experimentalist has used
<br>`45:45` their own notation for things
<br>`45:47` doesn't make much sense most of the time
<br>`45:49` you want to have your own
<br>`45:51` um you want to have your own uh
<br>`45:54` um names for the for the x's and for the
<br>`45:57` colors and for the
<br>`45:58` for the legends and uh specifically
<br>`46:01` including units if you want to publish
<br>`46:03` that and then you can do that easily
<br>`46:06` with this labs command and there's also
<br>`46:09` a title command if you want
<br>`46:11` here you can add a title and
<br>`46:14` annotate your plot as much as you want

### slide 22: extensions

<br>`46:17` and then you can get as complicated as
<br>`46:21` you want you can
<br>`46:22` download extensions for example some
<br>`46:25` nice extensions add
<br>`46:26` new geometries and new coordinate
<br>`46:29` systems to these plots
<br>`46:31` so here these uh plots that are used in
<br>`46:33` anatomy
<br>`46:34` they add the human body and mouse body
<br>`46:37` coordinate systems
<br>`46:38` and you can then easily without adding
<br>`46:40` having more complexity
<br>`46:42` than what i already showed you you can
<br>`46:45` have visualize your data
<br>`46:49` that you for example imaging data on the
<br>`46:52` mouse or
<br>`46:53` human body or whatever you want to do
<br>`46:55` now that looks like
<br>`46:56` a ton of different extensions to this
<br>`47:00` okay so this is a very efficient way of
<br>`47:02` visualizing data

### slide 23: there is also python implementation

<br>`47:03` that relies on a grammar or a set of
<br>`47:06` rules
<br>`47:07` i showed you an r implementation but
<br>`47:09` there's also a python implementation
<br>`47:12` and the python implementation is rather
<br>`47:14` new so it's just
<br>`47:16` i don't know what quality this is and
<br>`47:20` what we now want to do
<br>`47:24` is i want to uh
<br>`47:28` i want to show you how to use these
<br>`47:31` tools that we
<br>`47:33` that we've seen in the last couple of
<br>`47:34` lectures in a specific

> The following slides are nowhere found in the slides shared on the course website. The lecturer went through the jupyter notebook about a RNA sequencing project. 

<br>`47:37` data science project and for this we'll
<br>`47:40` just
<br>`47:41` go through the code of a real data
<br>`47:43` science project and this is a project
<br>`47:45` that fabian actually did
<br>`47:47` while he was in the group and the
<br>`47:50` uh starting point of this project
<br>`47:54` is a so-called sequencing experiment now
<br>`47:57` so i've already showed you this table
<br>`47:59` and here on the x-axis yeah
<br>`48:02` on the the color the rows in such an
<br>`48:05` experiment
<br>`48:06` on such that that look that would be so
<br>`48:08` to say a matrix that
<br>`48:10` experimentalists would send you so here
<br>`48:13` every row
<br>`48:14` is a different gene and every column is
<br>`48:20` a different cell
<br>`48:21` now we have now maybe then twenty
<br>`48:23` thousand cells thirty seven thousand
<br>`48:25` cells
<br>`48:26` and for each of these cells we have
<br>`48:29` roughly
<br>`48:30` ten thousand measurements yeah and
<br>`48:33` these measurements correspond to how
<br>`48:36` strongly
<br>`48:38` uh a certain gene yeah that's on the
<br>`48:42` in the row here is expressed in this
<br>`48:45` particular cell so these numbers here
<br>`48:47` correspond to how many products of these
<br>`48:50` genes these experimental techniques
<br>`48:53` found in a given cell yeah and the way
<br>`48:56` and these genes
<br>`48:57` you might hurt they tell us a lot about
<br>`49:00` what cells are doing and how they're
<br>`49:02` behaving and what kind of cells they are
<br>`49:04` so they're very important
<br>`49:06` molecular measurements of what's going
<br>`49:09` on inside cells now so for example here
<br>`49:13` this gene now that has this id here
<br>`49:16` that's a cryptic name and row four
<br>`49:20` is not expressed it has a little bit
<br>`49:23` information in this particular cell but
<br>`49:26` not in other cells
<br>`49:27` what other genes like this one here have
<br>`49:30` very
<br>`49:31` high expression values they have very
<br>`49:34` high counts of products from these genes
<br>`49:38` that were detected in these experiments
<br>`49:42` so what i have to tell you is that these
<br>`49:44` experiments are extremely messy
<br>`49:47` yeah so so especially there are there is
<br>`49:49` a step where
<br>`49:50` ex the data is exponentially amplified
<br>`49:54` and that exponentially amplifies errors
<br>`49:57` in these data sets so it's a
<br>`50:00` it's a big mess yeah and now we have to
<br>`50:02` find some structure
<br>`50:05` in these simple in this high dimensional
<br>`50:08` data set in these
<br>`50:10` genomics experiments and to show you how
<br>`50:13` this is working i'll share another file
<br>`50:19` um i'll share another screen
<br>`50:22` [Music]
<br>`50:24` where are we
<br>`50:28` here
<br>`50:31` here we go now i'll just give you a uh
<br>`50:34` like a hands-on look and
<br>`50:37` on how this actually works yeah i don't
<br>`50:40` tell you too much about the biological
<br>`50:43` background in this project because it's
<br>`50:45` not yet published
<br>`50:47` um so um can you see you can you should
<br>`50:50` be able to see
<br>`50:51` the browser right
<br>`50:54` and you can see that this here is
<br>`50:57` actually a combination
<br>`51:00` of python yeah the first block
<br>`51:03` and r yeah so this here
<br>`51:07` here he's loading some r packages
<br>`51:10` and here he's loading python packages
<br>`51:13` and all of this is a jupyter notebook
<br>`51:15` yeah so yeah combining r and python to
<br>`51:18` take the best of both worlds
<br>`51:23` yeah and then we then there's a lot of
<br>`51:25` data loading going on
<br>`51:27` yeah so i'll just go through of course
<br>`51:29` we don't have to look in detail how the
<br>`51:31` data is loaded
<br>`51:32` uh some some biological background
<br>`51:35` information about what
<br>`51:36` different genes are doing and
<br>`51:40` so on yeah and now
<br>`51:45` we start with the pre-processing of the
<br>`51:48` data
<br>`51:49` so as total that this data is messy
<br>`51:53` and this data has like
<br>`51:56` 80 percent nonsensical
<br>`52:00` the nonsensical information in other
<br>`52:03` words this is dominated by
<br>`52:05` technical noise our technical noise is
<br>`52:08` extremely strong
<br>`52:10` and it gives rise to very weird results
<br>`52:13` so the first step we always have to do
<br>`52:16` and this
<br>`52:17` particular example in genomics but also
<br>`52:19` in other data sets
<br>`52:20` is we have to look at the data and and
<br>`52:23` polish it in a way so that we can are
<br>`52:27` actually in principle able
<br>`52:29` to detect information here
<br>`52:34` so for example this plot here on the top
<br>`52:38` shows you basically what is the
<br>`52:40` percentage
<br>`52:42` of all information in a cell
<br>`52:46` that goes to certain genes yeah they
<br>`52:48` have these weird names they're
<br>`52:49` completely
<br>`52:50` irrelevant but you see that this gene on
<br>`52:53` the top here
<br>`52:54` that has an even weirder name
<br>`52:57` in some cell comprises eighty percent of
<br>`53:00` the
<br>`53:02` information yeah and that
<br>`53:05` does not make any biological sense but
<br>`53:08` because if you have
<br>`53:09` thirty thousand genes in a cell it can't
<br>`53:11` be that basically the cell
<br>`53:13` is packed completely packed with
<br>`53:15` products from a single gene you know
<br>`53:17` that that's
<br>`53:17` cannot happen in real life and that's
<br>`53:20` why we see that here there are a lot of
<br>`53:22` cells
<br>`53:23` yeah so everything where we have more
<br>`53:25` than maybe 30 percent here
<br>`53:27` where we don't have any reasonable
<br>`53:31` information now that means that we need
<br>`53:34` to do quality control now we
<br>`53:36` need to filter out cells that actually
<br>`53:40` have meaningful information and we have
<br>`53:42` to
<br>`53:42` keep away cells that don't have
<br>`53:44` meaningful information
<br>`53:46` yeah and what we do is we look at such
<br>`53:50` histograms here
<br>`53:52` so we took a look at these histograms
<br>`53:54` and we calculate probability densities
<br>`53:58` over all cells so all columns of this
<br>`54:01` matrix
<br>`54:02` and on the x-axis here is the
<br>`54:06` total amount of information that we have
<br>`54:09` for
<br>`54:09` for a cell so the total number of
<br>`54:11` molecules that we detected
<br>`54:13` for a single cell and you can see this
<br>`54:15` follows a distribution
<br>`54:18` and the first thing that you see there
<br>`54:20` are two blocks now some cells are worse
<br>`54:22` and some cells are better so there is
<br>`54:25` already some variance in the data
<br>`54:27` just because the quality of our
<br>`54:30` measurement
<br>`54:31` is different for two between two groups
<br>`54:33` of cells
<br>`54:35` but all of these are actually good
<br>`54:37` values yeah they're all good
<br>`54:39` yeah and uh we just take out some cells
<br>`54:42` here that is the
<br>`54:43` vertical line that are below one million
<br>`54:46` of these counts now these we throw away
<br>`54:51` now we can also
<br>`54:53` see look at other accounts so um
<br>`54:59` so this is for example how many genes
<br>`55:01` that we detect
<br>`55:02` and here we also cut off
<br>`55:06` here we also cut off
<br>`55:09` basically cells that are low quality
<br>`55:12` in these tails here we just remove them
<br>`55:14` from the data set
<br>`55:16` because we know that if we kept them in
<br>`55:18` the data set in the long term
<br>`55:19` we would have problems with
<br>`55:21` dimensionality reduction now they would
<br>`55:23` these things dominate in the end
<br>`55:26` things that are based on machine
<br>`55:28` learning clustering
<br>`55:29` dimensionality reduction so we remove
<br>`55:31` them from the data set
<br>`55:34` and now that's sorry excuse me
<br>`55:36` replications
<br>`55:37` yes so is there any uh is a systematic
<br>`55:41` way to set
<br>`55:43` the threshold to filter out
<br>`55:46` in this case uh it's a matter of
<br>`55:49` experience
<br>`55:50` yeah there's not a systematic way
<br>`55:53` normally
<br>`55:53` [Music]
<br>`55:55` you would set the threshold in such a
<br>`55:57` data set
<br>`55:58` you would set the threshold here in the
<br>`56:00` middle between the two
<br>`56:02` peaks but between but because the two
<br>`56:04` peaks are both at reasonable values
<br>`56:06` and they're all of the same height yeah
<br>`56:09` then
<br>`56:10` uh you know i said we would get we would
<br>`56:12` lose 50
<br>`56:13` of the data and that's a little bit too
<br>`56:15` much yeah but they're all reasonable but
<br>`56:17` we have to check later
<br>`56:19` that if we find two groups of cells in
<br>`56:22` the data
<br>`56:23` that these two groups are not
<br>`56:26` just representing uh these two peaks
<br>`56:30` here in the quality of the measurement
<br>`56:32` yeah the later we have to we now go go
<br>`56:35` on with analysis
<br>`56:37` and if there's something is suspicious
<br>`56:39` we go back to this stage here
<br>`56:42` and we might have to be more rigorous
<br>`56:45` with this
<br>`56:45` cut off here yeah so in this case in
<br>`56:49` this particular case there's no rigorous
<br>`56:51` way of doing that
<br>`56:52` it's a matter of how much do you expect
<br>`56:54` what is the good measurement
<br>`56:56` and uh basically now this is this is a
<br>`56:59` this is a
<br>`57:00` this is a pretty good example in terms
<br>`57:03` of these counts here
<br>`57:04` now if you if you're working on genomics
<br>`57:06` so this is this is actually zebra fish
<br>`57:08` so we have less than in other animals
<br>`57:11` in total and um but but here we don't
<br>`57:15` have basically
<br>`57:17` sometimes you have a another peak here
<br>`57:20` at very low values
<br>`57:22` and that we would then completely cut
<br>`57:24` off
<br>`57:26` so here the problem more is this one
<br>`57:28` here this plot
<br>`57:30` we have a lot of cells that have a high
<br>`57:33` percentage
<br>`57:34` of mitochondrial accounts so that that
<br>`57:37` are genes
<br>`57:38` or the dna that is in the mitochondria
<br>`57:42` and these genes do not produce
<br>`57:45` this dna does not produce many gene
<br>`57:48` products
<br>`57:49` yeah so it suspicious if you have too
<br>`57:51` much of that in this
<br>`57:53` in these cells and here we take out
<br>`57:56` roughly i guess 20 or 30
<br>`57:59` 20 20 of the cells
<br>`58:02` we lose in this step
<br>`58:05` yeah and we can also plot both with
<br>`58:08` respect to each other
<br>`58:09` for example we can here on the x-axis
<br>`58:11` have these different values that
<br>`58:13` represent the quality of our data
<br>`58:15` and then just in half these bars these
<br>`58:19` vertical and lines that we had in the
<br>`58:20` histograms
<br>`58:22` just in this scatter plot here yeah and
<br>`58:25` cut
<br>`58:25` and see which what are the kinds of
<br>`58:27` cells that we use here
<br>`58:29` uh visually yeah
<br>`58:33` okay now so now now we get rid of the
<br>`58:36` bad stuff the other things that are
<br>`58:38` totally crazy now the next thing
<br>`58:41` we need to do is to make
<br>`58:44` cells comparable so cells
<br>`58:48` still have different uh cells that
<br>`58:51` have different measurement qualities
<br>`58:54` they're still
<br>`58:55` different based on technical reasons so
<br>`58:57` for some cells we have a lot of
<br>`58:58` information
<br>`59:00` now we have a lot of these counts that
<br>`59:02` we detected
<br>`59:03` and in other cells we have less but we
<br>`59:06` want to make them comparable to each
<br>`59:08` other
<br>`59:08` and that's why we have to normalize the
<br>`59:11` data
<br>`59:12` yeah and there are fancy ways in
<br>`59:14` genomics there are fancy ways of doing
<br>`59:16` this and you can see we're
<br>`59:17` doing all of that basically and uh
<br>`59:21` so but we have to normalize the data you
<br>`59:24` have to make them comparable that's what
<br>`59:26` you always have to do
<br>`59:27` and what we also do here is because
<br>`59:30` these
<br>`59:30` these uh data counts you could see
<br>`59:34` like in the matrix that i showed you
<br>`59:36` there were very large numbers and very
<br>`59:38` small numbers
<br>`59:40` yeah and what we have so these
<br>`59:43` counts they live on an exponential scale
<br>`59:46` that's their these distributions are
<br>`59:48` very skewed it's a few cells that have a
<br>`59:51` huge amount or a few genes
<br>`59:52` that have a huge amount of these counts
<br>`59:55` of these
<br>`59:56` measurements yeah and that's not
<br>`59:58` something that works very well with
<br>`60:00` dimensionality reduction
<br>`60:02` or clustering methods so we take the
<br>`60:04` logarithm
<br>`60:05` we log transform the data for
<br>`60:08` any further processing now that's also
<br>`60:11` something that you do if your
<br>`60:13` data is too spread the other it comes
<br>`60:15` from some
<br>`60:16` exponential process also yeah then you
<br>`60:19` have the log transformers you want it to
<br>`60:21` be something
<br>`60:22` like normally distributed something
<br>`60:24` symmetrically and
<br>`60:25` rather compact as a distribution
<br>`60:30` yeah okay let's go on so here we can do
<br>`60:33` a variance stabilizing
<br>`60:35` uh transformation and we do more stuff
<br>`60:37` on the data
<br>`60:40` and then we can go and now we can start
<br>`60:44` to understand the data the first thing
<br>`60:46` we need to do
<br>`60:48` is to see does it actually make sense
<br>`60:51` what we do
<br>`60:52` what we have here are we actually
<br>`60:54` looking at biological information and
<br>`60:56` real information
<br>`60:57` or are we just looking at technical
<br>`61:00` aspects
<br>`61:01` of the experiments and as a first step
<br>`61:05` what we do here is we
<br>`61:08` plot a little pca fabian showed that
<br>`61:11` last week what a pca is
<br>`61:13` and these data on the pca on the
<br>`61:15` principal component analysis plots
<br>`61:18` they look like this and you can see
<br>`61:21` so here i plot for example the total
<br>`61:24` amount of these counts in a cell you
<br>`61:27` know that's a
<br>`61:28` that's a technical that's just measuring
<br>`61:31` the quality
<br>`61:33` of the measurements and you can see
<br>`61:35` there is some variability here so that
<br>`61:37` these cells have a little bit more these
<br>`61:40` cells are a little bit more
<br>`61:41` less and some of this technical
<br>`61:43` variability is captured
<br>`61:46` by the um by these experiments
<br>`61:50` by this principle component analysis so
<br>`61:53` here we're fine
<br>`61:54` with it it's not extreme we don't have
<br>`61:56` disconnected clusters
<br>`61:57` so we are fine with this it's already in
<br>`62:00` a good shape
<br>`62:01` and also we know that in cells can have
<br>`62:05` these differences
<br>`62:06` in the total number of molecules in the
<br>`62:09` cell for biological reasons
<br>`62:13` now and then we can look at these plots
<br>`62:15` here what is the percentage of variance
<br>`62:18` actually explained by certain principal
<br>`62:21` components now that's actually the
<br>`62:23` y-axis is
<br>`62:24` something else but we can order these
<br>`62:27` principal components
<br>`62:29` based on how much they explain the total
<br>`62:31` data
<br>`62:33` and what we do and that this is sort of
<br>`62:35` saying like a very professional
<br>`62:37` way of doing things is we do all other
<br>`62:39` calculations not on the real data
<br>`62:43` but on the principal components of the
<br>`62:45` data yeah that's an
<br>`62:46` intermediary step that we do just to get
<br>`62:49` cleaner results in the end
<br>`62:51` so so what we do here is we take the
<br>`62:53` first
<br>`62:54` 20 25 or so principal components
<br>`62:58` that constitute like 99 of the variance
<br>`63:01` of the total
<br>`63:02` plot and we say the rest is noise that's
<br>`63:04` a way of getting rid of the noise
<br>`63:06` in the data and now we go on
<br>`63:10` yeah and do dimensionality reduction
<br>`63:12` further dimensionality reduction
<br>`63:16` let me make this larger
<br>`63:24` now i hope you can see these plots
<br>`63:28` so this is a u map yeah so this is the
<br>`63:31` this is a umap
<br>`63:32` uh that is a non-linear way of reducing
<br>`63:36` the dimensions that
<br>`63:37` fabian showed to you last week
<br>`63:40` and you can see once we do the
<br>`63:42` non-linear dimensionality
<br>`63:44` reduction our data looks already much
<br>`63:47` more structured so these cells here
<br>`63:51` are from actually from the brain these
<br>`63:53` are brain cells
<br>`63:55` and of course there are different kinds
<br>`63:57` of cells in the brain
<br>`63:59` and because they're different kinds of
<br>`64:01` cells in the brain we also
<br>`64:03` expect here a structure
<br>`64:06` to pop up in these low-dimensional
<br>`64:09` representations
<br>`64:11` typically these clusters correspond to
<br>`64:13` different kinds of cells
<br>`64:16` yeah so we don't know that's just a gray
<br>`64:18` bunch of cells here
<br>`64:19` of dots and the two dimensional planes
<br>`64:21` we don't know what the x's are
<br>`64:23` and we don't know what these cells are
<br>`64:25` and now we have to dig a little bit
<br>`64:26` deeper
<br>`64:28` and we do clustering so here is
<br>`64:31` clustering
<br>`64:32` and that's clustering that's one of
<br>`64:35` these community based clustering
<br>`64:37` algorithms
<br>`64:39` and we did that for several
<br>`64:43` resolutions of the clustering yeah so in
<br>`64:45` clustering
<br>`64:46` in most of the time you have to tell the
<br>`64:48` algorithm
<br>`64:49` how many clusters you want yeah
<br>`64:53` and uh that's that's kind of a
<br>`64:54` resolution
<br>`64:56` that you give to these algorithms and uh
<br>`64:59` by doing this
<br>`65:00` you uh and what you see here are
<br>`65:03` different clusterings
<br>`65:06` with different resolutions now so here
<br>`65:09` you say okay
<br>`65:10` give me what is that 15 clusters
<br>`65:13` then you got this plot on the bottom
<br>`65:14` left if you say okay
<br>`65:16` give me what is it eight clusters then
<br>`65:19` you get this
<br>`65:20` these clusters on the top left
<br>`65:24` and you can have more clusters if you
<br>`65:27` want yeah
<br>`65:28` they're different stages but we don't
<br>`65:30` know yet
<br>`65:31` what makes sense yeah we don't know how
<br>`65:33` many real clusters there are in the data
<br>`65:37` but we can take all of them and we can
<br>`65:39` go one step further
<br>`65:41` how do we know that such a cluster is a
<br>`65:43` real biological cluster
<br>`65:46` we know that if the cells in a cluster
<br>`65:50` all share some property that is not
<br>`65:53` shared
<br>`65:54` by other that is not shown by other
<br>`65:57` cells
<br>`65:59` now then we know that this cluster is
<br>`66:01` something real
<br>`66:02` uh that really is going on in the brain
<br>`66:06` and the way we do that is
<br>`66:09` let's go down then we look at the
<br>`66:12` literature
<br>`66:13` so now we look at the literature we look
<br>`66:15` at papers
<br>`66:16` yeah so we say we look at papers and
<br>`66:18` then in these papers
<br>`66:20` we see okay there are different cells
<br>`66:22` and kinds of cells in the brain
<br>`66:25` and people have done experiments
<br>`66:28` genetic experiments for example where
<br>`66:30` they found for example
<br>`66:32` that stem cells express a certain gene
<br>`66:36` now for example this gluolar gene here
<br>`66:38` that's expressed by stem cells
<br>`66:40` and now we plot this umap with the color
<br>`66:45` representing how much of the products of
<br>`66:48` this glue
<br>`66:49` gene we found in a certain cell
<br>`66:53` and now that makes a little bit sense
<br>`66:54` and now here in this corner here on the
<br>`66:56` top left
<br>`66:58` these are our stem cells
<br>`67:01` and then we can see okay so there are
<br>`67:03` also neurons in the brain and
<br>`67:05` many other things let's what's going on
<br>`67:07` yeah so there's another cell type that
<br>`67:09` expresses this
<br>`67:11` cell yeah that's the more advanced cell
<br>`67:13` type
<br>`67:14` from stem cells yeah that's all now in
<br>`67:17` the next step here let's express
<br>`67:18` in these cells here and then you could
<br>`67:21` can go down
<br>`67:22` and identify all of these clusters
<br>`67:27` step by step and identify
<br>`67:30` what kind of cells you have in the data
<br>`67:34` yeah you can do that with more genes
<br>`67:37` even
<br>`67:38` so there's a lot of genes like these
<br>`67:40` genes here that identify neurons
<br>`67:43` and different kinds of neurons so here
<br>`67:45` we have a little
<br>`67:46` just feature of this plot that is
<br>`67:48` identified by this gene
<br>`67:50` and if you talk bibologies all of these
<br>`67:52` names uh
<br>`67:54` are associated with different shapes or
<br>`67:56` different functions of cells
<br>`67:59` we can also do more fancy stuff and to
<br>`68:01` look at different gene scores and add
<br>`68:03` groups of genes
<br>`68:05` do statistical computations yeah and
<br>`68:08` once we've do
<br>`68:09` done that we decide okay
<br>`68:12` for these set of genes here we have a
<br>`68:15` unique
<br>`68:16` we fulfill this condition that each of
<br>`68:18` these clusters here
<br>`68:19` for these clusters we fulfill the
<br>`68:21` condition
<br>`68:22` that each of these clusters has
<br>`68:26` a certain biological function or
<br>`68:28` represents a biological function
<br>`68:30` because we found a gene in the
<br>`68:32` literature
<br>`68:33` that corresponds to a certain cell type
<br>`68:35` in the body
<br>`68:37` that is expressed in one of them but not
<br>`68:39` in the others
<br>`68:41` yeah so that's uh that's very important
<br>`68:45` and then we can give these clusters
<br>`68:47` names here for example
<br>`68:49` retinol or radioglia cells
<br>`68:52` uh uh only oligodendrocyte
<br>`68:56` precursor cells and so on and neurons
<br>`68:59` and then you find okay so these orange
<br>`69:01` ones here are the neurons
<br>`69:02` yeah and uh here were the stem cells
<br>`69:06` and then you can start thinking okay
<br>`69:08` these sensors somehow
<br>`69:09` turn here into these neurons and they
<br>`69:12` mature
<br>`69:13` now they get they get more mature and
<br>`69:15` then at the end they turn into these
<br>`69:17` neurons here
<br>`69:18` and then we have other cell types in the
<br>`69:20` brain like microglia
<br>`69:23` and so on that we also can find here
<br>`69:27` now remember in the u map the
<br>`69:31` distances in the u map is the humor
<br>`69:35` keeps the global topology intact
<br>`69:38` now that means that cells that are close
<br>`69:40` in here are
<br>`69:42` actually also very similar on uh
<br>`69:45` in the in this high dimensional space
<br>`69:49` so it's actually tempting that you think
<br>`69:50` about these
<br>`69:52` paths here as a trajectory that cells
<br>`69:55` take while they take from while they go
<br>`69:58` from stem cells
<br>`70:00` into neurons in the brain
<br>`70:04` now so let's go on now there's a lot of
<br>`70:06` consistency checks
<br>`70:08` yeah so you have to check all kinds of
<br>`70:10` genes
<br>`70:11` yeah a lot of them and discuss a lot of
<br>`70:14` with the people who actually know
<br>`70:16` who do nothing else in their lives but
<br>`70:17` to look at these cells and the brains
<br>`70:19` and they know
<br>`70:20` all of these genes and all of the papers
<br>`70:22` in these genes
<br>`70:23` yeah and i also do more fancy stuff
<br>`70:28` yeah and uh then you can do with
<br>`70:32` different clustering uh and now we have
<br>`70:35` a
<br>`70:36` identification and this one i said is
<br>`70:38` the one
<br>`70:40` that we can live with with these eight
<br>`70:42` clusters
<br>`70:43` while for these higher clusters now we
<br>`70:46` have
<br>`70:47` several several clusters representing
<br>`70:49` the same cell type
<br>`70:51` and we can in principle come back later
<br>`70:53` to these higher clusters
<br>`70:56` and typically biologists once want you
<br>`70:58` to do to get as many clusters
<br>`71:02` as you can yeah um
<br>`71:05` yeah so now we have these classes and we
<br>`71:06` can have some measurements
<br>`71:08` of how good these clusters are actually
<br>`71:12` and there are specific plots for these
<br>`71:15` for this
<br>`71:15` for example these are called dot plots
<br>`71:18` and
<br>`71:19` um what these plots show is on the
<br>`71:22` x-axis
<br>`71:23` our gene names and on the y-axis
<br>`71:27` are the cluster names yeah
<br>`71:31` and the color represents how much
<br>`71:34` a gene on average is present in the
<br>`71:38` cluster
<br>`71:40` and the size of these plots tells you
<br>`71:44` how what is the fraction of cells that
<br>`71:47` have this gene on
<br>`71:49` in this cluster now so and if we go now
<br>`71:53` here
<br>`71:54` what we want to see is that these genes
<br>`71:56` that we have here
<br>`71:58` are only on in one cluster but not in
<br>`72:01` other clusters
<br>`72:02` now for example a good thing is this one
<br>`72:05` here
<br>`72:06` this only go this oc cluster
<br>`72:10` now there's only one cluster here
<br>`72:13` there's only there are these these genes
<br>`72:16` here that we have
<br>`72:17` identified for this cluster that is
<br>`72:20` called
<br>`72:21` marker genes the other computation tools
<br>`72:23` to detect them
<br>`72:25` they are only you only find that in this
<br>`72:28` cluster
<br>`72:28` but not in the other cluster same for
<br>`72:32` this mg this microglia
<br>`72:34` we only find these genes in this single
<br>`72:36` this one cluster but not in any other
<br>`72:39` cluster
<br>`72:40` and while we go for what's a messy one
<br>`72:44` opc's
<br>`72:45` or we go for this neurons here
<br>`72:49` then it's more messy and it's not so
<br>`72:53` clearly defined
<br>`72:54` so if we go back now for example
<br>`72:57` now if we go here if we look at these
<br>`72:59` plots then these
<br>`73:01` mg's microglia they were very clean
<br>`73:04` in this plot that i just showed you yeah
<br>`73:07` and that's also represented in this new
<br>`73:09` new
<br>`73:10` you map they're a different cell type
<br>`73:14` that is not produced presumably by the
<br>`73:17` same stem
<br>`73:18` cells as the neurons
<br>`73:21` also these ocs yeah as oligodendrocytes
<br>`73:25` i think
<br>`73:26` yeah that's separated from the rest so
<br>`73:29` there's no overlap here there's a
<br>`73:30` distinct cell types
<br>`73:33` while for things like that we had an
<br>`73:35` overlap between these material neurons
<br>`73:38` at the sixth cluster that's called six
<br>`73:40` here
<br>`73:41` yeah there we found that
<br>`73:44` there is an overlap actually in these
<br>`73:46` marketers they have the same genes
<br>`73:48` that they express and probably that
<br>`73:50` means that this cluster six
<br>`73:52` is an artifact yeah that we cannot take
<br>`73:55` too seriously
<br>`73:56` and on the right hand side you can see
<br>`73:58` that in the next step now we took these
<br>`74:01` i have went a little bit broader and
<br>`74:03` took this cluster six
<br>`74:04` into the interval neurons here
<br>`74:08` now so now of course i showed you
<br>`74:10` basically a finalized version
<br>`74:12` normally you go back between these steps
<br>`74:14` and the earlier steps
<br>`74:16` again and again the call it back to the
<br>`74:17` quality control
<br>`74:19` until you have that do not have any
<br>`74:21` trace
<br>`74:22` of experimental technical parameters
<br>`74:25` in your plots and then also you go back
<br>`74:29` between these clusterings your
<br>`74:31` experimental friends
<br>`74:32` who do the experiments and the
<br>`74:35` literature
<br>`74:35` until you find something that is really
<br>`74:37` corresponding to
<br>`74:40` to to what makes biologically sense
<br>`74:43` it's not that these techniques give you
<br>`74:46` automatically
<br>`74:47` something uh that this was like a
<br>`74:50` mathematical criterion
<br>`74:53` that would tell you uh what makes sense
<br>`74:55` and you have to do that always have to
<br>`74:56` do that yourself
<br>`74:59` that's not that you push a button and
<br>`75:00` then everything is
<br>`75:02` works automatically and that's why these
<br>`75:04` people who do these kind of
<br>`75:06` analysis are very much looked looked for
<br>`75:09` on the job market
<br>`75:12` okay so uh let me just see if there's
<br>`75:15` any
<br>`75:16` other anything other interesting i think
<br>`75:17` there's you can go on and on forever you
<br>`75:20` know you can give the experimental lists
<br>`75:22` you know so which genes are on and off
<br>`75:25` in which cells
<br>`75:26` and once the experimentalists have these
<br>`75:29` lists they can do more
<br>`75:30` experiments uh they can create for
<br>`75:33` example
<br>`75:34` new animals that lack these genes
<br>`75:37` and what i want to show you
<br>`75:40` is now something that's on the bottom
<br>`75:44` you know so that the analysis is very
<br>`75:46` lengthy
<br>`75:50` now there are many aspects of course
<br>`75:51` that are irrelevant for biology
<br>`75:54` um i just want to show you
<br>`76:01` a lot of stuff a lot of stuff now that's
<br>`76:04` what the biologists are interested in
<br>`76:05` right
<br>`76:06` so these they hold these jeans um
<br>`76:09` all the stuff all the stuff a lot of
<br>`76:11` stuff even more stuff
<br>`76:20` yeah if more more more more also a lot
<br>`76:22` of calculations
<br>`76:24` yeah more heat maps to check
<br>`76:28` you know which genes are on where and so
<br>`76:30` on yeah so that's all
<br>`76:32` uh uh consistency checks
<br>`76:35` and one thing i want to just to show you
<br>`76:38` is uh something that's called let me see
<br>`76:40` do we have
<br>`76:42` [Music]
<br>`76:43` okay is something that's called
<br>`76:46` trajectory inference you know that's
<br>`76:48` so so so these are cells from a brain
<br>`76:52` and what cells do is they start that
<br>`76:54` they divide and they produce other cells
<br>`76:57` and then they get more specialized over
<br>`76:59` time
<br>`77:00` so these cells they start as a stem cell
<br>`77:03` and then
<br>`77:04` they mature until they at some point
<br>`77:06` they are in you
<br>`77:07` a new one so what we did here is
<br>`77:11` uh what you did here and what you do in
<br>`77:12` many cases is you take
<br>`77:14` okay i have a snapshot data so this
<br>`77:17` fish or these fish were killed for the
<br>`77:20` measurement
<br>`77:21` i don't have a time course or anything
<br>`77:23` now i don't uh as a snapshot measurement
<br>`77:26` just one measurement
<br>`77:28` but i have different cells that are at
<br>`77:30` different stages of this dynamic process
<br>`77:33` of cell maturation so what then people
<br>`77:36` do is uh can we get the temporal
<br>`77:39` information back
<br>`77:40` yeah and this is the trajectory
<br>`77:42` inference of how
<br>`77:44` these different clusters and cell types
<br>`77:46` relate to each other
<br>`77:48` and where you then can calculate rates
<br>`77:51` of how
<br>`77:51` one cell go one cell type
<br>`77:54` the flux that from one cell type leaks
<br>`77:57` leads to another cell type
<br>`77:59` now and in principle based on this you
<br>`78:01` can then come up with stochastic
<br>`78:03` models that you can in principle also
<br>`78:05` compare them to
<br>`78:06` uh to other experiments or theoretical
<br>`78:09` work
<br>`78:10` now that's i just wanted to show you uh
<br>`78:13` at the end
<br>`78:13` and let me just go through here if
<br>`78:15` there's anything else that's worth
<br>`78:17` showing you
<br>`78:18` um a lot of stuff now then you can
<br>`78:21` compare to humans and other animals
<br>`78:24` you can see where there are similarities
<br>`78:27` uh
<br>`78:27` these fish here that we're looking at
<br>`78:29` are very interesting because they can
<br>`78:31` regenerate their brain they can build
<br>`78:33` new neurons
<br>`78:34` that's something we cannot do so it's so
<br>`78:36` much that we want
<br>`78:38` we want to learn what are the
<br>`78:39` similarities and difference why are we
<br>`78:41` not
<br>`78:41` able to do that as humans yeah and
<br>`78:45` um yeah and then uh
<br>`78:48` we are already you know at the end of
<br>`78:51` this very lengthy analysis
<br>`78:53` yeah so this is a typical data science
<br>`78:56` project
<br>`78:57` from start to end and so you can see
<br>`79:00` here a mixture of
<br>`79:01` r and python and
<br>`79:05` the important thing is that you cannot
<br>`79:07` what we showed you
<br>`79:09` in the last lectures you cannot just go
<br>`79:11` and take the data and
<br>`79:12` throw a umap on it or do some machine
<br>`79:15` learning on it
<br>`79:16` so a large part of the data
<br>`79:20` of this pipeline here is to actually
<br>`79:24` clean up the data and think about what
<br>`79:26` is the part of the data that makes sense
<br>`79:29` and what is the part of the data that
<br>`79:31` does not make sense
<br>`79:33` yeah so for example think about this new
<br>`79:34` york city flights
<br>`79:36` it doesn't make sense to have a negative
<br>`79:37` departure delay and it was a
<br>`79:39` it was a very uh that was a very good
<br>`79:41` question
<br>`79:42` yeah it actually uh makes sense and this
<br>`79:44` is so to say a data set
<br>`79:46` that is used for for teaching a lot so
<br>`79:48` it's already cleaned up a lot but
<br>`79:50` typically you expect
<br>`79:51` to have a lot of nonsensical
<br>`79:54` measurements
<br>`79:55` uh in your data yeah or sometimes you
<br>`79:57` have a departure delay of
<br>`79:59` 10 billion years or so that that would
<br>`80:02` be the correspondence in a real data
<br>`80:04` somebody made a typo somewhere yeah and
<br>`80:06` then you have that in your data set and
<br>`80:08` you have you have to
<br>`80:09` have to filter it out again now this
<br>`80:11` happens all the time if you
<br>`80:13` are not looking after this yeah so if
<br>`80:16` you're not taking care of this
<br>`80:18` then all of these nice plots here that i
<br>`80:20` showed you
<br>`80:21` they won't work now they only work
<br>`80:23` because we clean up the data
<br>`80:25` we normalize the data we transform the
<br>`80:28` data in a statistical way to make it
<br>`80:31` uh nicely behaved yeah it's
<br>`80:34` no huge outliers or so and then these
<br>`80:37` methods
<br>`80:38` like uh umap and so on work on the data
<br>`80:42` but you always have to do these
<br>`80:44` pre-processing steps
<br>`80:46` before that to make that work and the
<br>`80:47` next step is you you have these fancy
<br>`80:49` methods
<br>`80:50` but taking a loan they don't make sense
<br>`80:53` so you can see here how this order has
<br>`80:56` ordered this
<br>`80:56` trajectories cells move here along in
<br>`80:59` time
<br>`81:00` move along this line and turn into
<br>`81:02` neurons here
<br>`81:04` and of course we have many different
<br>`81:05` neurons in the brain
<br>`81:07` yeah and but to understand that what's
<br>`81:09` happening here this data to make sense
<br>`81:11` of this
<br>`81:12` now you have to come up with hypothesis
<br>`81:15` you have to connect these hypotheses
<br>`81:16` with
<br>`81:17` what is already out there in the
<br>`81:18` literature and then step by step you can
<br>`81:21` construct
<br>`81:22` an understanding about what are actually
<br>`81:24` here the degrees of freedom
<br>`81:26` that you see in this data set you know
<br>`81:29` and so this is this is an example and
<br>`81:32` this
<br>`81:32` is an iterative process that you improve
<br>`81:36` over time and so this is an example
<br>`81:39` that's a purity
<br>`81:40` purely data science project or there's
<br>`81:43` very little physics in it
<br>`81:45` and next time we show you how all of
<br>`81:47` these connects to something that we
<br>`81:49` actually
<br>`81:51` did in the first part of this lecture
<br>`81:53` namely field theory
<br>`81:54` face transitions criticality and so on
<br>`81:58` okay great so i'll stay online and in
<br>`82:01` case there are any questions otherwise
<br>`82:03` see you next week
<br>`82:08` bye
<br>`82:21` thank you it was very interesting yeah
<br>`82:24` so when are you when are you going 
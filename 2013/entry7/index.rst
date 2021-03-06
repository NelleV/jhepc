Entry 7 (First Place)
=====================

.. image:: entry7.png

Authors
-------

- Edward Taylor

Caption
-------

Demonstrating the quality of our fits to the joint colour--mass
distributions.— The histograms in each panel show the
incompleteness-corrected distribution of colours of z < 0.12 galaxies,
computed in bins of log M∗ centred on log M∗ = 8.8, 9.0, ...,
11.4. The left panel is for the effective (g-i) colour; the right
panel is for the intrinsic, dust-corrected, stellar colour, (g-i)*.
The errorbars show the statistical uncertainties on each these
distributions, derived by bootstrap resampling. The smooth curves show
the results of our modelling: the blue and red curves show the fit
distributions for the B- and R-populations; the black curves shows the
net B+R distributions. Underlaid beneath all this, the grey points
show the data themselves; the size of each point reflects the relative
1/Vmax scaling used to account for selection effects. Note that we
have not binned the data in the course of the fits; the binning in
this Figure is for illustrative purposes only. It is clear that the
fit model provides an excellent description of the observed data.

Description
-----------

These two panels are the showpiece of a new study that i have spent
the last 3 years (!!) working on, looking into the idea of
'bimodality' among galaxies.  I have just (finally!) submitted this
work to MNRAS; the paper is actually the first in a series of 5 in
which i am developing a phenomenological description of the main
stages of galaxy evolution.

The observational result of 'bimodality' has played a crucial role in
the development of our theoretical understanding of the process of
galaxy formation and evolution.  Let me explain how, as briefly as i
can.

It seems that there are two and only two kinds of galaxies: red ones,
and blue ones.  (This is, of course, an over simplification -- in
fact, it is exactly this kind of oversimplification that i am trying
to bust!  But it is fair to say that this is how a lot of people in
the field talk about things, even if they don't really believe it.)
In simple terms, a blue colour implies that a galaxy has formed at
least some stars in the past few hundred million years.  A red colour
can mean one of two things: it can mean either a very old stellar
population, with no star formation over the past billion years or so,
or it can mean that there is a lot of dust in the galaxy.  (Dust makes
things red: think about a sunset on a smoggy evening.)  So - modulo
dust - the difference between red and blue is the difference between
'star-forming' and 'dead'

The weird thing is that the most massive galaxies tend to be red and
dead.  This is weird because gravity is what drives star formation.
Naively, you might think that more mass means more gravity, and so
more star formation.  But that's not what happens: apparently, there
is something that kills or 'quenches' the process of star formation in
massive galaxies.  Nobody knows what this might be, even though this
quenching problem is one of the most intensively studied areas of
extragalactic astronomy over the last ten or twelve years.

Models of galaxy evolution have to include some ad hoc prescription
for when star formation is quenched, but pretty much every model has
its own prescription -- no one really understands what the real
physical mechanism is.  As ridiculous as it sounds, the best way to
constrain these models is simply to measure the relative and absolute
numbers of 'red' and 'blue' galaxies.

Even more ridiculously, even after ten or twelve years, no one has
really measured this well. Let me explain what i mean by that.

What people have done in the part (with only one notable exception, in
2004) is simply to draw a line that divides 'red' galaxies from 'blue'
ones.  The problem with this is that if you draw a different line, you
get a different answer.  And the decision about precisely where to
draw the line is always arguable, hence arbitrary.  This is even worse
than it sounds: different choices for the line give you
*qualitatively* different measurements.

So what I have done is to develop a mixture modelling approach.
Instead of drawing a line to separate 'red' and 'blue' *galaxies*, I
model the data as a mixture of two distinct but overlapping
*populations*.  This lets me figure out the number of galaxies in the
'red' and 'blue' populations without ever specifying whether any
particular galaxy belongs to which population.  This lets me get
around the problem of having to draw a line -- in fact, it gives a way
to derive an objective, phenomenological classification scheme that is
*based on the data*.

These plots show just how good a description of the data the mixture
modelling provides.

What's more, in the 'intrinsic' plot, I have actually performed a
correction for dust, so that I really am distinguishing galaxies based
on their stars, not just their apparent colours.  And even better than
that, although this point isn't visually emphasised in the plots I've
submitted, i get the same answer in both cases.  In other words, if
you do the mixture modelling well, you get the right answer, no matter
whether you do the dust correction or not -- I have definitely gotten
around the dust problem.  And that's pretty neat.

The only other thing that I'll say is that I had to learn a lot of
statistics in order to do all this.  The fits shown in each panel have
35-40 parameters (having done the full and proper Bayesian model
selection to make sure that these really are the best and simplest
descriptions of the data).  This is a level of statistical rigor that
is very, very rare in the field. But it is, in my opinion the way
forward in the new age of 'big data' astronomy.

That was a lot of background, but i hope it wasn't too painful to
read!

Instructions
------------

There are two `.json` archives that contain the data
for each of the two panels.  There is also the script `bimix.py` that
should use these data to make the two plots.  You can either (i hope!)
just `python bimix.py` at the command line, or run `bimix.makePlots()`
in interactive mode.

Products
--------

- :download:`PDF Panel 1 <bimix_effective.pdf>`

- :download:`PDF Panel 2 <bimix_intrinsic.pdf>`

Source
------

.. literalinclude:: ENTaylor_bimix.py

- :download:`Python source <ENTaylor_bimix.py>`

- :download:`JSON source (Panel 1) <bimix_effective.json>`

- :download:`JSON source (Panel 2) <bimix_intrinsic.json>`

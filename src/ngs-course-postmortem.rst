Teaching next-gen sequencing data analysis to biologists
########################################################

:author: C\. Titus Brown
:tags: python,ngs-course,bioinformatics,python
:date: 2010-06-14
:slug: ngs-course-postmortem
:category: python


Our `sequencing analysis course
<http://bioinformatics.msu.edu/ngs-summer-course-2010>`__ ended last
Friday, with an overwhelmingly positive response from the students.
The few negative comments that I got were largely about organizational
issues, and could be reshaped as suggestions for next time rather than
as condemnations of this year's course.

.. image:: http://ivory.idyll.org/permanent/ngs-2010-group.png
   :width: 65%

The 23 students -- most with no prior command-line experience -- spent
two weeks experiencing at first hand the challenges of dealing with
dozens of gigabytes of sequencing data.  Each of the students went
through genome-scale mapping, genome assembly, mRNAseq analysis on an
"emerging model organism" (a.k.a "one with a crappy genome", lamprey),
resequencing analysis on E. coli, and ChIP-seq analysis on Myxococcus
xanthus.  By the beginning of the second week, many students were working
with their own data -- a real victory.  Python programming competency
may take a bit longer, but many of them seem motivated.

If you had told me three weeks ago that we could pull this off, I
would have told you that you were crazy.  This does beg the question
of what I was thinking when I proposed the course -- but don't dwell
on that, please...

The locale was great, as you can see:

.. image:: http://ivory.idyll.org/permanent/ngs-2010-beach.png
   :width: 65%

One of the most important lessons of the course for me is that `cloud
computing works well to backstop this kind of course
<http://ivory.idyll.org/blog/jun-10/ngs-course-with-aws.html>`__.  I
was very worried about the suitabiliy and reliability and ease of use,
but AWS did a great job, providing an easy-to-use Web interface and a
good range of machine images.  I have little doubt that this course
would have been nearly impossible (and either completely ineffective
or much more expensive) without it.

In the end, we spent more on beer than on computational power.  That says
something important to me :)

The `course notes <http://ged.msu.edu/angus/>`__ are available under a
CC license although they need to be reworked to use publicly available
data sets before they become truly useful.  At that point I expect them
to become awesomely useful, though.

From the scientific perspective, the students derived a number of
significant benefits from the course.  One that I had not really
expected was that some students had no idea what went in to
computational "sausage", and were kind of shocked to see what kinds of
assumptions us comp bio people made on their behalf.  This was
especially true in the case of students from companies, who have
pipelines that are run on their data.  One student lamented that "we
used to look at the raw traces... now all we get are spreadsheet
summaries!"  Another student came to me in a panic because they didn't
realize that there *was* no one true answer -- that that was in fact
part of the "fun" of *all* biology, not just experimental biology.
These reactions alone made teaching the course worthwhile.

Of course, the main point is that many of the students seem to be
capable of at least starting their own analyses now.  I was surprised
at the practical power of our cut-and-paste approach -- for example,
if you look at the `Short-read assembly with ABySS tutorial
<http://ged.msu.edu/angus/tutorials/short-read-assembly.html>`__, it
turns out to be relatively straightforward to adapt this to doing
assemblies of your own genomic or transcriptomic data.  I based our
approach on Greg Wilson's post on `the failure of inquiry-based
teaching <http://pyre.third-bit.com/blog/archives/3761.html>`__ and so
far I like it.

I am particularly amused that we have now documented, in replicable
detail, the Kroos Lab MrpC ChIP analysis.  We also have the best
documentation for Jeff Barrick's breseq software, I think; this is
what is used to analyze the `Long Term Evolution Experiment
<http://en.wikipedia.org/wiki/E._coli_long-term_evolution_experiment>`__
lines -- and I can't wait for the anti-evolutionists to pounce on
that...  "Titus Brown -- making evolution experiments accessible to
creationists."  Yay?

There were a number of problems and mistakes that we had to
steamroller through.  In particular, more background and more advanced
tutorials would have be great, but we just didn't have time to write
them.  Some 454, Helicos, and SOLiD data sets (and next year, PacBio?)
would be a good addition.  We had a general lack of multiplexing data,
which is becoming a Big Thing now that sequencing is so ridiculously
deep. I would also like to introduce additional real data analyses
next year, reprising things like the `Cufflinks analysis
<http://www.nature.com/nbt/journal/v28/n5/abs/nbt.1621.html>`__ and
whole-vertebrate-genome ChIP-seq/mRNAseq `a la the Wold Lab
<http://www.nature.com/nmeth/journal/v6/n11s/abs/nmeth.1371.html>`__.
I'm weighing adding metagenomics data analysis in for a day, although
it's a pretty separate field of inquiry (and frankly much harder in
terms of "unknown unknowns").  We also desperately need some plant
genomics expertise, because frankly I know nothing about plant
genomes; my last-minute plant genomics TA fell through due to lack of
planning on my part.  (Conveniently, plant genomics is something MSU
is particularly good at, so I'm sure I can find someone next year.)

Oops, did I say next year?  Well, yes.  *If* I can find funding for my
princely salary, *then* I will almost certainly run the course again
next year.  I can cover TAs and my own room/board and speakers with
workshop fees, but if I'm going to keep room+board+fees under
\\$1000/student -- a practical necessity for most -- there's no way I
can pay myself, too.  And while this year I relied on my lovely,
patient, and frankly long-suffering wife to hold down the home fort
while I was away for two weeks, I simply can't put her through that
again, so I will need to pay for a nanny next year.  So doing it for
free is not an option.

In other words, **if you are a sequencing company, or an NIH/NSF/USDA
program director, interested in keeping this going, please get in
touch**.  I plan to apply for this `Initiative to Maximize Research
Education in Genomics
<http://grants.nih.gov/grants/guide/pa-files/PAR-09-245.html>`__ in
September, but I am not confident of getting that on the first try,
and in any case I will need letters of support from interested folks.
So `drop me a note at ctb@msu.edu <mailto:ctb@msu.edu>`__.

Course development this year was sponsored by the `MSU Gene Expression
in Disease and Development <http://www.bch.msu.edu/GEDD/>`__, to whom
I am truly grateful.  The course would simply not have been possible
without their support.

My overall conclusion is that it is possible to teach bench biologists
with no prior computational experience to achieve at least minimal
competency in real-world data analysis of next-generation sequencing
data.  I can't conclusively *demonstrate* this without doing a better
job of course evaluation, and of course only time will tell if it
sticks for any of the students, but right now I'm feeling pretty good
about the course overall.  Not to mention massively relieved.

--titus

p.s. Update from one student -- "It's not even 12 o'clock Monday
morning and I'm already getting people asking me how to run assemblies
and analyze data."  Heh.

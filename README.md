mess
====

Small command line utility for estimating effective sample size (ESS) for every
parameter contained in each of many [BEAST 2](http://www.beast2.org/) log files
sharing the same set of parameters. Mess has a few advantages over the
LogAnalyser utility distributed with BEAST when assessing the health of a large
number of similar analyses:

1. Only ESS values are computed and displayed, other irrelevant stats are ignored.

2. Results are colour-coded by default.

3. A compact output mode is available that uses only a single character per
   parameter to indicate whether the ESS is between 0 and 100, between 100 and
    200, or greater than 200.

4. Mess can estimate ESS values using a thinned copy of the trace, dramatically
   speeding up the calculation for large data sets.

For example, here is the output in the default mode. The name of each parameter
and the ESS value for that parameter in each log is listed explicitly:
![img](https://github.com/tgvaughan/mess/wiki/images/mess1.png)

In compact mode the parameters are not named and the actual ESS values aren't
listed, but ascii art is used to depict the health of each log.  The lowest ESS
in each log is given on the right of the art.
![img](https://github.com/tgvaughan/mess/wiki/images/mess2.png)

See `mess -h` for usage instructions.

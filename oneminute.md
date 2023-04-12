* We want to use APSIM to predict crop yield for every field in Iowa.
* At such a large scale, it would take more than it is desirable :)

* We build a statistical model.
* APSIM has +40 input variables.
* Having them all in our statistical model will lead to overfitting.

* We know some inputs are more important than others.
* Big question tho: take for example soil water absortion, is it
  equally relevant across diferent soil layers?????

* We start with a Gaussian Process.
* We propose a new covariance function with a functional length-scale
  parameter that regonizes that the input is a functional indexed by
  depth.

* We learn how fast the predictive relevance of soil water absorption
  decays over soil layers.
* We find that the top 8.8m keeps 99% of the predictive relevance :)
* We have a lower oos RMSE than a GP that treats the input as an
  unstructured vector.












<!--
* We extend current approaches to automatically learn from data how
  input relevance changes at different depths.
-->

<!------------------------------------------------------------------->

* We want to use APSIM to predict crop yield for every field in Iowa
  under various climate and land management configurations. This
  requires hundreds of thousands of APSIM run.
* One prediction takes 3 seconds, but at large scale it would take
  more than it is desirable :)
* We build a statistical model to predict yield at large scale.
* APSIM has +40 input variables. Having them all in our statistical
  model will lead to overfitting. And I'd rather that not happen :)

* We know some inputs are more important than others, e.g. soil
  water absorption.
* Big question tho: is it equally relevant across diferent soil layers?????

* We extend current approaches in the Gaussian Process literature to
  automatically learn from data how relevance changes at different
  depths.
* We propose a new Covariance function that regonizes that
  soil water absortion is a functional indexed by depth.
* We can now learn how fast soil water absorption predictive relevance
  decays over soil layers.
* In an application, we find that the top 8.8m keeps 99% of the
  predictive relevance :)
* Also, this improves prediction RMSE over a GP that treat the input as an
  unstructured vector.

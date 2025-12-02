# Test-Repo
Testing repository
[README.html](https://github.com/user-attachments/files/23890386/README.html)
<!DOCTYPE html>

<html>

<head>

<meta charset="utf-8" />
<meta name="generator" content="pandoc" />
<meta http-equiv="X-UA-Compatible" content="IE=EDGE" />


<div id="peir-ideas-patients-engaged-in-research-survey-enhanced-by-inclusion-diversity-equity-acceptance-and-safety-peir-ideas-scoring-standalone-function" class="section level1">
<h1>PEIR-IDEAS — Patients Engaged in Research Survey Enhanced by
Inclusion, Diversity, Equity, Acceptance, and Safety (PEIR-IDEAS)
Scoring (Standalone Function)</h1>
<p><a href="https://urldefense.com/v3/__http://LICENSE__;!!PFzsKvxRBh-H!b9x36Ji6NuqlbpBfsrUNwL2B7mXOJyH2EMJx9QmXyUO8CiLSLCG7tPET26OUhPVT8to71v9aL0Lt$"><img role="img" aria-label="License: MIT" src="data:image/svg+xml;charset=utf-8;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI4MiIgaGVpZ2h0PSIyMCIgcm9sZT0iaW1nIiBhcmlhLWxhYmVsPSJMaWNlbnNlOiBNSVQiPjx0aXRsZT5MaWNlbnNlOiBNSVQ8L3RpdGxlPjxsaW5lYXJHcmFkaWVudCBpZD0icyIgeDI9IjAiIHkyPSIxMDAlIj48c3RvcCBvZmZzZXQ9IjAiIHN0b3AtY29sb3I9IiNiYmIiIHN0b3Atb3BhY2l0eT0iLjEiLz48c3RvcCBvZmZzZXQ9IjEiIHN0b3Atb3BhY2l0eT0iLjEiLz48L2xpbmVhckdyYWRpZW50PjxjbGlwUGF0aCBpZD0iciI+PHJlY3Qgd2lkdGg9IjgyIiBoZWlnaHQ9IjIwIiByeD0iMyIgZmlsbD0iI2ZmZiIvPjwvY2xpcFBhdGg+PGcgY2xpcC1wYXRoPSJ1cmwoI3IpIj48cmVjdCB3aWR0aD0iNTEiIGhlaWdodD0iMjAiIGZpbGw9IiM1NTUiLz48cmVjdCB4PSI1MSIgd2lkdGg9IjMxIiBoZWlnaHQ9IjIwIiBmaWxsPSIjOTdjYTAwIi8+PHJlY3Qgd2lkdGg9IjgyIiBoZWlnaHQ9IjIwIiBmaWxsPSJ1cmwoI3MpIi8+PC9nPjxnIGZpbGw9IiNmZmYiIHRleHQtYW5jaG9yPSJtaWRkbGUiIGZvbnQtZmFtaWx5PSJWZXJkYW5hLEdlbmV2YSxEZWphVnUgU2FucyxzYW5zLXNlcmlmIiB0ZXh0LXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIiBmb250LXNpemU9IjExMCI+PHRleHQgYXJpYS1oaWRkZW49InRydWUiIHg9IjI2NSIgeT0iMTUwIiBmaWxsPSIjMDEwMTAxIiBmaWxsLW9wYWNpdHk9Ii4zIiB0cmFuc2Zvcm09InNjYWxlKC4xKSIgdGV4dExlbmd0aD0iNDEwIj5MaWNlbnNlPC90ZXh0Pjx0ZXh0IHg9IjI2NSIgeT0iMTQwIiB0cmFuc2Zvcm09InNjYWxlKC4xKSIgZmlsbD0iI2ZmZiIgdGV4dExlbmd0aD0iNDEwIj5MaWNlbnNlPC90ZXh0Pjx0ZXh0IGFyaWEtaGlkZGVuPSJ0cnVlIiB4PSI2NTUiIHk9IjE1MCIgZmlsbD0iIzAxMDEwMSIgZmlsbC1vcGFjaXR5PSIuMyIgdHJhbnNmb3JtPSJzY2FsZSguMSkiIHRleHRMZW5ndGg9IjIxMCI+TUlUPC90ZXh0Pjx0ZXh0IHg9IjY1NSIgeT0iMTQwIiB0cmFuc2Zvcm09InNjYWxlKC4xKSIgZmlsbD0iI2ZmZiIgdGV4dExlbmd0aD0iMjEwIj5NSVQ8L3RleHQ+PC9nPjwvc3ZnPg==" alt="License: MIT" /></a><br />
<strong>Status:</strong> pre-CRAN • simple R script for scoring
PEIRS</p>
<p>This repository provides a single R function,
<code>calculate_peirs_score()</code>, to score the <strong>Patients
Engaged in Research Scale (PEIRS) - IDEAS</strong>.<br />
It returns per-respondent <strong>raw totals</strong>, <strong>items
answered</strong>, a <strong>standardized 0–100 score</strong>, and a
<strong>response status</strong> flag. A custom <code>summary()</code>
method prints describe‑style statistics (n, mean, SD, min, quartiles,
max).</p>
<hr />
<div id="quick-start-two-ways" class="section level2">
<h2>Quick Start (two ways)</h2>
<div id="a-use-directly-from-github" class="section level3">
<h3>A) Use directly from GitHub</h3>
<pre class="r"><code># Load the function straight from this repo (no installation needed)
source("<a href="https://urldefense.com/v3/__https://raw.githubusercontent.com/quantlover/PEIR-IDEAS/main/calculate_peirs_score.R__;!!PFzsKvxRBh-H!b9x36Ji6NuqlbpBfsrUNwL2B7mXOJyH2EMJx9QmXyUO8CiLSLCG7tPET26OUhPVT8to71kUdTo_A$">https://raw.githubusercontent.com/quantlover/PEIR-IDEAS/main/calculate_peirs_score.R</a>")

# Example: score a data frame 'dat' with PEIRS items as columns
scores &lt;- calculate_peirs_score(dat)
summary(scores)</code></pre>
</div>
<div id="b-use-locally" class="section level3">
<h3>B) Use locally</h3>
<pre class="r"><code># Download calculate_peirs_score.R from this repo, then:
source(&quot;calculate_peirs_score.R&quot;)

scores &lt;- calculate_peirs_score(dat)
summary(scores)</code></pre>
<hr />
</div>
</div>
<div id="data-requirements" class="section level2">
<h2>Data Requirements</h2>
<ul>
<li>One row = one respondent.</li>
<li>Columns named with PEIRS item IDs (defaults):<br />
<code>pr2, pr4, pr7, pr11, pr12, pr13, pr14, t1, t2, t3, t4, t5, t6, t7, su1, su2, su3, be1, be2, be3, cn1, cn2, cn3, ct4, fv1, fv2, fv3</code>.<br />
</li>
<li>Responses typically on <strong>Likert 1–5</strong>. Non-numeric
columns are coerced to numeric; failures become <code>NA</code>.</li>
</ul>
<hr />
</div>
<div id="minimal-reproducible-example" class="section level2">
<h2>Minimal Reproducible Example</h2>
<pre class="r"><code># Simulate toy data with the default 23 items
set.seed(123)
items &lt;- c("pr2","pr4","pr7","pr11","pr12","pr13","pr14",
           "t1","t2","t3","t4","t5","t6","t7",
           "su1","su2","su3",
           "be1","be2","be3",
           "cn1","cn2","cn3","ct4",
           "fv1","fv2","fv3")

dat &lt;- as.data.frame(matrix(sample(1:5, 50*length(items), replace=TRUE), nrow=50))
names(dat) &lt;- items

# Load the scorer
# source("calculate_peirs_score.R")   # if local
# or source("<a href="https://urldefense.com/v3/__https://raw.githubusercontent.com/quantlover/PEIR-IDEAS/main/calculate_peirs_score.R__;!!PFzsKvxRBh-H!b9x36Ji6NuqlbpBfsrUNwL2B7mXOJyH2EMJx9QmXyUO8CiLSLCG7tPET26OUhPVT8to71kUdTo_A$">https://raw.githubusercontent.com/quantlover/PEIR-IDEAS/main/calculate_peirs_score.R</a>")

scores &lt;- calculate_peirs_score(dat)
head(scores, 3)
summary(scores)</code></pre>
<hr />
</div>
<div id="interpreting-peirs_standardized-0100" class="section level2">
<h2>Interpreting <code>PEIRS_standardized</code> (0–100)</h2>
<ul>
<li><strong>≥ 70%</strong> → High engagement<br />
</li>
<li><strong>&lt; 70%</strong> → Low engagement</li>
</ul>
<p>Notes: - The standardized score adjusts for the number of items
answered; it is comparable across respondents when using the same item
set. - Use <code>Response_Status</code> to flag incomplete responses
(default rule: &lt; 10 items answered ⇒ “Too few items”).</p>
<hr />
</div>
<div id="common-options" class="section level2">
<h2>Common Options</h2>
<pre class="r"><code># Allow partial item sets (compute with present items, warn about missing)
scores &lt;- calculate_peirs_score(dat, strict = FALSE)

# Custom minimum answered threshold
scores &lt;- calculate_peirs_score(dat, min_items_required = 12)

# Non-standard Likert range (e.g., 0–10 mapped to 0–4)
scores &lt;- calculate_peirs_score(dat, scale_from = c(0,10), scale_to = c(0,4))</code></pre>
<hr />
</div>
<div id="license" class="section level2">
<h2>License</h2>
<p>Released under the <strong>MIT License</strong>. See the <a href="https://urldefense.com/v3/__http://LICENSE__;!!PFzsKvxRBh-H!b9x36Ji6NuqlbpBfsrUNwL2B7mXOJyH2EMJx9QmXyUO8CiLSLCG7tPET26OUhPVT8to71v9aL0Lt$">LICENSE</a> file.</p>
<hr />
</div>
<div id="suggested-citations" class="section level2">
<h2>Suggested Citations</h2>
<ul>
<li>Abelson J, Li K, Wilson G, Shields K, Schneider C, Boesveld S.
Supporting quality patient and public engagement in health system
organizations: development and usability testing of the PEIRS tool.
<em>Health Expectations</em>. 2016;19(4):817–827. <a href="https://urldefense.com/v3/__https://doi.org/10.1111/hex.12378__;!!PFzsKvxRBh-H!b9x36Ji6NuqlbpBfsrUNwL2B7mXOJyH2EMJx9QmXyUO8CiLSLCG7tPET26OUhPVT8to71pPkDiE2$" class="uri">https://doi.org/10.1111/hex.12378</a><br />
</li>
<li><strong>PEIR-IDEAS</strong> (pre-CRAN). “calculate_peirs_score():
Scoring the Patients Engaged in Research Scale (PEIRS) - IDEAS in R.”
GitHub: quantlover/PEIR-IDEAS, 2025.</li>
</ul>
</div>
</div>




</div>

<script>

// add bootstrap table styles to pandoc tables
function bootstrapStylePandocTables() {
  $('tr.odd').parent('tbody').parent('table').addClass('table table-condensed');
}
$(document).ready(function () {
  bootstrapStylePandocTables();
});


</script>

<!-- tabsets -->

<script>
$(document).ready(function () {
  window.buildTabsets("TOC");
});

$(document).ready(function () {
  $('.tabset-dropdown > .nav-tabs > li').click(function () {
    $(this).parent().toggleClass('nav-tabs-open');
  });
});
</script>

<!-- code folding -->


<!-- dynamically load mathjax for compatibility with self-contained -->
<script>
  (function () {
    var script = document.createElement("script");
    script.type = "text/javascript";
    script.src  = "https://mathjax.rstudio.com/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML";
    document.getElementsByTagName("head")[0].appendChild(script);
  })();
</script>

</body>
</html>

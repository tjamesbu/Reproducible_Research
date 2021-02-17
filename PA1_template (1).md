


      
  <div id="readme" class="Box-body readme blob js-code-block-container p-5 p-xl-6 gist-border-0">
    <article class="markdown-body entry-content container-lg" itemprop="text"><table data-table-type="yaml-metadata">
  <thead>
  <tr>
  <th>title</th>
  <th>output</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div>Reproducible Research: Peer Assessment 1</div></td>
  <td><div><table>
  <thead>
  <tr>
  <th>html_document</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div><table>
  <thead>
  <tr>
  <th>keep_md</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div>true</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table>

<h2><a id="user-content-introduction" class="anchor" aria-hidden="true" href="#introduction"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Introduction</h2>
<p>This is an R Markdown document, created for the Coursera course "Reproducible Research", in completion of "Peer Assessment 1". The assignment requires students to write an R markdown document evidencing literate programming, using markdown and R programming techniques. There are 5 primary questions to be answered, dealing with processing and analysing data. The data provided to be worked upon, is called "activity monitoring data".</p>
<h3><a id="user-content-the-data" class="anchor" aria-hidden="true" href="#the-data"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>The Data</h3>
<p>The data provided for use, is derived from a study whereupon a single individual wore a "personal activity monitoring device". The study says that:</p>
<blockquote>
<p>"[Activity monitoring devices] are part of the “quantified self” movement – a group of enthusiasts who take measurements about themselves regularly to improve their health, to find patterns in their behavior, or because they are tech geeks. But these data remain under-utilized both because the raw data are hard to obtain and there is a lack of statistical methods and software for processing and interpreting the data."</p>
</blockquote>
<p>The device used in this particular data set collects data on the number of steps taken by an individual, in 5 minute intervals. Two months of data, October/November 2012 are included within the data set. The variables measured include steps (the number of steps taken), date (the day on which the steps measurement was taken) and interval, (the interval in which the steps measurement was taken.) The data is stored in csv format, with 17,598 observations and the aforementioned 3 variables recorded.</p>
<h2><a id="user-content-completing-the-assignment" class="anchor" aria-hidden="true" href="#completing-the-assignment"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Completing the Assignment</h2>
<h3><a id="user-content-question-1-loading-and-preprocessing-the-data" class="anchor" aria-hidden="true" href="#question-1-loading-and-preprocessing-the-data"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Question 1: Loading and preprocessing the data</h3>
<p>The data must be in the user's current working directory for the code to run correctly. The unzip function extracts the data from the zip file, before it is read into R. The object classes contained within each of the variables are defined, so as to speed up the reading process.</p>
<div class="highlight highlight-source-r"><pre>unzip(<span class="pl-s"><span class="pl-pds">"</span>activity.zip<span class="pl-pds">"</span></span>)
<span class="pl-smi">initialData</span> <span class="pl-k">&lt;-</span> read.csv(<span class="pl-s"><span class="pl-pds">"</span>activity.csv<span class="pl-pds">"</span></span>, <span class="pl-v">colClasses</span><span class="pl-k">=</span>c(<span class="pl-s"><span class="pl-pds">"</span>numeric<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>Date<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>numeric<span class="pl-pds">"</span></span>))</pre></div>
<p>An initial look at the data confirms its dimensions and contents.</p>
<div class="highlight highlight-source-r"><pre>head(<span class="pl-smi">initialData</span>)</pre></div>
<pre><code>##   steps       date interval
## 1    NA 2012-10-01        0
## 2    NA 2012-10-01        5
## 3    NA 2012-10-01       10
## 4    NA 2012-10-01       15
## 5    NA 2012-10-01       20
## 6    NA 2012-10-01       25
</code></pre>
<div class="highlight highlight-source-r"><pre>str(<span class="pl-smi">initialData</span>)</pre></div>
<pre><code>## 'data.frame':	17568 obs. of  3 variables:
##  $ steps   : num  NA NA NA NA NA NA NA NA NA NA ...
##  $ date    : Date, format: "2012-10-01" "2012-10-01" ...
##  $ interval: num  0 5 10 15 20 25 30 35 40 45 ...
</code></pre>
<h3><a id="user-content-question-2-what-is-mean-total-number-of-steps-taken-per-day" class="anchor" aria-hidden="true" href="#question-2-what-is-mean-total-number-of-steps-taken-per-day"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Question 2: What is mean total number of steps taken per day?</h3>
<p>The question states any missing values in the data set can be ignored. From using the summary functions previously, it is already known that there are NA values within the steps variable, so these can be removed now.</p>
<div class="highlight highlight-source-r"><pre><span class="pl-smi">data</span> <span class="pl-k">&lt;-</span> <span class="pl-smi">initialData</span>[<span class="pl-k">!</span>(is.na(<span class="pl-smi">initialData</span><span class="pl-k">$</span><span class="pl-smi">steps</span>)), ]</pre></div>
<p>To calculate the total number of steps taken per day, the data first needs to be grouped separately for each day, and then the sum of each group calculated. The aggregate function can complete both of these steps, and format the output in a tidy data frame.</p>
<div class="highlight highlight-source-r"><pre><span class="pl-smi">totalStepsDay</span> <span class="pl-k">&lt;-</span> aggregate(<span class="pl-smi">steps</span> <span class="pl-k">~</span> <span class="pl-smi">date</span>, <span class="pl-smi">data</span>, <span class="pl-smi">sum</span>)
head(<span class="pl-smi">totalStepsDay</span>)</pre></div>
<pre><code>##         date steps
## 1 2012-10-02   126
## 2 2012-10-03 11352
## 3 2012-10-04 12116
## 4 2012-10-05 13294
## 5 2012-10-06 15420
## 6 2012-10-07 11015
</code></pre>
<p>Creating exploratory plots are useful to be able to quickly see a view of all of the data, and pick out any potential patterns. Here, a histogram is created to indicate the frequency of total steps taken each day.</p>
<div class="highlight highlight-source-r"><pre><span class="pl-smi">paletteBlue</span> <span class="pl-k">&lt;-</span> colorRampPalette(c(<span class="pl-s"><span class="pl-pds">"</span>skyblue<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>darkblue<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>skyblue<span class="pl-pds">"</span></span>))
hist(<span class="pl-smi">totalStepsDay</span><span class="pl-k">$</span><span class="pl-smi">steps</span>, <span class="pl-v">breaks</span><span class="pl-k">=</span><span class="pl-c1">20</span>, <span class="pl-v">xlab</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Number of Steps Taken<span class="pl-pds">"</span></span>, 
     <span class="pl-v">main</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Histogram of the Total Number of Steps Taken per Day<span class="pl-pds">"</span></span>,
     <span class="pl-v">col</span><span class="pl-k">=</span>paletteBlue(<span class="pl-c1">22</span>), <span class="pl-v">family</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>serif<span class="pl-pds">"</span></span>)</pre></div>
<p><a target="_blank" rel="noopener noreferrer" href="/tjamesbu/Reproducible-Research-Course-Project-1/blob/master/figure/unnamed-chunk-5-1.png"><img src="/tjamesbu/Reproducible-Research-Course-Project-1/raw/master/figure/unnamed-chunk-5-1.png" alt="plot of chunk unnamed-chunk-5" style="max-width:100%;"></a></p>
<p>Finally, the summarise function can calculate the mean and median values of the total number of steps taken per day.</p>
<div class="highlight highlight-source-r"><pre>library(<span class="pl-smi">dplyr</span>)
<span class="pl-smi">totalStepsSummary</span> <span class="pl-k">&lt;-</span> summarise(<span class="pl-smi">totalStepsDay</span>, <span class="pl-v">meanOfTotalSteps</span><span class="pl-k">=</span>mean(<span class="pl-smi">totalStepsDay</span><span class="pl-k">$</span><span class="pl-smi">steps</span>),
                               <span class="pl-v">medianOfTotalSteps</span><span class="pl-k">=</span>median(<span class="pl-smi">totalStepsDay</span><span class="pl-k">$</span><span class="pl-smi">steps</span>))
print(<span class="pl-smi">totalStepsSummary</span>)</pre></div>
<pre><code>##   meanOfTotalSteps medianOfTotalSteps
## 1         10766.19              10765
</code></pre>
<p>Therefore the mean value calculated is <strong>10766.19</strong>, and the median value <strong>10765</strong>.</p>
<h3><a id="user-content-question-3-what-is-the-average-daily-activity-pattern" class="anchor" aria-hidden="true" href="#question-3-what-is-the-average-daily-activity-pattern"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Question 3: What is the average daily activity pattern?</h3>
<p>To look at the average daily pattern, we can use another exploratory graph, this time a time series plot. As this plot should look at the average number of steps taken for each interval, (utilising all days), the aggregate function must be used again, to split the data into groups for each interval, and then averaged with the mean function.</p>
<div class="highlight highlight-source-r"><pre><span class="pl-smi">meanStepsInterval</span> <span class="pl-k">&lt;-</span> aggregate(<span class="pl-smi">steps</span> <span class="pl-k">~</span> <span class="pl-smi">interval</span>, <span class="pl-smi">data</span>, <span class="pl-smi">mean</span>)
head(<span class="pl-smi">meanStepsInterval</span>)</pre></div>
<pre><code>##   interval     steps
## 1        0 1.7169811
## 2        5 0.3396226
## 3       10 0.1320755
## 4       15 0.1509434
## 5       20 0.0754717
## 6       25 2.0943396
</code></pre>
<p>The base R plotting system is used to create a time series plot, with each interval on the x axis, and the average steps data on the y axis.</p>
<div class="highlight highlight-source-r"><pre>plot(<span class="pl-v">x</span><span class="pl-k">=</span><span class="pl-smi">meanStepsInterval</span><span class="pl-k">$</span><span class="pl-smi">interval</span>, <span class="pl-v">y</span><span class="pl-k">=</span><span class="pl-smi">meanStepsInterval</span><span class="pl-k">$</span><span class="pl-smi">steps</span>, <span class="pl-v">type</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>l<span class="pl-pds">"</span></span>,
     <span class="pl-v">main</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Time Series Plot of Average Steps Taken per Interval<span class="pl-pds">"</span></span>,
     <span class="pl-v">ylab</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Number of Steps<span class="pl-pds">"</span></span>, <span class="pl-v">xlab</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Intervals (in 5 mins)<span class="pl-pds">"</span></span>,
     <span class="pl-v">col</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>darkblue<span class="pl-pds">"</span></span>, <span class="pl-v">lwd</span><span class="pl-k">=</span><span class="pl-c1">1.5</span>, <span class="pl-v">family</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>serif<span class="pl-pds">"</span></span>)</pre></div>
<p><a target="_blank" rel="noopener noreferrer" href="/tjamesbu/Reproducible-Research-Course-Project-1/blob/master/figure/unnamed-chunk-8-1.png"><img src="/tjamesbu/Reproducible-Research-Course-Project-1/raw/master/figure/unnamed-chunk-8-1.png" alt="plot of chunk unnamed-chunk-8" style="max-width:100%;"></a></p>
<p>The last part of this question asks "which five minute interval contains the maximum number of steps?" To answer this the max function can be used, which prints out the maximum value from a numeric vector.</p>
<div class="highlight highlight-source-r"><pre><span class="pl-smi">meanStepsInterval</span>[grep(max(<span class="pl-smi">meanStepsInterval</span><span class="pl-k">$</span><span class="pl-smi">steps</span>), <span class="pl-smi">meanStepsInterval</span><span class="pl-k">$</span><span class="pl-smi">steps</span>), ]</pre></div>
<pre><code>##     interval    steps
## 104      835 206.1698
</code></pre>
<p>So the interval with the maximum number of steps is interval <strong>835</strong>.</p>
<h3><a id="user-content-question-4-imputing-missing-values" class="anchor" aria-hidden="true" href="#question-4-imputing-missing-values"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Question 4: Imputing missing values</h3>
<p>As the data can be confirmed to contain some NA values as some of the observations:</p>
<div class="highlight highlight-source-r"><pre>anyNA(<span class="pl-smi">initialData</span>)</pre></div>
<pre><code>## [1] TRUE
</code></pre>
<p>It is necessary to find out whether the NA values are more-so clustered to one area within the data. Looking at each of the variables:</p>
<div class="highlight highlight-source-r"><pre><span class="pl-k">data.frame</span>(<span class="pl-v">steps</span><span class="pl-k">=</span>sum(is.na(<span class="pl-smi">initialData</span><span class="pl-k">$</span><span class="pl-smi">steps</span>)), 
           <span class="pl-v">interval</span><span class="pl-k">=</span>sum(is.na(<span class="pl-smi">initialData</span><span class="pl-k">$</span><span class="pl-smi">interval</span>)), 
           <span class="pl-v">date</span><span class="pl-k">=</span>sum(is.na(<span class="pl-smi">initialData</span><span class="pl-k">$</span><span class="pl-smi">date</span>)))</pre></div>
<pre><code>##   steps interval date
## 1  2304        0    0
</code></pre>
<p>It can be seen that all 2304 NA values are contained within the steps variable.</p>
<p>Therefore an imputing strategy must be devised to replace all of these missing values with usable numeric measurements. To do so, I decided to replace each missing value with the mean value for the same interval, averaged across all days.</p>
<p>I used a for loop to achieve this, first testing if each observation was an NA value, and if so, replacing it with the mean average for that interval, (as calculated in a previous question).</p>
<div class="highlight highlight-source-r"><pre><span class="pl-smi">imputedData</span> <span class="pl-k">&lt;-</span> <span class="pl-smi">initialData</span>
<span class="pl-k">for</span>(<span class="pl-smi">x</span> <span class="pl-k">in</span> <span class="pl-c1">1</span><span class="pl-k">:</span><span class="pl-c1">17568</span>) {
    <span class="pl-k">if</span>(is.na(<span class="pl-smi">imputedData</span>[<span class="pl-smi">x</span>, <span class="pl-c1">1</span>])<span class="pl-k">==</span><span class="pl-c1">TRUE</span>) {
        <span class="pl-smi">imputedData</span>[<span class="pl-smi">x</span>, <span class="pl-c1">1</span>] <span class="pl-k">&lt;-</span> <span class="pl-smi">meanStepsInterval</span>[<span class="pl-smi">meanStepsInterval</span><span class="pl-k">$</span><span class="pl-smi">interval</span> <span class="pl-k">%in%</span> <span class="pl-smi">imputedData</span>[<span class="pl-smi">x</span>, <span class="pl-c1">3</span>], <span class="pl-c1">2</span>]
    }
}
head(<span class="pl-smi">imputedData</span>)</pre></div>
<pre><code>##       steps       date interval
## 1 1.7169811 2012-10-01        0
## 2 0.3396226 2012-10-01        5
## 3 0.1320755 2012-10-01       10
## 4 0.1509434 2012-10-01       15
## 5 0.0754717 2012-10-01       20
## 6 2.0943396 2012-10-01       25
</code></pre>
<p>Now that the NA values have been replaced, a histogram from the imputed data can be created. This histogram should indicate the frequency of the total number of steps taken per day. Therefore again, the data must be grouped and "summed" by day.</p>
<div class="highlight highlight-source-r"><pre><span class="pl-smi">imputedTotalStepsDay</span> <span class="pl-k">&lt;-</span> aggregate(<span class="pl-smi">steps</span> <span class="pl-k">~</span> <span class="pl-smi">date</span>, <span class="pl-smi">imputedData</span>, <span class="pl-smi">sum</span>)
head(<span class="pl-smi">imputedTotalStepsDay</span>)</pre></div>
<pre><code>##         date    steps
## 1 2012-10-01 10766.19
## 2 2012-10-02   126.00
## 3 2012-10-03 11352.00
## 4 2012-10-04 12116.00
## 5 2012-10-05 13294.00
## 6 2012-10-06 15420.00
</code></pre>
<p>Creating the histogram:</p>
<div class="highlight highlight-source-r"><pre><span class="pl-smi">paletteRed</span> <span class="pl-k">&lt;-</span> colorRampPalette(c(<span class="pl-s"><span class="pl-pds">"</span>deeppink<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>darkred<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>deeppink<span class="pl-pds">"</span></span>))
hist(<span class="pl-smi">imputedTotalStepsDay</span><span class="pl-k">$</span><span class="pl-smi">steps</span>, <span class="pl-v">breaks</span><span class="pl-k">=</span><span class="pl-c1">20</span>, <span class="pl-v">xlab</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Number of Steps Taken<span class="pl-pds">"</span></span>, 
     <span class="pl-v">main</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Histogram of Total Number of Steps Taken per Day (With Imputed Values)<span class="pl-pds">"</span></span>,
     <span class="pl-v">col</span><span class="pl-k">=</span>paletteRed(<span class="pl-c1">22</span>), <span class="pl-v">family</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>serif<span class="pl-pds">"</span></span>)</pre></div>
<p><a target="_blank" rel="noopener noreferrer" href="/tjamesbu/Reproducible-Research-Course-Project-1/blob/master/figure/unnamed-chunk-14-1.png"><img src="/tjamesbu/Reproducible-Research-Course-Project-1/raw/master/figure/unnamed-chunk-14-1.png" alt="plot of chunk unnamed-chunk-14" style="max-width:100%;"></a></p>
<p>The question then asks for calculation of the mean and median total number of steps taken per day, which can be calculated using the summarise function.</p>
<div class="highlight highlight-source-r"><pre><span class="pl-smi">imputedStepsSummary</span> <span class="pl-k">&lt;-</span> summarise(<span class="pl-smi">imputedTotalStepsDay</span>, 
                                 <span class="pl-v">meanOfTotalSteps</span><span class="pl-k">=</span>mean(<span class="pl-smi">imputedTotalStepsDay</span><span class="pl-k">$</span><span class="pl-smi">steps</span>), 
                                 <span class="pl-v">medianOfTotalSteps</span><span class="pl-k">=</span>median(<span class="pl-smi">imputedTotalStepsDay</span><span class="pl-k">$</span><span class="pl-smi">steps</span>))  
print(<span class="pl-smi">imputedStepsSummary</span>)</pre></div>
<pre><code>##   meanOfTotalSteps medianOfTotalSteps
## 1         10766.19           10766.19
</code></pre>
<p>This a similar calculation to the one completed at the start of the assignment, (without the imputed values,) and thus they can be compared.</p>
<div class="highlight highlight-source-r"><pre>rbind(<span class="pl-smi">totalStepsSummary</span>, <span class="pl-smi">imputedTotalStepsSummary</span>)</pre></div>
<pre><code>##   meanOfTotalSteps medianOfTotalSteps
## 1         10766.19           10765.00
## 2         10766.19           10766.19
</code></pre>
<p>The values of the two data sets are very similar, if not exactly the same, due to the use of averaging functions when imputing the NA measurements. The mean values are the same, at <strong>10766.19</strong> steps, while the median value is slightly larger for the imputed data set, at <strong>10766.19</strong> steps, rather than <strong>10765</strong> steps.</p>
<p>If histograms of the two data sets (imputed and non-imputed) are compared:</p>
<div class="highlight highlight-source-r"><pre>par(<span class="pl-v">mfrow</span> <span class="pl-k">=</span> c(<span class="pl-c1">1</span>, <span class="pl-c1">2</span>))

hist(<span class="pl-smi">totalStepsDay</span><span class="pl-k">$</span><span class="pl-smi">steps</span>, <span class="pl-v">breaks</span><span class="pl-k">=</span><span class="pl-c1">20</span>, <span class="pl-v">xlab</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Number of Steps Taken<span class="pl-pds">"</span></span>, 
     <span class="pl-v">col</span><span class="pl-k">=</span>paletteBlue(<span class="pl-c1">22</span>), <span class="pl-v">family</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>serif<span class="pl-pds">"</span></span>, <span class="pl-v">ylim</span><span class="pl-k">=</span>c(<span class="pl-c1">0</span>, <span class="pl-c1">20</span>), <span class="pl-v">main</span><span class="pl-k">=</span><span class="pl-c1">NULL</span>)
hist(<span class="pl-smi">imputedTotalStepsDay</span><span class="pl-k">$</span><span class="pl-smi">steps</span>, <span class="pl-v">breaks</span><span class="pl-k">=</span><span class="pl-c1">20</span>, <span class="pl-v">xlab</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Number of Steps Taken<span class="pl-pds">"</span></span>, 
     <span class="pl-v">col</span><span class="pl-k">=</span>paletteRed(<span class="pl-c1">22</span>), <span class="pl-v">family</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>serif<span class="pl-pds">"</span></span>, <span class="pl-v">ylim</span><span class="pl-k">=</span>c(<span class="pl-c1">0</span>, <span class="pl-c1">20</span>), <span class="pl-v">main</span><span class="pl-k">=</span><span class="pl-c1">NULL</span>)
mtext(<span class="pl-s"><span class="pl-pds">"</span>Histograms of Total Number of Steps Taken per Day, Without/With Imputed Values<span class="pl-pds">"</span></span>,
      <span class="pl-v">adj</span><span class="pl-k">=</span><span class="pl-c1">0.95</span>, <span class="pl-v">family</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>serif<span class="pl-pds">"</span></span>, <span class="pl-v">font</span><span class="pl-k">=</span><span class="pl-c1">2</span>)</pre></div>
<p><a target="_blank" rel="noopener noreferrer" href="/tjamesbu/Reproducible-Research-Course-Project-1/blob/master/figure/unnamed-chunk-17-1.png"><img src="/tjamesbu/Reproducible-Research-Course-Project-1/raw/master/figure/unnamed-chunk-17-1.png" alt="plot of chunk unnamed-chunk-17" style="max-width:100%;"></a></p>
<p>It can be seen that the frequency of values increases in the second histogram, which is expected, due to the imputed values.</p>
<p>More explanations for the differences between the non and imputed data sets can be seen by looking at the NA values grouped by their date variable.</p>
<div class="highlight highlight-source-r"><pre><span class="pl-smi">naByDate</span> <span class="pl-k">&lt;-</span> <span class="pl-smi">initialData</span>[is.na(<span class="pl-smi">initialData</span><span class="pl-k">$</span><span class="pl-smi">steps</span>), ]
table(<span class="pl-smi">naByDate</span><span class="pl-k">$</span><span class="pl-smi">date</span>)</pre></div>
<pre><code>## 
## 2012-10-01 2012-10-08 2012-11-01 2012-11-04 2012-11-09 2012-11-10 
##        288        288        288        288        288        288 
## 2012-11-14 2012-11-30 
##        288        288
</code></pre>
<p>As there are exactly 288 intervals measured for each day:</p>
<div class="highlight highlight-source-r"><pre>length(unique(<span class="pl-smi">data</span><span class="pl-k">$</span><span class="pl-smi">interval</span>))</pre></div>
<pre><code>## [1] 288
</code></pre>
<p>It is therefore shown by the above table, that in the initial data set, missing observations are due to entirely missed days, (8 of the days) where no measurements were made whatsoever. This therefore reinforces that the imputing technique used, of utilising average interval data, was likely more useful than potentially using average daily data.</p>
<h3><a id="user-content-question-5-are-there-differences-in-activity-patterns-between-weekdays-and-weekends" class="anchor" aria-hidden="true" href="#question-5-are-there-differences-in-activity-patterns-between-weekdays-and-weekends"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Question 5: Are there differences in activity patterns between weekdays and weekends?</h3>
<p>The question indicates that the imputed data set should be used to answer this problem.<br>
To help in answering this question, firstly a new factor variable should be created within the data frame. This should indicate whether each day is a "weekday" or a "weekend".</p>
<p>To achieve this, I used the weekdays function to automatically calculate the day of the week each day resided upon, (Monday, Tuesday, etc.) Next, I wrote a for loop, which would assign the factor value "weekend" to all rows it read as having the values "Saturday" or "Sunday", and assign "weekday" to the others.</p>
<div class="highlight highlight-source-r"><pre><span class="pl-smi">daysData</span> <span class="pl-k">&lt;-</span> <span class="pl-smi">imputedData</span>
<span class="pl-smi">daysData</span><span class="pl-k">$</span><span class="pl-smi">days</span> <span class="pl-k">&lt;-</span> weekdays(<span class="pl-smi">daysData</span><span class="pl-k">$</span><span class="pl-smi">date</span>)
<span class="pl-smi">daysData</span><span class="pl-k">$</span><span class="pl-smi">weekday</span> <span class="pl-k">&lt;-</span> as.character(rep(<span class="pl-c1">0</span>, <span class="pl-v">times</span><span class="pl-k">=</span><span class="pl-c1">17568</span>))
<span class="pl-k">for</span>(<span class="pl-smi">x</span> <span class="pl-k">in</span> <span class="pl-c1">1</span><span class="pl-k">:</span><span class="pl-c1">17568</span>) {
    <span class="pl-k">if</span>(<span class="pl-smi">daysData</span>[<span class="pl-smi">x</span>, <span class="pl-c1">4</span>] <span class="pl-k">%in%</span> c(<span class="pl-s"><span class="pl-pds">"</span>Saturday<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>Sunday<span class="pl-pds">"</span></span>)) {
        <span class="pl-smi">daysData</span>[<span class="pl-smi">x</span>, <span class="pl-c1">5</span>] <span class="pl-k">&lt;-</span> <span class="pl-s"><span class="pl-pds">"</span>weekend<span class="pl-pds">"</span></span>
    } <span class="pl-k">else</span> {
        <span class="pl-smi">daysData</span>[<span class="pl-smi">x</span>, <span class="pl-c1">5</span>] <span class="pl-k">&lt;-</span> <span class="pl-s"><span class="pl-pds">"</span>weekday<span class="pl-pds">"</span></span>
    }
}
<span class="pl-smi">daysData</span><span class="pl-k">$</span><span class="pl-smi">weekday</span> <span class="pl-k">&lt;-</span> <span class="pl-k">factor</span>(<span class="pl-smi">daysData</span><span class="pl-k">$</span><span class="pl-smi">weekday</span>)
head(<span class="pl-smi">daysData</span>)</pre></div>
<pre><code>##       steps       date interval   days weekday
## 1 1.7169811 2012-10-01        0 Monday weekday
## 2 0.3396226 2012-10-01        5 Monday weekday
## 3 0.1320755 2012-10-01       10 Monday weekday
## 4 0.1509434 2012-10-01       15 Monday weekday
## 5 0.0754717 2012-10-01       20 Monday weekday
## 6 2.0943396 2012-10-01       25 Monday weekday
</code></pre>
<p>To compare the weekday and weekend data, and create two plots of the average number of steps taken per interval, the data has to be split into two groups of weekday/weekend data, using the newly created variable.</p>
<div class="highlight highlight-source-r"><pre><span class="pl-smi">weekdayData</span> <span class="pl-k">&lt;-</span> <span class="pl-smi">daysData</span>[<span class="pl-smi">daysData</span><span class="pl-k">$</span><span class="pl-smi">weekday</span><span class="pl-k">==</span><span class="pl-s"><span class="pl-pds">"</span>weekday<span class="pl-pds">"</span></span>, ]
<span class="pl-smi">weekendData</span> <span class="pl-k">&lt;-</span> <span class="pl-smi">daysData</span>[<span class="pl-smi">daysData</span><span class="pl-k">$</span><span class="pl-smi">weekday</span><span class="pl-k">==</span><span class="pl-s"><span class="pl-pds">"</span>weekend<span class="pl-pds">"</span></span>, ]</pre></div>
<p>Next, the average number of steps per interval is calculated, much like it has been done in previous questions.</p>
<div class="highlight highlight-source-r"><pre><span class="pl-smi">weekdayMean</span> <span class="pl-k">&lt;-</span> aggregate(<span class="pl-smi">steps</span> <span class="pl-k">~</span> <span class="pl-smi">interval</span>, <span class="pl-smi">weekdayData</span>, <span class="pl-smi">mean</span>)
<span class="pl-smi">weekendMean</span> <span class="pl-k">&lt;-</span> aggregate(<span class="pl-smi">steps</span> <span class="pl-k">~</span> <span class="pl-smi">interval</span>, <span class="pl-smi">weekendData</span>, <span class="pl-smi">mean</span>)</pre></div>
<p>Finally the panel plot is created. The x axis indicates each 5 minute interval, and the y axis shows the average number of steps taken. The two plots are divided into weekday, and weekend data.</p>
<div class="highlight highlight-source-r"><pre>par(<span class="pl-v">mfrow</span><span class="pl-k">=</span>c(<span class="pl-c1">2</span>, <span class="pl-c1">1</span>), <span class="pl-v">mar</span><span class="pl-k">=</span>c(<span class="pl-c1">4</span>, <span class="pl-c1">4.1</span>, <span class="pl-c1">3</span>, <span class="pl-c1">2.1</span>))
plot(<span class="pl-smi">weekdayMean</span><span class="pl-k">$</span><span class="pl-smi">interval</span>, <span class="pl-smi">weekdayMean</span><span class="pl-k">$</span><span class="pl-smi">steps</span>, <span class="pl-v">type</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>l<span class="pl-pds">"</span></span>,
     <span class="pl-v">main</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Time Series Plot of Average Steps Taken per Interval, for Weekdays<span class="pl-pds">"</span></span>,
     <span class="pl-v">xlab</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Intervals (in 5 mins)<span class="pl-pds">"</span></span>, <span class="pl-v">ylab</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Number of Steps<span class="pl-pds">"</span></span>, <span class="pl-v">family</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>serif<span class="pl-pds">"</span></span>,
     <span class="pl-v">col</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>darkred<span class="pl-pds">"</span></span>, <span class="pl-v">lwd</span><span class="pl-k">=</span><span class="pl-c1">1.5</span>, <span class="pl-v">ylim</span><span class="pl-k">=</span>c(<span class="pl-c1">0</span>, <span class="pl-c1">230</span>))
plot(<span class="pl-smi">weekendMean</span><span class="pl-k">$</span><span class="pl-smi">interval</span>, <span class="pl-smi">weekendMean</span><span class="pl-k">$</span><span class="pl-smi">steps</span>, <span class="pl-v">type</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>l<span class="pl-pds">"</span></span>,
     <span class="pl-v">main</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Time Series Plot of Average Steps Taken per Interval, for Weekends<span class="pl-pds">"</span></span>,
     <span class="pl-v">xlab</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Intervals (in 5 mins)<span class="pl-pds">"</span></span>, <span class="pl-v">ylab</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Number of Steps<span class="pl-pds">"</span></span>, <span class="pl-v">family</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>serif<span class="pl-pds">"</span></span>,
     <span class="pl-v">col</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>darkblue<span class="pl-pds">"</span></span>, <span class="pl-v">lwd</span><span class="pl-k">=</span><span class="pl-c1">1.5</span>, <span class="pl-v">ylim</span><span class="pl-k">=</span>c(<span class="pl-c1">0</span>, <span class="pl-c1">230</span>))</pre></div>
<p><a target="_blank" rel="noopener noreferrer" href="/tjamesbu/Reproducible-Research-Course-Project-1/blob/master/figure/unnamed-chunk-23-1.png"><img src="/tjamesbu/Reproducible-Research-Course-Project-1/raw/master/figure/unnamed-chunk-23-1.png" alt="plot of chunk unnamed-chunk-23" style="max-width:100%;"></a></p>
</article>
  </div>

    </div>

  

  <details class="details-reset details-overlay details-overlay-dark" id="jumpto-line-details-dialog">
    <summary data-hotkey="l" aria-label="Jump to line"></summary>
    <details-dialog class="Box Box--overlay d-flex flex-column anim-fade-in fast linejump" aria-label="Jump to line">
      <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="js-jump-to-line-form Box-body d-flex" action="" accept-charset="UTF-8" method="get">
        <input class="form-control flex-auto mr-3 linejump-input js-jump-to-line-field" type="text" placeholder="Jump to line&hellip;" aria-label="Jump to line" autofocus>
        <button type="submit" class="btn" data-close-dialog>Go</button>
</form>    </details-dialog>
  </details>


</div>



  </div>
</div>

    </main>
  </div>

  </div>

          
<div class="footer container-xl width-full p-responsive" role="contentinfo">
  <div class="position-relative d-flex flex-row-reverse flex-lg-row flex-wrap flex-lg-nowrap flex-justify-center flex-lg-justify-between pt-6 pb-2 mt-6 f6 text-gray border-top color-border-secondary ">
    <ul class="list-style-none d-flex flex-wrap col-12 col-lg-5 flex-justify-center flex-lg-justify-between mb-2 mb-lg-0">
      <li class="mr-3 mr-lg-0">&copy; 2021 GitHub, Inc.</li>
        <li class="mr-3 mr-lg-0"><a data-ga-click="Footer, go to terms, text:terms" href="https://github.com/site/terms">Terms</a></li>
        <li class="mr-3 mr-lg-0"><a data-ga-click="Footer, go to privacy, text:privacy" href="https://github.com/site/privacy">Privacy</a></li>
        <li class="mr-3 mr-lg-0"><a data-ga-click="Footer, go to security, text:security" href="https://github.com/security">Security</a></li>
        <li class="mr-3 mr-lg-0"><a href="https://www.githubstatus.com/" data-ga-click="Footer, go to status, text:status">Status</a></li>
        <li><a data-ga-click="Footer, go to help, text:Docs" href="https://docs.github.com">Docs</a></li>
    </ul>

    <a aria-label="Homepage" title="GitHub" class="footer-octicon d-none d-lg-block mx-lg-4" href="https://github.com">
      <svg height="24" class="octicon octicon-mark-github" viewBox="0 0 16 16" version="1.1" width="24" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"></path></svg>
</a>
    <ul class="list-style-none d-flex flex-wrap col-12 col-lg-5 flex-justify-center flex-lg-justify-between mb-2 mb-lg-0">
        <li class="mr-3 mr-lg-0"><a data-ga-click="Footer, go to contact, text:contact" href="https://github.com/contact">Contact GitHub</a></li>
        <li class="mr-3 mr-lg-0"><a href="https://github.com/pricing" data-ga-click="Footer, go to Pricing, text:Pricing">Pricing</a></li>
      <li class="mr-3 mr-lg-0"><a href="https://docs.github.com" data-ga-click="Footer, go to api, text:api">API</a></li>
      <li class="mr-3 mr-lg-0"><a href="https://services.github.com" data-ga-click="Footer, go to training, text:training">Training</a></li>
        <li class="mr-3 mr-lg-0"><a href="https://github.blog" data-ga-click="Footer, go to blog, text:blog">Blog</a></li>
        <li><a data-ga-click="Footer, go to about, text:about" href="https://github.com/about">About</a></li>
    </ul>
  </div>
  <div class="d-flex flex-justify-center pb-6">
    <span class="f6 text-gray-light"></span>
  </div>

  
</div>



  <div id="ajax-error-message" class="ajax-error-message flash flash-error" hidden>
    <svg class="octicon octicon-alert" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.22 1.754a.25.25 0 00-.44 0L1.698 13.132a.25.25 0 00.22.368h12.164a.25.25 0 00.22-.368L8.22 1.754zm-1.763-.707c.659-1.234 2.427-1.234 3.086 0l6.082 11.378A1.75 1.75 0 0114.082 15H1.918a1.75 1.75 0 01-1.543-2.575L6.457 1.047zM9 11a1 1 0 11-2 0 1 1 0 012 0zm-.25-5.25a.75.75 0 00-1.5 0v2.5a.75.75 0 001.5 0v-2.5z"></path></svg>
    <button type="button" class="flash-close js-ajax-error-dismiss" aria-label="Dismiss error">
      <svg class="octicon octicon-x" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M3.72 3.72a.75.75 0 011.06 0L8 6.94l3.22-3.22a.75.75 0 111.06 1.06L9.06 8l3.22 3.22a.75.75 0 11-1.06 1.06L8 9.06l-3.22 3.22a.75.75 0 01-1.06-1.06L6.94 8 3.72 4.78a.75.75 0 010-1.06z"></path></svg>
    </button>
    You can’t perform that action at this time.
  </div>

  <div class="js-stale-session-flash flash flash-warn flash-banner" hidden
    >
    <svg class="octicon octicon-alert" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.22 1.754a.25.25 0 00-.44 0L1.698 13.132a.25.25 0 00.22.368h12.164a.25.25 0 00.22-.368L8.22 1.754zm-1.763-.707c.659-1.234 2.427-1.234 3.086 0l6.082 11.378A1.75 1.75 0 0114.082 15H1.918a1.75 1.75 0 01-1.543-2.575L6.457 1.047zM9 11a1 1 0 11-2 0 1 1 0 012 0zm-.25-5.25a.75.75 0 00-1.5 0v2.5a.75.75 0 001.5 0v-2.5z"></path></svg>
    <span class="js-stale-session-flash-signed-in" hidden>You signed in with another tab or window. <a href="">Reload</a> to refresh your session.</span>
    <span class="js-stale-session-flash-signed-out" hidden>You signed out in another tab or window. <a href="">Reload</a> to refresh your session.</span>
  </div>
    <template id="site-details-dialog">
  <details class="details-reset details-overlay details-overlay-dark lh-default text-gray-dark hx_rsm" open>
    <summary role="button" aria-label="Close dialog"></summary>
    <details-dialog class="Box Box--overlay d-flex flex-column anim-fade-in fast hx_rsm-dialog hx_rsm-modal">
      <button class="Box-btn-octicon m-0 btn-octicon position-absolute right-0 top-0" type="button" aria-label="Close dialog" data-close-dialog>
        <svg class="octicon octicon-x" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M3.72 3.72a.75.75 0 011.06 0L8 6.94l3.22-3.22a.75.75 0 111.06 1.06L9.06 8l3.22 3.22a.75.75 0 11-1.06 1.06L8 9.06l-3.22 3.22a.75.75 0 01-1.06-1.06L6.94 8 3.72 4.78a.75.75 0 010-1.06z"></path></svg>
      </button>
      <div class="octocat-spinner my-6 js-details-dialog-spinner"></div>
    </details-dialog>
  </details>
</template>

    <div class="Popover js-hovercard-content position-absolute" style="display: none; outline: none;" tabindex="0">
  <div class="Popover-message Popover-message--bottom-left Popover-message--large Box box-shadow-large" style="width:360px;">
  </div>
</div>



  </body>
</html>


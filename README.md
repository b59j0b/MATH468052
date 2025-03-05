java c
MATH4/68052 Generalised Linear Models:    Coursework 
(2025) 
The   marks   awarded   for   this   coursework   constitute   30%   of the   total   assessment   for   the   module.Your   solution to the   coursework   should   be   reasonably   concise -   about   10   pages with   tables,   plots,   and   code,   but   there   is   no   penalty   if you   do   exceed   this.   It   should   take,   on   average,   about   9   hours   to   complete   all   the   work,   including   preparing   your   ﬁnal   document   to   be   submitted.
Please read all the instructions and advice given below carefully. The submission deadline is 10:00 am on Monday 10 March, 2025 .Late Submission of Work:   Any   student’s   work   that   is   submitted   after   the   given   deadline   will   be   classed   as   late,   unless   an   extension   has   already   been   agreed   via   mitigating   circumstances   or   a   DASS   extension.
The   following   rules   for   the   application   of penalties   for   late   submission   are   quoted   from   the   latest   University   policy   on   submission   of work   for   summative   assessment:”The   mark   awarded   will   reduce   by   10%   of   the   maximum   amount   available   per   24   hours   (e.g.    if   the   work   is   marked   out   of   100,   this   means   a   deduction   of   10   marks   per   24   hours   late.   If the   work   is   marked   out   of   20,   the   deduction   would   be   2   marks   each   24   hours   late.)    The   penalty   applies   as   soon   as   an   assignment   is   late;   a   10%   deduction   would   be   issued   if   an   assignment   is   submitted   immediately   after the   deadline,   and the work would   continue   to   attract   further   penalties   for   each   subsequent   24   hours   the   work   was   late,   until   the   assignment   is   submitted   or   no   marks   remain.”Your   submitted   solutions   should   all   be   in   one   typed   document.    This   should   be   prepared   using   LaTeX   or   R   Markdown.    For   each   question   you   should   provide   explanations   as   to   how   you   com-   pleted   what   is   required,   show   your   workings   and   also   comment   on   computational   results,   where   applicable.
When   you   include   a   plot,   be   sure   to   give   it   a   title   and   label   the   axes   correctly.When you have written or   used   R code   to   answer   any   of the   parts,   then   you   should   list   this   R code   after the particular written   answer to   which   it   applies.    This   may be   the   R   code   for   a   function   you   have   written   and/or   code   you   have   used   to   produce   numerical   results,   plots   and   tables.    R   code   should   also   be   clearly   annotated.
Do   not   use   screenshots   of   R   code/output.    Instead,   to   include   R   code,   use   the   verbatim   environ-   ment.Your ﬁle should be submitted through the module site on Blackboard to the Turnitin assessment    under    Assesment        Feedback    entitled    ’GLM’s    Coursework (2025)’ by the above time and date. The   work   will   be   marked   anonymously   on   Blackboard   so   please ensure that your ﬁlename is clear,   but   that   it   does   not   contain   your   name   and   student   id   number.   Similarly,   do   not   include   your   name   and   id   number   in   the   document   itself. Turnitin   will   generate   a   similarity   report   for   your   submitted   document   and   indicate   matches   to   other   sources,   including   billions   of   internet   documents      (both   live   and   archived),   a   subscription   repository   of   periodicals,   journals   and   publications,   as   well   as   submissions   from   other   students.   Please ensure that the document you   upload   represents   your   own   work   and   is   written   in   your   own   words.   The   Turnitin   report   will   be   available   for   you   to   see   shortly   after   the   due   date.This coursework should hopefully help to   reinforce   some   of the   methodology   you   have   been   study-   ing,   as   well   as   the   skills   in   R you   have   been   developing   in   the   module.    Correct   interpretation   and   meaningful   discussion   of   the   results   (i.e.    attempt   to   put   the   results   into   context)   are   important   in   order   to   achieve   a   high   mark   for   the   coursework.
1.    Suppose that we have   a random   sample   of data   pairs   (x1   ,   y1   ),   .   .   .   , (xn   ,   yn   ), where   theyi’s   are   observed   values   of   a   response   variable,   Y   ,   and   the   xi’s   are   associated   observed   values   of   a   numerical   covariate.
The   hypothesised   GLM   for   the   data   is:
yi   jxi      = µi    + ∈i      with   Yi   jxi      ~ N   (µi   ,   σ   2   )   and   E[∈i]   =   0,       i =   1, . . . ,   n
and
1/µi      = ηi    = β0    + β1   xi      = xiT β,      ,   i =   1,   .   .   .   ,   nYou   are   reminded   that   it   is   shown   in   Section   1.3   of the   notes   that   the   Normal   distribution   belongs   to   the   exponential   family   of distributions   (EFD).   The   natural   parameter,θ,   disper-   sion   parameter,   φ,   and   the   functions   a(φ),      b(θ),      c(y,   φ)   appearing   in   the   deﬁnition   of   the EFD   pdf are   all   clear   from   there.
(i)    Give expressions for   the vector of partial derivatives ∂β/∂e and the normal equations which   are   solved   to   ﬁnd   the   maximum   likelihood   estimates   of   the   parameters   in   the   above   GLM.   You   should   speciﬁcally   deﬁne   the   weights,   working   responses,   and   any   function   of the   dispersion   parameter   which   appear   in   these   equations.
What   is   the   Fisher   Information   matrix?      Give   its   particular   form   for   the   given   GLM.         [4]
(ii)    Give    the      expression      for      the      log-likelihood      function      of   the      parameters      based      on      the   random   sample   (x1   ,   y1   ), . . . , (xn   ,   yn   ).   Find   an   expression   for   the   estimated   values   of   µi   i =   1,   ...,   n for   t代 写MATH4/68052 Generalised Linear Models: Coursework (2025)R
代做程序编程语言he   saturated   model,   and   henceﬁnd      an   expression   for   the   scaled   deviance   of   the   model   with   linear   predictors      ηi       =   β0   + β1   xi   ,         i   =   1,   .   .   .   ,   n.    What   is   the   approximate   distribution   of   the   scaled   deviance   here?                   [3]A   random   sample   of data   such   as   described   above with   n = 300   is   contained   in the   ﬁle   cw-q1-dat   .   txt.    As   a   preliminary   to   the   next   parts,   read   the   data   into   R,   print   out   the   ﬁrst   six   rows   as   a   check,   and   then   produce   a   scatter   plot   of the   data.   Please   do   do   not   include   this   plot   in   your   report.
(iii)    Fit the   above   GLM to the   data using   R.   Produce   a   summary   of the   ﬁtted   model   object   commenting   on   all   the   results   included.    [4][To   visualise   your   ﬁtted   regression   model,   superimpose   the   regression   curve   from   your   ﬁtted   model   on   to   your   scatter   plot   of   the   data   as   a   check   of   the   ﬁt.      However,   you   should   not   submit   this   plot   as   part   of your   report.]
(iv)    Explaining   the   method   you   use,   calculate   an   approximate   95%   conﬁdence   interval   for   E[Yj   x   =   0.5].
[Note that the covariance matrix   for   the   parameter   estimates   can   be   obtained   by   using   the   vcov() function   on   the   ﬁtted   model   object.] [4]   [Total   marks   for   Q1   =   15] 
2.   The data in this question are from a study in the Philippines looking at household sizes and   which factors may be important in influencing them.   The data is   stored   in   the   spreadsheet   called PHH-data   . csv which contains n = 1300 observations of   households collected from ﬁve   particular regions in the country.   The values of the following variables are included:
total   = the number of people in the household other than the head of the household. 
(This is our response variable.) 
location   = where   the   house   is   located   (Central   Luzon, Davao   Region, Ilocos   Region,   Metro   Manila, or   Visayas)
age   = the age of the   head   of household
numLT5   = the number in the household   under   5   years   of   ageroof   = the type of roof in the household (either Predominantly Light/Salvaged Mate-   rial, or Predominantly Strong Material, where stronger material can sometimes be   used   as   a   proxy   for   greater   wealth).   These   are   coded   as ”PL/SM” and ”PSM”, respectively
Note that the column in the spreadsheet labelled household   is just an index from   1 : 1300. 
We will be modelling the   data   using   Poisson   GLMs   with   the   canonical   (log)   link   function   and having the counts in total   as the response variable for each one.
You can   read   the data into   R and convert   the   variables location and roof to   factor   variables   with the given reference levels using the   following   code.
phh<- read. csv(file="PHH-data. csv", header=TRUE)
names(phh)   head(phh)
phh$location<- factor(phh$location) levels(phh$location)
phh$location<- relevel(phh$location, ref= "CentralLuzon")
phh$roof<- factor(phh$roof) levels(phh$roof)
phh$roof<- relevel(phh$roof, ref= "PL/SM")(i)   Fit a Poisson GLM   with log link and a linear predictor including an   intercept   and   the   covariate   age.    ie.    log(λi   )   =   β0    + β1   age,   where   λi       is   the   mean   number   in   household   i = 1, ..., 1300 (other   than   the head) Comment on a summary of   the ﬁtted   model   object.
Produce an appropriate residual plot to check the ﬁt of your model and include this in   your report.   (To help in the interpretation of this plot   it can be helpful to   add   a   local polynomial regression line which can be done using the function loess   in R. Please see   the extra provided notes if you are not familiar with this.)   Comment, with reasons, on   what your plot tells you about the ﬁt of your model. 
How can you interpret the   value   ofβ(ˆ)1   .   the   coefficient of age   in your ﬁtted   model?        [4]
(ii)   Add age-squared to the linear predictor of the model in (ii) and ﬁt this new model in   R.   Comment on   a summary of the   ﬁtted   model.    As in   part   (ii),   check   the   ﬁt   of   your   new model using an appropriate residual plot, which should again   be   included   in   your   report.   Comment on the results.                [3]
(iii)   Now   add   the   variables   location, numLT5,   and   roof   to   your   linear   predictor   already containing age   and age-squared.   Summarise the ﬁt of   the model and comment on the   results.Show   that   the   linear   predictor   can   be   reduced   to   that   just   containing age, age-squared,   and numLT5.   Use this ﬁtted model to   estimate   the   value   of the   dispersion   parameter,   φ   .   Comment on your estimated value   of   φ   .                    [4]
(iv)   Using your ﬁtted model from part   (iii)   based   on   age,   age-squared,   and numLT5,   cal-   culate the   age of the head when   the   estimated   mean   number   in   the   household   (other   than the head) is a maximum, irrespective of the value   of mumLT5..
Calculate an approximate 95% conﬁdence   interval   for   the   maximum   mean   number   in   the household   (other than the head) when numLT5   =   1.                                [4][Total marks for   Q2   =   15][Total marks for the coursework   =   30]
ILOs Tested: 
ILO1:      write   down the   ﬁtted   model,   assess   goodness-of-ﬁt,   test   signiﬁcance   of parameters,   compare   models   and   use   the   chosen   model   to   calculate   various   quantities   of interest;
ILO2:      write   down   a   GLM with factors/covariates   as   appropriate,   state the   associated   assumptions   and   constraints,   derive   the   likelihood   equation   and   algorithms   for   model   ﬁtting;
ILO6:    use   generalised   linear   models    (GLMs),   including   logistic   regression   and   log   linear   models   with a Poisson response, to analyse    data with dependence on one or more explanatory   variables.

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com

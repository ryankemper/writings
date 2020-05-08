# The case for ending the "lockdown"

## Introduction

[**DISCLAIMER:** The original author is a layperson without medical/scientific credentials and this post represents a best-effort attempt to synthesize relevant research and unpack the policy implications of the "lockdown" approach as compared with the proposed alternative.]

[**Note:** See the very last section, **"(The End) Help us improve this review"**, for how you can contribute. [Here's where you can submit suggestions or identify issues](https://github.com/ryankemper/writings/issues).]

The following lays out what we now know about the Coronavirus epidemic, and upon review of the evidence concludes that **the unprecedented policy of "lockdown" runs the risk of resulting in far more mortality than the best alternative**. In short, this is because the lockdown harms the entire country, whereas death and serious complications due to COVID-19, while incredibly tragic, affects an extremely limited subset of the population when compared to the effects of the lockdown itself.

Furthermore, it seems likely, although it cannot be said for sure, that beyond increasing mortality from non-COVID-19 sources, that the policy of lockdown as well as the general culture of widespread fear may lead to us experiencing more COVID-19 deaths than we otherwise would have suffered. We'll dig into those details further on in this article, but for now it should be noted that the effects of social isolation, joblessness, and limited exposure to the outside world, are known to be heavily correlated with increased mortality through a number of independent mechanisms of action.

We characterize the root of United States policy towards the pandemic to be based upon the idea of "Containment", which attempts to reduce transmission to such an extent that the virus fades away without having achieved population-level immunity. In contrary to our current policy, we advocate for a policy of what we are calling "Pareto Mitigation" (per the ["Pareto Principle"](https://en.wikipedia.org/wiki/Pareto_principle)): a policy wherein the most vulnerable among us (primarily the elderly) are encouraged to self-isolate ("shelter in place"), while the majority of society is no longer prohibited from working and transacting more or less "as normal", with the (temporary) exception of large gatherings and a policy of encouragement of _voluntary_ usage of masks and physical distancing where warranted. This policy will allow us to mitigate deaths where they are likely to occur, while minimizing mortality that would be directly introduced by lockdown-based containment measures.

Care has been taken to be thorough while limiting the raw length of this writeup. As expected with a public health challenge this unique and unprecedented, it takes a lot of words to do the subject justice. For those short on time or who have difficulty understanding technical language, you are advised to skip to "Section 6: TL;DR - Simple Words Only", which explains the important parts in simple language that even children can understand.

## What's happened so far

A novel coronavirus, now dubbed SARS-CoV-2, emerged in late 2019 in China from a zoonotic source, and very quickly spread to the rest of the world, rapidly becoming the most serious pandemic in over a century.

The basic timeline as it pertains to the US is described in ["First Case of 2019 Novel Coronavirus in the United States"](https://www.nejm.org/doi/full/10.1056/NEJMoa2001191):

```
Dec 31 - China reports cluster of pneumonia cases
Jan 7  - China alerts health authorities that cluster is associated with SARS-CoV-2 (at the time it was called 2019-nCoV)
Jan 20 - First reported US case (they had active symptoms for a few days prior)
```

Evidence shows that the virus is rapidly transmissible between humans. The primary source of transmission is believed to be via infected _respiratory droplets_. When the viral particles within these droplets eventually make their ways to mucous membranes, such as the eyes, nose, mouth, or sexual organs, exposure occurs and infection may result.

The condition that results is known as COVID-19, and bears the characteristic marks of acute respiratory illness. A sizeable portion of those infected are either asymptomatic (no symptoms), or paucisymptomatic (few symptoms), whereas some go on to develop increasingly severe symptoms that in extreme cases culminate in the need for invasive ventilation, at which point death is very difficult to avoid (for those interested, we recommend starting by reading [Vo](https://www.medrxiv.org/content/10.1101/2020.04.17.20053157v1.full.pdf)).

In response, countries around the world have taken a series of unprecedented actions. For our purposes, we are going to focus on the path taken by the United States.

Upon the recommendation of top public health officials, the United States enacted a series of increasingly draconian measures, culminating in the forced shutdown of large swaths of the US economy that were deemed "non-essential".

These policies vary depending on the exact state and county in question.

Initially, extreme action seemed justified based off of the figures that were publicly available in early 2020. Troublingly, as new, better data has emerged, public policy has not changed accordingly, and indeed in many cases the "goalposts have been moved". Public health and media messaging around the lockdowns was initially centered around the seductively popular idea of "flattening the curve": a policy wherein measures are taken to slow tranmission of the virus in order to avoid a capacity over-run of the healthcare system that would result in excess mortality. These measures were largely based on the projections of models such as that of the Institute for Health Metrics and Evaluation (IMHE), which has been shown to have poor predictive value and to have massively overstated the numbers of hospitalizations, deaths, and therefore hospital capacity (ventilators, hospital beds, staff) necessary to effectively manage the crisis.

Weeks and months later, facts on the ground show that the purported collapse of the healthcare system did not occur. Moreover, this was not due to success in seriously curtailing the spread in hard-hit areas like New York, but was rather due to the aforementioned discovery that COVID-19, while extremely deadly in certain subsets of the population, was not nearly as deadly overall as previously thought. An analysis of the flawed IMHE model is outside the scope of this article, but suffice to say that the model is built on extremely dubious assumptions and represents an approach of blind curve-fitting rather than a true epidemiological model, and makes bizarre assumptions that result in an unrealistic symmetricality as far as death drop-off is concerned (see [this excellent analysis by "LessWrong" user Zvi](https://www.lesswrong.com/posts/QuzAwSTND6N4k7yNj/seemingly-popular-covid-19-model-is-obvious-nonsense)). Confronted with the reality of having "succeeded" in avoiding the collapse of the healthcare system, albeit arguably not due to the lockdown policy, policymakers have _not_ lifted the lockdown restrictions in much of the country, but on the contrary appear to have shifted the goal to a goal of total containment: staying locked down until COVID-19 has been suppressed to such an extent that it becomes feasible to perform widespread location tracking (dubbed "contact tracing"). Indeed, the current policy seems to be one of "indefinite postponement", the key assumption being that it is feasible to avoid exposure to SARS-CoV-2 until a safe and effective vaccine is developed and delivered to the global population, and that the indefinite lockdown will not lead to excess mortality. We strongly dispute these assumptions and believe that they don't hold up to scrutiny.

**One problem that we believe has not been adequately addressed by our leaders is the poor understanding of how infections spread, what a virus actually is, and how the immune system detects, fights off, and guards against future occurrences of previously-seen pathogens.** To that end, this article will be broken up into a series of sections.

The first section, **"The Basics"**, will cover the **absolute minimum that every citizen should know** about epidemiology and immunology.

The second section, **"How serious is COVID-19?"**, will cover emerging evidence regarding the transmission rate, lethality, and hospitalization rate of COVID-19. We'll see that current evidence strongly contradicts the models and figures upon which our public policy has purportedly been designed.

The third section, **"Lockdown-associated mortality and destabilization"**, will cover some of the theoretical and observed deleterious (negative) effects of the lockdown.

The fourth section, **"Pareto Mitigation: An evidence-based approach"**, covers our proposed alternative for a COVID-19 mitigation policy.

The fifth section, **"The Road to Hell is Paved With Good Intentions: Censorship and Superstition in the Post-COVID Era"**, examines the attitudes and beliefs that have led to widely respected public health officials resorting to policies that do not stand up to evidence-based examination, and furthermore examines the ethics and constitutionality of those same policies.

Finally, the intent of this article is to use the most precise language possible, while still remaining largely understandable to the average citizen. **This crisis effects us all and thus we should write and speak in a way that is accessible to all**. To that end, the final section is a "TL;DR" which uses only those words that are understandable by an elementary-school aged child, and focuses on reviewing the absolute most important points.

## Section 1: The Basics

First we need to understand what a [virus](https://en.wikipedia.org/wiki/Virus) is. A _virus_ is a type of infectious agent that uses the living cells of an organism to _replicate_ (reproduce itself). Generally this involves the virus "infecting" a cell and re-purposing its cellular machinery to manufacture thousands more viruses, until eventually the cell dies and the new "baby viruses" explode out of the cell, at which point they attempt to infect further cells. Viruses are extremely tiny: often around 1/100 the size of a "normal bacteria".

Next, we should understand the very basics of how our immune systems interact with viruses. The immune system is an incredibly intricate choreography composed of numerous different cell types. At a high level, the immune system's job is to distinguish "self" from "non-self" (the "enemy", in this case the SARS-CoV-2 virus). The immune system learns to adapt to [antigens](https://en.wikipedia.org/wiki/Antigen), which are molecules that can be used to recognize a type of pathogen. Once an antigen corresponding to a pathogen is detected, the immune system manufactures [antibodies](https://en.wikipedia.org/wiki/Antibody), which can attach to antigens in order to directly neutralize pathogens, or indirectly to help other killer immune cells neutralize the pathogen.

After the immune system successfully fights off an infection such as COVID-19, antibodies continue to circulate in the blood for some time, which is believed to prevent re-infection so long as sufficient antibodies are present. Eventually, these antibodies may no longer be present, but the immune system maintains _Memory B Cells_ which lie dormant, waiting to be exposed to the characteristic antigens that the immune system saw previously, at which point they spring to life, producing antibodies at a rapid rate. Thus, even if the body no longer had circulating antibodies in the blood, these memory cells allow the body to respond sooner, resulting in a more mild infection with lower peak viral load.

Thus, while it _may_ be possible to be re-infected with SARS-CoV-2 after sufficient time has passed (exactly how long is a matter of open research), these immune memory cells persist across decades and thus recovery means that that individual is much less likely to fall seriously ill, and overall will spread the virus much less than if there were no immunity. This mechanism is robust and well-studied, and thus while we are still researching exactly how long full immunity lasts as opposed to the "partial" immunity of memory cells, it is an incredibly safe assumption that this process works for SARS-CoV-2 as it does for any other coronavirus.

So, we've covered the basics of viruses and the immune system at the "individual" level, and now we need to talk about the "population" level. A critical concept to understand, and indeed one that has been unfairly stigmatized, is the concept of _herd immunity_. **Herd immunity is the natural result of individual immunity as applied to population-level dynamics**. That is to say, **herd immunity is a natural process** that happens when a pathogen has worked itself through enough of the population. Specifically, once the proportion of recovered in the population reaches `1 - (1/R_0)`, there are no longer enough vectors (infectable indviduals) remaining for exponential growth to occur. It's worth noting that this is the same principle that vaccination relies upon; vaccination is just an artificial way to build immunity without having to undergo the risks associated a full infection.

In order to talk about how infectious and how deadly COVID-19 is, there's three important epidemiological concepts that need to be understood:

   **(1a)** [Basic reproduction number](https://en.wikipedia.org/wiki/Basic_reproduction_number): Also called "R Nought", this number intuitively represents how many other people the average infected person goes on to infect, without accounting for population immunity. We classify how easily a disease spreads by its basic reproduction number, but note that there is not one "real" reproduction number. It's a function of environmental conditions, social interaction, etc.

   **(1b)** It's common to use the **effective reproduction number** R to describe in a more real sense how many people each individual is infecting on average at a moment in time. This is because the effective reproduction number accounts for non-susceptible individuals. This number needs to be at or below 1 in order to contain a disease.

   **(2)** [Case fatality rate](https://en.wikipedia.org/wiki/Case_fatality_rate): The proportion of _detected cases_ that result in death. This number will be higher than the "infection fatality rate" (the true "death rate") if there are undetected cases (as there are with COVID-19).

   **(3)** [Infection fatality rate](https://en.wikipedia.org/wiki/Case_fatality_rate#Terminology): The "true" death rate of an illness: in essence, it answers the question "what percentage of all people who get this thing are going to die?" We'll be talking a lot about the IFR of COVID-19 in the following section.

There's one last concept to cover: testing. Currently there're two broad categories of tests:

(1) PCR tests, which tells us whether someone actively has an infection of SARS-CoV-2 viral material. Note there is a "sweet spot" in the course of infection where positive results are most likely; testing too early or too late bears increasing risk of false negatives or false positives.

(2) _Serological_ (antibody) tests, which tell us whether someone has active circulating antibodies that respond to SARS-COV-2, which implies that they were previously infected (or perhaps are at the tail end of a current infection). These tests are critical for estimating the _prevalence_ of COVID-19 in the population.

Now that we've hopefully got these fundamental concepts down, it's time to talk about COVID-19 specifically.

## Section 2: How serious is COVID-19?

We'll start by diving right into the case and infection fatality rates.

After that, we'll take a look at an important paper and use it to examine the transmission dynamics of SARS-CoV-2 at the population level.

### Hospitalization and fatality rates

Initial reports claimed that COVID-19 had a CFR of around 4-5% and a shocking 20% hospitalization ratio. Fortunately, these initial reports don't tell the full story. We have since discovered via serological testing that the number of reported cases of COVID-19 massively understates the true prevalence of infection, and therefore that the true infection fatality rate is far lower than we might have assumed.

[One dutch antibody study](https://esb.nu/blog/20059695/we-kunnen-nu-gaan-rekenen-aan-corona) (not in English, unfortunately) gives us the following table of age-stratified hospitalization and mortality figures:

|Age group|Hospitalization rate|Mortality rate (IFR)|
|---|---|---|
|20-29|0.2%|0.004%|
|30-39|0.3%|0.007%|
|40-49|0.8%|0.014%|
|50-59|1.9%|0.103%|
|60-69|3.4%|0.492%|

A recent [danish antibody study](https://www.medrxiv.org/content/10.1101/2020.04.24.20075291v1) concluded the following: "combined IFR in patients younger than 70 is estimated at 82 per 100,000", or **.082%**.

Shifting to CFR, we have an [excellent study of italian healthcare workers](https://www.epicentro.iss.it/coronavirus/bollettino/Bollettino-sorveglianza-integrata-COVID-19_16-aprile-2020.pdf) which gives us the following figures (credit belongs to [reddit user PM_YOUR_WALLPAPER for this comment](https://old.reddit.com/r/COVID19/comments/g6nmtf/update_on_italian_progression_of_covid19/foatvgv/)):

|Age group|Mortality Rate (CFR)|
|---|---|
|18-29|0.00%|
|30-39|0.07%|
|40-49|0.08%|
|50-59|0.28%|
|60-69|1.41%|
|70-79|12.63%|
|Total|0.35%|

Why are these Italian numbers so much lower than CFRs reported elsewhere? Presumbably because the majority of these healthcare workers were tested, whereas CFR figures from other sources are missing anywhere from 2-100 cases for every case that's been discovered, leading to wildly inflated case fatality rate calculations.

In short, we see that the general IFR is almost certainly somewhere between .1-.7% (very wide range given to account for uncertainty). If we account for those under 18 years of age who in general are not covered by these surveys, we can use the fact that [US census data for 2019](https://www.census.gov/quickfacts/fact/table/US/PST045219) indicates that 22.4% of the population is below 18 years old to predict that our "true IFR" across the whole population is likely 20% less than the above figures show. We might also expect that widespread obesity and other risk factors in the US might make our fatality rates somewhat worse than other countries. Taking the above into holistic consideration, we believe that it is reasonable to surmise that if the entire population becomes infected, we would see an IFR of around .30%.

Much more interesting than the absolute fatality rate is the age-based risk distribution. The Italian data shows that the 70-79 age group was **8.95 times** as likely to die as the 60-69 age group, who in turn were **5.03 times** as likely to die as the 50-59 age group. In short, **there is a "mortality cliff" that starts to occur around age 60 and becomes incredibly visible around age 70 and beyond**. Finally, it's worth mentioning that we will discuss what this means for the workforce in later sections, but right now we can note that a huge portion of COVID-19 attributable deaths will occur in those who are old enough that they are no longer in the workforce. This is extremely relevant when discussing policies that shut down large segments of the workforce.

Before we proceed, we note that one of the most common arguments for lockdown is that those who are _not at risk_ are still at risk of spreading it to those who _are_ at-risk. We believe that in the long-run, building immunity in those who are not at risk will do a better job of protecting the at-risk than trying to avoid them ever getting infected in the first place.

Moving on, comparisons have been made, both affirmatively and negatively, towards Influenza. So let's briefly talk about how Influenza is different from Covid, and in what ways it's similar.

Influenza is characterized by a pattern of mortality in which the **very young** and the **very old** have a relatively extremely high chance of death ([see this graph](https://bmcmedicine.biomedcentral.com/articles/10.1186/1741-7015-10-162/figures/2)). In comparison, COVID-19 has a pattern of mortality where the **very old are extremely vulnerable**, whereas **COVID-19 is stunningly _not_ deadly in the very young**. A disease like COVID-19, which has such a "spiky" (highly variable) mortality rate based upon age and other comorbidities, is a _terrible_ candidate for a national lockdown, because **lockdown does not distinguish between those at risk and those who are not at risk**. This pattern of mortality is something we should be celebrating - **we have strong evidence that our children are safe**, and thus if anything in children it is rational to worry about Influenza, not COVID-19 - but unfortunately the wider population is not aware of this fact due to what we believe are misleading or outright false statements propagated by the media and, at times, even our trusted public health officials.

In short, the [statement](https://www.youtube.com/watch?v=2DekzGCJhJw&feature=youtu.be&t=53) by Dr. Fauci that COVID-19 is likely an order of magnitude deadlier than the flu has not held up to scrutiny. (To his credit, he was fairly clear that he was estimating it based off the data at the time, which we certainly cannot fault him for). On the contrary, we can use the above figures, which we feel are fairly conservative (meaning erring on the side of over-estimating risk), to state that overall COVID-19 is perhaps 3x as deadly as Influenza in the general population, whereas in infants and young children Influenza is likely 2 orders of magnitude _more_ deadly than COVID-19. **It is absolutely critical that we understand the age-stratified fatality rates of COVID-19 in order to craft effective and evidence-based public policy**.

### Lessons from Vo'

One of the seminal papers in the field is ["Suppression of COVID-19 outbreak in the municipality of Vo', Italy"](https://www.medrxiv.org/content/10.1101/2020.04.17.20053157v1.full.pdf) which "provides new insights into its [SARS-CoV-2] transmission dynamics, the duration of viral load detectability and the efficacy of the implemented control measures".

The Venetian region of Vo' employed a highly aggressive lockdown between 23 Feb 2020 and 8 March 2020. They enforced "the closure of *all* public services and commercial activities and imposed a ban on population movement". During this time the study authors conducted nasopharyngeal swabs two weeks apart, testing the _entire population_ twice. We're going to pull out just a few key insights here that will help us understand how SARS-CoV-2 spreads in communities and the progression of the associated disease COVID-19.

- "No infections were detected in either survey in 234 tested children ranging from 0 to 10 years, despite some of them living in the same household as infected people."
- "Older individuals showed a three-fold increase in the prevalence of infection"
- "The time to viral clearance (time from the earliest positive sample for the subjects with more than one sample in the first survey and a negative sample in the second survey) ranged from 8 to 13 days and was on average 9.3 days, with standard deviation 2.0 days."
- "These results suggest that asymptomatic infections may play a key role in the transmission of SARS-CoV-2. We also found evidence that transmission can occur before the onset of symptoms."
- "We estimated that on average **41-42% of the infections are asymptomatic** and that the **lockdown reduced SARS-CoV-2 transmissibility**, on average by 89-99%, depending on the assumed initial value of R_0^1 and on the duration of virus detectability"
- Effective reproduction number was **3.0** (95% CI 2.5-3.5) at the beginning of the study which declined to **0.14** (95% CI 0.0-0.29) by the end of the lockdown.

In conclusion, Vo' gives us strong evidence that asymptomatic spread plays a significant role, with their estimate being about half of cases being asymptomatic. This study provides evidence that extremely radical lockdown measures are effective in reducing spread. We'll examine this in more detail later when we characterize the policy of Containment and contrast it with our proposal of Pareto Mitigation. For now, we'll just say that the high proportion of asymptomatic transfer implies that one either needs to practice total containment (radical lockdown) or allow SARS-CoV-2 to pass through the population, whereas taking "half-measures" seems highly inadvisible.

### Transmissibility

Evidence shows that SARS-CoV-2 is quite efficiently transmitted between humans. Furthermore asymptomatic and pre-symptomatic spread occur extensively. This is shown by the above "Lessons from Vo'", and is further bolstered by the following study:

["Presymptomatic SARS-CoV-2 Infections and Transmission in a Skilled Nursing Facility"](https://www.nejm.org/doi/full/10.1056/NEJMoa2008457?query=recirc_mostViewed_railB_article) provides us with the following insights:

- "**Infection-control strategies focused solely on symptomatic residents were not sufficient to prevent transmission** after SARS-CoV-2 introduction into this facility"

- "**viable SARS-CoV-2** was isolated from specimens of asymptomatic and presymptomatic residents. Evidence of transmission from presymptomatic persons has been shown in epidemiologic investigations of SARS-CoV-2."

- "The data presented here suggest that sole reliance on symptom-based strategies may not be effective to prevent introduction of SARS-CoV-2 and further transmission in skilled nursing facilities."

Finally, estimates of the basic reproduction number vary between studies, but Vo's estimate of 3.0 seems like a decent figure to work off of.

## Section 3: Lockdown-associated Mortality and Destabilization

### Mass unemployment

Let's start with the obvious impact of lockdown: mass unemployment. Per https://www.dol.gov/ui/data.pdf, we are seeing "the **highest level of** the seasonally adjusted insured **unemployment** rate **in the history of the seasonally adjusted series**". The numbers themselves are shocking: "The total number of people claiming benefits in all programs for the **week ending April 4** was **12,506,993**, an increase of 4,300,016 from the previous week. There were 1,757,864 persons claiming benefits in all programs in the comparable weekin 2019."

In short, we know that **tens of millions** of Americans have lost their jobs. Contrary to popular belief, these job losses were not inevitable and there is no evidence that these would have occurred if we had not forced business closures. Indeed, it appears that we could have managed this crisis in the same way employers manage their employees being sick in any other scenario: by allowing employees to take sick days when they have symptoms. As we have discussed, the vast majority of the workforce is not at serious risk of COVID-19, and thus even in a New-York-style "worst-case scenario" most businesses would have operated with only mild-moderate efficiency impacts.

There are many that believe that unemployment, while unfortunate, is an abstract notion that has merely economic consequences: perhaps shareholders will lose some money, which is seen as a small price to pay compared to the alternative. **This could not be further from the truth.** We know that unemployment is directly correlated with increased mortality from suicide. But how much mortality should we expect? [One analysis from New Zealand](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1732539/pdf/v057p00594.pdf) concludes the following: "Being unemployed was associated with a **twofold to threefold increased relative risk of death by suicide**, compared with being employed. About **half of this association might be attributable to confounding by mental illness.**" So, very conservatively, we might expect that an unemployed citizen is now 50% more likely to commit suicide as a result.

[Per the National Institute of Mental Health](https://www.nimh.nih.gov/health/statistics/suicide.shtml), we saw **47,173 suicides in 2017**. But the relative risk of increased suicide, while significant in normal times, must surely be drastically worsened by the unique combination of social isolation, widespread fearmongering (including unfounded fears of possible re-infection and a fear that children are dying in significant numbers), and closures of natural forms of recreation such as beaches and public parks. **We are in uncharted territory, and thus predicting the actual number of suicides we will see is difficult**. However, it's not unimaginable that the US could see twice the normal rate of suicide this year, which would be on the order of an extra 50,000 deaths due to suicide.

Some might claim that the aforementioned environment of social isolation and widespread panic is not directly attributable to the lockdown itself, but we feel that such claims are dubious. It's worth noting that public support for the lockdown, which appears to be quite high, is precisely perpetuated by the widespread culture of fearmongering that has been encouraged by our media and by some members of government. We thus view lockdown and the culture of fear and misinformation around it as _the same system_.

In a hypothetical world where our public health officials were forthright with the American people, engaging in "straight talk" that discussed the facts plainly rather than resorting to baseless speculation and a general attitude of infantilization towards the American people, taking time to explain what a virus actually is and how it actually spreads in the real world, we believe that the American people would be more-or-less "rationally fearful", that is, afraid in proportion to the threat, as opposed to the current state of affairs where the level of panic and fear is entirely divorced from the ground truths.

### Social Isolation: more than just correlation?

**Finally, we need to examine the effects of social isolation itself**. Beyond the fact that social isolation prevents the natural exchange of microbes that occur between humans engaging in social contact, it should be noted that social isolation is directly thought to lead to increased all-cause mortality due to worsened health outcomes across pretty much every dimension that we can examine. [One review of the impacts of social isolation and loneliness in older adults](https://www.pnas.org/content/pnas/110/15/5797.full.pdf) concludes that "mortality was higher among more socially isolated and more lonely participants. However, after adjusting statistically for demographic factors and baseline health, **social isolation remained significantly associated with mortality** (hazard ratio 1.26, 95% confidence interval, 1.08–1.48 for the top quintile of isolation), but **loneliness did not** (haz-ard ratio 0.92, 95% confidence interval, 0.78–1.09). The association of social isolation with mortality was unchanged when loneliness was included in the model".

It's now popular to refer to what was previously called "social distancing" as "physical distancing" to note the fact physical distancing does not necessarily lead to loneliness; this is because loneliness can (perhaps) be mitigated to a limited extent by usage of social media and videoconferencing. Troublingly, we can see that it is the social isolation itself, and not the emotional feeling of loneliness, that is associated with death, and thus we can surmise, at least in older adults (but almost certainly in the broader population as well), that the widespread recommendations of social isolation ("stay at home", "social distancing", etc) will lead to increased all-cause mortality. Finally, we wish to highlight that a small increase in all-cause mortality amidst the general population due to social isolation could very easily dwarf COVID-19-associated mortality, which as we have discussed is primarily constrained to a very limited subset of the population.

### A preventable decline in preventative care

Other impacts of our misguided public-health policy have included a massive reduction in "elective" surgeries and preventative care, which we know will lead to increased death due to non-COVID-19 related causes in the long run. Even more troublingly, the fact that we enacted lockdown on a national scale and encouraged non-sick individuals to avoid going to their health professionals for preventative care led to an unforeseen consequence: **rather than preventing the collapse of our medical system, we have scaled down our medical infrastructure across the country.** A [news report by USA Today](https://www.usatoday.com/story/news/health/2020/04/02/coronavirus-pandemic-jobs-us-health-care-workers-furloughed-laid-off/5102320002/) indicates that **thousands of US medical workers have been furloughed**. Why? Because in areas that have not been sufficiently ravaged by COVID-19 - which indeed is the majority of the country - hospitals are more empty right now [written April 29 2020] than they have ever been. As a result, we have had to furlough medical workers in the midst of a global pandemic. This is directly attributable to our public policy; it was not an inevitable result of the pandemic. **Thus, the very policy ("flattening the curve") intended to protect our hospital capacity has instead crippled it.**

### General vaccination on the decline?

Additionally, [per FiercePharma](https://www.fiercepharma.com/marketing/retail-scripts-vaccines-and-acute-drugs-decline-sharply-amid-covid-19), the general avoidance of non-COVID-19-related medical care has led to **plummeting vaccination rates**. They claim that "total scripts of the shingles vaccine have **dipped 84%**", and "Use of Pfizer’s Prevnar 13 and Merck & Co.’s Pneumovax 23, both pneumococcal vaccines, **fell by 72% and 60%, respectively**".

We've now taken a stab at how to reason about lockdown-related mortality, but we should also examine the more "fuzzy" factors around destabilization of our broader systems. Implicit in our unprecedented response is the notion that COVID-19 is about as bad as it gets, and that we will not experience another pandemic of a different disease in the midst of this lockdown. This is playing with fire. While statistically the likelihood of a pandemic emerging in any given year is low, we know that we have seen several pandemics of varying severity over the last couple decades - the original SARS outbreak, Hong Kong Flu, H1N1, etc.

### Sometimes lightning does strike twice

**What would happen to our society if the "superbug" that so many of us suspect will emerge in our lifetimes rears its head?** Such a catastrophe would unfold at precisely the time that we have destroyed our economy, postponed life-saving elective surgery and preventative care (including, troublingly, vaccination of our children), and potentially decreased our natural ability to fight infection by adopting patterns of behavior that reduce the natural exchange of microbes that our immune systems rely on.

This is not a stable state for our society to be in. There is an ironic parallel to the concept of [cytokine storm](https://en.wikipedia.org/wiki/Cytokine_release_syndrome). Just as our immune systems sometimes get overzealous and destroy the body, so too has our response to COVID-19 ironically ended up damaging the stability of our economic and socioemotional systems and made us less resilient in the face of future crises.

### Debunking the claim that it's "just the economy"

**The notion that we can save more lives, and therefore prevent economic damage, by enforcing lockdown is not a reasonable position given what we now know.** Indeed, the portion of the American public most effected by lockdowns (the workforce, particularly those of lower socioeconomic status who cannot work from home) are not those at highest risk of COVID-19; rather, it is the elderly, and particularly the extremely elderly, who are suffering incredible mortality from this disease. In other words, a significant portion of COVID-19 deaths are occurring in those who are not part of our workforce. We are not saying that this means that their deaths don't matter; however, we are saying that **the lockdown introduces an entirely new class of mortality** that has much more far-reaching consequences than mortality due to COVID-19.

A much more accurate position is that **economic damage leads to lives lost**. This is a notion that is familiar to economists, but has been ignored by our politcians, who instead have been making absurd statements such as the false notion that "we cannot put a price on human life". **This is patently false, and admitting as such is neither callous nor insensitive**. The functioning of our economy, and indeed our day-to-day lives, depends on activities that carry inherent risk. For example, we lose over 38,000 Americans each year to car crashes. What this means is that we can calculate an implicit cost of human life that we have all unknowingly been operating under.

One [analysis of the costs of the lockdown](http://cep.lse.ac.uk/pubs/download/occasional/op049.pdf) uses the well-established approach of "wellbeing-years" to try to estimate a ballpark figure of what the lockdown is costing us. Their analysis focuses on the UK, but they conclude that maintaining lockdown in the UK beyond June 1 will lead to a net reduction in wellbeing-years. The broader point here, though, is that it is invalid to claim that we cannot make rational tradeoffs that balance across multiple factors, and instead must look at a single variable - lives purportedly lost due to COVID-19 - to craft public policy. This fallacious belief needs to be extinguished if our goal is to craft evidence-based public policy.

Remember, **flattening the curve does not reduce deaths in the long-run**, except insofar as it avoids overrunning hospitals, which we have already achieved. Flattening the curve is not beneficial for its own sake; indeed, it worsens the economic damage, and thus it should only be practiced until we know that we won't overwhelm hospitals. **The area under the curve remains the same**. We strongly believe that a rational examination of the evidence will show that practicing containment "until the vaccine" (which will take years and is not guaranteed to be possible, although we personally believe that we eventually will have an effective vaccine) is a reckless policy that risks incurring far more mortality than simply "biting the bullet".

To put it simply: **we previously had one very serious problem: COVID-19. Now we've enacted policy that has led to _two_ very serious problems: COVID-19 and an unprecedented economic destabilization.** There is no scientific paper in existence that can predict the full ramifications of what we've done.

### Magnifying inequality

Finally, we should mention that the effects of the lockdown are to magnify inequality across virtually every dimension. Lower-income students, many who do not own a personal laptop, are disadvantaged in a "distance-learning" model. Those who have lost their jobs tend to be those workers who are in a lower socio-economic bracket and have jobs that do not allow one to "work from home". This has created a further divide where high-paying professions such as Software Engineers have managed to escape largely unscathed, while many lower-paid Americans who were _already_ living paycheck-to-paycheck are now forbidden from working and forced to rely on incompetent government programs for assistance. Those who are single and live alone have now had most viable avenues of social interaction cut off from them.

## Section 4: Two Possible Paths

### Containment

Vo' showed us that successful containment requires placing incredible constraints on freedom of movement and assembly. By placing a near-total ban on "population movement", the effective reproduction number was decreased from **3.0** to **0.14**. With a decrease in reproduction that dramatic, a policy of containment becomes feasible. Techniques like "contact tracing" which are almost surely unworkable at scale, regardless of technological advances (see security researcher [Schneier on contact tracing](https://www.schneier.com/blog/archives/2020/05/me_on_covad-19_.html)), become possible when the true number of current infected drops to extremely low levels.

As long as containment is successfully in effect, deaths due to COVID-19 in the short-medium term can be indefinitely postponed.

**Because lifting containment in any serious way would allow the infection rate to surge, containment must be continually maintained until an artificial way to avoid COVID-19 mortality is developed.** While there are countless efforts underway to develop a vaccine, the length of time that developing a vaccine will require is highly uncertain. We don't have enough information to put an upper bound on time to develop a vaccine or an incredibly effective treatment, so the ultimate cost of maintaining such severe restrictions to personal freedoms and general wellbeing is similarly unbounded. Containment as practiced in Vo' carries a cost to the wellbeing of the population, and as such its cost increases roughly in proportion to how long it must be practiced for.

#### Dispelling the "Eradication Myth"

As far as we know, no serious (scientific) proponent of Containment has advocated for Eradication (suppressing COVID-19 so severely that it literally "dies out" and is no longer present in the global population).

However, we have observed that it is an unfortunately common misconception among everyday citizens who are in favor of a "lockdown"-style policy, that the ultimate goal of our policy of Containment is to eradicate COVID-19 from the face of the earth.

This notion is not considered remotely plausible by serious experts for a few reasons.

First, COVID-19 is a very highly infectious respiratory disease. Thus far it _appears_ to spread even more easily and efficiently than Influenza (see [this meta-analysis of Influenza's reproduction rate](https://bmcinfectdis.biomedcentral.com/articles/10.1186/1471-2334-14-480)), which is already itself a highly infectious respiratory disease. Despite this, many fall prey to a seductive-sounding notion that goes something like this: "why can't we all agree to not interact with society for a length of time larger than COVID-19's maximum incubation period? Wouldn't it then die out?". Now, we must understand that even under totalitarian regimes, coordinating such an effort across an entire population, let alone the entire planet, is impossible even with our modern surveillance and suppression techniques.

But to truly show how ridiculous this notion is, let's assume that we truly _could_ coordinate our efforts across _the entire globe_ such that _no infection occurs anywhere on Earth for the next 4 weeks_ (also we'll ignore the existence of the immunocompromised who can remain perpetually infected). Then what? Well, we immediately hit the second snag - the existence of animal reservoirs. As we covered in our initial timeline of SARS-CoV-2 and its associated disease COVID-19, **SARS-CoV-2 emerged from a natural animal source**. Thus, even if we eradicate COVID-19 from every human host on Earth, there will always be animal reservoirs of this pathogen that are capable of "jumping" to humans. Again, SARS-CoV-2 began via a zoonotic (animal) route, and thus given the opportunity it will happen again.

Those interested in learning about eradication at a high level might want to start with Wikipedia's [Eradication of infectious diseases](https://en.wikipedia.org/wiki/Eradication_of_infectious_diseases). The article makes it clear that "**The targeted organism [SARS-CoV-2 in this case] must not have a non-human reservoir** (or, in the case of animal diseases, the infection reservoir must be an easily identifiable species, as in the case of rinderpest), and/or amplify in the environment." Additionally, it shows that we have only ever successfully eradicated two diseases: smallpox and rinderpest.

### Pareto Mitigation

We've examined the policy of containment (the path the United States appears to be committing to currently), and seen that it allows us to indefinitely postpone mortality, at the cost that we can't stop doing it until we've made incredible advancements in prevention or treatment.

The alternative is to (primarily) focus our resources (testing, governmental assistance) on the most at-risk individuals and locations (such as elderly care facilities):

- Encourage at-risk groups to self quarantine, and utilize testing to protect them
    * All elderly, _especially nursing homes_ (all entrants to nursing homes need to take tests, wear face masks, wash hands, etc)
    * Those with comorbidities that place them at high risk (severe obesity, COPD, heart disease, etc)
        - The above is not an exhaustive list. They key is that we do have the data to identify those at risk.
- All others are _allowed_ to work and transact freely.
    * People are already scared stiff of this thing, they will take effective safety measures if we teach them how. We don't need to resort to compulsion.
    * By having non-at-risk indviduals develop natural immunity, they are less likely to spread to at-risk individuals in the long run.
- We don't think it's politically feasible, but in a perfect world we could allow citizens to choose [voluntary self-exposure](https://www.medrxiv.org/content/10.1101/2020.04.12.20062687v1). This should NEVER be compelled, nor should we roll out "immunity certificates" for ethical reasons (we don't have such certificates for any other disease, despite them being deadly). Self-exposure has the additional benefit of allowing administration of a _controlled dose_ of SARS-CoV-2. Initial viral load is speculated to affect the final outcome, although we are unaware of research proving or disproving this one way or the other.

So, what are the positives and negatives of such an approach? In order to evaluate the costs of _not_ implementing indefinite containment via a "lockdown" strategy, we need to have a reasonable [upper bound](https://en.wikipedia.org/wiki/Upper_and_lower_bounds) for the amount of COVID-19 deaths we might see.

["Report 9: Impact of non-pharmaceutical interventions (NPIs) to reduce COVID-19 mortality and healthcare demand"](https://www.imperial.ac.uk/media/imperial-college/medicine/sph/ide/gida-fellowships/Imperial-College-COVID19-NPI-modelling-16-03-2020.pdf) (hereafter referred to as "Ferguson")  is the key to getting a reasonable estimate of what a "worst-case" scenario might look like.

Ferguson models an overall IFR of 0.9% by adjusting figures from [Verity et al](https://www.medrxiv.org/content/10.1101/2020.03.09.20033357v1.full.pdf) to account for a non-uniform [attack rate](https://en.wikipedia.org/wiki/Attack_rate).

Rather than paraphrase their results, we'll just quote directly:

"In the (unlikely) absence of any control measures or spontaneous changes in individual behaviour, we would expect a peak in mortality (daily deaths) to occur after approximately 3 months (Figure 1A). In such scenarios, given an estimated R_0 of 2.4, **we predict 81% of the GB and US populations would be infected over the course of the epidemic**. Epidemic timings are approximate given the limitations of surveillance data in both countries: **The epidemic is predicted to be broader in the US than in GB and to peak slightly later. This is due to the larger geographic scale of the US, resulting in more distinct localised epidemics across states** (Figure 1B) than seen across GB. The higher peak in mortality in GB is due to the smaller size of the country and its older population compared with the US. In total, in an unmitigated epidemic, we would predict approximately 510,000 deaths in GB and **2.2 million** in the US, not accounting for the potential negative effects of health systems being overwhelmed on mortality."

So, modelling a **0.9% IFR** with a basic reproduction number of **2.4** leads to **82% of the US population getting infected**, ultimately ending up with **2.2 million deaths**. This seems like a reasonable upper bound on mortality.

Note that we suspect that accounting for voluntary, uncoerced changes in behavior, as well as the fact that different groups likely have different susceptibility to infection, implies that this "worst-case" scenario is unlikely. However, understanding "downside risk" - what would happen in a worst case scenario - is very important for evaluating the drawbacks of a policy. (By similar logic, when evaluating Containment, we noted the need to account for the fact that the potential length of containment is unbounded and therefore the potential economic and psychological harm is unbounded as well)

Thus this potential downside of short and medium term COVID-19 mortality is counterbalanced by avoidance of the lockdown-associated causes of mortality that we examined in Section 3.

### Which path do we take?

Before we look at how we answer this question, we should note that evidence points that "half-measures" - for example, what we've done in the US thus far - do not really accomplish anything. That's why we're presenting two possible paths and not three; we believe that a "middle road" solution carries all the risk of COVID-19-associated mortality that Pareto Mitigation risks, while also incurring the majorty of the lockdown-associated mortality and systemic destabilization that we have examined.

Additionally, we should note that, partly due to length and time constraints, we have not covered the "pulsed" approach of intermittent lockdown. However, our position is that such an approach carries the same fundamental flaw of representing a "half-measure": the potential for widespread economic closures in the future, even if in the present the lockdown has been temporarily lifted, represents an undue pressure on businesses and the economy at large and thus runs the same risk of experiencing "most of the negatives and few of the benefits".

Now, let's proceed. In order to make a rational decision, first we have to know what our values are.

**Is it worth it to decrease the wellbeing of an entire society in order to prevent as much medium-term COVID-19 death as we possibly can?** Would we be more horrified living in a free society with 2.2 million of our loved ones dead, than we would be in a society in which COVID-19 death was much lower, at the expense of potentially years of not being allowed to go outside without permission, having government-controlled drones barking warnings about the dangerous of violating the lockdown, and destroying a huge portion of our population's livelihoods?

How confident are we that lockdown-associated mortality is significantly lower than the mortality avoided by practicing indefinite containment?

Which unknown are we more afraid of - the potential costs to our general wellbeing, personal freedoms and economic functioning, or instead the potential lives lost?

The answer depends on our values. **The responsibility rests on each one of us as private citizens to decide which society we want to live in based on our own personal value structures.** Despite widespread statements to the contrary, epidemiologists, medical doctors, and politicians do not have a monopoly on policy decisions, nor on the values on which we base those decisions.

As such, **the ultimate decision on which path we should take is left as an exercise to the reader.**

## Section 5: The Road to Hell is Paved With Good Intentions: Censorship and Superstition in the Post-COVID Era

### How did we get here?

So, if a policy of Containment is truly such a bad idea, how did our public health officials, some of whom have decades of battle-tested experience, get it so wrong? It seems plausible that they were trying to prevent mortality, but their incentive structure is such that it is much worse to have done nothing and later find out that the virus was worse than we thought, than what actually happened, which is to have undertaken actions that were self-destructive and then discovered that the virus was way less deadly _overall_ than we thought.

Additionally, an environment of incredible stress and sleeplessness is known to destroy cognitive functioning. In particular, it shifts the human brain from a cognitive style that can think strategically and proactively avoid problems, to one that experiences tunnel vision and a rigidity in belief systems. That is to say, that [the conditions our well-intentioned officials](https://www.businessinsider.com/dr-anthony-fauci-daily-routine-coronavirus-pandemic-2020-4) have been operating under have put them, physiologically, in a state that makes it hard for any human to adequately process the torrent of incoming data and synthesize it into effective public policy.

### Be wary of "hero culture"

Still, we should note that the road to hell is paved with good intentions. And we should note that a "hero culture" is very dangerous. Public figures such as Anthony Fauci and Deborah Birx could certainly be described as heroes, but we need to avoid viewing them as infallible. Indeed, expressing a well-founded belief that contradicts a belief espoused by Fauci, (who is, we feel, correctly beloved by the American people), is unfortunately met with hostility and often blind rage.

### The Cassandra Effect

There's also an irony here: public figures like (in no particular order) Anthony Fauci, Michael Osterholm, Bill Gates, and Sam Harris have been very vocal about worrying about the eventual possibility of a "superbug" - imagine a pathogen that spreads like SARS-CoV-2 but kills like SARS-1 appeared to, or even one that wipes out the immune memory such as Measles. These are very real possibilities and we are right to be vigiliant against the emergence of such a pathogen. But the measures we use to fight those pathogens need to be different from the measures we use against a virus like SARS-CoV-2, which is in the same ballpark (meaning, within an order of magnitude) as Influenza as far as mortality is concerned. Thus, we feel that many individuals who have correctly been anticipating the potential emergence of the infamous "superbug", have incorrectly (but understandably) latched onto SARS-CoV-2 as this bug. And thus some have advocated policies that, beyond bearing the potential for increased mortality, have eroded our constitutionally-protected civil liberties to an extent that eclipses even that of September 11.

### The Soul of the Country is at Stake

We as American citizens need to fight against this worrying trend of censorship and mass surveillance. Other countries do not have our uniquely robust (that is to say, with few limitations) concept of freedom of speech/assembly. Thus we are in a unique position where **we are fighting not just to save lives, but perhaps more importantly, to save the soul of our country**.

So, we feel that we must say that the right to freedom of assembly (along with all of our other rights) are not luxuries that are graciously extended to us by the ruling class. On the contrary, the entire philosophy that birthed the United States views these rights as **inalienable**, that is to say, not dependent on some external factor. Now, judicial and historical precedent has shown that some extremely limited restrictions can be put on these rights. But such restrictions need to be as narrow as feasible, and must be backed by an incredibly rock-solid justification. Neither of those conditions have been met here. Those advocating a policy of containment, and with it, totalitarian-style lockdown, are not doing so based upon scientific evidence, but rather upon superstition and tribalism. Arguing against the lockdown should not be conflated with being "against science", whatever that all-too-common phrase is supposed to mean. Nor should naturalistic phenomena like that of "herd immunity" be viewed with suspicion.

Of particular concern is the widespread roll-out of censorship across our online platforms. This was sold to us as being used just to curtail the craziness of those who think that 5G is causing radiation sickness, or that healing crystals can cure disease. This was totally false; these powers of censorship were immediately used to engage in an unprecedented campaign of suppression. YouTube took down a video that was _posted by a well-known professional news organization_, which contained the _honest beliefs and insights of medical professionals_ Dr Erickson and Dr Masihi. It is true that their statements contained statistical errors and imprecise language, but that does not justify such censorship. **We don't defeat bad ideas by censoring them, we defeat them by shining a light on them**. Additionally, the talk (a) reflected their genuine beliefs, and (b) their overall conclusions and concepts espoused were entirely valid, (particularly regarding the dangers of immunological and social isolation) regardless of their questionable statistical figures. We note that there are scores of videos which cite false statistics that massively overestimate the mortality of COVID-19, that have not been removed, likely because they support the lockdown. **We need to fight back against the entire concept of "disinformation". Centralized authorities should not be allowed to decide what truth is, that is for each rational individual to decide for themselves**. Solving this problem is outside of the scope of the article, but needless to say, we believe this represents an existential threat to the fabric of our democratic republic.

These policies of censorship are particularly ironic when viewed in the lens of WHO's pattern of lying by omission: making statements that are technically true but omit important facts that would lead to a differing conclusion. The most egregious is the WHO statement that “there is currently no evidence that people who have recovered from COVID-19 and have antibodies are protected from a second infection” ([article](https://www.wvxu.org/post/chile-s-covid-19-card-sparks-controversy-over-uncertainty-evidence-about-immunity#stream/0)). Unlike other WHO statements, this statement was not a lie by omission, **it was an outright lie based off what we knew at the time**, and it forms part of a persistent pattern on part of the WHO to advocate for totalitarian policies while ironically having initially discouraged countries from closing borders during a global pandemic.

### Superstition endangers us all

Finally, we need to talk about the presence of widespread superstition regarding COVID-19. We're not talking about 5G or lizard people, we're talking about superstition being spread by our elected officials and by our media. Evidence-based reduction of disease transmission requires an intelligent understanding of the varying risk factors that contribute to disease. It cannot be oversimplified to trite phrases such as "stay home" (being outside while practicing physical distancing is, in our opinion, the best way to maintain mental/physical health while reducing transmission).

Wearing latex gloves does not magically protect against COVID-19; on the contrary, these gloves often serve as [fomites](https://en.wikipedia.org/wiki/Fomite) when used by those that do not understand proper sanitization and sterilization procedures. Similarly, dousing one's grocery store produce in Lysol is not a prudent move taken out of an abundance of caution, but **rather is the manifestation of OCD-like behavior** that we have shockingly encouraged in otherwise psychologically healthy individuals.

Needless to say, those suffering from OCD, paranoid schizophrenia, agoraphobia, social anxiety, generalized anxiety, and countless other mental health conditions are having their symptoms worsened by a culture of fear and mainstream-media-propagated misinformation that **was not an inevitable result of COVID-19**, but rather was our own doing. **These have real effects that hurt people in the real world**. One fascinating case study [documented the emergence of COVID-19 related paranoid delusions in a patient suffering from schizophrenic psychosis](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7162758/). It is unlikely, albeit still possible, that such manifestations would have emerged in a world where our public health officials were sticking to evidence-based public policy and neither causing baseless fear nor trying to give false hope through recommending broad usage of unproven treatments such as Hydroxychloroquine+Azithromycin. Both extremes are dangerous.

The usage of overly simplistic [thought-terminating phrases](https://en.wikipedia.org/wiki/Thought-terminating_clich%C3%A9), such as "flatten the curve", "hammer and dance", "stay inside", "stay safe", etc, have led to an environment where healthy dissent is met with derision and scorn, before being quickly censored by the powers-that-be. These phrases are used to terminate a discussion by pointing to a supposed self-evident fact, and dissent regarding the utility of these measures has been met with unprecedented levels of censorship that has been enabled, and indeed shepherded, by platforms such as Facebook, YouTube, and Twitter. This is not a healthy state of affairs and it does not equip us to frankly tackle public health challenges.

## Section 6: TL;DR - Simple Words Only

[Note: This section could be significantly improved. Check back in a couple days if interested, or track progress in [this issue](https://github.com/ryankemper/writings/issues/2)]

SARS-CoV-2 is a virus that can make you sick. Some people don't feel sick at all, some people feel a little bit sick, and a very small group of people, especially old people, get very sick and might die.

Our leaders have tried to stop people from getting sick by closing down schools and businesses. But schools and businesses are important, and in the long run they help people stay alive. Most of us don't get very sick, so we should focus on protecting the ones that do get very very sick.

We might get sick when "saliva" (spit) from other people gets onto us. We can reduce the chance of getting sick by washing our hands and not touching our face, and we can avoid making others sick by doing our best to avoid coughing or sneezing near other people. Some people may want to wear a mask to help avoid coughing, sneezing, or spitting on other people accidentally. They might also want to stay a few feet away from strangers to protect them.

Once you get sick, you can't get sick again for a long time. Eventually you might be able to get sick again, but it will not be nearly as bad. When enough people have gotten sick and then gotten better, the sickness can't spread any more.

## (The End) Help us improve this review

This is a living document and we encourage contributions in the form of pull requests or open issues. You can find the current list of open issues [here on Github](https://github.com/ryankemper/writings/issues). If you want to help flesh out the cited research, or feel that an argument is fallacious or could be improved, you are encouraged to open up a pull request [here](https://github.com/ryankemper/writings/pulls). You can also watch changes as they're made by checking the [commit history](https://github.com/ryankemper/writings/commits/master).

We will only accept contributions that we feel show a holistic understanding of the situation and fit with the style and intentions of this document, but if we end up rejecting your proposed changes we highly encourage you to [fork](https://en.wikipedia.org/wiki/Fork_(software_development)) and start your own branch.

Finally, you, the reader, are free to use or redistribute this content for any purpose. We merely request that you link back to the original post if citing/quoting it, but you are free to choose _not_ to do so.

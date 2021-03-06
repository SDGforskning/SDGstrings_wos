# Search query for SDG13 - Climate Action, Bergen topic-approach.

***Current status**: Not under active development, awaiting the action approaches to be finished. Similar to the original version (v2019.11).* 

**Contents**

1. Full query in copy-pasteable format
2. General notes about method for SDG13
3. Documentation and string sections for each target

## 1. Full query

<details>
  <summary>Click to show the final copy-pasteable full query for SDG13</summary>

```
TS=( ( ("educati*" OR "curriculum" OR "curricula" OR "institutional capacity" OR "human capacity" OR "systemic capacity" OR "awareness" OR "perception$" OR "technical knowledge transfer" OR "transfer of technical knowledge" OR "transfer of technolog*" OR "technology transfer$" OR "official development assistance" OR "official development aid" OR "foreign aid" OR "international aid" OR "cooperation fund" OR "investment$" OR "invest" OR "investing") AND ( (("climate change$" OR "global warming" OR "climatic change$") NEAR/15 ("mitigat*" OR "adapt*" OR "impact reduction" OR "early warning" OR "risk$") ) OR "climate mitigation" ) ) OR "Green climate fund" OR "climate action$" OR "climate governance" OR "climate mitigation" OR (("climate change$" OR "global warming" OR "climatic change$" OR "changing climate" OR (("climate" OR "atmospher*" OR "ocean") NEAR/3 "warming") OR (("sea ice*" OR "sea-ice" OR "glaci*") NEAR/5 ("melt*" OR "retreat*"OR "reced*")) OR ("permafrost" NEAR/3 ("degrada*" OR "decreas*" OR "melt*")) ) NEAR/10 ("action$" OR "sustainab*" OR "assessment$" OR "adapt*" OR "cope" OR "coping" OR "resilien*" OR "mitigat*" OR "impact reduction" OR "impact$" OR "effect$" OR "planning" OR "strateg*" OR "manag*" OR "policy" OR "policies" OR "legislat*" OR "govern*" OR "disaster risk reduction" OR "preparedness" ) ) OR ( ("GHG" OR "greenhouse gas" OR "greenhouse gases" OR "carbon footprint" OR ("climate" NEAR/5 ("anthropogenic" OR "human impact$")) ) ) OR (( "methane" OR "CH4" OR "nitrous oxide" OR "N2O" OR "carbon dioxide" OR "CO2" OR "carbon emissions" OR "hydrofluorocarbons" OR "HFCs" OR "perfluorocarbons" OR "PFCs" OR "sulphur hexafluoride" OR "sulfur hexafluoride" OR "SF6" ) AND ("climate change$" OR "climatic change$" OR "global warming" OR "changing climate" OR (("climate" OR "atmospher*" OR "ocean") NEAR/3 "warming") ) ) OR ((( ("hazard*" OR "catastroph*" OR "disaster*" OR ("extreme$" NEAR/3 ("climat*" OR "weather" OR "precipitation")) OR "drought$" OR "flood*" OR "collaps*" OR "tipping point" OR ("sea level" NEAR/3 ("chang*" OR "rising" OR "rise$")) ) ) OR "Livelihood Vulnerability Index" ) AND ("climate change$" OR "climatic change$" OR "global warming" OR "changing climate" OR (("climate" OR "atmospher*" OR "ocean") NEAR/3 "warming")) ) OR ("Kyoto protocol" OR "Paris Agreement" OR "COP 21" OR "COP21" OR "COP 22" OR "COP22" OR "COP 23" OR "COP23" OR "COP 24" OR "COP24" OR "UNFCCC" OR "United Nations Framework Convention on Climate Change" ) OR ("SDG13" OR "SDG$ 13" OR "SDG-13" OR "sustainable development goal$ 13" OR (("sustainable development goal$" OR "SDG$" OR "goal 13") NEAR/15 "climate")) )
```
</details>

## 2. General notes

Source of Targets and Indicators:
Statistics Division. (2021). *Global indicator framework for the Sustainable Development Goals and targets of the 2030 Agenda for Sustainable Development*. A/RES/71/313, E/CN.3/2018/2, E/CN.3/2019/2, E/CN.3/2020/2, E/CN.3/2021/2. Department of Economic and Social Affairs, United Nations. https://unstats.un.org/sdgs/indicators/Global%20Indicator%20Framework%20after%202021%20refinement_Eng.pdf [accessed 8 August 2021]
<sup id="SDGT+Is">[1](#f1)</sup>

* Definition of "capacity" : "[...] the ability of people, organizations and society as a whole to manage their affairs successfully"<sup id="UNDGcapacity">[2](#f2)</sup>.
* Definition of "capacity development" : "the process whereby people, organizations and society as a whole unleash, strengthen, create, adapt, and maintain capacity over time, in order to achieve development results"<sup id="UNDGcapacity">[2](#f2)</sup>.

## 3. Targets

## Target 13.1

> **13.1 Strengthen resilience and adaptive capacity to climate-related hazards and natural disasters in all countries**
>
>13.1.1 Number of deaths, missing persons and directly affected persons attributed to disasters per 100,000 population
>
>13.1.2 Number of countries that adopt and implement national disaster risk reduction strategies in line with the Sendai Framework for Disaster Risk Reduction 2015???2030
>
>13.1.3 Proportion of local governments that adopt and implement local disaster risk reduction strategies in line with national disaster risk reduction strategies

This query consists of 1 phrase.

``` Ceylon =
TS=
(
  (
  "hazard*" OR "catastroph*" OR "disaster*"
  OR ("extreme$" NEAR/3 ("climat*" OR "weather" OR "precipitation"))
  OR "drought$" OR "flood*"
  OR "collaps*" OR "tipping point"  
  OR ("sea level" NEAR/3 ("chang*" OR "rising" OR "rise$"))
  OR "livelihood vulnerability index"
  )
  AND
      ("climate change$" OR "climatic change$" OR "global warming" OR "changing climate"
      OR
        (("climate" OR "atmospher*" OR "ocean") NEAR/3 "warming")
      )
)
```

## Target 13.2, 13.3 (part) & 13.b

> **13.2 Integrate climate change measures into national policies, strategies and planning**
>
>13.2.1 Number of countries with nationally determined contributions, long-term strategies, national adaptation plans and adaptation communications, as reported to the secretariat of the United Nations Framework Convention on Climate Change
>
>13.2.2 Total greenhouse gas emissions per year		

> **13.3 Improve education, awareness-raising and human and institutional capacity on climate change mitigation, adaptation, impact reduction and early warning**
>
>13.3.1 Extent to which (i) global citizenship education and (ii) education for sustainable development are mainstreamed in (a) national education policies; (b) curricula; (c) teacher education; and (d) student assessment

> **13.b Promote mechanisms for raising capacity for effective climate change-related planning and management in least developed countries and small island developing States, including focusing on women, youth and local and marginalized communities**
>
>13.b.1 Number of least developed countries and small island developing States with nationally determined contributions, long-term strategies, national adaptation plans and adaptation communications, as reported to the secretariat of the United Nations Framework Convention on Climate Change

This query consists of 5 phrases.

Carbon capture/storage technology can contribute to climate mitigation (i.e. reduction of GHG) but in order to be consistent with our target interpretation method, any papers concerning it must relate the work to climate mitigation or reductions of GHG to be included. The same would apply to reforestation or other mitigation measures. Thus these are not included as individual search terms.

Re target 13.3 - Interpretatation of what should be considered as contributing to "human and institutional capacity" is challenging - according to the UNDG definition, it concerns anything that would increase the ability of people and institutions to successfully manage climate change mitigation, adaption, impact reduction and early warning. Here consider we that all research on these topics would contribute, and therefore they do not have to be combined with the concept of capacity.

##### Phrase 1:

``` Ceylon =
TS=
(
  "climate action$" OR "climate governance" OR "climate mitigation"  
)
```

##### Phrase 2:

Polar and alpine regions much in focus regarding climate change impacts.

Note that although target 14.B focuses on CC planning and management in small island developing states and least developed countries, other targets concern these things for all countries. Therefore we have not specified LDC or SIDS here - they will be included with the rest.

``` Ceylon =
TS=
(
  ("climate change$" OR "global warming" OR "climatic change$" OR "changing climate"
  OR (("climate" OR "atmospher*" OR "ocean") NEAR/3 "warming")
  OR (("sea ice*" OR "sea-ice" OR "glaci*") NEAR/5 ("melt*" OR "retreat*"OR "reced*"))
  OR ("permafrost" NEAR/3 ("degrada*" OR "decreas*" OR "melt*"))  
  )
  NEAR/10
      ("action$" OR "sustainab*" OR "assessment$"
      OR "adapt*" OR "cope" OR "coping" OR "resilien*" OR "mitigat*"
      OR "impact reduction"
      OR "impact$" OR "effect$"
      OR "planning" OR "strateg*" OR "manag*"
      OR "policy" OR "policies" OR "legislat*" OR "govern*"
      OR "disaster risk reduction" OR "preparedness"
      )
)
```

##### Phrase 3:

Reduction of GHGs = climate mitigation according to UNEP definition

``` Ceylon =
TS=
(
    "GHG" OR "greenhouse gas" OR "greenhouse gases"
    OR "carbon footprint"
    OR ("climate" NEAR/5 ("anthropogenic" OR "human impact$"))
)
```

##### Phrase 4:

The second part of this phrase covers the six main greenhouse gases (covered by the Kyoto Protocol) as listed in the 2014 IPCC Synthesis Report<sup id="IPCC2014">[3](#f4)</sup>.  

``` Ceylon =
TS=
(
  ("methane" OR "CH4" OR "nitrous oxide" OR "N2O" OR "carbon dioxide" OR "CO2" OR "carbon emissions"
  OR "hydrofluorocarbons" OR "HFCs" OR "perfluorocarbons" OR "PFCs" OR "sulphur hexafluoride" OR "sulfur hexafluoride" OR "SF6"
  )
  AND
    ("climate change$" OR "climatic change$" OR "global warming" OR "changing climate"
    OR (("climate" OR "atmospher*" OR "ocean") NEAR/3 "warming")
    )
)
```

##### Phrase 5:

Frameworks for action are included, as documents referencing these are likely to be discussing climate action (i.e. applied climate science rather than basic). This does pick up some results to do with energy transitions, but generally as related to climate. IPCC not included as their scenarios are referred to as a reference very often and in fields not necessarily directly contributing to the targets.

``` Ceylon =
TS=
(
  "Kyoto protocol"
  OR "Paris Agreement"
  OR "COP 21" OR "COP21" OR "COP 22" OR "COP22" OR "COP 23" OR "COP23" OR "COP 24" OR "COP24"
  OR "UNFCCC" OR "United Nations Framework Convention on Climate Change"
)
```

## Target 13.3 (part) & 13.a								

> **13.3 Improve education, awareness-raising and human and institutional capacity on climate change mitigation, adaptation, impact reduction and early warning**
>
>13.3.1 Extent to which (i) global citizenship education and (ii) education for sustainable development are mainstreamed in (a) national education policies; (b) curricula; (c) teacher education; and (d) student assessment

> **13.a Implement the commitment undertaken by developed-country parties to the United Nations Framework Convention on Climate Change to a goal of mobilizing jointly $100??billion annually by 2020 from all sources to address the needs of developing countries in the context of meaningful mitigation actions and transparency on implementation and fully operationalize the Green Climate Fund through its capitalization as soon as possible**
>
>13.a.1 Amounts provided and mobilized in United States dollars per year in relation to the continued existing collective mobilization goal of the $100 billion commitment through to 2025

This query consists of 1 phrase.

`Green climate fund` is a dedicated climate fund.

``` Ceylon =
TS=
(
  (
    ("educati*" OR "curriculum" OR "curricula"
    OR "institutional capacity" OR "human capacity" OR "systemic capacity"
    OR "awareness" OR "perception$"
    OR "technical knowledge transfer" OR "transfer of technical knowledge" OR "transfer of technolog*" OR "technology transfer$"
    OR "official development assistance" OR "official development aid" OR "foreign aid" OR "international aid" OR "cooperation fund" OR "investment$" OR "invest" OR "investing"
    )
    AND
        ("climate mitigation"
        OR
          (
            ("climate change$" OR "global warming" OR "climatic change$")
            NEAR/15
                ("mitigat*" OR "adapt*" OR "impact reduction" OR "early warning" OR "risk$")
          )
        )
  )
  OR "green climate fund"
)
```

## General SDG

``` Ceylon =
TS=
(
  "SDG13" OR "SDG$ 13" OR "SDG-13" OR "sustainable development goal$ 13"
  OR
    (
      ("sustainable development goal$" OR "SDG$" OR "goal 13")
      NEAR/15 "climate"
    )
)
```

## Footnotes
<b id="f1">1</b> This list includes "the global indicator framework as contained in A/RES/71/313, the refinements agreed by the Statistical Commission at its 49th session in March 2018 (E/CN.3/2018/2, Annex II) and 50th session in March 2019 (E/CN.3/2019/2, Annex II), changes from the 2020 Comprehensive Review (E/CN.3/2020/2, Annex II) and refinements (E/CN.3/2020/2, Annex III) from the 51st session in March 2020, and refinements from the 52nd session in March 2021 (E/CN.3/2021/2, Annex)".
(https://unstats.un.org/sdgs/indicators/indicators-list/) [???](#SDGT+Is)

<b id="f2">2</b> United Nations Development Group (2017) Capacity Development, UNDAF companion guidance. https://unsdg.un.org/resources/capacity-development-undaf-companion-guidance [accessed 19.12.2019] [???](#UNDGcapacity)

<b id="f3">3</b> IPCC, 2014: Climate Change 2014: Synthesis Report. Contribution of Working Groups I, II and III to the Fifth Assessment Report of the Intergovernmental Panel on Climate Change [Core Writing Team, R.K. Pachauri and L.A. Meyer (eds.)]. IPCC, Geneva, Switzerland, 151 pp. [???](#IPCC2014)

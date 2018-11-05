# Risk Management Tools based on Scaling Laws and Directional-Change Intrinsic Time

This public GitHub repository has been prepared as part of the European research initiative <a href="http://bigdatafinance.eu/">BigDataFinance 2015–2019</a>, an H2020 Marie Sklodowska-Curie Innovative Training Network “Training for Big Data in Financial Research and Risk Management”. The name of the corresponding project is "RP12: High-Frequency Trading Risk Management Tools Based on Scaling Laws". 

The repository contains a set of risk management and data analysis tools build using the theory of scaling laws in finance extensively outlined in work "Patterns in high-frequency FX data: discovery of 12 empirical scaling laws" (available <a href="https://www.tandfonline.com/doi/full/10.1080/14697688.2010.481632?casa_token=YrC9jdNgqoEAAAAA:QLUBgm93lnxMJTL3G6j4RBBCnep4yMQP7KKax2HBlchjdTXbl6fwkHhuFhyzZKjNsik3MWiVuuEO">online</a>) and the directional-change intrinsic time approach first time proposed in "A geographical model for the daily and weekly seasonal volatility in the foreign exchange market" (available <a href="https://www.sciencedirect.com/science/article/pii/026156069390004U">online</a>). Each folder contains classed and sets of methods written using the class-based and object-oriented computer-programming language Java. All files have self-explanatory names and are equipped by a detailed description of the main functionality as well as the references to the literature where these methods have first been described and validated.

All included tools have been tested using extensive sets of high-frequency data from the Forex and others high-frequency markets. Results of the tests are described in multiple research papers which are either submitted to peer-review journals or are at the final stage on the work and will be added to the description as soon as they reach any public resource. Among the submitted papers: "Instantaneous Volatility Seasonality of Bitcoin in Directional-Change Intrinsic Time" (<a href="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3243797">at SSRN</a>) and "Agent-Based Model in Directional-Change Intrinsic Time" (<a href="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3240456">at SSRN</a>).

<h3>The root directory contains several methods which can be directly employed for high-frequency real-time data analysis:</h3>

<ul>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/LiquidityIndicator_Analysis.java">LiquidityIndicator_Analysis.java</a></strong> - computes liquidity of historical time series represented by tick-by-tick price data  using the multiscale interpretation of liquidity based on the directional change and scaling laws. It is a wrapper for the "LiquidityIndicator" class from the "ievent" folder. To run the program one needs to specify the path to the analysed file and set up several parameters described at the header of the code.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/InstantaneousVolatilityActivity_Analisys.java">InstantaneousVolatilityActivity_Analisys.java</a></strong> - this class is the extension of the "ievents/VolatilitySeasonality" class modifies to be applicable to the set of historical or real-time high-frequency price data.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/VolatilityEstimatorMovingWindow_Analysis.java">VolatilityEstimatorMovingWindow_Analysis.java</a></strong> - this class is designed to perform the volatility analysis of high-frequency data computed in two ways: using the sum of squared return function which calculates the aggregated standard deviation of the time series over fixed and equal intervals and using the method based on the directional-change intrinsic time approach in detail described in the <a href="https://github.com/VladUZH/VlPetrov/blob/master/src/ievents/RealizedVolatility.java">RealizedVolatility.java</a> class.</li>
</ul>


<h3>The <em><a href="https://github.com/VladUZH/VlPetrov/tree/master/src/ievents">ievents</a></em> folder contains classes and methods related to the directional-change intrinsic time concept proposed and described in work "A geographical model for the daily and weekly seasonal volatility in the foreign exchange market" (available <a href="https://www.sciencedirect.com/science/article/pii/026156069390004U">online</a>): </h3>

<ul>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/ievents/DcOS.java">DcOS.java</a></strong> - Directional-Change dissection algorithm splits a historical price time series into a collection of directional-change  and overshoot points defined as the sequence of alternating trend changes of selected size.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/ievents/IE.java">IE.java</a></strong> - is an auxiliary class to keep information on the properties of each observed intrinsic event such as time and price levels.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/ievents/IntrinsicNetwork.java">IntrinsicNetwork.java</a></strong> - is an example of the Intrinsic Network introduced in the "Multi-scale Representation of High Frequency Market Liquidity" paper (available <a href="https://content.iospress.com/articles/algorithmic-finance/af054">online</a>).</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/ievents/LiquidityIndicator.java">LiquidityIndicator.java</a></strong> - is a realization of the liquidity indicator proposed in the research work "Multi-scale Representation of High Frequency Market Liquidity" (available <a href="https://content.iospress.com/articles/algorithmic-finance/af054">online</a>).</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/ievents/InstantaneousVolatility.java">InstantaneousVolatility.java</a></strong> - is the method used to translate the number of observed directional-change intrinsic events into the value of the instantaneous volatility. The approach is outlined in the research paper "Instantaneous Volatility Seasonality of Bitcoin in Directional-Change Intrinsic Time" (available <a href="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3243797">online</a>).</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/ievents/MovingWindowVolatilityEstimator.java">MovingWindowVolatilityEstimator.java</a></strong> - is the instantaneous volatility estimator based on the number of Directional Changes observed over given period of time (set as a parameter of the method) and described in the paper "Instantaneous Volatility Seasonality of Bitcoin in Directional-Change Intrinsic Time" (<a href="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3243797">available online</a>).</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/ievents/RealizedVolatility.java">RealizedVolatility.java</a></strong> - is the class where the realized volatility is computed using the number of observed directional-change intrinsic events combined with the variability of overshoots proceeding each directional change. The main idea of the approach is in details described in the paper "Bridging the gap between physical and intrinsic time" (work in progress).</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/ievents/RealizedVolatilitySeasonality.java">RealizedVolatilitySeasonality.java</a></strong> - based on the <a href="https://github.com/VladUZH/VlPetrov/blob/master/src/ievents/RealizedVolatility.java">RealizedVolatility.java</a> method this class provides a novel way of computing weekly seasonality of the realized volatility considering the evolution of the price curve from the point of view of directional-change intrinsic events.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/ievents/InstantaneousVolatilitySeasonality.java">InatantaneousVolatilitySeasonality.java</a></strong> - based on the <a href="https://github.com/VladUZH/VlPetrov/blob/master/src/ievents/InstantaneousVolatility.java">InstantaneousVolatility.java</a> method this class provides a novel way of computing weekly seasonality of the instantaneous volatility considering the evolution of the price curve from the point of view of directional-change intrinsic events.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/ievents/DcOSmultD.java">DcOSmultiD.java</a></strong> - is the extension of the originally one-dimensional version of the directional-change intrinsic time algorithm (class <a href="https://github.com/VladUZH/VlPetrov/blob/master/src/ievents/DcOS.java">DcOS.java</a>) to the multidimensional space. The space is formed by orthogonally placed independent exchange rates. The description of the multidimensional approach is provided in the paper "Multidimensional Directional-Change Intrinsic Time" (work in progress).</li>
</ul>

<h3>Folder <em><a href="https://github.com/VladUZH/VlPetrov/tree/master/src/scalinglaws">scalinglaws</a></em> contains tools which allow extracting scaling laws based on the directional-change intrinsic time as described in the paper "Patterns in high-frequency FX data: Discovery of 12 empirical scaling laws" (available <a href="https://www.tandfonline.com/doi/full/10.1080/14697688.2010.481632?casa_token=m2x82H9VNj0AAAAA:HxxRW0hHJb9vwtkg5S3ukhfglI58AzSWAND89y7JXRY5VIGprfGcuQvoR6VTPkgV4yP_lhogrPVsbg">online</a>). Numbers of scaling laws follow the same order selected in the paper. The code has been validated using high-frequency data from Forex and Bitcoin markets (work in progress):</h3>

<ul>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/MeanPriceMoveScalingLaw.java">MeanPriceMoveScalingLaw.java</a></strong> - "Mean price move scaling law", Law 0a, p=1.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/QuadraticMeanPriceMoveScalingLaw.java">QuadraticMeanPriceMoveScalingLaw.java</a></strong> - "Quadratic mean price move scaling law", Law 0a, p=2.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/DCcountScalingLaw.java">DCcountScalingLaw.java</a></strong> - "Number of Directional-Changes scaling law", Law 0b.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/PriceMoveCountScalingLaw.java">PriceMoveCountScalingLaw.java</a></strong> - "Price move count scaling law", Law 2.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/MaxPriceMoveScalingLaw.java">MaxPriceMoveScalingLaw.java</a></strong> - "Maximal price move during scaling law", Law 3, p=1.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/QuadraticMeanMaxPriceMoveScalingLaw.java">QuadraticMeanMaxPriceMoveScalingLaw.java</a></strong> - "Maximal price move during scaling law", Law 3, p=2.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/MeanTimePriceMoveScalingLaw.java">MeanTimePriceMoveScalingLaw.java</a></strong> - "Mean time of price move scaling law", Law 4.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/TimeDuringDCScalingLaw.java">TimeDuringDCScalingLaw.java</a></strong> - "Time during directional-change scaling law", Law 5.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/TotalMoveScalingLaw.java">TotalMoveScalingLaw.java</a></strong> - "Total move scaling law", Law 9(tm).</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/OSmoveScalingLaw.java">OSmoveScalingLaw.java</a></strong> - "Overshoot scaling law", Law 9(os).</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/DCmoveScalingLaw.java">DCmoveScalingLaw.java</a></strong> - "Directional-change move scaling law", Law 9(dc).</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/TimeTotMoveScalLaw.java">TimeTotMoveScalLaw.java</a></strong> - "Time total-move scaling law", Law 10(tm).</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/TimeDCScalingLaw.java">TimeDCScalingLaw.java</a></strong> - "Time of directional change scaling law", Law 10(dc).</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/TimeOSScalingLaw.java">TimeOSScalingLaw.java</a></strong> - "Time of overshoot scaling law", Law 10(os).</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/TMtickCountScalingLaw.java">TMtickCountScalingLaw.java</a></strong> - "Total move tick count scaling law", Law 11(tm).</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/DCtickCountScalingLaw.java">DCtickCountScalingLaw.java</a></strong> - "Directional change tick count scaling law", Law 11(dc).</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/OStickCountScalingLaw.java">OStickCountScalingLaw.java</a></strong> - "Overshoot tick count scaling law", Law 11(os).</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/CumulTMScalingLaw.java">CumulTMScalingLaw.java</a></strong> - "Cumulative total move scaling law" (coastline), Law 12(tm).</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/CumulOSScalingLaw.java">CumulOSScalingLaw.java</a></strong> - "Cumulative overshoot scaling law", Law 12(os).</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/scalinglaws/CumulDCScalingLaw.java">CumulDCScalingLaw.java</a></strong> - "Cumulative directional change scaling law", Law 12(dc).</li>
</ul>

<h3>Folder <em><a href="https://github.com/VladUZH/VlPetrov/tree/master/src/market">market</a></em> contains a set of auxiliary tools nucessarily to perform the real application of risk management tools presented in the repository:</h3>

<ul>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/market/Price.java">Price.java</a></strong> - is a simple class for elementary prices corresponding to some given moment of time. These are tick prices by default. Each class instance holds information on the bid and ask price levels as well as the time of when the new tick was registered.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/market/SpreadInfo.java">SpreadInfo.java</a></strong> - this method, applied to a historical (or real-time streamed) time series, returns Median, Mean, Min and Max spread characteristics characterised some given period of time.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/market/PriceMultiD.java">PriceMultiD.java</a></strong> - is the class to keep information on the multidimensional structure of prices used for the multidimensional version of the directional-change intrinsic time <a href="https://github.com/VladUZH/VlPetrov/blob/master/src/ievents/DcOSmultD.java">algorithm</a>. Collections of bid and ask prices composing each instance of the class are formed by individual components of exchange rates used in an experiment.</li>
</ul>

<h3>Folder <em><a href="https://github.com/VladUZH/VlPetrov/tree/master/src/tools">tools</a></em> is a collection of some traditional data management tools employed to analyse historical and real-time streams of high-frequency data:</h3>

<ul>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/tools/BM.java">BM.java</a></strong> - is the class used to generate time series of given lengths properties of which coincide with properties of simple Brownian Motion process.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/tools/GBM.java">GBM.java</a></strong>  - is the class used to generate time series of given lengths following Geometrical Brownian Motion process.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/tools/TraditionalVolatility.java">TraditionalVolatility.java</a></strong> - this class is traditional volatility estimator. Computes volatility of a given time series using the sum of squared returns.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/tools/MovingWindowVolatilityEstimator.java">MovingWindowVolatilityEstimator.java</a></strong> - is the classical volatility estimator which performs over a moving window the length of which is defined as a parameter of the code. The algorithm is based on the sum of squared returns computed over equal time intervals.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/tools/Tools.java">Tools.java</a></strong> - is a class containing a subset of simple methods used over the whole research work on the scaling laws and intrinsic time risk-management tools. The class is crucial for the stable work of almost all related experiments.</li>
<li><strong><a href="https://github.com/VladUZH/VlPetrov/blob/master/src/tools/ThetaTime.java">ThetaTime.java</a></strong> - is the class the idea of which is to perform as theta-time presented in work of "A geographical model for the daily and weekly seasonal volatility in the foreign exchange market" (available <a href="https://www.sciencedirect.com/science/article/pii/026156069390004U">online</a>).</li>
</ul>

<em>The project leading to this collection of tools has received funding from the European Union’s Horizon 2020 research and innovation programme under the Marie Skłodowska-Curie grant agreement No 675044</em>

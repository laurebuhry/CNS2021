# CNS 2021 Workshop "Clinical computational neuroscience: How computational neuroscience can solve problems from the clinic"

<script src="moment.js"></script>
<script src="moment-timezone-with-data.js"></script>

## Organizers: Xenia Kobeleva and Laure Buhry

## Date: July 7th  — 9:30 am to 5:45 pm (Paris Time)

## Description:

Despite great advances in understanding of brain function using computational neuroscience, complex neural activity analyses and models are rarely used for clinical purposes. This workshop aims to bridge this gap and to bring computational neuroscientists and clinicians together to discuss current challenges and solutions for bringing more computational neuroscience to patient-oriented questions. Topics will include translation from animal models to patients, exploration of virtual therapies and personalized medicine. Apart from several success stories of clinical computational neuroscience, we will also have discussion rounds to deep dive into current challenges of the computational neuroscience community and their potential solutions. The outcome of the workshop will be to:

* inform interested researchers on clinically relevant questions
* provide an overview of computational tools that can be used to answer these questions
* establish a working group on clinical computational neuroscience for all interested researchers and discuss practical steps to work on the roadblocks that were identified during the workshop
stablish a working group on clinical computational neuroscience for all interested researchers and discuss practical steps to work on the roadblocks that were identified during the workshop

The day will be organized around three challenges:
* [Challenge 1: Translation from animal models to patients: bridging species and scales](#ch1)
* [Challenge 2: Virtual therapies: exploring new options and refining existing treatments](#ch2)
* [Challenge 3: Personalized medicine: how to make models fit the patient](#ch3)

## Schedule

<script>
var start_time = moment.tz("2021-07-03 15:00", "Europe/Berlin"); // !!! also update start time in the <noscript> table in plain HTML

s = "<label for=\"tz-selector\">Timezone:&nbsp;</label>";
s += "<select class=\"select-css\" name=\"tz-selector\" id=\"tz-selector\" onChange=\"printTable(document.getElementById('schedule'), document.getElementById('tz-selector').value);\">";

moment.tz.names().forEach(function (item, index) {
	s += "<option value=\"" + item + "\"";
	if (item.localeCompare("Europe/Berlin") == 0) {
		s += " selected=\"selected\"";
	}
	s += ">" + item + "</option>";
});

s += "</select>";
document.write(s);

document.getElementById('tz-selector').value = "Europe/Berlin";

function printTable(el, in_tz) {
	//alert(in_tz);
	for (var i = 0; i < document.getElementsByClassName('timecell').length; ++i) {
		item = document.getElementsByClassName('timecell')[i];
		berlin_time = item.querySelector('noscript').innerHTML.replace(/^\s+|\s+$/g, '');
		//alert('old time: ' + berlin_time);
		//alert('attempted new time: ' + start_time.format("YYYY-MM-DD hh:mm:ss").slice(0, -8) + berlin_time + ":00");
		new_time = moment.tz(start_time.format("YYYY-MM-DD hh:mm:ss").slice(0, -8) + berlin_time + ":00", "Europe/Berlin").tz(in_tz);
		//alert('new time: ' + new_time.format());
		item.innerHTML = "<noscript>" + berlin_time + "</noscript>" + new_time.format('HH:mm');
	}
}

window.addEventListener('load', (event) => {
	printTable(document.getElementById('schedule'), document.getElementById('tz-selector').value);
});

</script>
<div id="schedule" name="schedule">
<table>
<tr>
<th>Time <noscript>(Berlin<br>timezone)</noscript></th>
<th>Description</th>
</tr>
<tr>
<td class="timecell"><noscript>09:30</noscript></td>
<td>Welcome and Introduction</td>
</tr>
	
<tr>
<td class="timecell"><noscript>09:45</noscript></td>
<td><a href="#Kirk">Kirk Leech: Update on the use of animals in research</a></td>
</tr>
	
<tr>
<td class="timecell"><noscript>10:15</noscript></td>
<td><a href="#Matthieu">Matthieu Gilson: Bridging spatial scales in biophysical models for translational clinical applications</a></td>
</tr>
	
<tr>
<td class="timecell"><noscript>10:45</noscript></td>
<td>Panel discussion</td>
</tr>
	
<tr>
<td class="timecell"><noscript>11:15</noscript></td>
<td>Break</td>
</tr>
	
<tr>
<td class="timecell"><noscript>11:30</noscript></td>
<td><a href="#Yujiang">Yujiang Wang: Towards time-adaptive treatments in epilepsy using data-driven subject-specific models</a></td>
</tr>
	
<tr>
<td class="timecell"><noscript>12:00</noscript></td>
<td><a href="#Jil">Jil Meier: Multiscale co-simulation of deep brain stimulation</a></td>
</tr>
	
<tr>
<td class="timecell"><noscript>13:00</noscript></td>
<td>Break</td>
</tr>
	
<tr>
<td class="timecell"><noscript>14:00</noscript></td>
<td><a href="#Christian">Christian Meisel: Resilience in neural systems: from an understanding based on dynamical principles towards clinical diagnostics</a></td>
</tr>
	
<tr>
<td class="timecell"><noscript>14:30</noscript></td>
<td><a href="#Vesna">Vesna Vuksanovic: Data-driven approach to neuroimaging analysis to identify dementia subtypes</a></td>
</tr>
	
<tr>
<td class="timecell"><noscript>15:00</noscript></td>
<td><a href="#Peter">Peter Hitchcock: On the Importance of Incorporating Time and Context in Computational Psychiatry Models</a></td>
</tr>
	
<tr>
<td class="timecell"><noscript>16:00</noscript></td>
<td>Break</td>
</tr>
		
<tr>
<td class="timecell"><noscript>16:30</noscript></td>
<td>Final discussion</td>
</tr>
	
</table>
</div>

## Registration
Please don’t forget to register for the conference at [https://www.cnsorg.org/cns-2021](https://www.cnsorg.org/cns-2021)

## Speakers
* [Kirk Leech, Executive Director of The European Animal Research Association (EARA)](#Kirk)
* [Matthieu Gilson, Institute of Neuroscience and Medicine (INM-6) and Institute for Advanced Simulation (IAS-6) and JARA Institute Brain Structure-Function Relationships (INM-10), Jülich Research Centre, Jülich, Germany, and Center for Brain and Cognition, Department of Information and Telecommunication technologies, Universitat Pompeu Fabra, Barcelona, Spain](#Matthieu)
* [Julien Modolo (panel discussion), Research Scientist at INSERM, LTSI (Laboratory of Signal and Image processing) Rennes, France](#Julien)
* [Yujiang Wang, CNNP Lab, Interdisciplinary Computing and ComplexBioSystems Group, School of Computing, Newcastle University, Newcastle upon Tyne, United Kingdom](#Yujiang)
* [Jil Meier, Berlin Institute of Health at Charité – Universitätsmedizin Berlin, Berlin, Germany, and Charité – Universitätsmedizin Berlin, corporate member of Freie Universität Berlin and Humboldt-Universität zu Berlin, Department of Neurology with Experimental Neurology, Brain Simulation Section, Berlin, Germany](#Jil)
* [Christian Meisel, Department of Neurology, Charité – Universitätsmedizin Berlin and Berlin Institute of Health, Berlin, Germany](#Christian)
* [Vesna Vuksanovic, Swansea University Medical School and Health Data Research United Kingdom](#Vesna)
* [Peter Hitchcock, Cognitive, Linguistic, and Psychological Sciences, Brown University, Providence, RI](#Peter)

## Talk abstracts:

## Challenge 1: Translation from animal models to patients: bridging species and scales<a name="ch1"></a>

### Kirk Leech<a name="Kirk"></a>
### Title: Update on the use of animals in research

The goal of this talk would be, for computational neuroscientists, to gain insight into the place of computational approaches in the translation from animal models to patients.

The talk will focus on the need for the research community to more pro-actively engage with regulators, media and public on the need for animals in research. I will use the recent example of EURL ECVAM proposals to immediately end the use of animal derived anti-bodies in research as an example of the dangers of the research community ‘falling asleep at the wheel’ whilst those totally opposed to animal use are increasing their engagement with regulators. I will also explain how European transparency agreements work – there are now 5 in operation, involving close to 340 institutions (with three more agreements close) – to show how they can play a role in improving public understanding and acceptance of animal research, including where we can and currently can’t move away from animal use.

#### Matthieu Gilson<a name="Matthieu"></a>
### Title: Bridging spatial scales in biophysical models for translational clinical applications

A great deal of dynamic models have been developed to reproduce signals obtained from neuroimaging techniques in order to formalize the relationship between structure and function. Such models typically relate empirical data like anatomical connectivity with mechanisms that describe the neuronal dynamics, which may be modelled at the microscopic level using spiking neurons or at a more mesoscopic level using neuronal population nodes. For neurology or neuropsychiatry, the computational models have been extended to incorporate data like neuromodulator or gene expression maps, which are of importance for neuropathologies. The goal is then to uncover their influence in shaping the activity patterns at the whole brain level. Such a model construction implies a number of choices in the design for the mechanisms, as well as parameters to estimate or set.

In this talk I will focus on models for functional magnetic resonance imaging (fMRI) and review recent advances in the direction of clinical research. Meanwhile pointing at strengths and limitations of those studies, I will argue for a modelling that keeps a balance between predictability and interpretability. The former is to be understood in the sense of enabling a robust decoding of the fMRI activity patterns for distinct conditions (e.g. patients versus controls, or different pathological subtypes) using the estimated model parameters to derive biomarkers. The latter is necessary to relate the model parameters back to biological variables, and uncover the mechanisms involved in the neuropathological activity, beyond a « simple » phenomenological or statistical analysis of the empirical data. This perspective has been recently developed in an opinion article [1], which proposes to combine decoding and biophysical models to achieve the desired modelling requirements.

### Julien Modolo (panel discussion)<a name="Julien"></a>
The translation of neuromodulation strategies from in vivo to in clinico is notoriously challenging. Among those challenges, emerging approaches attempt at combining morphological and computational approaches of electric field dosimetry combined with realistic models of neuronal activity to predict the response of brain tissue to specific neuromodulation sequences. In this discussion panel, I will discuss existing strategies on the topic, along with their assumptions and capabilities, and how this could bring neuromodulation faster from animal to human studies.


## Challenge 2: Virtual therapies: exploring new options and refining existing treatments<a name="ch2"></a>

### Yujiang Wang<a name="Yujiang"></a>
### Title: Towards time-adaptive treatments in epilepsy using data-driven subject-specific models

Epilepsy is increasingly being recognised as a dynamic disease, where seizure characteristics and severity change over time in each patient. Understanding why, in the same patient, one seizure is severe and debilitating, while the next seizure is relatively mild in symptoms is crucial for developing time-adaptive treatments that can render severe seizure into more benign forms.
To this end, we recently investigated over 500 seizure EEGs and found variable electrographic seizure dynamics within individual patients [1]. A detailed analysis of the nature of this within-subject variability revealed that specific recurrent patterns of brain dynamics during seizures can be of variable duration in each seizure or be completely absent [2]. Importantly, the variability appeared to follow subject-specific circadian or longer timescale modulations.
We hypothesise that markers of these modulations on different timescales can be captured on continuously recorded EEG data over days to years. In this talk I will show that several features in the continuously recorded EEG display fluctuations on ultradian, circadian, and infradian timescales, and several subject-specific timescales are strongly associated with the presence/absence or duration of recurrent patterns in each patient. Finally, I will also demonstrate that these fluctuations on different timescale provide a good explanation (above chance level) for how seizures change over time in each patient [3].
Our results indicate that slow (ultradian, circadian, and infradian) fluctuations captured from continuously recorded EEG may serve as a biomarker to track and predict how seizures change over time. This is an important step in interacting and controlling the seizure-modulating fluctuation. Ultimately, time-adaptive treatments (e.g. via drug-delivery systems) could not only render severe seizure into more benign forms, but may be able to suppress symptomatic seizures altogether, whilst reducing side-effects.


### Jil Meier<a name="Jil"></a>
### Title: Multiscale co-simulation of deep brain stimulation

Deep brain stimulation (DBS) has been successfully applied in various neurodegenerative diseases as an effective symptomatic treatment. However, its mechanisms of action within the brain network are still poorly understood. Many virtual DBS models analyze a subnetwork around the basal ganglia and its dynamics as a spiking network with their details validated by experimental data. However, connectomic evidence shows widespread effects of DBS affecting many different cortical and subcortical areas. From a clinical perspective, various effects of DBS besides the motoric impact have been demonstrated. The neuroinformatics platform The Virtual Brain (TVB) offers a modeling framework allowing us to virtually perform stimulation, including DBS, and forecast the outcome from a dynamic systems perspective prior to invasive surgery with DBS lead placement. For an accurate prediction of the effects of DBS, we implement a detailed spiking model of the basal ganglia, which we combine with TVB via our previously developed co-simulation environment. In the first demonstration of our model, we show that virtual DBS can move the basal ganglia firing rates of a Parkinson’s disease patient’s network towards the healthy regime. This study represents a proof of concept to perform virtual DBS in a co-simulation environment with TVB. The developed modeling approach has the potential to optimize DBS lead placement and configuration and forecast the success of DBS treatment for individual patients.

## Challenge 3: Personalized medicine: how to make models fit the patient<a name="ch3"></a>
	
### Christian Meisel<a name="Christian"></a>
### Title: Resilience in neural systems: from an understanding based on dynamical principles towards clinical diagnostics
In the recent years it has become apparent that dynamical system frameworks and bifurcation theory may apply to biomedical systems, beyond the systems classically considered in physics. Here, we will provide a critical survey of recent research in this field. We will discuss approaches building on dynamical systems theory to develop a better understanding of resilience and risk to rapid state changes, such as the onset of epileptic seizures, and how these theory-driven insights may provide clinical diagnostic markers.
	
### Vesna Vuksanovic<a name="Vesna"></a>
### Title: Data-driven approach to neuroimaging analysis to identify dementia subtypes

Understanding variations in neurodegeneration across brain disorders that cause dementia represents one of the main challenges in clinical neuroscience. Combining advanced neuroimaging with computational models in network neuroscience has already contributed to the understanding of biological bases of such variations. Here, I will present data on the analysis of the cortical networks, derived from magnetic resonance brain scans, to assess which organisational patterns of these networks are characteristics of dementia subtypes. Statistical methods of graph theory combined with hierarchical clustering was used to analyse topology of the cortical interactions across two types of dementia, frontotemporal dementia (its behavioural variant) and Alzheimer’s disease. The aim was to identify patients with more homogenous patterns of neurodegeneration.

	
### Peter Hitchcock<a name="Peter"></a>
### Title: On the Importance of Incorporating Time and Context in Computational Psychiatry Models
Why has computational psychiatry been slow to influence routine clinical practice? I will argue that one reason is the field has had difficulty recognizing the variability among mental health problems—and, consequently, the need to model context and temporal dynamics for many problems. I will propose three heuristics for deciding when modeling time and context is important. And as a case study of when such modeling is important, I will highlight contextual factors and temporal dynamics relevant to rumination and worry and thus to depression and anxiety disorders.

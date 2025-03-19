
<img src="https://cdn.prod.website-files.com/62d92550f6774db58d441cca/6324a2038936ecda71599a8b_OCF_Logo_black_trans.png" style="background-color:white;" />

Open Climate Fix (OCF) is a non-profit company, focused on building AI tools for a greener grid.
Every path to net zero has the electricity grid at its heart.
At Open Climate Fix, we're delivering cutting-edge technology for industry to accelerate the energy transition.

## How to get involved?
At OCF we are passionate that all the knowledge we produce remains open, to break down intellectual property barriers and subsequently reduce the “time to impact”. We therefore encourage external users to use our base code.

Here's how you can get involved:

### GitHub contributions

* Check out which [Github repositories](https://github.com/openclimatefix?view_as=public#overview-of-ocfs-repositories) are easy to contribute to in the section below using our (hopefully) helpful traffic light system 🚦;
* Have a look at our [list of "good first issues"](https://github.com/search?l=&p=1&q=user%3Aopenclimatefix+label%3A%22good+first+issue%22&ref=advsearch&type=Issues&utf8=%E2%9C%93&state=open) – these are GitHub Issues which do not require extensive familiarity with our code and should help get you started;
* We're also implementing a [contributions-welcome](https://github.com/search?q=user%3Aopenclimatefix+label%3A%22contributions-welcome%22&ref=advsearch&type=issues&utf8=%E2%9C%93&state=open) label to highlight issues we think are good for open source contribution. Note: this is a new tag, so not many issues use it yet! Feel free to ask to be assigned other issues, too, if something catches you eye, and we will be happy to clarify if it's community friendly.
* **Before you submit a pull request**, please ask to be assigned to the issue! Some issues are there for us to get back to and unfortunately might be completely inaccessible to OS contribution. Asking to be assigned first will prevent you from doing unnecessary work and lets everybody else know you're working on this already, so we don't get multiple PRs for the same issue;
* Once you're assigned to an issue, submit your PR and tag someone for a review! Our coding style is [here](https://github.com/openclimatefix/.github/blob/main/coding_style.md);
* First time contributing? Here's a [quick guide from firstcontributions](https://github.com/firstcontributions/first-contributions) to help you get started!
* Join our [GitHub Discussions](https://github.com/orgs/openclimatefix/discussions) to ask questions, share ideas, or engage with the community.
### Other ways to get involved
* Sign up to our [newsletter](https://ocfnews.substack.com/?utm_source=substack&utm_medium=web&utm_campaign=substack_profile) and follow us on [Bluesky](https://bsky.app/profile/openclimatefix.org) and [LinkedIn](https://www.linkedin.com/company/19123036/admin/) to learn the latest about our work;
* Use our datasets on [Hugging Face](https://huggingface.co/openclimatefix) or [EUMETSAT satellite data](https://console.cloud.google.com/marketplace/product/bigquery-public-data/eumetsat-seviri-rss?hl=en-GB&project=solar-pv-nowcasting) and let us know if it was useful;
* Use our ML models on [Hugging Face](https://huggingface.co/openclimatefix) and let us know if it was useful;
* Spread the word with your networks;
* Already contributed? Add OCF to the skills or volunteering section of your LinkedIn!
* Use our code(!) by following the guidelines below.
<details><summary><a>
  <h2>What if you use our code?</h2> <small>[ Click to expand ]</small>
</a></summary>

In order for us to understand the use of our models, and to demonstrate impact to future funders, it is invaluable for us to know who is using the code and, if possible, how.

We licence the code in this repository under a permissive MIT licence and if you are using the code or deriving from it, we request that you attribute the use of Open Climate Fix’s work in your product by adding the text below:

#### 'original code by [Open Climate Fix](https://github.com/openclimatefix)'

If you're a contributor, we'd love for you to share your work! We ask our community to refer to themselves as an Open Climate Fix Community Contributor, specifically across social media channels and on personal CVs or portfolios.

</details>

## How easy is it to get involved
We've set up this traffic light legend, so you can see how easy it is to get involved in each of our repositories.


| Level | Details|
|--- | ---- |
|[![ease of contribution: easy](https://img.shields.io/badge/ease%20of%20contribution:%20easy-32bd50)](https://github.com/openclimatefix#how-easy-is-it-to-get-involved) | These projects are easy to run, standalone, and have easily readable code. There should be issues for everyone at different skill levels.                         |
| [![ease of contribution: medium](https://img.shields.io/badge/ease%20of%20contribution:%20medium-f4900c)](https://github.com/openclimatefix#how-easy-is-it-to-get-involved)  | These projects are accessible to contributors but might depend on your skill level. They might depend on another bit of code or need you to investigate a little bit.
| [![ease of contribution: hard](https://img.shields.io/badge/ease%20of%20contribution:%20hard-bb2629)](https://github.com/openclimatefix#how-easy-is-it-to-get-involved) | We would not recommend going into these projects. They haven't been made "nice" and it might take a lot of digging in the code to understand what's going on.      |

You will usually see one of the corresponding badges on the repo's README.

## Overview of OCF's repositories

Click on the sections below to see the repo's.

<details><summary><a>Open Source Tools</a></summary>

| Repo                                                                                                     | Description                           | Main Developer                                     | Easy to contribute ? |
|----------------------------------------------------------------------------------------------------------|---------------------------------------|----------------------------------------------------| --- |
| [Open-Source-Quartz-Solar-Forecast](https://github.com/openclimatefix/Open-Source-Quartz-Solar-Forecast) | Open Source Solar Site Level Forecast | [Zak Watts](https://github.com/zakwatts) and [Peter Dudfield](https://github.com/peterdudfield)           | 🟢
| [NWP consumer](https://github.com/openclimatefix/nwp-consumer)                                           | Microservice for consuming NWP data.  | [Sol Cotton](https://github.com/devsjc) and [Peter Dudfield](https://github.com/peterdudfield)           | 🟢
| [Elexonpy](https://github.com/openclimatefix/elexonpy)                                                   | Python wrapper for UK Elexon data     | [Peter Dudfield](https://github.com/peterdudfield) | 🟢
| [open-data-pvnet](https://github.com/openclimatefix/open-data-pvnet)     | Solar Forecasting using PVNet on Open Data    | [Sukhil Patel](https://github.com/Sukh-P) and [Peter Dudfield](https://github.com/peterdudfield)| 🟢

</details>

<details><summary><a>Machine Learning</a></summary>

### Main repositories for our ML experiments

| Repo                                                                       | Description                                                                                                                                                                                                                                                                                                                              | Main Developer                                     | Easy to contribute? |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|---------------------|
| [ocf-data-sampler](https://github.com/openclimatefix/ocf-data-sampler)                   | Library for creating samples suitable for ML from weather and power datasets | [James Fulton](https://github.com/dfulu) and [Alex Udaltsova](https://github.com/AUdaltsova) | 🟢
| [PVnet](https://github.com/openclimatefix/pvnet)                           | PV net main repo | [James Fulton](https://github.com/dfulu), [Sukhil Patel](https://github.com/Sukh-P) and [Alex Udaltsova](https://github.com/AUdaltsova) | 🔴
| [PVNet-summation](https://github.com/openclimatefix/PVNet-summation)       | This project is used for training a model to sum the GSP predictions of PVNet into a national estimate     | [James Fulton](https://github.com/dfulu) and [Felix Peretz](https://github.com/felix-e-h-p) | 🔴                 |
| [pv-site-prediction](https://github.com/openclimatefix/pv-site-prediction) | ML experiments and models for SBRI project | [Zak Watts](https://github.com/zakwatts) and [Peter Dudfield](https://github.com/peterdudfield) | 🔴
| [UK PV National XG](https://github.com/openclimatefix/uk-pv-national-xg)   | National GSP PV forecasting using Gradient Boosted Methods.     | [Peter Dudfield](https://github.com/peterdudfield) and [Sukhil Patel](https://github.com/Sukh-P)  | 🔴                 |

### PyTorch implementations of ML models from the literature

| Repo                                                                         | Description  |    Main Developer      | Easy to contribute ? |
|------------------------------------------------------------------------------|------------------------|-------| --- |
| [Graph Weather](https://github.com/openclimatefix/graph_weather)         | PyTorch implementation of Ryan Keisler's 2022 "Forecasting Global Weather with Graph Neural Networks" paper (https://arxiv.org/abs/2202.07575) | [Jacob Bieker](https://github.com/jacobbieker) | 🟢
| [MetNet](https://github.com/openclimatefix/metnet)                           | PyTorch Implementation of Google Research's MetNet ([Sønderby et al. 2020](https://arxiv.org/abs/2003.12140)), inspired from Thomas Capelle's [metnet_pytorch](https://github.com/tcapelle/metnet_pytorch/tree/master/metnet_pytorch). | [Jacob Bieker](https://github.com/jacobbieker) | 🟢
| [Skillful Nowcasting](https://github.com/openclimatefix/skillful_nowcasting) | Implementation of DeepMind's Skillful Nowcasting GAN ([Ravuri et al. 2021](https://arxiv.org/abs/2104.00954)) in PyTorch Lightning. | [Jacob Bieker](https://github.com/jacobbieker) | 🟠
| [Perceiver Pytorch](https://github.com/openclimatefix/perceiver-pytorch)     | Implementation of DeepMind's Perceiver ([Jaegle et al. 2021](https://arxiv.org/abs/2103.03206)) and Perceiver IO ([Jaegle et al. 2021](https://arxiv.org/abs/2107.14795)) in Pytorch. Forked from [lucidrains/perceiver-pytorch](https://github.com/lucidrains/perceiver-pytorch) |[Jack Kelly](https://github.com/JackKelly) | 🔴

</details>

<details><summary><a>Operational Solar Forecasting</a></summary>

### General

| Repo                                                                               | Description  |    Main Developer      | Easy to contribute ? |
|------------------------------------------------------------------------------------|------------------------|-------| --- |
| [pv-site-datamodel](https://github.com/openclimatefix/pv-site-datamodel)           | Datamodel for PV sites | [Peter Dudfield](https://github.com/peterdudfield) and [Sol Cotton](https://github.com/devsjc) | 🟢
| [ocf-infrastructure](https://github.com/openclimatefix/ocf-infrastructure)                | Infrastructure code for OCF's cloud environments  | [Sol Cotton](https://github.com/devsjc) and [Peter Dudfield](https://github.com/peterdudfield) | 🟠
| [Satellite Consumer](https://github.com/openclimatefix/satellite-consumer)                                   | Consumer for Satellite data | [Sol Cotton](https://github.com/devsjc) and [Peter Dudfield](https://github.com/peterdudfield) | 🟠
| [analysis-dashboard ](https://github.com/openclimatefix/uk-analysis-dashboard )    | This is a Streamlit app for the OCF team that reports database statistics | [Peter Dudfield](https://github.com/peterdudfield) and [Aditya Sawant](https://github.com/ADIMANV) | 🔴
| [Nowcasting Alerts Cron](https://github.com/openclimatefix/nowcasting_alerts_cron) | Nowcasting Alerts cron Worker | [Brad Fulford](https://github.com/braddf) and [Sol Cotton](https://github.com/devsjc) | 🔴

## UK

| Repo                                                                              | Description  |    Main Developer      | Easy to contribute ? |
|-----------------------------------------------------------------------------------|------------------------|-------|  --- |
| [nowcasting_datamodel](https://github.com/openclimatefix/nowcasting_datamodel)    | Datamodel for the nowcasting project | [Peter Dudfield](https://github.com/peterdudfield) and [James Fulton](https://github.com/dfulu) | 🟢
| [GSPConsumer](https://github.com/openclimatefix/gspconsumer)                      | Collect GSP solar generation data from PVLive | [Peter Dudfield](https://github.com/peterdudfield) and [Sol Cotton](https://github.com/devsjc)  | 🟠
| [PVConsumer](https://github.com/openclimatefix/PVConsumer)                       | Consumer PV data from various sources | [Peter Dudfield](https://github.com/peterdudfield) | 🟠
| [PVoutput](https://github.com/openclimatefix/pvoutput)                            | Python code for downloading PV data from PVOutput.org | [Jack Kelly](https://github.com/JackKelly) | 🟠
| [pv-site-api](https://github.com/openclimatefix/pv-site-api)                      | Site specific API for SBRI project | [Peter Dudfield](https://github.com/peterdudfield) and [Brad Fulford](https://github.com/braddf)             | 🟠
| [pvnet_app](https://github.com/openclimatefix/pvnet_app)                          | Application for running PVNet in production | [James Fulton](https://github.com/dfulu) and [Peter Dudfield](https://github.com/peterdudfield) | 🟠
| [quartz-frontend](https://github.com/openclimatefix/quartz-frontend)              | Front End repo for the Nowcasting project. | [Brad Fulford](https://github.com/braddf) and [Peter Dudfield](https://github.com/peterdudfield) | 🟠
| [uk-pv-national-gsp-api](https://github.com/openclimatefix/uk-pv-national-gsp-api) | API for hosting nowcasting solar predictions | [Peter Dudfield](https://github.com/peterdudfield) and [Brad Fulford](https://github.com/braddf)| 🟠
| [pv-site-production](https://github.com/openclimatefix/pv-site-production)        | Production service for PV site level forecasts | [Peter Dudfield](https://github.com/peterdudfield) and [Zak Watts](https://github.com/zakwatts) | 🔴
| [uk-pv-forecast-blend](https://github.com/openclimatefix/uk-pv-forecast-blend) | Service to blend forecast together | [Peter Dudfield](https://github.com/peterdudfield) and [James Fulton](https://github.com/dfulu) | 🔴

## India

| Repo                                                                       | Description  |    Main Developer      | Easy to contribute ? |
|----------------------------------------------------------------------------|------------------------|-------| --- |
| [india-api](https://github.com/openclimatefix/india-api)                   | API India solar and wind data | [Sol Cotton](https://github.com/devsjc) and [Peter Dudfield](https://github.com/peterdudfield) | 🟢
| [india-forecast-app](https://github.com/openclimatefix/india-forecast-app) | Runs wind and PV forecasts for India and saves to database | [Sukhil Patel](https://github.com/Sukh-P) and [Peter Dudfield](https://github.com/peterdudfield) | 🔴

</details>

<details><summary><a>Other repos</a></summary>

| Repo                                                                     | Description                                                                                            | Main Developer                                 | Easy to contribute ? |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|------------------------------------------------| --- |
| [GFS Downloader](https://github.com/openclimatefix/gfs-downloader)       | NCEP GFS 0.25 Degree Global Forecast Grids Historical Archive: https://rda.ucar.edu/datasets/ds084.1/ | [Zak Watts](https://github.com/zakwatts) | 🟢
| [OCF Blocs2](https://github.com/openclimatefix/ocf_blosc2)               | Blosc2 codec used for OCF's Zarr compression | [Peter Dudfield](https://github.com/peterdudfield) | 🟢
| [Solar and Storage](https://github.com/openclimatefix/solar-and-storage) | Solar and Storage optimization code | [Peter Dudfield](https://github.com/peterdudfield) | 🟢
| [Status API](https://github.com/openclimatefix/quartz-status) | Status API for Quartz ecosystem | [Brad Fulford](https://github.com/braddf) and [Sol Cotton](https://github.com/devsjc) | 🟠
| [.github](https://github.com/openclimatefix/.github)                     | Various Community Health Files | [Peter Dudfield](https://github.com/peterdudfield) | 🔴


For a complete list of all of OCF's repositories tagged with "nowcasting", see [this link](https://github.com/search?l=&o=desc&q=topic%3Anowcasting+org%3Aopenclimatefix&s=updated&type=Repositories)

</details>


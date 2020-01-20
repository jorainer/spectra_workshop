# RforMassSpectrometry/Spectra workshop

*Presenter*: Johannes Rainer, Institute for Biomedicine, Eurac Research,
Bolzano, Italy.

This repository contains all files and data for my part of the [metaRbolomics
hackathon plus](https://rfmf-mpf-2020.sciencesconf.org/resource/page/id/32)
workshop of the [European RFMF Metabomeeting
2020](https://rfmf-mpf-2020.sciencesconf.org/) in Toulouse.

The workshop provides background information on the new mass spectrometry
infrastructure which is being developed as part of the
[RforMassSpectrometry](https://www.rformassspectrometry.org) initiative and
shows its usage on the example of matching an experimental MS2 spectrum against
a MS2 library. We will thus in particular focus on the functionality of the
[Spectra](https://github.com/RforMassSpectrometry/Spectra) R package.

The workshop consists of two parts:

- static presentation:
  [spectra_workshop_static.Rmd](spectra_workshop_static.Rmd), [html
  view](https://jorainer.github.io/spectra_workshop/spectra_workshop_static.html).
  
- interactive presentation:
  [spectra_workshop_interactive.org](spectra_workshop_interactive.org) (Emacs
  org-mode file); *Rmd* version:
  [spectra_workshop_interactive.Rmd](spectra_workshop_interactive.Rmd).


## Main topics

- What is [RforMassSpectrometry](https://www.rformassspectrometry.org/)?
- What is available as of now? (`MsCoreUtils`, `Spectra`)
- Flexible infrastructure: use different backends to load, represent, store
  data.
- Use case: match measured MS2 spectrum against database.
- Missing pieces:
  - plotting functionality
  - backends to import/work with MGF data, MassBank, ...
  - other things we haven't thought of?
- How can **you** contribute?

## Installation instructions

To run the examples above a recent version of R is required (>= 3.6.1) and a set
of packages, which can be installed with the commands below.

```r
install.packages("BiocManager")
BiocManager::install(c("remotes", "magrittr", "rmarkdown"))
BiocManager::install("RforMassSpectrometry/Spectra")
BiocManager::install("RforMassSpectrometry/MsBackendHmdb")
BiocManager::install(c("mzR", "BiocStyle"))
```

and use `git clone https://github.com/jorainer/spectra_workshop` to clone the
repository to your computer.

Note: on Windows you might have to use `type = "source"` in the installation
calls above to force installation of packages from source instead of using the
pre-built packages.

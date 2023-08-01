# Artifact Appendix

Papertitle: **Enter the title of your paper here**

Artifacts HotCRP Id: **#Enter your HotCRP Id here**

Requested Badge: Either **Available** or **Reproducible**


**Disclaimer:** *This template is strongly influence by the PDF of the USENIX artifacts evaluation process.*

## Description
A short description of your artifact and how it links to your paper.

### Security, Privacy, and Ethical Concers
Describe any risk for reviews while executing your artifact.
Risks might be to their machine's security, data privacy or others ethical concerns.
This is particularly important if destructive steps are taken or security mechanisms are disabled during the execution.

## Basic Requirements
In this section describe the minimal hardware and software requirements of your artifacts and estimate the compute-time and the storage, that is required to run the artifacts.

### Hardware Dependencies
Specify the required hardware (vendor, CPU/GPU/FPGA, number of processors/cores, microarchitecture, interconnect, memory, hardware counters, ...).
In case, your artifact requires special hardware provide instructions on how to gain access to the hardware.
For example, provide private SSH keys to access the machines remotely.
Please keep in mind that the anonymity of the reviewers needs to be maintained, and you may not collect or request personally identifying information (e.g., email, name, address).

### Software Dependencies
Describe the required OS and software packages to evaluate your artifact.
This is particularly important if you rely on some proprietary software that you cannot include in your package.
You must describe how to obtain and to install all third-party software, data sets, and models.

### Estimated Time and Storage Consumption
Provide an estimated value for the time the evaluation will take and the space on disk it will consume. 
This helps reviewers to schedule the evaluation in their time plan and to see if everything is running as intended.
More specifically, a reviewer, who knows that the evaluation might take 10 hours, does not expect an error, if,  after 1 hour, the computer is still calculating things.

## Environment
In the following, describe how to access our artifact and all related and necessary data and software components.
Afterwards, describe how to set up everything and how to verify that everything is set up correctly.

### Accessability
Describe how to access your artifacts via persistent sources.
Valid hosting options are institutional and third-party digital repositories.
Similar to USENIX we recommend Zenodo, FigShare, Dryad, Software Heritage, GitHub, or GitLab.
Do not use personal webpages.
For repositories that envolve over time (e.g. Git Repositories ) specify a specific commit-id or tag to be evaluated.
In case your repository changes during the evaluation to address the reviewer's feedback, update the commit-id or tag in this very document.


### Set up the Environment
Describe how the reviews should set up the environment for your artifacts, including download and install dependencies and the installation of the artifact it self.
Be as specific as possible here.
If possible use code segment to simply the work flow, e.g.,

```bash
git clone git@my_awesome_artifact.com/repo
apt install libxxx xxx
```

Describe the expected results, where it makes sense to do so.



### Testing the Environment
Describe the basic functionality tests to check if the environment is set up correctly.
This could be unit tests, training a ML model on a very low training data, and so forth.
If these tests succeed, all required software should be functioning correctly.
Include the expected output for unambiguous outputs of tests.
Use code segment so simplify the workflow, e.g.,
```bash
python envtest.py
```

## Evaluation Workflow
This section should include all the operational steps and experiments which must be performed to evaluate if your artifact is functional and to validate your paper’s key results and claims.
For that purpose, we ask you to use the two following subsections and cross-reference the items therein as explained next.

### Major Claims
Enumerate here the major claims (Cx) made in your paper.
Follows an example:

#### (C1): *[Optional Name]*
System_name achieves the same accuracy of the state-of-the-art systems for a task X while saving 2x storage resources.
This is proven by the experiment (E1) described in [refer to your paper’s sections] whose results are illustrated/reported in [refer to your paper’s plots, tables, sections or the sort].

#### (C2): *[Optional Name]*
System_name has been used to uncover new bugs in the Y software.
This is proven by the experiments (E2)
and (E3) in [ibid].

### Experiments
Link explicitly the description of your experiments to the items you have provided in the previous subsection about Major Claims.
Please provide your estimates of human- and compute-time for each of the listed experiments (using the suggested hardware/software
configuration above). Follows an example:

#### (E1): *[Optional Name]* *[30 human-minutes + 1 compute hour + 5GB disk]*
Provide a short explanation of the experiment and expected results.
Describe thoroughly the steps to perform the experiment and to collect and organize the results as expected from your paper.
Use code segments to support the reviewers, e.g.,
```bash
python experiment_e1.py
```
We encourage you to use the following structure with three main blocks for the description of your experiment.

**Preparation:** Describe in this block the steps required to prepare and configure the environment for this experiment.

**Execution:** Describe in this block the steps to run this experiment.
 
**Results:** Describe in this block the steps required to collect and interpret the results for this experiment.

#### (E2): *[Optional Name]* *[1 human-hour + 3 compute-hour]*
...

#### (E3): *[Optional Name]* *[1 human-hour + 3 compute-hour]*
...

In all of the above blocks, please provide indications about
the expected outcome for each of the steps (given the sug-
gested hardware/software configuration above).

## Limitations
Describe which specific tables and results are not reproducible with the provided artifacts.
If possible, provide an argument why this is not include/possible.

## Notes on Reusability
First, this section might not be applicable your artifacts.
You can use it to share information on how your artifact can be used beyond your research paper. 
This especially applies to general frameworks.
The overall goal of artifact evaluation is indeed not only to reproduce and verify your research but as well to help other research to re-use and improve on your artifacts.
Please describe how your artifacts can be adapted to other setting, e.g., more input dimensions, other datasets, customizing its behavior through replacing individual modules and functionality, or running more iterations of a specific part.

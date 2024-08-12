# PoPETs Artifact Review

PoPETs reviews and publishes digital artifacts related to its accepted papers. This process aids in the reproducibility of results and allows others to build on the work described in the paper. Artifact submissions are requested from authors of all accepted papers, and although they are optional, we strongly encourage you to submit your artifacts for review.

Possible artifacts include (but are not limited to):

 - Source code (e.g., system implementations, proof of concepts)
- Datasets (e.g., network traces, raw study data)
- Scripts for data processing or simulations
- Machine-generated proofs
- Formal specifications
- Build environments (e.g., VMs, Docker containers, configuration scripts)

Artifacts are evaluated by the artifact review committee. The committee evaluates the artifacts to ensure that they provide an acceptable level of utility, and feedback is given to the authors. Issues considered include software bugs, readability of documentation, appropriate licensing, and the reproducability of the results presented in the paper. After your artifact has been approved by the committee, we will accompany the paper link on petsymposium.org with a link to the artifact along with an artifact badge so that interested readers can find and use your hard work.

## Artifact Submission Guidelines

- All submitted artifacts should be relevant to their corresponding PoPETs paper. Please upload a copy of your paper.
- Many papers have several artifacts (e.g., multiple source code repositories, datasets, build environments), which is great! Please keep in mind that we'll need a single link to put on the PETS website and that all artifacts associated with your paper should be discoverable from that link.
- All submitted artifacts should be submitted by providing a link to where the artifacts are publicly hosted. Valid hosting options are institutional and third-party digital repositories. Please do not use personal web pages. The link should be persistent; for repositories that evolve over time (e.g., Git repositories), please specify a specific commit-id or tag to be evaluated.
- Please include a `README.md` file with your submission that briefly explains the type and purpose of the artifact. At a prominent position in the `README.md` file make clear to which paper the artifact belongs and how the artifact is relevant to the paper.
- All artifacts must be immediately available to the public and should not be behind any kind of paywall or restricted access. If the artifact requires you as an author to manually approve requests for access, it is not public and will not qualify as a PoPETs artifact submission. If you have concerns or questions about this please contact us directly.

### Source Code Submissions

- All source code should be accompanied by a `README.md` file or other documentation that describes how to build and/or run the code. Reviewers will provide feedback on the clarity of the instructions and attempt to follow them and build and/or run the code.
- Any source code submissions should be accompanied with a build environment such as a virtual machine or a Docker container that has been configured with all the dependencies and prerequisites necessary to build the code. If you use a virtual machine, please state how many resources it will consume and any configuration steps that are required. Your virtual machine should not usually have to download additional dependencies when you run your install scripts. If that is the case, reassess your build process and consider making changes to limit the amount of network resources needed. You can also use one of the VM images provided by us, which you can spawn from within HotCRP. In this case please provide the name of the used image. If your artifacts run on compute providers like AWS, or similiar, state the amount of money required to run the experiments and provide a account credentials with enough coins. Our reviewers won't invest their money or credit card to setup accounts. If this cannot be provided, provide a way of running your artifact on a local machine or the provided VMs. I neither is possible, consider choosen an other badge, see below.
- If the code is in a compiled language, the code should compile in the provided build environment by performing the provided instructions.
- Compilation and setup should be automated as much as possible. Ideally, there will be one script that builds your software, runs your tests, and produces the results in a comprehensible way.
- Please ensure your code has an open source license and clearly states this information. The following resources may help you to choose a license:
    - For a clear, easy to follow guide see: https://choosealicense.com/
    - For more in-depth detail on open source and copy-left licenses, see https://www.gnu.org/licenses/license-list.en.html and https://opensource.org/licenses
- Our goal is that the artifacts are useful as far into the future as possible. Some tips on improving the longevity of your source code artifact are:
    - Include the versions of your software's dependencies wherever possible
    - Mention specific hashes of git commits that match the state your artifact was in at the time of submission
    - Virtual machines will last longer than Docker files and allow researchers to more accurately reproduce your exact execution environment (though the tradeoff is that they will be larger)
    - Artifacts are not required to be able to run on all hardwares and OSes. If your artifact requires any particular hardware / OS, please make it clear in the submission.

### Dataset Submissions

- All datasets should be clearly documented in a way that allows researchers working on similar problems to re-use the dataset for their work.
- If the dataset includes survey results, please provide a copy of the original survey with raw results. This is vital for replication studies and helping researchers interpret the context of your results.
- If the dataset is very large (> 10 MB) please state so in the `README.md` or documentation.
- It's encouraged to accompany the data with processing scripts that produce any graphs or statistical output that appear in the paper.
 
## Artifact Badges

Each accepted artifact will be granted one of three badges. During the submission, the authors must select which badge they want their artifacts to be evaluated against. We encourage the authors to choose a appropriate badge, to ease the reviewing effort.

### Artifacts Available
This "Artifacts Available" badge indicates that the artifacts are publicly available at a permanent location with clear documentation on how it relates to the corresponding paper and, if applicable, how to execute/use the artifact. This badge does *not* mean that the reviewers have reproduced the results or checked the code for full functionality. The reviewer may however take some effort to check the relevance for the paper, and the presentation of the artifact.

### Artifacts Functional
First of all, the "Artifacts Functional" badges includes everything the "Available" badge does. In the following, we think of your experiments as been arranged in pipelines of multiple stages. The "Artifacts Functional" requires that each stage of your core experiments is represented. For the functional badge, individual stages can run in a simplified version to demonstrate that the submitted artifact in principle can generate the results presented in the paper. In some cases individual stages might be impossible to repeat (even in a simplified version). In such cases we expect a (potentional) simplified result to be given, which can be used to run the later stages of the pipeline. Because of the involved simplification, we do not expect the results to be reproduced exactly. For the "Artifacts Functional" badge your artifacts need to suggest that they can reproduce the results presented in your paper, if run in ``full'' mode instead being simplified. Every simplified stage must be mentioned clearly in the artifact. In the following we provide some examples for the "Artifacts Functional" badge: 

#### Examples
**Tools based on big machine learning models.** If a machine learning model is required to execute the presented tool, the authors should provide it unless they have a good reason not to do so (e.g., the model is incredibly big or proprietary). If they can't share the full model, we'd expect them to share some dummy model (perhaps with worse performance but a more manageable size), which can be used to test the principle functionality of the presented tool. Ideally the code to train the original model is provided (but not executed).

**Extensive computing requirements.** Similiarly to the point above; If your experiment has high computational requirements (days or weeks of compute time), please select the "Artifacts Functional" badge and (if possible) provide a simplified version of the experiment (less bits, less training data, less epochs,...) to enable the reviewers to check the functionality of that stage. Provide the results of the full experiment in addition, so that reviewers can check the later stages with the real results.

**User studies/crawling studies.** Ofcause extensive user studies and crawling studies cannot be repeated within the reviewing process. But the (anonymized/pseudonymized) raw data should be provided, incl. the evaluation scripts. However, we allow for exceptions for this point if a publication of raw data is not possible because of legal requirements, privacy, or ethical concerns, e.g., if a the data cannot be pseudonymized properly. In such cases a data set with dummy data can be used to test the functionality of the remaining stages.

**Special physical setups.** If your paper requires a special physical setup, provide (if possible) a way of simulating it (e.g., VMs) or at less the raw results of the experiments, so that reviewers can verify the remaining steps been functional. 

### Artifacts Reproduced
The "Artifacts Reproduced" badge includes everything the "Artifacts Functional" does, plus all the main contributions can actually be reproduced by the authors. Authors must specify the commands to run the artifacts clearly and describe how to reproduce each main finding of the paper. Best practice is to point out which part of the paper is reproduced by a given script, e.g., name th e table or figure. Also, the authors must highlight which results of the paper are not reproducible with the given artifacts and why. Note that minor additional experiment that do not contribute to much to the paper must not be included in the artifact. The artifact's quality, structure, and documentation must allow the reviewers to check whether the artifact works as claimed in the paper.

Even if the authors choose this option, the review committee may request to grant only an "Artifacts Functional" or "Artifacts Available" badge if the reviewers cannot reproduce the results (e.g., lack of computational resources, differing results, ...)


# What makes a Good Submission

To ensure a smooth submission process, please follow these important guidelines.
Firstly, authors should fill out the `template.md` file provided and include it in their artifacts.
Mention the badeg you deem reasonable for your artifact and, if neccessary, describe which stages are simplified or skipped and why.
This will help the reviewer better understand your work and ensure a seamless review process.
Secondly, prompt communication is essential.
Authors are kindly requested to respond to reviews and comments within a time span of two weeks.
This will facilitate constructive discussions and allow for timely feedback incorporation.
Lastly, in the event that changes are requested during the review process, we kindly ask authors to endeavor to incorporate them, at least partially, within two weeks after the request.
Your cooperation in adhering to these guidelines will greatly contribute to the efficiency and effectiveness of our submission and review process.
We eagerly anticipate receiving your high-quality contributions and look forward to showcasing your research!

# What Makes a Good Review

The goal of artifact review is to help ensure the artifacts are as useful as possible. Towards this goal, the review should check for the following points.
- Is the artifact publicly available at a permanent location?
- Documentations:
  - Is the relationship between the artifact and the paper clear?
  - If applicable, is the requirement for running the artifact clear?
  - If applicable, are the instructions to run the artifact sufficient?
  - If applicable, are the required dataset & packages publicly available?
- Reproducibility: In case that the authors choose "Artifact Reproduced" badge option, the reviewers should also check that the experiments run and the results displayed are similar to the ones in the paper.

Artifact review process is interactive and we expect the authors to take into account the reviewers' comments and modify their artifacts accordingly. As such, the reviews should contain sufficient details for the authors to make the appropriate changes; for example, if the code fails, then the review should include the environment that it is run on and the error messages. After the authors have fixed the issues, they will add a comment on the submission site, at which point the reviewers can either approve the artifact or provide additional comments for another rounds of revision.

# Volunteer for the Artifact Review Committee

We are looking for volunteers to serve on the artifact review committee. As a committee member, you will perform review of artifacts according to the guidelines above. We are looking for volunteers who will be interested in providing feedback on documentation and instructions, trying to get source code to build, or have experience with re-using published datasets. Please email artifact25@petsymposium.org to be on the review committee.
# Starting a new year for artifact review

Each August, just as PoPETs starts a new review cycle, we also start a new review cycle for artifact review. There are a few things that need to be done to set things up.

## Inviting artifact committee members

We need to make sure the artifact committee PC is ready to go by the first round deadline. I usually send an invitation email with some stats from the previous year and some changes for the upcoming year. This email is sent to the existing artifact committee as well as any new potential committee members. There is an option to sign up or nominate people to be on the artifact committee in the "Reviewer Nomination Form". If you have not gotten the list of artifact reviewers from the current chairs, you can try reaching out to them. We've gotten a large list of reviewers this way.

Once an artifact reviewer has replied to the invitation email, add them to the HotCRP instance. (See below.) You should also email the publicity chairs to update the list of committee members.

# Starting a new round of artifact reviews

## Creating a new HotCRP instance

We now use separate instances for different rounds. You'll need to email the PoPETs HotCRP admin to create a new instance. The URL for the artifact submission site has been https://artifact.petsymposium.org/artifactYYYY.R where YYYY is the 4 digits of the upcoming year and R is the round number. As an example, in November of 2023 we are now setting up the instance for the 2022 round 1 submission year and so the submission site is https://artifact.petsymposium.org/artifact2024.2.

The current HotCRP admin is Ian Goldberg. For up to date information, check for the "Infrastructure Chairs" on this year's CFP.

If this is the first round, you will have to add the email addresses of the reviewers that accepted the invitations directly. If this is not the first round, then HotCRP admin can run a script to copy over the email list from the previous round.

## Configuring the HotCRP instance

There is not much configuration necessary to accept submissions. Make sure you open submissions for the first round and set the submission deadline if desired. In the settings menu, select the "Submission Form" setting. Make sure both an abstract and PDF are required. Add a new submission field titled "Artifact link and brief description" of type "multiline text". Set the topics so reviewers can indicate preferences. So far we've used "source code", "data sets", and "other" but feel free to experiment :)

We recently added an indicator for specialized hardware, this helps for identifying artifacts that we may need to reach out to external reviewers for. 

Make sure you select "Save changes" before leaving the screen.

You will also want to ensure the review form has been configured to the preferred information. (e.g. artifact readiness, artifact award worthiness)

Text Input, label: Artifact Summary
Text Input, label: Comments to authors
Artifact Readiness
1. Not suitable for review
2. Needs work
3. Ready

Award Worthiness (Configure as not visible to authors)
1. Not suitable
2. Perhaps suitable
3. Definitely consider
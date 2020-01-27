# Taxonomy of Real Faults in Deep Learning Systems

The link to our replication package is
https://github.com/dlfaults/taxonomy/tree/master/replication

Our replication package consists of three main folders: Manual_Labelling, Interviews and Survey.

### Manual_Labelling

In this folder we have placed all the files associated with our manual labelling process. It is divided in 3 subfolders: SO_init, GitHub_init and Analysed_Artifacts.

##### GitHub_init

The GitHub mining process is explained in detail in Section 3.1.1 of the paper. The list of initially mined GitHub projects for each framework is presented  in the file {frameworkname}_init.csv. Each line in the file provides project name, the link to the project and its general information such as number of commits, issues, stars and etc. As part of our procedure, we removed projects that do not represent real software systems. For such projects we provide an explanation on why it should be excluded in the column "Comment". The files {frameworkname}_after_init_removal.csv present the list of remaining projects after the exclusion of such systems. The files {frameworkname}_top_100.csv list the top 100 projects we selected for our final analysis.

As explained in Section 3.1.1, to identify relevant commits and issues we used a vocabulary of related terms. The complete list of 11,968 stemmed words is presented in the file vocabulary_init.csv. The final list of 105 relevant words obtained by the exclusion of the words that appear less than 10 times and the further manual analysis is provided in the file vocabulary_final.csv.

##### SO_init 

The extraction procedure from StackOverflow is explained in detail in Section 3.1.2 of the paper. In the file query.rtf we provide the code of the query we have used to extract discussions related to each of the analysed frameworks (Keras, Torch, Tensorflow) from StackOverflow. As a result, we got a csv file that lists discussions for each of the frameworks (files keras.csv, torch.csv and tensorflow.csv).
 
##### Analysed_Artifacts

Our manual analysis was conducted in 6 rounds (Table 1 in the paper). We provide information about each round in a separate csv file round_{roundnumber}.csv. In each file we provide the following information: (1) **Entity Type** - whether it is a StackOverflow or GitHub artifact and which framework it corresponds to; (2) **Link** to the artifact; (3) **Number of Evaluators** - how many evaluators were assigned to this artifact; (4) **Conflict** - whether there was a conflict between evaluators when assigning tag to this artifact, has a value 0 for no and 1 for yes; (5) **Evaluator1..4** and **Tag1..4** - the ID of each evaluator and the tag provided by each of the assigned evaluators; (6) **Final Tag** - final tag assigned to the artifact; (7) **Taxonomy Tag** - the tag in the final taxonomy; 

The detailed information on the statistics of each round can be found in file stats.xlsx.

### Interviews

The background information about our interview participants is presented in the file interview_participant_info.xlsx. The interview guide we used to conduct the semi-structured interviews is in the file interview_guide.docx. In the subfolder "Transcriptions" we provide transcribed versions of all 20 interviews. 

We provide the details of open coding process for the interviews in the file interview_open_coding.xlsx. Each row corresponds to a part of the interview text to which at least one of the evaluators has assigned a tag. Therefore, each row contains the following information: (1) **Interview Num** - the interview number;	(2) **Evaluator 1** - tag provided by the first evaluator; (3) **Evaluator 2** - tag provided by the second evaluator;	(4) **Moderator Tag** - tag assigned by the moderator; (5) **Tag** - the final taxonomy tag; (6) **Status** - whether this tag has been added to the final taxonomy or not ("A" for yes and "R" for no). 

In the file Interview_Tags.xlsx we provide aggregated information about the tags obtained from interviews. The column "Number" shows the number of times the tag was extracted from the interviews. Similarly to the previous file, the column "Status" shows whether the tag became part of the final taxonomy or not.

### Survey

We provide the survey form we have used for our validation study in the file survey_form.pdf. The file with the information about participants and their answers to the survey questions are in the file participant_info_and_responses.xlsx. The percentages reported in Table 2 in the paper are calculated in this file (last rows with a bold font). 


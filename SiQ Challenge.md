Tags:: #research #projects 
Doc:: [Doc](https://docs.google.com/document/d/1FanPUUK2jmwestyGUM7YphKqHwsIoYsU_ApiWe7eanQ/edit?usp=share_link)

## Tasks
Baselines & Code
- [ ] #sheryl get MERLOT features, modify code to work with processed features 📅 2023-01-26
- [ ] #sheryl run MERLOT on SiQ 1.0, 2.0, and BMW. Clean up all into common data format 📅 2023-01-19
- [ ] #sheryl #leena get non-MERLOT baselines running & with processed features 📅 2023-01-26 
- [ ] #sheryl #leena #alex create Social-SDK: write up documentation for running baselines given data 📅

Debiasing
- [ ] #claire get baselines running on SiQ 1.0: RoBERTA, MERLOT w/ and w/o adversarial matching 📅 2023-01-16
- [ ] #claire build annotator interface, run MTurk to get new labels 📅 2023-01-23
- [ ] #claire get perf across all 4 metrics (MTurk for human labels between the three diff versions) 📅 2023-01-25

Writing
- [ ] #alex write workshop proposal outline 📅 2023-01-23
- [ ] #alex #leena write workshop proposal draft 📅 2023-01-26 
- [ ] #alex edit workshop proposal  📅 2023-02-02
- [ ] #alex submit workshop proposal 📅 2023-02-10

Other
- [ ] #alex #leena invite speakers 📅 2023-01-16 
- [ ] #alex make website draft 📅 2023-01-26
- [ ] #alex edit website 📅 2023-02-10 

## Project Vision

![[Pasted image 20230111113910.png]]

![[Pasted image 20230111113923.png]]

![[Pasted image 20230111113934.png]]
![[Pasted image 20230111113949.png]]

## Cal

```dataviewjs
await dv.view("tasksCalendar", {
pages: "dv.pages().file.where(f=>f.name.includes('SiQ')).tasks",
view: "month", firstDayOfWeek: "1", options: "style1" })
```

## Week 1: to Jan 19


```tasks
path includes SiQ Challenge
tags includes #sutton
due before Jan 21
```

### sheryl


### claire
```tasks
not done
path includes SiQ Challenge
tags includes #claire
short mode
```

### leena
```tasks
not done
path includes SiQ Challenge
tags includes #leena
short mode
due before Jan 21
```

### alex
```tasks
not done
path includes SiQ Challenge
tags includes #alex
short mode
due before Jan 21
```



## LP Meeting Notes

baselines
    multimodal
        transformer
        old style: takes features
    unimodal
        text
        video
        audio

features
    openface
    word alignment

evaluation
    teams disclose the external data you use
    in our presentation: disclose subgroups

timeline
    march 27: notification of acceptance
    end of june: when submissions are due for our workshop
    3 weeks for us to review (we may extend)
    august 13: (camera ready for proceedings)

follow up with LP re: intel money for workshop march 30

no matter what
    program committee
    evaluation

start an initial list of program committee

spotlight talks (10 mins) + posters: people submit as many as they want


Organizing
- LP will chat with Evonne. If she's open to co-leading and the other conditions we talked about, we'll merge with her ASI workshop.
- The above will influence our speaker invitations.

Proposal
- We'll write a proposal now as if we will not be merging. Leena and I will write a draft and send by Friday.

Debiasing
- We'll start off by getting a "gold rematching". For each question and correct answer, we'll trim down the set of candidate incorrect answers to the top K that confuse the text-only model the most. Then, given the video, question, correct answer, and this set of candidates, a human will output which element in the set should be the incorrect answer, or whether none are valid.
- In parallel, we'll be implementing strategy 1: adversarially matching automatically using the method from VCR and strategy 2: matching correct answers in the way described above except without the video, so it's much faster. We'll have two metrics for evaluating each strategy: (1) How close to random the text model does, and (2) How well each strategy recovers the gold labels
- Our goal is to verify that one of the two strategies works by Feb 10, so we know there's a good path before we hear about acceptance




## other / template

### Week 1
#### Last Week (Stand-Up)
- 
#### Paper Story / Structure
- 
#### This Week
- 
#### Backlog
- 
### Stand-Up
- person i
	1. (What you worked on)
	2. (What progress you made)
	3. (Any blockers)

### Week i-1
...

social-IQ 2, challenge, baseline debiasing
    goal
        ICCV deadline (when??)

    motivation
        want to clean up and get the social-iq data ready and accepted for a grand challenge which we'll hold in october to stimulate interest from the field
        want to put out the social-iq 2.0 paper + adversarial debiasing

    approach
        get workshop speakers: start Jan 10
            [alex]
            [leena]
        
        clean up all SiQ splits into common data format
            [sheryl]
        
        run all baselines on all datasets: by Jan 20
            [sheryl]
            [leena]
            non-PT
                LSTM
                F2F
            PT
                MERLOT
                UNITER
                data2vec
                gopher

        get adversarial matching working with RoBERTA + one of the models: Jan 20
            [claire]

        process features, go back and get models working from features alone: Jan 27
            [sheryl]
            [leena]

        get adversarial filtering working with RoBERTA + one of the models: Jan 27
            [claire]

        create website: Jan 27
            [alex]

        create common format for datasets & challenge, figure out how to get it up online. unify code for feature baselines: Feb 3

        write challenge proposal: Feb 10
            [alex]
            [leena]

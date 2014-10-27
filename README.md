# Name

Adrian Chen

# How many points have you earned?

100/100

(Make your own calculation and replace the number 0 with the points you think you've earned.)

# How many hours have you spent on this?

6

# When did you first start working on this week's learning challenges?

Friday

# What is the most difficult part about this week's challenge?

None of it was that bad, I just googled a lot on the mongoDB segment.

# Show and tell (8 points)

## Link (2 points)

[How Lumiata wants to scale medicine with machine learning and APIs](https://gigaom.com/2014/01/08/lumiata-does-graph-analysis-for-medical-data-raises-4m-from-khosla/)

## Discuss how you may apply the machine learning technique mentioned in this article to another interesting problem (6 points).

The idea that medicine isn't treated with intuition and decidal decisions are logically made means there is a growing field in this area for machines to diagnose common illnesses. The rate at which doctors misdiagnose illness is frightening, and just like with driving, machines don't have to be perfect, they just have to be better than people. Business desicions are usually logical descisions, and though they will have many more input variables, I thnk there is a future for machines to make well informed buisiness decisions.

# D3 IV

## Checkpoints (3 points x 4 = 12 points)

# 1. (3 points)

![image](d3/screenshots/CP1.png?raw=true)

[checkpoint](d3/src/checkpoint1.html)

# 2. (3 points)

![image](d3/screenshots/CP2.png?raw=true)

[checkpoint](d3/src/checkpoint2.html)

# 3. (3 points)

![image](d3/screenshots/CP3.png?raw=true)

[checkpoint](d3/src/checkpoint3.html)

# 4. (3 points)

![image](d3/screenshots/CP4.png?raw=true)

[checkpoint](d3/src/checkpoint4.html)

## Challenges (4 points x 3 = 12 points)

# 1. (4 points)

![image](d3/screenshots/CH1.png?raw=true)

# 2. (4 points)

![image](d3/screenshots/CH2.png?raw=true)

# 3. (4 points)

![image](d3/screenshots/CH3.png?raw=true)

[challenge3](d3//srcchallenge3.html)



# MongoDB II

## Checkpoints (6 points x 2 = 12 points)

### 1 (6 points)

[mongodb js code collecting github events about our course](mongoDB/src/mongodb4.js)

### 2 (6 points)

![terminal output of mongodb query](mongoDB/screenshots/CP2.png?raw=true)

## Challenge 1 (4 points x 10 = 40 points)

### 1 (4 points)

> db.course_events.findOne({"actor.login": "doubleshow"})

![screenshot](mongoDB/screenshots/CH1.png?raw=true)

### 2 (4 points)

> db.course_events.findOne({"actor.login": "doubleshow"}, {"actor": 1})

![screenshot](mongoDB/screenshots/CH2.png?raw=true)

### 3 (4 points)

> db.course_events.find({ "actor.login" : {$in : ["doubleshow", "chrisbopp"]}},{"created_at":1})

![screenshot](mongoDB/screenshots/CH3.png?raw=true)

### 4 (4 points)

> db.course_events.findOne({'type':'PushEvent'})

![screenshot](mongoDB/screenshots/CH4.png?raw=true)

### 5 (4 points)

> db.course_events.find({'type':'PushEvent'},{'payload.commits.author.name':1})

![screenshot](mongoDB/screenshots/CH5.png?raw=true)

### 6 (4 points)

> db.course_events.findOne({"type": "IssuesEvent"},{"payload":1})

![screenshot](mongoDB/screenshots/CH6.png?raw=true)

### 7 (4 points)

> db.course_events.find({"type": "IssuesEvent"},{"payload.issue.user.login":1});

![screenshot](mongoDB/screenshots/CH7.png?raw=true)

### 8 (4 points)

> db.course_events.find({"type": "IssuesEvent","payload.issue.state":"closed"},{"payload.issue.user.login":1,"payload.issue.state":1});

![screenshot](mongoDB/screenshots/CH8.png?raw=true)

### 9 (4 points)

> db.course_events.find({"type": "IssuesEvent","payload.issue.state":"open"},{"payload.issue.user.login":1,"payload.issue.state":1});

![screenshot](mongoDB/screenshots/CH9.png?raw=true)

### 10 (4 points)

> db.course_events.find({"type": "IssuesEvent","payload.issue.comments":{$gt:0}},{"payload.issue.user.login":1,"payload.issue.comments":1});

![screenshot](mongoDB/screenshots/CH10.png?raw=true)


## Challenge 2 (8 points x 2 = 16 points) 

### 1 (8 points)

What are the open issues about?

> db.course_events.find({"type": "IssuesEvent","payload.issue.state":"open"},{"payload.issue.body":1});

![screenshot](mongoDB/screenshots/CH11.png?raw=true)

### 2 (8 points)

How many site admins are active on our repo?

> db.course_events.find({"payload.issue.user.site_admin": true}).count()
> db.course_events.find({"payload.issue.user.site_admin": false}).count()

![screenshot](mongoDB/screenshots/CH12.png?raw=true)

## Основная часть

1. Создайте новый проект в teamcity на основе fork.
2. Сделайте autodetect конфигурации.

![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/b4715f73-7170-44de-9c59-8b516cb29bf3)

3. Сохраните необходимые шаги, запустите первую сборку master.

![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/9f3f035a-87f8-4cbf-b3d9-43c8a53d5ac0)

<details><summary>Logs</summary>
  
```
 
Build 'netology / Build' #1, default branch 'master'
Triggered 2023-09-27 08:02:40 by 'Git'
Started 2023-09-27 08:02:42 on agent 'ip_130.193.37.216'
Finished 2023-09-27 08:03:14 with status NORMAL 'Tests passed: 5'
VCS revisions: 'Netology_HttpsGithubComSemenAmbarnovExampleTeamcityGitRefsHeadsMaster' (Git, instance id 1): '817aad0ca811ebb403effd538c0a52542a6414c8' (branch: 'refs/heads/master')
TeamCity URL http://localhost:8111/viewLog.html?buildId=1&buildTypeId=Netology_Build 
TeamCity server version is 2023.05.4 (build 129421), server timezone: GMT (UTC)

[08:02:40]W: bt1 (33s)
[08:02:40]i: TeamCity server version is 2023.05.4 (build 129421)
[08:02:40] : The build is removed from the queue to be prepared for the start
[08:02:41] : Collecting changes in 1 VCS root
[08:02:41] :	 [Collecting changes in 1 VCS root] VCS Root details
[08:02:41] :		 [VCS Root details] "https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master" {instance id=1, parent internal id=1, parent id=Netology_HttpsGithubComSemenAmbarnovExampleTeamcityGitRefsHeadsMaster, description: "https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master"}
[08:02:41]i:	 [Collecting changes in 1 VCS root] Loading current repository state for VCS root 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'
[08:02:41]i:		 [Loading current repository state for VCS root 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'] VCS root 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master': git -c core.askpass=/opt/teamcity/temp/pass9862601573126222459 -c credential.helper= ls-remote origin
[08:02:41]i:	 [Collecting changes in 1 VCS root] Detecting changes in VCS root 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master' (used in 'Build')
[08:02:41]i:	 [Collecting changes in 1 VCS root] Will collect changes for 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master' starting from revision 817aad0ca811ebb403effd538c0a52542a6414c8
[08:02:41] :	 [Collecting changes in 1 VCS root] Compute revision for 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'
[08:02:41] :		 [Compute revision for 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'] Upper limit revision: 817aad0ca811ebb403effd538c0a52542a6414c8
[08:02:41]i:		 [Compute revision for 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'] MaxModId = 1
[08:02:41] :		 [Compute revision for 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'] The first revision that was detected in the branch refs/heads/master: db1c910a3f0442d9a9b9c3411db8c9c298019bf1
[08:02:41] :		 [Compute revision for 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'] The first revision that was detected in the branch refs/heads/master after the last change of the VCS root or checkout rules: db1c910a3f0442d9a9b9c3411db8c9c298019bf1
[08:02:41] :		 [Compute revision for 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'] Latest commit attached to build configuration (with id <= 1): 817aad0ca811ebb403effd538c0a52542a6414c8
[08:02:41] :		 [Compute revision for 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'] Computed revision: 817aad0ca811ebb403effd538c0a52542a6414c8
[08:02:41] : Starting the build on the agent "ip_130.193.37.216"
[08:02:42]i: Agent time zone: Europe/London
[08:02:42]i: Agent is running under JRE: 17.0.7+7-LTS
[08:02:42] : Updating tools for build (1s)
[08:02:42] :	 [Updating tools for build] Found 1 tool used by the build: maven3_6
[08:02:44] :	 [Updating tools for build] Tool maven3_6 updated successfully
[08:02:44] : Clearing temporary directory: /opt/buildagent/temp/buildTmp
[08:02:44]i: Preparing performance monitoring data directory: /opt/buildagent/system/perfmon
[08:02:44]i: Performance monitor is using command line: [perl, /opt/buildagent/system/perfmon/scripts/vmstatlinux.pl, /opt/buildagent/system/perfmon/temp/1/perfmon.csv, 1000]
[08:02:44]i: Starting performance monitoring process
[08:02:44]i: Performance monitoring process started
[08:02:44] : Publishing internal artifacts
[08:02:44] :	 [Publishing internal artifacts] Publishing 1 file using [WebPublisher]
[08:02:44] :	 [Publishing internal artifacts] Publishing 1 file using [ArtifactsCachePublisherImpl]
[08:02:44]i:	 [Publishing internal artifacts] Will publish 1 artifact(s) to TeamCity node with id MAIN_SERVER
[08:02:44] : Full checkout enforced. Reason: [Checkout directory is empty or doesn't exist]
[08:02:44] : Will perform clean checkout. Reason: Checkout directory is empty or doesn't exist
[08:02:44] : Checkout directory: /opt/buildagent/work/8e44ef381d17132e
[08:02:44] : Updating sources: auto checkout (on agent) (6s)
[08:02:44] :	 [Updating sources] Will use agent side checkout
[08:02:44] :	 [Updating sources] VCS Root: https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master (6s)
[08:02:44] :		 [VCS Root: https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master] revision: 817aad0ca811ebb403effd538c0a52542a6414c8
[08:02:44]i:		 [VCS Root: https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master] Mirrors automatically enabled
[08:02:44] :		 [VCS Root: https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master] Git version: 2.42.0.0
[08:02:44] :		 [VCS Root: https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master] Update git mirror (/opt/buildagent/system/git/git-DBA0D768.git) (5s)
[08:02:44] :			 [Update git mirror (/opt/buildagent/system/git/git-DBA0D768.git)] /usr/bin/git init --bare --initial-branch=main
[08:02:47] :			 [Update git mirror (/opt/buildagent/system/git/git-DBA0D768.git)] /usr/bin/git config http.sslCAInfo
[08:02:47] :			 [Update git mirror (/opt/buildagent/system/git/git-DBA0D768.git)] Local clone state requires 'git fetch'.
[08:02:48] :			 [Update git mirror (/opt/buildagent/system/git/git-DBA0D768.git)] /usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master (1s)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Enumerating objects: 346, done.        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:   0% (1/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:   1% (4/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:   2% (7/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:   3% (11/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:   4% (14/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:   5% (18/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:   6% (21/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:   7% (25/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:   8% (28/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:   9% (32/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  10% (35/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  11% (39/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  12% (42/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  13% (45/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  14% (49/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  15% (52/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  16% (56/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  17% (59/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  18% (63/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  19% (66/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  20% (70/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  21% (73/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  22% (77/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  23% (80/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  24% (84/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  25% (87/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  26% (90/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  27% (94/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  28% (97/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  29% (101/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  30% (104/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  31% (108/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  32% (111/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  33% (115/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  34% (118/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  35% (122/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  36% (125/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  37% (129/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  38% (132/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  39% (135/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  40% (139/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  41% (142/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  42% (146/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  43% (149/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  44% (153/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  45% (156/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  46% (160/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  47% (163/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  48% (167/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  49% (170/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  50% (173/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  51% (177/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  52% (180/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  53% (184/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  54% (187/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  55% (191/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  56% (194/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  57% (198/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  58% (201/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  59% (205/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  60% (208/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  61% (212/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  62% (215/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  63% (218/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  64% (222/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  65% (225/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  66% (229/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  67% (232/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  68% (236/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  69% (239/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  70% (243/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  71% (246/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  72% (250/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  73% (253/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  74% (257/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  75% (260/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  76% (263/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  77% (267/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  78% (270/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  79% (274/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  80% (277/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  81% (281/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  82% (284/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  83% (288/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  84% (291/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  85% (295/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  86% (298/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  87% (302/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  88% (305/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  89% (308/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  90% (312/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  91% (315/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  92% (319/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  93% (322/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  94% (326/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  95% (329/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  96% (333/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  97% (336/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  98% (340/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  99% (343/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects: 100% (346/346)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects: 100% (346/346), done.        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:   0% (1/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:   1% (2/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:   2% (3/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:   3% (5/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:   4% (6/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:   5% (8/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:   6% (9/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:   7% (11/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:   8% (12/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:   9% (13/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  10% (15/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  11% (16/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  12% (18/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  13% (19/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  14% (21/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  15% (22/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  16% (24/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  17% (25/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  18% (26/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  19% (28/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  20% (29/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  21% (31/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  22% (32/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  23% (34/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  24% (35/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  25% (36/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  26% (38/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  27% (39/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  28% (41/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  29% (42/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  30% (44/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  31% (45/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  32% (47/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  33% (48/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  34% (49/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  35% (51/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  36% (52/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  37% (54/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  38% (55/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  39% (57/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  40% (58/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  41% (60/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  42% (61/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  43% (62/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  44% (64/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  45% (65/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  46% (67/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  47% (68/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  48% (70/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  49% (71/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  50% (72/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  51% (74/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  52% (75/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  53% (77/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  54% (78/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  55% (80/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  56% (81/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  57% (83/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  58% (84/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  59% (85/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  60% (87/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  61% (88/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  62% (90/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  63% (91/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  64% (93/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  65% (94/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  66% (96/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  67% (97/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  68% (98/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  69% (100/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  70% (101/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  71% (103/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  72% (104/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  73% (106/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  74% (107/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  75% (108/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  76% (110/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  77% (111/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  78% (113/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  79% (114/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  80% (116/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  81% (117/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  82% (119/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  83% (120/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  84% (121/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  85% (123/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  86% (124/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  87% (126/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  88% (127/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  89% (129/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  90% (130/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  91% (132/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  92% (133/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  93% (134/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  94% (136/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  95% (137/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  96% (139/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  97% (140/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  98% (142/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  99% (143/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects: 100% (144/144)        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects: 100% (144/144), done.        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:   0% (1/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:   1% (4/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:   2% (7/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:   3% (11/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:   4% (14/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:   5% (18/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:   6% (21/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:   7% (25/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:   8% (28/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:   9% (32/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  10% (35/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  11% (39/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  12% (42/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  13% (45/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  14% (49/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  15% (52/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  16% (56/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  17% (59/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  18% (63/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  19% (66/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  20% (70/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  21% (73/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  22% (77/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  23% (80/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  24% (84/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  25% (87/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  26% (90/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  27% (94/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  28% (97/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  29% (101/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  30% (104/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  31% (108/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  32% (111/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  33% (115/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  34% (118/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  35% (122/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  36% (125/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  37% (129/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  38% (132/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  39% (135/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  40% (139/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  41% (142/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  42% (146/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  43% (149/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  44% (153/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  45% (156/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  46% (160/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  47% (163/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  48% (167/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  49% (170/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  50% (173/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  51% (177/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  52% (180/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  53% (184/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  54% (187/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  55% (191/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  56% (194/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  57% (198/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  58% (201/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  59% (205/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  60% (208/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  61% (212/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  62% (215/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  63% (218/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  64% (222/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  65% (225/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  66% (229/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  67% (232/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  68% (236/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  69% (239/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  70% (243/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  71% (246/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  72% (250/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  73% (253/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  74% (257/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  75% (260/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  76% (263/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  77% (267/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  78% (270/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  79% (274/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  80% (277/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  81% (281/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  82% (284/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  83% (288/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  84% (291/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  85% (295/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  86% (298/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  87% (302/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  88% (305/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  89% (308/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  90% (312/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  91% (315/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  92% (319/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  93% (322/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  94% (326/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  95% (329/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Total 346 (delta 118), reused 321 (delta 110), pack-reused 0        
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  96% (333/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  97% (336/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  98% (340/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects:  99% (343/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects: 100% (346/346)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Receiving objects: 100% (346/346), 45.56 KiB | 1.06 MiB/s, done.
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:   0% (0/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:   1% (2/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:   2% (3/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:   3% (4/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:   4% (5/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:   5% (6/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:   6% (8/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:   7% (9/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:   8% (10/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:   9% (11/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  10% (12/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  11% (13/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  12% (15/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  13% (16/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  14% (17/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  15% (18/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  16% (19/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  17% (21/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  18% (22/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  19% (23/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  20% (24/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  21% (25/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  22% (26/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  23% (28/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  24% (29/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  25% (30/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  26% (31/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  27% (32/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  28% (34/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  29% (35/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  30% (36/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  31% (37/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  32% (38/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  33% (39/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  34% (41/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  35% (42/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  36% (43/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  37% (44/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  38% (45/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  39% (47/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  40% (48/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  41% (49/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  42% (50/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  43% (51/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  44% (52/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  45% (54/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  46% (55/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  47% (56/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  48% (57/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  49% (58/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  50% (59/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  51% (61/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  52% (62/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  53% (63/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  54% (64/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  55% (65/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  56% (67/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  57% (68/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  58% (69/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  59% (70/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  60% (71/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  61% (72/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  62% (74/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  63% (75/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  64% (76/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  65% (77/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  66% (78/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  67% (80/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  68% (81/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  69% (82/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  70% (83/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  71% (84/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  72% (85/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  73% (87/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  74% (88/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  75% (89/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  76% (90/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  77% (91/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  78% (93/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  79% (94/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  80% (95/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  81% (96/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  82% (97/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  83% (98/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  84% (100/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  85% (101/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  86% (102/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  87% (103/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  88% (104/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  89% (106/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  90% (107/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  91% (108/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  92% (109/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  93% (110/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  94% (111/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  95% (113/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  96% (114/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  97% (115/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  98% (116/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas:  99% (117/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas: 100% (118/118)
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] Resolving deltas: 100% (118/118), done.
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] From https://github.com/SemenAmbarnov/example-teamcity
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master]  * [new branch]      master     -> master
[08:02:49]i:				 [/usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass14356226388437078160 -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master]  * [new branch]      master     -> origin/master
[08:02:49] :			 [Update git mirror (/opt/buildagent/system/git/git-DBA0D768.git)] /usr/bin/git log -n1 --pretty=format:%H%x20%s 817aad0ca811ebb403effd538c0a52542a6414c8 --
[08:02:49] :			 [Update git mirror (/opt/buildagent/system/git/git-DBA0D768.git)] /usr/bin/git pack-refs --all
[08:02:49] :		 [VCS Root: https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master] Update checkout directory (/opt/buildagent/work/8e44ef381d17132e) (1s)
[08:02:49] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] The .git directory is missing in '/opt/buildagent/work/8e44ef381d17132e'. Running 'git init'...
[08:02:49] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git init --initial-branch=main
[08:02:50] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git config lfs.storage /opt/buildagent/system/git/git-DBA0D768.git/lfs
[08:02:50] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git config core.sparseCheckout true
[08:02:50] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git config http.sslCAInfo
[08:02:50] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git show-ref
[08:02:50] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass5094867109269833922 -c credential.helper= ls-remote origin
[08:02:51] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git show-ref refs/remotes/origin/master
[08:02:51] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git log -n1 --pretty=format:%H%x20%s 817aad0ca811ebb403effd538c0a52542a6414c8 --
[08:02:51] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] No 'git fetch' required: commit '817aad0ca811ebb403effd538c0a52542a6414c8' is in the local repository clone pointed by 'refs/remotes/origin/master'.
[08:02:51] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git branch
[08:02:51] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git update-ref refs/heads/master 817aad0ca811ebb403effd538c0a52542a6414c8
[08:02:51] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass13525296495087007547 -c credential.helper= -c credential.helper=/opt/buildagent/temp/buildTmp/credHelper10381663373062179487.sh checkout -q -f master
[08:02:51] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git branch --set-upstream-to=refs/remotes/origin/master
[08:02:51] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] Cleaning https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master in /opt/buildagent/work/8e44ef381d17132e the file set ALL_UNTRACKED
[08:02:51] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git clean -f -d -x
[08:02:51] : Build preparation done
[08:02:51]W: Step 1/1: Maven (19s)
[08:02:51] :	 [Step 1/1] Initial M2_HOME not set
[08:02:51] :	 [Step 1/1] Current M2_HOME = /opt/buildagent/tools/maven3_6
[08:02:51] :	 [Step 1/1] PATH = /opt/buildagent/tools/maven3_6/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
[08:02:51] :	 [Step 1/1] Using watcher: /opt/buildagent/plugins/mavenPlugin/maven-watcher-jdk17/maven-watcher-agent.jar
[08:02:51] :	 [Step 1/1] Using agent local repository at /opt/buildagent/system/jetbrains.maven.runner/maven.repo.local
[08:02:51] :	 [Step 1/1] *** Start reading the project structure ***
[08:02:51]i:	 [Step 1/1] Initial MAVEN_OPTS not set
[08:02:51]i:	 [Step 1/1] Current MAVEN_OPTS not set
[08:02:53]i:	 [Step 1/1] [INFO] Scanning for projects...
[08:02:53]i:	 [Step 1/1] [INFO] Downloading from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/org/jetbrains/maven/info-maven3-plugin/1.0.3/info-maven3-plugin-1.0.3.pom
[08:02:53]i:	 [Step 1/1] [INFO] Downloaded from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/org/jetbrains/maven/info-maven3-plugin/1.0.3/info-maven3-plugin-1.0.3.pom (367 B at 14 kB/s)
[08:02:53]i:	 [Step 1/1] [INFO] Downloading from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/org/jetbrains/maven/info-maven3-plugin/1.0.3/info-maven3-plugin-1.0.3.jar
[08:02:53]i:	 [Step 1/1] [INFO] Downloaded from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/org/jetbrains/maven/info-maven3-plugin/1.0.3/info-maven3-plugin-1.0.3.jar (9.9 kB at 494 kB/s)
[08:02:53]i:	 [Step 1/1] [INFO] 
[08:02:53]i:	 [Step 1/1] [INFO] -----------------------< org.netology:plaindoll >-----------------------
[08:02:53]i:	 [Step 1/1] [INFO] Building plaindoll 0.0.1
[08:02:53]i:	 [Step 1/1] [INFO] --------------------------------[ jar ]---------------------------------
[08:02:53]i:	 [Step 1/1] [INFO] 
[08:02:53]i:	 [Step 1/1] [INFO] --- info-maven3-plugin:1.0.3:info (default-cli) @ plaindoll ---
[08:02:53]i:	 [Step 1/1] [INFO] Downloading from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/org/jetbrains/maven/maven-embedder-api/1.2.4/maven-embedder-api-1.2.4.pom
[08:02:53]i:	 [Step 1/1] [INFO] Downloaded from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/org/jetbrains/maven/maven-embedder-api/1.2.4/maven-embedder-api-1.2.4.pom (488 B at 244 kB/s)
[08:02:53]i:	 [Step 1/1] [INFO] Downloading from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/xerces/xercesImpl/2.12.2/xercesImpl-2.12.2.pom
[08:02:53]i:	 [Step 1/1] [INFO] Downloaded from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/xerces/xercesImpl/2.12.2/xercesImpl-2.12.2.pom (170 B at 57 kB/s)
[08:02:53]i:	 [Step 1/1] [INFO] Downloading from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/xml-apis/xml-apis/1.4.01/xml-apis-1.4.01.pom
[08:02:53]i:	 [Step 1/1] [INFO] Downloaded from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/xml-apis/xml-apis/1.4.01/xml-apis-1.4.01.pom (170 B at 57 kB/s)
[08:02:53]i:	 [Step 1/1] [INFO] Downloading from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/org/jetbrains/maven/maven-embedder-api/1.2.4/maven-embedder-api-1.2.4.jar
[08:02:53]i:	 [Step 1/1] [INFO] Downloading from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/xerces/xercesImpl/2.12.2/xercesImpl-2.12.2.jar
[08:02:53]i:	 [Step 1/1] [INFO] Downloaded from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/org/jetbrains/maven/maven-embedder-api/1.2.4/maven-embedder-api-1.2.4.jar (33 kB at 2.5 MB/s)
[08:02:53]i:	 [Step 1/1] [INFO] Downloading from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/xml-apis/xml-apis/1.4.01/xml-apis-1.4.01.jar
[08:02:53]i:	 [Step 1/1] [INFO] Downloading from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/org/codehaus/plexus/plexus-utils/1.1/plexus-utils-1.1.jar
[08:02:53]i:	 [Step 1/1] [INFO] Downloaded from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/xml-apis/xml-apis/1.4.01/xml-apis-1.4.01.jar (221 kB at 3.0 MB/s)
[08:02:53]i:	 [Step 1/1] [INFO] Downloaded from teamcity_maven_local_plugin_repo: file:/opt/buildagent/plugins/mavenPlugin/info-plugin/xerces/xercesImpl/2.12.2/xercesImpl-2.12.2.jar (1.4 MB at 12 MB/s)
[08:02:54]i:	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.1/plexus-utils-1.1.jar
[08:02:54]i:	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.1/plexus-utils-1.1.jar (169 kB at 254 kB/s)
[08:02:55]i:	 [Step 1/1] [INFO] ------------------------------------------------------------------------
[08:02:55]i:	 [Step 1/1] [INFO] BUILD SUCCESS
[08:02:55]i:	 [Step 1/1] [INFO] ------------------------------------------------------------------------
[08:02:55]i:	 [Step 1/1] [INFO] Total time:  1.643 s
[08:02:55]i:	 [Step 1/1] [INFO] Finished at: 2023-09-27T09:02:55+01:00
[08:02:55]i:	 [Step 1/1] [INFO] ------------------------------------------------------------------------
[08:02:55]i:	 [Step 1/1] Process exited with code 0
[08:02:55] :	 [Step 1/1] Initial MAVEN_OPTS not set
[08:02:55] :	 [Step 1/1] Current MAVEN_OPTS not set
[08:02:55] :	 [Step 1/1] Starting: /opt/java/openjdk/bin/java -Dagent.home.dir=/opt/buildagent -Dagent.name=ip_130.193.37.216 -Dagent.ownPort=9090 -Dagent.work.dir=/opt/buildagent/work -Dbuild.number=1 -Dbuild.vcs.number=817aad0ca811ebb403effd538c0a52542a6414c8 -Dbuild.vcs.number.1=817aad0ca811ebb403effd538c0a52542a6414c8 -Dbuild.vcs.number.Netology_HttpsGithubComSemenAmbarnovExampleTeamcityGitRefsHeadsMaster=817aad0ca811ebb403effd538c0a52542a6414c8 -Dclassworlds.conf=/opt/buildagent/temp/buildTmp/teamcity.m2.conf -Dcom.jetbrains.maven.watcher.report.file=/opt/buildagent/temp/buildTmp/maven-build-info.xml -Djava.io.tmpdir=/opt/buildagent/temp/buildTmp -Dmaven.home=/opt/buildagent/tools/maven3_6 -Dmaven.multiModuleProjectDirectory=/opt/buildagent/work/8e44ef381d17132e -Dteamcity.agent.cpuBenchmark=457 -Dteamcity.agent.dotnet.agent_url=http://localhost:9090/RPC2 -Dteamcity.agent.dotnet.build_id=1 -Dteamcity.auth.password=******* -Dteamcity.auth.userId=TeamCityBuildId=1 -Dteamcity.build.changedFiles.file=/opt/buildagent/temp/buildTmp/teamcity.changedFiles.txt -Dteamcity.build.checkoutDir=/opt/buildagent/work/8e44ef381d17132e -Dteamcity.build.id=1 -Dteamcity.build.properties.file=/opt/buildagent/temp/buildTmp/teamcity.build.parameters -Dteamcity.build.tempDir=/opt/buildagent/temp/buildTmp -Dteamcity.build.workingDir=/opt/buildagent/work/8e44ef381d17132e -Dteamcity.buildConfName=Build -Dteamcity.buildType.id=Netology_Build -Dteamcity.configuration.properties.file=/opt/buildagent/temp/buildTmp/teamcity.config.parameters -Dteamcity.maven.watcher.home=/opt/buildagent/plugins/mavenPlugin/maven-watcher-jdk17 -Dteamcity.projectName=netology -Dteamcity.runner.properties.file=/opt/buildagent/temp/buildTmp/teamcity.runner.parameters -Dteamcity.tests.recentlyFailedTests.file=/opt/buildagent/temp/buildTmp/teamcity.testsToRunFirst.txt -Dteamcity.version=2023.05.4 (build 129421) -Dmaven.repo.local=/opt/buildagent/system/jetbrains.maven.runner/maven.repo.local -classpath /opt/buildagent/tools/maven3_6/boot/plexus-classworlds-2.6.0.jar: org.codehaus.plexus.classworlds.launcher.Launcher -f /opt/buildagent/work/8e44ef381d17132e/pom.xml -B -Dmaven.test.failure.ignore=true clean test
[08:02:55] :	 [Step 1/1] in directory: /opt/buildagent/work/8e44ef381d17132e
[08:02:56] :	 [Step 1/1] [INFO] Scanning for projects...
[08:02:57] :	 [Step 1/1] [INFO] 
[08:02:57] :	 [Step 1/1] [INFO] -----------------------< org.netology:plaindoll >-----------------------
[08:02:57] :	 [Step 1/1] [INFO] Building plaindoll 0.0.1
[08:02:57] :	 [Step 1/1] [INFO] --------------------------------[ jar ]---------------------------------
[08:02:57] :	 [Step 1/1] [Maven Watcher] project started: org.netology:plaindoll:jar:0.0.1
[08:02:57] :	 [Step 1/1] org.netology:plaindoll (12s)
[08:02:57]i:		 [org.netology:plaindoll] ##teamcity[importData tc:tags='tc:internal' type='surefire' path='/opt/buildagent/work/8e44ef381d17132e/target/surefire-reports/TEST-*.xml' whenNoDataPublished='nothing' logAsInternal='true']
[08:02:57] :	 [Step 1/1] Importing data from '/opt/buildagent/work/8e44ef381d17132e/target/surefire-reports/TEST-*.xml' (not existing file) with 'surefire' processor
[08:02:57]i:		 [org.netology:plaindoll] ##teamcity[importData tc:tags='tc:internal' type='surefire' path='/opt/buildagent/work/8e44ef381d17132e/target/failsafe-reports/TEST-*.xml' whenNoDataPublished='nothing' logAsInternal='true']
[08:02:57] :	 [Step 1/1] [Maven Watcher] 
[08:02:57]i:	 [Step 1/1] ##teamcity[projectStarted tc:tags='tc:internal' projectId='org.netology:plaindoll:jar:0.0.1' groupId='org.netology' artifactId='plaindoll' testReportsDir0='/opt/buildagent/work/8e44ef381d17132e/target/surefire-reports' testReportsDir1='/opt/buildagent/work/8e44ef381d17132e/target/failsafe-reports']
[08:02:57] :	 [Step 1/1] Importing data from '/opt/buildagent/work/8e44ef381d17132e/target/failsafe-reports/TEST-*.xml' (not existing file) with 'surefire' processor
[08:02:57] :	 [Step 1/1] Surefire report watcher
[08:02:57] :		 [Surefire report watcher] Watching paths:
[08:02:57] :		 [Surefire report watcher] /opt/buildagent/work/8e44ef381d17132e/target/surefire-reports/TEST-*.xml
[08:02:57] :	 [Step 1/1] Surefire report watcher
[08:02:57] :		 [Surefire report watcher] Watching paths:
[08:02:57] :		 [Surefire report watcher] /opt/buildagent/work/8e44ef381d17132e/target/failsafe-reports/TEST-*.xml
[08:02:57] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-clean-plugin/2.5/maven-clean-plugin-2.5.pom
[08:02:57] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-clean-plugin/2.5/maven-clean-plugin-2.5.pom (3.9 kB at 9.4 kB/s)
[08:02:58] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-plugins/22/maven-plugins-22.pom
[08:02:58] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-plugins/22/maven-plugins-22.pom (13 kB at 174 kB/s)
[08:02:58] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/21/maven-parent-21.pom
[08:02:58] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/21/maven-parent-21.pom (26 kB at 334 kB/s)
[08:02:58] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/apache/10/apache-10.pom
[08:02:58] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/apache/10/apache-10.pom (15 kB at 239 kB/s)
[08:02:58] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-clean-plugin/2.5/maven-clean-plugin-2.5.jar
[08:02:58] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-clean-plugin/2.5/maven-clean-plugin-2.5.jar (25 kB at 391 kB/s)
[08:02:58] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-resources-plugin/2.6/maven-resources-plugin-2.6.pom
[08:02:58] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-resources-plugin/2.6/maven-resources-plugin-2.6.pom (8.1 kB at 127 kB/s)
[08:02:58] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-plugins/23/maven-plugins-23.pom
[08:02:58] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-plugins/23/maven-plugins-23.pom (9.2 kB at 174 kB/s)
[08:02:58] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/22/maven-parent-22.pom
[08:02:58] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/22/maven-parent-22.pom (30 kB at 488 kB/s)
[08:02:58] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/apache/11/apache-11.pom
[08:02:58] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/apache/11/apache-11.pom (15 kB at 221 kB/s)
[08:02:58] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-resources-plugin/2.6/maven-resources-plugin-2.6.jar
[08:02:58] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-resources-plugin/2.6/maven-resources-plugin-2.6.jar (30 kB at 394 kB/s)
[08:02:58] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-compiler-plugin/3.1/maven-compiler-plugin-3.1.pom
[08:02:58] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-compiler-plugin/3.1/maven-compiler-plugin-3.1.pom (10 kB at 182 kB/s)
[08:02:58] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-plugins/24/maven-plugins-24.pom
[08:02:58] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-plugins/24/maven-plugins-24.pom (11 kB at 216 kB/s)
[08:02:58] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/23/maven-parent-23.pom
[08:02:58] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/23/maven-parent-23.pom (33 kB at 494 kB/s)
[08:02:58] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/apache/13/apache-13.pom
[08:02:58] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/apache/13/apache-13.pom (14 kB at 254 kB/s)
[08:02:58] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-compiler-plugin/3.1/maven-compiler-plugin-3.1.jar
[08:02:59] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-compiler-plugin/3.1/maven-compiler-plugin-3.1.jar (43 kB at 565 kB/s)
[08:02:59] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-surefire-plugin/2.12.4/maven-surefire-plugin-2.12.4.pom
[08:02:59] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-surefire-plugin/2.12.4/maven-surefire-plugin-2.12.4.pom (10 kB at 205 kB/s)
[08:02:59] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/surefire/2.12.4/surefire-2.12.4.pom
[08:02:59] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/surefire/2.12.4/surefire-2.12.4.pom (14 kB at 276 kB/s)
[08:02:59] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-surefire-plugin/2.12.4/maven-surefire-plugin-2.12.4.jar
[08:02:59] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-surefire-plugin/2.12.4/maven-surefire-plugin-2.12.4.jar (30 kB at 575 kB/s)
[08:02:59] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/junit/junit/4.12/junit-4.12.pom
[08:02:59] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/junit/junit/4.12/junit-4.12.pom (24 kB at 408 kB/s)
[08:02:59] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/hamcrest/hamcrest-core/1.3/hamcrest-core-1.3.pom
[08:02:59] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/hamcrest/hamcrest-core/1.3/hamcrest-core-1.3.pom (766 B at 16 kB/s)
[08:02:59] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/hamcrest/hamcrest-parent/1.3/hamcrest-parent-1.3.pom
[08:02:59] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/hamcrest/hamcrest-parent/1.3/hamcrest-parent-1.3.pom (2.0 kB at 38 kB/s)
[08:02:59] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/junit/junit/4.12/junit-4.12.jar
[08:02:59] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/hamcrest/hamcrest-core/1.3/hamcrest-core-1.3.jar
[08:02:59] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/junit/junit/4.12/junit-4.12.jar (315 kB at 2.6 MB/s)
[08:02:59] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/hamcrest/hamcrest-core/1.3/hamcrest-core-1.3.jar (45 kB at 326 kB/s)
[08:02:59] :	 [Step 1/1] [INFO] 
[08:02:59] :	 [Step 1/1] [INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ plaindoll ---
[08:02:59] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-api/2.0.6/maven-plugin-api-2.0.6.pom
[08:02:59] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-api/2.0.6/maven-plugin-api-2.0.6.pom (1.5 kB at 27 kB/s)
[08:02:59] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven/2.0.6/maven-2.0.6.pom
[08:02:59] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven/2.0.6/maven-2.0.6.pom (9.0 kB at 181 kB/s)
[08:02:59] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/5/maven-parent-5.pom
[08:02:59] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/5/maven-parent-5.pom (15 kB at 238 kB/s)
[08:02:59] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/apache/3/apache-3.pom
[08:02:59] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/apache/3/apache-3.pom (3.4 kB at 57 kB/s)
[08:02:59] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.0/plexus-utils-3.0.pom
[08:02:59] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.0/plexus-utils-3.0.pom (4.1 kB at 58 kB/s)
[08:02:59] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/spice/spice-parent/16/spice-parent-16.pom
[08:02:59] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/spice/spice-parent/16/spice-parent-16.pom (8.4 kB at 167 kB/s)
[08:02:59] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/forge/forge-parent/5/forge-parent-5.pom
[08:03:00] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/forge/forge-parent/5/forge-parent-5.pom (8.4 kB at 155 kB/s)
[08:03:00] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-api/2.0.6/maven-plugin-api-2.0.6.jar
[08:03:00] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.0/plexus-utils-3.0.jar
[08:03:00] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-api/2.0.6/maven-plugin-api-2.0.6.jar (13 kB at 238 kB/s)
[08:03:00] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.0/plexus-utils-3.0.jar (226 kB at 3.3 MB/s)
[08:03:00] :	 [Step 1/1] [INFO] 
[08:03:00] :	 [Step 1/1] [INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ plaindoll ---
[08:03:00] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-project/2.0.6/maven-project-2.0.6.pom
[08:03:00] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-project/2.0.6/maven-project-2.0.6.pom (2.6 kB at 51 kB/s)
[08:03:00] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings/2.0.6/maven-settings-2.0.6.pom
[08:03:00] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings/2.0.6/maven-settings-2.0.6.pom (2.0 kB at 38 kB/s)
[08:03:00] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model/2.0.6/maven-model-2.0.6.pom
[08:03:00] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model/2.0.6/maven-model-2.0.6.pom (3.0 kB at 62 kB/s)
[08:03:00] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.4.1/plexus-utils-1.4.1.pom
[08:03:00] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.4.1/plexus-utils-1.4.1.pom (1.9 kB at 38 kB/s)
[08:03:00] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/1.0.11/plexus-1.0.11.pom
[08:03:00] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/1.0.11/plexus-1.0.11.pom (9.0 kB at 176 kB/s)
[08:03:00] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-container-default/1.0-alpha-9-stable-1/plexus-container-default-1.0-alpha-9-stable-1.pom
[08:03:00] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-container-default/1.0-alpha-9-stable-1/plexus-container-default-1.0-alpha-9-stable-1.pom (3.9 kB at 81 kB/s)
[08:03:00] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-containers/1.0.3/plexus-containers-1.0.3.pom
[08:03:00] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-containers/1.0.3/plexus-containers-1.0.3.pom (492 B at 10 kB/s)
[08:03:00] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/1.0.4/plexus-1.0.4.pom
[08:03:00] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/1.0.4/plexus-1.0.4.pom (5.7 kB at 120 kB/s)
[08:03:00] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/junit/junit/3.8.1/junit-3.8.1.pom
[08:03:00] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/junit/junit/3.8.1/junit-3.8.1.pom (998 B at 19 kB/s)
[08:03:00] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.0.4/plexus-utils-1.0.4.pom
[08:03:00] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.0.4/plexus-utils-1.0.4.pom (6.9 kB at 137 kB/s)
[08:03:00] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/classworlds/classworlds/1.1-alpha-2/classworlds-1.1-alpha-2.pom
[08:03:00] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/classworlds/classworlds/1.1-alpha-2/classworlds-1.1-alpha-2.pom (3.1 kB at 61 kB/s)
[08:03:00] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-profile/2.0.6/maven-profile-2.0.6.pom
[08:03:00] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-profile/2.0.6/maven-profile-2.0.6.pom (2.0 kB at 40 kB/s)
[08:03:00] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact-manager/2.0.6/maven-artifact-manager-2.0.6.pom
[08:03:00] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact-manager/2.0.6/maven-artifact-manager-2.0.6.pom (2.6 kB at 47 kB/s)
[08:03:00] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-repository-metadata/2.0.6/maven-repository-metadata-2.0.6.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-repository-metadata/2.0.6/maven-repository-metadata-2.0.6.pom (1.9 kB at 24 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact/2.0.6/maven-artifact-2.0.6.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact/2.0.6/maven-artifact-2.0.6.pom (1.6 kB at 27 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-registry/2.0.6/maven-plugin-registry-2.0.6.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-registry/2.0.6/maven-plugin-registry-2.0.6.pom (1.9 kB at 40 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-core/2.0.6/maven-core-2.0.6.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-core/2.0.6/maven-core-2.0.6.pom (6.7 kB at 132 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-parameter-documenter/2.0.6/maven-plugin-parameter-documenter-2.0.6.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-parameter-documenter/2.0.6/maven-plugin-parameter-documenter-2.0.6.pom (1.9 kB at 37 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/reporting/maven-reporting-api/2.0.6/maven-reporting-api-2.0.6.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/reporting/maven-reporting-api/2.0.6/maven-reporting-api-2.0.6.pom (1.8 kB at 36 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/reporting/maven-reporting/2.0.6/maven-reporting-2.0.6.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/reporting/maven-reporting/2.0.6/maven-reporting-2.0.6.pom (1.4 kB at 29 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/doxia/doxia-sink-api/1.0-alpha-7/doxia-sink-api-1.0-alpha-7.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/doxia/doxia-sink-api/1.0-alpha-7/doxia-sink-api-1.0-alpha-7.pom (424 B at 9.0 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/doxia/doxia/1.0-alpha-7/doxia-1.0-alpha-7.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/doxia/doxia/1.0-alpha-7/doxia-1.0-alpha-7.pom (3.9 kB at 72 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-error-diagnostics/2.0.6/maven-error-diagnostics-2.0.6.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-error-diagnostics/2.0.6/maven-error-diagnostics-2.0.6.pom (1.7 kB at 33 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/commons-cli/commons-cli/1.0/commons-cli-1.0.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/commons-cli/commons-cli/1.0/commons-cli-1.0.pom (2.1 kB at 44 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-descriptor/2.0.6/maven-plugin-descriptor-2.0.6.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-descriptor/2.0.6/maven-plugin-descriptor-2.0.6.pom (2.0 kB at 42 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interactivity-api/1.0-alpha-4/plexus-interactivity-api-1.0-alpha-4.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interactivity-api/1.0-alpha-4/plexus-interactivity-api-1.0-alpha-4.pom (7.1 kB at 151 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-monitor/2.0.6/maven-monitor-2.0.6.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-monitor/2.0.6/maven-monitor-2.0.6.pom (1.3 kB at 26 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/classworlds/classworlds/1.1/classworlds-1.1.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/classworlds/classworlds/1.1/classworlds-1.1.pom (3.3 kB at 65 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/2.0.5/plexus-utils-2.0.5.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/2.0.5/plexus-utils-2.0.5.pom (3.3 kB at 68 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/2.0.6/plexus-2.0.6.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/2.0.6/plexus-2.0.6.pom (17 kB at 342 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-filtering/1.1/maven-filtering-1.1.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-filtering/1.1/maven-filtering-1.1.pom (5.8 kB at 118 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-components/17/maven-shared-components-17.pom
[08:03:01] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-components/17/maven-shared-components-17.pom (8.7 kB at 178 kB/s)
[08:03:01] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.5.15/plexus-utils-1.5.15.pom
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.5.15/plexus-utils-1.5.15.pom (6.8 kB at 127 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/2.0.2/plexus-2.0.2.pom
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/2.0.2/plexus-2.0.2.pom (12 kB at 228 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interpolation/1.12/plexus-interpolation-1.12.pom
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interpolation/1.12/plexus-interpolation-1.12.pom (889 B at 19 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-components/1.1.14/plexus-components-1.1.14.pom
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-components/1.1.14/plexus-components-1.1.14.pom (5.8 kB at 122 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/plexus/plexus-build-api/0.0.4/plexus-build-api-0.0.4.pom
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/plexus/plexus-build-api/0.0.4/plexus-build-api-0.0.4.pom (2.9 kB at 55 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/spice/spice-parent/10/spice-parent-10.pom
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/spice/spice-parent/10/spice-parent-10.pom (3.0 kB at 64 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/forge/forge-parent/3/forge-parent-3.pom
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/forge/forge-parent/3/forge-parent-3.pom (5.0 kB at 101 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.5.8/plexus-utils-1.5.8.pom
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.5.8/plexus-utils-1.5.8.pom (8.1 kB at 155 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interpolation/1.13/plexus-interpolation-1.13.pom
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interpolation/1.13/plexus-interpolation-1.13.pom (890 B at 19 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-components/1.1.15/plexus-components-1.1.15.pom
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-components/1.1.15/plexus-components-1.1.15.pom (2.8 kB at 59 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/2.0.3/plexus-2.0.3.pom
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/2.0.3/plexus-2.0.3.pom (15 kB at 329 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-profile/2.0.6/maven-profile-2.0.6.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-project/2.0.6/maven-project-2.0.6.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact-manager/2.0.6/maven-artifact-manager-2.0.6.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-registry/2.0.6/maven-plugin-registry-2.0.6.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-core/2.0.6/maven-core-2.0.6.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact-manager/2.0.6/maven-artifact-manager-2.0.6.jar (57 kB at 698 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-parameter-documenter/2.0.6/maven-plugin-parameter-documenter-2.0.6.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-project/2.0.6/maven-project-2.0.6.jar (116 kB at 1.4 MB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/reporting/maven-reporting-api/2.0.6/maven-reporting-api-2.0.6.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-profile/2.0.6/maven-profile-2.0.6.jar (35 kB at 271 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/doxia/doxia-sink-api/1.0-alpha-7/doxia-sink-api-1.0-alpha-7.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/reporting/maven-reporting-api/2.0.6/maven-reporting-api-2.0.6.jar (9.9 kB at 74 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-parameter-documenter/2.0.6/maven-plugin-parameter-documenter-2.0.6.jar (21 kB at 153 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-repository-metadata/2.0.6/maven-repository-metadata-2.0.6.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-error-diagnostics/2.0.6/maven-error-diagnostics-2.0.6.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-registry/2.0.6/maven-plugin-registry-2.0.6.jar (29 kB at 198 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/commons-cli/commons-cli/1.0/commons-cli-1.0.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/doxia/doxia-sink-api/1.0-alpha-7/doxia-sink-api-1.0-alpha-7.jar (5.9 kB at 34 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-descriptor/2.0.6/maven-plugin-descriptor-2.0.6.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-repository-metadata/2.0.6/maven-repository-metadata-2.0.6.jar (24 kB at 132 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interactivity-api/1.0-alpha-4/plexus-interactivity-api-1.0-alpha-4.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-error-diagnostics/2.0.6/maven-error-diagnostics-2.0.6.jar (14 kB at 72 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/classworlds/classworlds/1.1/classworlds-1.1.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-core/2.0.6/maven-core-2.0.6.jar (152 kB at 782 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact/2.0.6/maven-artifact-2.0.6.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/commons-cli/commons-cli/1.0/commons-cli-1.0.jar (30 kB at 154 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings/2.0.6/maven-settings-2.0.6.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-descriptor/2.0.6/maven-plugin-descriptor-2.0.6.jar (37 kB at 162 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model/2.0.6/maven-model-2.0.6.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interactivity-api/1.0-alpha-4/plexus-interactivity-api-1.0-alpha-4.jar (13 kB at 57 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-monitor/2.0.6/maven-monitor-2.0.6.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact/2.0.6/maven-artifact-2.0.6.jar (87 kB at 360 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-container-default/1.0-alpha-9-stable-1/plexus-container-default-1.0-alpha-9-stable-1.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/classworlds/classworlds/1.1/classworlds-1.1.jar (38 kB at 154 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/junit/junit/3.8.1/junit-3.8.1.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings/2.0.6/maven-settings-2.0.6.jar (49 kB at 197 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/2.0.5/plexus-utils-2.0.5.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-monitor/2.0.6/maven-monitor-2.0.6.jar (10 kB at 36 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-filtering/1.1/maven-filtering-1.1.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model/2.0.6/maven-model-2.0.6.jar (86 kB at 289 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/plexus/plexus-build-api/0.0.4/plexus-build-api-0.0.4.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-container-default/1.0-alpha-9-stable-1/plexus-container-default-1.0-alpha-9-stable-1.jar (194 kB at 618 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interpolation/1.13/plexus-interpolation-1.13.jar
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/junit/junit/3.8.1/junit-3.8.1.jar (121 kB at 366 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/2.0.5/plexus-utils-2.0.5.jar (223 kB at 672 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-filtering/1.1/maven-filtering-1.1.jar (43 kB at 127 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/plexus/plexus-build-api/0.0.4/plexus-build-api-0.0.4.jar (6.8 kB at 19 kB/s)
[08:03:02] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interpolation/1.13/plexus-interpolation-1.13.jar (61 kB at 170 kB/s)
[08:03:03]W:	 [Step 1/1] [WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[08:03:03] :	 [Step 1/1] [INFO] skip non existing resourceDirectory /opt/buildagent/work/8e44ef381d17132e/src/main/resources
[08:03:03] :	 [Step 1/1] [INFO] 
[08:03:03] :	 [Step 1/1] [INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ plaindoll ---
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-api/2.0.9/maven-plugin-api-2.0.9.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-api/2.0.9/maven-plugin-api-2.0.9.pom (1.5 kB at 32 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven/2.0.9/maven-2.0.9.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven/2.0.9/maven-2.0.9.pom (19 kB at 394 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/8/maven-parent-8.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/8/maven-parent-8.pom (24 kB at 513 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/apache/4/apache-4.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/apache/4/apache-4.pom (4.5 kB at 98 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact/2.0.9/maven-artifact-2.0.9.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact/2.0.9/maven-artifact-2.0.9.pom (1.6 kB at 35 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.5.1/plexus-utils-1.5.1.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.5.1/plexus-utils-1.5.1.pom (2.3 kB at 50 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-core/2.0.9/maven-core-2.0.9.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-core/2.0.9/maven-core-2.0.9.pom (7.8 kB at 173 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings/2.0.9/maven-settings-2.0.9.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings/2.0.9/maven-settings-2.0.9.pom (2.1 kB at 47 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model/2.0.9/maven-model-2.0.9.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model/2.0.9/maven-model-2.0.9.pom (3.1 kB at 67 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-parameter-documenter/2.0.9/maven-plugin-parameter-documenter-2.0.9.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-parameter-documenter/2.0.9/maven-plugin-parameter-documenter-2.0.9.pom (2.0 kB at 43 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-profile/2.0.9/maven-profile-2.0.9.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-profile/2.0.9/maven-profile-2.0.9.pom (2.0 kB at 46 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-repository-metadata/2.0.9/maven-repository-metadata-2.0.9.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-repository-metadata/2.0.9/maven-repository-metadata-2.0.9.pom (1.9 kB at 42 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-error-diagnostics/2.0.9/maven-error-diagnostics-2.0.9.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-error-diagnostics/2.0.9/maven-error-diagnostics-2.0.9.pom (1.7 kB at 37 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-project/2.0.9/maven-project-2.0.9.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-project/2.0.9/maven-project-2.0.9.pom (2.7 kB at 59 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact-manager/2.0.9/maven-artifact-manager-2.0.9.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact-manager/2.0.9/maven-artifact-manager-2.0.9.pom (2.7 kB at 55 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-registry/2.0.9/maven-plugin-registry-2.0.9.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-registry/2.0.9/maven-plugin-registry-2.0.9.pom (2.0 kB at 39 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-descriptor/2.0.9/maven-plugin-descriptor-2.0.9.pom
[08:03:03] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-descriptor/2.0.9/maven-plugin-descriptor-2.0.9.pom (2.1 kB at 41 kB/s)
[08:03:03] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-monitor/2.0.9/maven-monitor-2.0.9.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-monitor/2.0.9/maven-monitor-2.0.9.pom (1.3 kB at 29 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-toolchain/1.0/maven-toolchain-1.0.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-toolchain/1.0/maven-toolchain-1.0.pom (3.4 kB at 76 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-utils/0.1/maven-shared-utils-0.1.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-utils/0.1/maven-shared-utils-0.1.pom (4.0 kB at 90 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-components/18/maven-shared-components-18.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-components/18/maven-shared-components-18.pom (4.9 kB at 107 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/code/findbugs/jsr305/2.0.1/jsr305-2.0.1.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/code/findbugs/jsr305/2.0.1/jsr305-2.0.1.pom (965 B at 21 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-incremental/1.1/maven-shared-incremental-1.1.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-incremental/1.1/maven-shared-incremental-1.1.pom (4.7 kB at 103 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-components/19/maven-shared-components-19.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-components/19/maven-shared-components-19.pom (6.4 kB at 132 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-api/2.2.1/maven-plugin-api-2.2.1.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-api/2.2.1/maven-plugin-api-2.2.1.pom (1.5 kB at 32 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven/2.2.1/maven-2.2.1.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven/2.2.1/maven-2.2.1.pom (22 kB at 467 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/11/maven-parent-11.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/11/maven-parent-11.pom (32 kB at 705 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/apache/5/apache-5.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/apache/5/apache-5.pom (4.1 kB at 89 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-core/2.2.1/maven-core-2.2.1.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-core/2.2.1/maven-core-2.2.1.pom (12 kB at 248 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings/2.2.1/maven-settings-2.2.1.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings/2.2.1/maven-settings-2.2.1.pom (2.2 kB at 47 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model/2.2.1/maven-model-2.2.1.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model/2.2.1/maven-model-2.2.1.pom (3.2 kB at 69 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interpolation/1.11/plexus-interpolation-1.11.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interpolation/1.11/plexus-interpolation-1.11.pom (889 B at 19 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-parameter-documenter/2.2.1/maven-plugin-parameter-documenter-2.2.1.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-parameter-documenter/2.2.1/maven-plugin-parameter-documenter-2.2.1.pom (2.0 kB at 44 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/slf4j/slf4j-jdk14/1.5.6/slf4j-jdk14-1.5.6.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/slf4j/slf4j-jdk14/1.5.6/slf4j-jdk14-1.5.6.pom (1.9 kB at 42 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/slf4j/slf4j-parent/1.5.6/slf4j-parent-1.5.6.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/slf4j/slf4j-parent/1.5.6/slf4j-parent-1.5.6.pom (7.9 kB at 141 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/slf4j/slf4j-api/1.5.6/slf4j-api-1.5.6.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/slf4j/slf4j-api/1.5.6/slf4j-api-1.5.6.pom (3.0 kB at 54 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/slf4j/jcl-over-slf4j/1.5.6/jcl-over-slf4j-1.5.6.pom
[08:03:04] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/slf4j/jcl-over-slf4j/1.5.6/jcl-over-slf4j-1.5.6.pom (2.2 kB at 46 kB/s)
[08:03:04] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-profile/2.2.1/maven-profile-2.2.1.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-profile/2.2.1/maven-profile-2.2.1.pom (2.2 kB at 48 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact/2.2.1/maven-artifact-2.2.1.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact/2.2.1/maven-artifact-2.2.1.pom (1.6 kB at 35 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-repository-metadata/2.2.1/maven-repository-metadata-2.2.1.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-repository-metadata/2.2.1/maven-repository-metadata-2.2.1.pom (1.9 kB at 42 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-error-diagnostics/2.2.1/maven-error-diagnostics-2.2.1.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-error-diagnostics/2.2.1/maven-error-diagnostics-2.2.1.pom (1.7 kB at 38 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-project/2.2.1/maven-project-2.2.1.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-project/2.2.1/maven-project-2.2.1.pom (2.8 kB at 46 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact-manager/2.2.1/maven-artifact-manager-2.2.1.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact-manager/2.2.1/maven-artifact-manager-2.2.1.pom (3.1 kB at 69 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/backport-util-concurrent/backport-util-concurrent/3.1/backport-util-concurrent-3.1.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/backport-util-concurrent/backport-util-concurrent/3.1/backport-util-concurrent-3.1.pom (880 B at 19 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-registry/2.2.1/maven-plugin-registry-2.2.1.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-registry/2.2.1/maven-plugin-registry-2.2.1.pom (1.9 kB at 45 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-descriptor/2.2.1/maven-plugin-descriptor-2.2.1.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-descriptor/2.2.1/maven-plugin-descriptor-2.2.1.pom (2.1 kB at 43 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-monitor/2.2.1/maven-monitor-2.2.1.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-monitor/2.2.1/maven-monitor-2.2.1.pom (1.3 kB at 27 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/plexus/plexus-sec-dispatcher/1.3/plexus-sec-dispatcher-1.3.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/plexus/plexus-sec-dispatcher/1.3/plexus-sec-dispatcher-1.3.pom (3.0 kB at 66 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/spice/spice-parent/12/spice-parent-12.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/spice/spice-parent/12/spice-parent-12.pom (6.8 kB at 133 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/forge/forge-parent/4/forge-parent-4.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/forge/forge-parent/4/forge-parent-4.pom (8.4 kB at 156 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.5.5/plexus-utils-1.5.5.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.5.5/plexus-utils-1.5.5.pom (5.1 kB at 117 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/plexus/plexus-cipher/1.4/plexus-cipher-1.4.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/plexus/plexus-cipher/1.4/plexus-cipher-1.4.pom (2.1 kB at 47 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-component-annotations/1.5.5/plexus-component-annotations-1.5.5.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-component-annotations/1.5.5/plexus-component-annotations-1.5.5.pom (815 B at 18 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-containers/1.5.5/plexus-containers-1.5.5.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-containers/1.5.5/plexus-containers-1.5.5.pom (4.2 kB at 96 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/2.0.7/plexus-2.0.7.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/2.0.7/plexus-2.0.7.pom (17 kB at 376 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-compiler-api/2.2/plexus-compiler-api-2.2.pom
[08:03:05] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-compiler-api/2.2/plexus-compiler-api-2.2.pom (865 B at 20 kB/s)
[08:03:05] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-compiler/2.2/plexus-compiler-2.2.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-compiler/2.2/plexus-compiler-2.2.pom (3.6 kB at 82 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-components/1.3.1/plexus-components-1.3.1.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-components/1.3.1/plexus-components-1.3.1.pom (3.1 kB at 70 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/3.3.1/plexus-3.3.1.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/3.3.1/plexus-3.3.1.pom (20 kB at 401 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/spice/spice-parent/17/spice-parent-17.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/spice/spice-parent/17/spice-parent-17.pom (6.8 kB at 130 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/forge/forge-parent/10/forge-parent-10.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/forge/forge-parent/10/forge-parent-10.pom (14 kB at 301 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.0.8/plexus-utils-3.0.8.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.0.8/plexus-utils-3.0.8.pom (3.1 kB at 71 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/3.2/plexus-3.2.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/3.2/plexus-3.2.pom (19 kB at 426 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-compiler-manager/2.2/plexus-compiler-manager-2.2.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-compiler-manager/2.2/plexus-compiler-manager-2.2.pom (690 B at 16 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-compiler-javac/2.2/plexus-compiler-javac-2.2.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-compiler-javac/2.2/plexus-compiler-javac-2.2.pom (769 B at 17 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-compilers/2.2/plexus-compilers-2.2.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-compilers/2.2/plexus-compilers-2.2.pom (1.2 kB at 28 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-container-default/1.5.5/plexus-container-default-1.5.5.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-container-default/1.5.5/plexus-container-default-1.5.5.pom (2.8 kB at 57 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.4.5/plexus-utils-1.4.5.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.4.5/plexus-utils-1.4.5.pom (2.3 kB at 51 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-classworlds/2.2.2/plexus-classworlds-2.2.2.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-classworlds/2.2.2/plexus-classworlds-2.2.2.pom (4.0 kB at 92 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/xbean/xbean-reflect/3.4/xbean-reflect-3.4.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/xbean/xbean-reflect/3.4/xbean-reflect-3.4.pom (2.8 kB at 62 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/xbean/xbean/3.4/xbean-3.4.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/xbean/xbean/3.4/xbean-3.4.pom (19 kB at 394 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/log4j/log4j/1.2.12/log4j-1.2.12.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/log4j/log4j/1.2.12/log4j-1.2.12.pom (145 B at 3.2 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/commons-logging/commons-logging-api/1.1/commons-logging-api-1.1.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/commons-logging/commons-logging-api/1.1/commons-logging-api-1.1.pom (5.3 kB at 119 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/collections/google-collections/1.0/google-collections-1.0.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/collections/google-collections/1.0/google-collections-1.0.pom (2.5 kB at 58 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/google/1/google-1.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/google/1/google-1.pom (1.6 kB at 35 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/junit/junit/3.8.2/junit-3.8.2.pom
[08:03:06] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/junit/junit/3.8.2/junit-3.8.2.pom (747 B at 14 kB/s)
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-api/2.0.9/maven-plugin-api-2.0.9.jar
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact/2.0.9/maven-artifact-2.0.9.jar
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.5.1/plexus-utils-1.5.1.jar
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-core/2.0.9/maven-core-2.0.9.jar
[08:03:06] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings/2.0.9/maven-settings-2.0.9.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings/2.0.9/maven-settings-2.0.9.jar (49 kB at 963 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-api/2.0.9/maven-plugin-api-2.0.9.jar (13 kB at 239 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-parameter-documenter/2.0.9/maven-plugin-parameter-documenter-2.0.9.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-profile/2.0.9/maven-profile-2.0.9.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.5.1/plexus-utils-1.5.1.jar (211 kB at 3.6 MB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model/2.0.9/maven-model-2.0.9.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact/2.0.9/maven-artifact-2.0.9.jar (89 kB at 1.5 MB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-repository-metadata/2.0.9/maven-repository-metadata-2.0.9.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-parameter-documenter/2.0.9/maven-plugin-parameter-documenter-2.0.9.jar (21 kB at 186 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-error-diagnostics/2.0.9/maven-error-diagnostics-2.0.9.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-repository-metadata/2.0.9/maven-repository-metadata-2.0.9.jar (25 kB at 208 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-project/2.0.9/maven-project-2.0.9.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model/2.0.9/maven-model-2.0.9.jar (87 kB at 740 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-registry/2.0.9/maven-plugin-registry-2.0.9.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-core/2.0.9/maven-core-2.0.9.jar (160 kB at 1.3 MB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-descriptor/2.0.9/maven-plugin-descriptor-2.0.9.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-profile/2.0.9/maven-profile-2.0.9.jar (35 kB at 292 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact-manager/2.0.9/maven-artifact-manager-2.0.9.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-error-diagnostics/2.0.9/maven-error-diagnostics-2.0.9.jar (14 kB at 86 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-monitor/2.0.9/maven-monitor-2.0.9.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-registry/2.0.9/maven-plugin-registry-2.0.9.jar (29 kB at 172 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-toolchain/1.0/maven-toolchain-1.0.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact-manager/2.0.9/maven-artifact-manager-2.0.9.jar (58 kB at 321 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-utils/0.1/maven-shared-utils-0.1.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-descriptor/2.0.9/maven-plugin-descriptor-2.0.9.jar (37 kB at 205 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/code/findbugs/jsr305/2.0.1/jsr305-2.0.1.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-project/2.0.9/maven-project-2.0.9.jar (122 kB at 597 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-incremental/1.1/maven-shared-incremental-1.1.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-monitor/2.0.9/maven-monitor-2.0.9.jar (10 kB at 48 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-component-annotations/1.5.5/plexus-component-annotations-1.5.5.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-toolchain/1.0/maven-toolchain-1.0.jar (33 kB at 148 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-compiler-api/2.2/plexus-compiler-api-2.2.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/code/findbugs/jsr305/2.0.1/jsr305-2.0.1.jar (32 kB at 133 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-compiler-manager/2.2/plexus-compiler-manager-2.2.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-utils/0.1/maven-shared-utils-0.1.jar (155 kB at 623 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-compiler-javac/2.2/plexus-compiler-javac-2.2.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-incremental/1.1/maven-shared-incremental-1.1.jar (14 kB at 50 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-container-default/1.5.5/plexus-container-default-1.5.5.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-component-annotations/1.5.5/plexus-component-annotations-1.5.5.jar (4.2 kB at 16 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-classworlds/2.2.2/plexus-classworlds-2.2.2.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-compiler-api/2.2/plexus-compiler-api-2.2.jar (25 kB at 91 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/xbean/xbean-reflect/3.4/xbean-reflect-3.4.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-compiler-javac/2.2/plexus-compiler-javac-2.2.jar (19 kB at 64 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/log4j/log4j/1.2.12/log4j-1.2.12.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-compiler-manager/2.2/plexus-compiler-manager-2.2.jar (4.6 kB at 15 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/commons-logging/commons-logging-api/1.1/commons-logging-api-1.1.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-classworlds/2.2.2/plexus-classworlds-2.2.2.jar (46 kB at 144 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/collections/google-collections/1.0/google-collections-1.0.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/xbean/xbean-reflect/3.4/xbean-reflect-3.4.jar (134 kB at 396 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/junit/junit/3.8.2/junit-3.8.2.jar
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/commons-logging/commons-logging-api/1.1/commons-logging-api-1.1.jar (45 kB at 121 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-container-default/1.5.5/plexus-container-default-1.5.5.jar (217 kB at 558 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/collections/google-collections/1.0/google-collections-1.0.jar (640 kB at 1.6 MB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/log4j/log4j/1.2.12/log4j-1.2.12.jar (358 kB at 889 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/junit/junit/3.8.2/junit-3.8.2.jar (121 kB at 299 kB/s)
[08:03:07] :	 [Step 1/1] [INFO] Changes detected - recompiling the module!
[08:03:07]W:	 [Step 1/1] [WARNING] File encoding has not been set, using platform encoding UTF-8, i.e. build is platform dependent!
[08:03:07] :	 [Step 1/1] [INFO] Compiling 2 source files to /opt/buildagent/work/8e44ef381d17132e/target/classes
[08:03:08] :	 [Step 1/1] [INFO] 
[08:03:08] :	 [Step 1/1] [INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ plaindoll ---
[08:03:08]W:	 [Step 1/1] [WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[08:03:08] :	 [Step 1/1] [INFO] skip non existing resourceDirectory /opt/buildagent/work/8e44ef381d17132e/src/test/resources
[08:03:08] :	 [Step 1/1] [INFO] 
[08:03:08] :	 [Step 1/1] [INFO] --- maven-compiler-plugin:3.1:testCompile (default-testCompile) @ plaindoll ---
[08:03:08] :	 [Step 1/1] [INFO] Changes detected - recompiling the module!
[08:03:08]W:	 [Step 1/1] [WARNING] File encoding has not been set, using platform encoding UTF-8, i.e. build is platform dependent!
[08:03:08] :	 [Step 1/1] [INFO] Compiling 1 source file to /opt/buildagent/work/8e44ef381d17132e/target/test-classes
[08:03:08] :	 [Step 1/1] [INFO] 
[08:03:08] :	 [Step 1/1] [INFO] --- maven-surefire-plugin:2.12.4:test (default-test) @ plaindoll ---
[08:03:08] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/surefire-booter/2.12.4/surefire-booter-2.12.4.pom
[08:03:08] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/surefire-booter/2.12.4/surefire-booter-2.12.4.pom (3.0 kB at 66 kB/s)
[08:03:08] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/surefire-api/2.12.4/surefire-api-2.12.4.pom
[08:03:08] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/surefire-api/2.12.4/surefire-api-2.12.4.pom (2.5 kB at 55 kB/s)
[08:03:08] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/maven-surefire-common/2.12.4/maven-surefire-common-2.12.4.pom
[08:03:08] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/maven-surefire-common/2.12.4/maven-surefire-common-2.12.4.pom (5.5 kB at 123 kB/s)
[08:03:08] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugin-tools/maven-plugin-annotations/3.1/maven-plugin-annotations-3.1.pom
[08:03:08] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugin-tools/maven-plugin-annotations/3.1/maven-plugin-annotations-3.1.pom (1.6 kB at 37 kB/s)
[08:03:08] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugin-tools/maven-plugin-tools/3.1/maven-plugin-tools-3.1.pom
[08:03:08] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugin-tools/maven-plugin-tools/3.1/maven-plugin-tools-3.1.pom (16 kB at 368 kB/s)
[08:03:08] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/reporting/maven-reporting-api/2.0.9/maven-reporting-api-2.0.9.pom
[08:03:08] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/reporting/maven-reporting-api/2.0.9/maven-reporting-api-2.0.9.pom (1.8 kB at 35 kB/s)
[08:03:08] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/reporting/maven-reporting/2.0.9/maven-reporting-2.0.9.pom
[08:03:08] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/reporting/maven-reporting/2.0.9/maven-reporting-2.0.9.pom (1.5 kB at 31 kB/s)
[08:03:08] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-toolchain/2.0.9/maven-toolchain-2.0.9.pom
[08:03:08] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-toolchain/2.0.9/maven-toolchain-2.0.9.pom (3.5 kB at 76 kB/s)
[08:03:08] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/commons/commons-lang3/3.1/commons-lang3-3.1.pom
[08:03:08] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/commons/commons-lang3/3.1/commons-lang3-3.1.pom (17 kB at 356 kB/s)
[08:03:08] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/commons/commons-parent/22/commons-parent-22.pom
[08:03:08] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/commons/commons-parent/22/commons-parent-22.pom (42 kB at 953 kB/s)
[08:03:08] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/apache/9/apache-9.pom
[08:03:08] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/apache/9/apache-9.pom (15 kB at 345 kB/s)
[08:03:08] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-common-artifact-filters/1.3/maven-common-artifact-filters-1.3.pom
[08:03:08] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-common-artifact-filters/1.3/maven-common-artifact-filters-1.3.pom (3.7 kB at 84 kB/s)
[08:03:08] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-components/12/maven-shared-components-12.pom
[08:03:08] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-components/12/maven-shared-components-12.pom (9.3 kB at 217 kB/s)
[08:03:08] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/13/maven-parent-13.pom
[08:03:09] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/13/maven-parent-13.pom (23 kB at 503 kB/s)
[08:03:09] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/apache/6/apache-6.pom
[08:03:09] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/apache/6/apache-6.pom (13 kB at 284 kB/s)
[08:03:09] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-container-default/1.0-alpha-9/plexus-container-default-1.0-alpha-9.pom
[08:03:09] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-container-default/1.0-alpha-9/plexus-container-default-1.0-alpha-9.pom (1.2 kB at 25 kB/s)
[08:03:09] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/surefire-booter/2.12.4/surefire-booter-2.12.4.jar
[08:03:09] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/surefire-api/2.12.4/surefire-api-2.12.4.jar
[08:03:09] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/maven-surefire-common/2.12.4/maven-surefire-common-2.12.4.jar
[08:03:09] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/commons/commons-lang3/3.1/commons-lang3-3.1.jar
[08:03:09] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-common-artifact-filters/1.3/maven-common-artifact-filters-1.3.jar
[08:03:09] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/surefire-booter/2.12.4/surefire-booter-2.12.4.jar (35 kB at 680 kB/s)
[08:03:09] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.0.8/plexus-utils-3.0.8.jar
[08:03:09] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/maven-surefire-common/2.12.4/maven-surefire-common-2.12.4.jar (263 kB at 5.1 MB/s)
[08:03:09] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/reporting/maven-reporting-api/2.0.9/maven-reporting-api-2.0.9.jar
[08:03:09] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-common-artifact-filters/1.3/maven-common-artifact-filters-1.3.jar (31 kB at 565 kB/s)
[08:03:09] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-toolchain/2.0.9/maven-toolchain-2.0.9.jar
[08:03:09] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/surefire-api/2.12.4/surefire-api-2.12.4.jar (118 kB at 2.0 MB/s)
[08:03:09] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugin-tools/maven-plugin-annotations/3.1/maven-plugin-annotations-3.1.jar
[08:03:09] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.0.8/plexus-utils-3.0.8.jar (232 kB at 2.4 MB/s)
[08:03:09] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-toolchain/2.0.9/maven-toolchain-2.0.9.jar (38 kB at 380 kB/s)
[08:03:09] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugin-tools/maven-plugin-annotations/3.1/maven-plugin-annotations-3.1.jar (14 kB at 137 kB/s)
[08:03:09] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/reporting/maven-reporting-api/2.0.9/maven-reporting-api-2.0.9.jar (10 kB at 97 kB/s)
[08:03:09] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/commons/commons-lang3/3.1/commons-lang3-3.1.jar (316 kB at 2.7 MB/s)
[08:03:09] :	 [Step 1/1] [INFO] Surefire report directory: /opt/buildagent/work/8e44ef381d17132e/target/surefire-reports
[08:03:09] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/surefire-junit4/2.12.4/surefire-junit4-2.12.4.pom
[08:03:09] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/surefire-junit4/2.12.4/surefire-junit4-2.12.4.pom (2.4 kB at 52 kB/s)
[08:03:09] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/surefire-providers/2.12.4/surefire-providers-2.12.4.pom
[08:03:09] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/surefire-providers/2.12.4/surefire-providers-2.12.4.pom (2.3 kB at 52 kB/s)
[08:03:09] :	 [Step 1/1] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/surefire-junit4/2.12.4/surefire-junit4-2.12.4.jar
[08:03:09] :	 [Step 1/1] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/surefire/surefire-junit4/2.12.4/surefire-junit4-2.12.4.jar (37 kB at 684 kB/s)
[08:03:09] :	 [Step 1/1] 
[08:03:09] :	 [Step 1/1] -------------------------------------------------------
[08:03:09] :	 [Step 1/1]  T E S T S
[08:03:09] :	 [Step 1/1] -------------------------------------------------------
[08:03:09] :	 [Step 1/1] Running plaindoll.WelcomerTest
[08:03:09] :	 [Step 1/1] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.136 sec
[08:03:10] :	 [Step 1/1] 
[08:03:10] :	 [Step 1/1] Results :
[08:03:10] :	 [Step 1/1] 
[08:03:10] :	 [Step 1/1] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0
[08:03:10] :	 [Step 1/1] 
[08:03:10] :	 [Step 1/1] [Maven Watcher] 
[08:03:10]i:	 [Step 1/1] ##teamcity[projectFinished tc:tags='tc:internal' projectId='org.netology:plaindoll:jar:0.0.1']
[08:03:10] :	 [Step 1/1] [INFO] ------------------------------------------------------------------------
[08:03:10] :	 [Step 1/1] [INFO] BUILD SUCCESS
[08:03:10] :	 [Step 1/1] [INFO] ------------------------------------------------------------------------
[08:03:10] :	 [Step 1/1] [INFO] Total time:  13.075 s
[08:03:10] :	 [Step 1/1] [INFO] Finished at: 2023-09-27T09:03:10+01:00
[08:03:10] :	 [Step 1/1] [INFO] ------------------------------------------------------------------------
[08:03:10] :	 [Step 1/1] [Maven Watcher] building report document...
[08:03:10] :	 [Step 1/1] [Maven Watcher] building report document done
[08:03:10] :	 [Step 1/1] [Maven Watcher] writing report to /opt/buildagent/temp/buildTmp/maven-build-info.xml
[08:03:10] :	 [Step 1/1] [Maven Watcher] done writing report
[08:03:10] :	 [Step 1/1] Process exited with code 0
[08:03:10] :	 [Step 1/1] Publishing artifacts
[08:03:10] :		 [Publishing artifacts] Collecting files to publish: [/opt/buildagent/temp/buildTmp/.tc-maven-bi/maven-build-info.xml.gz => .teamcity]
[08:03:10] :		 [Publishing artifacts] Publishing 1 file using [WebPublisher]: /opt/buildagent/temp/buildTmp/.tc-maven-bi/maven-build-info.xml.gz => .teamcity
[08:03:10] :		 [Publishing artifacts] Publishing 1 file using [ArtifactsCachePublisherImpl]: /opt/buildagent/temp/buildTmp/.tc-maven-bi/maven-build-info.xml.gz => .teamcity
[08:03:10]i:		 [Publishing artifacts] Will publish 1 artifact(s) to TeamCity node with id MAIN_SERVER
[08:03:10] :	 [Step 1/1] Waiting for 2 service processes to complete
[08:03:10]i:	 [Step 1/1] plaindoll.WelcomerTest
[08:03:10]i:		 [plaindoll.WelcomerTest] welcomerSaysFarewell
[08:03:10]i:		 [plaindoll.WelcomerTest] welcomerSaysHunter
[08:03:10]i:		 [plaindoll.WelcomerTest] welcomerSaysSilver
[08:03:10]i:		 [plaindoll.WelcomerTest] welcomerSaysSomething
[08:03:10]i:		 [plaindoll.WelcomerTest] welcomerSaysWelcome
[08:03:10] :	 [Step 1/1] Surefire report watcher
[08:03:10] :		 [Surefire report watcher] 1 report found for paths:
[08:03:10] :		 [Surefire report watcher] /opt/buildagent/work/8e44ef381d17132e/target/surefire-reports/TEST-*.xml
[08:03:10] :		 [Surefire report watcher] Successfully parsed
[08:03:10] :			 [Successfully parsed] 1 report
[08:03:10] :			 [Successfully parsed] target/surefire-reports/TEST-plaindoll.WelcomerTest.xml
[08:03:10]i: Stopping performance monitoring process
[08:03:14]i: Performance monitoring process stopped
[08:03:14]i: Publishing performance monitoring build stages data
[08:03:14] : Publishing artifacts
[08:03:14] :	 [Publishing artifacts] Collecting files to publish: [/opt/buildagent/system/perfmon/temp/1/perfmon.csv=>.teamcity/perfmon/, /opt/buildagent/temp/agentTmp/build_stages.txt=>.teamcity/perfmon/]
[08:03:14] :	 [Publishing artifacts] Publishing 2 files using [WebPublisher]: /opt/buildagent/system/perfmon/temp/1/perfmon.csv, /opt/buildagent/temp/agentTmp/build_stages.txt => .teamcity/perfmon
[08:03:14] :	 [Publishing artifacts] Publishing 2 files using [ArtifactsCachePublisherImpl]: /opt/buildagent/system/perfmon/temp/1/perfmon.csv, /opt/buildagent/temp/agentTmp/build_stages.txt => .teamcity/perfmon
[08:03:14]i:	 [Publishing artifacts] Will publish 2 artifact(s) to TeamCity node with id MAIN_SERVER
[08:03:14] : Publishing internal artifacts
[08:03:14] :	 [Publishing internal artifacts] Publishing 1 file using [WebPublisher]
[08:03:14] :	 [Publishing internal artifacts] Publishing 1 file using [ArtifactsCachePublisherImpl]
[08:03:14]i:	 [Publishing internal artifacts] Will publish 1 artifact(s) to TeamCity node with id MAIN_SERVER
[08:03:14] : Build finished

```

</details>


4. Поменяйте условия сборки: если сборка по ветке `master`, то должен происходит `mvn clean deploy`, иначе `mvn clean test`.
![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/2c88e45b-6bbe-427a-96c3-6f0e42b67de8)



5. Для deploy будет необходимо загрузить [settings.xml](./teamcity/settings.xml) в набор конфигураций maven у teamcity, предварительно записав туда креды для подключения к nexus.
6. В pom.xml необходимо поменять ссылки на репозиторий и nexus.
7. Запустите сборку по master, убедитесь, что всё прошло успешно и артефакт появился в nexus.

![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/f1919a18-9af9-4e10-bcff-5b19398aceae)

<details><summary>Logs</summary>
  
```
Build 'netology / Build' #3, default branch 'master'
Triggered 2023-09-27 08:37:49 by 'admin'
Started 2023-09-27 08:37:53 on agent 'ip_130.193.37.216'
Finished 2023-09-27 08:38:13 with status NORMAL 'Tests passed: 5'
VCS revisions: 'Netology_HttpsGithubComSemenAmbarnovExampleTeamcityGitRefsHeadsMaster' (Git, instance id 1): '817aad0ca811ebb403effd538c0a52542a6414c8' (branch: 'refs/heads/master')
TeamCity URL http://localhost:8111/viewLog.html?buildId=3&buildTypeId=Netology_Build 
TeamCity server version is 2023.05.4 (build 129421), server timezone: GMT (UTC)

[08:37:49]W: bt1 (24s)
[08:37:49]i: TeamCity server version is 2023.05.4 (build 129421)
[08:37:49] : The build is removed from the queue to be prepared for the start
[08:37:49] : Collecting changes in 1 VCS root (1s)
[08:37:49] :	 [Collecting changes in 1 VCS root] VCS Root details
[08:37:49] :		 [VCS Root details] "https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master" {instance id=1, parent internal id=1, parent id=Netology_HttpsGithubComSemenAmbarnovExampleTeamcityGitRefsHeadsMaster, description: "https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master"}
[08:37:49]i:	 [Collecting changes in 1 VCS root] Loading current repository state for VCS root 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master' (1s)
[08:37:49]i:		 [Loading current repository state for VCS root 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'] VCS root 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master': git -c core.askpass=/opt/teamcity/temp/pass10809212607208947582 -c credential.helper= ls-remote origin
[08:37:50]i:	 [Collecting changes in 1 VCS root] Detecting changes in VCS root 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master' (used in 'Build')
[08:37:50]i:	 [Collecting changes in 1 VCS root] Will collect changes for 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master' starting from revision 817aad0ca811ebb403effd538c0a52542a6414c8
[08:37:50] :	 [Collecting changes in 1 VCS root] Compute revision for 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'
[08:37:50] :		 [Compute revision for 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'] Upper limit revision: 817aad0ca811ebb403effd538c0a52542a6414c8
[08:37:50]i:		 [Compute revision for 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'] MaxModId = 1
[08:37:50] :		 [Compute revision for 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'] The first revision that was detected in the branch refs/heads/master: db1c910a3f0442d9a9b9c3411db8c9c298019bf1
[08:37:50] :		 [Compute revision for 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'] The first revision that was detected in the branch refs/heads/master after the last change of the VCS root or checkout rules: db1c910a3f0442d9a9b9c3411db8c9c298019bf1
[08:37:50] :		 [Compute revision for 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'] Latest commit attached to build configuration (with id <= 1): 817aad0ca811ebb403effd538c0a52542a6414c8
[08:37:50] :		 [Compute revision for 'https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master'] Computed revision: 817aad0ca811ebb403effd538c0a52542a6414c8
[08:37:50] : Starting the build on the agent "ip_130.193.37.216"
[08:37:53]i: Agent time zone: Europe/London
[08:37:53]i: Agent is running under JRE: 17.0.7+7-LTS
[08:37:53] : Updating tools for build
[08:37:53] :	 [Updating tools for build] Found 1 tool used by the build: maven3_6
[08:37:53] :	 [Updating tools for build] All used tools are up-to-date
[08:37:53] : Clearing temporary directory: /opt/buildagent/temp/buildTmp
[08:37:53]i: Preparing performance monitoring data directory: /opt/buildagent/system/perfmon
[08:37:53]i: Performance monitor is using command line: [perl, /opt/buildagent/system/perfmon/scripts/vmstatlinux.pl, /opt/buildagent/system/perfmon/temp/3/perfmon.csv, 1000]
[08:37:53]i: Starting performance monitoring process
[08:37:53]i: Performance monitoring process started
[08:37:53] : Publishing internal artifacts
[08:37:53] :	 [Publishing internal artifacts] Publishing 1 file using [WebPublisher]
[08:37:53] :	 [Publishing internal artifacts] Publishing 1 file using [ArtifactsCachePublisherImpl]
[08:37:53]i:	 [Publishing internal artifacts] Will publish 1 artifact(s) to TeamCity node with id MAIN_SERVER
[08:37:53] : Using vcs information from agent file: 8e44ef381d17132e.xml
[08:37:53] : Checkout directory: /opt/buildagent/work/8e44ef381d17132e
[08:37:53] : Updating sources: auto checkout (on agent) (1s)
[08:37:53] :	 [Updating sources] Will use agent side checkout
[08:37:53] :	 [Updating sources] VCS Root: https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master (1s)
[08:37:53] :		 [VCS Root: https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master] revision: 817aad0ca811ebb403effd538c0a52542a6414c8
[08:37:53]i:		 [VCS Root: https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master] Mirrors automatically enabled
[08:37:53] :		 [VCS Root: https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master] Git version: 2.42.0.0
[08:37:53] :		 [VCS Root: https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master] Update git mirror (/opt/buildagent/system/git/git-DBA0D768.git) (1s)
[08:37:53] :			 [Update git mirror (/opt/buildagent/system/git/git-DBA0D768.git)] /usr/bin/git config http.sslCAInfo
[08:37:53] :			 [Update git mirror (/opt/buildagent/system/git/git-DBA0D768.git)] /usr/bin/git show-ref
[08:37:53] :			 [Update git mirror (/opt/buildagent/system/git/git-DBA0D768.git)] /usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass9215857802574156309 -c credential.helper= ls-remote origin
[08:37:54] :			 [Update git mirror (/opt/buildagent/system/git/git-DBA0D768.git)] /usr/bin/git show-ref refs/heads/master
[08:37:54] :			 [Update git mirror (/opt/buildagent/system/git/git-DBA0D768.git)] /usr/bin/git log -n1 --pretty=format:%H%x20%s 817aad0ca811ebb403effd538c0a52542a6414c8 --
[08:37:54] :			 [Update git mirror (/opt/buildagent/system/git/git-DBA0D768.git)] No 'git fetch' required: commit '817aad0ca811ebb403effd538c0a52542a6414c8' is in the local repository clone pointed by 'refs/heads/master'.
[08:37:54] :			 [Update git mirror (/opt/buildagent/system/git/git-DBA0D768.git)] /usr/bin/git pack-refs --all
[08:37:54] :		 [VCS Root: https://github.com/SemenAmbarnov/example-teamcity.git#refs/heads/master] Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)
[08:37:54] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git rev-parse --is-shallow-repository
[08:37:54] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git config lfs.storage /opt/buildagent/system/git/git-DBA0D768.git/lfs
[08:37:54] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git config core.sparseCheckout true
[08:37:54] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git config http.sslCAInfo
[08:37:54] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git show-ref
[08:37:54] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git show-ref refs/remotes/origin/master
[08:37:54] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git log -n1 --pretty=format:%H%x20%s 817aad0ca811ebb403effd538c0a52542a6414c8 --
[08:37:54] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] No 'git fetch' required: commit '817aad0ca811ebb403effd538c0a52542a6414c8' is in the local repository clone pointed by 'refs/remotes/origin/master'.
[08:37:54] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git branch
[08:37:54] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git -c core.askpass=/opt/buildagent/temp/buildTmp/pass16505570040027386653 -c credential.helper= -c credential.helper=/opt/buildagent/temp/buildTmp/credHelper16461547102621898697.sh reset --hard 817aad0ca811ebb403effd538c0a52542a6414c8
[08:37:54] :			 [Update checkout directory (/opt/buildagent/work/8e44ef381d17132e)] /usr/bin/git branch --set-upstream-to=refs/remotes/origin/master
[08:37:54] : Build preparation done
[08:37:54]W: Step 1/2: Master(mvn clean deploy) (Maven) (15s)
[08:37:54]i:	 [Step 1/2] Build step condition "teamcity.build.branch contains master" is satisfied
[08:37:54] :	 [Step 1/2] Using predefined Maven user settings: settings.xml
[08:37:54] :	 [Step 1/2] Using predefined Maven user settings: settings.xml
[08:37:54] :	 [Step 1/2] Initial M2_HOME not set
[08:37:54] :	 [Step 1/2] Current M2_HOME = /opt/buildagent/tools/maven3_6
[08:37:54] :	 [Step 1/2] PATH = /opt/buildagent/tools/maven3_6/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
[08:37:54] :	 [Step 1/2] Using watcher: /opt/buildagent/plugins/mavenPlugin/maven-watcher-jdk17/maven-watcher-agent.jar
[08:37:54] :	 [Step 1/2] Using agent local repository at /opt/buildagent/system/jetbrains.maven.runner/maven.repo.local
[08:37:54] :	 [Step 1/2] *** Start reading the project structure ***
[08:37:54]i:	 [Step 1/2] Initial MAVEN_OPTS not set
[08:37:54]i:	 [Step 1/2] Current MAVEN_OPTS not set
[08:37:56]i:	 [Step 1/2] [INFO] Scanning for projects...
[08:37:56]i:	 [Step 1/2] [INFO] 
[08:37:56]i:	 [Step 1/2] [INFO] -----------------------< org.netology:plaindoll >-----------------------
[08:37:56]i:	 [Step 1/2] [INFO] Building plaindoll 0.0.1
[08:37:56]i:	 [Step 1/2] [INFO] --------------------------------[ jar ]---------------------------------
[08:37:56]i:	 [Step 1/2] [INFO] 
[08:37:56]i:	 [Step 1/2] [INFO] --- info-maven3-plugin:1.0.3:info (default-cli) @ plaindoll ---
[08:37:57]i:	 [Step 1/2] [INFO] ------------------------------------------------------------------------
[08:37:57]i:	 [Step 1/2] [INFO] BUILD SUCCESS
[08:37:57]i:	 [Step 1/2] [INFO] ------------------------------------------------------------------------
[08:37:57]i:	 [Step 1/2] [INFO] Total time:  0.311 s
[08:37:57]i:	 [Step 1/2] [INFO] Finished at: 2023-09-27T09:37:57+01:00
[08:37:57]i:	 [Step 1/2] [INFO] ------------------------------------------------------------------------
[08:37:57]i:	 [Step 1/2] Process exited with code 0
[08:37:57] :	 [Step 1/2] Initial MAVEN_OPTS not set
[08:37:57] :	 [Step 1/2] Current MAVEN_OPTS not set
[08:37:57] :	 [Step 1/2] Starting: /opt/java/openjdk/bin/java -Dagent.home.dir=/opt/buildagent -Dagent.name=ip_130.193.37.216 -Dagent.ownPort=9090 -Dagent.work.dir=/opt/buildagent/work -Dbuild.number=3 -Dbuild.vcs.number=817aad0ca811ebb403effd538c0a52542a6414c8 -Dbuild.vcs.number.1=817aad0ca811ebb403effd538c0a52542a6414c8 -Dbuild.vcs.number.Netology_HttpsGithubComSemenAmbarnovExampleTeamcityGitRefsHeadsMaster=817aad0ca811ebb403effd538c0a52542a6414c8 -Dclassworlds.conf=/opt/buildagent/temp/buildTmp/teamcity.m2.conf -Dcom.jetbrains.maven.watcher.report.file=/opt/buildagent/temp/buildTmp/maven-build-info.xml -Djava.io.tmpdir=/opt/buildagent/temp/buildTmp -Dmaven.home=/opt/buildagent/tools/maven3_6 -Dmaven.multiModuleProjectDirectory=/opt/buildagent/work/8e44ef381d17132e -Dteamcity.agent.cpuBenchmark=457 -Dteamcity.agent.dotnet.agent_url=http://localhost:9090/RPC2 -Dteamcity.agent.dotnet.build_id=3 -Dteamcity.auth.password=******* -Dteamcity.auth.userId=TeamCityBuildId=3 -Dteamcity.build.changedFiles.file=/opt/buildagent/temp/buildTmp/teamcity.changedFiles.txt -Dteamcity.build.checkoutDir=/opt/buildagent/work/8e44ef381d17132e -Dteamcity.build.id=3 -Dteamcity.build.properties.file=/opt/buildagent/temp/buildTmp/teamcity.build.parameters -Dteamcity.build.tempDir=/opt/buildagent/temp/buildTmp -Dteamcity.build.workingDir=/opt/buildagent/work/8e44ef381d17132e -Dteamcity.buildConfName=Build -Dteamcity.buildType.id=Netology_Build -Dteamcity.configuration.properties.file=/opt/buildagent/temp/buildTmp/teamcity.config.parameters -Dteamcity.maven.userSettings.path=/opt/buildagent/temp/buildTmp/maven_settings_5256269390012514746.xml -Dteamcity.maven.watcher.home=/opt/buildagent/plugins/mavenPlugin/maven-watcher-jdk17 -Dteamcity.projectName=netology -Dteamcity.runner.properties.file=/opt/buildagent/temp/buildTmp/teamcity.runner.parameters -Dteamcity.tests.recentlyFailedTests.file=/opt/buildagent/temp/buildTmp/teamcity.testsToRunFirst.txt -Dteamcity.version=2023.05.4 (build 129421) -Dmaven.repo.local=/opt/buildagent/system/jetbrains.maven.runner/maven.repo.local -classpath /opt/buildagent/tools/maven3_6/boot/plexus-classworlds-2.6.0.jar: org.codehaus.plexus.classworlds.launcher.Launcher -f /opt/buildagent/work/8e44ef381d17132e/pom.xml -B -s /opt/buildagent/temp/buildTmp/maven_settings_5256269390012514746.xml -Dmaven.test.failure.ignore=true clean deploy
[08:37:57] :	 [Step 1/2] in directory: /opt/buildagent/work/8e44ef381d17132e
[08:37:58] :	 [Step 1/2] [INFO] Scanning for projects...
[08:37:58] :	 [Step 1/2] [INFO] 
[08:37:58] :	 [Step 1/2] [INFO] -----------------------< org.netology:plaindoll >-----------------------
[08:37:58] :	 [Step 1/2] [INFO] Building plaindoll 0.0.1
[08:37:58] :	 [Step 1/2] [INFO] --------------------------------[ jar ]---------------------------------
[08:37:58] :	 [Step 1/2] [Maven Watcher] project started: org.netology:plaindoll:jar:0.0.1
[08:37:58] :	 [Step 1/2] org.netology:plaindoll (11s)
[08:37:58]i:		 [org.netology:plaindoll] ##teamcity[importData tc:tags='tc:internal' type='surefire' path='/opt/buildagent/work/8e44ef381d17132e/target/surefire-reports/TEST-*.xml' whenNoDataPublished='nothing' logAsInternal='true']
[08:37:58] :	 [Step 1/2] Importing data from '/opt/buildagent/work/8e44ef381d17132e/target/surefire-reports/TEST-*.xml' (not existing file) with 'surefire' processor
[08:37:58]i:		 [org.netology:plaindoll] ##teamcity[importData tc:tags='tc:internal' type='surefire' path='/opt/buildagent/work/8e44ef381d17132e/target/failsafe-reports/TEST-*.xml' whenNoDataPublished='nothing' logAsInternal='true']
[08:37:58] :	 [Step 1/2] [Maven Watcher] 
[08:37:58]i:	 [Step 1/2] ##teamcity[projectStarted tc:tags='tc:internal' projectId='org.netology:plaindoll:jar:0.0.1' groupId='org.netology' artifactId='plaindoll' testReportsDir0='/opt/buildagent/work/8e44ef381d17132e/target/surefire-reports' testReportsDir1='/opt/buildagent/work/8e44ef381d17132e/target/failsafe-reports']
[08:37:58] :	 [Step 1/2] Importing data from '/opt/buildagent/work/8e44ef381d17132e/target/failsafe-reports/TEST-*.xml' (not existing file) with 'surefire' processor
[08:37:58] :	 [Step 1/2] Surefire report watcher
[08:37:58] :		 [Surefire report watcher] Watching paths:
[08:37:58] :		 [Surefire report watcher] /opt/buildagent/work/8e44ef381d17132e/target/surefire-reports/TEST-*.xml
[08:37:58] :	 [Step 1/2] Surefire report watcher
[08:37:58] :		 [Surefire report watcher] Watching paths:
[08:37:58] :		 [Surefire report watcher] /opt/buildagent/work/8e44ef381d17132e/target/failsafe-reports/TEST-*.xml
[08:37:59] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-jar-plugin/2.4/maven-jar-plugin-2.4.pom
[08:37:59] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-jar-plugin/2.4/maven-jar-plugin-2.4.pom (5.8 kB at 14 kB/s)
[08:37:59] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-jar-plugin/2.4/maven-jar-plugin-2.4.jar
[08:37:59] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-jar-plugin/2.4/maven-jar-plugin-2.4.jar (34 kB at 382 kB/s)
[08:37:59] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-shade-plugin/3.2.4/maven-shade-plugin-3.2.4.pom
[08:37:59] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-shade-plugin/3.2.4/maven-shade-plugin-3.2.4.pom (11 kB at 189 kB/s)
[08:37:59] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-plugins/34/maven-plugins-34.pom
[08:37:59] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-plugins/34/maven-plugins-34.pom (11 kB at 170 kB/s)
[08:37:59] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/34/maven-parent-34.pom
[08:37:59] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/34/maven-parent-34.pom (43 kB at 702 kB/s)
[08:37:59] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/apache/23/apache-23.pom
[08:38:00] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/apache/23/apache-23.pom (18 kB at 259 kB/s)
[08:38:00] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-shade-plugin/3.2.4/maven-shade-plugin-3.2.4.jar
[08:38:00] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-shade-plugin/3.2.4/maven-shade-plugin-3.2.4.jar (134 kB at 1.6 MB/s)
[08:38:00] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-install-plugin/2.4/maven-install-plugin-2.4.pom
[08:38:00] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-install-plugin/2.4/maven-install-plugin-2.4.pom (6.4 kB at 130 kB/s)
[08:38:00] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-install-plugin/2.4/maven-install-plugin-2.4.jar
[08:38:00] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-install-plugin/2.4/maven-install-plugin-2.4.jar (27 kB at 528 kB/s)
[08:38:00] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-deploy-plugin/2.7/maven-deploy-plugin-2.7.pom
[08:38:00] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-deploy-plugin/2.7/maven-deploy-plugin-2.7.pom (5.6 kB at 108 kB/s)
[08:38:00] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-deploy-plugin/2.7/maven-deploy-plugin-2.7.jar
[08:38:00] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-deploy-plugin/2.7/maven-deploy-plugin-2.7.jar (27 kB at 516 kB/s)
[08:38:00] :	 [Step 1/2] [INFO] 
[08:38:00] :	 [Step 1/2] [INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ plaindoll ---
[08:38:00] :	 [Step 1/2] [INFO] Deleting /opt/buildagent/work/8e44ef381d17132e/target
[08:38:00] :	 [Step 1/2] [INFO] 
[08:38:00] :	 [Step 1/2] [INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ plaindoll ---
[08:38:00]W:	 [Step 1/2] [WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[08:38:00] :	 [Step 1/2] [INFO] skip non existing resourceDirectory /opt/buildagent/work/8e44ef381d17132e/src/main/resources
[08:38:00] :	 [Step 1/2] [INFO] 
[08:38:00] :	 [Step 1/2] [INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ plaindoll ---
[08:38:01] :	 [Step 1/2] [INFO] Changes detected - recompiling the module!
[08:38:01]W:	 [Step 1/2] [WARNING] File encoding has not been set, using platform encoding UTF-8, i.e. build is platform dependent!
[08:38:01] :	 [Step 1/2] [INFO] Compiling 2 source files to /opt/buildagent/work/8e44ef381d17132e/target/classes
[08:38:01] :	 [Step 1/2] [INFO] 
[08:38:01] :	 [Step 1/2] [INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ plaindoll ---
[08:38:01]W:	 [Step 1/2] [WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[08:38:01] :	 [Step 1/2] [INFO] skip non existing resourceDirectory /opt/buildagent/work/8e44ef381d17132e/src/test/resources
[08:38:01] :	 [Step 1/2] [INFO] 
[08:38:01] :	 [Step 1/2] [INFO] --- maven-compiler-plugin:3.1:testCompile (default-testCompile) @ plaindoll ---
[08:38:01] :	 [Step 1/2] [INFO] Changes detected - recompiling the module!
[08:38:01]W:	 [Step 1/2] [WARNING] File encoding has not been set, using platform encoding UTF-8, i.e. build is platform dependent!
[08:38:01] :	 [Step 1/2] [INFO] Compiling 1 source file to /opt/buildagent/work/8e44ef381d17132e/target/test-classes
[08:38:02] :	 [Step 1/2] [INFO] 
[08:38:02] :	 [Step 1/2] [INFO] --- maven-surefire-plugin:2.12.4:test (default-test) @ plaindoll ---
[08:38:02] :	 [Step 1/2] [INFO] Surefire report directory: /opt/buildagent/work/8e44ef381d17132e/target/surefire-reports
[08:38:02] :	 [Step 1/2] 
[08:38:02] :	 [Step 1/2] -------------------------------------------------------
[08:38:02] :	 [Step 1/2]  T E S T S
[08:38:02] :	 [Step 1/2] -------------------------------------------------------
[08:38:02] :	 [Step 1/2] Running plaindoll.WelcomerTest
[08:38:02] :	 [Step 1/2] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.103 sec
[08:38:02] :	 [Step 1/2] 
[08:38:02] :	 [Step 1/2] Results :
[08:38:02] :	 [Step 1/2] 
[08:38:02] :	 [Step 1/2] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0
[08:38:02] :	 [Step 1/2] 
[08:38:02] :	 [Step 1/2] [INFO] 
[08:38:02] :	 [Step 1/2] [INFO] --- maven-jar-plugin:2.4:jar (default-jar) @ plaindoll ---
[08:38:02] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-archiver/2.5/maven-archiver-2.5.pom
[08:38:02] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-archiver/2.5/maven-archiver-2.5.pom (4.5 kB at 81 kB/s)
[08:38:02] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-archiver/2.1/plexus-archiver-2.1.pom
[08:38:02]i:	 [Step 1/2] plaindoll.WelcomerTest
[08:38:02]i:		 [plaindoll.WelcomerTest] welcomerSaysFarewell
[08:38:02]i:		 [plaindoll.WelcomerTest] welcomerSaysHunter
[08:38:02]i:		 [plaindoll.WelcomerTest] welcomerSaysSilver
[08:38:02]i:		 [plaindoll.WelcomerTest] welcomerSaysSomething
[08:38:02]i:		 [plaindoll.WelcomerTest] welcomerSaysWelcome
[08:38:02] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-archiver/2.1/plexus-archiver-2.1.pom (2.8 kB at 53 kB/s)
[08:38:02] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-io/2.0.2/plexus-io-2.0.2.pom
[08:38:02] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-io/2.0.2/plexus-io-2.0.2.pom (1.7 kB at 35 kB/s)
[08:38:02] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-components/1.1.19/plexus-components-1.1.19.pom
[08:38:02] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-components/1.1.19/plexus-components-1.1.19.pom (2.7 kB at 56 kB/s)
[08:38:02] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/3.0.1/plexus-3.0.1.pom
[08:38:02] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/3.0.1/plexus-3.0.1.pom (19 kB at 380 kB/s)
[08:38:02] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interpolation/1.15/plexus-interpolation-1.15.pom
[08:38:03] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interpolation/1.15/plexus-interpolation-1.15.pom (1.0 kB at 18 kB/s)
[08:38:03] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/commons-lang/commons-lang/2.1/commons-lang-2.1.pom
[08:38:03] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/commons-lang/commons-lang/2.1/commons-lang-2.1.pom (9.9 kB at 191 kB/s)
[08:38:03] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/classworlds/classworlds/1.1-alpha-2/classworlds-1.1-alpha-2.jar
[08:38:03] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-archiver/2.5/maven-archiver-2.5.jar
[08:38:03] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interpolation/1.15/plexus-interpolation-1.15.jar
[08:38:03] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-archiver/2.1/plexus-archiver-2.1.jar
[08:38:03] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-io/2.0.2/plexus-io-2.0.2.jar
[08:38:03] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/classworlds/classworlds/1.1-alpha-2/classworlds-1.1-alpha-2.jar (38 kB at 481 kB/s)
[08:38:03] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/commons-lang/commons-lang/2.1/commons-lang-2.1.jar
[08:38:03] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-archiver/2.5/maven-archiver-2.5.jar (22 kB at 156 kB/s)
[08:38:03] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interpolation/1.15/plexus-interpolation-1.15.jar (60 kB at 438 kB/s)
[08:38:03] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/commons-lang/commons-lang/2.1/commons-lang-2.1.jar (208 kB at 1.6 MB/s)
[08:38:03] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-io/2.0.2/plexus-io-2.0.2.jar (58 kB at 343 kB/s)
[08:38:03] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-archiver/2.1/plexus-archiver-2.1.jar (184 kB at 1.0 MB/s)
[08:38:03] :	 [Step 1/2] [INFO] Building jar: /opt/buildagent/work/8e44ef381d17132e/target/plaindoll-0.0.1.jar
[08:38:03] :	 [Step 1/2] [INFO] 
[08:38:03] :	 [Step 1/2] [INFO] --- maven-shade-plugin:3.2.4:shade (default) @ plaindoll ---
[08:38:03] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-api/3.0/maven-plugin-api-3.0.pom
[08:38:03] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-api/3.0/maven-plugin-api-3.0.pom (2.3 kB at 40 kB/s)
[08:38:03] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven/3.0/maven-3.0.pom
[08:38:03] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven/3.0/maven-3.0.pom (22 kB at 456 kB/s)
[08:38:03] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/15/maven-parent-15.pom
[08:38:03] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/15/maven-parent-15.pom (24 kB at 348 kB/s)
[08:38:03] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model/3.0/maven-model-3.0.pom
[08:38:03] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model/3.0/maven-model-3.0.pom (3.9 kB at 64 kB/s)
[08:38:03] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/2.0.4/plexus-utils-2.0.4.pom
[08:38:03] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/2.0.4/plexus-utils-2.0.4.pom (3.3 kB at 69 kB/s)
[08:38:03] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact/3.0/maven-artifact-3.0.pom
[08:38:03] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact/3.0/maven-artifact-3.0.pom (1.9 kB at 26 kB/s)
[08:38:03] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/sisu-inject-plexus/1.4.2/sisu-inject-plexus-1.4.2.pom
[08:38:03] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/sisu-inject-plexus/1.4.2/sisu-inject-plexus-1.4.2.pom (5.4 kB at 112 kB/s)
[08:38:03] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/inject/guice-plexus/1.4.2/guice-plexus-1.4.2.pom
[08:38:03] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/inject/guice-plexus/1.4.2/guice-plexus-1.4.2.pom (3.1 kB at 67 kB/s)
[08:38:03] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/inject/guice-bean/1.4.2/guice-bean-1.4.2.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/inject/guice-bean/1.4.2/guice-bean-1.4.2.pom (2.6 kB at 49 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/sisu-inject/1.4.2/sisu-inject-1.4.2.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/sisu-inject/1.4.2/sisu-inject-1.4.2.pom (1.2 kB at 25 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/sisu-parent/1.4.2/sisu-parent-1.4.2.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/sisu-parent/1.4.2/sisu-parent-1.4.2.pom (7.8 kB at 123 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/forge/forge-parent/6/forge-parent-6.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/forge/forge-parent/6/forge-parent-6.pom (11 kB at 211 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-component-annotations/2.0.0/plexus-component-annotations-2.0.0.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-component-annotations/2.0.0/plexus-component-annotations-2.0.0.pom (750 B at 11 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-containers/2.0.0/plexus-containers-2.0.0.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-containers/2.0.0/plexus-containers-2.0.0.pom (4.8 kB at 91 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/5.1/plexus-5.1.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/5.1/plexus-5.1.pom (23 kB at 409 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-classworlds/2.2.3/plexus-classworlds-2.2.3.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-classworlds/2.2.3/plexus-classworlds-2.2.3.pom (4.0 kB at 67 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/sisu-inject-bean/1.4.2/sisu-inject-bean-1.4.2.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/sisu-inject-bean/1.4.2/sisu-inject-bean-1.4.2.pom (5.5 kB at 121 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/sisu-guice/2.1.7/sisu-guice-2.1.7.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/sisu-guice/2.1.7/sisu-guice-2.1.7.pom (11 kB at 209 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-core/3.0/maven-core-3.0.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-core/3.0/maven-core-3.0.pom (6.6 kB at 141 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings/3.0/maven-settings-3.0.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings/3.0/maven-settings-3.0.pom (1.9 kB at 40 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings-builder/3.0/maven-settings-builder-3.0.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings-builder/3.0/maven-settings-builder-3.0.pom (2.2 kB at 39 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interpolation/1.14/plexus-interpolation-1.14.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interpolation/1.14/plexus-interpolation-1.14.pom (910 B at 19 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-components/1.1.18/plexus-components-1.1.18.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-components/1.1.18/plexus-components-1.1.18.pom (5.4 kB at 88 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-repository-metadata/3.0/maven-repository-metadata-3.0.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-repository-metadata/3.0/maven-repository-metadata-3.0.pom (1.9 kB at 39 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model-builder/3.0/maven-model-builder-3.0.pom
[08:38:04] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model-builder/3.0/maven-model-builder-3.0.pom (2.2 kB at 42 kB/s)
[08:38:04] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-aether-provider/3.0/maven-aether-provider-3.0.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-aether-provider/3.0/maven-aether-provider-3.0.pom (2.5 kB at 54 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-api/1.7/aether-api-1.7.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-api/1.7/aether-api-1.7.pom (1.7 kB at 36 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-parent/1.7/aether-parent-1.7.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-parent/1.7/aether-parent-1.7.pom (7.7 kB at 158 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-util/1.7/aether-util-1.7.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-util/1.7/aether-util-1.7.pom (2.1 kB at 41 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-impl/1.7/aether-impl-1.7.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-impl/1.7/aether-impl-1.7.pom (3.7 kB at 79 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-spi/1.7/aether-spi-1.7.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-spi/1.7/aether-spi-1.7.pom (1.7 kB at 34 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.3.0/plexus-utils-3.3.0.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.3.0/plexus-utils-3.3.0.pom (5.2 kB at 110 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-artifact-transfer/0.12.0/maven-artifact-transfer-0.12.0.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-artifact-transfer/0.12.0/maven-artifact-transfer-0.12.0.pom (11 kB at 205 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-components/33/maven-shared-components-33.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-components/33/maven-shared-components-33.pom (5.1 kB at 113 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/33/maven-parent-33.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/33/maven-parent-33.pom (44 kB at 849 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/apache/21/apache-21.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/apache/21/apache-21.pom (17 kB at 372 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-common-artifact-filters/3.0.1/maven-common-artifact-filters-3.0.1.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-common-artifact-filters/3.0.1/maven-common-artifact-filters-3.0.1.pom (4.8 kB at 101 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-components/30/maven-shared-components-30.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-components/30/maven-shared-components-30.pom (4.6 kB at 94 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/30/maven-parent-30.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-parent/30/maven-parent-30.pom (41 kB at 826 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/apache/18/apache-18.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/apache/18/apache-18.pom (16 kB at 313 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-utils/3.1.0/maven-shared-utils-3.1.0.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-utils/3.1.0/maven-shared-utils-3.1.0.pom (5.0 kB at 100 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/commons-io/commons-io/2.5/commons-io-2.5.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/commons-io/commons-io/2.5/commons-io-2.5.pom (13 kB at 283 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/commons/commons-parent/39/commons-parent-39.pom
[08:38:05] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/commons/commons-parent/39/commons-parent-39.pom (62 kB at 784 kB/s)
[08:38:05] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/apache/16/apache-16.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/apache/16/apache-16.pom (15 kB at 285 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.1.1/plexus-utils-3.1.1.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.1.1/plexus-utils-3.1.1.pom (5.1 kB at 86 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/4.0/plexus-4.0.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/4.0/plexus-4.0.pom (22 kB at 439 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/commons-codec/commons-codec/1.11/commons-codec-1.11.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/commons-codec/commons-codec/1.11/commons-codec-1.11.pom (14 kB at 279 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/commons/commons-parent/42/commons-parent-42.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/commons/commons-parent/42/commons-parent-42.pom (68 kB at 1.1 MB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/slf4j/slf4j-api/1.7.5/slf4j-api-1.7.5.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/slf4j/slf4j-api/1.7.5/slf4j-api-1.7.5.pom (2.7 kB at 54 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/slf4j/slf4j-parent/1.7.5/slf4j-parent-1.7.5.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/slf4j/slf4j-parent/1.7.5/slf4j-parent-1.7.5.pom (12 kB at 251 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm/8.0/asm-8.0.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm/8.0/asm-8.0.pom (2.9 kB at 60 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/ow2/ow2/1.5/ow2-1.5.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/ow2/ow2/1.5/ow2-1.5.pom (11 kB at 255 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm-commons/8.0/asm-commons-8.0.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm-commons/8.0/asm-commons-8.0.pom (3.7 kB at 61 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm-tree/8.0/asm-tree-8.0.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm-tree/8.0/asm-tree-8.0.pom (3.1 kB at 65 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm-analysis/8.0/asm-analysis-8.0.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm-analysis/8.0/asm-analysis-8.0.pom (3.2 kB at 66 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/jdom/jdom2/2.0.6/jdom2-2.0.6.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/jdom/jdom2/2.0.6/jdom2-2.0.6.pom (4.6 kB at 90 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-dependency-tree/3.0.1/maven-dependency-tree-3.0.1.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-dependency-tree/3.0.1/maven-dependency-tree-3.0.1.pom (7.5 kB at 147 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/eclipse/aether/aether-util/0.9.0.M2/aether-util-0.9.0.M2.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/eclipse/aether/aether-util/0.9.0.M2/aether-util-0.9.0.M2.pom (2.0 kB at 40 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/eclipse/aether/aether/0.9.0.M2/aether-0.9.0.M2.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/eclipse/aether/aether/0.9.0.M2/aether-0.9.0.M2.pom (28 kB at 472 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/commons-io/commons-io/2.6/commons-io-2.6.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/commons-io/commons-io/2.6/commons-io-2.6.pom (14 kB at 280 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/vafer/jdependency/2.4.0/jdependency-2.4.0.pom
[08:38:06] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/vafer/jdependency/2.4.0/jdependency-2.4.0.pom (15 kB at 279 kB/s)
[08:38:06] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm-util/8.0/asm-util-8.0.pom
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm-util/8.0/asm-util-8.0.pom (3.7 kB at 65 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/guava/guava/28.2-android/guava-28.2-android.pom
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/guava/guava/28.2-android/guava-28.2-android.pom (11 kB at 195 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/guava/guava-parent/28.2-android/guava-parent-28.2-android.pom
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/guava/guava-parent/28.2-android/guava-parent-28.2-android.pom (13 kB at 235 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/guava/failureaccess/1.0.1/failureaccess-1.0.1.pom
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/guava/failureaccess/1.0.1/failureaccess-1.0.1.pom (2.4 kB at 46 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/guava/guava-parent/26.0-android/guava-parent-26.0-android.pom
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/guava/guava-parent/26.0-android/guava-parent-26.0-android.pom (10 kB at 221 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/oss/oss-parent/9/oss-parent-9.pom
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/oss/oss-parent/9/oss-parent-9.pom (6.6 kB at 103 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/guava/listenablefuture/9999.0-empty-to-avoid-conflict-with-guava/listenablefuture-9999.0-empty-to-avoid-conflict-with-guava.pom
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/guava/listenablefuture/9999.0-empty-to-avoid-conflict-with-guava/listenablefuture-9999.0-empty-to-avoid-conflict-with-guava.pom (2.3 kB at 50 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/code/findbugs/jsr305/3.0.2/jsr305-3.0.2.pom
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/code/findbugs/jsr305/3.0.2/jsr305-3.0.2.pom (4.3 kB at 97 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/oss/oss-parent/7/oss-parent-7.pom
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/oss/oss-parent/7/oss-parent-7.pom (4.8 kB at 93 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/checkerframework/checker-compat-qual/2.5.5/checker-compat-qual-2.5.5.pom
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/checkerframework/checker-compat-qual/2.5.5/checker-compat-qual-2.5.5.pom (2.7 kB at 60 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/errorprone/error_prone_annotations/2.3.4/error_prone_annotations-2.3.4.pom
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/errorprone/error_prone_annotations/2.3.4/error_prone_annotations-2.3.4.pom (2.1 kB at 38 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/errorprone/error_prone_parent/2.3.4/error_prone_parent-2.3.4.pom
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/errorprone/error_prone_parent/2.3.4/error_prone_parent-2.3.4.pom (5.4 kB at 115 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/j2objc/j2objc-annotations/1.3/j2objc-annotations-1.3.pom
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/j2objc/j2objc-annotations/1.3/j2objc-annotations-1.3.pom (2.8 kB at 64 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/commons/commons-lang3/3.7/commons-lang3-3.7.pom
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/commons/commons-lang3/3.7/commons-lang3-3.7.pom (28 kB at 599 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-api/3.0/maven-plugin-api-3.0.jar
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/sisu-inject-plexus/1.4.2/sisu-inject-plexus-1.4.2.jar
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/sisu-inject-bean/1.4.2/sisu-inject-bean-1.4.2.jar
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/sisu-guice/2.1.7/sisu-guice-2.1.7-noaop.jar
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model/3.0/maven-model-3.0.jar
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-plugin-api/3.0/maven-plugin-api-3.0.jar (49 kB at 589 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-core/3.0/maven-core-3.0.jar
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/sisu-inject-bean/1.4.2/sisu-inject-bean-1.4.2.jar (153 kB at 1.4 MB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings/3.0/maven-settings-3.0.jar
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/sisu-inject-plexus/1.4.2/sisu-inject-plexus-1.4.2.jar (202 kB at 1.7 MB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings-builder/3.0/maven-settings-builder-3.0.jar
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/sisu/sisu-guice/2.1.7/sisu-guice-2.1.7-noaop.jar (472 kB at 3.6 MB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-repository-metadata/3.0/maven-repository-metadata-3.0.jar
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model/3.0/maven-model-3.0.jar (165 kB at 1.2 MB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model-builder/3.0/maven-model-builder-3.0.jar
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings/3.0/maven-settings-3.0.jar (47 kB at 267 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-aether-provider/3.0/maven-aether-provider-3.0.jar
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-settings-builder/3.0/maven-settings-builder-3.0.jar (38 kB at 213 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-impl/1.7/aether-impl-1.7.jar
[08:38:07] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-repository-metadata/3.0/maven-repository-metadata-3.0.jar (30 kB at 155 kB/s)
[08:38:07] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-spi/1.7/aether-spi-1.7.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-model-builder/3.0/maven-model-builder-3.0.jar (148 kB at 691 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-api/1.7/aether-api-1.7.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-spi/1.7/aether-spi-1.7.jar (14 kB at 56 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-util/1.7/aether-util-1.7.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-aether-provider/3.0/maven-aether-provider-3.0.jar (51 kB at 210 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interpolation/1.14/plexus-interpolation-1.14.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-impl/1.7/aether-impl-1.7.jar (106 kB at 430 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-classworlds/2.2.3/plexus-classworlds-2.2.3.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-api/1.7/aether-api-1.7.jar (74 kB at 273 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-core/3.0/maven-core-3.0.jar (527 kB at 1.9 MB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-component-annotations/2.0.0/plexus-component-annotations-2.0.0.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/plexus/plexus-sec-dispatcher/1.3/plexus-sec-dispatcher-1.3.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-interpolation/1.14/plexus-interpolation-1.14.jar (61 kB at 208 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/sonatype/plexus/plexus-cipher/1.4/plexus-cipher-1.4.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/aether/aether-util/1.7/aether-util-1.7.jar (108 kB at 361 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact/3.0/maven-artifact-3.0.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-classworlds/2.2.3/plexus-classworlds-2.2.3.jar (46 kB at 153 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.3.0/plexus-utils-3.3.0.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-component-annotations/2.0.0/plexus-component-annotations-2.0.0.jar (4.2 kB at 13 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-artifact-transfer/0.12.0/maven-artifact-transfer-0.12.0.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/plexus/plexus-sec-dispatcher/1.3/plexus-sec-dispatcher-1.3.jar (29 kB at 90 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-common-artifact-filters/3.0.1/maven-common-artifact-filters-3.0.1.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/sonatype/plexus/plexus-cipher/1.4/plexus-cipher-1.4.jar (13 kB at 40 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-utils/3.1.0/maven-shared-utils-3.1.0.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/maven-artifact/3.0/maven-artifact-3.0.jar (52 kB at 150 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/commons-codec/commons-codec/1.11/commons-codec-1.11.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-common-artifact-filters/3.0.1/maven-common-artifact-filters-3.0.1.jar (61 kB at 165 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/slf4j/slf4j-api/1.7.5/slf4j-api-1.7.5.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.3.0/plexus-utils-3.3.0.jar (263 kB at 689 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm/8.0/asm-8.0.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-artifact-transfer/0.12.0/maven-artifact-transfer-0.12.0.jar (120 kB at 311 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm-commons/8.0/asm-commons-8.0.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-shared-utils/3.1.0/maven-shared-utils-3.1.0.jar (164 kB at 410 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm-tree/8.0/asm-tree-8.0.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/slf4j/slf4j-api/1.7.5/slf4j-api-1.7.5.jar (26 kB at 60 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm-analysis/8.0/asm-analysis-8.0.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/commons-codec/commons-codec/1.11/commons-codec-1.11.jar (335 kB at 756 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/jdom/jdom2/2.0.6/jdom2-2.0.6.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm/8.0/asm-8.0.jar (122 kB at 267 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-dependency-tree/3.0.1/maven-dependency-tree-3.0.1.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm-tree/8.0/asm-tree-8.0.jar (53 kB at 113 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/eclipse/aether/aether-util/0.9.0.M2/aether-util-0.9.0.M2.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm-commons/8.0/asm-commons-8.0.jar (72 kB at 152 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/commons-io/commons-io/2.6/commons-io-2.6.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm-analysis/8.0/asm-analysis-8.0.jar (33 kB at 67 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/vafer/jdependency/2.4.0/jdependency-2.4.0.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/jdom/jdom2/2.0.6/jdom2-2.0.6.jar (305 kB at 593 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm-util/8.0/asm-util-8.0.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/shared/maven-dependency-tree/3.0.1/maven-dependency-tree-3.0.1.jar (37 kB at 71 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/guava/guava/28.2-android/guava-28.2-android.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/eclipse/aether/aether-util/0.9.0.M2/aether-util-0.9.0.M2.jar (134 kB at 254 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/guava/failureaccess/1.0.1/failureaccess-1.0.1.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/commons-io/commons-io/2.6/commons-io-2.6.jar (215 kB at 402 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/guava/listenablefuture/9999.0-empty-to-avoid-conflict-with-guava/listenablefuture-9999.0-empty-to-avoid-conflict-with-guava.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/ow2/asm/asm-util/8.0/asm-util-8.0.jar (85 kB at 151 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/code/findbugs/jsr305/3.0.2/jsr305-3.0.2.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/guava/failureaccess/1.0.1/failureaccess-1.0.1.jar (4.6 kB at 8.1 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/checkerframework/checker-compat-qual/2.5.5/checker-compat-qual-2.5.5.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/vafer/jdependency/2.4.0/jdependency-2.4.0.jar (180 kB at 314 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/errorprone/error_prone_annotations/2.3.4/error_prone_annotations-2.3.4.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/guava/listenablefuture/9999.0-empty-to-avoid-conflict-with-guava/listenablefuture-9999.0-empty-to-avoid-conflict-with-guava.jar (2.2 kB at 3.8 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/com/google/j2objc/j2objc-annotations/1.3/j2objc-annotations-1.3.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/code/findbugs/jsr305/3.0.2/jsr305-3.0.2.jar (20 kB at 33 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/apache/commons/commons-lang3/3.7/commons-lang3-3.7.jar
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/errorprone/error_prone_annotations/2.3.4/error_prone_annotations-2.3.4.jar (14 kB at 22 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/checkerframework/checker-compat-qual/2.5.5/checker-compat-qual-2.5.5.jar (5.9 kB at 9.5 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/j2objc/j2objc-annotations/1.3/j2objc-annotations-1.3.jar (8.8 kB at 14 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/commons/commons-lang3/3.7/commons-lang3-3.7.jar (500 kB at 756 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/com/google/guava/guava/28.2-android/guava-28.2-android.jar (2.6 MB at 3.4 MB/s)
[08:38:08] :	 [Step 1/2] [INFO] Replacing original artifact with shaded artifact.
[08:38:08] :	 [Step 1/2] [INFO] Replacing /opt/buildagent/work/8e44ef381d17132e/target/plaindoll-0.0.1.jar with /opt/buildagent/work/8e44ef381d17132e/target/plaindoll-0.0.1-shaded.jar
[08:38:08] :	 [Step 1/2] [INFO] 
[08:38:08] :	 [Step 1/2] [INFO] --- maven-install-plugin:2.4:install (default-install) @ plaindoll ---
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.0.5/plexus-utils-3.0.5.pom
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.0.5/plexus-utils-3.0.5.pom (2.5 kB at 32 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/3.1/plexus-3.1.pom
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/3.1/plexus-3.1.pom (19 kB at 396 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-digest/1.0/plexus-digest-1.0.pom
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-digest/1.0/plexus-digest-1.0.pom (1.1 kB at 22 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-components/1.1.7/plexus-components-1.1.7.pom
[08:38:08] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-components/1.1.7/plexus-components-1.1.7.pom (5.0 kB at 100 kB/s)
[08:38:08] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/1.0.8/plexus-1.0.8.pom
[08:38:09] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/1.0.8/plexus-1.0.8.pom (7.2 kB at 151 kB/s)
[08:38:09] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-container-default/1.0-alpha-8/plexus-container-default-1.0-alpha-8.pom
[08:38:09] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-container-default/1.0-alpha-8/plexus-container-default-1.0-alpha-8.pom (7.3 kB at 148 kB/s)
[08:38:09] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.0.5/plexus-utils-3.0.5.jar
[08:38:09] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-digest/1.0/plexus-digest-1.0.jar
[08:38:09] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-digest/1.0/plexus-digest-1.0.jar (12 kB at 228 kB/s)
[08:38:09] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/3.0.5/plexus-utils-3.0.5.jar (230 kB at 4.0 MB/s)
[08:38:09] :	 [Step 1/2] [INFO] Installing /opt/buildagent/work/8e44ef381d17132e/target/plaindoll-0.0.1.jar to /opt/buildagent/system/jetbrains.maven.runner/maven.repo.local/org/netology/plaindoll/0.0.1/plaindoll-0.0.1.jar
[08:38:09] :	 [Step 1/2] [INFO] Installing /opt/buildagent/work/8e44ef381d17132e/pom.xml to /opt/buildagent/system/jetbrains.maven.runner/maven.repo.local/org/netology/plaindoll/0.0.1/plaindoll-0.0.1.pom
[08:38:09] :	 [Step 1/2] [INFO] 
[08:38:09] :	 [Step 1/2] [INFO] --- maven-deploy-plugin:2.7:deploy (default-deploy) @ plaindoll ---
[08:38:09] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.5.6/plexus-utils-1.5.6.pom
[08:38:09] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.5.6/plexus-utils-1.5.6.pom (5.3 kB at 98 kB/s)
[08:38:09] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/1.0.12/plexus-1.0.12.pom
[08:38:09] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus/1.0.12/plexus-1.0.12.pom (9.8 kB at 213 kB/s)
[08:38:09] :	 [Step 1/2] [INFO] Downloading from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.5.6/plexus-utils-1.5.6.jar
[08:38:09] :	 [Step 1/2] [INFO] Downloaded from central: https://repo.maven.apache.org/maven2/org/codehaus/plexus/plexus-utils/1.5.6/plexus-utils-1.5.6.jar (251 kB at 4.1 MB/s)
[08:38:09] :	 [Step 1/2] [INFO] Uploading to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/0.0.1/plaindoll-0.0.1.jar
[08:38:09] :	 [Step 1/2] [INFO] Uploaded to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/0.0.1/plaindoll-0.0.1.jar (3.2 kB at 7.1 kB/s)
[08:38:09] :	 [Step 1/2] [INFO] Uploading to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/0.0.1/plaindoll-0.0.1.pom
[08:38:10] :	 [Step 1/2] [INFO] Uploaded to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/0.0.1/plaindoll-0.0.1.pom (1.5 kB at 5.6 kB/s)
[08:38:10] :	 [Step 1/2] [INFO] Downloading from nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/maven-metadata.xml
[08:38:10] :	 [Step 1/2] [INFO] Uploading to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/maven-metadata.xml
[08:38:10] :	 [Step 1/2] [INFO] Uploaded to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/maven-metadata.xml (301 B at 2.3 kB/s)
[08:38:10] :	 [Step 1/2] [Maven Watcher] 
[08:38:10]i:	 [Step 1/2] ##teamcity[projectFinished tc:tags='tc:internal' projectId='org.netology:plaindoll:jar:0.0.1']
[08:38:10] :	 [Step 1/2] [INFO] ------------------------------------------------------------------------
[08:38:10] :	 [Step 1/2] [INFO] BUILD SUCCESS
[08:38:10] :	 [Step 1/2] [INFO] ------------------------------------------------------------------------
[08:38:10] :	 [Step 1/2] [INFO] Total time:  11.662 s
[08:38:10] :	 [Step 1/2] [INFO] Finished at: 2023-09-27T09:38:10+01:00
[08:38:10] :	 [Step 1/2] [INFO] ------------------------------------------------------------------------
[08:38:10] :	 [Step 1/2] [Maven Watcher] building report document...
[08:38:10] :	 [Step 1/2] [Maven Watcher] building report document done
[08:38:10] :	 [Step 1/2] [Maven Watcher] writing report to /opt/buildagent/temp/buildTmp/maven-build-info.xml
[08:38:10] :	 [Step 1/2] [Maven Watcher] done writing report
[08:38:10] :	 [Step 1/2] Process exited with code 0
[08:38:10] :	 [Step 1/2] Publishing artifacts
[08:38:10] :		 [Publishing artifacts] Collecting files to publish: [/opt/buildagent/temp/buildTmp/.tc-maven-bi/maven-build-info.xml.gz => .teamcity]
[08:38:10] :		 [Publishing artifacts] Publishing 1 file using [WebPublisher]: /opt/buildagent/temp/buildTmp/.tc-maven-bi/maven-build-info.xml.gz => .teamcity
[08:38:10] :		 [Publishing artifacts] Publishing 1 file using [ArtifactsCachePublisherImpl]: /opt/buildagent/temp/buildTmp/.tc-maven-bi/maven-build-info.xml.gz => .teamcity
[08:38:10]i:		 [Publishing artifacts] Will publish 1 artifact(s) to TeamCity node with id MAIN_SERVER
[08:38:10] :	 [Step 1/2] Waiting for 2 service processes to complete
[08:38:10] :	 [Step 1/2] Surefire report watcher
[08:38:10] :		 [Surefire report watcher] 1 report found for paths:
[08:38:10] :		 [Surefire report watcher] /opt/buildagent/work/8e44ef381d17132e/target/surefire-reports/TEST-*.xml
[08:38:10] :		 [Surefire report watcher] Successfully parsed
[08:38:10] :			 [Successfully parsed] 1 report
[08:38:10] :			 [Successfully parsed] target/surefire-reports/TEST-plaindoll.WelcomerTest.xml
[08:38:10]W: Step 2/2: Master(mvn clean test) (Maven)
[08:38:10]W:	 [Step 2/2] Build step Master(mvn clean test) (Maven) is skipped because of unfulfilled condition: "teamcity.build.branch does not contain master"
[08:38:10]i: Stopping performance monitoring process
[08:38:13]i: Performance monitoring process stopped
[08:38:13]i: Publishing performance monitoring build stages data
[08:38:13] : Publishing artifacts
[08:38:13] :	 [Publishing artifacts] Collecting files to publish: [/opt/buildagent/system/perfmon/temp/3/perfmon.csv=>.teamcity/perfmon/, /opt/buildagent/temp/agentTmp/build_stages.txt=>.teamcity/perfmon/]
[08:38:13] :	 [Publishing artifacts] Publishing 2 files using [WebPublisher]: /opt/buildagent/system/perfmon/temp/3/perfmon.csv, /opt/buildagent/temp/agentTmp/build_stages.txt => .teamcity/perfmon
[08:38:13] :	 [Publishing artifacts] Publishing 2 files using [ArtifactsCachePublisherImpl]: /opt/buildagent/system/perfmon/temp/3/perfmon.csv, /opt/buildagent/temp/agentTmp/build_stages.txt => .teamcity/perfmon
[08:38:13]i:	 [Publishing artifacts] Will publish 2 artifact(s) to TeamCity node with id MAIN_SERVER
[08:38:13] : Publishing internal artifacts
[08:38:13] :	 [Publishing internal artifacts] Publishing 1 file using [WebPublisher]
[08:38:13] :	 [Publishing internal artifacts] Publishing 1 file using [ArtifactsCachePublisherImpl]
[08:38:13]i:	 [Publishing internal artifacts] Will publish 1 artifact(s) to TeamCity node with id MAIN_SERVER
[08:38:13] : Build finished
```

</details>

8. Мигрируйте `build configuration` в репозиторий.
![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/c6b65b68-e85a-4c50-9404-53cd77e386ba)

[Ссылка на .teamcity](https://github.com/SemenAmbarnov/example-teamcity/tree/master/.teamcity)

9. Создайте отдельную ветку `feature/add_reply` в репозитории.
10. Напишите новый метод для класса Welcomer: метод должен возвращать произвольную реплику, содержащую слово `hunter`.

Welcomer.java  

```
    public String sayHunter() {
            return "When the first hunter succumbed to the curse of blood, nightmare filled the streets of Yarnam.";
    }
```

11. Дополните тест для нового метода на поиск слова `hunter` в новой реплике.

WelcomerTest.java  

```
	@Test
	public void netologySaysHunter() {
		assertThat(welcomer.sayHunter(), containsString("hunter"));
	}
```
12. Сделайте push всех изменений в новую ветку репозитория.
13. Убедитесь, что сборка самостоятельно запустилась, тесты прошли успешно.

![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/92c66be3-4fb0-4724-8ed8-fdfc88172bd5)
![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/db1afaee-d1eb-43c3-8210-98cde6c393b8)

<details><summary>Master logs</summary>
	
```
Build 'netology / Build' #20, default branch 'master'
Triggered 2023-09-27 11:03:21 by 'admin'
Started 2023-09-27 11:03:27 on agent 'ip_130.193.37.216'
Finished 2023-09-27 11:03:47 with status NORMAL 'Tests passed: 5'
VCS revisions: 'Netology_HttpsGithubComSemenAmbarnovExampleTeamcityGitRefsHeadsMaster' (Git, instance id 3): '61760d1d5d3f6eeb2b10895799d35a307b119a82' (branch: 'refs/heads/master')
TeamCity URL http://localhost:8111/viewLog.html?buildId=21&buildTypeId=Netology_Build 
TeamCity server version is 2023.05.4 (build 129421), server timezone: GMT (UTC)

[11:03:21]W: bt1 (26s)
[11:03:21]i: TeamCity server version is 2023.05.4 (build 129421)
[11:03:21] : The build is removed from the queue to be prepared for the start
[11:03:21] : Collecting changes in 1 VCS root (6s)
[11:03:21] :	 [Collecting changes in 1 VCS root] VCS Root details
[11:03:21] :		 [VCS Root details] "git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master" {instance id=3, parent internal id=1, parent id=Netology_HttpsGithubComSemenAmbarnovExampleTeamcityGitRefsHeadsMaster, description: "git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master"}
[11:03:21]i:	 [Collecting changes in 1 VCS root] Loading current repository state for VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master' (1s)
[11:03:21]i:		 [Loading current repository state for VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': git -c credential.helper= ls-remote origin
[11:03:21]i:		 [Loading current repository state for VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': Warning: Permanently added 'github.com,140.82.121.4' (ECDSA) to the list of known hosts.
[11:03:22]i:	 [Collecting changes in 1 VCS root] Detecting changes in VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master' (used in 'Build')
[11:03:22]i:	 [Collecting changes in 1 VCS root] Will collect changes for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master' starting from revision 7a7e047647e4f6aba856032be88b564f84e3973d
[11:03:22]i:	 [Collecting changes in 1 VCS root] VCS revisions for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master' - 7a7e047647e4f6aba856032be88b564f84e3973d..61760d1d5d3f6eeb2b10895799d35a307b119a82
[11:03:22]i:	 [Collecting changes in 1 VCS root] Processing combined checkout rule for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master' 
[11:03:22]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': git -c credential.helper= ls-remote origin
[11:03:23]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': Warning: Permanently added 'github.com,140.82.121.4' (ECDSA) to the list of known hosts.
[11:03:24]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': git -c credential.helper= remote prune origin
[11:03:24]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': Warning: Permanently added 'github.com,140.82.121.4' (ECDSA) to the list of known hosts.
[11:03:25]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': git -c credential.helper= fetch --progress --no-tags --recurse-submodules=no git@github.com:SemenAmbarnov/example-teamcity.git +refs/heads/master:refs/heads/master
[11:03:26]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': Warning: Permanently added 'github.com,140.82.121.4' (ECDSA) to the list of known hosts.
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': remote: Enumerating objects: 5, done.        
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': remote: Counting objects:  20% (1/5)        
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': remote: Counting objects:  40% (2/5)        
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': remote: Counting objects:  60% (3/5)        
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': remote: Counting objects:  80% (4/5)        
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': remote: Counting objects: 100% (5/5)        
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': remote: Counting objects: 100% (5/5), done.        
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': remote: Compressing objects:  33% (1/3)        
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': remote: Compressing objects:  66% (2/3)        
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': remote: Compressing objects: 100% (3/3)        
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': remote: Compressing objects: 100% (3/3), done.        
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': remote: Total 3 (delta 2), reused 0 (delta 0), pack-reused 0        
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': Receiving objects:  33% (1/3)
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': Receiving objects:  66% (2/3)
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': Receiving objects: 100% (3/3)
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': Receiving objects: 100% (3/3), 719 bytes | 719.00 KiB/s, done.
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': Resolving deltas:   0% (0/2)
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': Resolving deltas:  50% (1/2)
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': Resolving deltas: 100% (2/2)
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': Resolving deltas: 100% (2/2), completed with 2 local objects.
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': From github.com:SemenAmbarnov/example-teamcity
[11:03:27]i:	 [Collecting changes in 1 VCS root] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master':    7a7e047..61760d1  master     -> master
[11:03:27]i:	 [Collecting changes in 1 VCS root] Done collecting changes for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': 1 changes collected 1 changes persisted, total time: 4s,874ms, persisting time: 2ms
[11:03:27] :	 [Collecting changes in 1 VCS root] Compute revision for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'
[11:03:27] :		 [Compute revision for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'] Upper limit revision: 61760d1d5d3f6eeb2b10895799d35a307b119a82
[11:03:27]i:		 [Compute revision for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'] MaxModId = 13
[11:03:27] :		 [Compute revision for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'] The first revision that was detected in the branch refs/heads/master: 4077c14e7ca293b7f8bd1d91835825c20d6da087
[11:03:27] :		 [Compute revision for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'] The first revision that was detected in the branch refs/heads/master after the last change of the VCS root or checkout rules: 4077c14e7ca293b7f8bd1d91835825c20d6da087
[11:03:27] :		 [Compute revision for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'] Latest commit attached to build configuration (with id <= 13): 61760d1d5d3f6eeb2b10895799d35a307b119a82
[11:03:27] :		 [Compute revision for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'] Computed revision: 61760d1d5d3f6eeb2b10895799d35a307b119a82
[11:03:27] : Starting the build on the agent "ip_130.193.37.216"
[11:03:27]i: Agent time zone: Europe/London
[11:03:27]i: Agent is running under JRE: 17.0.7+7-LTS
[11:03:27] : Updating tools for build
[11:03:27] :	 [Updating tools for build] Found 1 tool used by the build: maven3_6
[11:03:27] :	 [Updating tools for build] All used tools are up-to-date
[11:03:27] : Clearing temporary directory: /opt/buildagent/temp/buildTmp
[11:03:27]i: Preparing performance monitoring data directory: /opt/buildagent/system/perfmon
[11:03:27]i: Performance monitor is using command line: [perl, /opt/buildagent/system/perfmon/scripts/vmstatlinux.pl, /opt/buildagent/system/perfmon/temp/21/perfmon.csv, 1000]
[11:03:27]i: Starting performance monitoring process
[11:03:27]i: Performance monitoring process started
[11:03:27] : Publishing internal artifacts
[11:03:27] :	 [Publishing internal artifacts] Publishing 1 file using [WebPublisher]
[11:03:27] :	 [Publishing internal artifacts] Publishing 1 file using [ArtifactsCachePublisherImpl]
[11:03:27]i:	 [Publishing internal artifacts] Will publish 1 artifact(s) to TeamCity node with id MAIN_SERVER
[11:03:27] : Using vcs information from agent file: 1b1eb3af197f1f01.xml
[11:03:27] : Checkout directory: /opt/buildagent/work/1b1eb3af197f1f01
[11:03:27] : Updating sources: auto checkout (on agent) (4s)
[11:03:27] :	 [Updating sources] Will use agent side checkout
[11:03:27] :	 [Updating sources] VCS Root: git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master (4s)
[11:03:27] :		 [VCS Root: git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master] revision: 61760d1d5d3f6eeb2b10895799d35a307b119a82
[11:03:27]i:		 [VCS Root: git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master] Mirrors automatically enabled
[11:03:27] :		 [VCS Root: git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master] Git version: 2.42.0.0
[11:03:27] :		 [VCS Root: git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master] Update git mirror (/opt/buildagent/system/git/git-FEE48162.git) (4s)
[11:03:27] :			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] /usr/bin/git config http.sslCAInfo
[11:03:27] :			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] /usr/bin/git show-ref
[11:03:27] :			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] /usr/bin/git -c credential.helper= ls-remote origin
[11:03:30] :			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] /usr/bin/git show-ref refs/heads/master
[11:03:30] :			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] /usr/bin/git log -n1 --pretty=format:%H%x20%s 61760d1d5d3f6eeb2b10895799d35a307b119a82 --
[11:03:30]i:			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] fatal: bad object 61760d1d5d3f6eeb2b10895799d35a307b119a82
[11:03:30] :			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] 'git fetch' required: commit '61760d1d5d3f6eeb2b10895799d35a307b119a82' is not found in the local repository clone.
[11:03:30] :			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] /usr/bin/git -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master (2s)
[11:03:32]i:				 [/usr/bin/git -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Enumerating objects: 5, done.        
[11:03:32]i:				 [/usr/bin/git -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  20% (1/5)        
[11:03:32]i:				 [/usr/bin/git -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  40% (2/5)        
[11:03:32]i:				 [/usr/bin/git -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  60% (3/5)        
[11:03:32]i:				 [/usr/bin/git -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects:  80% (4/5)        
[11:03:32]i:				 [/usr/bin/git -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects: 100% (5/5)        
[11:03:32]i:				 [/usr/bin/git -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Counting objects: 100% (5/5), done.        
[11:03:32]i:				 [/usr/bin/git -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  33% (1/3)        
[11:03:32]i:				 [/usr/bin/git -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects:  66% (2/3)        
[11:03:32]i:				 [/usr/bin/git -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects: 100% (3/3)        
[11:03:32]i:				 [/usr/bin/git -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Compressing objects: 100% (3/3), done.        
[11:03:32]i:				 [/usr/bin/git -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] remote: Total 3 (delta 2), reused 0 (delta 0), pack-reused 0        
[11:03:32]i:				 [/usr/bin/git -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master] From github.com:SemenAmbarnov/example-teamcity
[11:03:32]i:				 [/usr/bin/git -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master]    7a7e047..61760d1  master     -> master
[11:03:32]i:				 [/usr/bin/git -c credential.helper= fetch --progress --recurse-submodules=no origin +refs/heads/master:refs/heads/master]    7a7e047..61760d1  master     -> origin/master
[11:03:32] :			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] /usr/bin/git log -n1 --pretty=format:%H%x20%s 61760d1d5d3f6eeb2b10895799d35a307b119a82 --
[11:03:32] :			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] /usr/bin/git pack-refs --all
[11:03:32] :		 [VCS Root: git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master] Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)
[11:03:32] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git rev-parse --is-shallow-repository
[11:03:32] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git config lfs.storage /opt/buildagent/system/git/git-FEE48162.git/lfs
[11:03:32] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git config core.sparseCheckout true
[11:03:32] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git config http.sslCAInfo
[11:03:32] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git show-ref
[11:03:32] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git show-ref refs/remotes/origin/master
[11:03:32] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git log -n1 --pretty=format:%H%x20%s 61760d1d5d3f6eeb2b10895799d35a307b119a82 --
[11:03:32] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] No 'git fetch' required: commit '61760d1d5d3f6eeb2b10895799d35a307b119a82' is in the local repository clone pointed by 'refs/remotes/origin/master'.
[11:03:32] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git branch
[11:03:32] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git -c credential.helper= reset --hard 61760d1d5d3f6eeb2b10895799d35a307b119a82
[11:03:32] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git branch --set-upstream-to=refs/remotes/origin/master
[11:03:32] : Build preparation done
[11:03:32]W: Step 1/2: Master(mvn clean deploy) (Maven) (8s)
[11:03:32]i:	 [Step 1/2] Build step condition "teamcity.build.branch contains master" is satisfied
[11:03:32] :	 [Step 1/2] Using predefined Maven user settings: settings.xml
[11:03:32] :	 [Step 1/2] Using predefined Maven user settings: settings.xml
[11:03:32] :	 [Step 1/2] Initial M2_HOME not set
[11:03:32] :	 [Step 1/2] Current M2_HOME = /opt/buildagent/tools/maven3_6
[11:03:32] :	 [Step 1/2] PATH = /opt/buildagent/tools/maven3_6/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
[11:03:32] :	 [Step 1/2] Using watcher: /opt/buildagent/plugins/mavenPlugin/maven-watcher-jdk17/maven-watcher-agent.jar
[11:03:32] :	 [Step 1/2] Using agent local repository at /opt/buildagent/system/jetbrains.maven.runner/maven.repo.local
[11:03:32] :	 [Step 1/2] *** Start reading the project structure ***
[11:03:32]i:	 [Step 1/2] Initial MAVEN_OPTS not set
[11:03:32]i:	 [Step 1/2] Current MAVEN_OPTS not set
[11:03:34]i:	 [Step 1/2] [INFO] Scanning for projects...
[11:03:34]i:	 [Step 1/2] [INFO] 
[11:03:34]i:	 [Step 1/2] [INFO] -----------------------< org.netology:plaindoll >-----------------------
[11:03:34]i:	 [Step 1/2] [INFO] Building plaindoll 0.1.2
[11:03:34]i:	 [Step 1/2] [INFO] --------------------------------[ jar ]---------------------------------
[11:03:34]i:	 [Step 1/2] [INFO] 
[11:03:34]i:	 [Step 1/2] [INFO] --- info-maven3-plugin:1.0.3:info (default-cli) @ plaindoll ---
[11:03:34]i:	 [Step 1/2] [INFO] ------------------------------------------------------------------------
[11:03:34]i:	 [Step 1/2] [INFO] BUILD SUCCESS
[11:03:34]i:	 [Step 1/2] [INFO] ------------------------------------------------------------------------
[11:03:34]i:	 [Step 1/2] [INFO] Total time:  0.371 s
[11:03:34]i:	 [Step 1/2] [INFO] Finished at: 2023-09-27T12:03:34+01:00
[11:03:34]i:	 [Step 1/2] [INFO] ------------------------------------------------------------------------
[11:03:34]i:	 [Step 1/2] Process exited with code 0
[11:03:34] :	 [Step 1/2] Initial MAVEN_OPTS not set
[11:03:34] :	 [Step 1/2] Current MAVEN_OPTS not set
[11:03:34] :	 [Step 1/2] Starting: /opt/java/openjdk/bin/java -Dagent.home.dir=/opt/buildagent -Dagent.name=ip_130.193.37.216 -Dagent.ownPort=9090 -Dagent.work.dir=/opt/buildagent/work -Dbuild.number=20 -Dbuild.vcs.number=61760d1d5d3f6eeb2b10895799d35a307b119a82 -Dbuild.vcs.number.1=61760d1d5d3f6eeb2b10895799d35a307b119a82 -Dbuild.vcs.number.Netology_HttpsGithubComSemenAmbarnovExampleTeamcityGitRefsHeadsMaster=61760d1d5d3f6eeb2b10895799d35a307b119a82 -Dclassworlds.conf=/opt/buildagent/temp/buildTmp/teamcity.m2.conf -Dcom.jetbrains.maven.watcher.report.file=/opt/buildagent/temp/buildTmp/maven-build-info.xml -Djava.io.tmpdir=/opt/buildagent/temp/buildTmp -Dmaven.home=/opt/buildagent/tools/maven3_6 -Dmaven.multiModuleProjectDirectory=/opt/buildagent/work/1b1eb3af197f1f01 -Dteamcity.agent.cpuBenchmark=457 -Dteamcity.agent.dotnet.agent_url=http://localhost:9090/RPC2 -Dteamcity.agent.dotnet.build_id=21 -Dteamcity.auth.password=******* -Dteamcity.auth.userId=TeamCityBuildId=21 -Dteamcity.build.changedFiles.file=/opt/buildagent/temp/buildTmp/teamcity.changedFiles.txt -Dteamcity.build.checkoutDir=/opt/buildagent/work/1b1eb3af197f1f01 -Dteamcity.build.id=21 -Dteamcity.build.properties.file=/opt/buildagent/temp/buildTmp/teamcity.build.parameters -Dteamcity.build.tempDir=/opt/buildagent/temp/buildTmp -Dteamcity.build.workingDir=/opt/buildagent/work/1b1eb3af197f1f01 -Dteamcity.buildConfName=Build -Dteamcity.buildType.id=Netology_Build -Dteamcity.configuration.properties.file=/opt/buildagent/temp/buildTmp/teamcity.config.parameters -Dteamcity.maven.userSettings.path=/opt/buildagent/temp/buildTmp/maven_settings_1031458590324304971.xml -Dteamcity.maven.watcher.home=/opt/buildagent/plugins/mavenPlugin/maven-watcher-jdk17 -Dteamcity.projectName=netology -Dteamcity.runner.properties.file=/opt/buildagent/temp/buildTmp/teamcity.runner.parameters -Dteamcity.tests.recentlyFailedTests.file=/opt/buildagent/temp/buildTmp/teamcity.testsToRunFirst.txt -Dteamcity.version=2023.05.4 (build 129421) -Dmaven.repo.local=/opt/buildagent/system/jetbrains.maven.runner/maven.repo.local -classpath /opt/buildagent/tools/maven3_6/boot/plexus-classworlds-2.6.0.jar: org.codehaus.plexus.classworlds.launcher.Launcher -f /opt/buildagent/work/1b1eb3af197f1f01/pom.xml -B -s /opt/buildagent/temp/buildTmp/maven_settings_1031458590324304971.xml -Dmaven.test.failure.ignore=true clean deploy
[11:03:34] :	 [Step 1/2] in directory: /opt/buildagent/work/1b1eb3af197f1f01
[11:03:36] :	 [Step 1/2] [INFO] Scanning for projects...
[11:03:36] :	 [Step 1/2] [INFO] 
[11:03:36] :	 [Step 1/2] [INFO] -----------------------< org.netology:plaindoll >-----------------------
[11:03:36] :	 [Step 1/2] [INFO] Building plaindoll 0.1.2
[11:03:36] :	 [Step 1/2] [INFO] --------------------------------[ jar ]---------------------------------
[11:03:36] :	 [Step 1/2] [Maven Watcher] project started: org.netology:plaindoll:jar:0.1.2
[11:03:36] :	 [Step 1/2] org.netology:plaindoll (4s)
[11:03:36]i:		 [org.netology:plaindoll] ##teamcity[importData tc:tags='tc:internal' type='surefire' path='/opt/buildagent/work/1b1eb3af197f1f01/target/failsafe-reports/TEST-*.xml' whenNoDataPublished='nothing' logAsInternal='true']
[11:03:36] :	 [Step 1/2] Importing data from '/opt/buildagent/work/1b1eb3af197f1f01/target/failsafe-reports/TEST-*.xml' (not existing file) with 'surefire' processor
[11:03:36]i:		 [org.netology:plaindoll] ##teamcity[importData tc:tags='tc:internal' type='surefire' path='/opt/buildagent/work/1b1eb3af197f1f01/target/surefire-reports/TEST-*.xml' whenNoDataPublished='nothing' logAsInternal='true']
[11:03:36] :	 [Step 1/2] [Maven Watcher] 
[11:03:36]i:	 [Step 1/2] ##teamcity[projectStarted tc:tags='tc:internal' projectId='org.netology:plaindoll:jar:0.1.2' groupId='org.netology' artifactId='plaindoll' testReportsDir0='/opt/buildagent/work/1b1eb3af197f1f01/target/failsafe-reports' testReportsDir1='/opt/buildagent/work/1b1eb3af197f1f01/target/surefire-reports']
[11:03:36] :	 [Step 1/2] Importing data from '/opt/buildagent/work/1b1eb3af197f1f01/target/surefire-reports/TEST-*.xml' (not existing file) with 'surefire' processor
[11:03:36] :	 [Step 1/2] Surefire report watcher
[11:03:36] :		 [Surefire report watcher] Watching paths:
[11:03:36] :		 [Surefire report watcher] /opt/buildagent/work/1b1eb3af197f1f01/target/failsafe-reports/TEST-*.xml
[11:03:36] :	 [Step 1/2] Surefire report watcher
[11:03:36] :		 [Surefire report watcher] Watching paths:
[11:03:36] :		 [Surefire report watcher] /opt/buildagent/work/1b1eb3af197f1f01/target/surefire-reports/TEST-*.xml
[11:03:36] :	 [Step 1/2] [INFO] 
[11:03:36] :	 [Step 1/2] [INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ plaindoll ---
[11:03:36] :	 [Step 1/2] [INFO] Deleting /opt/buildagent/work/1b1eb3af197f1f01/target
[11:03:36] :	 [Step 1/2] [INFO] 
[11:03:36] :	 [Step 1/2] [INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ plaindoll ---
[11:03:37]W:	 [Step 1/2] [WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[11:03:37] :	 [Step 1/2] [INFO] skip non existing resourceDirectory /opt/buildagent/work/1b1eb3af197f1f01/src/main/resources
[11:03:37] :	 [Step 1/2] [INFO] 
[11:03:37] :	 [Step 1/2] [INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ plaindoll ---
[11:03:37] :	 [Step 1/2] [INFO] Changes detected - recompiling the module!
[11:03:37]W:	 [Step 1/2] [WARNING] File encoding has not been set, using platform encoding UTF-8, i.e. build is platform dependent!
[11:03:37] :	 [Step 1/2] [INFO] Compiling 2 source files to /opt/buildagent/work/1b1eb3af197f1f01/target/classes
[11:03:38] :	 [Step 1/2] [INFO] 
[11:03:38] :	 [Step 1/2] [INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ plaindoll ---
[11:03:38]W:	 [Step 1/2] [WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[11:03:38] :	 [Step 1/2] [INFO] skip non existing resourceDirectory /opt/buildagent/work/1b1eb3af197f1f01/src/test/resources
[11:03:38] :	 [Step 1/2] [INFO] 
[11:03:38] :	 [Step 1/2] [INFO] --- maven-compiler-plugin:3.1:testCompile (default-testCompile) @ plaindoll ---
[11:03:38] :	 [Step 1/2] [INFO] Changes detected - recompiling the module!
[11:03:38]W:	 [Step 1/2] [WARNING] File encoding has not been set, using platform encoding UTF-8, i.e. build is platform dependent!
[11:03:38] :	 [Step 1/2] [INFO] Compiling 1 source file to /opt/buildagent/work/1b1eb3af197f1f01/target/test-classes
[11:03:38] :	 [Step 1/2] [INFO] 
[11:03:38] :	 [Step 1/2] [INFO] --- maven-surefire-plugin:2.12.4:test (default-test) @ plaindoll ---
[11:03:38] :	 [Step 1/2] [INFO] Surefire report directory: /opt/buildagent/work/1b1eb3af197f1f01/target/surefire-reports
[11:03:38] :	 [Step 1/2] 
[11:03:38] :	 [Step 1/2] -------------------------------------------------------
[11:03:38] :	 [Step 1/2]  T E S T S
[11:03:38] :	 [Step 1/2] -------------------------------------------------------
[11:03:38] :	 [Step 1/2] Running plaindoll.WelcomerTest
[11:03:38] :	 [Step 1/2] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.077 sec
[11:03:39] :	 [Step 1/2] 
[11:03:39] :	 [Step 1/2] Results :
[11:03:39] :	 [Step 1/2] 
[11:03:39] :	 [Step 1/2] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0
[11:03:39] :	 [Step 1/2] 
[11:03:39] :	 [Step 1/2] [INFO] 
[11:03:39] :	 [Step 1/2] [INFO] --- maven-jar-plugin:2.4:jar (default-jar) @ plaindoll ---
[11:03:39]i:	 [Step 1/2] plaindoll.WelcomerTest
[11:03:39]i:		 [plaindoll.WelcomerTest] welcomerSaysFarewell
[11:03:39]i:		 [plaindoll.WelcomerTest] welcomerSaysHunter
[11:03:39]i:		 [plaindoll.WelcomerTest] welcomerSaysSilver
[11:03:39]i:		 [plaindoll.WelcomerTest] welcomerSaysSomething
[11:03:39]i:		 [plaindoll.WelcomerTest] welcomerSaysWelcome
[11:03:39] :	 [Step 1/2] [INFO] Building jar: /opt/buildagent/work/1b1eb3af197f1f01/target/plaindoll-0.1.2.jar
[11:03:39] :	 [Step 1/2] [INFO] 
[11:03:39] :	 [Step 1/2] [INFO] --- maven-shade-plugin:3.2.4:shade (default) @ plaindoll ---
[11:03:39] :	 [Step 1/2] [INFO] Replacing original artifact with shaded artifact.
[11:03:39] :	 [Step 1/2] [INFO] Replacing /opt/buildagent/work/1b1eb3af197f1f01/target/plaindoll-0.1.2.jar with /opt/buildagent/work/1b1eb3af197f1f01/target/plaindoll-0.1.2-shaded.jar
[11:03:39] :	 [Step 1/2] [INFO] 
[11:03:39] :	 [Step 1/2] [INFO] --- maven-install-plugin:2.4:install (default-install) @ plaindoll ---
[11:03:39] :	 [Step 1/2] [INFO] Installing /opt/buildagent/work/1b1eb3af197f1f01/target/plaindoll-0.1.2.jar to /opt/buildagent/system/jetbrains.maven.runner/maven.repo.local/org/netology/plaindoll/0.1.2/plaindoll-0.1.2.jar
[11:03:39] :	 [Step 1/2] [INFO] Installing /opt/buildagent/work/1b1eb3af197f1f01/pom.xml to /opt/buildagent/system/jetbrains.maven.runner/maven.repo.local/org/netology/plaindoll/0.1.2/plaindoll-0.1.2.pom
[11:03:39] :	 [Step 1/2] [INFO] 
[11:03:39] :	 [Step 1/2] [INFO] --- maven-deploy-plugin:2.7:deploy (default-deploy) @ plaindoll ---
[11:03:40] :	 [Step 1/2] [INFO] Uploading to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/0.1.2/plaindoll-0.1.2.jar
[11:03:40] :	 [Step 1/2] [INFO] Uploaded to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/0.1.2/plaindoll-0.1.2.jar (3.2 kB at 15 kB/s)
[11:03:40] :	 [Step 1/2] [INFO] Uploading to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/0.1.2/plaindoll-0.1.2.pom
[11:03:40] :	 [Step 1/2] [INFO] Uploaded to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/0.1.2/plaindoll-0.1.2.pom (1.5 kB at 14 kB/s)
[11:03:40] :	 [Step 1/2] [INFO] Downloading from nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/maven-metadata.xml
[11:03:40] :	 [Step 1/2] [INFO] Downloaded from nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/maven-metadata.xml (332 B at 9.8 kB/s)
[11:03:40] :	 [Step 1/2] [INFO] Uploading to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/maven-metadata.xml
[11:03:40] :	 [Step 1/2] [INFO] Uploaded to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/maven-metadata.xml (363 B at 2.2 kB/s)
[11:03:40] :	 [Step 1/2] [Maven Watcher] 
[11:03:40]i:	 [Step 1/2] ##teamcity[projectFinished tc:tags='tc:internal' projectId='org.netology:plaindoll:jar:0.1.2']
[11:03:40] :	 [Step 1/2] [INFO] ------------------------------------------------------------------------
[11:03:40] :	 [Step 1/2] [INFO] BUILD SUCCESS
[11:03:40] :	 [Step 1/2] [INFO] ------------------------------------------------------------------------
[11:03:40] :	 [Step 1/2] [INFO] Total time:  4.190 s
[11:03:40] :	 [Step 1/2] [INFO] Finished at: 2023-09-27T12:03:40+01:00
[11:03:40] :	 [Step 1/2] [INFO] ------------------------------------------------------------------------
[11:03:40] :	 [Step 1/2] [Maven Watcher] building report document...
[11:03:40] :	 [Step 1/2] [Maven Watcher] building report document done
[11:03:40] :	 [Step 1/2] [Maven Watcher] writing report to /opt/buildagent/temp/buildTmp/maven-build-info.xml
[11:03:40] :	 [Step 1/2] [Maven Watcher] done writing report
[11:03:40] :	 [Step 1/2] Process exited with code 0
[11:03:40] :	 [Step 1/2] Publishing artifacts
[11:03:40] :		 [Publishing artifacts] Collecting files to publish: [/opt/buildagent/temp/buildTmp/.tc-maven-bi/maven-build-info.xml.gz => .teamcity]
[11:03:40] :		 [Publishing artifacts] Publishing 1 file using [WebPublisher]: /opt/buildagent/temp/buildTmp/.tc-maven-bi/maven-build-info.xml.gz => .teamcity
[11:03:40] :		 [Publishing artifacts] Publishing 1 file using [ArtifactsCachePublisherImpl]: /opt/buildagent/temp/buildTmp/.tc-maven-bi/maven-build-info.xml.gz => .teamcity
[11:03:40]i:		 [Publishing artifacts] Will publish 1 artifact(s) to TeamCity node with id MAIN_SERVER
[11:03:40] :	 [Step 1/2] Waiting for 2 service processes to complete
[11:03:41] :	 [Step 1/2] Surefire report watcher
[11:03:41] :		 [Surefire report watcher] 1 report found for paths:
[11:03:41] :		 [Surefire report watcher] /opt/buildagent/work/1b1eb3af197f1f01/target/surefire-reports/TEST-*.xml
[11:03:41] :		 [Surefire report watcher] Successfully parsed
[11:03:41] :			 [Successfully parsed] 1 report
[11:03:41] :			 [Successfully parsed] target/surefire-reports/TEST-plaindoll.WelcomerTest.xml
[11:03:41]W: Step 2/2: Master(mvn clean test) (Maven)
[11:03:41]W:	 [Step 2/2] Build step Master(mvn clean test) (Maven) is skipped because of unfulfilled condition: "teamcity.build.branch does not contain master"
[11:03:41]i: Stopping performance monitoring process
[11:03:47]i: Performance monitoring process stopped
[11:03:47]i: Publishing performance monitoring build stages data
[11:03:47] : Publishing artifacts
[11:03:47] :	 [Publishing artifacts] Collecting files to publish: [/opt/buildagent/system/perfmon/temp/21/perfmon.csv=>.teamcity/perfmon/, /opt/buildagent/temp/agentTmp/build_stages.txt=>.teamcity/perfmon/]
[11:03:47] :	 [Publishing artifacts] Publishing 2 files using [WebPublisher]: /opt/buildagent/system/perfmon/temp/21/perfmon.csv, /opt/buildagent/temp/agentTmp/build_stages.txt => .teamcity/perfmon
[11:03:47] :	 [Publishing artifacts] Publishing 2 files using [ArtifactsCachePublisherImpl]: /opt/buildagent/system/perfmon/temp/21/perfmon.csv, /opt/buildagent/temp/agentTmp/build_stages.txt => .teamcity/perfmon
[11:03:47]i:	 [Publishing artifacts] Will publish 2 artifact(s) to TeamCity node with id MAIN_SERVER
[11:03:47] : Publishing internal artifacts
[11:03:47] :	 [Publishing internal artifacts] Publishing 1 file using [WebPublisher]
[11:03:47] :	 [Publishing internal artifacts] Publishing 1 file using [ArtifactsCachePublisherImpl]
[11:03:47]i:	 [Publishing internal artifacts] Will publish 1 artifact(s) to TeamCity node with id MAIN_SERVER
[11:03:47] : Build finished

```

</details>

<details><summary>Feature/add_reply logs</summary>

```
Build 'netology / Build' #16, branch 'feature/add_reply'
Triggered 2023-09-27 10:48:58 by 'admin'
Started 2023-09-27 10:49:00 on agent 'ip_130.193.37.216'
Finished 2023-09-27 10:49:21 with status NORMAL 'Tests passed: 5'
VCS revisions: 'Netology_HttpsGithubComSemenAmbarnovExampleTeamcityGitRefsHeadsMaster' (Git, instance id 3): 'b54e3efbb9c8bc9101b5714036b37535d135566a' (branch: 'refs/heads/feature/add_reply')
TeamCity URL http://localhost:8111/viewLog.html?buildId=16&buildTypeId=Netology_Build 
TeamCity server version is 2023.05.4 (build 129421), server timezone: GMT (UTC)

[10:48:58]W: bt1 (22s)
[10:48:58]i: TeamCity server version is 2023.05.4 (build 129421)
[10:48:58] : The build is removed from the queue to be prepared for the start
[10:48:58] : Collecting changes in 1 VCS root (1s)
[10:48:58] :	 [Collecting changes in 1 VCS root] VCS Root details
[10:48:58] :		 [VCS Root details] "git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master" {instance id=3, parent internal id=1, parent id=Netology_HttpsGithubComSemenAmbarnovExampleTeamcityGitRefsHeadsMaster, description: "git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master"}
[10:48:58]i:	 [Collecting changes in 1 VCS root] Loading current repository state for VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master' (1s)
[10:48:58]i:		 [Loading current repository state for VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': git -c credential.helper= ls-remote origin
[10:48:58]i:		 [Loading current repository state for VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'] VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master': Warning: Permanently added 'github.com,140.82.121.3' (ECDSA) to the list of known hosts.
[10:49:00]i:	 [Collecting changes in 1 VCS root] Detecting changes in VCS root 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master' (used in 'Build')
[10:49:00]i:	 [Collecting changes in 1 VCS root] Will collect changes for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master' starting from revision 4077c14e7ca293b7f8bd1d91835825c20d6da087
[10:49:00] :	 [Collecting changes in 1 VCS root] Compute revision for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'
[10:49:00] :		 [Compute revision for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'] Upper limit revision: b54e3efbb9c8bc9101b5714036b37535d135566a
[10:49:00]i:		 [Compute revision for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'] MaxModId = 10
[10:49:00] :		 [Compute revision for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'] The first revision that was detected in the branch refs/heads/feature/add_reply: b54e3efbb9c8bc9101b5714036b37535d135566a
[10:49:00] :		 [Compute revision for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'] The first revision that was detected in the branch refs/heads/feature/add_reply after the last change of the VCS root or checkout rules: b54e3efbb9c8bc9101b5714036b37535d135566a
[10:49:00] :		 [Compute revision for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'] Latest commit attached to build configuration (with id <= 10): b54e3efbb9c8bc9101b5714036b37535d135566a
[10:49:00] :		 [Compute revision for 'git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master'] Computed revision: b54e3efbb9c8bc9101b5714036b37535d135566a
[10:49:00] : Starting the build on the agent "ip_130.193.37.216"
[10:49:01]i: Agent time zone: Europe/London
[10:49:01]i: Agent is running under JRE: 17.0.7+7-LTS
[10:49:01] : Updating tools for build
[10:49:01] :	 [Updating tools for build] Found 1 tool used by the build: maven3_6
[10:49:01] :	 [Updating tools for build] All used tools are up-to-date
[10:49:01] : Clearing temporary directory: /opt/buildagent/temp/buildTmp
[10:49:01]i: Preparing performance monitoring data directory: /opt/buildagent/system/perfmon
[10:49:01]i: Performance monitor is using command line: [perl, /opt/buildagent/system/perfmon/scripts/vmstatlinux.pl, /opt/buildagent/system/perfmon/temp/16/perfmon.csv, 1000]
[10:49:01]i: Starting performance monitoring process
[10:49:01]i: Performance monitoring process started
[10:49:01] : Publishing internal artifacts
[10:49:01] :	 [Publishing internal artifacts] Publishing 1 file using [WebPublisher]
[10:49:01] :	 [Publishing internal artifacts] Publishing 1 file using [ArtifactsCachePublisherImpl]
[10:49:01]i:	 [Publishing internal artifacts] Will publish 1 artifact(s) to TeamCity node with id MAIN_SERVER
[10:49:01] : Using vcs information from agent file: 1b1eb3af197f1f01.xml
[10:49:01] : Checkout directory: /opt/buildagent/work/1b1eb3af197f1f01
[10:49:01] : Updating sources: auto checkout (on agent) (2s)
[10:49:01] :	 [Updating sources] Will use agent side checkout
[10:49:01] :	 [Updating sources] VCS Root: git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master (2s)
[10:49:01] :		 [VCS Root: git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master] revision: b54e3efbb9c8bc9101b5714036b37535d135566a
[10:49:01]i:		 [VCS Root: git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master] Mirrors automatically enabled
[10:49:01] :		 [VCS Root: git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master] Git version: 2.42.0.0
[10:49:01] :		 [VCS Root: git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master] Update git mirror (/opt/buildagent/system/git/git-FEE48162.git) (2s)
[10:49:01] :			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] /usr/bin/git config http.sslCAInfo
[10:49:01] :			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] /usr/bin/git show-ref
[10:49:01] :			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] /usr/bin/git -c credential.helper= ls-remote origin
[10:49:03] :			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] /usr/bin/git show-ref refs/heads/feature/add_reply
[10:49:03] :			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] /usr/bin/git log -n1 --pretty=format:%H%x20%s b54e3efbb9c8bc9101b5714036b37535d135566a --
[10:49:03] :			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] No 'git fetch' required: commit 'b54e3efbb9c8bc9101b5714036b37535d135566a' is in the local repository clone pointed by 'refs/heads/feature/add_reply'.
[10:49:03] :			 [Update git mirror (/opt/buildagent/system/git/git-FEE48162.git)] /usr/bin/git pack-refs --all
[10:49:03] :		 [VCS Root: git@github.com:SemenAmbarnov/example-teamcity.git#refs/heads/master] Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)
[10:49:03] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git rev-parse --is-shallow-repository
[10:49:03] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git config lfs.storage /opt/buildagent/system/git/git-FEE48162.git/lfs
[10:49:03] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git config core.sparseCheckout true
[10:49:03] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git config http.sslCAInfo
[10:49:03] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git show-ref
[10:49:03] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git show-ref refs/remotes/origin/feature/add_reply
[10:49:03] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git log -n1 --pretty=format:%H%x20%s b54e3efbb9c8bc9101b5714036b37535d135566a --
[10:49:03] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] No 'git fetch' required: commit 'b54e3efbb9c8bc9101b5714036b37535d135566a' is in the local repository clone pointed by 'refs/remotes/origin/feature/add_reply'.
[10:49:03] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git branch
[10:49:03] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git -c credential.helper= reset --hard b54e3efbb9c8bc9101b5714036b37535d135566a
[10:49:03] :			 [Update checkout directory (/opt/buildagent/work/1b1eb3af197f1f01)] /usr/bin/git branch --set-upstream-to=refs/remotes/origin/feature/add_reply
[10:49:03] : Build preparation done
[10:49:03]W: Step 1/2: Master(mvn clean deploy) (Maven)
[10:49:03]W:	 [Step 1/2] Build step Master(mvn clean deploy) (Maven) is skipped because of unfulfilled condition: "teamcity.build.branch contains master"
[10:49:03]W: Step 2/2: Master(mvn clean test) (Maven) (8s)
[10:49:03]i:	 [Step 2/2] Build step condition "teamcity.build.branch does not contain master" is satisfied
[10:49:03] :	 [Step 2/2] Using predefined Maven user settings: settings.xml
[10:49:03] :	 [Step 2/2] Using predefined Maven user settings: settings.xml
[10:49:03] :	 [Step 2/2] Initial M2_HOME not set
[10:49:03] :	 [Step 2/2] Current M2_HOME = /opt/buildagent/tools/maven3_6
[10:49:03] :	 [Step 2/2] PATH = /opt/buildagent/tools/maven3_6/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
[10:49:03] :	 [Step 2/2] Using watcher: /opt/buildagent/plugins/mavenPlugin/maven-watcher-jdk17/maven-watcher-agent.jar
[10:49:03] :	 [Step 2/2] Using agent local repository at /opt/buildagent/system/jetbrains.maven.runner/maven.repo.local
[10:49:03] :	 [Step 2/2] *** Start reading the project structure ***
[10:49:03]i:	 [Step 2/2] Initial MAVEN_OPTS not set
[10:49:03]i:	 [Step 2/2] Current MAVEN_OPTS not set
[10:49:05]i:	 [Step 2/2] [INFO] Scanning for projects...
[10:49:05]i:	 [Step 2/2] [INFO] 
[10:49:05]i:	 [Step 2/2] [INFO] -----------------------< org.netology:plaindoll >-----------------------
[10:49:05]i:	 [Step 2/2] [INFO] Building plaindoll 0.1.1
[10:49:05]i:	 [Step 2/2] [INFO] --------------------------------[ jar ]---------------------------------
[10:49:05]i:	 [Step 2/2] [INFO] 
[10:49:05]i:	 [Step 2/2] [INFO] --- info-maven3-plugin:1.0.3:info (default-cli) @ plaindoll ---
[10:49:05]i:	 [Step 2/2] [INFO] ------------------------------------------------------------------------
[10:49:05]i:	 [Step 2/2] [INFO] BUILD SUCCESS
[10:49:05]i:	 [Step 2/2] [INFO] ------------------------------------------------------------------------
[10:49:05]i:	 [Step 2/2] [INFO] Total time:  0.360 s
[10:49:05]i:	 [Step 2/2] [INFO] Finished at: 2023-09-27T11:49:05+01:00
[10:49:05]i:	 [Step 2/2] [INFO] ------------------------------------------------------------------------
[10:49:05]i:	 [Step 2/2] Process exited with code 0
[10:49:05] :	 [Step 2/2] Initial MAVEN_OPTS not set
[10:49:05] :	 [Step 2/2] Current MAVEN_OPTS not set
[10:49:05] :	 [Step 2/2] Starting: /opt/java/openjdk/bin/java -Dagent.home.dir=/opt/buildagent -Dagent.name=ip_130.193.37.216 -Dagent.ownPort=9090 -Dagent.work.dir=/opt/buildagent/work -Dbuild.number=16 -Dbuild.vcs.number=b54e3efbb9c8bc9101b5714036b37535d135566a -Dbuild.vcs.number.1=b54e3efbb9c8bc9101b5714036b37535d135566a -Dbuild.vcs.number.Netology_HttpsGithubComSemenAmbarnovExampleTeamcityGitRefsHeadsMaster=b54e3efbb9c8bc9101b5714036b37535d135566a -Dclassworlds.conf=/opt/buildagent/temp/buildTmp/teamcity.m2.conf -Dcom.jetbrains.maven.watcher.report.file=/opt/buildagent/temp/buildTmp/maven-build-info.xml -Djava.io.tmpdir=/opt/buildagent/temp/buildTmp -Dmaven.home=/opt/buildagent/tools/maven3_6 -Dmaven.multiModuleProjectDirectory=/opt/buildagent/work/1b1eb3af197f1f01 -Dteamcity.agent.cpuBenchmark=457 -Dteamcity.agent.dotnet.agent_url=http://localhost:9090/RPC2 -Dteamcity.agent.dotnet.build_id=16 -Dteamcity.auth.password=******* -Dteamcity.auth.userId=TeamCityBuildId=16 -Dteamcity.build.changedFiles.file=/opt/buildagent/temp/buildTmp/teamcity.changedFiles.txt -Dteamcity.build.checkoutDir=/opt/buildagent/work/1b1eb3af197f1f01 -Dteamcity.build.id=16 -Dteamcity.build.properties.file=/opt/buildagent/temp/buildTmp/teamcity.build.parameters -Dteamcity.build.tempDir=/opt/buildagent/temp/buildTmp -Dteamcity.build.workingDir=/opt/buildagent/work/1b1eb3af197f1f01 -Dteamcity.buildConfName=Build -Dteamcity.buildType.id=Netology_Build -Dteamcity.configuration.properties.file=/opt/buildagent/temp/buildTmp/teamcity.config.parameters -Dteamcity.maven.userSettings.path=/opt/buildagent/temp/buildTmp/maven_settings_17680643663192905238.xml -Dteamcity.maven.watcher.home=/opt/buildagent/plugins/mavenPlugin/maven-watcher-jdk17 -Dteamcity.projectName=netology -Dteamcity.runner.properties.file=/opt/buildagent/temp/buildTmp/teamcity.runner.parameters -Dteamcity.tests.recentlyFailedTests.file=/opt/buildagent/temp/buildTmp/teamcity.testsToRunFirst.txt -Dteamcity.version=2023.05.4 (build 129421) -Dmaven.repo.local=/opt/buildagent/system/jetbrains.maven.runner/maven.repo.local -classpath /opt/buildagent/tools/maven3_6/boot/plexus-classworlds-2.6.0.jar: org.codehaus.plexus.classworlds.launcher.Launcher -f /opt/buildagent/work/1b1eb3af197f1f01/pom.xml -B -s /opt/buildagent/temp/buildTmp/maven_settings_17680643663192905238.xml -Dmaven.test.failure.ignore=true clean deploy
[10:49:05] :	 [Step 2/2] in directory: /opt/buildagent/work/1b1eb3af197f1f01
[10:49:07] :	 [Step 2/2] [INFO] Scanning for projects...
[10:49:07] :	 [Step 2/2] [INFO] 
[10:49:07] :	 [Step 2/2] [INFO] -----------------------< org.netology:plaindoll >-----------------------
[10:49:07] :	 [Step 2/2] [INFO] Building plaindoll 0.1.1
[10:49:07] :	 [Step 2/2] [INFO] --------------------------------[ jar ]---------------------------------
[10:49:07] :	 [Step 2/2] [Maven Watcher] project started: org.netology:plaindoll:jar:0.1.1
[10:49:07] :	 [Step 2/2] org.netology:plaindoll (4s)
[10:49:07]i:		 [org.netology:plaindoll] ##teamcity[importData tc:tags='tc:internal' type='surefire' path='/opt/buildagent/work/1b1eb3af197f1f01/target/failsafe-reports/TEST-*.xml' whenNoDataPublished='nothing' logAsInternal='true']
[10:49:07] :	 [Step 2/2] Importing data from '/opt/buildagent/work/1b1eb3af197f1f01/target/failsafe-reports/TEST-*.xml' (not existing file) with 'surefire' processor
[10:49:07]i:		 [org.netology:plaindoll] ##teamcity[importData tc:tags='tc:internal' type='surefire' path='/opt/buildagent/work/1b1eb3af197f1f01/target/surefire-reports/TEST-*.xml' whenNoDataPublished='nothing' logAsInternal='true']
[10:49:07] :	 [Step 2/2] [Maven Watcher] 
[10:49:07]i:	 [Step 2/2] ##teamcity[projectStarted tc:tags='tc:internal' projectId='org.netology:plaindoll:jar:0.1.1' groupId='org.netology' artifactId='plaindoll' testReportsDir0='/opt/buildagent/work/1b1eb3af197f1f01/target/failsafe-reports' testReportsDir1='/opt/buildagent/work/1b1eb3af197f1f01/target/surefire-reports']
[10:49:07] :	 [Step 2/2] Importing data from '/opt/buildagent/work/1b1eb3af197f1f01/target/surefire-reports/TEST-*.xml' (not existing file) with 'surefire' processor
[10:49:07] :	 [Step 2/2] Surefire report watcher
[10:49:07] :		 [Surefire report watcher] Watching paths:
[10:49:07] :		 [Surefire report watcher] /opt/buildagent/work/1b1eb3af197f1f01/target/failsafe-reports/TEST-*.xml
[10:49:07] :	 [Step 2/2] Surefire report watcher
[10:49:07] :		 [Surefire report watcher] Watching paths:
[10:49:07] :		 [Surefire report watcher] /opt/buildagent/work/1b1eb3af197f1f01/target/surefire-reports/TEST-*.xml
[10:49:08] :	 [Step 2/2] [INFO] 
[10:49:08] :	 [Step 2/2] [INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ plaindoll ---
[10:49:08] :	 [Step 2/2] [INFO] Deleting /opt/buildagent/work/1b1eb3af197f1f01/target
[10:49:08] :	 [Step 2/2] [INFO] 
[10:49:08] :	 [Step 2/2] [INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ plaindoll ---
[10:49:08]W:	 [Step 2/2] [WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[10:49:08] :	 [Step 2/2] [INFO] skip non existing resourceDirectory /opt/buildagent/work/1b1eb3af197f1f01/src/main/resources
[10:49:08] :	 [Step 2/2] [INFO] 
[10:49:08] :	 [Step 2/2] [INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ plaindoll ---
[10:49:08] :	 [Step 2/2] [INFO] Changes detected - recompiling the module!
[10:49:08]W:	 [Step 2/2] [WARNING] File encoding has not been set, using platform encoding UTF-8, i.e. build is platform dependent!
[10:49:08] :	 [Step 2/2] [INFO] Compiling 2 source files to /opt/buildagent/work/1b1eb3af197f1f01/target/classes
[10:49:09] :	 [Step 2/2] [INFO] 
[10:49:09] :	 [Step 2/2] [INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ plaindoll ---
[10:49:09]W:	 [Step 2/2] [WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[10:49:09] :	 [Step 2/2] [INFO] skip non existing resourceDirectory /opt/buildagent/work/1b1eb3af197f1f01/src/test/resources
[10:49:09] :	 [Step 2/2] [INFO] 
[10:49:09] :	 [Step 2/2] [INFO] --- maven-compiler-plugin:3.1:testCompile (default-testCompile) @ plaindoll ---
[10:49:09] :	 [Step 2/2] [INFO] Changes detected - recompiling the module!
[10:49:09]W:	 [Step 2/2] [WARNING] File encoding has not been set, using platform encoding UTF-8, i.e. build is platform dependent!
[10:49:09] :	 [Step 2/2] [INFO] Compiling 1 source file to /opt/buildagent/work/1b1eb3af197f1f01/target/test-classes
[10:49:09] :	 [Step 2/2] [INFO] 
[10:49:09] :	 [Step 2/2] [INFO] --- maven-surefire-plugin:2.12.4:test (default-test) @ plaindoll ---
[10:49:09] :	 [Step 2/2] [INFO] Surefire report directory: /opt/buildagent/work/1b1eb3af197f1f01/target/surefire-reports
[10:49:09] :	 [Step 2/2] 
[10:49:09] :	 [Step 2/2] -------------------------------------------------------
[10:49:09] :	 [Step 2/2]  T E S T S
[10:49:09] :	 [Step 2/2] -------------------------------------------------------
[10:49:10] :	 [Step 2/2] Running plaindoll.WelcomerTest
[10:49:10] :	 [Step 2/2] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.114 sec
[10:49:10] :	 [Step 2/2] 
[10:49:10] :	 [Step 2/2] Results :
[10:49:10] :	 [Step 2/2] 
[10:49:10] :	 [Step 2/2] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0
[10:49:10] :	 [Step 2/2] 
[10:49:10] :	 [Step 2/2] [INFO] 
[10:49:10] :	 [Step 2/2] [INFO] --- maven-jar-plugin:2.4:jar (default-jar) @ plaindoll ---
[10:49:10] :	 [Step 2/2] [INFO] Building jar: /opt/buildagent/work/1b1eb3af197f1f01/target/plaindoll-0.1.1.jar
[10:49:10] :	 [Step 2/2] [INFO] 
[10:49:10] :	 [Step 2/2] [INFO] --- maven-shade-plugin:3.2.4:shade (default) @ plaindoll ---
[10:49:10]i:	 [Step 2/2] plaindoll.WelcomerTest
[10:49:10]i:		 [plaindoll.WelcomerTest] welcomerSaysFarewell
[10:49:10]i:		 [plaindoll.WelcomerTest] welcomerSaysHunter
[10:49:10]i:		 [plaindoll.WelcomerTest] welcomerSaysSilver
[10:49:10]i:		 [plaindoll.WelcomerTest] welcomerSaysWelcome
[10:49:10]i:		 [plaindoll.WelcomerTest] netologySaysHunter
[10:49:10] :	 [Step 2/2] [INFO] Replacing original artifact with shaded artifact.
[10:49:10] :	 [Step 2/2] [INFO] Replacing /opt/buildagent/work/1b1eb3af197f1f01/target/plaindoll-0.1.1.jar with /opt/buildagent/work/1b1eb3af197f1f01/target/plaindoll-0.1.1-shaded.jar
[10:49:10] :	 [Step 2/2] [INFO] 
[10:49:10] :	 [Step 2/2] [INFO] --- maven-install-plugin:2.4:install (default-install) @ plaindoll ---
[10:49:10] :	 [Step 2/2] [INFO] Installing /opt/buildagent/work/1b1eb3af197f1f01/target/plaindoll-0.1.1.jar to /opt/buildagent/system/jetbrains.maven.runner/maven.repo.local/org/netology/plaindoll/0.1.1/plaindoll-0.1.1.jar
[10:49:10] :	 [Step 2/2] [INFO] Installing /opt/buildagent/work/1b1eb3af197f1f01/pom.xml to /opt/buildagent/system/jetbrains.maven.runner/maven.repo.local/org/netology/plaindoll/0.1.1/plaindoll-0.1.1.pom
[10:49:10] :	 [Step 2/2] [INFO] 
[10:49:10] :	 [Step 2/2] [INFO] --- maven-deploy-plugin:2.7:deploy (default-deploy) @ plaindoll ---
[10:49:11] :	 [Step 2/2] [INFO] Uploading to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/0.1.1/plaindoll-0.1.1.jar
[10:49:11] :	 [Step 2/2] [INFO] Uploaded to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/0.1.1/plaindoll-0.1.1.jar (3.2 kB at 15 kB/s)
[10:49:11] :	 [Step 2/2] [INFO] Uploading to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/0.1.1/plaindoll-0.1.1.pom
[10:49:11] :	 [Step 2/2] [INFO] Uploaded to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/0.1.1/plaindoll-0.1.1.pom (1.5 kB at 15 kB/s)
[10:49:11] :	 [Step 2/2] [INFO] Downloading from nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/maven-metadata.xml
[10:49:11] :	 [Step 2/2] [INFO] Downloaded from nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/maven-metadata.xml (301 B at 10 kB/s)
[10:49:11] :	 [Step 2/2] [INFO] Uploading to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/maven-metadata.xml
[10:49:11] :	 [Step 2/2] [INFO] Uploaded to nexus: http://158.160.126.24:8081/repository/maven-releases/org/netology/plaindoll/maven-metadata.xml (332 B at 4.0 kB/s)
[10:49:11] :	 [Step 2/2] [Maven Watcher] 
[10:49:11]i:	 [Step 2/2] ##teamcity[projectFinished tc:tags='tc:internal' projectId='org.netology:plaindoll:jar:0.1.1']
[10:49:11] :	 [Step 2/2] [INFO] ------------------------------------------------------------------------
[10:49:11] :	 [Step 2/2] [INFO] BUILD SUCCESS
[10:49:11] :	 [Step 2/2] [INFO] ------------------------------------------------------------------------
[10:49:11] :	 [Step 2/2] [INFO] Total time:  4.193 s
[10:49:11] :	 [Step 2/2] [INFO] Finished at: 2023-09-27T11:49:11+01:00
[10:49:11] :	 [Step 2/2] [INFO] ------------------------------------------------------------------------
[10:49:11] :	 [Step 2/2] [Maven Watcher] building report document...
[10:49:11] :	 [Step 2/2] [Maven Watcher] building report document done
[10:49:11] :	 [Step 2/2] [Maven Watcher] writing report to /opt/buildagent/temp/buildTmp/maven-build-info.xml
[10:49:11] :	 [Step 2/2] [Maven Watcher] done writing report
[10:49:11] :	 [Step 2/2] Process exited with code 0
[10:49:11] :	 [Step 2/2] Publishing artifacts
[10:49:11] :		 [Publishing artifacts] Collecting files to publish: [/opt/buildagent/temp/buildTmp/.tc-maven-bi/maven-build-info.xml.gz => .teamcity]
[10:49:11] :		 [Publishing artifacts] Publishing 1 file using [WebPublisher]: /opt/buildagent/temp/buildTmp/.tc-maven-bi/maven-build-info.xml.gz => .teamcity
[10:49:11] :		 [Publishing artifacts] Publishing 1 file using [ArtifactsCachePublisherImpl]: /opt/buildagent/temp/buildTmp/.tc-maven-bi/maven-build-info.xml.gz => .teamcity
[10:49:11]i:		 [Publishing artifacts] Will publish 1 artifact(s) to TeamCity node with id MAIN_SERVER
[10:49:11] :	 [Step 2/2] Waiting for 2 service processes to complete
[10:49:12] :	 [Step 2/2] Surefire report watcher
[10:49:12] :		 [Surefire report watcher] 1 report found for paths:
[10:49:12] :		 [Surefire report watcher] /opt/buildagent/work/1b1eb3af197f1f01/target/surefire-reports/TEST-*.xml
[10:49:12] :		 [Surefire report watcher] Successfully parsed
[10:49:12] :			 [Successfully parsed] 1 report
[10:49:12] :			 [Successfully parsed] target/surefire-reports/TEST-plaindoll.WelcomerTest.xml
[10:49:12]i: Stopping performance monitoring process
[10:49:21]i: Performance monitoring process stopped
[10:49:21]i: Publishing performance monitoring build stages data
[10:49:21] : Publishing artifacts
[10:49:21] :	 [Publishing artifacts] Collecting files to publish: [/opt/buildagent/system/perfmon/temp/16/perfmon.csv=>.teamcity/perfmon/, /opt/buildagent/temp/agentTmp/build_stages.txt=>.teamcity/perfmon/]
[10:49:21] :	 [Publishing artifacts] Publishing 2 files using [WebPublisher]: /opt/buildagent/system/perfmon/temp/16/perfmon.csv, /opt/buildagent/temp/agentTmp/build_stages.txt => .teamcity/perfmon
[10:49:21] :	 [Publishing artifacts] Publishing 2 files using [ArtifactsCachePublisherImpl]: /opt/buildagent/system/perfmon/temp/16/perfmon.csv, /opt/buildagent/temp/agentTmp/build_stages.txt => .teamcity/perfmon
[10:49:21]i:	 [Publishing artifacts] Will publish 2 artifact(s) to TeamCity node with id MAIN_SERVER
[10:49:21] : Publishing internal artifacts
[10:49:21] :	 [Publishing internal artifacts] Publishing 1 file using [WebPublisher]
[10:49:21] :	 [Publishing internal artifacts] Publishing 1 file using [ArtifactsCachePublisherImpl]
[10:49:21]i:	 [Publishing internal artifacts] Will publish 1 artifact(s) to TeamCity node with id MAIN_SERVER
[10:49:21] : Build finished

```
</details>

14. Внесите изменения из произвольной ветки `feature/add_reply` в `master` через `Merge`.
15. Убедитесь, что нет собранного артефакта в сборке по ветке `master`.
16. Настройте конфигурацию так, чтобы она собирала `.jar` в артефакты сборки.
![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/81c40963-815c-49b7-b10c-3942d4986f41)

17. Проведите повторную сборку мастера, убедитесь, что сбора прошла успешно и артефакты собраны.
![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/738b30b6-a8b5-41cc-bd3f-52c46439711b)


18. Проверьте, что конфигурация в репозитории содержит все настройки конфигурации из teamcity.



19. В ответе пришлите ссылку на репозиторий.

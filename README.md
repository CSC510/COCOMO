#Homework 3
##	Theory 1: COCOMO
  -	List 1: 
    -	Prec: have we done this before?
      <br>Prec measures the experience with similar projects.
      <br>We could assign people to projects according to whether they have relevant experience before, which will increase this factor.
    - Flex: development flexibility
      <br> Flex contains the need for software conformance and premium on early completion.
      <br> In development process, if a new requirement conforms to a pre-established requirement, the Flex rating would be high.
    - Team: team cohesion
      <br> Team accounts for sources of project instability and entropy of a project.
      <br> If we cooperate with the stakeholders who don't have enough ability and experience in communication and operation, Team factor will decrease.
    - Pmat: process maturity
      <br> Pmat is based on Capability Maturity Model (CMM), and Key Process Areas (KPAs).
      <br> We can increase Pmat by increase the rating of Capability Maturity Model, and the percentage of compliance for Key Process Areas.
    - Resl: any risk resolution activities?
      <br> Resl combines of design thoroughness and risk elimination.
      <br> We could modify the Risk Management Plan to identify all critical risk items, establishes milestones for resolving them, so that Resl will decrease.
  - List 2: 
    - Rely: required reliability
      <br> Rely tells if the software could perform its function over a period of time.
      <br> If the project cannot be finished with an entire safety inspection, it might have very bad impacts on human life, which increases Rely rating.
    - Data: secondary memory storage requirements
      <br> Data measures the affect large data requirements have on product development.
      <br> If the size of the database is high, then it will increase the effort required to generate the test data that will be used to exercise the program, which lead to high Data.
    - Cplx: program complexity
      <br> Cplx contains five areas, which measure the complexity of the product.
      <br> We can modify the code of the program to make it smaller and easier to reuse, so that we can decrease the difficulty of development, which could decrease Cplx.
    - Ruse: software reuse
      <br> Ruse tells the additional effort needed to construct for reuse projects
      <br> If we can create more generic design of software, more elaborate documentation, and more extensive testing, Ruse rating will be increased.
    - Docu: documentation requirements
      <br> Docu measures the suitability of the project's documentation to its life-cycle needs.
      <br> If the document of the project is very excessive for life-cycle needs, it will be difficult to maintain the software, and the Docu rating increases.
    - Time: runtime pressure
      <br> Time is a measure of the execution time constraint imposed upon a software system.
      <br> We can optimize the program through enough tests to reduce the percentage of available execution time expected to be used by the system, which decrease Time.
    - Stor: main memory requirements
      <br> Stor represents the degree of main storage constraint imposed on a software system.
      <br> The software can be modified to reduce some redundant functions, then the percentage of the usage of available storage increase, and so dose Stor.
    - Pvol: platform volatility
      <br> Pvol means the complex of hardware and software the product calls on to perform.
      <br> We can maintain the stability of the software by testing and modifying, thus reducing the times of update, and reduce Pvol rating such as using Docker to build.
  - List 3:
    - Acap: analyst capability
      <br> ACAP shows the ability of analysts. 
      <br> We could cooperate with analysts who have high analysis ,design ability, competent efficiency and thoroughness, which could help increase Acap.
    - Pcap: programmer capability
      <br> Pcap evaluation is based on the capability of the programmers as a team. 
      <br> We could assign the project to programmers who have high ability, efficiency, and thoroughness in coding, which will increase Pcap.
    - Pcon: programmer continuity
      <br> The rating scale for PCON is in terms of the project's annual personnel turnover.
      <br> If the program is not tested enough, there might be more personnel turnover, which means the system is not stable enough and Pcon is low.
    - Aexp: analyst experience
      <br> Aexp is dependent on the level of applications experience of the project team.
      <br> We can cooperate with a project team who is more experienced with the application, so that Aexp rating would be increased.
    - Pexp: programmer experience
      <br> Pexp is related with the understanding of the use of more powerful platforms.
      <br> We could assign the project to programmers with high understanding of using more graphic user interface, database, and networking, then Pexp increased.
    - Ltex: language and tool experience
      <br> Ltex measures the level of programming language and software tool experience.
      <br> The program can be assigned to a team with experience of 6 or more years, so that the proficiency leads to the increase of Ltex.
    - Tool: use of tools
      <br> The tool rating tells whether software tools used in development is simple or mature.
      <br> The use of strong, mature, and proactive lifecycle tools, could help to make development easier, and increase Tool rating.
    - Site: multiple site development
      <br> Site is determined by site collocation and communication support.
      <br> If we can use international distribution and full interactive multimedia instead of some surface mail and phone access, the Site will increase.
    - Sced: length of schedule
      <br> The Sced rating measures the schedule constraint imposed on the project team.
      <br> We can manage our timetable to make sure more issues are solved in the earlier phases of development, so that Sced will increase.

	
##Theory 2: Treatments (management actions)

        @rx
        def improvePersonnel(): return dict(
          acap=[5],pcap=[5],pcon=[5], aexp=[5], pexp=[5], ltex=[5])
The method will improve personnel’s ability to analyze and programming such as giving them some training, which increase these personnel factors.

        @rx
        def improveTeam(): return dict(Team = [5])	
Improve team cohesion such as running some team activities to build team spirits or arranging some competition among different teams.

         @rx
        def relaxSchedule(): return dict(sced = [5])
Postpone the original schedule or just give more time at the planning phase of the project, which will relax the tight schedule.
  
##	Projects
###	Difference between flight and ground

- Difference 1: the kloc in flight is from 7 to 418 while the kloc in ground is from 11 to 392
- Difference 2: the cplx in flight is [3,4,5,6] while in ground is [1,2,3,4]
- Difference 3:the rely in flight is [3,4,5] while in ground is [1,2,3,4]

###	Difference between osp and osp2 

- Difference 1: the prec in osp is [1,2] while in osp2 is [3,4,5]
-	Difference 2: the tool in osp is [2,3] while in osp2 is [5]
-	Difference 3:the site in osp is [3] while in osp2 is [6]

## 	Bad Smells

        Stink[('sced','rely')] =
        [[0,0,0,1,2,0],
         [0,0,0,0,1,0],
         [0,0,0,0,0,0],
         [0,0,0,0,0,0],
         [0,0,0,0,0,0],
         [0,0,0,0,0,0]]
         
As you can see that the time schedule is very tight, however the required software responsibility is high, which will lead to a bad smell.

        Stink[('sced','aexp')] = 
        [[4,2,1,0,0,0],
        [2,1,0,0,0,0],
        [1,0,0,0,0,0],
        [0,0,0,0,0,0],
        [0,0,0,0,0,0],
        [0,0,0,0,0,0]]
From the table we can see that the time schedule is very tight, while the analyst team is not very experienced, therefore will lead to bad smell.

        Stink[('rely','pcap')] = 
        [[0,0,0,0,0,0],
         [0,0,0,0,0,0],
         [1,0,0,0,0,0],
         [2,1,0,0,0,0],
         [4,2,1,0,0,0],
         [0,0,0,0,0,0]]
From the table we know that the programmers are of low capability, while required reliance is high, therefore a software failure is only at the corner.


## Practice

###Result

####Smells
<img src=smell.png />

####Effort
<img src=effort.png/>
- As you can see the Treatment perfectTeam improved the efforts but worse the bad smells.
- As you can see the Treatment easyTaskExtendDeadline improved the badsmells but worse the effort.	
- As you can see the Treatment improvePlatformandPersonnel both improved the bad smells and the effort
 
More on https://github.com/jessexu20/COCOMO/blob/master/src/

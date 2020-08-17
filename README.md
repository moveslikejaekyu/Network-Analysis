### Network-Analysis
What i studied and did with Network analysis.
In this page, gonna write what i did with network analysis with projects first, and new things that i studied(ex. node2vec, GNN etc..)


# Project (Network analysis with Yonsei Edu-data)

Now i'm in master of Industrial engineering, Yonsei Uni. Really happy to study data science with variational domains and techniques. </br>
And the most happiest thing is, i can particiapte many projects concerned with data science. This can make me learn many domain issues and related machine learning techiques!
Though we study Machine learning and data scinece really deeply and be clevered, it is useless if we can applied to real-world problems.
So i think projects are really important for upgrading my personal ability to cope with real-world problem (because i dont want to remain in academic area but want to be kinda data analyst,engineer ) </br>

In this section - Network analysis, im gonna introduce my first project.
The whole project name is "Research on Development of Education System based on Big Data Analysis".
This project aims to develop a future-oriented convergence education research model that can combine various majors. 
It is a study that utilizes big data in the field to break away from the existing one-sided education methods and come up with measures to realize personal-tailored 
precision education. 
Based on the collection and analysis of educational big data, the CTL model can be developed and an artificial intelligence-based diagnostic system can be established. 
To this end, we would like to present an education platform based on artificial intelligence and big data, which is the core of the Fourth Industrial Revolution.
Through research, we hope to secure the ease of personalized education that utilizes educational big data and realize education that maximizes the ability of learners according to their understanding of learning. 
It also expects to realize better education by sharing the results of the big data analysis of education with professors to induce the development of new teaching techniques.

And my role in here was finding kinda new&hidden educational issue in Uni with Yonsei edu-data.
So i did Network analysis with edu data.
The edu - data : i made this from YONSEI EDUCATIONAL DATABASE, used many interesting tables (Classes taken by several students, class info data, major info data etc...) 
This database is established using 'YSCEC' data, a learning management system that supports online and offline integrated education of Yonsei University. 
The 'YSCEC' data used in this study is intended for the entire 'YSCEC' data for 2016 and 2017.Usage data was generated from approximately 118 million data by database, 426 tables (classes), 1429 Object Properties indicating connectivity between tables, 3426 Data Properties representing column relationships belonging to the table, and about 1 billion RDF-type Triple.



[3] 네트워크 분석을 이용한 수업간의 연결관계 및 융합학과 집단 발견모델 개발
 
[3.1] 개요
Network analysis is a method of quantitatively analyzing the structure or diffusion process of individuals and groups by modelling them into nodes and links. 
This has recently drawn much attention in the fields of social science, including sociology, economics, and business administration, as well as natural sciences such as physics, medicine and biology. 
The increase and accumulation of big data due to the development of Internet services is also increasing opportunities to utilize network data in practice.
There are many things around us that exist in the form of a network, such as Internet networks, road networks, telecommunications networks, and power grids. 
As such, the network has always existed around us and provides the main environment for moving the socio-economic system. 
Therefore, this network analysis can serve as an important methodology for understanding the connections and interrelationships of components in the network structure and increasing the efficiency of the network as a whole.

These network-type data were found in this study. 
Usually, this structure could be found in a large frame. 
The first discovery was a network between tables in a self-built DB that organized YSCEC data. 
Through the network between these tables, we were able to see clusters of tables tied together with similar attributes through community detections. 
When I looked at the DB in detail, I could see the categories and clusters by table that I could refer to. 
Following these attempts, I thought that I could cluster data that can be extracted from DB through network analysis. 
[Figure 1] is visualized and tabulated.

네트워크 분석이란 개인과 집단들의 관계를 노드와 링크로 모형화하여 그것의 구조나 확산과정을 계량적으로 분석하는 방법이다. 이는 사회학, 경제학, 경영학을 비롯한 사회과학 분야에서뿐만 아니라 물리학, 의학, 생물학 등의 자연과학 분야에서도 최근 많은 주목을 받고 있다. 인터넷 서비스의 발달로 인한 빅데이터의 증가 및 축적은 실무적으로도 네트워크 데이터의 활용 기회를 증대시키고 있다.
인터넷 네트워크, 도로 네크워크, 통신망, 전력망과 같이 우리 주변에는 많은 것들이 네트워크 형태의 구조로 존재하고 있다. 이와 같이 네트워크는 우리 주변에 언제나 존재했었고  사회경제시스템을 움직이는 주된 환경을 제공하고 있다. 때문에 이런 네트워크 분석은 네트워크 구조안의 구성요소들의 연결 및 상호관계를 이해하게 하고 네트워크 전체의 효율성을 높이는 중요한 방법론으로서 역할을 할 수 있다.
이번 연구에 있어서 이러한 네트워크(망) 형태의 데이터들을 발견할 수 있었다. 대게 큰틀에서 이런 구조를 발견할 수 있었다. 처음으로 발견한 것은 YSCEC데이터를 정리한 자체 구축 DB에서 테이블간의 네트워크이다. 이 테이블간의 네트워크를 커뮤니티 디텍션을 통해 우리는 테이블들이 비슷한 속성끼리 묶인 군집을 볼 수 있었다. DB를 세부적으로 살펴볼 때 참고할 수 있는 테이블별 카테고리, 군집을 알 수 있었다. 이런 시도에 이어 DB에서 추출할 수 있는 데이터들에서도 네트워크 분석을 하여 군집화를 해볼 수 있다는 생각을 했다. [그림1]은 이를 시각화하고 표로 정리한 것이다.


![noname01.png](깃헙이미지/noname01.png)
[그림1] DB 테이블들의 네트워크 그래프(Community Detection 통한 군집화)


I explored the structure of DB to find this data. To explain the structure in detail, in each 'lecture' place, a small number of administrators or a number of behaviors that occur when a participant 'student' interacts with each other were stored in a table. 
Since the YSCEC data itself is stored on the homepage of each lecture, tables (quiz, assignment registration, questions, discussions, etc.) were mainly used to store data for each activity performed within the lecture, and tables were available for information about the lecture and information about the students who took it.
This study explores all lectures and tables that can be applied to students as much as possible. For example, when it comes to tables that store data about 'discussion boards,' there were many lectures that were actively used, but not so. Therefore, the use of the data in this table will result in the exclusion of a large amount of lectures during analysis, which will lose the advantages of big data and lack the entire nature of Yonsei University's education system. Therefore, I explored the subject by looking for tables where more lectures and student data are available. 
Figure 2 shows the Excel sheet used to explore these tables. It went through a process of exploring tables with a large number of data one by one.
이런 데이터를 찾기위해 DB의 구조에 대해 탐색했다. 구조에 대해 풀어서 설명한다면 각 ‘강의’라는 장소에서 ‘학생’이라는 참여자가 소수의 관리자 또는 그들끼리 상호작용하며 생기는 여러 행위들이 테이블로 저장되었다. YSCEC데이터자체가 강의별로 개설되는 홈페이지에 저장되는 데이터들이기 때문에 그 안에서 이루어진 각종 행위에 대해 행위별로 데이터를 저장하는 테이블들(퀴즈, 과제등록, 질문, 토론 등등)이 주였고 강의에 대한 정보와 이를 수강한 학생정보에 관한 테이블이 있었다. 
 본 연구는 최대한 모든 강의와 학생들에게 적용할 수 있는 테이블을 탐색한다. 예를들면 ‘토론게시판’에 관한 데이터를 저장하는 테이블에 관해 말해보자면, 이 테이블을 적극적으로 사용한 강의들도 있지만, 그렇지도 않은 강의들도 많았다. 때문에 이 테이블의 데이터를 이용하게 된다면 분석시 많은 양의 강의에 대해서 제외하게 되므로 빅데이터의 장점이 손실되며 연세대학교 교육시스템이라는 전체의 속성이 결여된다. 때문에 보다 많은 강의와 학생들 데이터를 이용할 수 있는 테이블들을 찾아 주제를 탐색했다. 그림2는 이런 테이블들을 탐색할 때 사용한 엑셀시트이다. 데이터갯수가 많은 테이블부터 차례차례 탐색하는 과정을 거쳤다.



![noname02.png](noname02.png)
[그림2] DB 테이블들의 이름, 행(데이터)개수, 그리고 설명을 정리한 엑셀시트

The tables that exist in common for all lectures did not really exist. 
Some lectures are enthusiastically used by YSCEC, but others are not even used at all. 
However, the basic information about the lecture and the students taking the course were entered, and the YSCEC for each lecture was opened, so we looked up if there was a table containing the lecture information and student information. 
There existed a lecture information table for almost all lectures and a table with the serial numbers of the students who took the course. 
Using this method, we were able to make a list of courses for each student, and through this, we thought that we could derive the connection relationship between subjects in a network format and analyze various kinds of subjects. 
Based on this, we started to study the subject of 'Connection Relationship Between Classes Using Network Analysis and Development of Convergence Studies and Group Discovery Model'.
모든 강의에 대해 공통적으로 존재하는 테이블은 사실 존재하지 않았다. YSCEC을 열렬히 이용하는 강의들도 있지만 아예 사용조차 하지않는 강의들도 있기 때문이다. 허나 강의에 대한 기본적인 정보와 수강하는 학생들에 관한 정보는 입력된 후 각 강의별 YSCEC이 개설되는 점에서 강의정보와 학생들정보를 담는 테이블이 있는지 조회했다. 거의 모든 강의에 대해 강의정보 테이블과 수강한 학생들의 일련번호가 저장된 테이블이 존재했다. 이를 이용해 학생별 수강과목들 목록을 만들 수 있었고 이를 통해 과목별 연결관계를 도출하여 과목끼리의 관계를 네트워크 형식으로 도출 및 각종 분석을 할 수 있을 것이라 생각했다. 이에 기반해 ‘네트워크 분석을 이용한 수업간의 연결관계 및 융합학과 집단 발견모델 개발’ 주제의 연구를 시작하게 되었다.

![Deep learning](certificate_deep_learning.png)
[그림28] M_HAKSA_CLASS_STUDENT 테이블 - 강의이름과 수강한 학생의 일련번호 저장

![Deep learning](certificate_deep_learning.png)
[그림29] 학생별 수강과목 목록을 list형식으로 저장한 txt파일 

[3.2] Experiments
Using the list of student-specific courses derived from the "M_HAKSA_CLASS_STUDENT" table, the network matrix was derived to calculate the number of common students in each subject, use it as a link weight, and create a network of subjects as nodes. 
This is a matrix of rows and columns of lectures, and for this purpose, the number of concurrent lecture-course classes for each student was calculated using python. 
For example, when a student had a course list of "Modern Society and Psychology," "Cultural Anthropology of the Global Age," "Computer Graphics Design," and "Material Analysis Theory," 
it was calculated that he would be +1 in the line of "Modern Society and Psychology" and "Cultural Anthropology of the Global Village Era." 
In other words, each value is the number of students who took two classes simultaneously during the entire course. 
The total number of classes was about 20,000, so about 20,000 x 20,000 Matrixes were calculated. 
Through this calculated Matrix, i decided to identify the connections and strength of connections between subjects and to use Community Detection among subgrouping methods of prior research.

M_HAKSA_CLASS_STUDENT 테이블을 통해 도출한 학생별 수강과목들 목록을 이용해서과목별 공통된 수강학생들의 수를 계산하고 이를 링크(edge) weight로 사용하고, 과목들을 노드로 하는 네트워크를 만들고자 network matrix를 도출했다. 강의를 행과 열로 하는 matrix이며 이를 위해 학생별로 강의-강의 동시 수강 횟수를 python을 이용해 계산하여 기입했다. 예를 들면 학 학생이 
['현대사회와심리학', '지구촌시대의문화인류학', '컴퓨터그래픽디자인', '재료분석론']의 수강목록을 가질 때, '현대사회와심리학'행과 '지구촌시대의문화인류학'열에 +1이 되게 계산했다. 즉 각 값은 두 개의 수업을 전체 수강내역중 동시에 수강한 학생들의 수이다. 전체 수업의 개수가 약 2만개이기 때문에 약 2만 x 2만 Matrix 산출이 되었다. 이렇게 산출된 Matrix를 통해 과목들간의 연결관계 및 연결강도를 파악하기로 했으며 선행연구의 Subgrouping 방법 중 Community Detection을 이용해보기로 했다. 

![Deep learning](certificate_deep_learning.png) 
[그림30] 2만 x 2만 Matrix의 일부

However, the disadvantage is that the size of the data is too large at 20,000 x 20,000 matrix, resulting in longer analysis and computing times. 
Therefore, we rewritten Matrix, where only classes that fit the subject of analysis are lined up and worked hard. 
Classes were limited to Sinchon, undergraduate majors and optional liberal arts classes on future campuses, while classes on international campuses, graduate schools, compulsory liberal arts, affiliated foundations and seasonal semesters were excluded. 
Sinchon, the task of summarizing only undergraduate majors and elective liberal arts classes on future campuses was sorted out and sorted out the departments and majors belonging to each class using the M_COURSE_CATEGORY table. A total of 5024 subjects were reconstructed, approximately 1/4 of the nodes and significantly reduced analysis and calculation time.
Network graphs are generated using Python module NetwrockX and Gephi, a visualization and analysis tool. We used NetwrockX to create additional graph weighting and gxef file, and we used it to do various visualizations and analyses using Gephi.
Community Detection was performed with one analysis. Detection was performed through the adjustment of the Resolution coefficient. The Resolution coefficient was 0.3,0.5,0.7,1 and so on, and the Modularity values added from each were compared. 
When the Resolution coefficient was 0.5, the Modularity value was the largest with 0.573, and this Resolution coefficient was used to determine the optimal network graph.

허나 2만 x 2만 matrix로 데이터 크기가 너무 커 분석 및 컴퓨팅 시간이 길다는 단점이 있다. 때문에 분석 주제에 맞는 수업들만 행과 열로하는 Matrix를 재작성했다. 수업에는 신촌, 미래 캠퍼스의 학부 전공 및 선택 교양수업만으로 한정했고 국제캠퍼스, 대학원, 필수교양, 계열기초, 계절학기 수업은 제외시켰다. 신촌, 미래 캠퍼스의 학부 전공 및 선택 교양인 수업들만 간추려내는 작업은 M_COURSE_CATEGORY 테이블을 이용하여 수업마다 소속된 학과, 전공교양 여부를 알아내어 분류하였다. 총 5024개의 과목들로 재구성되었으며 약 노드 수가 1/4이되며 분석 및 계산시간이 월등히 줄었다. 
 네트워크 그래프는 파이썬 모듈 NetwrokX와 시각화 및 분석 tool인 Gephi 이용하여 생성한다. NetwrokX를 이용해 추가적인 그래프 경량화 및 gxef파일을 생성했고 이를 Gephi에 이용하여 각종 시각화 및 분석을 실시했다.
 한 분석으로 Community Detection을 실시했다. Resolution 계수 조정을 통해 detection 실시했는데 이때 Resolution 계수 0.3,0.5,0.7,1 등등 다양하게 실시하였고 각각에서 더출된 Modularity 값을 비교했다. Resolution 계수가 0.5일 때 Modularity 값이 0.573으로 가장 크기에 이 Resolution 계수값을 이용한 것이 최적의 네트워크 그래프라 판단했다.


![Deep learning](certificate_deep_learning.png)
[그림31] 연세대학교 수업 네트워크 커뮤니티 

The above picture is 'Yonsei Uni's Class Network Community Graph'. 
Nodes bound together in the same community were marked in the same color. The number of communities is 27 and the graph density is 0.08. 
We used this network and started in-dept analysis

First, I checked the assigned class list for each community. It was necessary to see what the classes assigned to each community were and what the commonalities were. 
Since it is difficult to identify commonalities only by the names of classes, the department of belonging to the classes was further labeled. 
This work also used the M_COURSE_CATEGORY table to find out which departments belonged to each class.
위 그림은 ‘연세대학교 수업 네트워크 커뮤니티 그래프’이다. 같은 커뮤니티로 묶여진 노드끼리 같은 색깔로 표기되었다. 커뮤니티 개수는 27개이며 graph density는 0.08이다. 이 네트워크를 이용해 세부분석을 실시했다.
우선 각 커뮤니티별 할당된 수업리스트들을 확인했다. 커뮤니티별로 할당된 수업들이 어떤 것들인지, 공통된 점들이 무엇인지를 확인해볼 필요가 있었다. 수업들의 이름만으로는 공통점을 확인하기가 어렵기에 수업들의 소속학과를 추가적으로 라벨링했다. 이 작업 또한 M_COURSE_CATEGORY 테이블을 이용하여 수업마다 소속된 학과를 알아낼 수 있었다.

![Deep learning](certificate_deep_learning.png)
[그림32] 강의의 소속학과 라멜링 예시

After labelling departments in each class, detailed analyses were now conducted for each community. 
By checking the number of departments in each community, we explored what is common in the community. 
수업별 소속학과 라벨링 후 이제 각 커뮤니티마다 세부적인 분석을 실시했다. 커뮤니티마다 소속학과 수를 확인해봄으로 커뮤니티의 공통된 점이 무엇인지를 탐색했다. 
     

![Deep learning](certificate_deep_learning.png)
[그림33] 각 커뮤니티의 소속학과 수 예시
After checking the number of departments under the table, the results of the three-part class were derived in histogram. 
What is certain about each community is that it was named after specific departments and colleges, and the newly determined community of unfamiliar combinations of departments was named "convergence".
표를 통해 소속학과 수를 확인해본 후 세부분석 결과를 히스토그램으로 도출했다. 커뮤니티별로 속성이 확실한 것은 특정과 및 단과대 이름을 붙여 네이밍했으며 새롭게 판단되는, 익숙하지 않은 조합의 학과들로 어우러진 커뮤니티는 ‘융합’으로 네이밍했다.



![Deep learning](certificate_deep_learning.png)
[그림34] 각 커뮤니티별 세부분석 결과 히스토그램
A total of four convergence communities were determined and the convergence (2) communities were analyzed in detail.
총 4개의 융합 커뮤니티가 있다 판단했고 그 중 융합(2) 커뮤니티를 세부적으로 분석해보았다.

![Deep learning](certificate_deep_learning.png)

[그림35] 융합(2) 커뮤니티 정보
The convergence2 community had 260 nodes, or 518% of the 5,024 nodes. Among them, clothing, environmental studies, media promotion and video studies, and daily design majors accounted for most of them. 
Nodes marked as College of Living Science and College of Social Sciences were also all three departments after class inquiry. 
In what way did these three departments become integrated? Based on the Department of Media Promotion and Film Studies (Sociological Science College), the two remaining majors were compared. 
We drew out how classes in each department were connected and which classes were most connected. 
This was done after the reconstruction of rows and columns consisting only of the classes in the Cabinet from the initially derived network matrix.
 융합2 커뮤니티는 5024개의 노드중 5,18%인 260개의 노드가 존재했다. 그 중 의류환경학, 언론홍보영상학, 생활디자인전공이 대부분을 차지했다. 생활과학대학, 사회과학대학으로 표기된 노드들 또한 수업조회를 해본 결과 모두 3개의 학과의 수업들이였다. 이 3개의 과는 어떤 점에서 융합되게 되었을까? 언론홍보영상학부(사회과학대학)을 기준으로 나머지 2개의 전공들을 비교했다. 각 과의 수업들이 어떤식으로 연결되어있는지, 어떤 수업이 가장 연결이 많았는지를 도출했다. 이는 처음에 도출한 network matrix에서 각과의 수업들로만 이루어진 행과 열로 재구성 후에 실시했다. 

![Deep learning](certificate_deep_learning.png)

[그림36] 언론홍보영상학부와 의류환경학의 수업 연결성

[그림37] 언론홍보영상학부와 의류환경학의 높은 연결성을 가지는 수업
Ten classes with the highest degree of connection between the Department of Media Promotion and Film and the Department of Clothing and Environmental Studies have been selected. 
There is a media introduction, interpersonal relations and communication.
언론홍보영상학부와 의류환경학의 연결된 수업들 중 가장 높은 연결도를 가진 수업들 10개를 추려냈다. 언록한개론, 대인관계와 커뮤니케이션 등이 있다.

![Deep learning](certificate_deep_learning.png)

[그림38] 언론홍보영상학부와 생활디자인전공의 높은 연결성을 가지는 수업
I have selected 10 classes with the highest degree of connection among the linked classes in the Department of Media Promotion and Film and the Department of Life Design. 
There is an unpublished introduction, communication design workshop, etc.
In fact, as a result of consulting with a professor of journalism and video, he said that students in the department of media promotion and video studies take classes in daily design to take computer classes related to video production or design, which are not open on confectionery. 
In comparison to this advice, it can be seen that the need for a convergence of two departments exists in students. Through this result, it is possible to propose the opening of a convergence department or a convergence class group.
For future analysis, we will try to find convergent needs by removing the connection diagram between oligarchs, creating an ego-network for each unit, and then trying several more.

언론홍보영상학부와 생활디자인전공의 연결된 수업들 중 가장 높은 연결도를 가진 수업들 10개를 추려냈다. 언록한개론, 커뮤니케이션디자인워크샵 등이 있다.
실제로 언론홍보영상학부 교수님에게 자문 결과, 언론홍보영상학부 학생들은 과자체에 개설되지 않지만 그들에게 필요한 역량인 영상제작 또는 디자인 관련 컴퓨터 수업을 듣기 위해 생활디자인전공의 수업들을 듣는다고 했다. 이런 자문에 빗대어  생각해 봤을 때, 두 개 학과의 융합적 과목 개설 소요가  학생들에게서 존재한다는 것을 알 수 있다. 이 결과를 통해 융합학과 개설이라던지, 융합 수업 군 개설에 대한 제안이 가능하다.
향후 분석으로는 과끼리의 연결도를 제거 후 community detection 실시, 단과대별로 ego-network를 만든 뒤 분석 등 여러 개를 다시 시도하여 융합적인 니즈를 발견해 보려한다.








                

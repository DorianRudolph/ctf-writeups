**DISCLAIMER**: Solved after competition ended.

# Challenge

We are given the following python script: [cactus.py](./cactus.py) and output file [output.txt](./output.txt)

```python
import random


class Oracle:

    def __init__(self, secret, bits=512):
        self.secret = secret #flag
        self.bits = bits #512
        self.range = 2*self.bits #1024

    def sample(self, w):
        r = random.randint(0, 2^self.range) #random number from 0 to 1026 inclusive
        idx = range(self.bits) #range(512)
        random.shuffle(idx) #shuffle range(512)
        e = sum(1<<i for i in idx[:w]) #in binary, e should have 10 "1"s 
        return self.secret*r+e #10*r + e


o = Oracle(flag)
for i in range(100):
    print o.sample(10)
```

```
85720688574901385675874003924800144844912384936442688595500031069628084089994889799455870305255668650207573833404251746014971622855385123487876620597588598431866760767383346912312450930789335025523091583845145848492010576266010285780099843929938835071916767707164625955551912287459939023260166124120548
77962512091199992642827059103001506487009814860760060214943251657703589526131408819724920527056082073802439329851269345467673358921624752372623898370501227356250221599651784239005396992497785771736767609833510020797652143800064595937159499486139012761943257892728932858762721697361153716679
145216494968533502226373290834951226575318379068300240142165220636322329800820739604020343212515268612285031620136032524458455590385244897842744179708627222925163472259137889329394583992635708506515170349215946969853734219087482706531412663408992720759874962371162227167703292067604
22471164185778948846616314884862809170224712236778832159178760144716584475687620391588559665300942002640014234983924169707348721101802077811605928829934265547221036626086479281120923604551224746215443805310519089515940482966241314186233140024534576660574205213909320073515804505415815206736944724902636289403
10715086071862673209484250490600018105614048117055336074437503883703510511249361224931983788156958581275946729175531468251871452856923140435984577574698574828908557712435554548795605606360818608195907503311214056517854351586894471544596503031194175617992995177613913469268092589226525764572615136625915
83711609936427134449095706957812641450109750914494813081542999091433675869135634569781123344976238916218333821683839595717745725444712034656129512302332615655738810740814304573772573844013130143257849334335151454694606825948958789024566572000709118055392397316650930583951520687266298746716324533338
8452712498170643941637436558664265704301557216577944354047371344426782440907597751590676094202515006314790319892114058862120757622558492172053558495585505439214406886312646108658799916551376686099411333286760918946150935698631582622272715720115132079687043280791169658931
351111940402796075728379920075981393284761128699669252487168127261196632432619068618571244770327218791250222421623815151677323767215657465806342637967722899175377864822245456805979878214360469469266170933566706583365032942320547198544215195110325759845103362710160915853638965534448609252906992916439609319
1161731959748268017810986326679609812602547032546401921137321765090578638406565916832162745700122148898280252961088260195667644723081957584211587135769099480095724084240046491248164193448749512281751691043358042226458499617816929886799317721373524952063558621930155069358585399333717
297403381695556612559612499629980112026252040331878891811154371863188131432080874709033662899231270117959744758038594610090917049108981141558166116220478925156594168089511675791635479206467839216996225169817520075125956963684147588572955531872842910066758287245007647860898778639934882
1339385758982834151185531311325002263201756014631917009304687985462938813906170153116497973519619822659493341146941433531483931607115392554498072196863508975354990106813134390752255118850529529103093270574620004629990773738080607036119275832101034750699020032879480878966213604961865524588200665005185
159667224762777584932509817042947085285396100834836603320203779394976951349517125262796637239410856087147395747535399619517795039071487492859135380558090461813193075810349065766058793745334953152473502139587234739746583621077620007931338971819555253302259203413930262857721639881869726961492234
1081947199765842424529591879509026010150599323721976877318063532086628152436172512203606540057921920808293160946190599534351047801861499980289103827892100253508375928830535787031560937623887814768444444943859391209084349575316804965918177828995719471527769368932307731553790
148701690847778306279806249814990056013126020165939445905577185931594065716040437354516831449615635058979872379019297305045458524554490570779083058110239462578297084044746295222442050315311446351563932198579105320070235225680682964083143740146348664506862779239154638173400356225918816
5357543035931336604742125245300009052807024058527668037218751941851755255624680612465991894078479290637973364587765734125935726428461570217992288787349287401967283887412115514372019287850051661395337904694374278204527531522714560919855948730287987848637250835919852544336533786513820660273546879804075
8863311460481781141746416676937941075153709659930434578989576454853657824757125219971944776154496375261537574471193391385403783592849407838528701977454233080185890270878996084464165942609211014284748915047110917272595311176039037567152579581785763754694379694231278333135521387
1161731959748268017810986326679609812602547032546401921137321765090578638406565916832162745700122148898280252961088260195667644723081957584211776927896787548976239672102986518888755417552230506964664251042563745464743562678051719737361277423828739443863270016065889226064541127927908
359538626972463181545861038157804946723595395788461314546860162315465351611001926265416954644815072042240227759742786715317579537628833244985694861278948248755535786849730970552604439202493499577074388402400498243158051537630093520676944045909757836230242036435558063188536396495306266644606160898048020563195
4646927838993072071243945306718439250410188130185607684549287060362314553626263667328650982800488595593121011844353040782670578892327830336846345565944983205571783876398312106070895030732185951410587098716624237888995296119907919644674780980684438586149399080602200662425858681751448
4431655730240890570873208338468970537576854829965217289494788227426828912378562609985972388077248187630768787235596695692701891796424703919264169279739294679646766549289708608946844833317445633863756179467420618184215060293506500998236840469763391195936057754551259721035062460
623700096729599941142616472824012051896078518886080481719546013261628716209051270557799364216448656590419514638810154763741386871372998018980991186964009818850001772797216856161608624859953089447941924658316197090625826548628827547907855328132989590724317892086006856556601989563821604691218
540973599882921212264795939754513005075299661860988438659031766043314076218086256101803270028960960404146580473095299767175523900931131062965635409430025778999138359382484748610516416882189568444936392068785674132028613974905644144899301786213818162927862230434819218818126
10715086071862673209484250490600018105614048117055336074437503883703510511249361224931983788156958581275946729175531468251871452856923140435984577574698574803934567774824253166778627652276575698668158836811955398841520068662456511723021499156660175313963247088697935532352930734671513362126665895008119
159667224762777584932509817042947085285396100834836603320203779394976951349517125262796637239410856087147395747535399619517795039071487492859133743862786513625600453836086859285902773889366791661104615719368190207102819799538777727377670945215446697493154124229810855808129735550943560973298173
5357543035931336604742125245300009052807024058527668037218751941851755255624680612465991894078479290637973364587765734125935726428461570217992288787349287401967283887412115492715825750282123216077411077278491487973790504406543832317523579182308505755804013464492471785326137262169188550698061041588779
9745314011399999080353382387875188310876226857595007526867906457212948690766426102465615065882010259225304916231408668183459169865203094046782574245889153110422636017511290518448248203408439583591337211408330868450034790838552449125145946116894317042715149545350973764521048789039486471266
74350845423889153139903124907495028006563010082969722952788592965797032858020218677258415724807817529489936189509648652522729262277245285489439006956515816674279843327297282708238070502393595891859790351629882625237283796041281410290145165244877625826193733026903280052020319631457476
1189613526782226450238449998519920448105008161327515567244617487452752525728323498836134651596925080471838979032154378440363668196435924567880947699448759598795860009688760324320909146425001257246341350867386266962208055363398605354835167417678563211098125950567819367161133447969044992
20437404769635530871361256581497226916530700906859085224986083762557049772738192033637969566644589579154866655684531151298277765001150399085969119214436673744077039889425621441128299105051503169429932398813504876495023575579413568410888391131735757008758013612182949408319961820768370042717386855
67621699985365151533099492469314125634412457732623554832378970755414259527260782012725408753620120050518322559136912470896940488396780886347067047088655578336021865127515525611566876820567910210575445582822515465515632025654083110563932972733858026811597709914842515743124
40874809539271061742722513162994453833061401813718170449972167525114099545476384067275939133289179158309733311369062302596555530002300798171938238428873347488153716182038234655159867843880164041258583559511279499109101755781202798770688947417171893182213567247152974050399156275867533908400304880
359538626972463181545861038157804946723595395788461314546860162315465351611001926265416954644815072042240227759742786715317579537628833244985694861278948248755536186433548396853089462400043978386396105647359397412707961424727694414984050249644847764724763430179227511828838173555217184325112189503207066455249
74350845423889153139903124907495028006563010082969722952788592965797032858020218677258415724807817529489936189509648652522729262277245285789125343495566736905992992600399268319465699392144923906821623416233191393260559936009087469960046121079493785095752490157587836333360565012108130
9293855677986144142487890613436878500820376260371215369098574120724629107252527334657301965600977191186242023688706081565341157784655660673692691155148805588602988250374986083346275822971560815740039900678135223179429653037092839476383536290569806981316560131688492690542477636423955
36304123742133375556593322708737806643829594767075060035541305159080582450205184901005085803128817153071257905034008131114613897596311176067486349891941296984328176430944966202977938760093207389106299714962750971179498382659687045785827267034944935560722992622501168326638837853325
669692879491417075592765655662501131600878007315958504652343992731469406953085076558248986759809911329746670573470716765741965803557696277249036098418660925248959068495182397752276399423587609413519748511900528183632475314191298922750800481986046714625783379325807330023181085822126007288073779620844
276978483140055660679575521154310658598553426872826080593424264214176807023660163124123274254828011726923049202224793480793868237276543994954010579941731507522226666911123900119507028261051424387805070550330658000657217345482578532536874324606900994300621977954606994862044524
9293855677986144142487890613436878500820376260371215369098574120724629107252527334657301965600977191186242023688706081565341157784662207454908483415629992790537222951101365324407285524007143919818064189531501158400812603788282223357572758763234445034644871275137112123951439737030366
567251933470833993071770667324028228809837418235547813055332893110634100784456014078204465673887768016738404766156377048665842149942362126054474217061582934610455845841168821401927446449150527045611339810008737718307797490794841655374200163671846174179648970690420693374879093275
159667224762777584932509817042947085285396100834836603320203779394976951349517125262796637239410856087147395747535399619517795039071487492859133743862789752744579663545161489530408639880243530828659603173671123038747526644471752833501955931466038989786002878164330845473717678038847531046752036
653996952628336987883560210607911261328982429019490727199554680401825592727622145076415026132626866532955732981904996841544888480036812770751015166813956045459734352419554473366328834119276779101362128554347259599714986906389809073778441118255102375688973300943691759755458571150647907565314858605
638668899051110339730039268171788341141584403339346413280815117579907805398068501051186548957643424348589582990141598478071180156285949971436744472450051407582094016340011501689097573451821672960687408433628577848435532591664046831389609335129720404094434594085911908663121795402270303324435432
1307993905256673975767120421215822522657964858038981454399109360803651185455244290152830052265253733065911465963809993683089776960073625541502023629723953558227304126268881807408542606862240002849992359867807260788619881309930209952024698380097980725443859211757889801027586372014751263455146382095
163499238157084246970890052651977815332245607254872681799888670100456398181905536269103756533156716633238933245476249210386222120009203192687752953715505876946816128708169143785719122244258867040414563109905928471258342522439719183811764179425095175317515765664349784911965957366447433494458266030
594806763391113225119224999259960224052504080663757783622308743726376262864161749418067325798462540235919489516077189220181834098217962283116332422977368392061099512996944851852798598172392803249685563012942740962308730476701384742029251127242493756986151198453962871668725632875753159
2163894399531684849059183759018052020301198647443953754636127064173256304872345024407213080115843841616586321892381199068806844103175676500418629726082683679892609654495023689529471608158323216637330194189031812759774289538845061942787723043201781320051714573855317145816030
4327788799063369698118367518036104040602397294887907509272254128346512609744690048814426160231687683233172643784762398137410737988661792204896796592682903677900827234712129428596729250905294698192055777617142561088753032239172268274672860398384533461996261812368082480966859
148701690847778306279806249814990056013126020165939445905577185931594065716040437354516831449615635058979872379019297305045458524554490570779083058110239463964632096371667343151607240502897242667017348664528831607743024532978066179857437920768440771485072616445382464955267751676741862
9979201547673599058281863565184192830337256302177287707512736212186059459344820328924789827463178505446712234220962476219862189941967968303696677339076131137067531662179635282375742767733325702110773286648907343319545508402941396524811219606784968749216310477584613366720132737962925832939088
4872657005699999540176691193937594155438113428797503763433953228606474345383213051232807532941005129612652458115704334091729584932601547023288993648156326709765985433690001616794646984492906400747029073439396844847697832004658105225772707111772913077971282735661740575017221540436538353269
179769313486231590772930519078902473361797697894230657273430081157732675805500963132708477322407536021120113879871393357658789768814416622492847430639474124377767894985787406166353360914933998290290910299620026999807155017813670481233383255417776674856992887828967457557619353338756533987803114854584752856685
9293855677986144142487890613436878500820376260371215369098574120724629107252527334657301965600977191186242023688706081565341157784655660673692691131901323266210686615504914189778533471485492187297951022575828782974963289905506932510282680360039510620299677538418685921408311822153720
9979201547673599058281863565184192830337256302177287707512736212186059459344820328924789827463178505446712234220962476219862189941967968303695860589759414863433478252401685467348169888499357832383622817761652383936582296241099724304513913923999624228378302140251014627113139123367988631275973
4872657005699999540176691193937594155438113428797503763433953228606474345383213051232807532941005129612652458115704334091729584932601547023314567109835157515499874125162197815534891053126741051857880846141208360183312351887953221019967670852162024425293214415813079326109370344633183927007
33810849992682575766549746234657062817206228866311777416189485377707129763630391006362704376810060025259161279568456235448470243808171874384034667913484015473065471426822834329531962991810726221128724218371314821808352369599189379595727945159665499942637377732804878587147
81749619078542123485445026325988907666122803627436340899944335050228199090952768134551878266578358316619466622738124605193111060004601596343876476857746695738453074531088424631543294523053445482788727320618480540869213611467164521020792995312429240156489041322143025857135834897273591359090311898
2323463919496536035621972653359219625205094065092803842274643530181157276813131833664325491400244297796560505922176520391335289446163915169203609920551489660631291245667148632570794290638499404343424118565150787948004710146427490980591482014541519921724335417763233574205814738224862
2743062034396844341627968125593604635037196317966166035056000994228098690879836473582587849768181396806642362668936055872479091931372323951612051859122835149807249350401520810622713939896167192818731643405961386779355075558434070904780806607751798012403694245192097904543357118999910331529995920449814887
1161731959748268017810986326679609812602547032546401921137321765090578638406565916832162745700122148898280252961088260195667644723081957584211586391486245801392946049799966200996662487499828665083260184509792036152208095558938996492141515572047744045574559899111420151420361964271744
1247400193459199882285232945648024103792157037772160963439092026523257432418102541115598728432897313180839029277620309527482773742745996037961982373928019637700009090939146553206476900411375604610451825164571629236424498572615856048410099140129053665562014012019242374960930879612118565139667
19033816428515623203815199976318727169680130581240249075913879799244040411653175981378154425550801287549423664514470055045818691142974793059722632390792703918759890338537187861431689313883816383422340110815720441750435200753094041633273753375145081923163122467525355169128017114685514056
719077253944926363091722076315609893447190791576922629093720324630930703222003852530833909289630144084480455519485573430635159075257666489971389722557896497524165136131046508585261637530755429107286182655892919946076968295960365110100787970788790238048032560954488168453310887624733425979857590987387957672894
669692879491417075592765655662501131600878007315958504652343992731469406953085076558248986759809911329746670573470716765741965803557696277249036098418660931490169732564085251790679715438572684051185094922015546287209146940036967288321704497519203168294490366679046442286521512566226714945067886012194
171441377149802771351748007849600289689824769872885377191000062139256168179989779598911740610511337300415147666808503492029943245710770246975753241195177196875440078598451664692263582600170603493041659485108637282000341852384002669445941798140405630053436891576980218288855606882337518763004898080242114
39916806190694396233127454260736771321349025208709150830050944848744237837379281315699159309852714021786848936883849904879448759767871873221513527055531096091328941503356870875047358874972359013727954634412412754777064332919403067922140347416676768436088364776725560231114912584546819519571053
297403381695556612559612499629980112026252040331878891811154371863188131432080874709033662899231270117959744758038594610090917049108981141558172216362747675793726908961614194301132044565072721739433899367708446124438748170578933774155558137111625909114850756117694726888085361440732718
155925024182399985285654118206003012974019629721520120429886503315407179052262817639449841054112164147604878659702538690935346717843249504745247796741002454712500443199303568556813603923982149765415120110325124643590285169339388021450468398353145096395872730526615496112178992979520091746660
623700096729599941142616472824012051896078518886080481719546013261628716209051270557799364216448656590419514638810154763741386871372998018980991186964009865367680127716055269068454242857045592213817473453114616092973850532414337372824364941143078126378015374988469968260954309741532756553609
17311155196253478792473470072144416162409589179551630037089016513386050438978760195257704640926750732932690575139049592549616764829783999684625661246284180991982313188667661121890924870502715191934802824580964019039981171204184077833242592692849871616723952403685718772002788
2615987810513347951534240842431645045315929716077962908798218721607302370910488580305660104530507466131822931927619987366179553920147251083004047364196499831369088419808384290714052880838496380274971280245182183649850789409725056031358839868697514641328516672403212672252031450253181244895600988980
85720688574901385675874003924800144844912384936442688595500031069628084089994889799455870305255668650207573833404251746014971622855385123487876620597588703921603554476694185570839139454743316554551247612968485897604130301877529037512000791558017888294263189888230408621171227360759635828618824474598588
4758454107128905800953799994079681792420032645310062268978469949811010102913293995344538606387700321887355916128617513761454672785743698316077386107904879522847930549443689606963389546329617821972660370936414800169683792282616311794604743628215420196992534684378641537314064780184896367
70906491683854249133971333415503528601229677279443476631916611638829262598057001759775558209235971002092300595769547131083230321117044989046496651389481965693226690004442149851303729022248881233857717484428371431896448354263332141267112194631838366169052781496189561081895822754
638668899051110339730039268171788341141584403339346413280815117579907805398068501051186548957643424348589582990141598478071180156285949971436535180038059048011268691168703468291254489288844118132875145749256952315849328258377994952320882612663716131755144449419367823460666756750841126211880893
311850048364799970571308236412006025948039259443040240859773006630814358104525635278899682108224328295209757319405077381870693435686499009490495593482004909426420493281996994321577451217711223547966274630419788582646132195635181047941733108264197637696370967325709497719601937343394471309024
8452712498170643941637436558664265704301557216577944354047371344426782440907597751590676094202515006314790319892114058862117560964237298876364441182271699867648272978176853847043206677807975169195524112336927751709842858997499551340001522809055133734186492269324624723274
342882754299605542703496015699200579379649539745770754382000124278512336359979559197823481221022674600830295333617006984059886491421540493951506482390354393725906168817656944421068045574903904761507179069912566059230353619213850248633909312496602150766296613928355581006690894983975206090571020921889235
43888992550349509466047490009497674160595141087458656560896015907649579054077383577321405596290902348906277802702976893959665470901957183225792829745965362396965937582485469411348974941457437519928021902648694730844156776538574812601453103126105495469998888774565504480398330060395316038121219805113539140
148701690847778306279806249814990056013126020165939445905577185931594065716040437354516831449615635058979872379019297305045458524555329377322148357638916680221482414655954498861912363133202145539996799511533611968589436667257652913948192168523708683380306000154719082425353653602004716
702223880805592151456759840151962786569522257399338504974336254522393264865238137237142489540654437582500444843247630303354647534431314931612685275935445798350655833690973837305990813211223944108032523756797743173906424630474927860469366073183637613976281627490028773492993499879192557678442004560805288516
79833612381388792466254908521473542642698050417418301660101889697488475674758562631398318619705428043573697873767699809758897519535743746429567076518306250321667102742400803479875382988205285144602998467363445056770530201048385146222789483144846010988439689414975223195621330556074264582170390
38981256045599996321413529551500753243504907430380030107471625828851794763065704409862460263528041036901219664925634672733836679460812376605305946995956773039813391993758583603213340515768153953248223006627940493064968347973925594017151695012479122008877128229556841394316667513585714442608
326998476314168493941780105303955630664491214509745363599777340200912796363811072538207513066313433266477866490952498420772444240018406385375505907430986779905229774883726145716064039614183599091580710001505418328178515875728287442819830666208828460314384594065173299217689851073972922087853664616
10715086071862673209484250490600018105614048117055336074437503883703510511249361224931983788156958581275946729175531468251871452856923140435984577574908071802839920857415269236967248227417739760593030928446468245035441636876299476051856524203456797756612072518647877926937995333968502556459282279353826
2269007733883335972287082669296112915239349672942191252221331572442536403137824056312817862695551072066953619064625508194663368599769448406663254670871573831506653564687861931994344522266136002053294969244282834092570223577045569108782752942072124046851990673126306718546896266262
311850048364799970571308236412006025948039259443040240859773006630814358104525635278899682108224328295209757319405077381870693435686499009490495593677114193819750400859977621856364864550224170893009384522981032588801229166825598821733689495061047311419695358279148499836829924533799073927369
175555970201398037864189960037990696642380564349834626243584063630598316216309534309285622385163609395625111210811907575838661883607828732903171318983861449587663958422720382174819970807960026763462653637339578061557604033895858449810274193712756378521348131742035156200149490053836559437289929566749716761
5109351192408882717840314145374306729132675226714771306246520940639262443184548008409492391661147394788716663921132787824569441250287599771493955779800203167876896146633723201356517427424053962705284999915534899951518909098001214334663638848571206719402919749996759886156666138926073370282298119
167423219872854268898191413915625282900219501828989626163085998182867351738271269139562246689952477832436667643367679191435491450889424069312259024604665231311477621481628955746781439404577458183134030273454609443839831814813799677783731771694473418316493561305174910604353125570560102800242453589468
351111940402796075728379920075981393284761128699669252487168127261196632432619068618571244770327218791250222421623815151677323767215657465806342637967722951549580764932260637134584054632795311781977202421018443945770709475013210516114239617885321307416343032797706209241510318417565658852099412959658328968
8452712498170643941637436558664265704301557216577944354047371344426782440907597751590676094202515006314790319892114058862117560952042968596008623655407033230543806574403122967612142897595758746785421297125953273092218200663133291073343050608353835620928790613550660010937
1339385758982834151185531311325002263201756014631917009304687985462938813906170153116497973519619822659493341146941433531483931607115392554498072197256315848302527131214717154371567017116527251008520404686974326552891650925750243221247445074543915282030280177333904016448390874266613939932126020558965
1107913932560222642718302084617242634394213707491304322373697056856707228094640652496493097019312046907692196808899173923175472949121784722570529635815601073303740077882176519125363075557711385093141677713259716693627558829530694894822507952419237158530347467119549107097895258
74350845423889153139903124907495028006563010082969722952788592965797032858020218677258415724807817529489936189509648652522729262277251832170757321338859760441211891341492363516683943097344776601334835857749377548332016006885042906462569837823026214385601686620982410300189622400093803
10463951242053391806136963369726580181263718864311851635192874886429209483641954321222640418122029864527291727710479949464718215680589004332016189037791577152079613050475698412775548046381522861183778718190731777596471147595418551260357958381470574269507510821762339825690615585031959945406320617040
8863311460481781141746416676937941075153709659930434578989576454853657824757125219971944776154496375261537574471193391385403783695142864335288586705798628179676607669946943069392905885061641728220564027918449348641480576779375646087432784573797458805960435193128331974223644370
342882754299605542703496015699200579379649539745770754382000124278512336359979559197823481221022674600830295333617006984059886491421540493951506482390459142225358845334215813603772891192865833780836629158267613116386339568201670400131193564590368703658779008862349841853653479391203904732101031259068996
21944496275174754733023745004748837080297570543729328280448007953824789527038691788660702798145451174453138901351488446979832735450978591612896414872982681198464238299940657042605123985627322585091634066000703560929420929319376032533900894809481184711225105009984435701987788821419801914245017790613660446
39916806190694396233127454260736771321349025208709150830050944848744237837379281315699159309852714021786848936883849904879448759767871873214783439162367143929976158393777276838553051534240098503523195379952159347098909183055315965260276533838010349227822704288726567447703697075139957257839787
41855804968213567224547853478906320725054875457247406540771499545716837934567817284890561672488119458109166910841919797858872862722356017328064756151166307827869405371116955728496001280076961304101387952664156170655663056581077934961838053373193410246502699980157151319418413500425224500574820074883
```

Couple of things to note:
1. There's a bug with the line `random.randint(0, 2^self.range)`. It was probably intended to use exponentiation but in python the ^ operator means xor, so what's actually caluclated is 2 xor 1024 not 2 to the power of 1024.
2. The e value used in binary should have 10 high bits.
3. Because the secret is multiplied by a maximum value of 1026, which is pretty small, and the e value will most likely be large, the secret will be mostly preserved.

With this in mind we tried the following strategy: because we have 100 different outputs, there's a high chance that the r value used is a power of 2 (2^0 to 2^10), so we can take each output and right shift it from 0 to 10, get 11 different values, and decode each one as a string and see if it starts with `sctf`. We're assuming that when an r value of a power of 2 is used, that the e value contains powers of 2 bigger than 1024 so it doesn't affect the computation of secret * r.

We implemented this attack with [this](./solution.py) python script:

```python
import binascii

def solve(o):
    st = []
    for i in range(11):
        ss_hex = hex(o >> i)[2:].replace('L', '')
        if len(ss_hex) % 2 == 1:
            ss_hex = '0' + ss_hex
        st.append(binascii.unhexlify(ss_hex))
    return st

outputs = open("output.txt", "rb").readlines()
for o in outputs:
    w = solve(long(o))
    for i in range(11):
        if "sctf" in w[i]:
            print w[i]
```

Running it we see the following flag twice: `sctf»wh@0ps_th4t_w4sît_sxp0nent1ati0n}`. Obviously the flag is close to a real flag but has a few errors (which implies that the e value used did slightly affect the secret * r computation). We can fix the errors by looking at the binary numerical value of the string, and then removing some of the bits of the bytes that look wrong.

# Flag

`sctf{wh00ps_th4t_w4snt_3xp0nent1ati0n}`
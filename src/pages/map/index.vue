<template>
  <div class="background" v-on:scroll="true">
    <img class="zhongshan" @click="showtext1()" 
      src="https://636c-cloud1-5gvc6j32238c5e8b-1313536818.tcb.qcloud.la/%E4%B8%AD%E5%B1%B1%E9%99%B5.PNG?sign=2219a77447e4c772b471dee6211c760d&t=1661948352" />
    <div class="header-box">
    <div class="showbox" v-if="show_bool" @click="show_bool=false">
     <span style="font-weight: bolder">{{ textshow.p1 }}</span>
     <br>
     ⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆
     <br>
     <p>{{ textshow.p2 }}</p>
     <p>{{ textshow.p3 }}</p>
     <p>{{ textshow.p4 }}</p>
     <p>{{ textshow.p5 }}</p> 
     
      <br>
      -------------------------------------------
      <br>
     <span style="font-weight: bolder">{{ transhow.p1 }}</span>
     <br>
     ⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆⋆
     <br>
     <p>{{ transhow.p2 }}</p>
     <p>{{ transhow.p3 }}</p>
     <p>{{ transhow.p4 }}</p>
     <p>{{ transhow.p5 }}</p> 

    </div>
    </div>
      <!-- 弹窗1: 中山陵 -->
    <!-- <div class="header-box" >
        <mask ref="testmask1" top="0"
              :noclickhide="false"
              @onHideHander="onhidemask1()"
              @onShowHander="onshowmask1()">
        <activeModel :showActive="showActive.showActive1" >
            <div class="box" v-on:scroll="true" @click="clickHandle">
              中山陵 
              中山陵是中国近代伟大的民主革命先行者孙中山先生的陵寝及其附属纪念建筑群，位于南京市玄武区紫金山南麓钟山风景名胜区内，陵寝面积8万余平方米，于1926年春动工，至1929年夏建成。
               1925年3月12日上午9点30分，孙中山先生因胆囊癌在北平（今北京）铁狮子胡同行辕与世长辞，举国悲痛。逝世前一天，孙中山提出效仿列宁保留遗体，并要求葬于南京。临终前对宋庆龄、汪精卫等人说：“吾死之后，可葬于南京紫金山麓，因南京为临时政府成立之地，所以不可忘辛亥革命也。”
                中山陵被誉为“中国近代建筑史上第一陵”，陵墓建筑按南北向中轴线对称布置在中茅山南麓的缓坡上，从空中往下看，中山陵像一座平卧的“自由钟”，取“木铎警世”之意。山下孝经鼎是钟的尖顶，半月形广场是钟顶圆弧，而陵墓顶端墓室的穹隆顶，就像一颗溜圆的钟摆锤。含“唤起民众，以建民国”之意。
                  1961年，中山陵被国务院公布为首批全国重点文物保护单位；1982年，被列为国家级风景名胜区；1991年，被国家旅游局列为中国旅游胜地四十佳；2007年，被列为首批国家AAAAA级旅游景区；2016年，入选首批“中国20世纪建筑遗产”名录。
              
              ----------------------------
              
              Dr. Sun Yat-sen's Mausoleum 
                Dr. Sun Yat-sen's Mausoleum is the mausoleum of the great forerunner of China's modern democratic revolution, Dr. Sun Yat-sen, and its ancillary memorial buildings. Located in the Zhongshan Hill Scenic Area at the southern foot of Purple Mountain in Xuanwu District, Nanjing， it covers an area of over 80,000 square metres, which was built in the spring of 1926 and completed by the summer of 1929.
                  To the grief of the nation, Dr. Sun died of gall bladder cancer at the Iron Lion Hutong Regiment in Beiping (Beijing) at 9.30 a.m. on 12 March 1925. The day before his death, Sun proposed to follow Lenin's example and asked to be buried in Nanjing. Before he died, he told Song Qingling, Wang Jingwei and others, 'After my death, I should be buried at the foot of Purple Mountain in Nanjing. Because Nanjing is where the Provisional Government was founded, the 1911 Revolution must not be forgotten."
                    Known as the first mausoleum in the history of modern Chinese architecture", the mausoleum is symmetrically arranged on a north-south axis on a gentle slope at the southern foot of Zhongmao Mountain, and when viewed from the air, it resembles a lying “Liberty Bell”, taking the meaning of “Wooden bell to warn the world". The Xiaojing Ding at the bottom of the hill is the spire of the bell, the half-moon square is the arc of the bell, and the dome of the chamber at the top of the mausoleum is like a rounded pendulum, which means "to arouse the people to build the Republic of China".
                     In 1961, Dr. Sun Yat-sen's Mausoleum was announced by the State Council as one of the first national key cultural relics protection units; in 1982, it was listed as a national scenic spot; in 1991, it was listed as one of the top 40 tourist attractions in China by the National Tourism Administration; in 2007, it was listed as one of the first national AAAAA tourist attractions; in 2016, it was selected as one of the first "China's 20th Century Architectural Heritage". 
            </div>
          

        </activeModel>           -->

        
        <!-- </mask> -->


    <img class="massacre" @click="showtext2()" 
      src="https://636c-cloud1-5gvc6j32238c5e8b-1313536818.tcb.qcloud.la/%E5%8D%97%E4%BA%AC%E5%A4%A7%E5%B1%A0%E6%9D%80%E9%81%87%E9%9A%BE%E5%90%8C%E8%83%9E%E7%BA%AA%E5%BF%B5%E9%A6%86.PNG?sign=5163ae1cc3adff271293a38ff60f636f&t=1661937687"/>
      <!-- 弹窗2：南京大屠杀纪念馆 -->
        <!-- <mask ref="testmask2" top="0"
              :noclickhide="false"
              @onHideHander="onhidemask2()"
              @onShowHander="onshowmask2()">
        <activeModel :showActive="showActive.showActive2" >
          <div>
            <div class="box">
              侵华日军南京大屠杀遇难同胞纪念馆<br>  侵华日军南京大屠杀遇难同胞纪念馆位于南京市建邺区水西门大街418号，通称江东门纪念馆，选址于南京大屠杀江东门集体屠杀遗址及遇难者丛葬地，是中国首批国家一级博物馆，首批全国爱国主义教育示范基地，全国重点文物保护单位，首批国家级抗战纪念设施、遗址名录，也是国际公认的二战期间三大惨案纪念馆之一。<br>  江东门纪念馆是为铭记侵华日军攻占中国首都南京后制造了惨无人道的南京大屠杀的暴行而筹建，是中国人民承段全民族灾难的实证性、遗址型专史纪念馆，也是中国唯一一座有关侵华日军南京大屠杀的专史陈列馆及国家公祭日主办地。<br>   侵华日军南京大屠杀遇难同胞纪念馆分展览集会区、遗址悼念区、和平公园区和馆藏交流区等4个功能性区域。从20世纪80年代建馆以来，侵华日军南京大屠杀遇难同胞纪念馆共收藏国家珍贵文物6000余件，其中一级文物300余件。主要陈列的文物有当年日军屠杀现场照片，历史档案资料，中外人士当年对这次历史惨案所写的纪实、报道和出版的专著、图书、报刊，以及尚健在的1000多位幸存者的名册、证言、证词和实物；当年屠杀南京军民的日军军官和士兵的日记、供词等。<br>  2016年9月，侵华日军南京大屠杀遇难同胞纪念馆入选“首批中国20世纪建筑遗产”名录。
              <br>
              ----------------------------
              <br>
              The Nanjing Massacre Memorial Hall<br> The Nanjing Massacre Memorial Hall is located at 418 Shuiximen Street, Jianye District, Nanjing, where is the site of the Nanjing Massacre at Jiangdongmen and the burial site of the victims of the massacre, commonly known as Jiangdongmen Memorial Hall. It is one of the first national museums in China, one of the first national patriotic education demonstration bases, one of the first national key cultural relics protection units, one of the first list of national anti-war memorial facilities and sites, and one of the three internationally recognized memorials to the tragedies of World War II.<br> The Jiangdongmen Memorial Hall was built to remember the inhuman atrocities Japanese invaders made after the invasion of Nanjing, the capital of China, which is It is an evidence-based, site-specific historical memorial of the Chinese people\'s commitment to the nationwide disaster,  the only museum in China dedicated to the history of the Nanjing Massacre by the  Japanese invaders and the host  of the National Memorial Day.<br>  It is divided into four functional areas: the exhibition and assembly area, the site memorial area, the peace park area and the collection exchange area. Since its establishment in the 1980s, the Nanjing Massacre Memorial Hall has collected more than 6,000 pieces of precious national cultural relics, including more than 300 first-class relics. The main cultural relics on display include photographs of the scene of the massacre, historical archival materials, chronicles, reports and published monographs, books and newspapers written by Chinese and foreign people about the tragedy, as well as the roster, testimonies, evidence and objects of more than 1,000 survivors who are still alive; diaries and confessions of the Japanese officers and soldiers who massacred the Nanjing soldiers and civilians.<br>  In September 2016, it was selected as one of the first Chinese 20th Century Architectural Heritage Sites.
            </div>
          </div>

        </activeModel>          

        
        </mask> -->

      
    <img class="museum"  @click="showtext3()"
      src="https://636c-cloud1-5gvc6j32238c5e8b-1313536818.tcb.qcloud.la/%E5%8D%97%E4%BA%AC%E5%8D%9A%E7%89%A9%E9%99%A2.PNG?sign=fe0f29d5d57d45e849ec990ac1ce6544&t=1661937917" />
      <!-- 弹窗3: 南京博物院 -->
      
        <!-- <mask ref="testmask3" top="0"
              :noclickhide="false"
              @onHideHander="onhidemask3()"
              @onShowHander="onshowmask3()">
        <activeModel :showActive="showActive.showActive3" >
          <div>
            <div class="box">
              南京博物院<br>  南京博物院坐落于南京市紫金山南麓、中山门内北侧，其前身是民国二十二年（1933年）蔡元培倡建的国立中央博物院。目前是中国三大博物馆之一，也是我国第一座由国家投资兴建的大型综合类博物馆，被评为'全国公共文化设施管理先进单位'、"国家一级博物馆"、"全国爱国主义教育示范基地"。<br>  南京博物院占地13万余平方米，为“一院六馆”格局，即历史馆、特展馆、数字馆、艺术馆、非遗馆、民国馆。建筑布局体现了"金镶玉成，宝藏其中"的理念，在前后关系、檐口高度、材质颜色以及细部装饰等方面形成视觉平衡。整体风貌既有传统元素，又有现代气息，二者协调融合、交相辉映。<br>  南京博物院现拥有各类藏品43万余件（套），上至旧石器时代，下迄当代，既有全国性的，又有江苏地域性的；既有宫廷传世品，又有考古发掘品，还有一部分来源于社会征集及捐赠，均为历朝历代的珍品佳作，可以说是一座巨大的中华民族文化艺术宝库。青铜、玉石、陶瓷、金银器皿、竹木牙角、漆器、丝织刺绣、书画、印玺、碑刻造像等文物品类一应俱有，每一品种又自成历史系列，成为数千年中华文明历史发展最为直接的见证。
              <br>
              ----------------------------
              <br>
              Nanjing Museum<br>  The Nanjing Museum is located at the southern foothill of the Purple Mountain in Nanjing, north of Zhongshan Gate, and its predecessor was the National Central Museum, which was built in 1933 by Cai Yuanpei. It is currently one of the three major museums in China, and the first large comprehensive museum built with state investment, and it wasrated as 'National Advanced Unit for the Management of Public Cultural Facilities", "National Level Museum" and "National Patriotic Education Demonstration Base".<br>  Covering an area of more than 130,000 square meters, the Nanjing Museum features "six galleries in one museum", namely the History Gallery, the Special Exhibition Gallery, the Digital Gallery, the Art Gallery, the Non-Foreign Heritage Gallery and the Republican Gallery. The layout of the building reflects the concept "gorgeous and elegant decoration with treasures inside", creating a visual balance in terms of the relationship between front and back, the height of the eaves, the color of the materials and the decorative details. The overall appearance has both traditional elements and modern styles, with a harmonious blend of the two.<br>   The Nanjing Museum now has a collection of over 430,000 pieces (sets), ranging from the Paleolithic period to contemporary times, both nationally and geographically in Jiangsu; there are court heirlooms and archaeological excavations, as well as some social collections and donations, all of which are treasures from various dynasties and generations, making it a huge treasure trove of Chinese culture and art. Bronze, jade, ceramics, gold and silver vessels, bamboo, wood, tooth and lacquer ware, silk weaving and embroidery, calligraphy and painting, seals, inscriptions and statues are all available, each in its own historical series, becoming the most direct witness to the historical development of Chinese civilization over thousands of years.
            </div>
          </div>
        </activeModel>          
        </mask> -->


    <img class="brocade" @click="showtext4()" 
      src="https://636c-cloud1-5gvc6j32238c5e8b-1313536818.tcb.qcloud.la/%E5%8D%97%E4%BA%AC%E4%BA%91%E9%94%A6%E5%8D%9A%E7%89%A9%E9%A6%86.PNG?sign=7774477079961221c8ed62172e1668b3&t=1661938631" />  
      <!-- 弹窗4: 云锦博物馆 -->
        <!-- <mask ref="testmask4" top="0"
              :noclickhide="false"
              @onHideHander="onhidemask4()"
              @onShowHander="onshowmask4()">
        <activeModel :showActive="showActive.showActive4" >
          <div>
            <div class="box">
              南京云锦博物馆<br>  中国南京云锦博物馆位于江苏省南京市建邺区茶亭东街240号，是中国唯一的云锦专业博物馆，主要展示以南京云锦为代表的中国民族织锦艺术，是“新金陵四十八景”之一。<br>  中国南京云锦博物馆前身是创建于1984年的中国织锦工艺陈列馆，由江苏省南京云锦工艺研究生产试验中心主办，馆内荟萃了从战国到明清以来最具代表性的云锦精品实物资料及南京云锦研究所近年来精心复制的我国历代珍贵丝织文物，是一处独具文化内涵和古代科技知识的民族文化遗产。<br>  南京云锦博物馆以专业性、趣味性、互动性让更多的游客认识中国的瑰宝、丝绸的传奇、文化的璀璨，肩负起南京云锦文化的传承与保护工作。2009年，南京云锦博物馆被中宣部命名为全国爱国主义教育示范基地。<br>  南京云锦博物馆每年接待海内外数百万游客及专家学者，并代表国家、文化部等，多次参与各项对外文化交流活动，足迹遍布意大利、法国、美国、澳大利亚、比利时、挪威、韩国、日本、香港、台湾等20余个国家和地区，广泛受到国内外专家、学者、民众的追捧与好评。
              <br>
              ----------------------------
              <br>
              Nanjing Brocade Museum<br> Located at 240 Chating East Street, Jianye District, Nanjing, Jiangsu Province, the Nanjing Brocade Museum is the only museum specialized in cloud brocade in China, mainly displaying the art of Chinese national brocade, represented by Nanjing brocade, and is one of the 'New Jinling 48 Scenes".<br>  Formerly known as the Chinese Brocade Craft Exhibition Hall in 1984, the museum is organized by the Nanjing Brocade Craft Research and Production Experimentation Centre of Jiangsu Province, and comprises a collection of the most representative brocade objects from the Warring States to the Ming and Qing Dynasties, as well as precious silk weaving relics from the Nanjing Brocade Research Institute that have been carefully reproduced in recent years. It is a national cultural heritage with unique cultural connotation and ancient scientific and technological knowledge.<br>  Nanjing Brocade Museum, with its professionalism, interest and interactivity, enables more visitors to understand the treasures of China, the legend of silk and the brilliance of culture, and shoulders the inheritance and protection of Nanjing brocade culture.<br>  In 2009, the Nanjing Brocade Museum was named as a “National Demonstration Base for Patriotism Education” by the Ministry of Propaganda.<br>  The Nanjing Brocade Museum receives millions of visitors and scholars from home and abroad every year, and on behalf of the State and the Ministry of Culture, it has participated in many foreign cultural exchange activities in more than 20 countries and regions, including Italy, France, the United States, Australia, Belgium, Norway, Korea, Japan, Hong Kong and Taiwan, and has been widely pursued and praised by experts, scholars and people at home and abroad. 
            </div>
          </div>
        </activeModel>          
        </mask> -->

    <img class="dujiang" @click="showtext5()" 
      src="https://636c-cloud1-5gvc6j32238c5e8b-1313536818.tcb.qcloud.la/%E6%B8%A1%E6%B1%9F%E8%83%9C%E5%88%A9%E7%BA%AA%E5%BF%B5%E9%A6%86.PNG?sign=16947a80c6972f547e006a37dac83d22&t=1661935242" />
      <!-- 弹窗5: 渡江胜利博物馆 -->
      
        <!-- <mask ref="testmask5" top="0"
              :noclickhide="false"
              @onHideHander="onhidemask5()"
              @onShowHander="onshowmask5()">
        <activeModel :showActive="showActive.showActive5" >
          <div>
            <div class="box">
              南京渡江胜利纪念馆<br>  南京渡江胜利纪念馆旧址坐落在六朝古都南京挹江门城楼上。挹江门城楼地处扬子江畔，与风景秀丽的狮子山、八字山相连。渡江胜利纪念馆新馆建于2009年，是南京市委市政府为纪念渡江战役胜利暨南京解放60周年而异地新建的。<br>  渡江胜利纪念馆由主馆区、渡江胜利广场、渡江胜利纪念碑、挹江门城楼等部分组成，总占地面积20000平方米，建筑面积约9000平方米，展厅面积4000余平方米。主馆区使用仿木结构的外立面，并做成“木船”形状，寓意“驶向胜利之船”。入口处上方镌刻邓小平1987年4月题写的“渡江胜利纪念馆”馆名。主展厅内共展示各类文物和复制品400余件，珍贵历史照片500余幅。展览共分为六部分，分别为序厅、“风雨苍黄”、“天翻地覆”、“人间正道”、“胜利之都”与纪念厅。<br>  渡江胜利、南京解放是重大历史转折性事件，它宣告了国民党政权的灭亡，标志着中国近代史的结束，新中国的诞生，同时赋予了南京英雄之城、胜利之都的历史文化内涵。
              <br>
              ----------------------------
              <br>
              Nanjing Yangtze River Crossing Victory Memorial Hall<br>  The former site of the Nanjing Yangtze River Crossing Victory Memorial Hall is situated on the Yijiangmen Citadel in the ancient capital of Nanjing during the Six Dynasties. The Yijiangmen Citadel is located on the banks of the Yangtse River, and is connected to the scenic Lion Hill and the Bazi Hill. The new Memorial Hall was built in 2009 by the Nanjing Municipal Party Committee and Municipal Government to commemorate the 60th anniversary of the victory in the Yangtze River Crossing Campaign and the liberation of Nanjing.<br>  It consists of the main pavilion, the River Crossing Victory Square, the River Crossing Victory Monument and the Yijiangmen Citadel, covering a total area of 20,000 square meters, with a construction area of about 9,000 square meters and an exhibition hall of over 4,000 square meters. The main pavilion is made of an imitation wooden facade and is shaped like a "wooden boat", signifying "the boat that sails to victory". Above the entrance is engraved the name of the Memorial Hall of Victory over the River, which was inscribed by Deng Xiaoping in April 1987. The main exhibition hall displays more than 400 pieces of various cultural relics and replicas, and more than 500 precious historical photographs. The exhibition is divided into six parts, namely the Prologue Hall, the "Stormy Weather", the "Heaven and Earth Overturned", the "Righteous Path on Earth", the "Victory City " and the Memorial Hall.<br>  The victory of the River Crossing Campaign and the liberation of Nanjing was a major historical turning point that announced the demise of the Kuomintang regime, marked the end of China's modern history and the birth of a new China, and gave Nanjing the historical and cultural connotations of a city of heroes and a capital of victory.  
            </div>
          </div>
        </activeModel>          
        </mask> -->

    <img class="palace"  @click="showtext6()" 
      src="https://636c-cloud1-5gvc6j32238c5e8b-1313536818.tcb.qcloud.la/%E6%80%BB%E7%BB%9F%E5%BA%9C.PNG?sign=c7f11175e65849286a01029b6d3634ae&t=1661938920" /> 
      <!-- 弹窗6: 总统府 -->
        <!-- <mask ref="testmask6" top="0"
              :noclickhide="false"
              @onHideHander="onhidemask6()"
              @onShowHander="onshowmask6()">
        <activeModel :showActive="showActive.showActive6" >
          <div>
            <div class="box">
              总统府<br>  南京总统府位于南京市玄武区长江路292号，是中国近代建筑遗存中规模最大、保存最完整的建筑群，也是南京民国建筑的主要代表之一，中国近代历史的重要遗址。从1840年鸦片战争至1949年南京解放的100多年里，作为中国近现代政治中心的南京，总统府多次成为中国政治军事的中枢、重大事件的策源地。<br>  南京总统府至今已有600多年的历史，最早可追溯到明初的归德侯府和汉王府。1912年1月1日，孙中山在此宣誓就职中华民国临时大总统，辟为大总统府，后为南京国民政府总统府。<br>  南京总统府建筑群占地面积约9万平方米，既有中国古代传统的江南园林，也有近代西风东渐的建筑遗存。其中分布着总统府文物史料、孙中山与南京临时政府、太平天国、清两江总督署等十多个文物史料和复原陈列。<br>  1982年2月，总统府内“太平天国天王府遗址”被国务院公布为全国重点文物保护单位；1998年，辟为中国近代史博物馆；2001年，总统府内“孙中山临时大总统府及南京国民政府建筑遗存”被国务院公布为全国重点文物保护单位；2004年，被列为国家AAAA级旅游景区；2016年9月，入选“首批中国20世纪建筑遗产”名录。
              <br>
              ----------------------------
              <br>
              Nanjing Presidential Palace<br>  Located at 292 Changjiang Road, Xuanwu District, Nanjing, the Presidential Palace is the largest and best-preserved architectural heritage group in modern China, and one of the main representatives of Nanjing's Republican architecture, an important site in China's modern history. During the 100 years from the Opium War in 1840 to the liberation of Nanjing in 1949, the Presidential Palace, as the political heart of modern China, became the political and military hub of China and the source of major events.<br>  The Presidential Palace has a history of over 600 years, dating back to the early Ming Dynasty when it was the residence of the Marquis of Gui De and the King of Han, and was inaugurated by Sun Yat-sen as the Provisional President of the Republic of China on 1 January 1912, and later became the Presidential Palace of the Nanjing National Government.<br>  The Presidential Palace complex in Nanjing covers an area of about 90,000 square meters and contains both the traditional Jiangnan gardens of ancient China and the architectural remains of the western and eastern styles of modern times. It is dotted with more than a dozen cultural relics and historical materials of the Presidential Palace, Sun Yat-sen and the Provisional Government of Nanjing, and the Taiping Heavenly Kingdom.<br>  In February 1982, the site of the Taiping Heavenly Kingdom Palace was declared a National Key Cultural Relics Protection Unit by the State Council; in 1998, it was set up as the Museum of Modern Chinese History; in 2001, the Presidential Palace was declared a National Key Cultural Relics Protection Unit by the State Council. In 2001, the Presidential Palace was declared a National Key Cultural Relics Protection Unit by the State Council; in 2004, it was listed as a National AAAA Grade Tourist Attractions; and in September 2016, it was selected as one of the "First Batch of China's 20th Century Architectural Heritage".
            </div>
          </div>
        </activeModel>          
        </mask>

    </div>  -->
  </div>
</template>

<script>
import activeModel from '@/components/activeModel'
import mask from '@/components/mask'
export default {
  data () {
    return {
      textshow: ' ',
      transhow: ' ',
      show_bool: false,
      // 中山陵、南京大屠杀纪念馆、南京博物院、云锦博物馆、渡江胜利博物馆、总统府
      text: {
        text1: {
          p1: '中山陵',
          p2: '中山陵是中国近代伟大的民主革命先行者孙中山先生的陵寝及其附属纪念建筑群，位于南京市玄武区紫金山南麓钟山风景名胜区内，陵寝面积8万余平方米，于1926年春动工，至1929年夏建成.',
          p3: '1925年3月12日上午9点30分，孙中山先生因胆囊癌在北平（今北京）铁狮子胡同行辕与世长辞，举国悲痛。逝世前一天，孙中山提出效仿列宁保留遗体，并要求葬于南京。临终前对宋庆龄、汪精卫等人说：“吾死之后，可葬于南京紫金山麓，因南京为临时政府成立之地，所以不可忘辛亥革命也。',
          p4: '中山陵被誉为“中国近代建筑史上第一陵”，陵墓建筑按南北向中轴线对称布置在中茅山南麓的缓坡上，从空中往下看，中山陵像一座平卧的“自由钟”，取“木铎警世”之意。山下孝经鼎是钟的尖顶，半月形广场是钟顶圆弧，而陵墓顶端墓室的穹隆顶，就像一颗溜圆的钟摆锤。含“唤起民众，以建民国”之意。',
          p5: '1961年，中山陵被国务院公布为首批全国重点文物保护单位；1982年，被列为国家级风景名胜区；1991年，被国家旅游局列为中国旅游胜地四十佳；2007年，被列为首批国家AAAAA级旅游景区；2016年，入选首批“中国20世纪建筑遗产”名录。'
        },
        text2: {
          p1: '侵华日军南京大屠杀遇难同胞纪念馆',
          p2: '侵华日军南京大屠杀遇难同胞纪念馆位于南京市建邺区水西门大街418号，通称江东门纪念馆，选址于南京大屠杀江东门集体屠杀遗址及遇难者丛葬地，是中国首批国家一级博物馆，首批全国爱国主义教育示范基地，全国重点文物保护单位，首批国家级抗战纪念设施、遗址名录，也是国际公认的二战期间三大惨案纪念馆之一。',
          p3: '江东门纪念馆是为铭记侵华日军攻占中国首都南京后制造了惨无人道的南京大屠杀的暴行而筹建，是中国人民承段全民族灾难的实证性、遗址型专史纪念馆，也是中国唯一一座有关侵华日军南京大屠杀的专史陈列馆及国家公祭日主办地。',
          p4: '侵华日军南京大屠杀遇难同胞纪念馆分展览集会区、遗址悼念区、和平公园区和馆藏交流区等4个功能性区域。从20世纪80年代建馆以来，侵华日军南京大屠杀遇难同胞纪念馆共收藏国家珍贵文物6000余件，其中一级文物300余件。主要陈列的文物有当年日军屠杀现场照片，历史档案资料，中外人士当年对这次历史惨案所写的纪实、报道和出版的专著、图书、报刊，以及尚健在的1000多位幸存者的名册、证言、证词和实物；当年屠杀南京军民的日军军官和士兵的日记、供词等。',
          p5: '2016年9月，侵华日军南京大屠杀遇难同胞纪念馆入选“首批中国20世纪建筑遗产”名录。'
        },
        text3: {
          p1: '南京博物院',
          p2: '南京博物院坐落于南京市紫金山南麓、中山门内北侧，其前身是民国二十二年（1933年）蔡元培倡建的国立中央博物院。目前是中国三大博物馆之一，也是我国第一座由国家投资兴建的大型综合类博物馆，被评为\'全国公共文化设施管理先进单位\'、"国家一级博物馆"、"全国爱国主义教育示范基地"。',
          p3: '南京博物院占地13万余平方米，为“一院六馆”格局，即历史馆、特展馆、数字馆、艺术馆、非遗馆、民国馆。建筑布局体现了"金镶玉成，宝藏其中"的理念，在前后关系、檐口高度、材质颜色以及细部装饰等方面形成视觉平衡。整体风貌既有传统元素，又有现代气息，二者协调融合、交相辉映。',
          p4: '南京博物院现拥有各类藏品43万余件（套），上至旧石器时代，下迄当代，既有全国性的，又有江苏地域性的；既有宫廷传世品，又有考古发掘品，还有一部分来源于社会征集及捐赠，均为历朝历代的珍品佳作，可以说是一座巨大的中华民族文化艺术宝库。青铜、玉石、陶瓷、金银器皿、竹木牙角、漆器、丝织刺绣、书画、印玺、碑刻造像等文物品类一应俱有，每一品种又自成历史系列，成为数千年中华文明历史发展最为直接的见证。',
          p5: ' '
        },
        text4: {
          p1: '南京云锦博物馆',
          p2: '中国南京云锦博物馆位于江苏省南京市建邺区茶亭东街240号，是中国唯一的云锦专业博物馆，主要展示以南京云锦为代表的中国民族织锦艺术，是“新金陵四十八景”之一。',
          p3: '中国南京云锦博物馆前身是创建于1984年的中国织锦工艺陈列馆，由江苏省南京云锦工艺研究生产试验中心主办，馆内荟萃了从战国到明清以来最具代表性的云锦精品实物资料及南京云锦研究所近年来精心复制的我国历代珍贵丝织文物，是一处独具文化内涵和古代科技知识的民族文化遗产。',
          p4: '南京云锦博物馆以专业性、趣味性、互动性让更多的游客认识中国的瑰宝、丝绸的传奇、文化的璀璨，肩负起南京云锦文化的传承与保护工作。2009年，南京云锦博物馆被中宣部命名为全国爱国主义教育示范基地。',
          p5: '南京云锦博物馆每年接待海内外数百万游客及专家学者，并代表国家、文化部等，多次参与各项对外文化交流活动，足迹遍布意大利、法国、美国、澳大利亚、比利时、挪威、韩国、日本、香港、台湾等20余个国家和地区，广泛受到国内外专家、学者、民众的追捧与好评。'
        },
        text5: {
          p1: '南京渡江胜利纪念馆',
          p2: '南京渡江胜利纪念馆旧址坐落在六朝古都南京挹江门城楼上。挹江门城楼地处扬子江畔，与风景秀丽的狮子山、八字山相连。渡江胜利纪念馆新馆建于2009年，是南京市委市政府为纪念渡江战役胜利暨南京解放60周年而异地新建的。',
          p3: '渡江胜利纪念馆由主馆区、渡江胜利广场、渡江胜利纪念碑、挹江门城楼等部分组成，总占地面积20000平方米，建筑面积约9000平方米，展厅面积4000余平方米。主馆区使用仿木结构的外立面，并做成“木船”形状，寓意“驶向胜利之船”。入口处上方镌刻邓小平1987年4月题写的“渡江胜利纪念馆”馆名。主展厅内共展示各类文物和复制品400余件，珍贵历史照片500余幅。展览共分为六部分，分别为序厅、“风雨苍黄”、“天翻地覆”、“人间正道”、“胜利之都”与纪念厅。',
          p4: '渡江胜利、南京解放是重大历史转折性事件，它宣告了国民党政权的灭亡，标志着中国近代史的结束，新中国的诞生，同时赋予了南京英雄之城、胜利之都的历史文化内涵。',
          p5: ' '
        },
        text6: {
          p1: '总统府',
          p2: '南京总统府位于南京市玄武区长江路292号，是中国近代建筑遗存中规模最大、保存最完整的建筑群，也是南京民国建筑的主要代表之一，中国近代历史的重要遗址。从1840年鸦片战争至1949年南京解放的100多年里，作为中国近现代政治中心的南京，总统府多次成为中国政治军事的中枢、重大事件的策源地。',
          p3: '南京总统府至今已有600多年的历史，最早可追溯到明初的归德侯府和汉王府。1912年1月1日，孙中山在此宣誓就职中华民国临时大总统，辟为大总统府，后为南京国民政府总统府。',
          p4: '南京总统府建筑群占地面积约9万平方米，既有中国古代传统的江南园林，也有近代西风东渐的建筑遗存。其中分布着总统府文物史料、孙中山与南京临时政府、太平天国、清两江总督署等十多个文物史料和复原陈列。',
          p5: '1982年2月，总统府内“太平天国天王府遗址”被国务院公布为全国重点文物保护单位；1998年，辟为中国近代史博物馆；2001年，总统府内“孙中山临时大总统府及南京国民政府建筑遗存”被国务院公布为全国重点文物保护单位；2004年，被列为国家AAAA级旅游景区；2016年9月，入选“首批中国20世纪建筑遗产”名录。'
        }
      },
      trans: {
        trans1: {
          p1: 'Dr. Sun Yat-sen\'s Mausoleum',
          p2: 'Dr. Sun Yat-sen\'s Mausoleum is the mausoleum of the great forerunner of China\'s modern democratic revolution, Dr. Sun Yat-sen, and its ancillary memorial buildings. Located in the Zhongshan Hill Scenic Area at the southern foot of Purple Mountain in Xuanwu District, Nanjing， it covers an area of over 80,000 square metres, which was built in the spring of 1926 and completed by the summer of 1929.',
          p3: 'To the grief of the nation, Dr. Sun died of gall bladder cancer at the Iron Lion Hutong Regiment in Beiping (Beijing) at 9.30 a.m. on 12 March 1925. The day before his death, Sun proposed to follow Lenin\'s example and asked to be buried in Nanjing. Before he died, he told Song Qingling, Wang Jingwei and others, \'After my death, I should be buried at the foot of Purple Mountain in Nanjing. Because Nanjing is where the Provisional Government was founded, the 1911 Revolution must not be forgotten."',
          p4: 'Known as the first mausoleum in the history of modern Chinese architecture", the mausoleum is symmetrically arranged on a north-south axis on a gentle slope at the southern foot of Zhongmao Mountain, and when viewed from the air, it resembles a lying “Liberty Bell”, taking the meaning of “Wooden bell to warn the world". The Xiaojing Ding at the bottom of the hill is the spire of the bell, the half-moon square is the arc of the bell, and the dome of the chamber at the top of the mausoleum is like a rounded pendulum, which means "to arouse the people to build the Republic of China".',
          p5: 'In 1961, Dr. Sun Yat-sen\'s Mausoleum was announced by the State Council as one of the first national key cultural relics protection units; in 1982, it was listed as a national scenic spot; in 1991, it was listed as one of the top 40 tourist attractions in China by the National Tourism Administration; in 2007, it was listed as one of the first national AAAAA tourist attractions; in 2016, it was selected as one of the first "China\'s 20th Century Architectural Heritage".'
        },
        trans2: {
          p1: 'The Nanjing Massacre Memorial Hall',
          p2: 'The Nanjing Massacre Memorial Hall is located at 418 Shuiximen Street, Jianye District, Nanjing, where is the site of the Nanjing Massacre at Jiangdongmen and the burial site of the victims of the massacre, commonly known as Jiangdongmen Memorial Hall. It is one of the first national museums in China, one of the first national patriotic education demonstration bases, one of the first national key cultural relics protection units, one of the first list of national anti-war memorial facilities and sites, and one of the three internationally recognized memorials to the tragedies of World War II.',
          p3: 'The Jiangdongmen Memorial Hall was built to remember the inhuman atrocities Japanese invaders made after the invasion of Nanjing, the capital of China, which is It is an evidence-based, site-specific historical memorial of the Chinese people\'s commitment to the nationwide disaster,  the only museum in China dedicated to the history of the Nanjing Massacre by the  Japanese invaders and the host  of the National Memorial Day.',
          p4: 'It is divided into four functional areas: the exhibition and assembly area, the site memorial area, the peace park area and the collection exchange area. Since its establishment in the 1980s, the Nanjing Massacre Memorial Hall has collected more than 6,000 pieces of precious national cultural relics, including more than 300 first-class relics. The main cultural relics on display include photographs of the scene of the massacre, historical archival materials, chronicles, reports and published monographs, books and newspapers written by Chinese and foreign people about the tragedy, as well as the roster, testimonies, evidence and objects of more than 1,000 survivors who are still alive; diaries and confessions of the Japanese officers and soldiers who massacred the Nanjing soldiers and civilians.',
          p5: 'In September 2016, it was selected as one of the first Chinese 20th Century Architectural Heritage Sites.'
        },
        trans3: {
          p1: 'Nanjing Museum',
          p2: 'The Nanjing Museum is located at the southern foothill of the Purple Mountain in Nanjing, north of Zhongshan Gate, and its predecessor was the National Central Museum, which was built in 1933 by Cai Yuanpei. It is currently one of the three major museums in China, and the first large comprehensive museum built with state investment, and it wasrated as \'National Advanced Unit for the Management of Public Cultural Facilities", "National Level Museum" and "National Patriotic Education Demonstration Base".',
          p3: 'Covering an area of more than 130,000 square meters, the Nanjing Museum features "six galleries in one museum", namely the History Gallery, the Special Exhibition Gallery, the Digital Gallery, the Art Gallery, the Non-Foreign Heritage Gallery and the Republican Gallery. The layout of the building reflects the concept "gorgeous and elegant decoration with treasures inside", creating a visual balance in terms of the relationship between front and back, the height of the eaves, the color of the materials and the decorative details. The overall appearance has both traditional elements and modern styles, with a harmonious blend of the two.',
          p4: 'The Nanjing Museum now has a collection of over 430,000 pieces (sets), ranging from the Paleolithic period to contemporary times, both nationally and geographically in Jiangsu; there are court heirlooms and archaeological excavations, as well as some social collections and donations, all of which are treasures from various dynasties and generations, making it a huge treasure trove of Chinese culture and art. Bronze, jade, ceramics, gold and silver vessels, bamboo, wood, tooth and lacquer ware, silk weaving and embroidery, calligraphy and painting, seals, inscriptions and statues are all available, each in its own historical series, becoming the most direct witness to the historical development of Chinese civilization over thousands of years.',
          p5: ' '
        },
        trans4: {
          p1: 'Nanjing Brocade Museum',
          p2: 'Located at 240 Chating East Street, Jianye District, Nanjing, Jiangsu Province, the Nanjing Brocade Museum is the only museum specialized in cloud brocade in China, mainly displaying the art of Chinese national brocade, represented by Nanjing brocade, and is one of the \'New Jinling 48 Scenes".',
          p3: 'Formerly known as the Chinese Brocade Craft Exhibition Hall in 1984, the museum is organized by the Nanjing Brocade Craft Research and Production Experimentation Centre of Jiangsu Province, and comprises a collection of the most representative brocade objects from the Warring States to the Ming and Qing Dynasties, as well as precious silk weaving relics from the Nanjing Brocade Research Institute that have been carefully reproduced in recent years. It is a national cultural heritage with unique cultural connotation and ancient scientific and technological knowledge.',
          p4: 'Nanjing Brocade Museum, with its professionalism, interest and interactivity, enables more visitors to understand the treasures of China, the legend of silk and the brilliance of culture, and shoulders the inheritance and protection of Nanjing brocade culture.',
          p5: 'In 2009, the Nanjing Brocade Museum was named as a “National Demonstration Base for Patriotism Education” by the Ministry of Propaganda.The Nanjing Brocade Museum receives millions of visitors and scholars from home and abroad every year, and on behalf of the State and the Ministry of Culture, it has participated in many foreign cultural exchange activities in more than 20 countries and regions, including Italy, France, the United States, Australia, Belgium, Norway, Korea, Japan, Hong Kong and Taiwan, and has been widely pursued and praised by experts, scholars and people at home and abroad.'
        },
        trans5: {
          p1: 'Nanjing Yangtze River Crossing Victory Memorial Hall',
          p2: 'The former site of the Nanjing Yangtze River Crossing Victory Memorial Hall is situated on the Yijiangmen Citadel in the ancient capital of Nanjing during the Six Dynasties. The Yijiangmen Citadel is located on the banks of the Yangtse River, and is connected to the scenic Lion Hill and the Bazi Hill. The new Memorial Hall was built in 2009 by the Nanjing Municipal Party Committee and Municipal Government to commemorate the 60th anniversary of the victory in the Yangtze River Crossing Campaign and the liberation of Nanjing.',
          p3: 'It consists of the main pavilion, the River Crossing Victory Square, the River Crossing Victory Monument and the Yijiangmen Citadel, covering a total area of 20,000 square meters, with a construction area of about 9,000 square meters and an exhibition hall of over 4,000 square meters. The main pavilion is made of an imitation wooden facade and is shaped like a \'wooden boat", signifying "the boat that sails to victory". Above the entrance is engraved the name of the Memorial Hall of Victory over the River, which was inscribed by Deng Xiaoping in April 1987. The main exhibition hall displays more than 400 pieces of various cultural relics and replicas, and more than 500 precious historical photographs. The exhibition is divided into six parts, namely the Prologue Hall, the "Stormy Weather", the "Heaven and Earth Overturned", the "Righteous Path on Earth", the "Victory City " and the Memorial Hall.',
          p4: 'The victory of the River Crossing Campaign and the liberation of Nanjing was a major historical turning point that announced the demise of the Kuomintang regime, marked the end of China\'s modern history and the birth of a new China, and gave Nanjing the historical and cultural connotations of a city of heroes and a capital of victory.',
          p5: ' '
        },
        trans6: {
          p1: 'Nanjing Presidential Palace',
          p2: 'Located at 292 Changjiang Road, Xuanwu District, Nanjing, the Presidential Palace is the largest and best-preserved architectural heritage group in modern China, and one of the main representatives of Nanjing\'s Republican architecture, an important site in China\'s modern history. During the 100 years from the Opium War in 1840 to the liberation of Nanjing in 1949, the Presidential Palace, as the political heart of modern China, became the political and military hub of China and the source of major events.',
          p3: 'The Presidential Palace has a history of over 600 years, dating back to the early Ming Dynasty when it was the residence of the Marquis of Gui De and the King of Han, and was inaugurated by Sun Yat-sen as the Provisional President of the Republic of China on 1 January 1912, and later became the Presidential Palace of the Nanjing National Government.',
          p4: 'The Presidential Palace complex in Nanjing covers an area of about 90,000 square meters and contains both the traditional Jiangnan gardens of ancient China and the architectural remains of the western and eastern styles of modern times. It is dotted with more than a dozen cultural relics and historical materials of the Presidential Palace, Sun Yat-sen and the Provisional Government of Nanjing, and the Taiping Heavenly Kingdom.',
          p5: 'In February 1982, the site of the Taiping Heavenly Kingdom Palace was declared a National Key Cultural Relics Protection Unit by the State Council; in 1998, it was set up as the Museum of Modern Chinese History; in 2001, the Presidential Palace was declared a National Key Cultural Relics Protection Unit by the State Council. In 2001, the Presidential Palace was declared a National Key Cultural Relics Protection Unit by the State Council; in 2004, it was listed as a National AAAA Grade Tourist Attractions; and in September 2016, it was selected as one of the \'First Batch of China\'s 20th Century Architectural Heritage".'
        }
      },
      showActive: {
        showActive1: true,
        showActive2: true,
        showActive3: true,
        showActive4: true,
        showActive5: true,
        showActive6: true
      }
    }
  },
  components: { mask, activeModel },
  methods: {
    // 弹窗1控制：
    showtext1 () {
      this.show_bool = true
      this.textshow = this.text.text1
      this.transhow = this.trans.trans1
      console.log(this.textshow)
      console.log(this.textshow.id)
      // this.$refs.testmask1.showMask()
    },
    onhidemask1 () {
      this.showActive.showActive1 = false
    },
    onshowmask1 () {
      let _this = this
      setTimeout(() => {
        console.log('>>>>>>>', _this.showActive.showActive1)
        _this.showActive.showActive1 = true
        console.log('>>>>>>>', _this.showActive.showActive1)
      }, 100)
    },
    // 弹窗2控制：
    showtext2 () {
      this.show_bool = true
      this.textshow = this.text.text2
      this.transhow = this.trans.trans2
    },
    onhidemask2 () {
      this.showActive.showActive2 = false
    },
    onshowmask2 () {
      let _this = this
      setTimeout(() => {
        console.log('>>>>>>>', _this.showActive.showActive2)
        _this.showActive.showActive2 = true
        console.log('>>>>>>>', _this.showActive.showActive2)
      }, 100)
    },
    // 弹窗3控制：
    showtext3 () {
      this.show_bool = true
      this.textshow = this.text.text3
      this.transhow = this.trans.trans3
    },
    onhidemask3 () {
      this.showActive.showActive3 = false
    },
    onshowmask3 () {
      let _this = this
      setTimeout(() => {
        console.log('>>>>>>>', _this.showActive.showActive3)
        _this.showActive.showActive3 = true
        console.log('>>>>>>>', _this.showActive.showActive3)
      }, 100)
    },
    // 弹窗4控制：
    showtext4 () {
      this.show_bool = true
      this.textshow = this.text.text4
      this.transhow = this.trans.trans4
    },
    onhidemask4 () {
      this.showActive.showActive4 = false
    },
    onshowmask4 () {
      let _this = this
      setTimeout(() => {
        console.log('>>>>>>>', _this.showActive.showActive4)
        _this.showActive.showActive4 = true
        console.log('>>>>>>>', _this.showActive.showActive4)
      }, 100)
    },
    // 弹窗5控制：
    showtext5 () {
      this.show_bool = true
      this.textshow = this.text.text5
      this.transhow = this.trans.trans5
    },
    onhidemask5 () {
      this.showActive.showActive5 = false
    },
    onshowmask5 () {
      let _this = this
      setTimeout(() => {
        console.log('>>>>>>>', _this.showActive.showActive5)
        _this.showActive.showActive5 = true
        console.log('>>>>>>>', _this.showActive.showActive5)
      }, 100)
    },
    // 弹窗6控制：
    showtext6 () {
      this.show_bool = true
      this.textshow = this.text.text6
      this.transhow = this.trans.trans6
    },
    onhidemask6 () {
      this.showActive.showActive6 = false
    },
    onshowmask6 () {
      let _this = this
      setTimeout(() => {
        console.log('>>>>>>>', _this.showActive.showActive6)
        _this.showActive.showActive6 = true
        console.log('>>>>>>>', _this.showActive.showActive6)
      }, 100)
    },
    clickHandle (ev) {
      console.log('clickHandle:', ev)
      // throw {message: 'custom test'}
    }
  }
}
</script>

<style scoped>
.background {
  position: absolute;
  overflow-x: scroll;
  overflow-y: scroll;
  right:auto; 
  scale: 100%;
  justify-content: center; 
  text-align: center; 
  width: 100%;
  height: 700px;
  background-size: 100% 100%;
  z-index: 0;
  background-image: url(https://636c-cloud1-5gvc6j32238c5e8b-1313536818.tcb.qcloud.la/map2.jpeg?sign=356a4cdbd2fb1696bef1905af264602e&t=1661949268);
}
.zhongshan {
  position: absolute;
  width: 20%;
  height: 15%;
  right: 3%;
  top: 37%;
  z-index: 0;
}

.massacre {
  position: absolute;
  width: 20%;
  height: 15%;
  left: 15%;
  top: 45%;
  z-index: 0;
}

.museum {
  position: absolute;
  width: 25%;
  height: 20%;
  right: 18%;
  bottom: 15%;
  z-index: 0;
}

.brocade {
  position: absolute;
  width: 25%;
  height: 15%;
  right: 60%;
  top: 32%;
  z-index: 0;
}
.dujiang {
  position: absolute;
  width: 25%;
  height: 15%;
  left: 20%;
  top: 10%;
  z-index: 0;
}

.palace {
  position: absolute;
  width: 25%;
  height: 15%;
  right: 22%;
  top: 40%;
  z-index: 0;
}
.header-box {
  height: 100vh;
  top: 100px;
  z-index: 99;
  overflow-y: scroll;
  
}
.showbox {
  position: absolute;
  height: 80vh;
  top: 10%;
  width: 80%;
  right: 10%;
  background-color: white;
  border-radius: 30px;
  border: 5px 5px 5px 5px;
  border-style: solid;
  border-color: rgb(237, 222, 13);
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  font-size: medium;
  z-index: 999;
  overflow-y: scroll; 
}
</style>

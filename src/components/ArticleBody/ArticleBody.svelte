<!-- 
@component
### ArticleBody component
This is a general workspace illustrating what an article body might look like if you use only the components included in this template.  
ArticleBody doesn&rsquo;t accept any props. All contents will need to be hand-placed by a designer directly inside this component.  
In this example, Grid and GridRow help establish the width of the article body&rsquo;s contents. 
Documentation included with those components and accessed by VSCode tooltip explains each component in greater detail.

#### State in this component
- innerWidth: int - pixel width of the viewport.
- isMobile: boolean - derived from innerWidth, true if less than 768 pixels
- isTablet: boolean - derived from innerWidth, true if between 768 pixels inclusive and 1024 pixels exclusive
- isDesktop: boolean - derived from innerWidth, true if greater than 1024 pixels inclusive

#### Using state in this component
You can use any of the three derived states to render different variants of a GridRow component reactively.
The following example uses a ternary to render an image edge-to-edge on mobile but inline otherwise.

#### Example
```svelte
  <GridRow
    variant={isMobile ? "fullBleed" : "inline"}
  >
    <Image
      src="https://arc.stimg.co/startribunemedia/4SPNT7DI36ANT2SOB5N5EJAIJU.jpg"
      alt="Descriptive alt text"
      caption="Caption tk tk tk"
    />
  </GridRow>
```
-->

<script>
  import Grid from "../Grid/Grid.svelte";
  import GridRow from "../Grid/_GridRow.svelte";
  import Subhead from "./_Subhead.svelte";
  import Paragraph from "./_Paragraph.svelte";
    import StoryPause from "./_StoryPause.svelte";
    import BreakRight from "./_BreakRight.svelte";

  import Image from "../Image/Image.svelte";
  import ScrollySection from "../Scrolly/ScrollySection.svelte";
 
  let innerWidth = $state(0);
  let isMobile = $derived(innerWidth < 768);
  let isTablet = $derived(innerWidth >= 768 && innerWidth < 1024);
  let isDesktop = $derived(innerWidth >= 1024);
</script>

<svelte:window bind:innerWidth />

<Grid additionalClasses={"gap-y-5"}>
  <GridRow variant={"inline"} additionalClasses={"gap-y-5"}>

<Paragraph><span style="font-family: 'Graphik-Semibold'; text-transform: uppercase; font-size: 95%;">RED LAKE, MINN. — The final home game of the season</span> kicks off on the south side of the reservation in a few hours. That gives the football team&rsquo;s head coach just enough time to pick up his daughters at school, drop them at day care and hustle home to finish last-minute arrangements for Senior Night.</Paragraph>
<Paragraph>	Nolan Desjarlait stays in motion to keep his mind from drifting, to live in the moment. <i>Focus on what&rsquo;s in front of you</i>, he says often. The coach preaches this advice to everyone, and the words help him carry the weight of a losing streak that never ends and grief that will never go away.	</Paragraph>
<Paragraph>	Desjarlait grew up on the Red Lake Reservation, a star athlete at Red Lake High School. He is now the school&rsquo;s athletic director and coaches three varsity sports. If a game is happening on the reservation, he&rsquo;s there.	</Paragraph>
<Paragraph>	&ldquo;I can&rsquo;t say no to kids,&rdquo; Desjarlait says. He tries to be everywhere, tries to be everything these kids need. Until he gets to the one place he lets himself be still.	</Paragraph>
<Paragraph>	The house is a quarter mile off the main road, nestled between tall pine trees. Desjarlait gets out of his car and heads toward the edge of the property, stopping when he reaches a clearing that overlooks two lakes.	</Paragraph>
<Paragraph>	Nolan Desjarlait Jr.&rsquo;s grave site is here, surrounded by old sports equipment and the boy&rsquo;s favorite memorabilia. There is a Steph Curry sign. A basketball is on the ground. A football. The baseball bat his 10-year-old son used in a game shortly before he died. A flower wreath hangs on a tree. Solar lights illuminate the area at night. Wooden benches with hand-carved inscriptions invite visitors to sit.	</Paragraph>


<!-- ONE UP -->
</GridRow>
<GridRow variant={"fullBleed"}>
<div class="md:max-w-7xl mt-8 mb-12 mx-auto px-2">
<img class="block mb-2" src="https://arc.stimg.co/startribunemedia/TLGL7HENGOHOLHWFJAM4JIZKT4.jpg?w=1400format=auto&compress&cs=tinysrgb" alt="photo">
<div class="caption font-utility-meta-reg-02 text-tertiary text-center md:max-w-[650px] mx-auto xs:max-w-[100%] xs:min-w-[250px] !text-[14px] !leading-[1.25] pt-2">On a clearing overlooking two lakes on the Red Lake Nation in northern Minnesota, Nolan Desjarlait visited the grave site of his son, Nolan Desjarlait Jr., who died in an ATV wreck at age 10. The high school seniors Desjarlait coaches this year were teammates and best friends of Nolan Jr., and they&rsquo;ve dedicated their seasons to him. The grave house is part of traditional burials by the Red Lake Band of Chippewa Indians.</div>
</div>
</GridRow>
<GridRow variant={"inline"} additionalClasses={"gap-y-5"}>



<Paragraph>	Desjarlait picks up the bat and leans it against his son&rsquo;s grave. He remembers the game when Nolan Jr. used it. Sometimes he sits here for hours, remembering everything.	</Paragraph>
<Paragraph>	People here still marvel at young Nolan Jr.&rsquo;s athletic talent. He would have been a senior at Red Lake High this year, undoubtedly a star athlete, his father his coach.	</Paragraph>
<Paragraph>	His friends are seniors now. This is their Senior Night. They have not won a game in their career, because Red Lake has not won a game in their lifetime. Records suggest that 1999 was the last time the Red Lake Warriors won a varsity football game. Low participation puts them at a disadvantage against opponents that have twice as many players. Injuries force them to rely on middle-school players, or sometimes forfeit games.	</Paragraph>
<Paragraph>	But the players who never win keep coming back. They keep showing up for one another and for the coach who refuses to quit on them.	</Paragraph>
<Paragraph>	&ldquo;I don&rsquo;t know how many times throughout all these five years I wanted to quit,&rdquo; says senior Justin Brown, tears welling. &ldquo;I just can&rsquo;t. These are my brothers.&rdquo;	</Paragraph>
<Paragraph>	At halftime, the seniors get roses from Desjarlait and his wife, Nicole. The couple bring carnations for the other players and donuts and cupcakes for family members. Red Lake is losing, but the mood is upbeat.	</Paragraph>
<Paragraph>	Parents join their sons on the field for pictures and treats. Players gather for a group photo, then cheer when their coach joins them.	</Paragraph>
<Paragraph>	&ldquo;This is <i>our</i> half!&ldquo; junior receiver Gerald Kingbird Jr. yells to teammates as they buckle their helmets for the second half.	</Paragraph>
<Paragraph>	Kingbird Jr. is wearing No. 12 this season. He switched numbers because that was Nolan Jr.&rsquo;s jersey number in every sport.	</Paragraph>
<Paragraph>	&ldquo;I think about him every day,&rdquo; Kingbird Jr. says.	</Paragraph>




  <!-- THREE UP -->
  </GridRow>
  <GridRow variant={"fullBleed"}>
    <div class="md:max-w-7xl mt-8 mb-4 mx-auto px-2">
<div class="md:max-w-7xl mt-4 mb-1 mx-auto px-0">
<img class="block mb-0" src="https://arc.stimg.co/startribunemedia/RALTEZG24V4US6GSDMJT5PKFN4.jpg?w=2000format=auto&compress&cs=tinysrgb" alt="photo">

</div>
<div class="md:flex">
<div class="mr-0 lg:w-1/2 md:w-full xs:w-full md:mr-1 xs:mr-0 xs:mb-5 md:mb-2">
<div class="bg-no-repeat bg-cover bg-center xl:h-[24rem] lg:h-[24rem] md:h-[24rem] mb-0 xs:h-[20rem]" style="background-image: url('https://arc.stimg.co/startribunemedia/47KJNOFH6ERFTPUIAQIY7EYPAM.jpg?w=1200format=auto&compress&cs=tinysrgb');"></div>
</div>
<div class="md:ml-0 lg:w-1/2 md:w-full xs:w-full xs:ml-0">
<div class="bg-no-repeat bg-cover bg-center h-[28rem]xl:h-[24rem] lg:h-[24rem] md:h-[24rem] mb-0 xs:h-[20rem]" style="background-image: url('https://arc.stimg.co/startribunemedia/AOENSAZKC74EENELLWTQS37M7Q.jpg?w=1200format=auto&compress&cs=tinysrgb');">
</div>
</div>

</div>
<div class="caption font-utility-meta-reg-02 text-tertiary text-center md:max-w-[650px] mx-auto xs:max-w-[100%] xs:min-w-[250px] !text-[14px] !leading-[1.25] pt-2">At top, Red Lake High School football players, from left to right, Douglas Feather, Ty Beaulieu, Gerald Kingbird Jr., Makoons Wakonabo, Ayden Lussier and Andrew Roy lined up during the first week of practice in August. The team averages fewer than 20 players, and coach Nolan Desjarlait instructs his team not to count players on the opposing sideline — too discouraging. He sometimes teaches basic skills like how to put on a helmet, above with sixth-grader John Morris. Other junior varsity players like Elias Morris and Austin Perkins, above right, both eighth-graders, also suit up for varsity to help fill out the roster. &ldquo;Coaching is having fun with kids and making them feel welcomed and wanting to be here,&rdquo; Desjarlait says. &ldquo;My job is to keep them moving.&rdquo;</div>
</div>
  </GridRow>
  <GridRow variant={"inline"} additionalClasses={"gap-y-5"}>






<StoryPause></StoryPause>

<Paragraph><span style="font-family: 'Graphik-Semibold'; text-transform: uppercase; font-size: 95%;">The Warriors&rsquo; old football plaques</span> fit comfortably on one small shelf of the glass trophy case that stretches along the gymnasium entrance. A display at the far end highlights the baseball team. The hallways are empty on this summer day, and Desjarlait smiles as he stares at the ensemble of pictures and trophies. He had a hand in most of them.</Paragraph>
<Paragraph>	The Desjarlait name is well known on the reservation, stretching back generations. Nolan&rsquo;s grandfather Leo Desjarlait was a Navy man who served in World War II. He died in 2014 two weeks shy of his 99th birthday. Nolan was his personal barber in the final years of his life.	</Paragraph>
<Paragraph>	Nolan&rsquo;s dad, Leo Desjarlait Jr., was Red Lake&rsquo;s fire chief throughout his son&rsquo;s childhood. He now works for the reservation&rsquo;s Transit Department and Ramona, Nolan&rsquo;s mom, is program director for the department.	</Paragraph>
<Paragraph>	Located 250 miles northwest of Minneapolis, the reservation is home to the Red Lake Band of Chippewa Indians and the largest lake contained entirely within the state&rsquo;s borders. More than 5,500 members make up the Red Lake Nation, which is governed by a democratically elected chair and Tribal Council that upholds and protects its sovereignty. The high school has an enrollment of 327 students.	</Paragraph>


<BreakRight>
<iframe src="https://datawrapper.dwcdn.net/evgrB/4/" border="0" frameborder="0" scrolling="no" width="100%" height="285"></iframe>
</BreakRight>



<Paragraph>	Across these nearly 900 square miles, Nolan Desjarlait&rsquo;s athletic feats in the 1990s were legendary. A game-saving double play he turned by himself in his sophomore year helped send Red Lake to its first and only baseball state tournament appearance. He was all-conference in three sports as a senior.	</Paragraph>
<Paragraph>	Desjarlait played two years of college baseball and was back home working as an electrician when the school district invited him to coach middle school sports. He became the high school&rsquo;s athletic director in 2007, and also serves as head boys basketball coach, assistant baseball coach and football coach. He also ran the school&rsquo;s mail operation for years.	</Paragraph>
<Paragraph>	Football is a tough sell at Red Lake High. The boys basketball team has advanced to the state tournament nine times since 1997, and many student-athletes here skip football to save their bodies for hoops. By the time Desjarlait took over in 2008, the team had been dismissed from its conference over frequent forfeits and cancellations. The Warriors found a new conference home a decade ago, but challenges remain.	</Paragraph>



<!-- ONE UP -->
</GridRow>
<GridRow variant={"fullBleed"}>
<div class="md:max-w-7xl mt-8 mb-12 mx-auto px-2">
<img class="block mb-2" src="https://arc.stimg.co/startribunemedia/RFFSATSML52WHFQODEG423ILQE.jpg?w=2000format=auto&compress&cs=tinysrgb" alt="photo">
<div class="caption font-utility-meta-reg-02 text-tertiary text-center md:max-w-[650px] mx-auto xs:max-w-[100%] xs:min-w-[250px] !text-[14px] !leading-[1.25] pt-2">The Red Lake Warriors experienced Friday Night Lights on their home field for the first time in decades this year when the school bought stadium lights. Although they lost in the home opener under the lights, the players remained upbeat.</div>
</div>
</GridRow>
<GridRow variant={"inline"} additionalClasses={"gap-y-5"}>




<Paragraph>	Four players showed up to Desjarlait&rsquo;s first football practice in 2008. Undeterred, he stressed the importance of being physically active and urged his players to tell friends to join them. He&rsquo;d stop kids in the hallway between classes and recruit them, using one of his favorite lines: <i>You might like it, and you might love it</i>.	</Paragraph>
<Paragraph>	Without a robust feeder program at the youth level, many kids come to football tryouts having never played the sport. Desjarlait&rsquo;s coaching often includes rudimentary tasks such as teaching players how to properly put on helmets and pads.	</Paragraph>
<Paragraph>	Red Lake averages fewer than 20 players. Opponents often have twice as many, and Desjarlait makes a point of instructing his team not to count players on the opposite sideline. Too intimidating.	</Paragraph>
<Paragraph>	Once, Desjarlait wanted to forfeit a game because he had only 13 players available that night. The opposing school begged him to play because it was their Parents Night. Desjarlait agreed to play, but the game ended at halftime with too many Warriors suffering cramps.	</Paragraph>
<Paragraph>	At home after some games, Desjarlait wonders how he keeps doing it. The answer always comes.	</Paragraph>
<Paragraph>	&ldquo;I refuse to give up on them,&rdquo; he says.	</Paragraph>
<Paragraph>	Desjarlait&rsquo;s patience is as deep and wide as the big lake by the school. He does not kick players off the team for skipping practice or games. He pours himself into the kids who are there that day, and then welcomes those who show up tomorrow with encouragement to keep coming back. He answers to &ldquo;Uncle Nolan&ldquo; from players who know him well and need him often.	</Paragraph>
<Paragraph>	His voice is usually soft and calming. He finds positives even in a lopsided loss — in fact, especially in those moments, because life&rsquo;s scoreboard matters far more to Desjarlait than the one in the end zone. Do his players graduate? Do they become productive adults? Are they being accountable to their families and employers? He counts those as victories.	</Paragraph>
<Paragraph>	&ldquo;I&rsquo;m teaching them how to be a young man in a football helmet,&rdquo; he says.	</Paragraph>



  <!-- THREE UP -->
  </GridRow>
  <GridRow variant={"fullBleed"}>
    <div class="md:max-w-7xl mt-8 mb-4 mx-auto px-2">
<div class="md:max-w-7xl mt-4 mb-1 mx-auto px-0">
<img class="block mb-0" src="https://arc.stimg.co/startribunemedia/RR7FQ2VASWQXOAXE6VXWICEHV4.jpg?w=2000format=auto&compress&cs=tinysrgb" alt="photo">

</div>
<div class="md:flex">
<div class="mr-0 lg:w-1/2 md:w-full xs:w-full md:mr-1 xs:mr-0 xs:mb-5 md:mb-2">
<div class="bg-no-repeat bg-cover bg-center xl:h-[24rem] lg:h-[24rem] md:h-[24rem] mb-0 xs:h-[20rem]" style="background-image: url('https://arc.stimg.co/startribunemedia/V6FBUJA7BKM7RRUNDP7IPJZN5I.jpg?w=1200format=auto&compress&cs=tinysrgb');"></div>
</div>
<div class="md:ml-0 lg:w-1/2 md:w-full xs:w-full xs:ml-0">
<div class="bg-no-repeat bg-cover bg-center h-[28rem]xl:h-[24rem] lg:h-[24rem] md:h-[24rem] mb-0 xs:h-[20rem]" style="background-image: url('https://arc.stimg.co/startribunemedia/I6NRNGXWFDJHXZUIUKD6VREFPY.jpg?w=1200format=auto&compress&cs=tinysrgb');">
</div>
</div>

</div>
<div class="caption font-utility-meta-reg-02 text-tertiary text-center md:max-w-[660px] mx-auto xs:max-w-[100%] xs:min-w-[250px] !text-[14px] !leading-[1.25] pt-2">Red Lake players, from left, Randy Sayers Jr., Steve Rainey, Justin Brown, Cade Beaulieu and Brayden Beaulieu showed their frustration en route to a 54-20 loss.  Quarterback Cade Beaulieu displayed the ups and downs of the season, with a touchdown and then a painful breather on the field during halftime. &ldquo;That&rsquo;s the thing about Red Lake football,&rdquo; says Beaulieu, who is also a standout basketball player. &ldquo;No matter how bad we get beat, there&rsquo;s always hope we&rsquo;ll get a win the next week.&rdquo;</div>
</div>
  </GridRow>
  <GridRow variant={"inline"} additionalClasses={"gap-y-5"}>




<Paragraph>	At age 48, Desjarlait has been at it long enough to be coaching a second generation of Red Lake families, sons of fathers who played for him.	</Paragraph>
<Paragraph>	He wants players to enjoy football while embracing the physical nature of it. As an incentive, he once told the team that the player with the cleanest uniform at the end of road games would have to clean the inside of the bus after the ride home. One night, the kid who lost the contest realized it and immediately dropped and started rolling around in mud as the team huddled postgame. Desjarlait enjoyed his ingenuity so much that he cleaned the bus himself that night.	</Paragraph>
<Paragraph>	&ldquo;Coaching is having fun with kids and making them feel welcomed and wanting to be here,&rdquo; he says. &ldquo;My job is to keep them moving.&rdquo;	</Paragraph>
<Paragraph>	Coaching keeps him moving, too. The reminder to stay in motion is always resting on his chest, a pendant attached to a necklace he never takes off.	</Paragraph>
<Paragraph>	It holds a picture of Nolan Jr.	</Paragraph>


<StoryPause></StoryPause>



<Paragraph><span style="font-family: 'Graphik-Semibold'; text-transform: uppercase; font-size: 95%;">The tiny ballhandling wizard</span> was a dazzling halftime show, sinking three-pointer after three-pointer. &ldquo;M-V-P! M-V-P!&rdquo; the Crookston student section chanted. They loved the kid. Everyone did.</Paragraph>
<Paragraph>	Nicole and Nolan&rsquo;s only son seemed destined to be a star athlete. He always had a basketball in his hands, and he was always begging his dad to take him to the gym to shoot baskets. His parents made YouTube videos of his ballhandling routines, and he stole the show with those halftime performances at varsity games.	</Paragraph>
<Paragraph>	Kids his age looked up to him and followed him around. As a 9-year-old, Nolan Jr. put together a basketball team that entered tournaments across northern Minnesota. The Little Warriors won most of their games.	</Paragraph>
<Paragraph>	&ldquo;He was way beyond our skill level for our age,&rdquo; says senior quarterback Cade Beaulieu.	</Paragraph>
<Paragraph>	Nolan Jr. was sure to be Red Lake&rsquo;s starting quarterback, starting point guard and starting shortstop, then a college athlete. Everybody just knew it.	</Paragraph>



<!-- ONE UP -->
</GridRow>
<GridRow variant={"fullBleed"}>
<div class="md:max-w-7xl mt-8 mb-12 mx-auto px-2">
<img class="block mb-2" src="https://arc.stimg.co/startribunemedia/PKIWMGU3YNJ63T4NAMJ3DIRFSY.jpg?w=2000format=auto&compress&cs=tinysrgb" alt="photo">
<div class="caption font-utility-meta-reg-02 text-tertiary text-center md:max-w-[650px] mx-auto xs:max-w-[100%] xs:min-w-[250px] !text-[14px] !leading-[1.25] pt-2">Coach Desjarlait talked to senior Justin Brown during a home game. &rdquo;I don&rsquo;t know how many times throughout all these five years I wanted to quit,&rdquo; says Brown. &rsquo;I just can&rsquo;t. These are my brothers.&rdquo;</div>
</div>
</GridRow>
<GridRow variant={"inline"} additionalClasses={"gap-y-5"}>



<Paragraph>	He picked jersey No. 12 because that&rsquo;s the number his dad wore in high school. In his first youth league baseball game, Nolan Jr. made a sweet diving play at second base. It&rsquo;s a slow-motion replay in Desjarlait&rsquo;s memory.	</Paragraph>
<Paragraph>	&ldquo;He caught the ball, laid on his back and he threw the guy out,&rdquo; he says.	</Paragraph>
<Paragraph>	That was his son&rsquo;s final baseball game.	</Paragraph>
<Paragraph>	Days later, the family gathered at home to celebrate youngest child Skylar&rsquo;s second birthday. Nolan Jr. received permission to use an ATV to drive a bag of trash to a dumpster down the road. He lost control on the road and the ATV crashed, killing him. He was 10 years old.	</Paragraph>
<Paragraph>	The grief that enveloped his father and mother included moments of anger and regret for allowing their son to leave the yard that day. But they vowed to stick together and support each other by living a positive life for the sake of their marriage and their daughters.	</Paragraph>
<Paragraph>	After seeking guidance from reservation elders and spiritual advisers, they buried their son in their backyard. Desjarlait comes here often, to feel his son&rsquo;s presence.	</Paragraph>
<Paragraph>	A black bear cuts through their backyard occasionally, walking close by the grave site. This comforts Desjarlait, a member of the Ojibwe Bear Clan.	</Paragraph>
<Paragraph>	&ldquo;He&rsquo;s with us,&rdquo; he says.	</Paragraph>
<Paragraph>	Desjarlait wasn&rsquo;t sure he wanted to continue coaching after his son&rsquo;s death. He wasn&rsquo;t sure of much of anything. But he returned to work a few months later, and everything changed in a moment he can scarcely explain.	</Paragraph>
<Paragraph>	He arrived at school at his usual time to start sorting mail. He was alone in the office. The mail machine started running, which can only happen by pressing a button. No one had pressed the button.	</Paragraph>
<Paragraph>	<i>Son, is that you? Are you telling me something?</i> Desjarlait called out.	</Paragraph>
<Paragraph>	The machine stopped. An overhead light flickered. A moment later, the machine started running again.	</Paragraph>
<Paragraph>	&ldquo;It was a golden moment,&rdquo; he says.	</Paragraph>
<Paragraph>	Right then, Desjarlait promised himself and his son that he would keep moving, stay focused on what&rsquo;s in front of him.	</Paragraph>
<Paragraph>	&ldquo;What&rsquo;s in front of me is my kids, my family,&rdquo; he says. &ldquo;What&rsquo;s around me is other people&rsquo;s kids who look up to me to coach them.&rdquo;	</Paragraph>



 <!-- TWO UP -->
</GridRow>
<GridRow variant={"fullBleed"}>
<div class="md:max-w-7xl mt-8 mb-12 mx-auto px-2">
<div class="md:flex">
<div class="mr-0 lg:w-1/2 md:w-1/2 xs:w-full md:mr-1 xs:mr-0 xs:mb-5 md:mb-0">
<div class="bg-no-repeat bg-cover bg-center xl:h-[28rem] lg:h-[28rem] md:h-[28rem] mb-2 xs:h-100%" style="background-image: url('https://arc.stimg.co/startribunemedia/P6QAC7VD347JMSND3T5K6MIMO4.jpg?w=1200format=auto&compress&cs=tinysrgb');"></div>
</div>
<div class="md:ml-0 lg:w-1/2 md:w-1/2 xs:w-full xs:ml-0">
<div class="bg-no-repeat bg-cover bg-center xl:h-[28rem] lg:h-[28rem] md:h-[28rem] mb-2 xs:h-[15rem]" style="background-image: url('https://arc.stimg.co/startribunemedia/IYWYNCSRLONJZTHIGRG32QSCMA.jpg?w=1200format=auto&compress&cs=tinysrgb');"></div>

</div>
</div>
<div class="caption font-utility-meta-reg-02 text-tertiary text-center md:max-w-[650px] mx-auto xs:max-w-[100%] xs:min-w-[250px] !text-[14px] !leading-[1.25] pt-2">Coach Nolan Desjarlait was all-conference in three sports as a senior at Red Lake and went on to play two years of college baseball. But at age 48, he&rsquo;s still not quite ready to hang up his glove. After playing in an adult-league softball game in Bemidji, he sat with his daughters Aishja, 5, and Emerald, 6, and parents Leo Desjarlait Jr. and Ramona Desjarlait. At his office at the high school, the coach is also surrounded by photos and memorabilia of family and teams. And he always wears a pendant with a photo of Nolan Jr.</div>
</div>
</GridRow>
<GridRow variant={"inline"} additionalClasses={"gap-y-5"}>





<Paragraph>	Desjarlait takes comfort knowing his son&rsquo;s final resting place is steps away from the family&rsquo;s home. He points to a section of his property near the grave where he hopes to build a home for his daughters. Maybe two houses, so that the entire family can live together forever.	</Paragraph>
<Paragraph>	Their oldest child, Lexi, a Division III college basketball player who topped 2,000 points scoring in high school, is the only sibling who has memories of their brother. Skylar is now 9. Two daughters, Emerald, 6, and Aishja, 5, were born after Nolan Jr.&rsquo;s death.	</Paragraph>
<Paragraph>	The girls all want to wear No. 12 in sports.	</Paragraph>


<StoryPause></StoryPause>


<Paragraph><span style="font-family: 'Graphik-Semibold'; text-transform: uppercase; font-size: 95%;">The first practice of the season</span> starts at 3 p.m. Two carloads of players roll up a few minutes late, hustling over from a basketball camp.</Paragraph><Paragraph>	The first practice of the season starts at 3 p.m. Two carloads of players roll up a few minutes late, hustling over from a basketball camp.	</Paragraph>
<Paragraph>	Desjarlait fits players for their helmets. One needs help buckling his chin strap.	</Paragraph>
<Paragraph>	Sixteen players are here, 12 high-schoolers and four in middle school. The coaches expect attendance to increase as the season continues.	</Paragraph>
<Paragraph>	The sinewy Beaulieu, who has been the starting quarterback since eighth grade, is nursing a minor injury, so he can only watch. He&rsquo;s a standout basketball player who hopes to play in college.	</Paragraph>
<Paragraph>	Kingbird Jr. is 6-1 and one of the school&rsquo;s best athletes. He plays receiver and cornerback and is a skilled basketball player, too.	</Paragraph>
<Paragraph>	And there&rsquo;s Brown, a towering presence with long black hair. He plays multiple positions, occasionally even running back, and never fails to make teammates laugh.	</Paragraph>
<Paragraph>	Brown introduces himself as &ldquo;Slug,&rdquo; but with a twist.	</Paragraph>
<Paragraph>	&ldquo;Dollar sign-L-U-G,&rdquo; he says, laughing. He got the nickname in middle school. The dollar sign is his touch.	</Paragraph>
<Paragraph>	The first workout of the season is hard. Optimism abounds, though, as Desjarlait gathers his players for a huddle after the 45-minute session. Each kid gets an opportunity to say a few words. Everyone repeats the same message: great work today, bring a friend tomorrow.	</Paragraph>



<!-- THREE UP -->
  </GridRow>
  <GridRow variant={"fullBleed"}>
    <div class="md:max-w-7xl mt-8 mb-4 mx-auto px-2">
<div class="md:max-w-7xl mt-4 mb-1 mx-auto px-0">
<img class="block mb-0" src="https://arc.stimg.co/startribunemedia/TBBGXEVY4ZAKXW3AAV53J4UNLE.jpg?w=2000format=auto&compress&cs=tinysrgb" alt="photo">

</div>
<div class="md:flex">
<div class="mr-0 lg:w-1/2 md:w-full xs:w-full md:mr-1 xs:mr-0 xs:mb-5 md:mb-2">
<div class="bg-no-repeat bg-cover bg-center xl:h-[24rem] lg:h-[24rem] md:h-[24rem] mb-0 xs:h-[20rem]" style="background-image: url('https://arc.stimg.co/startribunemedia/M5VAWFBCJNUR4Y32LMGGKUMUR4.jpg?w=1200format=auto&compress&cs=tinysrgb');"></div>
</div>
<div class="md:ml-0 lg:w-1/2 md:w-full xs:w-full xs:ml-0">
<div class="bg-no-repeat bg-cover bg-center h-[28rem]xl:h-[24rem] lg:h-[24rem] md:h-[24rem] mb-0 xs:h-[20rem]" style="background-image: url('https://arc.stimg.co/startribunemedia/PE6IVWBE3FAFLKUHHUP3F7NXZM.jpg?w=1200format=auto&compress&cs=tinysrgb');">
</div>
</div>

</div>
<div class="caption font-utility-meta-reg-02 text-tertiary text-center md:max-w-[650px] mx-auto xs:max-w-[100%] xs:min-w-[250px] !text-[14px] !leading-[1.25] pt-2">Players made their way to the field the day before the season opener in August. In the fall, quarterback Cade Beaulieu warmed up in the parking lot near a teammate&rsquo;s pickup, which carried evidence of a successful whitetail hunt, and fans watched a middle-school game at Red Lake.</div>
</div>
  </GridRow>
  <GridRow variant={"inline"} additionalClasses={"gap-y-5"}>




<Paragraph>	Training camp flies by, never enough time to feel comfortable for the season opener. Desjarlait stops by the school cafeteria at 3 p.m. before the game to make himself a walking taco.	</Paragraph>
<Paragraph>	This is a big night: the first game in decades that the Warriors will play under lights at their home field. The school purchased stadium lights this year for the football and baseball fields. Desjarlait controls them with an app on his phone. He is thrilled that his players finally get to experience Friday Night Lights on their home field.	</Paragraph>
<Paragraph>	Red Lake opens against New York Mills, a Class 1A power that advanced to the state semifinals last season. The temperature is near 90 degrees, and Desjarlait worries about his players having to play both offense and defense.	</Paragraph>
<Paragraph>	The Warriors dress 18 players, including three middle-schoolers and a senior playing in his first football game. New York Mills brings 35.	</Paragraph>
<Paragraph>	Desjarlait huddles his players before they make the walk down a gravel road to the field. He is wearing a white T-shirt with a photo of Nolan Jr.&rsquo;s smiling face in the middle. The shirt has No. 12 on the back.	</Paragraph>
<Paragraph>	&ldquo;Who&rsquo;s nervous?&ldquo; he asks.	</Paragraph>
<Paragraph>	Nobody raises a hand.	</Paragraph>
<Paragraph>	&ldquo;Good,&rdquo; he says, &ldquo;I&rsquo;m glad you&rsquo;re not nervous. This is a clean slate.&rdquo;	</Paragraph>
<Paragraph>	New York Mills scores a touchdown on its first play, a 50-yard run. Red Lake fumbles the kickoff, New York Mills recovers and scores another touchdown. The score is 53-0 at halftime.	</Paragraph>
<Paragraph>	The Warriors keep battling and score a touchdown in the final minute. Their sideline erupts in cheers. The final score is 70-6 but the mood does not reflect it. The Warriors find simple joy in playing football. A touchdown or a diving tackle sends a euphoric jolt across their sideline. Teammates constantly encourage one another.	</Paragraph>
<Paragraph>	With New York Mills stretching its lead on another touchdown late in the first half, the team&rsquo;s biggest body and boldest personality stops as he walks back to the sideline and gazes at the horizon.	</Paragraph>
<Paragraph>	&ldquo;That&rsquo;s beautiful,&rdquo; Brown says.	</Paragraph>
<Paragraph>	The sun is setting over the top of the school in a magnificent orange glow. Brown motions to get the attention of a game official standing nearby.	</Paragraph>
<Paragraph>	&ldquo;That&rsquo;s beautiful,&rdquo; he repeats, pointing to the sky.	</Paragraph>
<Paragraph>	The official looks and nods his head.	</Paragraph>
<Paragraph>	Brown takes a few more seconds to savor it, then turns around and gets set for yet another kickoff.	</Paragraph>


<!-- ONE UP -->
</GridRow>
<GridRow variant={"fullBleed"}>
<div class="md:max-w-7xl mt-8 mb-12 mx-auto px-2">
<img class="block mb-2" src="https://arc.stimg.co/startribunemedia/OKOSUKBZFMGX6VUC775QXVZ2DE.jpg?w=2000format=auto&compress&cs=tinysrgb" alt="photo">
<div class="caption font-utility-meta-reg-02 text-tertiary text-center md:max-w-[650px] mx-auto xs:max-w-[100%] xs:min-w-[250px] !text-[14px] !leading-[1.25] pt-2">Red Lake players warmed up before their homecoming game in September. The Warriors lost three players to injuries and had to forfeit their next game, but they forged on with 16 players. The team continued to recruit classmates, ending workouts with: great work today, bring a friend tomorrow.</div>
</div>
</GridRow>
<GridRow variant={"inline"} additionalClasses={"gap-y-5"}>




<Paragraph>	In the postgame huddle, a player shouts, &ldquo;We&rsquo;ve got a good chance at a win this season!&ldquo; Teammates yell and high-five as they head back to the locker room.	</Paragraph>
<Paragraph>	&ldquo;That&rsquo;s the thing about Red Lake football,&rdquo; says Beaulieu, the captain. &ldquo;No matter how bad we get beat, there&rsquo;s always hope we&rsquo;ll get a win the next week.&rdquo;	</Paragraph>
<Paragraph>	Perseverance has become a hallmark of Red Lake, something opponents respect. Conference coaches voted Desjarlait Coach of the Year after his team went 0-8 a few seasons ago.	</Paragraph>
<Paragraph>	New York Mills coach Matt Radniecki tells his players to think about the commitment to teammates that Red Lake players exhibit.	</Paragraph>
<Paragraph>	&ldquo;It&rsquo;s not easy to jump on the field when you haven&rsquo;t had success,&rdquo; Radniecki says, &ldquo;but they had fun doing it.&rdquo;	</Paragraph>
<Paragraph>	Two weeks later, the Warriors remain optimistic as they prepare for a road game at Bagley. Hunting season on the reservation started this week and two players bagged deer. Players toss footballs in the parking lot outside the locker room as they wait for the team bus.	</Paragraph>
<Paragraph>	Nineteen players make this trip, including the most seniors they&rsquo;ve had in years: eight. Three young boys on a playground run to wave at the bus as it embarks on the 40-minute drive down Hwy. 1.	</Paragraph>
<Paragraph>	The bus is mostly quiet, except for a faint sound of &rsquo;90s music playing over the stereo system, but the locker room pregame buzzes with excitement. After coaches go over final strategy reminders, Beaulieu huddles teammates for a pep talk.	</Paragraph>
<Paragraph>	&ldquo;Nobody expects us to win!&ldquo; he shouts, reminding them that it&rsquo;s been a long time since the Warriors did just that.	</Paragraph>
<Paragraph>	Their competitive spirit is visible, but the Warriors are overmatched and outnumbered again. Bagley returns the opening kickoff for a touchdown, then scores repeatedly. The Warriors keep competing hard as Bagley inserts backups. Final score: 54-20.	</Paragraph>
<Paragraph>	In the postgame huddle, Desjarlait and his assistants encourage players to keep their heads up, keep battling. Each player gets a turn to say something, and each message is positive.	</Paragraph>
<Paragraph>	&ldquo;No matter what the score is, they come here to have fun,&rdquo; Desjarlait says as players walk to the locker room. &ldquo;I&rsquo;m just here to help them. It&rsquo;s life. We&rsquo;re always here for them regardless.&rdquo;	</Paragraph>
<Paragraph>	The team makes a pit stop at a convenience store to grab snacks for the ride home. Laughter fills the bus. Desjarlait sits in the front seat, staring out the front window into the darkness, always mindful that the next obstacle lurks.	</Paragraph>
<Paragraph>	That obstacle appears a few days later.	</Paragraph>
<Paragraph>	Homecoming festivities start with good news. Brown is named homecoming king and just in case anyone needs a reminder, he wears his crown as he leaves the locker room in uniform before the game.	</Paragraph>




<!-- THREE UP -->
  </GridRow>
  <GridRow variant={"fullBleed"}>
    <div class="md:max-w-7xl mt-8 mb-4 mx-auto px-2">
<div class="md:max-w-7xl mt-4 mb-1 mx-auto px-0">
<img class="block mb-0" src="https://arc.stimg.co/startribunemedia/BKFSYNFRAMNVLSSZI2RDZBJMYM.jpg?w=2000format=auto&compress&cs=tinysrgb" alt="photo">

</div>
<div class="md:flex">
<div class="mr-0 lg:w-1/2 md:w-full xs:w-full md:mr-1 xs:mr-0 xs:mb-5 md:mb-2">
<div class="bg-no-repeat bg-cover bg-center xl:h-[24rem] lg:h-[24rem] md:h-[24rem] mb-0 xs:h-[20rem]" style="background-image: url('https://arc.stimg.co/startribunemedia/YZLN4YF7BW5KTEITDHNYDJMPNY.jpg?w=1000format=auto&compress&cs=tinysrgb');"></div>
</div>
<div class="md:ml-0 lg:w-1/2 md:w-full xs:w-full xs:ml-0">
<div class="bg-no-repeat bg-cover bg-center h-[28rem]xl:h-[24rem] lg:h-[24rem] md:h-[24rem] mb-0 xs:h-[20rem]" style="background-image: url('https://arc.stimg.co/startribunemedia/NMHFWOUHDCT642J2IF3S2YUZJU.jpg?w=1000format=auto&compress&cs=tinysrgb');">
</div>
</div>

</div>
<div class="caption font-utility-meta-reg-02 text-tertiary text-center md:max-w-[650px] mx-auto xs:max-w-[100%] xs:min-w-[250px] !text-[14px] !leading-[1.25] pt-2">Life&rsquo;s scoreboard matters far more to coach Nolan Desjarlait than the one in the end zone, including memories made. Justin Brown, who plays multiple positions on the team, topped off his football uniform with a crown and a new title: homecoming king. Desjarlait marked Senior Night with roses for seniors like Brayden Beaulieu at halftime. And the players celebrated after the homecoming game with a dance in the school cafeteria, where Cade Beaulieu did the limbo with classmates. Although they lost both games, the Warriors found joy in football. &ldquo;No matter what the score is, they come here to have fun,&rdquo; Desjarlait said. &ldquo;I&rsquo;m just here to help them. It&rsquo;s life. We&rsquo;re always here for them regardless.&rdquo;</div>
</div>
  </GridRow>
  <GridRow variant={"inline"} additionalClasses={"gap-y-5"}>




<Paragraph>	But the loss to Wadena-Deer Creek puts their season in peril. Three players suffer injuries that require hospital visits. Beaulieu&rsquo;s case is the most serious, a concussion that requires further examination at a Bemidji hospital. A knee gash sidelines Kingbird Jr.	</Paragraph>
<Paragraph>	Desjarlait has no choice but to forfeit the next game. He is concerned the Warriors might not be able to finish the rest of the schedule. He worries about his players and exposing them to injury.	</Paragraph>
<Paragraph>	But his team wants to keep playing and with 16 players available, they forge on. Losses continue. The Warriors keep vowing to show up on Monday. They keep trying to recruit friends to join them.	</Paragraph>
<Paragraph>	&ldquo;They don&rsquo;t understand everything about it,&rdquo; Brown says of classmates. &ldquo;All they see is the score. But it&rsquo;s fun. Everyone on the team is my family.&rdquo;	</Paragraph>


<StoryPause></StoryPause>


<Paragraph>	<span style="font-family: 'Graphik-Semibold'; text-transform: uppercase; font-size: 95%;">Nicole attends as many games as possible,</span> but sometimes she has a hard time sitting in the stands because of all the reminders of her son. She finds inspiration watching her husband on the sideline, still pouring himself into these kids who need him.	</Paragraph>
<Paragraph>	&ldquo;Nolan is so loyal and kind and so calm,&rdquo; she says. &ldquo;He tells me we&rsquo;ve got to live for today and live for now, for the girls.&rdquo;	</Paragraph>
<Paragraph>	And for the boys.	</Paragraph>
<Paragraph>	These young men Desjarlait coaches on the field every day, the ones he rarely stops thinking about, the ones who will not quit on him: He has known them since they were young kids.	</Paragraph>
<Paragraph>	These faces staring back at him were his son&rsquo;s best friends. Their bond went deeper than friendship, deeper than being classmates and teammates. They considered themselves brothers.	</Paragraph>
<Paragraph>	They were young kids when Nolan Jr. died. Their hurt has not gone away.	</Paragraph>
<Paragraph>	&ldquo;Everything I do,&rdquo; Beaulieu says, &ldquo;I just try to go extra hard to make him proud.&rdquo;	</Paragraph>
<Paragraph>	Kingbird Jr. plans to wear uniform No. 12 in basketball, too.	</Paragraph>
<Paragraph>	&ldquo;I switched because this is his senior year,&rdquo; he says.	</Paragraph>
<Paragraph>	The loss of a child can send parents down different paths, searching for new purposes. Nicole ran for a seat on the school board and won. Nolan found his purpose in coaching. He deals with his pain privately while investing in kids in the most public way he knows. Head football coach, at the front of the room, in the center of the team huddle.	</Paragraph>
<Paragraph>	&ldquo;I&rsquo;m being as strong as I can for my nation and my family,&rdquo; he says.	</Paragraph>
<Paragraph>	Senior Night requires all of Desjarlait&rsquo;s focus. None of his players want to miss this, the regular-season finale.	</Paragraph>
<Paragraph>	Beaulieu is back from a concussion but moves to receiver as a precaution. Senior Josh Stillday has taken over at quarterback and performs admirably. Senior Gordon Thompson Jr. plays receiver one-handed since he has a broken finger that is covered with a splint.	</Paragraph>
<Paragraph>	The scoreboard isn&rsquo;t working, but the final score is irrelevant. Polk County West holds a decisive edge, but the Warriors and their cheering section celebrate when Brown scores the team&rsquo;s only touchdown in the game&rsquo;s final minute.	</Paragraph>



<!-- ONE UP -->
</GridRow>
<GridRow variant={"fullBleed"}>
<div class="md:max-w-7xl mt-8 mb-12 mx-auto px-2">
<img class="block mb-2" src="https://arc.stimg.co/startribunemedia/UKZNWPS5DYR4RG3WJU3MLCG3YY.jpg?w=2000format=auto&compress&cs=tinysrgb" alt="photo">
<div class="caption font-utility-meta-reg-02 text-tertiary text-center md:max-w-[650px] mx-auto xs:max-w-[100%] xs:min-w-[250px] !text-[14px] !leading-[1.25] pt-2">Coach Nolan Desjarlait closed the door, the last one out of the locker room after a September game. Red Lake's 0-9 season won&rsquo;t be remembered for wins and losses. It was played for Nolan Desjarlait Jr., who would have been a senior this year.</div>
</div>
</GridRow>
<GridRow variant={"inline"} additionalClasses={"gap-y-5"}>



<Paragraph>	The postgame huddle on the field has an air of finality, even though the Warriors are guaranteed one playoff game. (They will lose the following week.)	</Paragraph>
<Paragraph>	A school dance starts in an hour. Players are excited to get there. A few of them say their girlfriends want to stay until the last song. They are ready to hustle to the locker room but perform their favorite drill — Warrior Jacks — one final time.	</Paragraph>
<Paragraph>	Players gather in a circle and shout out each letter of their nickname — <i>W-A-R-R-I-O-R-S</i> — as they perform jumping jacks. They finish by yelling &ldquo;Warriors&ldquo; three times.	</Paragraph>
<Paragraph>	Their voices echo across the field, followed by a roar of teenagers making their way to the locker room.	</Paragraph>
<Paragraph>	Desjarlait will soon walk off the field alone. He will make a slow loop around the field in his SUV, loading water coolers and yard markers into the back. He will be the last one to leave the locker room, finishing his final chore by flicking off the new stadium lights from his phone.	</Paragraph>
<Paragraph>	Staying busy helps keep his emotions at bay. He figures everything will hit him at home later, when he has time to be still, when he visits that sacred place in the clearing overlooking the lake.	</Paragraph>
<Paragraph>	Stillday, the senior who took over at quarterback in a pinch, lingers on the field as the other players rush off into the cool, damp night. A layer of fog settles over the lights. Fans have gone home but he isn&rsquo;t ready to move on yet. He sits in the end zone, tears streaming down his cheeks.	</Paragraph>
<Paragraph>	Desjarlait kneels and pulls him close. The coach is misty-eyed as he thanks Stillday for being a leader and congratulates him on making straight A&rsquo;s and for not missing a single football practice.	</Paragraph>
<Paragraph>	&ldquo;I love being on this field,&rdquo; Stillday says. &ldquo;I wouldn&rsquo;t trade anything for this.&rdquo;	</Paragraph>
<Paragraph>	The record book will note for eternity that the Red Lake Warriors did not win this season. Their hearts tell them something different.	</Paragraph>
  </GridRow>








</Grid>

<style>
  a {
    text-decoration-line: underline;
    text-decoration-color: #00854b;
    text-underline-offset: 2px;
  }

  a:hover {
    color: #00854b;
  }
</style>

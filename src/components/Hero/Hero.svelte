<!--
@component
### Hero component 
Renders a visual replica of the Immersive Template hero. 

#### Optional properties
- sectionLabel: string;
- headline: string;
- timestamp: string;
- heroImageUrl: string;
- heroImageCaption: string;
- heroImageAltText: string;
- dek: string;
- authorName: string;
- authorBioUrl: string;
-->

<script>
  import Grid from "../Grid/Grid.svelte";
  import GridRow from "../Grid/_GridRow.svelte";
  import SectionLabel from "./_SectionLabel.svelte";
  import Headline from "./_Headline.svelte";
  import Timestamp from "./_Timestamp.svelte";
  import Image from "../Image/Image.svelte";
  import Dek from "./_Dek.svelte";
  import Byline from "./_Byline.svelte";

  /** @type {{sectionLabel?: string; headline?: string; timestamp?: string; heroImageUrl?: string; heroImageCaption?: string; heroImageAltText?: string; dek?: string; authorName?: string; authorBioUrl?: string;}} */
  let {
    sectionLabel = "yayaya",
    headline = "",
    timestamp = "",
    heroImageUrl = "",
    heroImageCaption = "",
    heroImageAltText = "",
    dek = "",
    authorName = "",
    authorBioUrl = "",
  } = $props();
</script>



<style>
div.byline {
  font-family: "Graphik";
}

div.dateline {
 letter-spacing: 3px;
}

div.subhead {
}

</style>


  <GridRow variant={"fullBleed"}>
<div class="md:flex xs:block mb-4">
  <div class="w-1/2 xs:w-full bg-black md:h-[95vh] md:min-h-[825px] xs:h-[525px] text-white">

  <h1 class="md:pt-[140px] xs:pt-[50px] md:text-[3.5rem] xs:text-[2.75rem] max-w-[440px] px-4 font-[publico-banner-light-italic] mx-auto text-center">The Red Lake Nation football team hasn't won a game in years, but its coach keeps his kids undefeated</h1>
      <div class="dateline mx-auto text-center uppercase !text-[12px] pt-3">December 2, 2022</div>



  <div class="byline mx-auto text-center pt-16 !text-[15px]">By <b>Chip Scoggins</b> Star Tribune</div>
  <div class="byline mx-auto text-center pt-1 !text-[15px]"> Photos by <b>Aaron Lavinksy</b> Star Tribune</div>

  


  
  
  </div>
  <div class="w-1/2 xs:w-full  bg-[url(https://ststatic.stimg.co/images/migrated-directus-images/redlake_sidehero.jpg)] bg-cover bg-right md:h-[95vh] md:min-h-[825px] xs:h-[140vw]"></div>
</div>

  <div class="subhead mx-auto font-[publico-text-roman] text-[1.75rem] max-w-[850px] text-center pt-12 pb-8 leading-[1.5]">They often play against opponents with twice as many players. Sometimes, coach Nolan Desjarlait wonders how he keeps doing it. The answer always comes: &ldquo;I refuse to give up on them.&rdquo;</div> 

</GridRow>

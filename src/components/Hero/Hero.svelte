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

<Grid additionalClasses="gap-y-8 md:gap-y-10">
  <GridRow>
    <div class="flex justify-center my-6">
      <SectionLabel>none</SectionLabel>
    </div>
    <div class="flex flex-col gap-y-6 md:gap-y-8 text-center">
      <Headline>{headline}</Headline>
      <Timestamp>{timestamp}</Timestamp>
    </div>
  </GridRow>

  {#if heroImageUrl}
    <GridRow variant={"fullBleed"}>
      <Image
        variant={"captionCentered"}
        src={heroImageUrl}
        alt={heroImageAltText}
        caption={heroImageCaption}
      />
    </GridRow>
  {/if}

  <GridRow
    additionalClasses="justify-self-center md:max-w-[535px] md:text-center lg:max-w-[712px]"
  >
    <div class="flex flex-col gap-y-5 md:justify-items-center md:items-center">
      <Dek>
        {dek}
      </Dek>
      <div class="flex items-center w-full gap-x-2 md:justify-center">
        <div class="flex flex-col gap-y-0.5 gap-x-1 md:flex-row">
          {#if authorName}
            <div class="flex">
              <Byline href={authorBioUrl}>By {authorName}</Byline>
            </div>
          {/if}

          <span class="text-text-secondary font-utility-label-reg-02">
            The Minnesota Star Tribune
          </span>
        </div>
      </div>
    </div>
  </GridRow>
</Grid>

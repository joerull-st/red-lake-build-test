<!-- 
@component
### story pause
recreating the story pause element of antiquity

-->

<script>
  /** @type {{children?: function}} */
  let { children } = $props();
</script>

<style>
.story-pause {
    margin: auto;
    min-width: 100%;
    padding: 40px 0;
}
.icons li {
    background: none repeat scroll 0 0 black;
    height: 7px;
    width: 7px;
    margin-right: 10px;
    vertical-align: top;
    border-radius: 50%;
    display: inline-block;
}
</style>

<div class="story-pause"> 

    <ul class="icons" style="
        margin: auto;
        width: 100%;
        text-align: center;
    ">
          <li></li>
          <li></li>
          <li></li>
        </ul>
    </div>
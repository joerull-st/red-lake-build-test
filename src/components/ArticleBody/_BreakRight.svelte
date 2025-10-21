<!-- 
    @component
    ### breaking out to the right
making an outbreaking map element    
    -->
    
    <script>
      /** @type {{children?: function}} */
      let { children } = $props();
    </script>
    
    <style>
    .dw-breakright {
        float:right;
    }
    </style>
    
    <div class="dw-breakright lg:max-w-[300px] lg:ml-auto lg:mr-[-120px] !xs:mx-auto !xs:w-full float-right"> 
        {@render children?.()}

        </div>
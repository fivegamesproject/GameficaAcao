<script setup>
    import HeaderItem from './HeaderItem.vue';
    import HeaderLogo from './HeaderLogo.vue';
    import HeaderAccount from './HeaderAccount.vue';
</script>


<template>
  <header>
    <div id="topNavigation">
        <div>
            <HeaderLogo />
        </div>

        <div class="headerEnd">
            <ul class="itemList">
                <HeaderItem item-name="Home" item-link="#" />
                <HeaderItem item-name="About Us" item-link="#" />
                <HeaderItem item-name="How it Works" item-link="#" />
                <HeaderItem item-name="Contact" item-link="#" />
            </ul>
       
            <HeaderAccount />
        </div>

    </div>
  </header>
</template>
  
  <style scoped>
    #topNavigation {
      width: 100%;
      max-width: 1110px;
      display: flex;
      flex-direction: row;
      justify-content: space-between;
    }
    
    .itemList{
      display: flex;
      flex-direction: row;
      gap: 15px;
    }
    
    .headerEnd{
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 50px;
    }

    header{
      padding-top: 20px;
    }

  
  </style>
  
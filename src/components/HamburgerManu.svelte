<script>
    let isHover = false;
    let isOpen = false; 
    function handleHover() { 
        isHover = true;
    }
    function handleMouseout() {
        isHover = false;
    }
    function  handleClick () {
        isOpen = !isOpen;
    }

</script>

<div class="menu {isOpen?"open":""}" on:mouseover={handleHover} on:mouseleave={handleMouseout} on:click={handleClick}>
    <span class="top">
        <div  class="{isHover? "active": ""}"></div>
    </span>
    <span class="middle"></span>
    <span class="bottom">
        <div class="{isHover? "active": ""}"></div>
    </span>
</div>

<style>
    div.menu {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        background-color: var(--dark-purple);
        transition: 300ms ease-out;
        position:absolute;
        margin-left: 100px;
        border-radius: 50%;
    }

    div.open { 
        padding: 150%;
    }

    span {
        width: 20px;
        height: 2px;
        background-color: white;
        margin-bottom: 4px;
    }

    span.top, span.bottom  { 
        position: relative;
    }

    span.top div, span.bottom div { 
        border: white solid 1px;
        width: 4px;
        height: 4px;
        position: absolute;
        display: inline-block;
        top: -2px;
        background-color: var(--dark-purple);
    }


    span.top div { 
        left: 0px;
        transition:  150ms;
    }

    span.top div.active { 
        left: 7px;
    }
    

    span.bottom div { 
        right: 0px;
        transition: right 150ms;
    }

    span.bottom div.active { 
        right: 7px;
    }

</style>
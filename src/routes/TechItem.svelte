<script>

export let linkTechImg;
export let nameLinkImg;
export let linkNav
function openLink(){
    window.open(linkNav)
}
</script>

{#if linkNav === ''}
<li class="tech__el" >
    <img src={linkTechImg} alt="Logo d'une technologie que j'utilise" class="tech__img">
    <p class="sect__txt">
        {nameLinkImg}
    </p>
</li>
{:else}
<li class="tech__el tech__el--big" on:click={openLink}>
    <img src={linkTechImg} alt="Logo d'une technologie que j'utilise" class="tech__img">
    <p class="sect__txt">
        {nameLinkImg}
    </p>
</li>
{/if}

<style>

.tech__el{
    width: 45%;
    height: 60px;
    display: flex;
    flex-direction: row;
    column-gap: 20px;
    color: #000;
    font-size: 18px;
    align-items: center;
    
}
.tech__el--big{
    width: 100%;
    cursor: pointer;
    transition: 0.6s;
    padding: 12px 20px;
    height: 80px;
}
.tech__el--big:hover{
    transition: 0.3s;
    transform: translateX(20px);
    color: #FFF3E1;
}
.tech__img{
    height: 100%;
    aspect-ratio: 1/1;
}
@media(min-width: 600px){
    .tech__el{
        width: 30%;
        font-size: 28px;
    }
    .tech__el--big{
    width: 48%;
}
}
</style>
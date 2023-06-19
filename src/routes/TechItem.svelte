<script>

export let linkTechImg;
export let nameLinkImg;

</script>

<li class="tech__el">
    <img src={linkTechImg} alt="Logo d'une technologie que j'utilise" class="tech__img">
    <p class="sect__txt">
        {nameLinkImg}
    </p>
</li>

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
.tech__img{
    height: 100%;
    aspect-ratio: 1/1;
}
@media(min-width: 600px){
    .tech__el{
        width: 30%;
        font-size: 28px;
    }
}
</style>